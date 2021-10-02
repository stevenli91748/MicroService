**基于 Kubernetes 的微服务架构，并采用 Spring Cloud Kubernetes 做了适配，其中主要的技术组件包括：**

**环境感知**：Spring Cloud Kubernetes 本身引入了 Fabric8 的Kubernetes Client作为容器环境感知，不过引用的版本相当陈旧，如 Spring Cloud Kubernetes 1.1.2 中采用的是 Fabric8 Kubernetes Client 4.4.1，Fabric8 提供的兼容性列表中该版本只支持到 Kubernetes 1.14，实测在 1.16 上也能用，但是在 1.18 上无法识别到最新的 Api-Server，因此 Maven 引入依赖时需要手工处理，排除旧版本，引入新版本（本工程采用的是 4.10.1）。

**配置中心**：采用 Kubernetes 的 ConfigMap 来管理，通过Spring Cloud Kubernetes Config自动将 ConfigMap 的内容注入到 Spring 配置文件中，并实现动态更新。

**服务发现**：采用 Kubernetes 的 Service 来管理，通过Spring Cloud Kubernetes Discovery自动将 HTTP 访问中的服务转换为FQDN。

**负载均衡**：采用 Kubernetes Service 本身的负载均衡能力实现（就是 DNS 负载均衡），可以不再需要 Ribbon 这样的客户端负载均衡了。Spring Cloud Kubernetes 从 1.1.2 开始也已经移除了对 Ribbon 的适配支持，也（暂时）没有对其代替品 Spring Cloud LoadBalancer 提供适配。

**服务网关**：网关部分仍然保留了 Zuul，未采用 Ingress 代替。这里有两点考虑，一是 Ingress Controller 不算是 Kubernetes 的自带组件，它可以有不同的选择（KONG、Nginx、Haproxy，等等），同时也需要独立安装，作为演示工程，出于环境复杂度最小化考虑未使用 Ingress；二是 Fenix's Bookstore 的前端工程是存放在网关中的，移除了 Zuul 之后也仍然要维持一个前端工程的存在，不能进一步缩减工程数量，也就削弱了移除 Zuul 的动力。

**服务熔断**：仍然采用 Hystrix，Kubernetes 本身无法做到精细化的服务治理，包括熔断、流控、监视，等等，我们将在基于 Istio 的服务网格架构中解决这个问题。

**认证授权**：仍然采用 Spring Security OAuth 2，Kubernetes 的 RBAC 授权可以解决服务层面的访问控制问题，但 Security 是跨越了业务和技术的边界的，认证授权模块本身仍承担着对前端用户的认证、授权职责，这部分是与业务相关的
