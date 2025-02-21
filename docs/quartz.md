# 前言
<font style="color:rgb(77, 77, 77);">参考网站：</font>

[Spring boot整合quartz方法_springboot quartz-CSDN博客](https://blog.csdn.net/In23754/article/details/144282719)

[Quartz任务调度.pdf](https://www.yuque.com/attachments/yuque/0/2025/pdf/43514497/1739928271948-4553e00c-9625-487e-983f-a857158a39d8.pdf)

---

<font style="color:rgb(77, 77, 77);">JobDetail绑定指定的Job，每次Scheduler调度执行一个Job的时候，首先会拿到对应的Job，然后创建该Job实例，再去执行Job中的execute()的内容，任务执行结束后，关联的Job对象实例会被释放，且会被JVM GC清除。</font>

<font style="color:rgb(77, 77, 77);">为什么设计成JobDetail + Job，不直接使用Job?</font>

:::tips
<font style="color:rgb(77, 77, 77);">JobDetail定义的是任务数据，而真正的执行逻辑是在Job中。</font>

<font style="color:rgb(77, 77, 77);">这是因为任务是有可能并发执行，如果Scheduler直接使用Job，就会存在对同一个Job实例并发访问的问题。而JobDetail & Job 方式，Sheduler每次执行，都会根据JobDetail创建一个新的Job实例，这样就可以规避并发访问的问题。</font>

:::

---

# <font style="color:rgb(79, 79, 79);">Quartz引入依赖</font>
<font style="color:rgb(77, 77, 77);">首先，要在Springboot项目可以直接引入下面依赖</font>

```java
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-quartz</artifactId>
        </dependency>
```

## 1.创建所需实体类
### 1.1任务实体类
创建任务实体类方便方法以及接口入参

```java
/**
 * 添加作业
 *
 * @author zfl
 * @date 2025/02/17
 */

@ApiModel(description = "添加作业")
@Data
public class JobInfo {
   @ApiModelProperty(value = "任务名称" ,required = true,example = "job1")
   private String jobName;
   @ApiModelProperty(value = "Corn表达式",required = true,example = "0/5 * * * * ?")
   private String cron;
   @ApiModelProperty(value = "获取任务类型地址",required = true,example = "com.example.quartz.HelloJob")
   private String jobClassName;
   @ApiModelProperty(value = "获取调度器名称",required = true,example = "job1")
   private String triggerName;
}
```

### 1.2 任务详细信息实体类
方便查询所有定时任务的相关信息

```java

/**
 * 作业详细信息
 *
 * @author zfl
 * @date 2025/02/17
 */
@ApiModel(description = "作业详细信息")
@Data
@AllArgsConstructor
@NoArgsConstructor
public class JobDetailInfo {
    @ApiModelProperty("任务名称")
    private String jobName;
    @ApiModelProperty("组名称")
    private String groupName;
    @ApiModelProperty("trigger触发器名称")
    private String triggerName;
    @ApiModelProperty("trigger触发器类型")
    private String triggerType;
    @ApiModelProperty("cron表达式")
    private String cronExpression;
    @ApiModelProperty("下一次触发时间")
    private String nextFireTime;
    @ApiModelProperty("状态")
    private String state;

}

```

## 2.创建对应方法接口并重写方法
```java
package com.example.quartz.service;

import com.example.config.ResultResponse;
import com.example.quartz.jobinfo.JobDetailInfo;
import org.quartz.SchedulerException;

import java.util.List;

/**
 * Quartz服务
 *
 * @author zfl
 * @date 2025/02/17
 */

public interface QuartzService {

    /**
     * 选择职务信息
     *
     * @return 结果响应
     * @author zfl
     */
    public List<JobDetailInfo> selectJobInfo() throws SchedulerException;

    /**
     * 添加cron作业
     *
     * @param jobName      作业名称
     * @param cron         cron
     * @param jobClassName 作业类名称
     * @param triggerName  触发器名称
     * @return 结果响应
     * @author zfl
     */
    public ResultResponse addCronJob(String jobName, String cron, String jobClassName, String triggerName);

    /**
     * 更新cron作业
     *
     * @param jobName     作业名称
     * @param cron        cron
     * @param triggerName 触发器名称
     * @return 结果响应
     * @author zfl
     */
    public ResultResponse updateCronJob(String jobName,String cron, String triggerName);

    /**
     * 暂停cron作业
     *
     * @param jobName     作业名称
     * @param triggerName 触发器名称
     * @return 结果响应
     * @author zfl
     */
    public ResultResponse pauseCronJob(String jobName, String triggerName);

    /**
     * 恢复cron作业
     *
     * @param jobName     作业名称
     * @param triggerName 触发器名称
     * @return 结果响应
     * @author zfl
     */
    public ResultResponse resumeCronJob(String jobName, String triggerName);

    /**
     * 删除cron作业
     *
     * @param jobName     作业名称
     * @param triggerName 触发器名称
     * @return 结果响应
     * @author zfl
     */
    public ResultResponse removeCronJob(String jobName,String triggerName);
}

```

---

```java

/**
 * quart服务impl
 *
 * @author zfl
 * @date 2025/02/17
 */
@Service
public class QuartServiceImpl implements QuartzService {
    @Resource
    private Scheduler scheduler;
    private static final String DEFAULT_JOB_GROUP = "default_job_group";

    private static final String DEFAULT_TRIGGER_GROUP = "default_trigger_group";

    private static final String TRIGGER_PRE = "Trigger_";


    @Override
    public List<JobDetailInfo> selectJobInfo() throws SchedulerException {
        List<JobDetailInfo> jobDetails = new ArrayList<>();

        Set<JobKey> jobKeys = scheduler.getJobKeys(GroupMatcher.anyJobGroup());

        for (JobKey jobKey : jobKeys) {
            List<? extends Trigger> triggers = scheduler.getTriggersOfJob(jobKey);
            for (Trigger trigger : triggers) {
                Trigger.TriggerState triggerState = scheduler.getTriggerState(trigger.getKey());

                String cronExpression = "";
                if (trigger instanceof CronTrigger) {
                    cronExpression = ((CronTrigger) trigger).getCronExpression();
                }

                JobDetailInfo jobDetailInfo = new JobDetailInfo(
                        jobKey.getName(),
                        jobKey.getGroup(),
                        trigger.getKey().getName(),
                        trigger.getClass().getSimpleName(),
                        cronExpression,
                        trigger.getNextFireTime() != null ? trigger.getNextFireTime().toString() : "N/A",
                        triggerState.name()
                );

                jobDetails.add(jobDetailInfo);
            }
        }
        return jobDetails;
    }

    @Override
    public ResultResponse addCronJob(String jobName, String cron, String jobClassName, String triggerName) {
        try {
            JobKey jobKey = JobKey.jobKey(jobName, DEFAULT_JOB_GROUP);
            if (scheduler.checkExists(jobKey)) {
                return ResultResponse.error("【添加定时任务】该作业已存在");
            }
            //构建job
            JobDetail job = (JobDetail) JobBuilder
                    .newJob((Class<? extends Job>) Class.forName(jobClassName))
                    .withIdentity(jobKey)
                    .build();
            //Cron表达式定时构造器
            CronScheduleBuilder cronSchedule = CronScheduleBuilder.cronSchedule(cron);
            //构建Trigger
            Trigger trigger = TriggerBuilder.newTrigger()
                    .withIdentity(TriggerKey.triggerKey(TRIGGER_PRE + triggerName, DEFAULT_TRIGGER_GROUP))
                    .withSchedule(cronSchedule)
                    .build();
            //启动调度
            scheduler.scheduleJob(job, trigger);
            scheduler.start();
        } catch (Exception e) {
            return ResultResponse.error("创建定任务失败，原因是：" + e.getMessage());
        }
        return ResultResponse.success(jobName + "创建定时任务成功！");

    }

    @Override
    public ResultResponse updateCronJob(String jobName, String cron, String triggerName) {
        try {
            TriggerKey triggerKey = TriggerKey.triggerKey(TRIGGER_PRE + triggerName, DEFAULT_TRIGGER_GROUP);
            CronScheduleBuilder cronSchedule = CronScheduleBuilder.cronSchedule(cron);
            CronTrigger trigger = (CronTrigger) scheduler.getTrigger(triggerKey);
            trigger = trigger.getTriggerBuilder().withIdentity(triggerKey).withSchedule(cronSchedule).build();
            scheduler.rescheduleJob(triggerKey, trigger);
            return ResultResponse.success("更新定时任务成功！");
        } catch (Exception e) {
            return ResultResponse.error("更新定时任务失败，原因为：" + e.getMessage());
        }
    }


    @Override
    public ResultResponse pauseCronJob(String jobName, String triggerName) {
        try {
            TriggerKey triggerKey = TriggerKey.triggerKey(TRIGGER_PRE + triggerName, DEFAULT_TRIGGER_GROUP);
            JobKey jobKey = JobKey.jobKey(jobName, DEFAULT_JOB_GROUP);

            // 检查作业和触发器是否存在
            if (!scheduler.checkExists(jobKey) || !scheduler.checkExists(triggerKey)) {
                return ResultResponse.error("作业或触发器不存在");
            }

            // 暂停触发器
            scheduler.pauseTrigger(triggerKey);
            return ResultResponse.success("暂停定时任务成功！");
        } catch (Exception e) {
            return ResultResponse.error("暂停定时任务失败，原因是：" + e.getMessage());
        }

    }

    @Override
    public ResultResponse resumeCronJob(String jobName, String triggerName) {
        try {
            // 构建触发器key
            TriggerKey triggerKey = TriggerKey.triggerKey(TRIGGER_PRE + triggerName, DEFAULT_TRIGGER_GROUP);
            // 恢复触发器
            scheduler.resumeTrigger(triggerKey);
            return ResultResponse.success("恢复定时任务成功！");
        } catch (Exception e) {
            return ResultResponse.error("恢复定时任务失败，原因是：" + e.getMessage());
        }
    }

    @Override
    public ResultResponse removeCronJob(String jobName,String triggerName) {
        try {
            JobKey jobKey = JobKey.jobKey(jobName, DEFAULT_JOB_GROUP);
            TriggerKey triggerKey = TriggerKey.triggerKey(TRIGGER_PRE + triggerName, DEFAULT_TRIGGER_GROUP);

            if (!scheduler.checkExists(jobKey) || !scheduler.checkExists(triggerKey)) {
                return ResultResponse.error("【删除定时任务】作业或触发器不存在");
            }

            scheduler.unscheduleJob(triggerKey);
            scheduler.deleteJob(jobKey);

            return ResultResponse.success(jobName + "删除定时任务成功！");
        } catch (Exception e) {
            return ResultResponse.error("删除定时任务失败，原因为：" + e.getMessage());
        }
    }
}

```

---

```java

/**
 * Quartz控制器
 *
 * @author zfl
 * @date 2025/01/23
 */
@Api(tags = "Quartz定时任务框架")
@RestController
@RequestMapping("/quartz")
public class QuartzController {
    @Resource
    private QuartzService quartzService;
    @ApiOperation("查看定时任务列表")
    @GetMapping("/selectJobInfo")
    public ResultResponse<List<JobDetailInfo>> selectJobInfo() throws SchedulerException {
        List<JobDetailInfo> jobDetailInfos = quartzService.selectJobInfo();
        return ResultResponse.success(jobDetailInfos);
    }
    @ApiOperation("创建定时任务")
    @PostMapping("/addQuartz")
    public ResultResponse addQuartz(@RequestBody JobInfo jobInfo) {
        final ResultResponse resultResponse = quartzService.addCronJob(jobInfo.getJobName(), jobInfo.getCron(), jobInfo.getJobClassName(), jobInfo.getTriggerName());
        return ResultResponse.success(resultResponse);
    }
    @ApiOperation("修改定时任务")
    @PostMapping("/updateJob")
    public ResultResponse updateJob(@RequestBody JobInfo jobInfo) {
        return quartzService.updateCronJob(jobInfo.getJobName(), jobInfo.getCron(), jobInfo.getTriggerName());
    }
    @ApiOperation("暂停定时任务")
    @PostMapping("/pauseJob")
    public ResultResponse pauseJob(@RequestBody JobInfo jobInfo) {
        return quartzService.pauseCronJob(jobInfo.getJobName(), jobInfo.getTriggerName());
    }
    @ApiOperation("恢复定时任务")
    @PostMapping("/resumeJob")
    public ResultResponse resumeJob(@RequestBody JobInfo jobInfo) {
        return quartzService.resumeCronJob(jobInfo.getJobName(), jobInfo.getTriggerName());
    }
    @ApiOperation("删除定时任务")
    @DeleteMapping("/removeCronJob")
    public ResultResponse removeCronJob(@RequestBody JobInfo jobInfo) {
        return quartzService.removeCronJob(jobInfo.getJobName(), jobInfo.getTriggerName());
    }
}

```

