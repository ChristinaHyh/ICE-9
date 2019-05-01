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

我是在本地修改好再push到github上的，该部分参考文档如下：

[Add to Your Site](https://www.netlifycms.org/docs/add-to-your-site/)

[Migrating your Jekyll site to Netlify](https://www.netlify.com/blog/2017/05/11/migrating-your-jekyll-site-to-netlify/?_ga=2.171346216.960609573.1554181992-139167350.1554020394)

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

其中`index.html`可以如下：

<pre><code class="language-css">&lt;html&gt;
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

我的`config.yml`配置如下，可根据个人情况修改，详细见文档：[Configuration](https://www.netlifycms.org/docs/configuration-options/#collections)和[Widgets](https://www.netlifycms.org/docs/widgets/)

<pre><code class="language-css">backend:
  name: git-gateway
  branch: master 
publish_mode: editorial_workflow
media_folder: "/assets/img" 
collections: 
- name: "post" 
  label: "Post" 
  folder: "/_posts" 
  sort: "date:desc" 
  create: true
  slug: "\{\{year\}\}-\{\{month\}\}-\{\{day\}\}-\{\{slug\}\}"
  fields: 
    - {label: "Permalink", name: "permalink", widget: "string", default: "/YYYY/MM/DD/root", required: false}
    - {label: "Title", name: "title", widget: "string", tagname: "h1"}
    - {label: "Subtitle", name: "subtitle", widget: "string", tagname: "h3"}
    - {label: "Cover Image", name: "cover", widget: "image",required: false}
    - {label: "Author", name: "author", widget: "string"}
    - {label: "Tags", name: "tags", widget: "string", required: true}
    - {label: "Publish Date", name: "date", widget: "datetime", format: "YYYY-MM-DD"}
    - {label: "Body", name: "body", widget: "markdown"}
    - {label: "Layout", name: "layout", widget: "hidden", default: "post"}
</code></pre>

 然后在你网站的主页`<head>`里加上：

<pre><code class="language-css">&lt;script src="https://identity.netlify.com/v1/netlify-identity-widget.js"&gt;&lt;/script&gt;</code></pre>

在`</body>`前加上：

<pre><code class="language-css">&lt;script&gt;
     if (window.netlifyIdentity) {
        window.netlifyIdentity.on("init", user => {
           if (!user) {
              window.netlifyIdentity.on("login", () => {
                 document.location.href = "/admin/";
              });
            }
         });
     }
&lt;/script&gt; </code></pre>

由于我的Jekyll使用的是H2O主题，所以我`<head>`部分加在`/_includes/head.html`，`</body>`部分加在`/_layouts/default.html`

**3.Netlify绑定github的repo**

Netlify：[app.netlify.com](https://app.netlify.com/)

按照向导创建好

![](/assets/img/2019-04-29_133700.png)

注意在Build command和Publish directory填写`jekyll build`与`_site`下图是配置好的设置里的，如果是绑定github上Jekyll博客的话，向导应该会自动填写

![](/assets/img/2019-04-29_145037.png)

建好之后如下

![](/assets/img/2019-04-29_133822.png)

点击Domain Settings设置域名，如果原先向导有填，此处应该已经建好一个xxx.com和www.xxx.com，但是后面会有个Check DNS configuration，点击可以查看帮助，建议将域名解析到Netlify上，我原先将域名解析到github，后续Deploy后，在Preview里后台登录没有问题，而站点登录时则出现`Failed to load settings from /.netlify/identity`错误，设置好如下图，其中Netlify二级域名可自己设定，方便CNAME解析

如果不想将域名解析到Netlify，也可以直接用在Netlify设置的二级域名`xxx.netlify.com/admin`登录后台

![](/assets/img/2019-04-29_145948.png)

在Access control的OAuth绑定第1步在OAuth Apps注册的ID和Secret

![](/assets/img/2019-04-29_151617.png)

**4.Netlify Deploy及开启Identity与Git Gateway服务**

选择Deploy点击Deploy Site

![](/assets/img/2019-04-29_151856.png)

部署完成后，点击Identity启动服务，在Registration选择Invite only，在Git Gateway授权并开启服务

![](/assets/img/2019-04-29_152047.png)

![](/assets/img/2019-04-29_152118.png)

**5.用户设置及后台登录**

后台管理地址：xxx.com/admin

官方后台[demo](https://cms-demo.netlify.com/#/collections/posts)

在刚刚Registration页面里点击Identity tab可进行用户管理，如需密码设置和邮箱验证可在后台管理的登录界面完成
