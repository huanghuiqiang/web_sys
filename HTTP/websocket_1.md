## websock 的历史和简单使用

### websocket 的历史

最早的 HTTP，是请求应答模式，传输的是整个 HTML 页面。
AJAX 技术出现后，能够只传输需要更新的数据。
但是 HTTP 协议本身，还是限制了数据的传输。主要是两方面，一是请求应答的模型。二是他的请求头太大了、携带了 Cookie 这些不必要的信息，
而且无法从服务器主动发送消息。（虽然这些后来在 HTTP2.0 得到了优化。）基于这些历史背景，websoket 协议诞生了。它天生就是为了高效传输数据。

1.通过 websocket 握手的方式，建立连接

2.先发送一个 HTTP 请求，里面的请求头包含 UpGrade 字段，告诉浏览器，想要建立 websocket 连接

```
GET ws://websocket.example.com/ HTTP/1.1
Origin: http://example.com
Connection: Upgrade
Host: websocket.example.com
Upgrade: websocket
```

3.服务器支持 websocket 协议，通过 Upgrade 字段，同意升级协议。

```
HTTP/1.1 101 WebSocket Protocol Handshake
Date: Wed, 16 Oct 2013 10:07:34 GMT
Connection: Upgrade
Upgrade: WebSocket
```

4.HTTP 协议，已经被 websockt 协议取代，现在双方都可以发送报文了。

### 创建一个简单的 websoket 实例

```
// 1.新建一个 WebSocket实例
var socket = new WebSocket('wss://echo.websocket.org');

// 2.通过websocket发送数据
socket.send(message);

// 3.监听websocket成功建立，执行回调函数onopen
socket.onopen = function (event) {

};

// 4.处理返回的数据

socket.onmessage = function (event) {
var message = event.data;
};

// 5.关闭websocket链接
 socket.close();

监听关闭事件
socket.onclose = function (event) {
};

```
