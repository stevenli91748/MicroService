
# 目录
* [Dubbo概述](#Dubbo概述)



### Dubbo概述

Dubbo是一套微服务系统的协调者，在它这套体系中，一共有三种角色，分别是：服务提供者（下面简称提供者）、服务消费者（下面简称消费者）、注册中心。

你在使用的时候需要将Dubbo的jar包引入到你的项目中，也就是每个服务都要引入Dubbo的jar包。然后当这些服务初始化的时候，Dubbo就会将当前系统需要发布的服务
、以及当前系统的IP和端口号发送给注册中心，注册中心便会将其记录下来。这就是服务发布的过程。与此同时，也是在系统初始化的时候，Dubbo还会扫描一下当前系统
所需要引用的服务，然后向注册中心请求这些服务所在的IP和端口号。接下来系统就可以正常运行了。当系统A需要调用系统B的服务的时候，A就会与B建立起一条RPC信道，
然后再调用B系统上相应的服务。

这，就是Dubbo的作用。



# 有用的参考

* [Dubbo-从入门到深入](http://ifeve.com/dubbo-learn-book/)
* [Springboot 整合 Dubbo/ZooKeeper 详解 SOA 案例](http://ifeve.com/springboot-%E6%95%B4%E5%90%88-dubbozookeeper-%E8%AF%A6%E8%A7%A3-soa-%E6%A1%88%E4%BE%8B/)
* [Dubbo剖析-整体架构分析](http://ifeve.com/dubbo-framework/)
* [Dubbo入门---搭建一个最简单的Demo框架](https://blog.csdn.net/noaman_wgs/article/details/70214612)