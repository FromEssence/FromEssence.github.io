---
title: TCP端口“共享”问题
date: 2020-05-03 08:31:52
tags:
- 计算机网络
---

首先注意，这里的”共享“不是指“不同服务在相同端口上监听”(所谓的"端口复用")。

### 问题1：server端口

Q：一个web server部署在(监听)80端口，那么多个clients向80端口发起请求时server怎么区分？

A：从高层次来看，监听在某个端口的server是可以同时保持与多个clients的连接的，由于`<src ip:port>`不同，可以建立多个sockets。



具体实现时，server在建立新连接后实际上是建立了新的socket。

### 问题2：client端口

Q：既然server端可以根据`<src ip:port>`的不同区分连接，那client上同一个端口号可不可以同时保持与多个不同服务的连接呢？

### 参考

1. [Can different sockets share a port?](https://stackoverflow.com/questions/11129212/tcp-can-two-different-sockets-share-a-port/11129641#)

2. [how do multi clients connect simultaneously to one port?](https://stackoverflow.com/questions/3329641/how-do-multiple-clients-connect-simultaneously-to-one-port-say-80-on-a-server)