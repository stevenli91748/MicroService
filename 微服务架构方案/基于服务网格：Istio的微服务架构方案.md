
**基于 Istio 的服务网格架构，其中主要的技术组件包括：**

**配置中心**：通过 Kubernetes 的 ConfigMap 来管理。

**服务发现**：通过 Kubernetes 的 Service 来管理，由于已经不再引入 Spring Cloud Feign 了，所以在 OpenFeign 中，直接使用短服务名进行访问。

**负载均衡**：未注入边车代理时，依赖 KubeDNS 实现基础的负载均衡，一旦有了 Envoy 的支持，就可以配置丰富的代理规则和策略。

**服务网关**：依靠 Istio Ingress Gateway 来实现，已经移除了 Kubernetes 版本中保留的 Zuul 网关。

**服务容错**：依靠 Envoy 来实现，已经移除了 Kubernetes 版本中保留的 Hystrix。

**认证授权**：依靠 Istio 的安全机制来实现，实质上已经不再依赖 Spring Security 进行 ACL 控制，但 Spring Security OAuth 2 仍然以第三方 JWT 授权中心的角色存在，为系统提供终端用户认证，为服务网格提供令牌生成、公钥JWKS等支持
