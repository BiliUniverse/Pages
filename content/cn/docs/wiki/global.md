---
title: "🌐 Global"
description: ""
date: 2023-04-21T17:00:00+08:00
lastmod: 2023-04-21T17:00:00+08:00
draft: false
images: []
menu:
  docs:
    parent: "wiki"
weight: 230
toc: true
---

```
⚠️注意：使用前请务必检查`默认配置`是否与您的实际情况相符
如不符,请使用`BoxJs`正确填写要`启用的地区`和对应`策略组或节点`名称
```

## 简介
  * 自动识别番剧影视内容地区限制并切换线路至对应地区
    * 点开任意地区限制的番剧或影视内容，直接播放，无需配置文件内置策略与规则组
    * 局域网环境下，多设备同时观看不同地区内容，互不影响
  * 自定义搜索地区，快捷返回各区搜索结果

## 功能列表
  * 强制返回的CDN主机名类型    
    * IP: 返回远端DNS解析地址（强烈不推荐！严重影响域名分流规则与CDN重定向）
    * HTTP: 返回HTTP域名（推荐，免去重定向时MitM操作）
    * HTTPS: 返回HTTPS域名（重定向时需对指定域名启用MitM）
      * 此选项不限于媒体流的解析结果，搜索等其他返回的内容如图片音频也受此选项影响
      * 选择`返回域名`的情况下，对于本身无`域名`只有`IP`的返回结果无效
  * 自动识别和分类功能地区设置
    * 务必与代理软件策略相对应
  * 搜索时自定义搜索地区
    * `搜索关键词` + `空格` + `地区名称`
    * 如：`电锯人 🇭🇰` 或 `辉夜 台湾` 或 `尼尔 港`
    * 支持的地区关键词有：
      * 中国大陆：`CN` `CHN` `中` `中国` `🇨🇳`
      * 中国香港：`HK` `HKG` `港` `香港` `🇭🇰`
      * 中国澳门：`澳` `澳门` `🇲🇴`
      * 中国台湾：`TW` `TWN` `台` `台湾` `🇹🇼`
      * ~~东南亚（国际版）：`SEA` `东南亚` `🇺🇳` `TH` `泰` `泰国` `🇹🇭` `SG` `新` `新加坡` `🇸🇬` `MY` `马` `马来西亚` `🇲🇾`~~
        * ~~东南亚（国际版）未来可能细分~~
        * 国际版已拆分独立

## 使用方式
### 配置方法
  * 方法1: 直接使用
    * 采用默认配置
      * 默认配置的地区识别与分流为`中国大陆`,`中国香港`,`中国台湾`
        * 如果与您需要启用的地区设置不同，请参考`方法2`自行修改
        * 东南亚（国际版）暂不可用
      * 默认配置的各地区的策略组名分别为`DIRECT`,`🇭🇰香港`,`🇲🇴澳门`,`🇹🇼台湾`
        * 如果与您配置文件中的策略组或节点名称不符，请参考`方法2`自行修改

  * 方法2: 配合`BoxJs`及订阅使用
    1. 安装`BoxJs`插件并更新引用资源或脚本:
       * 安装方法及下载链接详见: [🧰 BoxJs](../boxjs)
    2. 在`BoxJs`的配置面板中进行个性化设置:
      1. 浏览器访问[BoxJs.com](http://boxjs.com)
      2. 在[`应用`](http://boxjs.com/#/app)页面点开`📺 BiliBili`折叠
      3. 在[`📺 BiliBili: Global`](http://boxjs.com/#/app/BiliBili.Global)根据需要填写您的设置信息

## 安装链接
### 正式版
  * Loon:
    * 需要[3.0.6(534)](https://t.me/LoonNews/948)及以上版本
    * 🆕点击一键安装: [BiliBili.Global.plugin](https://api.boxjs.app/loon/import?plugin=https://raw.githubusercontent.com/BiliUniverse/Global/main/modules/BiliBili.Global.plugin "📺 BiliBili: Global") 
    * `插件`链接: [BiliBili.Global.plugin](https://github.com/BiliUniverse/Global/raw/main/modules/BiliBili.Global.plugin "📺 BiliBili: Global")
  * Quantumult X:
    * ❌`Quantumult X`暂不支持，请等待开发者修复
    * ~~🆕点击一键安装: [BiliBili.Global.snippet](https://api.boxjs.app/quanx/add-resource?remote-resource=%7B%22rewrite_remote%22%3A%5B%22https%3A%2F%2Fraw.githubusercontent.com%2FBiliUniverse%2FGlobal%2Fmain%2Fmodules%2FBiliBili.Global.snippet%3Fraw%3Dtrue%2Ctag%3D%EF%BF%BD%EF%BF%BD%20BiliBili%3A%20Global%22%5D%7D "📺 BiliBili: Global")~~
    * ~~`重写`链接: [BiliBili.Global.snippet](https://github.com/BiliUniverse/Global/raw/main/modules/BiliBili.Global.snippet "📺 BiliBili: Global")~~
  * Surge(Shadowrocket):
    * ❓`Shadowrocket`支持情况不明
    * ☑️`Surge`不完全支持，请等待开发者修复
      * APP端番剧首次打开时，无法应用地区查询结果，需来回切换一下集数（此情况只在每个番剧首次打开时出现）
    * 🆕点击一键安装(Shadowrocket): [BiliBili.Global.sgmodule](https://api.boxjs.app/shadowrocket/install?module=https://raw.githubusercontent.com/BiliUniverse/Global/main/modules/BiliBili.Global.sgmodule "📺 BiliBili: Global")
    * `模块`链接: [BiliBili.Global.sgmodule](https://github.com/BiliUniverse/Global/raw/main/modules/BiliBili.Global.sgmodule "📺 BiliBili: Global")
  * Stash:
    * `覆写`链接: [BiliBili.Global.stoverride](https://github.com/BiliUniverse/Global/raw/main/modules/BiliBili.Global.stoverride "📺 BiliBili: Global")
### 🧪测试版
  * Surge:
    * `模块`链接: [BiliBili.Global.beta.sgmodule](https://github.com/BiliUniverse/Global/raw/beta/modules/BiliBili.Global.beta.sgmodule "📺 BiliBili: Global")