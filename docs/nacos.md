# Nacos学习

## 一、关于nacos配置加载

<font style="color:rgb(77, 77, 77);">如何去加载nacos中的配置文件:</font>

![](https://cdn.nlark.com/yuque/0/2024/png/43514497/1724320811389-98998e26-f6b6-441f-a9d5-ff1331dfd713.png)

---

```xml
//服务注册发现依赖，用于把本地服务注册到nacos的注册中心中
<spring-cloud-alibaba.version>2021.0.5.0</spring-cloud-alibaba.version>
<spring-cloud-starter-bootstrap.version>3.1.3</spring-cloud-starter-bootstrap.version>

            <dependency>
                <groupId>com.alibaba.cloud</groupId>
                <artifactId>spring-cloud-starter-alibaba-nacos-discovery</artifactId>
                <version>${spring-cloud-alibaba.version}</version>
            </dependency>
            <dependency>
                <groupId>com.alibaba.cloud</groupId>
                <artifactId>spring-cloud-starter-alibaba-nacos-config</artifactId>
                <version>${spring-cloud-alibaba.version}</version>
            </dependency>
             <!--由于2021版本去除了-bootstrap.yml支持、所以我们要加上去-->
            <dependency>
                <groupId>org.springframework.cloud</groupId>
                <artifactId>spring-cloud-starter-bootstrap</artifactId>
                <version>${spring-cloud-starter-bootstrap.version}</version>
            </dependency
              

<dependency>
  <groupId>com.alibaba.cloud</groupId>
  <artifactId>spring-cloud-starter-alibaba-nacos-discovery</artifactId>
</dependency>
<dependency>
  <groupId>com.alibaba.cloud</groupId>
  <artifactId>spring-cloud-starter-alibaba-nacos-config</artifactId>
</dependency>
<dependency>
  <groupId>org.springframework.cloud</groupId>
  <artifactId>spring-cloud-starter-bootstrap</artifactId>
</dependency>
```

---

## 二、配置文件的优先级

当使用对应的bootstrap进行配置的时候要注意对应的配置的优先级：<font style="color:#DF2A3F;">bootstrap.yml>application.properties>application.yml>外部文件</font>（多文件遵守properties>yml）

```yaml
spring:
  application:
    name: xcplus-content-api
  profiles:
    active: dev
  cloud:
    nacos:
      server-addr: 1.94.110.193:8848
      discovery:
        username: nacos
        password: nacos
      config:
        namespace: dev
        group: xcplus-content
        file-extension: yaml
        refresh-enabled: true
```

---

服务注册： 当服务启动的时候会把服务注册到 nacos 上具体规则是${spring.application.name}

```yaml
spring:
  application:
    name: xcplus-content-api   #注册服务名到nacos
  profiles:
    active: dev
  cloud:
    nacos:
      server-addr: 1.94.110.193:8848
      discovery:
        username: nacos
        password: nacos
    
```

---

## 三、配置管理

当服务启动的时候自动会拉去 nacos 上的配置具体规则

${spring.applcation.name}-${spring.profiles.active}-${spring.could.nacos.config.file-extension}

```yaml
spring:
  application:
    name: xcplus-content-api	#${spring.application.name}
  profiles:
    active: dev #${spring.profiles.active}
  cloud:
    nacos:
      server-addr: 1.94.110.193:8848
      config:
        namespace: dev
        group: xcplus-content
        file-extension: yaml  #${spring.could.nacos.config.file-extension}
        refresh-enabled: true
```

