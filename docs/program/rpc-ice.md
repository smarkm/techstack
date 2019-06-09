[Home](/) > [编程](program/) > [RPC 框架](program/rpc)
# ICE 模型
[https://zeroc.com/products/ice](https://zeroc.com/products/ice)

ICE 是很早之前写C++的时候用过，太长时间没有写过C++, 所以本文之作摘要，不做具体分析，如果以后还会用到或有需要的情况下在进行详细整理，而Java的开发者来说Java生态中有更多合适的RPC框架使用
## IDL
ICE采用自定义Slice(Specification Language for Ice)作为IDL，具体可参考[https://doc.zeroc.com/ice/3.7/the-slice-language](https://doc.zeroc.com/ice/3.7/the-slice-language)

## 代码生成器
ICE提供`slice2*`工具来生成目标语言代码，`slice2java`,`slice2cpp`等