---
title: DDOS 压力测试
tags: []
id: '1773'
categories:
  - - 短文
date: 2016-07-14 09:15:33
---

今天，我在 Google 上搜了几个免费的 DDOS 压力测试软件，对我的服务器进行 NTP 攻击，为预防真正 DDOS 攻击做实战，具体结果如下：
<!-- more -->

## 攻击对象

攻击对象均为我自己的 VPS，系统为 Ubuntu 16.04 LTS，在软件上均无特殊防护，服务提供商和位置为：

*   Vultr 硅谷，未购买 DDOS 防御
*   Vultr 日本，无 DDOS 防御
*   OVH 加拿大，包含 DDOS 高级防御
*   36cloud 香港，无 DDOS 防御

## 结果

Vultr 的两个服务器在每次被攻击时，检查 Vultr 自己提供的面板，都能看到有 1o0Mbps 的带宽（服务器不限带宽），单核 CPU 上升至 40%，服务器的 Ping 服务未遭到影响。 OVH 在被攻击时，能看到有 50Mbps 的带宽（服务器是 100Mbps 带宽），CPU 没有增加，应该是有 DDOS 防御的效果。 36cloud 被直接打挂，截止到目前已经被指向黑洞快一小时了，毕竟本来带宽就很小。被黑洞了 12 小时，之后终于恢复正常。
