# 面试怪圈聊天室
基于Websocket通讯的聊天室

## 项目介绍
匿名聊天室是一款基于websocket通讯的聊天室，每次进入聊天室后都会以一个非常优雅的名字和头像进入群聊。
你不知道我是谁，我也不知道你是谁，非常有趣！

以下是项目的两种张截图，可以点击[面试怪圈聊天室](http://139.155.78.177:7788)来体验。

该项目的前端为响应式编程，因此无论从手机端浏览器或者pc端浏览器甚至是微信、支付宝等打开，都能很好的兼容。

### 移动端效果：
![image](https://user-images.githubusercontent.com/7221514/138122312-1329f8fd-f4a5-4132-9b7c-6717875ff5e8.png)
### pc端效果：
![image](https://user-images.githubusercontent.com/7221514/138122623-22c100b9-59d8-4e51-b447-b52e79cdacb7.png)


## 技术架构
项目代码简单也非常易懂，特别适合新手入手，尤其是想对聊天室有基础的认识，并无从下手的同学，
### 技术选型
- 前端采用semantic+html+css+jquery开发
- 后端基于springboot开发

其中，semantic一个极易快速上手的前端架构封装，并且为响应式的。可以点击[官网](https://semantic-ui.com/)查看

### 性能&瓶颈
该项目的核心是消息的广播，并不存储消息的内容。因此，无磁盘IO的性能瓶颈，内存主要用于临时缓存接收并未广播的消息，因此1g的内存足以支持一定数量级的链接。
保守估计在1g2c的资源下：至少支持1000+的群聊客户端。


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

### Linux后台运行

- 使用maven命令`maven clean install`编译安装后，在target目录下找到以下jar包： 
r-chat-0.0.1-SNAPSHOT.jar
- 拷贝到目标服务器，输入以下命令启动：
```
nohup java -jar r-chat-0.0.1-SNAPSHOT.jar &
```
- 启动成功后，会看到和开发工具（IDEA/Eclipse）运行一样的启动成功日志

### 访问项目
浏览器输入:http://ip:7788即可访问


## 工程目录介绍
### 后端目录
![image](https://user-images.githubusercontent.com/7221514/138259846-529a932c-61b7-4df2-a37b-be6db8e16d59.png)
### 前端目录
![image](https://user-images.githubusercontent.com/7221514/138261874-2d34964a-1ce2-4c0d-9a42-d73309db4e55.png)


## 核心文件介绍

### RChatSocketServer.java
websocket服务端，封装了`onOpen`、`onClose`、`onMessage`、`onError`事件，用于接收建立链接、关闭链接、接收消息、错误事件。
针对不同的事件进行不同的事件处理器：
- onOpen事件处理
1. 为每一个链接初始化一个客户端对象
2. 将客户端对象维护在客户端管理器中
3. 对客户端推送一条「文明聊天」的系统消息事件
4. 广播「加入群聊」事件通知给所有客户端：xxx加入群聊
5. 广播「当前在线人数」事件给所有客户端

- onClose事件处理
1. 根据会话的Id获取当前退出的客户端对象
2. 广播「退出群聊」事件通知给所有客户端：xxx退出群聊
3. 从客户端管理器中移除客户端对象
4. 广播「当前在线人数」事件给所有客户端

- onMessage事件处理
1. 根据会话的Id获取当前退出的客户端对象
2. 将接收的客户端消息广播给所有的客户端

- onError事件处理
暂无

### CommunicationEvent.java
该类为客户端和服务端通讯的核心协议类，任何通讯都遵守该协议。主要有`type`和`data`两个重要属性：
- type为支持的协议类，该类型决定data的泛型的类型
type目前支持3中，可参考类`EnumCommunicationEventType`：
1. 普通消息  
即聊天过程的消息内容
2. 系统消息  
xxx加入群聊、xxx退出群聊、文明聊天提示等都属于这种类型。
3. 在线人数
该事件通知在线的人数，用于实时刷新客户端右上角的在线人数提醒。

- data为泛型，T由type决定，即事件的具体传输内容

### ClientManager.java
该类为客户端的管理器，由`onOpen`和`onClose`事件来添加和移除客户端对象，由此可以获知：在线人数就是该管理器中维护的客户端个数。
开发以下4个方法，用于管理客户端：
- addClient:添加客户端
- removeClient:移除客户端
- get:根据会话Id获取客户端对象
- getConnectedClients:获取当前在线的客户端对象


### ClientGenerator.java
该类是客户端生成器，是非常有趣的一个类。为每个链接的客户端提供不同的头像及名称，采用随机的方式生成。
可下载源码来查看。

### chat.js
该js文件200多行代码，完成前端所有交互，是前端的核心类，包括：
链接的建立
各种类型事件的处理
消息输入&发送的组件事件处理等




## 注意事项
在开发该项目也遇到一些问题和细节的处理与考虑，如下：
- 链接建立后偶发性自动断开链接
该问题在开发完整体验证后遇到的，非常难找到问题的根源，虽然最终没有弄清楚原因，但解决方案如下：
将发送消息的代码由`session.getAsyncRemote().sendText`修改为`session.getBasicRemote().sendText`

- 消息发送输入框的体验优化
进入界面焦点聚集在输入框，并且发送后，焦点仍然要聚焦再次
同时输入框增加回车发送事件，大大提升聊天体验

- 自动滚动消息
消息展示窗口，如果消息能够自动滚动，不仅便捷而且灵动

- 其他人的消息与我的消息分隔展示
广播会将消息推送给所有人包括自己的聊天窗口，为了区分哪个是自己发送的消息，可采用业界认可的左右分隔展示，更直观


## 扩展&优化
基于该项目可以做更多的扩展和优化，可以让聊天有有趣，比如：
- 支持表情
- 内置虚拟聊天机器人
- 支持单聊
- 支持随机聊天

以上是我的一些随想，扩展下让代码更风骚~

## 写在最后
该项目在哄小朋友睡着之后，历时4个小时，肝到下半夜两点完成，若有不足之处，可以留言反馈，谢谢~

## 以下是我
可爱猪猪（keaizhuzhu、Yesterday都是我）  
就职阿里、京东的码农  
发布面试小抄，全网下载量几千《java面试怪圈内卷手册》
[面试怪圈官网](http://www.mianshiguaiquan.com)上传了几百份程序员梦寐以求的各种学习资料  

![image](https://user-images.githubusercontent.com/7221514/138284864-68d1d89c-4c61-41bf-a24c-63d99a58a055.png) 

创办公众号「`面试怪圈`」，可在公众号中回复“交个朋友”加我好友，一起交流和改进：  

![image](https://user-images.githubusercontent.com/7221514/138284178-c496aa5b-5987-4569-b593-ee978cd8597a.png)






