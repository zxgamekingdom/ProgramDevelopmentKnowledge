# 生命周期事件

`OnConnectedAsync`

当客户端连接时

`OnDisconnectedAsync`

当客户端断开连接时

# 通讯方式

## Long Polling（长轮询）

客户端发起请求，服务端如果有数据需要发送给客户端则返回数据给客户端，如果服务端无数据发送给客户端，则服务端挂起客户端的请求，等待服务端有数据需要发送时在将客户端的请求恢复并返回数据给客户端。循环执行这个过程。本质上是不断的发起HTTP请求。

## Server-Sent Events（服务器发送事件）

SSE时服务端主动向客户端推送数据的一种方式。客户端发起请求，服务端返回的不是一次性数据包，而是一个数据流，数据流代表着会有持续不断的数据从服务端返回给客户端，而客户端不关闭连接，也会一直等待并接收服务端返回的数据。本质也是一次HTTP请求，只不过下载的内容从一次性的数据包变为了会有源源不断数据的数据流。单工通讯（服务端->客户端）。

## Web Socket

类似Socket TCP的全双工通讯（客户端<->服务端）。Web Socket只是在握手时会使用HTTP协议，一旦握手完毕，Web Socket之间的通讯就和HTTP没有什么关系了。

# Hub生命周期
​		客户端每一次调用Hub的方法时，SignalR服务端就会创建一个新的Hub对象执行客户端需要调用的对应方法。

​		但是`OnConnectedAsync`方法与`OnDisconnectedAsync`方法只是在客户端连接和断开时才会被调用。

# `OnDisconnectedAsync`没有如预期情况被调用？

目前已知只有Web Socket通讯方式，当浏览器或者网页对应选项卡被关闭时才会调用`OnDisconnectedAsync`方法。Long Polling是不会被调用的。SSE未知！

如果手动调用了SignalR的关闭方法，无论什么通讯方式都会触发Hub的`OnDisconnectedAsync`方法。

# SignalR Web Socket没有发送自定义标头

根据微软的文档与实际测试得出，使用Web Socket与Server Send Event是无法在浏览器中设置标头的。

如果认证方式基于自定义标头信息，则Web Socket无法认证通过。

解决方法一：

​		在SignalR客户端中请求的地址中，将自定义标头信息的内容包含到该地址的查询字符串中，在Asp.Net Core写一个中间件（注意！中间件是有顺序的），在中间件中判断地址的查询字符串中是否包含这些用于认证的信息，如果包含，则直接将这些认证信息转存到Request的标头中。

解决方法二：

​		在SignalR客户端中请求的地址中，将自定义标头信息的内容包含到该地址的查询字符串中，为Asp.Net Core的身份认证添加根据查询字符串的内容进行认证的逻辑。

# 断开连接

调用`Hub`中的`Context`属性的`Abort`方法。

# SendAsync与InvokeAsync区别

Send调用的是没有返回值的方法。

Invoke调用的是有返回值的方法。

