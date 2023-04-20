---
title: "快速上手"
description: "使用 BiliUniverse 系列模块的简明指南"
lead: "使用 BiliUniverse 系列模块的简明指南"
date: 2023-04-20T20:00:00+08:00
lastmod: 2023-04-20T20:00:00+08:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 110
toc: true
---

{{< alert icon="💡" text="请完整阅读所有内容，如果有疑问请首先浏览完整 Wiki 或者 Google 获取解答，如果内容存在冲突以 Wiki 为准。" />}}

## 检查依赖

- #### 哔哩哔哩 App
  - **本土版 Bilibili** (粉色/白色图标) - 现已支持
  - **东南亚版 Bilintl** (蓝色图标) - 尚未发布

- #### 系统
  - **iOS/iPadOS** - 16.4 测试通过 (推荐 iOS 15+)
  - **macOS(Safari)** - 13 测试通过
  - **tvOS** - 16.4 测试通过

- #### 支持的代理工具
  - **[Loon](https://nsloon.com/)** - 推荐
  - **[Surge](https://nssurge.com/)** - 推荐
  - **[Stash](https://stash.wiki/)**
  - **[Quantumult X](https://quantumult.app/x/)** - 部分支持
  - **[Shadowrocket](https://apps.apple.com/app/shadowrocket/id932747118)** - 部分支持

{{< details "为什么“部分支持”？" >}}
BiliUniverse 模块工作时需要代理工具提供支持，由于某些原因，部分代理工具并不能满足模块所需的所有特性，因此只能使用部分功能。访问 [兼容性问题 →]({{< relref "compatibility-issues" >}}) 获取详细信息。  
另外需要注意的是，模块依赖代理工具中的 [MitM](https://manual.nssurge.com/book/understanding-surge/cn/#mitm-%E6%94%BB%E5%87%BB) 功能完成必要工作，请检查代理工具是否开启 MitM / 系统是否安装并信任 CA 证书，具体配置请参照你所使用的代理工具的相关教程。
{{< /details >}}


## 安装模块

点击标题访问对应模块的 Wiki（安装链接在页面底部）：

#### [<img src="/enhanced_108x.png" height="30" width="30"/> Enhanced](https://github.com/BiliUniverse/Universe/wiki/%E2%9A%99-Enhanced#%E7%AE%80%E4%BB%8B)

全面自定义哔哩哔哩 App 主界面，修改首页和底栏元素的显示顺序和触发功能。

#### [<img src="/global_108x.png" height="30" width="30"/> Global](https://github.com/BiliUniverse/Universe/wiki/%F0%9F%8C%90-Global)

自动识别番剧影视地区限制并切换线路至对应地区，快捷返回各区域搜索结果。

#### <img src="/roaming_108x.png" height="30" width="30"/> Roaming (🚧 开发中)

通过公共解析服务器实现地区漫游，进而提供其他增强功能。  
尚未上线，请耐心等待。

## 完成配置

点击 [这里](https://github.com/BiliUniverse/Universe/wiki/%F0%9F%A7%B0-BoxJs#%E8%AE%A2%E9%98%85%E9%93%BE%E6%8E%A5) 按照提示安装 BoxJs 并添加本项目的订阅链接。

{{< details "为什么打不开 BoxJs？" >}}
你在这里可能会遇到访问 boxjs.com 时加载失败或者加载出奇怪网站的问题。实际上在 BoxJs 模块正常工作的时候，对这个域名的访问请求会被重定向到本地，在互联网上是不存在 BoxJs 页面的！  
所以这时你应该首先检查 模块是否安装 / 远程资源是否更新 / MitM 是否正确配置，而不是到群里问 “这个网站怎么打不开啊”（笑
{{< /details >}}

在 BoxJs 中选择对应模块的配置页面，认真阅读每一个选项，参照 Wiki 完成配置。

祝你玩的开心！
