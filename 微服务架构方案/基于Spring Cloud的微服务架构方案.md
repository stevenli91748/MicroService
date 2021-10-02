**基于 Spring Cloud 微服务架构，微服务部分主要采用了 Netflix OSS 组件进行支持，它们包括：**

**配置中心**：默认采用Spring Cloud Config，亦可使用Spring Cloud Consul、Spring Cloud Alibaba Nacos代替。

**服务发现**：默认采用Netflix Eureka，亦可使用Spring Cloud Consul、Spring Cloud ZooKeeper、Etcd等代替。

**服务网关**：默认采用Netflix Zuul，亦可使用Spring Cloud Gateway代替。

**服务治理**：默认采用Netflix Hystrix，亦可使用Sentinel、Resilience4j代替。

**进程内负载均衡**：默认采用Netfilix Ribbon，亦可使用Spring Cloud Loadbalancer代替。

**声明式 HTTP 客户端**：默认采用Spring Cloud OpenFeign。声明式的 HTTP 客户端其实没有找替代品的必要性，如果需要，可考虑Retrofit，或者使用 RestTemplete 乃至于更底层的OkHTTP、HTTPClient以命令式编程来访问，多写一些代码而已了。
