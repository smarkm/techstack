[Home](/) > [编程](program/) 
## [RPC 框架](program/rpc)
### RPC 模型
* IDL（Interface description language） 定义
* 代码生成器
* 序列化协议
* Transport 协议
* RPC 处理框架

#### IDL
IDL 是接口描述语言，没有什么好解释的就是描述定义数据、接口的工具，在RPC模型中IDL可以看作为服务或接口的Meta信息，用来定义服务、接口和数据。

#### 代码生成器
代码生成器是一个通过IDL生成目标语言代码的compiler，通常代码生成器是和IDL绑定的，提供IDL的时候会提供相应的代码生成器，根据IDL描述用户可以使用代码生成器生成目标语言的代码（列如，gRPC的protoc，Corba的idl, Thrift的thrift，ZeroC ICE的的）

#### 序列化协议
在编程领域序列化是将程序语言描述的数据或对象转换成便于存储和传输的数据格式，序列化同时伴有反序列化否则没什么意义， 序列化协议无非两种，一种是二进制序列化，另一种是基于字符串的序列化

* 二进制序列化协议 Java的Serilization，
* 字符串序列化 ： XML，Json，Protobuf

#### Transport协议
Transport协议是指如何进行数据传输，也就是通过`何种方式`传输`什么样的`数据，是RPC框架将序列化后的数据进行传输的方式，通常我们描述Transport协议为（基于`传输方式`的`数据类型`的传输），例如基于Socket的Json传输，或基于Socket的二进制传输，或基于http的xml传输

#### RPC 处理框架
通常一个跨语言的RPC框架会包含以上4部分内容，RPC框架为开发者提供了整套的工具和使用方法，针对不同语言的实现每个RPC框架都有所不同，此部分会在具体的RPC框架模型中描述。RPC采用C/S结构：
* Server Side：Server端包含对定义的`接口或服务的实现`和用来处理客户端调用的`RPC Server`，负责`解析Request`,`调用服务方法`,`编码Response`
* Client Side：Client端通常通过Stub/Proxy对象（实现service和方法）来调用服务和方法，Stub/Proxy对象负责`编码Request`,`执行rpc调用`,`解码Response`


### [gRPC 模型](program/rpc-grpc)
### [Thrift 模型](program/rpc-thrift)
[^_^]: ### [Corba 模型（Leacy）](program/rpc-corba)
### [ZeroC ICE](program/rpc-ice)
