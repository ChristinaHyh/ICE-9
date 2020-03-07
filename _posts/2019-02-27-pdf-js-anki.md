---
layout: post
title: 'PDF.js+Chrome+Anki=任性学习专业英语'
date: 2019-02-27
author: Christina
tags: TOOLS
---

---

### **前言**

最近开始需要大量阅读英文文献，无奈专业词汇匮乏，又不想赖着翻译软件翻译，其实除了专业词汇，其他阅读倒也还好，于是开始寻找工具，能够高效率划词又能积累词汇，感谢[老黄老巢](https://www.laohuang.net/20180213/online-dictionary-helper/)的工具，在此写一篇小白安装使用教程，省去辗转寻找各安装包，若想继续详细了解，请移步[老黄老巢](https://www.laohuang.net)博客。

### **工具**

* Chrome([下载地址](https://www.google.com/chrome/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/chrome.exe))
* Anki PC版([下载地址](https://apps.ankiweb.net/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/anki-2.0.exe))
* Anki Android版(自行各大应用市场下载)
* 在线词典助手插件([下载地址](https://chrome.google.com/webstore/detail/online-dictionary-helper/lppjdajkacanlmpbbcdkccjkdbpllajb?hl=zh-CN)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/dic.crx))
* Anki-connect([下载地址](https://github.com/FooSoft/anki-connect)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/ankiconnect.zip))
* PDF.js([下载地址](https://mozilla.github.io/pdf.js/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/pdfjs.zip))
* Anki卡片模版([直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/anki.apkg))

### **安装**

**1.安装Chrome、Anki PC版、Anki手机端**

为使用AnkiConnect插件建议PC安装Anki2.0版本的，可在官网页面最下方找到旧版安装包，或可点击本文中“直接下载”进行下载

**2.安装在线词典助手扩展程序**

打开扩展程序，勾选“开发者模式”
      
![](/assets/img/a.png)

![](/assets/img/b.png)
      
直接将dic.crx拖放到扩展程序安装

**3.安装Anki Connect** 

解压ankiconnect.zip，将里面的AnkiConnect.py复制到Anki的插件文件夹下，该文件夹地址如下：

![](/assets/img/c.png)
      
重启Anki
      
      
**4.导入Anki模版**

打开Anki，导入刚刚下载的模版anki.apkg
      
![](/assets/img/d.png)
      
为使手机端和电脑端词汇同步，请自行到anki官网注册帐号

**5.配置**

在扩展程序里点击在线词典助手的详情，打开“允许访问文件网址”

![](/assets/img/e.png)
      
打开Anki，登录帐号，点击在线词典助手扩展程序里的“扩展程序选项”
      
![](/assets/img/f.png)
      
在“输出选项”中选择AnkiConnect，也可选择AnkiWeb，“脚本选项”里有词典可选择
      
以下是我的配置，可以根据个人喜好调整
      
![](/assets/img/g.png)

![](/assets/img/h.png)

![](/assets/img/i.png)      
        
**6.安装PDF.js**

解压pdfjs.zip，用chrome浏览器打开/pdfjs-2.0.943-dist/web/viewer.html，点击下图按钮打开本地pdf

![](/assets/img/j.png)


**7.使用划词与自动生成Anki卡片**

启用在线词典助手即可划词，点击加号可添加到Anki，可手机电脑同步浏览背诵，单击卡片显示中文释义
       
![](/assets/img/k.png)

![](/assets/img/l.png)

![](/assets/img/m.png)

关于Anki的强大功能，还请另行摸索

---

### 2020-03-07更新

由于2020.02后，PC端Anki 2.1版本以下的数据不能同步到Anki Web上了，本教程中使用的是Anki 2.0及对应版本的AnkiConnect，这里更新一下支持Anki2.1的AnkiConnect的安装，详细见[官网文档](https://ankiweb.net/shared/info/2055492159)

Anki 2.1 | [下载地址](https://apps.ankiweb.net/) | [直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/anki-2.1.exe) 

打开Anki，点击“工具”→“附加组件”→“获取插件”，在“代码”一栏输入`2055492159`后，点击ok即可安装AnkiConnect，待安装完成后，重启Anki，配置及使用方法不变。

![](/assets/img/2020-03-07_193146.png)

![](/assets/img/2020-03-07_193250.png)
