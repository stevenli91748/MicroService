**微服务架构设计的首要任务就是合理划分微服务，即围绕业务功能创建微服务项目。在划分微服务时，有关微服务粗细粒度的考量，建议在平台创建的初始阶段使用粗粒度的方法，按业务功能进行划分。随着业务的发展及其运营的情况，再依据发展规模考虑是否继续细分。下面，我们将使用水平划分法和垂直划分法两种方法相结合的方式创建微服务**

**一方面在水平方向上**：

**根据业务功能划分微服务，并把这次划分所创建的微服务称为REST API微服务。REST API微服务负责业务功能的行为设计，主要完成数据管理方面的工作，并通过使用REST协议，对外提供接口服务。**

**另一方面在垂直方向上**：

**再以REST API微服务为基础，实现前后端分离设计，创建Web UI微服务。Web UI微服务不直接访问数据，它只专注于人机交互界面的设计，它的数据存取将通过调用REST API微服务来完成。这样，经过两次微服务划分，我们就可以创建出REST API和Web UI两种类型的微服务。也就是说，我们只要使用两种类型的微服务，就可以构建一个复杂的业务系统。**

**使用REST API和Web UI微服务，结合高性能和高并发的设计，再通过微服务的多副本发布，就可以构建一个能适应任何规模访问的、多维的、稳定牢固的网格结构，并且这个网格结构还具有自由伸缩的特性，可以根据业务的发展规模进行扩充或者缩编，这样就可以快速地搭建一个可持续扩展的系统平台**


# [MicroService 面试](https://github.com/stevenli91748/MicroService/blob/master/interview.md)

# 一个微服务的例子

<a href="https://ibb.co/3pm6X2T"><img src="https://i.ibb.co/x1q9vW2/image.png" alt="image" border="0"></a>

# [15种微服务架构框架汇总](http://dockerone.com/article/9892)
# [Top 10 Microservices frameworks for 2020](https://medium.com/microservices-architecture/top-10-microservices-framework-for-2020-eefb5e66d1a2)
# [基于SpringCloud微服务系统设计,5万字总结！](https://segmentfault.com/a/1190000039889988)
# [微服务的设计模式](https://www.kubernetes.org.cn/9532.html)
# [SpringBoot+CQRS微服务设计模式教程 ](https://www.jdon.com/55380)
# [一张图看懂微服务架构路线](https://www.kubernetes.org.cn/9711.html)

