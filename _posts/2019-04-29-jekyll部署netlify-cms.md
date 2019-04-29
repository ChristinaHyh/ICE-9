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

我是在本地修改好再push到github上的

在Jekyll博客的根目录下创建两个文件，`Gemfile`和`.ruby-version`

`Gemfile`的内容如下：

<pre><code class="language-css">source "https://rubygems.org"
gem 'github-pages
</code></pre>

`.ruby-version`的内容如下：

<pre><code class="language-css">2.6.2</code></pre>

然后同样在根目录下创建文件夹`admin`，里面有两个文件`index.html`和`config.yml`

<pre><code class="language-css">admin
 ├ index.html
 └ config.yml
</code></pre>

其中index.html可以如下：

<pre><code class="language-css">
&lt;html&gt;

&lt;head&gt;

  &lt;meta charset="utf-8" /&gt;

  &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" /&gt;

  &lt;title&gt;Content Manager&lt;/title&gt;

  &lt;link rel="stylesheet" href="https://unpkg.com/netlify-cms@^1.0/dist/cms.css" /&gt;

  &lt;script src="https://identity.netlify.com/v1/netlify-identity-widget.js"&gt;&lt;/script&gt;

&lt;/head&gt;

&lt;body&gt;

  &lt;script src="https://unpkg.com/netlify-cms@^2.9.1/dist/netlify-cms.js"&gt;&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;

</code></pre>

我的config.yml配置如下，可根据个人情况修改，详细见文档：[Configuration](https://www.netlifycms.org/docs/configuration-options/#collections)和[Widgets](https://www.netlifycms.org/docs/widgets/)

<pre><code class="language-css">backend:

  name: git-gateway

  branch: master # Branch to update (master by default)



\# This line should \*not\* be indented

publish_mode: editorial_workflow



media_folder: "/assets/img" # Folder where user uploaded files should go

logo_url: https://hyahui.com/assets/icons/author.svg

\# show_preview_links: true

</code></pre>

**3.Netlify绑定github的repo**

Netlify：按照向导创建好

**4.Netlify Deploy及开启Identity与Git Gateway服务**

**5.用户设置及后台登录**
