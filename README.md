myth  
================
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/d0dd634df7854d27add47fcfaea0e9d5)](https://www.codacy.com/app/yu199195/myth?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=yu199195/myth&amp;utm_campaign=Badge_Grade)
[![Total lines](https://tokei.rs/b1/github/yu199195/myth?category=lines)](https://github.com/yu199195/myth)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg?label=license)](https://github.com/yu199195/myth/blob/master/LICENSE)
[![Maven Central](https://img.shields.io/maven-central/v/org.dromara/myth.svg?label=maven%20central)](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22org.dromara%22%20AND%20myth)
[![Javadocs](http://www.javadoc.io/badge/org.dromara/myth.svg)](http://www.javadoc.io/doc/org.dromara/myth)
[![Build Status](https://travis-ci.org/yu199195/myth.svg?branch=master)](https://travis-ci.org/yu199195/myth)
[![QQ群](https://img.shields.io/badge/chat-on%20QQ-ff69b4.svg?style=flat-square)](https://shang.qq.com/wpa/qunwpa?idkey=2e9e353fa10924812bc58c10ab46de0ca6bef80e34168bccde275f7ca0cafd85)
#####  采用消息队列解决分布式事务的开源框架, 基于java语言来开发（JDK1.8），支持dubbo，springcloud,motan等rpc框架进行分布式事务。

#  Features

  * ##### 天然无缝集成 spring-boot-starter 。
  
  * ##### RPC框架支持 : dubbo,motan,springcloud。

  * ##### 消息中间件支持 : jms(activimq),amqp(rabbitmq),kafka,roceketmq。

  * ##### 本地事务存储支持 : redis,mogondb,zookeeper,file,mysql。

  * ##### 事务日志序列化支持 ：java，hessian，kryo，protostuff。

  * ##### 采用Aspect AOP 切面思想与Spring无缝集成，天然支持集群,高可用,高并发。

  * #####  配置简单，集成简单，源码简洁，稳定性高，已在生产环境使用。

  * ##### 内置经典的分布式事务场景demo工程，并有swagger-ui可视化界面可以快速体验。


#  源码解析

  * ## https://juejin.im/post/5a5c63986fb9a01cb64ec517 
  
 ```
 ` myth-annotation` myth分布式事务框架注解(如 @myth注解),业务层主要通过该注解标记来实现分布式事务功能，dubbo, motan等rpc框架需要依赖此工程，为公共基础工程。

`myth-common ` 一个公共项目，里面主要是一些配置，枚举，异常定义等。
`myth-core` 该项目是myth框架的核心实现，包括服务的启动，调用流程，aop切面，重试机制等实现。

`myth-rpc` 该项目是对主流rpc框架的支持，包括dubbo、motan、springcloud。
`myth-dubbo` 该项目是对dubbo框架的支持，里面主要针对dubbo的特性的实现。

`myth-springcloud` 该项目是对springcloud框架的支持，里面主要针对springcloud的特性的实现。
`myth-motan` 该项目是对motan框架的支持，里面主要针对motan的特性的实现。

`myth-brpc` 未完待续。。。
`myth-grpc` 未完待续。。。
`myth-mq `，主要对主流MQ系列框架的支持，包括activeMq, kafka, rabbitmq, rocketmq 。
`myth-jms` 该项目是对消息中间件activemq的支持，里面主要针对activemq的特性的实现。
`myth-kafka `该项目是对消息中间件kafka的支持，里面主要针对kafka的特性的实现。
`myth-rabbitmq` 该项目是对消息中间件rabbitmq的支持，里面主要针对rabbitmq的特性的实现。
`myth-rocketmq` 该项目是对消息中间件rocketmq的支持，里面主要针对rocketmq的特性的实现。
`myth-demo `这是实战体验的demo项目，里面有针对dubbo用户、motan用户、springcloud用户的案列，里面具体的配置，用户可以参考 myth-demo-dubbo、 myth-`demo-springcloud` 以及 myth-demo-motan 。
`myth-dashboard `该项目是分布式事务管理后台的前端源码，采用vue.js + element UI 实现
`myth-admin` 该项目是分布式事务的跟踪管理后台（调用链跟踪，控制补偿事务等功能）
```

  
#  视频详解

  * ## 环境搭建以及运行 : http://www.iqiyi.com/w_19rw5zuigl.html
  * ## 原理讲解（1）：http://www.iqiyi.com/w_19rw5ztpkh.html
  * ## 原理讲解（2）：http://www.iqiyi.com/w_19rw5zslm1.html
  


# Prerequisite

  *   #### JDK 1.8+

  *   #### Maven 3.2.x

  *   #### Git

  *   ####  RPC framework dubbo or motan or springcloud。

  *   #### Message Oriented Middleware


# Quick Start

* #### Clone & Build
   ```
   > git clone https://github.com/yu199195/myth.git

   > cd myth

   > mvn -DskipTests clean install -U
   ```

* #### execute this sql       
 https://github.com/yu199195/myth/tree/master/myth-demo/sql/myth-mysql-demo.sql

* #### Find the RPC framework that works for you
 https://github.com/yu199195/myth/tree/master/myth-demo


* ## [Dubbo Quick Start](https://github.com/yu199195/myth/wiki/Dubbo-Quick-Start)

* ##  [SpringCloud Quick Start](https://github.com/yu199195/myth/wiki/SpringCloud--Quick-Start)

* ##  [Motan Quick Start](https://github.com/yu199195/myth/wiki/Motan-Quick-Start)

# Configuration

* ####  [配置详解](https://github.com/yu199195/myth/wiki/Configuration)

# User Guide

* #### 关于jar包引用问题，现在jar包还未上传到maven的中央仓库，所以使用者需要自行获取代码，然后打包上传到自己maven私服

   ```
   > git clone https://github.com/yu199195/myth.git

   > mvn -DskipTests clean deploy -U
   ```
* #### 关于jar包版本问题 ，现在因为没有传到中央仓库，如果引用的话，请自行设置相应的版本。


*  ## [Dubbo User Guide](https://github.com/yu199195/myth/wiki/Dubbo-User-Guide)

*  ## [Motan User Guide](https://github.com/yu199195/myth/wiki/Motan-User-Guide)

*  ## [SpringCloud User Guide](https://github.com/yu199195/myth/wiki/SpringCloud-User-Guide)

# FAQ

* ### 为什么我下载的代码后，用idea打开没有相应的get set 方法呢？
   ##### 答：因为框架使用了Lombok包，它是在编译的时期，自动生成get set方法，并不影响运行，如果觉得提示错误难受，请自行下载lombok包插件，[lombok官网](http://projectlombok.org/)

* ### 为什么我运行demo工程，找不到applicationContent.xml呢？
  ##### 答：请设置项目的资源文件夹。
  
* ### 为什么我启动myth-admin项目的时候，会报mongo 集群连接错误呢？
  ##### 答：这是因为项目里面有mongo代码，spring boot会自动配置，该错误没有关系，只要admin项目能正常启动就行。

# Support

 * ###  如有任何问题欢迎加入QQ群进行讨论
 
   ![](https://yu199195.github.io/images/qq.png)
   
   
 * ###  微信公众号
   ![](https://yu199195.github.io/images/public.jpg)

# Contribution
