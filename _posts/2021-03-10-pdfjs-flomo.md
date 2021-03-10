---
layout: post
title: 'PDF.js+Chrome+flomo=构建思想闪光流'
date: 2021-03-10
author: Christina
tags: 工具
---

---

### **前言**

工科科研党在读文献时，总有这么一个问题，读过不记笔记就容易忘，而很多时候，这些读过的文献都有可能是科研idea的源泉，但是传统的在pdf上高亮批注的做笔记方式虽然能防止灵感溜走，但是也有一些不便，比如分类整合问题，回顾翻阅不集中等，于是在[flomo](https://flomoapp.com)这个强大的记录想法川流工具的帮助下，我能够分类整理阅读文献的灵感碎片，还能回顾与整合这些闪光点，本文是我初步使用flomo用于自己学术需求的一些札记与分享。

### **工具**

* Chrome ([下载地址](https://www.google.com/chrome/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/chrome.exe))
* PDF.js ([下载地址](https://mozilla.github.io/pdf.js/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/pdfjs.zip))
* flomo ([官网](https://flomoapp.com/))
  * flomoplus：([下载地址](https://chrome.google.com/webstore/detail/flomoplus/kcijjmomofpdcpeiagibojhjifhegepj)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/flomo/flomoplus.crx))
  * flomo API：([下载地址](https://chrome.google.com/webstore/detail/flomo-api/bliaamgfpeogldcelkmkegfofapaocfn)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/flomo/flomoapi.crx))

### **安装**

### 1. 安装Chrome

### 2. 安装flomo的chrome插件

打开扩展程序，勾选“开发者模式”
      
![](/assets/img/a.png)

![](/assets/img/b.png)
      
直接将flomoapi.crx或flomoplus.crx拖放到扩展程序安装

flomoapi适合极简主义者，只打算使用pdfjs阅读的pdf做笔记到flomo

flomoplus适合那些在微信读书、得到等平台电子书笔记汇入flomo的读者

个人更喜欢flomoapi

### 3.  探索flomo，并获得api

[flomo官网](https://flomoapp.com/)

flomo公众号：flomoapp

获取api：

![](/assets/img/flomoapi.png)

### 4. 添加api至插件

**flomo API**

在扩展程序里点击flomo API的详情，打开“允许访问文件网址”
      
再点击扩展程序里的“扩展程序选项”，在下图处输入上述获得的api后点击Save API即可
      
![](/assets/img/f.png)

![](/assets/img/flomoapi-saveapi.png)

**flomo plus**

在扩展程序里点击flomo plus的详情，点击扩展程序里的“扩展程序选项”，在下图处输入上述获得的api后点击保存即可
      
![](/assets/img/flomoplus-saveapi.png)        

### 6.  安装PDF.js

解压pdfjs.zip，用chrome浏览器打开/pdfjs-2.0.943-dist/web/viewer.html，点击下图按钮打开本地pdf

![](/assets/img/j.png)

### 7. 我是如此这般地使用（flomo API）

用pdfjs优雅地打开文献，发现对自己有用的小闪光，点击flomo api插件的小浮窗，不知不觉地保存了一条笔记，抓住脑子一闪而过的灵感，在flomo后台写下此时的想法，备注标签，文献来源，保存。在某个呆滞还未入睡的夜晚，用手机打开app flomo，随机漫步那些曾经的读过的文献和idea，思考、回顾、发光，当这些想法凝聚到某个程度，便把零碎的闪光点，整合成一个个小灯泡，写论文的时候，随需取用

![](/assets/img/flomoapi-1.png)

![](/assets/img/flomoapi-2.png)

![](/assets/img/flomoapi-3.png)

关于flomo plus的使用可参考[此处](![](https://mp.weixin.qq.com/s/UXcvwsD_vjhUwUxAz9HDxA))
