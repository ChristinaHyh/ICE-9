---
layout: post
title: 'UCalculator'
subtitle: 不确定度计算器——解决理工科生的日常烦恼
date: 2019-08-30
author: Christina
tags: TOOLS
---

---

### **前言**

这是我在2017年参加GoogleStudyJams活动时开发的app，这个活动真的很赞，最后拿到的Google的证书也很赞，可惜活动已经停办了，也算是恰好赶上了末班车，拿到了绝版证书。由于是自己第一次学习Android开发并独立完成的第一个app，有点感情，当时恰逢大物实验写实验报告需要计算大量不确定度，于是就开发了这个不确定度计算器，能减少很多繁琐的计算过程，又能保留中间列算式需要体现在报告里的中间数，考虑到自己以后应该也不会再更新和维护这个应用了，于是就打算放在博客上，供有可能需要的人使用以及自己偶尔回头看看这段有点意思的小白Android学习之旅。

### **介绍**

![](/assets/img/calculator.png)

**UCalculator可以计算：**

> ①直接测量结果的不确定度及其中间计算量标准偏差Sx
> 
> ②直线拟合的斜率与截距的不确定度及其中间计算量斜率b、截距a、斜率标准差Sb、截距标准差Sa

![](/assets/img/app.png)

### **说明**

1.先输入测量次数N，点击“OK”（可支持50个，正常实验报告不会超过50）

2.录入Yi时通过点击“NEXT”进行下一个数据的录入

3.可通过“-”、“+”查看第Xi个变量对应的Yi值，点击“EDIT”可以修改数据，以防止录入数据时出错再重新输入的情况

4.选择需要计算的结果，点击“CALCULATE”即可在Result一栏查看计算结果

5.点击“OTHERS”可以查看计算相应结果的中间数据

6.“RESET”一键重置数据，开始另一轮计算

### **应用下载**

* [UCalculator](https://github.com/ChristinaHyh/ICE-9/releases/download/1.1/UCalculator.apk)



