RPC 模型
同步滚动：
IDL（Interface description language） 定义
代码生成器
序列化协议
Transport 协议
RPC 处理框架
IDL
IDL 是接口描述语言，没有什么好解释的就是描述定义数据、接口的工具，在RPC模型中IDL可以看作为服务或接口的Meta信息，用来定义服务、接口和数据。

代码生成器
代码生成器是一个通过IDL生成目标语言代码的compiler，通常代码生成器是和IDL绑定的，提供IDL的时候会提供相应的代码生成器，根据IDL描述用户可以使用代码生成器生成目标语言的代码（列如，gRPC的protoc，Corba的idl[.exe], Thrift的ww，ZeroC ICE的的）

序列化协议
在编程领域序列化是将程序语言描述的数据或对象转换成便于存储和传输的数据格式，序列化同时伴有反序列化否则没什么意义， 序列化协议无非两种，一种是二进制序列化，另一种是基于字符串的序列化

二进制序列化协议 Java的Serilization，
字符串序列化 ： XML，Json，Protobuf
Transport协议
Transport协议是指如何进行数据传输，是RPC框架将序列化后的数据进行传输的方式，通常我们描述Transport会带上序列化协议的类型，例如基于Socket的Json传输，或者是基于Socket的二进制传输

RPC 处理框架
通常一个跨语言的RPC框架会包含以上4部分内容，RPC框架为开发者提供了整套的工具和使用方法，针对不同语言的实现每个RPC框架都有所不同，此部分会在具体的RPC框架模型中描述。