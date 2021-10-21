# 面试怪圈匿名聊天室
基于Websocket通讯的匿名聊天室

## 项目介绍
匿名聊天室是一款基于websocket通讯的匿名聊天室，每次进入聊天室后都会以一个非常优雅的名字和头像进入群聊。

你不知道我是谁，我也不知道你是谁，非常有趣！

以下是项目的两种张截图，可以点击[面试怪圈匿名聊天室](http://139.155.78.177:7788)来体验。

该项目的前端为响应式编程，因此无论从手机端浏览器或者pc端浏览器甚至是微信、支付宝等打开，都能很好的兼容。

### 移动端效果：
![image](https://user-images.githubusercontent.com/7221514/138122312-1329f8fd-f4a5-4132-9b7c-6717875ff5e8.png)
### pc端效果：
![image](https://user-images.githubusercontent.com/7221514/138122623-22c100b9-59d8-4e51-b447-b52e79cdacb7.png)


## 技术架构
项目代码简单也非常易懂，特别适合新手入手，尤其是想对聊天室有基础的认识，并无从下手的同学，
该项目：
- 前端采用semantic+html+css+jquery开发
- 后端基于springboot开发

其中，semantic一个极易快速上手的前端架构封装，并且为响应式的。可以点击[官网](https://semantic-ui.com/)查看

## 功能介绍
该聊天室功能简约，上手急速：
- 基本功能为群聊，并且匿名
- 每次刷新都以新的身份进入，即新的头像和名称
- 右上角显示当前在线的人数，可以体现聊天的热度
- 聊天内容0存储，只有客户端展示。真正做到私密聊天。
- 响应式前端编程，兼容一切客户端。
- 「加入群聊」、「退出群聊」通知，了解对方的在线状态。

## 环境配置
- JDK8+的运行环境
- WINDOWS/LINUX操作系统
- MAVEN
- 无需存储

## 运行项目
### 开发工具（IDEA/Eclipse）运行
- 将项目拉取到本地后，使用使用MAVEN命令进行编译安装(安装过程确保网络畅通)
```
maven clean install
```
- 项目中找到`RChatApplication.java`，在开发工具中找到main函数即可启动，启动成功后，日志如下：
```

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v2.5.5)

2021-10-20 23:46:03.325  INFO 20605 --- [           main] com.msgqer.rchat.RChatApplication        : Starting RChatApplication using Java 1.8.0_181 on keaizhuzhudeAir with PID 20605 (/Users/xieyu/git/r-chat/target/classes started by keaizhuzhu in /Users/xieyu/git/r-chat)
2021-10-20 23:46:03.335  INFO 20605 --- [           main] com.msgqer.rchat.RChatApplication        : No active profile set, falling back to default profiles: default
2021-10-20 23:46:06.942  INFO 20605 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 7788 (http)
2021-10-20 23:46:06.990  INFO 20605 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2021-10-20 23:46:06.990  INFO 20605 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.53]
2021-10-20 23:46:07.211  INFO 20605 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2021-10-20 23:46:07.211  INFO 20605 --- [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 3714 ms
2021-10-20 23:46:08.048  INFO 20605 --- [           main] o.s.b.a.w.s.WelcomePageHandlerMapping    : Adding welcome page template: index
2021-10-20 23:46:08.311  WARN 20605 --- [           main] org.thymeleaf.templatemode.TemplateMode  : [THYMELEAF][main] Template Mode 'LEGACYHTML5' is deprecated. Using Template Mode 'HTML' instead.
2021-10-20 23:46:08.557  INFO 20605 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 7788 (http) with context path ''
2021-10-20 23:46:08.578  INFO 20605 --- [           main] com.msgqer.rchat.RChatApplication        : Started RChatApplication in 7.323 seconds (JVM running for 9.671)

```


## 工程目录介绍
### 后端目录
![image](https://user-images.githubusercontent.com/7221514/138259846-529a932c-61b7-4df2-a37b-be6db8e16d59.png)
### 前端目录
![image](https://user-images.githubusercontent.com/7221514/138261874-2d34964a-1ce2-4c0d-9a42-d73309db4e55.png)

                 



                        
                   





