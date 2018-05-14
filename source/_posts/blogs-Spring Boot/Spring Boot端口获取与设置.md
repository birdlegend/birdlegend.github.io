---
layout: deep
title: Spring Boot2.0端口获取与设置
date: 2018-05-07 21:11:02
tags:
- Spring Boot
- Config
categories:
- Spring Boot
---

## 参考文献
[Spring 2.0 doc](https://docs.spring.io/spring-boot/docs/current-SNAPSHOT/reference/htmlsingle/#production-ready-customizing-management-server-port)

## 端口设置
#### 配置方法
> Change the HTTP Port
In a standalone application, the main HTTP port defaults to 8080 but can be set with server.port (for example, in application.properties or as a System property). Thanks to relaxed binding of Environment values, you can also use SERVER_PORT (for example, as an OS environment variable).  
#### 关闭http端口但仍然创建WebApplicationContext
> To switch off the HTTP endpoints completely but still create a WebApplicationContext, use server.port=-1. (Doing so is sometimes useful for testing.)  
#### 随机端口
> To scan for a free port (using OS natives to prevent clashes) use server.port=0.


## 运行时端口获取
#### 测试类中
++ 只能在测试环境下使用 ++
```
@RunWith(SpringJUnit4ClassRunner.class)
@SpringBootTest(webEnvironment=WebEnvironment.RANDOM_PORT)
public class MyWebIntegrationTests {

	@Autowired
	ServletWebServerApplicationContext server;

	@LocalServerPort
	int port;

	// ...

}
```

#### 使用用ApplicationListener获取
> You can access the port the server is running on from log output or from the ServletWebServerApplicationContext through its WebServer. The best way to get that and be sure that it has been initialized is to add a @Bean of type ApplicationListener<ServletWebServerInitializedEvent> and pull the container out of the event when it is published.

```
import org.springframework.boot.web.servlet.context.ServletWebServerInitializedEvent;
import org.springframework.context.ApplicationListener;
import org.springframework.stereotype.Component;

/**
 * Created by zsb on 2018/5/11.
 */
@Component
public class PtpApplicationListener implements ApplicationListener<ServletWebServerInitializedEvent> {
    private int port;

    @Override
    public void onApplicationEvent(ServletWebServerInitializedEvent event) {
        port = event.getApplicationContext().getWebServer().getPort();
        System.out.println("port::" + port);
    }
}
```
