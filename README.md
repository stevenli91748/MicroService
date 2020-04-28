# [MicroService 面试](https://github.com/stevenli91748/MicroService/blob/master/interview.md)

# 目录

# 一个微服务的例子

<a href="https://ibb.co/3pm6X2T"><img src="https://i.ibb.co/x1q9vW2/image.png" alt="image" border="0"></a>


# 微服务的关注点在能力分治，将同类型的能力聚集在一个应用中，做到功能解耦，分别演化。这里涉及到两个点：微服务内部组件间如何调用 & 微服务整体如何对外提供服务。成熟方案是通过微服务框架（如SpringCloud）的功能组件完成，如前者属于服务治理和发现（Eureka），后者通过网关（gateway）

作者：熊泰克
链接：https://www.zhihu.com/question/303381841/answer/734772554
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。


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
  * [2020年最全微服务架构教程全集](https://www.bilibili.com/video/av81820341/?spm_id_from=333.788.videocard.6)
  * [Dubbo+zookeeper+SpringBoot+Redis+MQ微服务架构实战开发](https://www.bilibili.com/video/av68559539/?spm_id_from=333.788.videocard.3)
  * [基于SpringCloud构建微服务电商项目](https://www.bilibili.com/video/av64134293/?spm_id_from=333.788.videocard.1)
  * [基于微服务的秒杀项目实战](https://www.bilibili.com/video/av39729418?from=search&seid=5921434574097814719)
  * [千锋Java【2019Java微服务架构(SpringBoot+Dubbo+Zookeeper](https://www.bilibili.com/video/av46149892?from=search&seid=11436815724766326537)
  * [（千锋教育）Java 微服务实战合集】iToken](https://www.bilibili.com/video/av29882762?from=search&seid=10238601020049542725)
  * [【千锋】Java微服务架构实战教程（179集）](https://www.bilibili.com/video/av43943035/?spm_id_from=333.788.videocard.0)
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


