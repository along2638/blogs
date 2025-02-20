1.官网：

[FastExcel - 让Excel处理更简单](https://idev.cn/fastexcel/zh-CN/)

### <font style="background-color:rgb(250, 250, 250);">概述</font>
<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">FastExcel 提供了一种简单的方式来读取 Excel 文件。用户只需定义一个 POJO 类来表示数据结构，然后通过 FastExcel 的监听器机制读取数据。</font>

```java
<dependency>
    <groupId>cn.idev.excel</groupId>
    <artifactId>fastexcel</artifactId>
    <version>1.0.0</version>
</dependency>
```



```java
/**
 * 工作
 *
 * @author zfl
 * @date 2025/02/12
 */
@ApiModel(description = "工作")
@Data
@TableName("upload_data")
@AllArgsConstructor
@NoArgsConstructor
public class UploadData {
    @TableId(value = "business_id", type = IdType.AUTO)
    @ApiModelProperty("任务ID")
    @ExcelProperty("任务ID")
    private String  businessId;
    @ExcelProperty("姓名")
    @ApiModelProperty("姓名")
    private String  name;
    @ExcelProperty("项目名称")
    @ApiModelProperty("项目名称")
    private String  projectName;
    @ExcelProperty("任务名称")
    @ApiModelProperty("任务名称")
    private String  businessName;
}

```

### <font style="background-color:rgb(250, 250, 250);">数据监听器：</font>
[AnalysisEventListener 与 ReadListener 的区别](https://idev.cn/fastexcel/zh-CN/docs/advance_api#%E5%8C%BA%E5%88%AB%E6%80%BB%E7%BB%93)

:::tips
_**<font style="color:#DF2A3F;">注意:监听器不能被 Spring 管理,每次读取 Excel 文件时需要重新实例化。</font>**_

:::

```java
/**
 * 上传数据监听器
 *
 * @author zfl
 * @date 2025/02/12
 */
@Slf4j
public class UploadDataListener extends AnalysisEventListener<UploadData> {

    private final ArrayList<UploadData> list=new ArrayList<>();

    @Override
    public void invoke(UploadData uploadData, AnalysisContext analysisContext) {
        log.info("读取数据:{}",uploadData);
        list.add(uploadData);
    }

    @Override
    public void doAfterAllAnalysed(AnalysisContext analysisContext) {
        log.info("所有数据解析状态:");
        UploadDataServiceImpl uploadDataService= new UploadDataServiceImpl();
        uploadDataService.saveBatch(list);
    }

}

```

## 读操作：
### 创建读取并下载数据接口
```java
/**
 * 快速excel控制器
 *
 * @author zfl
 * @date 2025/02/12
 */
@Slf4j
@Api(tags = "fastExcel学习")
@RestController
@RequestMapping("/excel")
public class FastExcelController {
    @PostMapping("/upload")
    public ResultResponse<String> upLoad(@RequestParam("file") MultipartFile file) {
        if (file.isEmpty()) {
            return ResultResponse.error("文件为空");
        }
        try {
            FastExcel.read(file.getInputStream(), UploadData.class, new UploadDataListener()).sheet().doRead();
            return ResultResponse.success("上传成功");


        } catch (IOException e) {
            log.info("文件读取失败");
            return ResultResponse.error("文件读取失败");
        }


    }
}
```

## 写操作
### 创建写入并下载 Excel 接口
```java
    @ApiOperation("数据导出excel")
    @GetMapping("/download")
    public void download(HttpServletResponse response) throws IOException {
        final List<UploadData> uploadDataList = uploadDataService.list();
        response.setContentType("application/vnd.openxmlformats-officedocument.spreadsheetml.sheet");
        response.setCharacterEncoding("utf-8");
        String fileName = URLEncoder.encode("测试", "UTF-8").replaceAll("\\+", "%20");
        response.setHeader("Content-disposition", "attachment;filename*=utf-8''" + fileName + ".xlsx");

        FastExcel.write(response.getOutputStream(), UploadData.class)
                .sheet("模板")
                .doWrite(uploadDataList);
    }
```

---

补充知识：

### <font style="color:rgb(44, 44, 54);">使用场景</font>
**<font style="color:rgb(44, 44, 54);">Web开发</font>**<font style="color:rgb(44, 44, 54);">：当需要通过网页上传或下载 Excel 文件时，这个 MIME 类型用于指定内容类型。例如，在设置 HTTP 响应头时，可以使用它来告知浏览器即将接收的是一个 Excel 文件。</font>

+ <font style="color:rgb(44, 44, 54);"> 示例（在 Java Servlet 中）：</font>

```java
response.setContentType("application/vnd.openxmlformats-officedocument.spreadsheetml.sheet");
response.setHeader("Content-Disposition", "attachment; filename=yourfile.xlsx");
```

+ **<font style="color:rgb(44, 44, 54);">文件上传</font>**<font style="color:rgb(44, 44, 54);">：在处理文件上传请求时，可以根据 </font>`<font style="color:rgb(44, 44, 54);">Content-Type</font>`<font style="color:rgb(44, 44, 54);"> 请求头判断上传的文件是否为 </font>`<font style="color:rgb(44, 44, 54);">.xlsx</font>`<font style="color:rgb(44, 44, 54);"> 格式的 Excel 文件。</font>
+ **<font style="color:rgb(44, 44, 54);">文档管理</font>**<font style="color:rgb(44, 44, 54);">：在需要对不同类型的文档进行分类管理的应用中，可以利用 MIME 类型区分不同的文件格式。</font>

### <font style="color:rgb(44, 44, 54);">相关信息</font>
+ <font style="color:rgb(44, 44, 54);">对于旧版 Excel 文件（如</font><font style="color:rgb(44, 44, 54);"> </font>`<font style="color:rgb(44, 44, 54);">.xls</font>`<font style="color:rgb(44, 44, 54);">），其对应的 MIME 类型是</font><font style="color:rgb(44, 44, 54);"> </font>`<font style="color:rgb(44, 44, 54);">application/vnd.ms-excel</font>`<font style="color:rgb(44, 44, 54);">。</font>
+ <font style="color:rgb(44, 44, 54);">使用这种 MIME 类型不仅可以帮助正确识别文件类型，还可以提高用户体验，比如直接提示用户下载而不是尝试在浏览器内打开不适合的内容。</font>

<font style="color:rgb(44, 44, 54);">了解和正确应用 MIME 类型对于确保文件在网络中的正确传输和处理至关重要。无论是在开发 Web 应用程序还是处理文件上传/下载功能时，准确地设置 MIME 类型都是必不可少的一步。</font>

---

## 常见问题(部分)
详细常见问题请查看：[https://idev.cn/fastexcel/zh-CN/docs/FAQ](https://idev.cn/fastexcel/zh-CN/docs/FAQ)

### <font style="background-color:rgb(250, 250, 250);">Lombok注解</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">使用FastExcel时，实体类中的Lombok注解有何作用？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 实体类中常用的Lombok注解如</font>`@Getter`、`@Setter`、`@EqualsAndHashCode`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">用于自动生成getter、setter方法及equals和hashCode方法。如果不想使用这些自动生成的方法，可以自行实现。</font>

### <font style="background-color:rgb(250, 250, 250);">字段匹配</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何解决部分字段无法正确读取或写入的问题？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 确保实体类字段遵循驼峰命名规则，避</font>免使用`@Accessors(chain = true)`，推荐使用`@Builder`替代。另外，确保实体类中使用了`@ExcelProperty`注解标记参与读写的字

### <font style="background-color:rgb(250, 250, 250);">并发读取</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">为何不能将Listener交给Spring管理？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> Listener不应被Spring管理，因为这会导致Listener变成单例模式，在并发读取文件时可能引发数据混淆问题。每次读取文件时应新建一个Listener实例</font>

### <font style="background-color:rgb(250, 250, 250);">字段映射</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何处理实体类字段与Excel列名不一致的情况？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以使用</font>`@ExcelProperty`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">注解来指定实体类字段与Excel列名的对应关系。例如：</font>

```java
@ExcelProperty("姓名")
private String name;
```

### <font style="background-color:rgb(250, 250, 250);">数据校验</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何在读取Excel数据时进行校验？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以在</font>`ReadListener`中<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">实现数据校验逻辑。例如：</font>

```java
public class DataValidatorListener extends AnalysisEventListener<DemoData> {
    @Override
    public void invoke(DemoData data, AnalysisContext context) {
        if (data.getName() == null || data.getName().isEmpty()) {
            throw new RuntimeException("姓名不能为空");
        }
        // 处理数据
    }
}
```

### <font style="background-color:rgb(250, 250, 250);">错误处理</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何处理读取过程中抛出的异常？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以在</font>`ReadListener`中<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">捕获并处理异常。例如：</font>

```java
public class ErrorHandlingListener extends AnalysisEventListener<DemoData> {
    @Override
    public void invoke(DemoData data, AnalysisContext context) {
        try {
            // 处理数据
        } catch (Exception e) {
            // 处理异常
        }
    }
}


@Slf4j
public class ExceptionHandlingListener implements ReadListener<DemoData> {
 
    @Override
    public void onException(Exception exception, AnalysisContext context) {
        log.error("解析异常: {}", exception.getMessage());
        if (exception instanceof ExcelDataConvertException) {
            ExcelDataConvertException ex = (ExcelDataConvertException) exception;
            log.error("第 {} 行, 第 {} 列解析错误，数据: {}",
                      ex.getRowIndex(),
                      ex.getColumnIndex(),
                      ex.getCellData());
        }
    }
 
    @Override
    public void invoke(DemoData data, AnalysisContext context) {}
 
    @Override
    public void doAfterAllAnalysed(AnalysisContext context) {}
}
```

### <font style="background-color:rgb(250, 250, 250);">多Sheet读取</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何读取包含多个Sheet的Excel文件？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以使用</font>`MultipleSheetsListener`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">来处理多Sheet的读取。例如：</font>

```java
FastExcel.read(file, MultipleSheetsData.class, new MultipleSheetsListener()).doReadAll();
```

<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">或者，可以在读取前获取所有Sheet的信息：</font>

```java
ExcelReader excelReader = FastExcel.read(file, MultipleSheetsData.class, multipleSheetsListener).build();
List<ReadSheet> sheets = excelReader.excelExecutor().sheetList();
for (ReadSheet readSheet : sheets) {
    excelReader.read(readSheet);
}
excelReader.finish();
```



### <font style="background-color:rgb(250, 250, 250);">获取Excel总行数</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何获取Excel文件的总行数？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以在监</font>听器中使用`analysisContext.readSheetHolder().getApproximateTotalRowNumber()`方法获取大致的行数。例如：

```java
@Override
public void doAfterAllAnalysed(AnalysisContext context) {
    int totalRows = context.readSheetHolder().getApproximateTotalRowNumber();
    System.out.println("总行数: " + totalRows);
}
```

### <font style="background-color:rgb(250, 250, 250);">自定义读取监听器</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何自定义读取监听器？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A: </font>**可以继承`AnalysisEventListener`类并实现自己的逻辑。例如：

```java
public class CustomReadListener extends AnalysisEventListener<DemoData> {
    @Override
    public void invoke(DemoData data, AnalysisContext context) {
        // 处理数据
    }
 
    @Override
    public void doAfterAllAnalysed(AnalysisContext context) {
        // 所有数据读取完成后执行的操作
    }
}
```

### <font style="background-color:rgb(250, 250, 250);">读取时忽略未标注的字段</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 如何在读取时忽略未标注</font>`@ExcelProperty`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">的字段？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 在类的最上面加入</font>`@ExcelIgnoreUnannotated`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">注解。例如：</font>

```java
@Data
@ExcelIgnoreUnannotated
public class DemoData {
    @ExcelProperty("姓名")
    private String name;
}
```

### <font style="background-color:rgb(250, 250, 250);">导出时设置单元格数据格式</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何在导出时设置单元格的数据格式？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以在实体类属性上使用</font>`@ContentStyle`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">注解来设置数据格式。例如：</font>

```java
@ExcelProperty("金额")
@ContentStyle(dataFormat = 4) // 4对应货币格式
private Double amount;
```

### <font style="background-color:rgb(250, 250, 250);">读取时处理空值</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何在读取时处理空值？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以在</font>`ReadListener`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">中处理空值。例如：</font>

```java
public class NullValueHandlerListener extends AnalysisEventListener<DemoData> {
    @Override
    public void invoke(DemoData data, AnalysisContext context) {
        if (data.getName() == null) {
            data.setName("默认值");
        }
        // 处理数据
    }
}
```

### <font style="background-color:rgb(250, 250, 250);">读取时过滤数据</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">Q:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> </font><font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">如何在读取时过滤数据？</font>
+ **<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">A:</font>**<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);"> 可以在</font>`ReadListener`<font style="color:rgb(51, 65, 85);background-color:rgb(250, 250, 250);">中实现过滤逻辑。例如：</font>

```java
public class DataFilterListener extends AnalysisEventListener<DemoData> {
    @Override
    public void invoke(DemoData data, AnalysisContext context) {
        if (data.getAmount() > 1000) {
            // 保存或处理数据
        }
    }
}
```

