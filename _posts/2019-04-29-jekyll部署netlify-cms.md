---
title: Jekyll部署Netlify CMS
subtitle: 轻松管理你的博客
author: Christina
tags: TOOLS
date: '2019-04-29'
layout: post
---
> Jekyll托管在github上，但每次发文章都需要push，有些不便，于是将博客部署到[Netlify](https://app.netlify.com)，以便后台管理

**1.创建**[**OAuth Apps**](https://github.com/settings/developers)**并获取Client ID
和Client Secret**

 

![](/assets/img/2019-04-29_133258.png)

其中Authorization callback URL填：https://api.netlify.com/auth/done

**2.在github的Jekyll博客repo创建admin文件夹及Gemfile和.ruby-version**

我是在本地修改好push到github上的

在Jekyll博客的根目录下创建两个文件，`Gemfile`和`.ruby-version`

`Gemfile`的内容如下：

<pre><code class="language-css">source "https://rubygems.org"
gem 'github-pages</code></pre>


`.ruby-version`的内容如下：

<pre><code class="language-css">2.6.2</code></pre>



**3.Netlify绑定github的repo**

Netlify：按照向导创建好

**4.Netlify Deploy及开启Identity与Git Gateway服务**



**5.用户设置及后台登录**
