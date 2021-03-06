# [Dubbo面试](https://mp.weixin.qq.com/s?__biz=MzIwNjg4MzY4NA==&mid=2247484066&idx=1&sn=50a4fe0a52e4e5c86fd50d81d1d38b1a&chksm=971b9ca9a06c15bf119817522acd8bb0a5987b80b18f97ab648fc366795c255f1535756a1066&scene=21#wechat_redirect)


# 目录
* [Dubbo概述](#Dubbo概述)
* [Dubbox概述](#Dubbox概述)

[精尽 Dubbo 学习指南](http://svip.iocoder.cn/Dubbo/tutorials/)|[Dubbo有些哪些注册中心？](https://blog.csdn.net/meism5/article/details/104290442?utm_medium=distribute.pc_relevant.none-task-blog-baidujs_baidulandingword-2&spm=1001.2101.3001.4242)|[Dubbo官方网站](https://dubbo.apache.org/zh/)|
---|---|---|

[相较于 Dubbo，Spring Cloud 有何优缺点？](https://www.zhihu.com/question/50806354/answer/1099399169)|[Dubbo 的 8000 字图文详解](https://zhuanlan.zhihu.com/p/140472651?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656&utm_content=first)|[阿里系Dubbo和Spring Cloud微服务架构，哪个比较好](https://zhuanlan.zhihu.com/p/176422784?utm_source=wechat_session&utm_medium=social&utm_oi=991812777480134656&utm_content=first)|
---|---|---|

* [Dubbo 源码分析 - SPI 机制](https://www.tianxiaobo.com/2018/10/01/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-SPI-%E6%9C%BA%E5%88%B6/)
* [Dubbo 源码分析 - 自适应拓展原理](https://www.tianxiaobo.com/2018/10/13/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E8%87%AA%E9%80%82%E5%BA%94%E6%8B%93%E5%B1%95%E5%8E%9F%E7%90%86/)
* [Dubbo 源码分析 - 服务导出](https://www.tianxiaobo.com/2018/10/31/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E6%9C%8D%E5%8A%A1%E5%AF%BC%E5%87%BA/)
* [Dubbo 源码分析 - 服务引用](https://www.tianxiaobo.com/2018/11/12/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E6%9C%8D%E5%8A%A1%E5%BC%95%E7%94%A8/)
* [Dubbo 源码分析 - 集群容错之Directory](https://www.tianxiaobo.com/2018/11/17/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E9%9B%86%E7%BE%A4%E5%AE%B9%E9%94%99%E4%B9%8BDirectory/)
* [Dubbo 源码分析 - 集群容错之 Router](https://www.tianxiaobo.com/2018/11/20/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E9%9B%86%E7%BE%A4%E5%AE%B9%E9%94%99%E4%B9%8B-Router/)
* [Dubbo 源码分析 - 集群容错之 Cluster](https://www.tianxiaobo.com/2018/11/24/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E9%9B%86%E7%BE%A4%E5%AE%B9%E9%94%99%E4%B9%8B-Cluster/)
* [Dubbo 源码分析 - 集群容错之 LoadBalance](https://www.tianxiaobo.com/2018/11/29/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E9%9B%86%E7%BE%A4%E5%AE%B9%E9%94%99%E4%B9%8B-LoadBalance/)
* [Dubbo 源码分析 - 服务调用过程](https://www.tianxiaobo.com/2019/01/09/Dubbo-%E6%BA%90%E7%A0%81%E5%88%86%E6%9E%90-%E6%9C%8D%E5%8A%A1%E8%B0%83%E7%94%A8%E8%BF%87%E7%A8%8B/)





### Dubbo概述

Dubbo只针对服务治理，相当于Spring Cloud中的一个子集。能和Dubbo相互比较的应该是gRPC，Thrift之类的框架

对于性能这块，Dubbo确实要比Spring Cloud好，原因大家也都清楚，Dubbo基于Netty的TCP及二进制的数据传输，Spring Cloud基于HTTP，HTTP每次都要创建连
接，传输的也是文本内容，自然在性能上有些损耗

Dubbo是阿里巴巴开源的分布式服务框架，属于同步调用，当一个系统的服务太多时，需要一个注册中心来处理服务发现问题，例如使用ZooKeeper这类配置服务器进行服务的地址管理：服务的发布者要向ZooKeeper
发送请求，将自己的服务地址和函数名称等信息记录在案；服务的调用者要知道服务的相关信息，具体的机器地址在ZooKeeper查询得到。这种同步的调用机制足够直观简单，只是没有“订阅——推送”机制

Dubbo是一套微服务系统的协调者，在它这套体系中，一共有三种角色，分别是：服务提供者（下面简称提供者）、服务消费者（下面简称消费者）、注册中心。

你在使用的时候需要将Dubbo的jar包引入到你的项目中，也就是每个服务都要引入Dubbo的jar包。然后当这些服务初始化的时候，Dubbo就会将当前系统需要发布的服务
、以及当前系统的IP和端口号发送给注册中心，注册中心便会将其记录下来。这就是服务发布的过程。与此同时，也是在系统初始化的时候，Dubbo还会扫描一下当前系统
所需要引用的服务，然后向注册中心请求这些服务所在的IP和端口号。接下来系统就可以正常运行了。当系统A需要调用系统B的服务的时候，A就会与B建立起一条RPC信道，
然后再调用B系统上相应的服务。

这，就是Dubbo的作用。

**Dubbo 是不需要微服务网关的**


### Dubbox概述

Dubbox = Dubbo + REST

对于性能这块，Dubbo确实要比Spring Cloud好，原因大家也都清楚，Dubbo基于Netty的TCP及二进制的数据传输，Spring Cloud基于HTTP，HTTP每次都要创建连
接，传输的也是文本内容，自然在性能上有些损耗。·Spring Cloud带来的性能损耗对于大部分应用来说是可以接受的，而它具有的HTTP风格的API交互，在不同的语言中是通用的，且对每个微服务的测试来说是非常方便的，也就是说Spring Cloud用小的性能损耗换来了更多好处。当当网在Dubbo的基础上加上REST的支持扩展出目前的Dubbox也是这个道理


# 视频

* [尚硅谷Java视频教程_Dubbo](https://www.bilibili.com/video/av30612478?from=search&seid=11334929433863206245)
* [微服务架构需要解决的问题--Dubbo](https://www.bilibili.com/video/av65833021?p=13)
* [2小时实战Apache顶级项目-RPC框架Dubbo分布式服务调度](https://www.imooc.com/learn/1096)
# 有用的参考

* [微服务面试必问的Dubbo，这么详细还怕自己找不到工作](https://server.51cto.com/Micro-652532.htm)
* [Dubbo面试题（2020最新版）](https://blog.csdn.net/ThinkWon/article/details/104390006)
* [Dubbo-从入门到深入](http://ifeve.com/dubbo-learn-book/)
* [Springboot 整合 Dubbo/ZooKeeper 详解 SOA 案例](http://ifeve.com/springboot-%E6%95%B4%E5%90%88-dubbozookeeper-%E8%AF%A6%E8%A7%A3-soa-%E6%A1%88%E4%BE%8B/)
* [Dubbo剖析-整体架构分析](http://ifeve.com/dubbo-framework/)
* [Dubbo入门---搭建一个最简单的Demo框架](https://blog.csdn.net/noaman_wgs/article/details/70214612)
* [比较spring cloud和dubbo，各自的优缺点是什么](https://blog.csdn.net/u010664947/article/details/80007767)
* [为什么要用dubbo，dubbo和zookeeper关系，简单的dubbo搭建](https://blog.csdn.net/u013206293/article/details/79643588)
* [2019最详细Dubbo相关面试题！](https://zhuanlan.zhihu.com/p/65193437)
* [dubbo面试题！会这些，说明你真正看懂了dubbo源码](https://mp.weixin.qq.com/s?__biz=MzA5NTUzNTA2Mw==&mid=2454932968&idx=1&sn=f85707232789cbb41c2bebffcb67507b&scene=21#wechat_redirect)
* [Java分布式开发不得不知的Dubbo技术详细介绍](https://blog.csdn.net/u011277123/article/details/78081798?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522158527005719195239834846%2522%252C%2522scm%2522%253A%252220140713.130056874..%2522%257D&request_id=158527005719195239834846&biz_id=0&utm_source=distribute.pc_search_result.none-task)
