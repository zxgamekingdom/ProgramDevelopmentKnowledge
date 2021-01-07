# Blazor概述

## 服务端

基于SignalR通讯库实现的Web库。与普通的Asp.Net Core的其他的View技术是差不多的，Razor都是在服务端运行完毕后返回给服务端的。

## Web Assembly端

基于Web Assembly实现的Web库。Razor是完全运行在浏览器中的。

# 服务端的Razor组件实现的`IDisposable`接口或者`IAsyncDisposable`不一定会被调用！

服务端的Blazor的SignalR使用的通讯方式可能是Long Polling。目前如果浏览器的选项卡或者浏览器被关闭时，如果SignalR的通讯方式为Long Polling，SignalR库本身是完全没有办法探知的，也没有找到相关的超时设置！

所以安全起见，将服务端Blazor的SignalR的通讯方式设置为WebSockets，不采用其他的通讯方式。

如果浏览器或者浏览器的选项卡被关闭时，Web Socket是可以探知到连接被关闭的，这点和Socket TCP类似。