# 在线书籍
* [微服务治理：体系，架构， 实践---2020](https://weread.qq.com/web/reader/69e327a071eeeee269e177e)
* [微服务架构基础（Spring Boot + Spring Cloud + Docker）---将编程开发，持续集成，部署运维等环节都讲到，照着本书可搭建一套运行环境，构建一个demo](https://weread.qq.com/web/reader/69532da0717d3026695636ekc81322c012c81e728d9d180)
* [微服务分布式架构基础与实战： 基于Spring Boot + Spring Cloud](https://weread.qq.com/web/reader/f6732e8071dbddd6f674178)
* [Spring Cloud微服务架构进阶---讲得非常详细](https://weread.qq.com/web/reader/c9932ea07163ff6ac993e0dkc81322c012c81e728d9d180)
* [Spring Cloud微服务架构实战---2020](https://weread.qq.com/web/reader/ca932ea071d7c798ca9a714)
* [Spring Cloud Alibaba微服务原理与实战---2020](https://weread.qq.com/web/reader/0f132410811e3ac57g011a6akc81322c012c81e728d9d180)
* [大型企业微服务架构实践与运营---2019](https://weread.qq.com/web/reader/49b325d0717d34aa49b0645)
* [名师讲坛： JAVA微服务架构实战（SpringBoot + SpringCloud + Docker + RabbitMQ）---2020 李兴华](https://weread.qq.com/web/reader/0e03209071c96a420e02710)
* [微服务实战：Dubbox+Spring Boot+Docker](https://weread.qq.com/web/reader/6dc322d072052f1d6dcce13kc81322c012c81e728d9d180)
* [Spring微服务架构设计---2020](https://weread.qq.com/web/reader/9de32c5071db56e39decfc8)
* [Kubernetes微服务实战---2020](https://weread.qq.com/web/reader/f1c32df071eeef5bf1cc214)
* [分布式微服务架构： 原理与实战---2019](https://weread.qq.com/web/reader/01b3264071a4952901b85ab)
* [微服务分布式架构开发实战](https://weread.qq.com/web/reader/d19329f0715a41a7d19438bkc81322c012c81e728d9d180)
---

# [微服务例子](https://github.com/stevenli91748/MicroService/blob/master/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E4%BE%8B%E5%AD%90/README.md)

---

[Service Mesh微服务](https://github.com/stevenli91748/MicroService/blob/master/Service%20Mesh/README.md)|
---|

# 目录

### 1 微服务架构设计---微服务的关注点在能力分治，将同类型的能力聚集在一个应用中，做到功能解耦，分别演化。这里涉及到两个点：微服务内部组件间如何调用 & 微服务整体如何对外提供服务。成熟方案是通过微服务框架（如SpringCloud）的功能组件完成，如前者属于服务治理和发现（Eureka），后者通过网关（gateway）
  * [ 微服务领域驱动设计](https://weread.qq.com/web/reader/d9e327a07188b377d9eb7dakc7432af0210c74d97b01b1c)
  * 服务治理
    * [注册中心的设计与实现](https://github.com/aCoder2013/blog/issues/32) 
    * [微服务分布式配置中心组件](https://github.com/stevenli91748/MicroService/blob/master/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E5%88%86%E5%B8%83%E5%BC%8F%E9%85%8D%E7%BD%AE%E4%B8%AD%E5%BF%83%E7%BB%84%E4%BB%B6/README.md) 
    * 服务调用
    * 服务容错 
    * [服务网关](https://github.com/stevenli91748/MicroService/tree/master/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E7%BD%91%E5%85%B3)
    * 链路追踪
  * 微服务应用安全——Security
  * 微服务之分布式事务解决方案
    * [Seata 分布式事务](https://github.com/stevenli91748/JAVA-Architecture/blob/master/JAVA%20Framework/Spring%20Cloud/Spring%20Cloud%20Alibaba%E5%A5%97%E4%BB%B6/Seata.md)
    * [亿级流量架构之分布式事务思路及方法](https://www.cnblogs.com/Courage129/p/14433462.html)
    * [亿级流量架构之分布式事务解决方案对比](https://www.cnblogs.com/Courage129/p/14443653.html) 
    * [微服务分布式事务之LCN、TCC特点、事务补偿机制缘由以及设计重点](https://www.cnblogs.com/Courage129/p/14528981.html)
    * [微服务下如何保证事务的一致性](https://weread.qq.com/web/reader/d9e327a07188b377d9eb7dake3632bd0222e369853df322)
      * Apache RocketMQ--RocketMQ事务消息中间件主要解决了生产者端的消息发送与本地事务执行的原子性问题
  * Rest API微服务设计   ------Spring Cloud与Docker高并发微服务架构设计实施 
  * WebUI API微服务设计
  * 微服务之间调用规则设计
  * 数据最终一致性设计
  * 分布式集群架构设计
  * 微服务运行环境安全设计 
 ### 2 微服务设计 
  * [微服务设计和高并发实践](https://weread.qq.com/web/reader/2fe329c071e041322feb53dk33e3289021c33e75ff09694)
  * [高并发微服务架构设计](https://weread.qq.com/web/reader/ca932ea071d7c798ca9a714k70e32fb021170efdf2eca12)
    *  自然的压力分解
    *  可弹性伸缩的集群环境
    *  高度的独立性设计
    *  API的分层调用关系
    *  高可用的基础资源支持
    *  快速响应的自动化基础设施
    *  完善的监控体系
    *  微服务的安全保障
  * [大型电商平台微服务设计入门案例](https://weread.qq.com/web/reader/ca932ea071d7c798ca9a714k33e3289021c33e75ff09694)  
### [3 微服务架构方案](https://github.com/stevenli91748/MicroService/blob/master/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%9E%B6%E6%9E%84%E6%96%B9%E6%A1%88/README.md)
  * [1 基于Spring Cloud的微服务架构方案    ](https://icyfenix.cn/exploration/projects/microservice_arch_springcloud.html)
  * [2 基于Kubernetes的微服务架构方案 ](https://icyfenix.cn/exploration/projects/microservice_arch_kubernetes.html)
  * [3 基于服务网格：Istio的微服务架构方案 ](https://icyfenix.cn/exploration/projects/servicemesh_arch_istio.html)
  * [4 基于无服务：AWS Lambda的微服务架构方案 ](https://icyfenix.cn/exploration/projects/serverless_arch.html)

---

## 微服务架构的关键问题
   * 1 微服务架构的通信机制---微服务架构包括微服务外部通信和微服务内部通信， 对于通信方式来说，有些程序对实时数据很敏感，只能使用接口的方式进行实时调用；而有的程序对实时数据并没有太多要求，但是通信量很大，这时就可以使用异步消息进行调用。在微服务架构模式中，你将使用两种不同类型的通信，**同步通信以及异步通信。同步通信是指服务之间通过 HTTP 或 GRPC 相互调用。异步通信意味着服务通过消息总线或事件总线相互交互，这意味着服务之间没有直接连接**
       * [微服务系统实践--远程过程调用](https://weread.qq.com/web/reader/2fe329c071e041322feb53dk02e32f0021b02e74f10ece8) 
       * [微服务外部通信的架构方案---有很多实现微服务外部通信的方式。最通用最流行的三个方式是](#微服务外部通信的架构方案)
         * [1 API REST-based](#1-API-REST-based微服务架构方案实现方式)
           * [API的分层调用关系](https://weread.qq.com/web/reader/ca932ea071d7c798ca9a714kb6d32b90216b6d767d2f0dc) 
         * [2 applicaiton REST-based](#2-applicaiton-REST-based微服务架构方案实现方式)
         * [3 中心化的消息](#3-中心化的消息微服务架构方案实现方式)
       * [微服务内部通信的架构方案](#微服务内部通信的架构方案)
         * [1 基于HTTP协议的同步机制（REST、RPC）](#1-基于HTTP协议的同步机制)
           * [Dubbo](https://github.com/stevenli91748/MicroService/blob/master/Dubbo/README.md)
         * [2 基于消息队列的异步消息处理机制（AMQP-based message broker）](#2-基于消息队列的异步消息处理机制)
           * [kafka](https://github.com/stevenli91748/Message-Server-System/tree/master/Kafka)
           * [RabbitMQ]()
       * [微服务通信的设计模式](https://blog.51cto.com/u_13609606/3118362)
         * [微服务架构的进程间通信(RPC)](https://blog.51cto.com/u_15064630/3612514) 
         * [微服务架构中的进程间通信](https://blog.51cto.com/u_3664660/3213999)
         * [微服务优化之使用gRPC做微服务的内部通信](https://blog.51cto.com/u_15127584/2782244)
       * [微服务之间最佳调用方式是什么](https://blog.51cto.com/u_15127651/2895828)
       * 微服务之间的通信的方式
         * Feign
         * [RestTemplate ](https://github.com/stevenli91748/MicroService/blob/master/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E4%B9%8B%E9%97%B4%E7%9A%84%E9%80%9A%E4%BF%A1%E7%9A%84%E6%96%B9%E5%BC%8F/README.md)
         * [OpenFeign](https://www.jianshu.com/p/7d45185ae7f1) 
   * 2 分布式数据管理
       * 处理读请求
       * 处理更新请求
   * [3 微服务稳定性保证的常用手段](https://weread.qq.com/web/reader/d9e327a07188b377d9eb7dak341323f021e34173cb3824c)
   * [4 微服务下如何保证事务的一致性](https://weread.qq.com/web/reader/d9e327a07188b377d9eb7dake3632bd0222e369853df322)
   * [5 微服务编排](https://weread.qq.com/web/reader/d9e327a07188b377d9eb7dak17e328b022b17e62166fad4)

## 微服务外部通信的架构方案

客户端可以向micro service发起RESTful HTTP请求，但是会有这种情况发生：客户端为了完成一个业务逻辑，需要发起多个HTTP请求，从而造成系统的吞吐率下降，再加上无线网络的延迟高，会严重影响客户端的用户体验，为了解决这个问题，一般会在服务器集群前面再加一个角色：API gateway，由它负责与客户度对接，并将客户端的请求转化成对内部服务的一系列调用。这样做还有个好处是，服务升级不会影响到客户端，只需要修改API gateway即可

### 1 API REST-based微服务架构方案实现方式

适合网站提供小规模的，自包含的服务。很多互联网网站都提供这样的服务，比如OAuth2服务

<a href="https://ibb.co/1q2sk47"><img src="https://i.ibb.co/7Wygq0j/api-rest-based.png" alt="api-rest-based" border="0"></a>

### 2 applicaiton REST-based微服务架构方案实现方式

不同于上面的架构，客户端看到的是web界面或者富客户端程序，而不是调用API。UI层独立发布，可以访问服务组件

<a href="https://ibb.co/bdzPcPK"><img src="https://i.ibb.co/cTD141r/application-rest-base.png" alt="application-rest-base" border="0"></a>

### 3 中心化的消息微服务架构方案实现方式

它类似前面的模式，但是使用一个轻量级的消息broker取代RESTful的服务调用。这个轻量级的broker不会执行服务的编排，传输和路由，这和SOA不同，不要把它看作SOA的简化版

<a href="https://ibb.co/g6KPRcT"><img src="https://i.ibb.co/XVR3CGs/image.png" alt="image" border="0"></a>


## 微服务内部通信的架构方案

   内部服务之间的通信方式有两种：基于HTTP协议的同步机制（REST、RPC）；基于消息队列的异步消息处理机制（AMQP-based message broker）

### 1 基于HTTP协议的同步机制


### 2 基于消息队列的异步消息处理机制


###  微服务架构解决方案：
    SpringCloud，是一套生态，就是解决以上分布架构的4个问题, 想使用SpringCloud，必须掌握SpringBoot，因为SpringCloud是基于SpringBoot；

     1. Spring Cloud Netflix，出来了一套解决方案:
     
        Api网关，zuul组件
        Feign--->HttpClient--->HTTP的通信方式，同步并阻塞
        服务注册与发现，Eureka
        熔断机制，Hystrix

        2018年年底，Netflix宣布无限期停止维护。生态不再维护，就会脱节。

    2. Apache Dubbo zookeeper，第二套解决系统
        Api：没有！要么找第三方插件，要么自己实现
        Dubbo是一个高性能的基于Java实现的，RPC通信框架！
        服务注册与发现，zookeeper：动物园管理者（Hadoop，Hive）
        没有：借助了Hystrix

        不完善，Dubbo

    3. SpringCloud Alibaba 一站式解决方案	
    
### 当前各大IT公司用的微服务架构有那些？

         阿里：dubbo+HFS

         京东：JFS

         新浪：Motan

         当当网：DubboX  

### Dubbo 和 SpringCloud对比:

**最大区别：Spring Cloud 抛弃了Dubbo的RPC通信，采用的是基于HTTP的REST方式**

item|Dubbo |Spring Cloud|
---|---|---|
服务注册中心|	Zookeeper|	Spring Cloud Netfilx Eureka|
服务调用方式|	RPC|	REST API|
服务监控|	Dubbo-monitor|	Spring Boot Admin|
断路器|	不完善|	Spring Cloud Netfilx Hystrix|
服务网关|	无|	Spring Cloud Netfilx Zuul|
分布式配置|	无|	Spring Cloud Config|
服务跟踪|	无|	Spring Cloud Sleuth|
消息总栈|	无|	Spring Cloud Bus|
数据流|	无	|Spring Cloud Stream|
批量任务|	无|	Spring Cloud Task|

[Java架构：一文读懂微服务架构的重构策略](https://developer.51cto.com/art/201905/597080.htm)|[微服务架构经验和教训](http://www.ityouknow.com/springcloud/2017/10/19/micro-service-practice.html)|
---|---|

[阿里架构师教你：如何快速搭建一个微服务架构](https://www.bilibili.com/video/BV1n4411K7yb/?spm_id_from=333.788.videocard.10)|[耦合到底意味着什么呢](https://zhuanlan.zhihu.com/p/105463736?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656&utm_content=first)|
---|---|

[云原生应用之路——从Kubernetes到Cloud Native](https://jimmysong.io/kubernetes-handbook/cloud-native/from-kubernetes-to-cloud-native.html)|[如何基于 Spring Cloud Alibaba 构建微服务体系](https://www.kubernetes.org.cn/8373.html)|
---|---|

[ChaosBlade x SkyWalking 微服务高可用实践](https://mp.weixin.qq.com/s/f1JdQ5ux-8yHfnVf4q3p2g)|[微服务框架：如果不用Spring Boot，还可以选择谁](https://www.kubernetes.org.cn/9526.html)|
---|---|

[【项目实战】微服务多租户系统后台管理系统---基于SpringBoot2.x、SpringCloud和SpringCloudAlibaba并采用前后端分离的企业级微服务多租户系统架构](https://gitee.com/zlt2000/microservices-platform)|
---|

[手摸手教你从开发到部署(CI/CD)GO微服务系列 ](https://learnku.com/docs/go-micro-build/1.0)|
---|


# 微服务架构深度解析与最佳实践

* [微服务架构深度解析与最佳实践 - 第一部分](https://xie.infoq.cn/article/780637fdbddd12dc908490e66)
* [微服务架构深度解析与最佳实践 - 第二部分](https://xie.infoq.cn/article/814b147cfed5741aa83c57fc0)
* [微服务架构深度解析与最佳实践 - 第三部分](https://xie.infoq.cn/article/c9900f79fe6ffb03410f93ff6)
* [微服务架构深度解析与最佳实践 - 第四部分](https://xie.infoq.cn/article/a754381ce1dd3705b1ce7a641)
* [微服务架构深度解析与最佳实践 - 第五部分](https://xie.infoq.cn/article/20d999bba379e2a72c753728f)
* [微服务架构深度解析与最佳实践 - 第六部分](https://xie.infoq.cn/article/b7efd2998561f98eae0665ffd)
* [微服务架构深度解析与最佳实践 - 第七部分](https://xie.infoq.cn/article/634514d5adbabfc2c05ac003e)
* [微服务架构深度解析与最佳实践（全篇汇总）](https://xie.infoq.cn/article/d6a88dcc243146fa605b1c3bf)

# 微服务例子程序

#### 最全面微服务教程：SpringBoot + DDD + Apache Kafka实现最终一致性
  *  [最全面微服务教程：SpringBoot + DDD + Apache Kafka实现最终一致性(1) ](https://www.jdon.com/56424)
  *  [最全面微服务教程：SpringBoot + DDD + Apache Kafka实现最终一致性(1) 英文版](https://itnext.io/eventual-consistency-with-spring-for-apache-kafka-cfbbed450b5e)
  *  [最全面微服务教程: SpringBoot + DDD + Apache Kafka实现最终一致性(2)：在Kubernetes与Istio运维微服务](https://www.jdon.com/56429)
  *  [[最全面微服务教程: SpringBoot + DDD + Apache Kafka实现最终一致性(2)：在Kubernetes与Istio运维微服务 英文版](https://itnext.io/eventual-consistency-with-spring-for-apache-kafka-part-2-of-2-23bedd512ccf)

* [Microservice Architecture with Spring Boot, Spring Cloud and Docker 例子程序](https://github.com/sqshq/piggymetrics 'This is a tutorial project, which demonstrates Microservice Architecture Pattern using Spring Boot, Spring Cloud and Docker')
 
* [Spring Cloud 微服务(一) 什么是微服务](https://www.jianshu.com/p/2ba8c687d835)
* [Spring Cloud 微服务(二) 创建一个简单的服务](https://www.jianshu.com/p/98a4d25e7f5d)
* [Spring Cloud 微服务(三) 服务发现Eureka](https://www.jianshu.com/p/67b0d2108f67)
* [Spring Cloud 微服务(四) Docker化](https://www.jianshu.com/p/1ce2bc8ce674)
* [Spring Cloud 微服务(五) 部署到AWS ECS](https://www.jianshu.com/p/1617d6948ee8)
* [Spring Cloud 微服务(六) 服务消费Feign](https://www.jianshu.com/p/07303bc4b015)
* [Spring Cloud 微服务 (遇到的问题汇总）](https://www.jianshu.com/p/2e2820269dd2)


* [AWS 上的项目：将整体式应用程序拆分为微服务（使用 Amazon Elastic Container Service、Docker 和 Amazon EC2）](https://aws.amazon.com/cn/getting-started/hands-on/break-monolith-app-microservices-ecs-docker-ec2/)

# 微服务理论主题

  * [单体应⽤和微服务各是什麽？](#单体应⽤和微服务各是什麽？)
  * 单体应⽤拆分成微服务的正确姿势
    * [什么是服务化](#什么是服务化)
    * [什么时候进⾏服务化拆分？](#什么时候进⾏服务化拆分)
    * [服务化拆分的两种姿势](#服务化拆分的两种姿势)
    * [服务化拆分的前置条件](#服务化拆分的前置条件)
    * [引⼊微服务架构需要解决的问题](#引⼊微服务架构需要解决的问题)
  * [正常的微服务调⽤的流程  ](#正常的服务调⽤的流程)
  * 微服务架构的组成部份
    * [服务描述](https://github.com/stevenli91748/MicroService/blob/master/%E6%9C%8D%E5%8A%A1%E6%8F%8F%E8%BF%B0/README.md)
    * [注册中心](https://github.com/stevenli91748/MicroService/blob/master/%E6%B3%A8%E5%86%8C%E4%B8%AD%E5%BF%83/README.md)
    * [服务框架](https://github.com/stevenli91748/MicroService/blob/master/%E6%9C%8D%E5%8A%A1%E6%A1%86%E6%9E%B6/README.md)
    * [服务监控---发现问题](https://github.com/stevenli91748/MicroService/blob/master/%E6%9C%8D%E5%8A%A1%E7%9B%91%E6%8E%A7/README.md)
    * [服务跟踪---定位问题](https://github.com/stevenli91748/MicroService/blob/master/%E6%9C%8D%E5%8A%A1%E8%B7%9F%E8%B8%AA/README.md)
    * [服务治理---解决问题](https://github.com/stevenli91748/MicroService/blob/master/%E6%9C%8D%E5%8A%A1%E6%B2%BB%E7%90%86/README.md)

# 微服务技术栈有那些


微服务技术条目|	落地技术|
---|---|
服务开发|	SpringBoot、Spring、SpringMVC等|
服务配置与管理|	Netfix公司的Archaius、阿里的Diamond等|
服务注册与发现|	Eureka、Consul、Zookeeper等|
服务调用|	Rest、PRC、gRPC|
服务熔断器|	Hystrix、Envoy等|
负载均衡|	Ribbon、Nginx等|
服务接口调用(客户端调用服务的简化工具)|	Fegin等|
消息队列|	Kafka、RabbitMQ、ActiveMQ等|
服务配置中心管理|	SpringCloudConfig、Chef等|
服务路由(API网关)|	Zuul等|
服务监控|	Zabbix、Nagios、Metrics、Specatator等|
全链路追踪|	Zipkin、Brave、Dapper等|
数据流操作开发包|	SpringCloud Stream(封装与Redis，Rabbit，Kafka等发送接收消息)|
时间消息总栈|	SpringCloud Bus|
服务部署|	Docker、OpenStack、Kubernetes等|
---|---|


# 微服务架构设计模式主题
  * [链式设计模式](https://lh3.googleusercontent.com/U3WxwmMmdc2j3OdmyrJx1_29cA5vLGWXpohfiTLNOhebQbH449H744A9dAQCHkNC6-CgGTdid5QtyhzbIMDSc41KjSFu0Z1UFCbM_NnNmX42DMyMOH1ATBsOVI33G5yy3oGHv1Z2dYYDNWFsvU4ayV0JH9SNONazKucGcu3N2d2kz0UIwCIbz71FJwi4DzmJ11zVMx39gtbc5f4xlfel-gO0qm6GEu7-UOLwEfgXLcz2XVqBgESP9NSH1CcXGobvojVrFaTAY1BPZOxTcZ3H40fA-LFPtFFCQN9dPjmrVEMQqtWArhMvvzM_OuMFs8oI2R9TJ0WRv-hjW_hry6q-sIvYXb1bU3lKZx7B8LoYPWHv1bgrwpJaqjNLojbNOQrDfsPYUVUOzJ6DvqtfWAS8q1JOYqjxHob7qGo-3r5ntoDXtJ9cpN8C1pSb2C3q8GM1LaPavT8f65UOS-HRdModHw2gQmCH1TipoPjx4BGaxFJ0QZEsiC5gOwjj_cCp163OFbz29byogHciPsiVFx0Lcg0-Sxs9hVV6Z4eqH-Y0HXd4m6jEDTPU1Jj7dHdVY2RZF_j54UF3v8MKZSrrc3B0bw_Cm6chSYNJW21VedQtZV2zYJGh-WQ9ozjq_BCXWnXHje2xcKW6GlzjGToaFHI_wOxEOWhjcYhDwA6aRBbyIYntbHgK5M9-ulSmqXOB=w1024-h575-no?authuser=0)
  * [聚合器设计模式(常用)](https://lh3.googleusercontent.com/mwBUdMABkBxUG4oNxL1ba9CmNmqrKZaqmhAb7OtfCNwY9Ap2OJfpxgMWOtKJ1yOaQUqd_FtR4obCj6W6PoOm2JLz4-R-J_ILGdtUn4yH2hzaBc39Rya_4ud6KtymYKdutZwK3JGHWwprtWwP94WDdChVRbAIzI4xoWDy0EVtGU-4dbRmESFzaiPs7FHG6G3M-d7oYiENS-gjTS8Uxvy6btHSRbuJ4xNRmqw7heEr8EHlNrHC25DmP7AW5VLycR_9D5w8AhNWAMHa6H6UgQotNNAHbJjNT0wSbSSEa_yG9NPDYc4NDntzbjWS9UQhiLqg2vh6CA_TEa6m78rixWWVAEcwORVhHP5AbBSzm3ds4B_Vblia0uudMH0eCvwvK5QQ5AyXyM_mEN0_AguzRg_5V4bZoJ6DWZt9cEelpL2ii-VyxEJgo0a5T1L_zF1mwMrDgUOWC173I0SpkKgtGlHnix6mNBmCpvgpllpCUq1qlN6DjSUPmDZwjzmGimMUhYbvOFrV0O99KFPsQdwGpfsyjjae9GtdumDVnvfwmKdzOzM6qnSIHpHGEOZVhNOfw514qEzuE2wvP2pJ_yohC9UoqyVTyy1ii3vO-dphHodSzH59uqSSgYA6Vt2d-Z_jJUnXXQO_UhfFxSVQekfBMWZPpfM0268aVGcm2jodWTC7LMvbJhiaXsyL_4vZEJVB=w1024-h528-no?authuser=0)
  * [数据共享设计模式(常用)](https://lh3.googleusercontent.com/ibLk5TeYS8Ifko8_13UruNbYeomoepvfCY79HVzPVS1t3wKc5tQIhSGO4hclhkzbFOUFUhLIE1T780r2Uggkt-xIorXwEt5eWkAOisuyu9XKiVBda-j5drse633hfZk4jFLydsmIUYwFmO7mndAwEot2jrId0T9hFRqjogWfy8VA90cc1HeJCY-_9ygv67Q_ifnPJb5izf3kAwhKm02fgEaVkm-WzACiZY8awCr9k8RAUnozVfjbgwQ-i35fbXb5LvySFTDNlhoaGP2kqXWKIUe3BVRq0RGd8kaRhVN7y0mpoQuUY_gtlvSwRimiu7Z9MwXTprni-FQodopWwWgGmwaBqfBTYE9qzmOMs8Bg2_kPGvJkTCY13XbkdnRwZ6TsNu_0khU35wYSldwurgA0fndVl_NYQdoPX99jB5-JGODNC4K2S7TxiFDjjP-Ye98GIaVMSORcfSC2kKlRCtYshQVZ2MSGNb6W3mtgECGKgzIn8ItgOuXqnS9ypOJB90TmzTUHX2wv-G7_ios-Mv5k0A9tPrKDSOJAt9_1CKDSM7YsD3F_oYJ_d23s9nzKpOn1AenrnI7HlhBApAH2MCsN78zNHiL5nvyYlb5ZpPWisHNrlwqB4u1ffzEjVz1lZhy0kPRt5hEdaJTcKZbBYySe_EAypGV0xrfZftcqG-hCdjZaxtdX7JEL65cwKIl_=w1024-h634-no?authuser=0)
  * [异步消息设计模式(常用)](https://lh3.googleusercontent.com/SLtOHnLWEHTJ1wGJeq5nmSlHfs-dNQsRyXaruuqqLVvR2h6qpq4_8R9oU7CqQFQaJ5SEwpgCUPo4D4iXfM88H3S1lKGIZ7zShPpWyQPUfC-_0QngMGPHCthFwXZWENvTbk7q6usckqxKQDv4hQrY4JXMjigkGPy3PsuDIdygf3OxfmGpJ3GmeOijGF7zZb2VojDGXXfDkxpO2oWfm6HTds3aOMlqX_YpeFTX7smPpWCFqUAR31QFDOCCtGejcphSkZB4MeTwu15de0lGGE-B-2LoAUknwSiqqePFQ1HJgxLDNeoqBoWgw-KSEKTf4SsfBXx_cD4lLJUp4Py2-lgWk32Ax-Se5Z8BAPS9AuVwWpv_xslVF0Sm3WviKED_XcteXMoV4S4SzrbmWwgw05hkD0tmKncrJQd-3keL36BYsXuRsrAghWLcCIivk7-pGjcklYtSWrvvUTvNW4BSUQIAioj1UJlXOwvFP-qofZPZUnvp98mXmlWVbMgoQHs_XZFdh1Jr0Nlafe7zWI0IV2qzfyHC-vVg7AMwv-UqHqTC2jrXkTkDkiDdcRqFQav6Q3OL5xs1znt3wFuTSFeu_iE5BUACxaAC2SjchXS4QOa7l608HKZWfXv51LJqCjHxi836bS-wRpOViZJahvRA2UB-NGwABtQVOvoYokuSbYvRiSHyphj59nlBQI9jctGQ=w1024-h640-no?authuser=0)
  * CQRS模式
    * [SpringBoot+CQRS微服务设计模式教程 ](https://www.jdon.com/55380) 

# 微服务开发框架主题
  * 微服务网关
  * 微服务监控
    * Nagios
  * 微服务通信
    * RPC
    * REST
    * HAL
    * 消息队列
    * 后台任务处理系统
  * 微服务配置
  * 微服务日志
    * Splunk
  * 微服务测试
    * 微服务的测试策略
    * 微服务的单元测试
    * 微服务的的集成测试
    * 基于消费者驱动的契约测试
    * 微服务的组件测试
    * 微服务的端到端测试

# 微服务持续集成 交付 部署主题

# 微服务运维平台主题

---

## 单体应⽤和微服务各是什麽？

    单体应⽤:
    
    早些年，各⼤互联⽹公司的应⽤技术栈⼤致可分为LAMP（Linux + Apache + MySQL + PHP）和MVC（Spring +iBatis/Hibernate + Tomcat）两⼤流派。
    ⽆论是LAMP还是MVC，都是为单体应⽤架构设计的，其优点是学习成本低，开发上⼿快，测试、部署、运维也⽐较⽅便，甚⾄⼀个⼈就可以完成⼀个⽹站的开发
    与部署。以MVC架构为例，业务通常是通过部署⼀个WAR包到Tomcat中，然后启动Tomcat，监听某个端⼝即可对外提供服务

    微服务:
    
    微服务就是将庞杂臃肿的单体应⽤拆分成细粒度的服务，独⽴部署，并交给各个中⼩团队来负责开发、测试、上线和运维整个⽣命周期
    

## 什么是服务化

    服务化就是把传统的单机应⽤中通过JAR包依赖产⽣的本地⽅法调⽤，改造成通过RPC接⼝产⽣的远程⽅法调⽤

## 什么时候进⾏服务化拆分

    项⽬第⼀阶段的主要⽬标是快速开发和验证想法，证明产品思路是否可⾏。这个阶段功能设计⼀般不会太复杂，开发采取快速迭代的⽅式，架构也不适合过度设计。
    所以将所有功能打包部署在⼀起，集中地进⾏开发、测试和运维，对于项⽬起步阶段，是最⾼效也是最节省成本的⽅式。当可⾏性验证通过，功能进⼀步迭代，就
    可以加⼊越来越多的新特性。
    
    产品上线后，经过⼀段时间的运营，⽤户开始逐步增多，可⾏性验证通过，下⼀阶段就需要进⼀步增加更多的新特性来吸引更多的⽬标⽤户.⼀般情况下，这个时候
    就需要⼤规模地扩张开发⼈员，以⽀撑多个功能的开发。如果这个时候继续采⽤单体应⽤架构，多个功能模块混杂在⼀起开发、测试和部署的话，就会导致不同功
    能之间相互影响，⼀次打包部署需要所有的功能都测试OK才能上线,不仅如此，多个功能模块混部在⼀起，对线上服务的稳定性也是个巨⼤的挑战,⼀旦单体应⽤同
    时进⾏开发的⼈员超过10⼈，就会遇到上⾯的问题，这个时候就该考虑进⾏服务化拆分了。

## 服务化拆分的前置条件

    从单体应⽤迁移到微服务架构时必将⾯临也必须解决的问题
    
    服务如何定义：
    
    对于单体应⽤来说，不同功能模块之前相互交互时，通常是以类库的⽅式来提供各个模块的功能。对于微服务来说，每个服务都运⾏在各⾃的进程之中，
    应该以何种形式向外界传达⾃⼰的信息呢？答案就是接⼝，⽆论采⽤哪种通讯协议，是HTTP还是RPC，服务之间的调⽤都通过接⼝描述来约定，约定内容包括接
    ⼝名、接⼝参数以及接⼝返回值。
    
    服务如何发布和订阅：
    单体应⽤由于部署在同⼀个WAR包⾥，接⼝之间的调⽤属于进程内的调⽤。⽽拆分为微服务独⽴部署后，服务提供者该如何对外暴露⾃⼰的地址，服务调⽤者该如
    何查询所需要调⽤的服务的地址呢？这个时候你就需要⼀个类似登记处的地⽅，能够记录每个服务提供者的地址以供服务调⽤者查询，在微服务架构⾥，这个地⽅
    就是注册中⼼
    
    服务如何监控：
    通常对于⼀个服务，我们最关⼼的是QPS（调⽤量）、AvgTime（平均耗时）以及P999（99.9%的请求性能在多少毫秒以内）这些指标。这时候你就需要⼀种通⽤的
    监控⽅案，能够覆盖业务埋点、数据收集、数据处理，最后到数据展示的全链路功能

    服务如何治理：
    可以想象，拆分为微服务架构后，服务的数量变多了，依赖关系也变复杂了。⽐如⼀个服务的性能有问题时，依赖的服务都势必会受到影响。可以设定⼀个调⽤性
    能阈值，如果⼀段时间内⼀直超过这个值，那么依赖服务的调⽤可以直接返回，这就是熔断，也是服务治理最常⽤的⼿段之⼀。

    故障如何定位：
    在单体应⽤拆分为微服务之后，⼀次⽤户调⽤可能依赖多个服务，每个服务⼜部署在不同的节点上，如果⽤户调⽤出现问题，你需要有⼀种解决⽅案能够将⼀次
    ⽤户请求进⾏标记，并在多个依赖的服务系统中继续传递，以便串联所有路径，从⽽进⾏故障定位。
    

## 服务化拆分的两种姿势

   
    那么服务化拆分具体该如何实施呢？⼀个最有效的⼿段就是将不同的功能模块服务化，独⽴部署和运维
   
    纵向拆分：
    
    是从业务维度进⾏拆分。标准是按照业务的关联程度来决定，关联⽐较密切的业务适合拆分为⼀个微服务，⽽功能相对⽐较独⽴的业务适合单独拆分为⼀个微服务

    横向拆分：
    
    是从公共且独⽴功能维度拆分。标准是按照是否有公共的被多个其他服务调⽤，且依赖的资源独⽴不与其他业务耦合。
    
    前期，可以稍微粗粒度⼀些。先进⾏纵向拆分，把基础功能（⽤户系统）独⽴部署以维护。其它业务功能关联不紧密的可以独⽴部署，可以看这些业务在公司发展
    ⽅向的重要性后⾯，可以看清哪些功能是其他业务系统⼀定要调⽤的，同时，⾃身系统内也有其他繁杂的功能，那么可以进⾏横向切分，把被频繁调⽤的服务抽象
    并独⽴部署

    ⽆论是纵向拆分还是横向拆分，都是将单体应⽤庞杂的功能进⾏拆分，抽离成单独的服务部署。实际业务中这两种拆分⽅式⼀般是相互结合使⽤的，如果业务⽐较
    多分散，适合做纵向拆分。如果多个业务之间有公共模块耦合，适合把公共模块拆分出来，适合做横向拆分


## 引⼊微服务架构需要解决的问题


    服务化拆分后会带来的分布式服务事务的⼀致性问题，分布式数据⼀致性问题,，拆微服务势必会提⾼运维、问题追踪、分布式事务等复杂度
    
    所以微服务整个技术栈都要考虑进去, 微服务只能解决单体膨胀后的痛，但也会带来架构复杂性

## 正常的服务调⽤的流程

    ⾸先服务提供者（就是提供服务的⼀⽅）按照⼀定格式的服务描述，向注册中⼼注册服务，声明⾃⼰能够提供哪些服务以及服务的地址是什么，完成服务发布。
    
    接下来服务消费者（就是调⽤服务的⼀⽅）请求注册中⼼，查询所需要调⽤服务的地址，然后以约定的通信协议向服务提供者发起请求，得到请求结果后再按照约
    定的协议解析结果。
    
    ⽽且在服务的调⽤过程中，服务的请求耗时、调⽤量以及成功率等指标都会被记录下来⽤作监控，调⽤经过的链路信息会被记录下来，⽤于故障定位和问题追踪。
    在这期间，如果调⽤失败，可以通过重试等服务治理⼿段来保证成功率。







    
---

* [几种常见的微服务架构方案]()
  * [一个成功的程序员，自然要懂微服务，汇总微服务架构的15钟框架！](https://juejin.im/post/5e6786f0f265da571a39e108)
  * ZeroC IceGrid微服务架构
  * Spring Cloud微服务架构
  * Docker Swarm微服务架构
  * 基于消息队列的微服务架构


* 微框架
  * 与微服务之间的关系
  *   
* 微服务架构
* Docker虚拟化
* Spring Cloud

* [微服务概述](https://github.com/stevenli91748/MicroService/blob/master/%E5%BE%AE%E6%9C%8D%E5%8A%A1%E6%A6%82%E8%BF%B0.md) 
* [Dubbo](https://github.com/stevenli91748/MicroService/blob/master/Dubbo/README.md)
* [容器化部署Docker](https://github.com/stevenli91748/Engineering-special/blob/master/Docker/README.md)
* [自动化构建Jenkins](https://github.com/stevenli91748/Engineering-special/blob/master/Jenkins/README.md)


# 微服务视频
  * [百万并发微服务架构最新实战301集](https://www.bilibili.com/video/BV1P7411A7Bc/?spm_id_from=333.788.b_7265636f5f6c697374.10)
  * [Dubbo+zookeeper+SpringBoot+Redis+MQ微服务架构实战开发](https://www.bilibili.com/video/BV1VJ411g7Zq/?spm_id_from=333.788.videocard.5)
  * [微服务实施的最佳实践、一致性、压测、容量评估、调用链一网打尽](https://www.youtube.com/watch?v=9DDGZnaQfwc)
  * [2020年最全微服务架构教程全集](https://www.bilibili.com/video/av81820341/?spm_id_from=333.788.videocard.6)
  * [Dubbo+zookeeper+SpringBoot+Redis+MQ微服务架构实战开发](https://www.bilibili.com/video/av68559539/?spm_id_from=333.788.videocard.3)
  * [基于SpringCloud构建微服务电商项目](https://www.bilibili.com/video/av64134293/?spm_id_from=333.788.videocard.1)
  * [基于微服务的秒杀项目实战](https://www.bilibili.com/video/av39729418?from=search&seid=5921434574097814719)
  * [千锋Java【2019Java微服务架构(SpringBoot+Dubbo+Zookeeper](https://www.bilibili.com/video/av46149892?from=search&seid=11436815724766326537)
  * [（千锋教育）Java 微服务实战合集】iToken](https://www.bilibili.com/video/av29882762?from=search&seid=10238601020049542725)
  * [【千锋】Java微服务架构实战教程）](https://www.bilibili.com/video/BV1QW41197DF/?spm_id_from=333.788.videocard.5)
  * [（千锋教育）Java 微服务架构 ](https://www.bilibili.com/video/av35685648?from=search&seid=2311148845795845298)
  * [微服务架构需要解决的问题](https://www.bilibili.com/video/av65833021)
  * [Java高级架构师课程全套学习视频（2000分钟干货讲解](https://www.bilibili.com/video/av62954343/?spm_id_from=333.788.videocard.1)
  * [尚学堂丨微服务架构阶段全套教程](https://www.bilibili.com/video/av47580663/?spm_id_from=333.788.videocard.0)
  * [Java微服务架构视频教程(Docker、Spring Boot、MyBatis)（上）](https://www.bilibili.com/video/av35881272/?spm_id_from=333.788.videocard.1)
  * [Java微服务架构视频教程(Docker、Spring Boot、MyBatis)（下）](https://www.bilibili.com/video/av35881732/?spm_id_from=333.788.videocard.4)
  * [千锋达摩院】微服务架构 2.0（上）Linux + Docker + Kubernetes +SpringBoot+SpringCloud ](https://www.bilibili.com/video/av62628434/?p=2)
  * [千锋达摩院】微服务架构 2.0（下）Linux + Docker + Kubernetes +SpringBoot+SpringCloud](https://www.bilibili.com/video/av74438452/?spm_id_from=333.788.videocard.1)
  * [微服务架构的分布式事务控制解决方案](https://www.bilibili.com/video/av82804614?from=search&seid=2930700588961193916)
  
# 有用的参考
 * [分布式服务架构与微服务架构概念的区别与联系是怎样的](https://www.zhihu.com/question/28253777)
 * [微服务难点：基础数据如何设计，为做到共享，我们这样做](https://www.toutiao.com/a6821112334535098893/?log_from=bd6d21d01d7a4_1630181950026)
 * [微服务间的调用和应用内调用有啥区别](https://juejin.cn/post/6844903825392812045)
 * [微服务调用链追踪中心搭建](https://mp.weixin.qq.com/s?__biz=MzU4ODI1MjA3NQ==&mid=2247483764&idx=1&sn=964629a4e1d42d84047986529376eb28&chksm=fdded7b0caa95ea6a038c623f8813c239e3c6cf87a6cd3818277369f6c287a6833d7826b9bdd&scene=21#wechat_redirect)
 * [微服务应用性能如何？APM监控工具来告诉你！](https://www.jianshu.com/p/6f8072a2a349)
 * [微服务调用为啥用RPC框架，http不更简单吗](https://zhuanlan.zhihu.com/p/61364466)
 * [微服务之间的最佳调用方式](https://zhuanlan.zhihu.com/p/105463736?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656&utm_content=first)
 * [烟囱式到SOA再到微服务](https://www.jianshu.com/p/a095c59baf31)
 * [对微服务和RESTful的理解](https://blog.csdn.net/maoyeqiu/article/details/70917550)
 * [微服务调用链追踪中心搭建](https://mp.weixin.qq.com/s?__biz=MzU4ODI1MjA3NQ==&mid=2247483764&idx=1&sn=964629a4e1d42d84047986529376eb28&chksm=fdded7b0caa95ea6a038c623f8813c239e3c6cf87a6cd3818277369f6c287a6833d7826b9bdd&scene=21#wechat_redirect)
  * 架构解密.从分布式到微服务.pdf
 * [0基础教你搭建一套可自动化构建的微服务框架](https://blog.csdn.net/u010425776/article/details/79240104?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
 * [零基础秒懂：手把手教你搭建一套微服务框架！](https://blog.csdn.net/wufaliang003/article/details/79464737?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
 * [为什么要用分布式架构，又为什么要用微服务](https://blog.csdn.net/world6/article/details/79114105)
 * [一分钟弄懂什么是分布式和微服务](https://blog.csdn.net/zhonglunsheng/article/details/83153451)
 * [微服务为什么一定要上Docker？](https://zhuanlan.zhihu.com/p/53686883?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)
 * [五分钟阅读阿里巴巴架构师如何使用微服务框架搭建电商平台全过程](https://blog.csdn.net/pingdouble/article/details/79527044)
 * [程序员一般喜欢浏览哪些网站呢？](https://www.zhihu.com/question/283272958/answer/598956527?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656)

* [微服务架构专题](http://blog.didispace.com/micro-serivces-arch/)
* [【双11狂欢的背后】微服务注册中心如何承载大型系统的千万级访问？--石杉的架构笔记](https://mp.weixin.qq.com/s/qjMphuPiihBmU2QtFMIfzw)
* [【性能优化之道】每秒上万并发下的Spring Cloud参数优化实战！--石杉的架构笔记](https://mp.weixin.qq.com/s/aH0LHgfhxpvp1IY-XbEMWA)
* [微服务架构如何保障双11狂欢下的99.99%高可用？--石杉的架构笔记](https://mp.weixin.qq.com/s/lBeQSSPX7OeWO6SmWYf1Mg)
* [Spring Cloud微服务架构的生产实践与性能优化！--石杉的架构笔记](https://mp.weixin.qq.com/s/FhspnvbIl71uIZ61K8cUoA)
* [微服务架构之技术选型及架构设计](https://blog.csdn.net/luzhangtong/article/details/81147603)
* [基于OpenResty和Node.js的微服务架构实践](https://www.getui.com/cn/industry/2017/05/050376.html)
* [自建电商平台分布式微服务架构--服务治理、服务隔离](https://blog.csdn.net/chengyun19830206/article/details/82530776)
* [Building Microservices: Using an API Gateway](https://www.nginx.com/blog/building-microservices-using-an-api-gateway/)
* [使用API网关构建微服务--实际例子](https://cloud.tencent.com/developer/article/1032069?fromSource=waitui)
* [微服务架构中的进程间通信](https://cloud.tencent.com/developer/article/1032067)
* [《微服务》九大特性](http://blog.didispace.com/20160917-microservices-note/)
* [微网关与服务啮合](http://blog.didispace.com/microgateway-and-service-mesh/)
* [那些没说出口的研发之痛，做与不做微服务的几大理由](http://blog.didispace.com/choose-microservices-or-monoliths-reasons/)
* [手把手0基础项目实战（一）——教你搭建一套可自动化构建的微服务框架](https://juejin.im/post/5a97fbb46fb9a028b5475043)
* [从单体架构升级到微服务，在代码层面应注意的一些问题](https://www.javazhiyin.com/40420.html)
* [一文详解微服务架构](https://www.javazhiyin.com/42246.html)

* [从零开始搭建一套微服务框架（一）方案制定](https://blog.csdn.net/kris1122/article/details/87717563?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
* [从零开始搭建一套微服务框架（二）搭建微服务调度中心Zookeeper](https://blog.csdn.net/kris1122/article/details/88290122?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
* [从零开始搭建一套微服务框架（三）搭建项目框架](https://blog.csdn.net/kris1122/article/details/88311015?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
* [从零开始搭建一套微服务框架（四）集成hystrix](https://blog.csdn.net/kris1122/article/details/88351343?depth_1-utm_source=distribute.pc_relevant_right.none-task&utm_source=distribute.pc_relevant_right.none-task)
* [从零开始搭建一套微服务框架（五）集成nacos](https://blog.csdn.net/kris1122/article/details/88547450?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)
* [从零开始搭建一套微服务框架（六）集成fescar](https://blog.csdn.net/kris1122/article/details/88554452?depth_1-utm_source=distribute.pc_relevant.none-task&utm_source=distribute.pc_relevant.none-task)

---

* [Spring Cloud 微服务(一) 什么是微服务](https://www.jianshu.com/p/2ba8c687d835)
* [Spring Cloud 微服务(二) 创建一个简单的服务](https://www.jianshu.com/p/98a4d25e7f5d)
* [Spring Cloud 微服务(三) 服务发现Eureka](https://www.jianshu.com/p/67b0d2108f67)
* [Spring Cloud 微服务(四) Docker化](https://www.jianshu.com/p/1ce2bc8ce674)
* [Spring Cloud 微服务(五) 部署到AWS ECS](https://www.jianshu.com/p/1617d6948ee8)
* [Spring Cloud 微服务(六) 服务消费Feign](https://www.jianshu.com/p/07303bc4b015)
* [Spring Cloud 微服务 (遇到的问题汇总）](https://www.jianshu.com/p/2e2820269dd2)


