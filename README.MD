# Spring Cloud Config

## 目录

- [快速开始](quick-start.md)
  - 客户端用法
- Spring Cloud Config 服务器
  - 环境仓库
  - 健康指示器
  - 安全
  - 加密/解密
  - Key管理
  - 创建Key存储器用于测试
  - 用多重keys和key循环
  - 提供加密的属性
- 提供其他格式
- 提供纯文本
- 嵌入config服务器
- 推送通知和Spring Cloud Bus
- Spring Cloud Client 客户端
  - 配置第一个BootStrap
  - 发现第一个BootStrap
  - 配置客户端快速失败
  - 配置客户端重试
  - 定位远程配置资源
  - 安全
  - 宝库

---

### 1.3.1.RELEASE

Spring Cloud Config在分布式系统中为外部化配置提供服务端和客户端的支持,通过配置服务器,你可以集中管理所有环境下应用的外部属性,在客户端和服务端的概念上对于Spring Environment和PropertySource是相等的,所以他们十分适合Spring应用程序,而且可以用于其他任何程序或者任何语言.随着应用程序从开发到测试再到生产环境一系列部署流程,你可以管理这些不同环境的配置,而且可以确信在不同环境中他们都将正常工作.默认的服务端存储实现是git,所以你可以很容易的版本化配置环境,同时还可以访问很多工具来管理内容.通过Spring配置十分容易添加可变更的实现和集成.