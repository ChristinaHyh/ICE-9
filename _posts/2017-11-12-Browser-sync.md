---
layout: post
title: '使用Browser-sync'
date: 2017-11-12
author: Christina
lang: cn
tags: TOOLS
---

---

什么是[Browser-sync](https://www.browsersync.io/ )？

### 1. 安装Node.js和Browser-sync    

Browser-sync依赖Node.js（简称Node），因此需要先从[nodejs.org](https://nodejs.org/en/)下载安装包安装Node，Node.js安装完成后在命令行中跑下面的命令安装browser-sync


<pre><code class="language-css">npm install -g browser-sync</code></pre>


### 2. 使用Browser-sync 

打开命令行，切换到工作目录：  
<pre><code class="language-css">cd /Users/xhz1/Desktop/poi</code></pre>

Chrome是默认浏览器：
<pre><code class="language-css">browser-sync start --server --files "stylesheets/*.css, *.html"</code></pre>     

Chrome不是默认浏览器：    
<pre><code class="language-css">browser-sync start --server --browser "Google Chrome"
                          --files "stylesheets/*.css, *.html"</code></pre>   
### 3. 退出Browser-sync 


<pre><code class="language-css">ctrl+c</code></pre>




 