短连接：基于 AJAX 技术，使用 XmlHttpRequest 对象

长连接：通过 AJAX 发送，服务器如果没有更新，会保持连接。
优点：减少建立连接的延迟
缺点：需要重复发送报文头部信息

插件：能够调用 Tcp 协议层的接口，双通道协议
缺点：独立于 H5 之外的

Stream 连接：之前是报文是明文，这里开始改用二进制发送，使用 stream 作为数据结构
优点：能够使用同一个管道进行传输。不需要每次发起请求，都建立一个新请求。

webSocket 连接：双通道协议
跨域的方式：

WebScoket 支持跨域,

HTTP 协议，通过设置 Head 头部
数据类型：

WebSocket，支持二进制协议
延迟:

WebScoket < Stream < newWorm Plugin < long-poling

参考链接
[My Understanding of HTTP Polling, Long Polling, HTTP Streaming and WebSockets](https://stackoverflow.com/questions/12555043/my-understanding-of-http-polling-long-polling-http-streaming-and-websockets)
