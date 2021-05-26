---
layout: post
title: 'PDF.js+Chrome+不背单词=懒人构建语境库'
date: 2021-05-26
author: Christina
tags: 工具
subtitle: 真懒噢~

---


---


### **前言**

之前写过一篇基于Anki的语境习词库构建[方法](https://hyahui.com/pdf-js-anki)，但是Anki用起来可能门槛稍微高一点，于是又写下这篇基于「[不背单词](https://www.bbdc.cn/)」的懒人版语境习词库的构建方法。

### **工具**

* Chrome ([下载地址](https://www.google.com/chrome/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/chrome.exe)) 
* 「不背单词」划词插件 ([下载地址](https://chrome.google.com/webstore/detail/%E4%B8%8D%E8%83%8C%E5%8D%95%E8%AF%8D%E6%9F%A5%E8%AF%8D/cklfipcjofdnmdolnfngpmokdaejidim)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/bbdc.crx))
* PDF.js ([下载地址](https://mozilla.github.io/pdf.js/)丨[直接下载](https://github.com/ChristinaHyh/ICE-9/releases/download/1.0/pdfjs.zip))
* 「不背单词」 ([下载地址](https://www.bbdc.cn/))

### **安装**

**1.安装Chrome、「不背单词」**

根据自己的平台选择合适的安装包下载安装即可

**2.安装不背单词扩展程序**

打开扩展程序，勾选“开发者模式”
      
![](/assets/img/a.png)

![](/assets/img/b.png)
      
直接将bbdc.crx拖放到扩展程序安装

**3.配置**

在扩展程序里点击「不背单词」的详情，打开“允许访问文件网址”

![](/assets/img/e.png)
      
点击chrome扩展程序窗口的「不背单词」图标，进行账号登陆与划词开启

![](/assets/img/bbdc.png)      

![](/assets/img/bbdchc.png)      

**4.安装PDF.js**

解压pdfjs.zip，用chrome浏览器打开/pdfjs-2.0.943-dist/web/viewer.html，点击下图按钮打开本地pdf

![](/assets/img/j.png)

**5.使用划词与添加到生词本**

用pdfjs打开本地pdf阅读时，使用「不背单词」划词，点击添加到生词本即可添加生词，可手机端同步浏览背诵，「不背单词」自带丰富的英美剧例句库以及强大的复习、默写、随身听等功能，付费用户甚至支持词根词缀、柯林斯词典等功能，如有兴趣，请自行探索
       
![](/assets/img/bbdcuse.png)

---




