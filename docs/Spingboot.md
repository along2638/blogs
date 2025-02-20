### spring 创建 bean 常见的八种方式：
1.xml+<bean/>

2.xml:context+注解(@Component+4个@Bean)3.配置类+扫描+注解(@Component+4个@Bean)

_**@Bean定义FactoryBean接口**_

_**@ImportResource**_

_**@Configuration注解的proxyBeanMethods属性**_

4.@Import导入bean的类@Import导入配置类

5.AnnotationConfigApplicationContext调用register方法 6.@Import导入ImportSelector 接口

7.@Import导入ImportBeanDefinitionRegistrar 接口

8.@Import导入BeanDefinitionRegistryPostProcessor 接口

### <font style="color:rgb(44, 44, 54);">HttpServletRequest</font>
<font style="color:rgb(44, 44, 54);">在Servlet中，可以通过</font>`<font style="color:rgb(44, 44, 54);">HttpServletRequest</font>`<font style="color:rgb(44, 44, 54);">对象来获取客户端的IP地址。通常使用</font>`<font style="color:rgb(44, 44, 54);">getRemoteAddr()</font>`<font style="color:rgb(44, 44, 54);">方法来直接获取客户端的IP地址。此外，还可以从HTTP请求头中查找</font>`<font style="color:rgb(44, 44, 54);">X-Forwarded-For</font>`<font style="color:rgb(44, 44, 54);">或</font>`<font style="color:rgb(44, 44, 54);">X-Real-IP</font>`<font style="color:rgb(44, 44, 54);">等字段，因为这些字段可能会包含经过代理服务器或负载均衡器的真实客户端IP地址。</font>

```java
protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
    String clientIp = request.getRemoteAddr(); // 获取客户端IP地址

    // 检查是否有代理服务器或负载均衡器设置的头部
    String forwardedFor = request.getHeader("X-Forwarded-For");
    if (forwardedFor != null && forwardedFor.length() > 0) {
        clientIp = forwardedFor.split(",")[0]; // 取第一个IP作为客户端IP
    }

    String realIp = request.getHeader("X-Real-IP");
    if (realIp != null && realIp.length() > 0) {
        clientIp = realIp; // 如果存在X-Real-IP，则取这个IP
    }

    // 输出客户端IP地址
    System.out.println("Client IP: " + clientIp);
    // 进一步处理...
}
```

1. **<font style="color:rgb(44, 44, 54);">注意安全性和准确性</font>**<font style="color:rgb(44, 44, 54);">： 使用</font>`<font style="color:rgb(44, 44, 54);">X-Forwarded-For</font>`<font style="color:rgb(44, 44, 54);">或</font>`<font style="color:rgb(44, 44, 54);">X-Real-IP</font>`<font style="color:rgb(44, 44, 54);">等请求头来获取客户端IP地址时，需要注意这些字段可能被恶意修改或伪造。因此，在涉及安全敏感操作时，应谨慎使用这些字段，并考虑使用可信的代理服务器或负载均衡器提供的信息。</font>
2. **<font style="color:rgb(44, 44, 54);">IPv6支持</font>**<font style="color:rgb(44, 44, 54);">： 如果客户端使用IPv6连接，则</font>`<font style="color:rgb(44, 44, 54);">getRemoteAddr()</font>`<font style="color:rgb(44, 44, 54);">返回的可能是IPv6地址。在这种情况下，需要额外处理IPv6地址。</font>

#### <font style="color:rgb(44, 44, 54);">示例代码</font>
<font style="color:rgb(44, 44, 54);">以下是一个简单的Servlet示例，演示如何获取客户端IP地址：</font>

```java
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import java.io.IOException;
import java.io.PrintWriter;

@WebServlet("/client-ip")
public class ClientIpServlet extends HttpServlet {

    @Override
    protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        String clientIp = request.getRemoteAddr(); // 获取客户端IP地址

        // 检查是否有代理服务器或负载均衡器设置的头部
        String forwardedFor = request.getHeader("X-Forwarded-For");
        if (forwardedFor != null && forwardedFor.length() > 0) {
            clientIp = forwardedFor.split(",")[0]; // 取第一个IP作为客户端IP
        }

        String realIp = request.getHeader("X-Real-IP");
        if (realIp != null && realIp.length() > 0) {
            clientIp = realIp; // 如果存在X-Real-IP，则取这个IP
        }

        // 输出客户端IP地址
        PrintWriter out = response.getWriter();
        out.println("<html><body>");
        out.println("<h1>Client IP: " + clientIp + "</h1>");
        out.println("</body></html>");
    }
}
```

