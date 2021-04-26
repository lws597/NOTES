---
title: computer_networking
abbrlink: 40772
date: 2021-04-20 10:46:58
updated:
tags:
categories:
keywords:
description:
top_img:
comments:
cover:
toc:
toc_number:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
---
# Interview Q&A Computer Networking





## 数据链路层



### 广播信道

广播通信：

- 硬件地址（物理地址、MAC 地址）
- 单播（unicast）帧（一对一）：收到的帧的 MAC 地址与本站的硬件地址相同
- 广播（broadcast）帧（一对全体）：发送给本局域网上所有站点的帧
- 多播（multicast）帧（一对多）：发送给本局域网上一部分站点的帧



## 运输层



### 为什么客户端释放最后需要 TIME-WAIT 等待 2MSL 呢？

1. 为了保证客户端发送的最后一个 ACK 报文能够到达服务端。若未成功到达，则服务端超时重传 FIN+ACK 报文段，客户端再重传 ACK，并重新计时。
2. 防止已失效的连接请求报文段出现在本连接中。TIME-WAIT 持续 2MSL 可使本连接持续的时间内所产生的所有报文段都从网络中消失，这样可使下次连接中不会出现旧的连接报文段。