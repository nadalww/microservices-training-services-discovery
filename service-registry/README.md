## 使用Ribbon 客户端负载均衡

**Part 1, 运行Eureka Server和CategoryService

1.  启动EurekaServer

2.  启动两个CategoryService实例
  - run it by Gradle
    SERVER_PORT=9090 gradle bootRun
    SERVER_PORT=9191 gradle bootRun
  - run it by Jar file
    SERVER_PORT=9090 java -jar xxxxx.jar 
    SERVER_PORT=9191 java -jar xxxxx.jar 

3. 检查Eureka Server，查看注册的Category service

**Part 2, 使用FeignClient实现EventService

1. 打开EventService项目

2. 使用FeingClient调用Category Service

3. 运行EventService，
	- SERVER_PORT=9292 gradle bootRun
	- SERVER_PORT=9292 java -jar xxxxx.jar 

4. 访问localhost:9292/category