##### springboot3 集成 mybatisplus 问题
[https://blog.csdn.net/siaok/article/details/141941040](https://blog.csdn.net/siaok/article/details/141941040)

```xml
<!-- https://mvnrepository.com/artifact/com.baomidou/mybatis-plus-spring-boot3-starter -->
<dependency>
  <groupId>com.baomidou</groupId>
  <artifactId>mybatis-plus-spring-boot3-starter</artifactId>
  <version>3.5.5</version>
</dependency>

```

---

### ResponseBodyAdvice
参考：

[Spring Boot——统一功能处理_springboot 统一响应处理器-CSDN博客](https://blog.csdn.net/2202_76097976/article/details/144052096)

```java
@ControllerAdvice
public class ResponseAdvice implements ResponseBodyAdvice {
    @Override
    public boolean supports(MethodParameter returnType, Class converterType) {
        return true;// false：不处理  true：处理
    }
 
    @Override
    public Object beforeBodyWrite(Object body, MethodParameter returnType, MediaType selectedContentType, Class selectedConverterType, ServerHttpRequest request, ServerHttpResponse response) {
        return Result.success(body);
    }
}
```



:::info
在 ResponseBodyAdvice 的 beforeBodyWrite 方法中，传递的参数提供了关于响应体及其上下文的详细信息。这些参数可以帮助你更灵活地处理和修改响应体。下面是对每个参数的详细介绍：

:::

参数说明

**Object body：**

+ 用途：这是控制器方法返回的实际响应体对象。
+ 示例：如果控制器方法返回一个 String 或 Map，那么 body 就是这个 String 或 Map 对象。

**MethodParameter returnType：**

+ 用途：表示控制器方法的返回类型。
+ 示例：如果你有一个控制器方法返回 String，那么 returnType 将包含该方法的返回类型信息。

常用方法：

getGenericParameterType()：获取方法的泛型返回类型。

getParameterType()：获取方法的具体返回类型。

getMethod()：获取方法的 java.lang.reflect.Method 对象。

hasMethodAnnotation(Class<? extends Annotation> annotationType)：检查方法是否带有指定的注解。

**MediaType selectedContentType：**

+ 用途：表示客户端请求的或服务器选择的内容类型（MIME 类型）。
+ 示例：如果客户端请求的是 JSON 格式的数据，那么 selectedContentType 可能是 application/json。

常用方法：

getType()：获取内容类型的主类型（如 application）。

getSubtype()：获取内容类型的子类型（如 json）。

toString()：获取完整的 MIME 类型字符串（如 application/json）。

Class<? extends HttpMessageConverter<?>> selectedConverterType：

用途：表示 Spring 选择用于将响应体转换为 HTTP 响应格式的消息转换器类型。

示例：如果响应体是 JSON 格式，那么 selectedConverterType 可能是 MappingJackson2HttpMessageConverter。

常用方法：通常不需要直接使用这个类的方法，但它可以帮助你了解 Spring 选择了哪种消息转换器来处理响应体。

**ServerHttpRequest request：**

+ 用途：表示当前的 HTTP 请求。
+ 示例：你可以通过 request 获取请求头、请求参数等信息。

常用方法：

getHeaders()：获取请求头。

getMethodValue()：获取请求方法（如 GET、POST）。

getURI()：获取请求 URI。

getQueryParams()：获取查询参数。

**ServerHttpResponse response：**

+ 用途：表示当前的 HTTP 响应。
+ 示例：你可以通过 response 设置响应头、状态码等信息。

常用方法：

setStatusCode(HttpStatus status)：设置响应状态码。

getHeaders()：获取响应头。

getStatusCode()：获取响应状态码。

---

