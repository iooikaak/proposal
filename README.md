# The Kratos Proposal repository
这个仓库主要用于讨论 Kratos 微服务框架的规范记录，不限于各个语言和平台。

# Goals

* APIs 协议通信以 HTTP/gRPC 为基础，通过 Protobuf 进行定义；
* Errors 通过 Protobuf 定义对应的 Enum 作为错误码，以及国际化信息显示；
* Metadata 在协议通信 HTTP/gRPC 中，规范化服务元信息传递；
* Tracing 框架中统一使用 OpenTracing 规范进行实现；
* Plugins 在设计框架中，通过插件化方式提供扩展能力；
* Templates 提供基础的应用模板，并可以定制化；
* Service Mesh 规范化服务网格使用方式；
* Tools 提供轻量的工具，生成对应的应用模板；

# Proposal Categories

提议需要以模块方式进行规范命名：

* apis-n
* errors-nn
* metadata-nnn
* templates-nnnn

