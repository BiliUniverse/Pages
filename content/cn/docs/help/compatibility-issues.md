---
title: "兼容性问题"
description: "代理工具特性支持"
lead:  ""
date: 2023-04-20T20:00:00+08:00
lastmod: 2023-04-20T20:00:00+08:00
draft: false
images: []
menu:
  docs:
    parent: "help"
weight: 620
toc: true
---

{{< alert icon="💡" text="建议阅读 <a href=\"https://trello.com/b/5qmVzMIg/ios%E4%B8%BB%E6%B5%81vpn%E5%8A%9F%E8%83%BD%E5%B7%AE%E5%BC%82\">iOS 主流 VPN 功能差异</a>"/>}}

BiliUniverse 模块工作时需要代理工具提供支持，由于某些原因，部分代理工具并不能满足模块所需的所有特性，因此只能使用部分功能。

已知问题有：

##  Quantumult X - 兼容模式
Quantumult X 无法使用脚本修改当前请求的策略，所以不能使用查询模式。  
Quantumult X 必须在脚本开始前就决定脚本的类型，所以要么是修改请求，要么是构造响应，而模块包含的脚本中这两种逻辑都有，所以无法进行重写 CDN 的操作。
