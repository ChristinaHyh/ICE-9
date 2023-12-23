---
layout: post
title: 'Obsidian+Zotero助力科研'
date: 2023-04-23
author: Christina
tags: 工具
subtitle: 研究生的自我修养

---


---

## 前言

时隔两年，重启博客。这两年，思想流浪了很久，在各种化学反应中愣是没沉淀完全，终还是溶解在这信息爆炸的洪流之中了。

前些日子连绵的雨仿佛让我都要发霉了，连同脑中那些离散的想法，慢慢发酵，逐渐腐烂。

过载的信息，凌乱的想法，日积月累的知识，感觉自己都快被扔进学术垃圾桶了。 

于是，在世界读书日的今天，我决心重回这个地方，思考、输出。



这篇POST介绍的是如何使用Obsidian和Zotero联动管理学术文献与笔记，以及研究生的自我修养工作流，我会在自己的不断测评调整中慢慢完善它，主要内容包括：

- [个人知识管理库的构建](https://hyahui.com/ob-for-research#%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E7%AE%A1%E7%90%86%E5%BA%93%E7%9A%84%E6%9E%84%E5%BB%BA)
  - 基于「大脑外延」思想的**专业特色知识结构库**构建
  - Obsidian与Zotero联动配制与使用
  - Ob与Zotero插件推荐
- [高效工具的调用](https://hyahui.com/ob-for-research#%E9%AB%98%E6%95%88%E5%B7%A5%E5%85%B7%E7%9A%84%E8%B0%83%E7%94%A8)
  - flomo——零碎知识收集器
  - Diigo——文献纲要提炼器
  - X-mol——文献入库筛选器
  - TickTick——任务清单制定器
  - Anki——学术名词积累器
- [如何用此库为自己赋能](https://hyahui.com/ob-for-research#%E5%A6%82%E4%BD%95%E7%94%A8%E6%AD%A4%E5%BA%93%E4%B8%BA%E8%87%AA%E5%B7%B1%E8%B5%8B%E8%83%BD)
  - 提高学术写作精准用词能力
  - 构建特色的专业知识结构
  - ……

---

## 个人知识管理库的构建

### 基于「大脑外延」思想的**专业特色知识结构库**构建

**底层思想源自船长的大脑外延公开课：[[1]](https://lrl.lonelyreader.com/#/teachingActivities/vod?productKeyId=C195&type=VOD&activityKeyId=cDygohtzQJivX1ulULRTUA) [[2]](https://lrl.lonelyreader.com/#/teachingActivities/vod?productKeyId=C195&type=VOD&unitId=47254&activityKeyId=_CRoCg-gSMez-hXGDQ66nQ)**

> 放置盒（缓存）：想法搜集器，用于记下那些在你脑中一闪而过的想法
>
> 发散数据库（硬盘）：概念仓、输入源，结构化记录那些后期不断发散让你记也记不住的知识
>
> 收敛数据库（算法）：目标导向的工程任务，基于工程目标的主动式学习
>
> 任务清单（执行程序）：细化成可执行的重复动作



我认为，一个工具要好上手，那它一定要是足够“简单的”。“适配”/“个性化”则是这个工具的拓展。因此，我只共享了在“科研”这个基调下的简单版Ob库——Ob for Research（OFR），我尽可能简约化，但我不得不承认，这个库里存在着我的小习惯，这些你都可以在后期慢慢使用中去调整以适配你自己。

在介绍如何使用OFR库之前，我先简单介绍一下该库的构建逻辑。这是我现阶段的想法，也许在未来我会慢慢优化它。

1. 分类的逻辑：OFR库以物理空间上对房间的划分来进行工作区分类——在什么地方，做什么样的事。
2. 运转的逻辑：
   - Admin-速览/概念集 → 发散数据库（硬盘）：用于存放特色知识结构中涉及的关键概念
   - Admin-速览/任务版 → 放置盒（缓存）& 收敛数据库（算法）&  任务清单（执行程序）

3. 方法论：目标设定与实现（待更）



以下才是该库的使用说明书：

```
├─Admin-速览
├─Blog-博客
├─Lab-实验室
│  ├─分析结果
│  ├─原始数据
│  └─试验手册
├─Library-图书馆
│  ├─专业书籍
│  └─自由梦想
├─Literature-文献库
│  ├─mdnotes
│  ├─pdfs
│  └─文献专题
├─Study-书房
│  ├─指南方法
│  ├─研究方案
│  └─论文草稿
└─Warehouse-库房
    ├─Assets
    │  └─2023
    ├─Scripts
    ├─Templates
    ├─任务库
    ├─写作库
    │  ├─副词性
    │  ├─动词性
    │  ├─名词性
    │  ├─固定搭配
    │  ├─形容性
    │  └─连接词
    └─概念库
        ├─概念仓
        └─概念集
```

#### Admin-速览

顾名思义，这里是数据库的合集，为你提供最直接的视角

#### Blog-博客

这里是产出的圣地，你可以分享你的见解、思考，毕竟“输出带动输入”也是一种很不错的学习方式

#### Lab-实验室

用来存放那些与实验有关的东西，如果你希望在ob里也能看到其他格式的文件，可以进行如下操作：

![](/assets/img/2023-12-20_222727.jpg)      

#### Library-图书馆

对我来说，我的藏书有两种，一类是与科研相关的专业书籍，一类是那些另外沉浸的“杂书”，你可以根据你的习惯进行分类，这里没有什么规则

#### Literature-文献库

这里包括mdnotes，pdfs和文献专题，mdnotes用于存放基于模板创建的Zotero和ob双链的空白笔记，pdfs用于存放Zotero保存的附件文献pdf，这两个文件夹里的文件都是通过联动自动创建的，如果你想更改文件夹名，请记得在Zotero也修改相应的文件夹名。文献专题用于存放针对某一专题的文献总结，如果想更加便捷地使用，可以通过obsidian的quickadd插件实现

#### Study-书房

这里是一个可以专心与安静工作的地方，包括指南方法、研究方案和论文草稿，研究方案和论文草稿我设置了便捷按钮，可点击侧栏按钮直接根据模板创建笔记（模板在库房的Templates）。指南方法我常用于存放检测方法、仪器使用方法等。

在OFR库的右上侧栏有一个日历板块，单机相应的日期可以创建日记，也许你会想把日记存放在书房，所以我把日记位置的设置方法放在了这里：

![](/assets/img/ 2023-12-20_223557.jpg)     

#### Warehouse-库房

这里存放了模板、脚本和图片数据，正如库房一般。

- Assets用于存放ob的所有图片，我会根据年份文件夹进行分类

- Scripts和Templates用于存放脚本和模板

- 任务库，写作库，概念库分别用于存放速览中数据库表任务板、写作典和概念集所创建/所需要展示的文件

这里对“概念卡片”和“概念合集”快捷按钮做个说明：概念卡片用于记录单个名词的释义，概念合集用于收集某些相近概念卡片合集



我在OFR插件中保留了一些我觉得不错的ob插件，如果你想了解更多，可以进一步探索，但不要忘记，插件是为了服务记录笔记本身，所以最重要的还是，记录。



### Obsidian与Zotero联动配置与使用（基于Windows操作系统）

#### 0.软件下载

- 文献信息管理软件：[Zotero](https://www.zotero.org/) - 考虑到插件兼容性，建议安装6.0版本

- zotero插件：

  - [Zotfile](https://zotfile.com/) - 用于自动重命名附件并存放到指定目录 （[直接下载](https://github.com/jlegewie/zotfile/releases/download/v5.1.2/zotfile-5.1.2-fx.xpi)）
  - [Mdnotes](https://argentinaos.com/zotero-mdnotes/) - 基于模板将文献生成markdown笔记（[直接下载](https://github.com/argenos/zotero-mdnotes/releases/download/0.2.3/mdnotes-0.2.3.xpi)）
  - [Better Bibtex](https://retorque.re/zotero-better-bibtex/) - 用于生成citation key，实现zotero与obsidian的联动（[直接下载](https://github.com/retorquere/zotero-better-bibtex/releases/download/v6.7.136/zotero-better-bibtex-6.7.136.xpi)）
  - [Zotero-pdf-translate](https://zotero.yuque.com/staff-gkhviy/pdf-trans)（可选） - 在zotero中实现划词翻译等功能（[直接下载](https://github.com/windingwind/zotero-pdf-translate/releases/download/v1.0.25/zotero-pdf-translate.xpi)）

- Python环境及包管理工具：[Anaconda](https://www.anaconda.com/) - 安装时需要添加环境变量（[直接下载](https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Windows-x86_64.exe)），安装完成后，运行以下命令安装相应模块：

  ```
  conda activate base
  
  pip install pyperclip bibtexparser
  ```

  <u>注：如在此步安装有困难，可自行使用搜索引擎进行搜索以寻求解决方案，此处不赘述</u>

- 文件格式转换工具：[Pandoc](https://pandoc.org/installing.html) - 安装完成后可在命令行输入`pandoc --version`查看安装信息，同样需要添加环境变量

- [Ob for Research库](https://github.com/ChristinaHyh/ICE-9/releases/download/zotero-ob/OFR.zip)

[一键打包下载Zotero及其插件与Anaconda（更新日期：2023-11-25）](https://github.com/ChristinaHyh/ICE-9/releases/download/zotero-ob/Zotero-Ob.zip)

#### 1.联动配置

- zotero基础设置：菜单栏「编辑」→「首选项」，设置zotero数据与pdf文件存储位置，在本Ob for Research库，pdf储存在`X:\…\Ob for Research\Literature-文献库\pdfs`

  ![](/assets/img/zotero-1.png)      
  
  ![](/assets/img/zotero-2.png)  
  
- 安装zotero插件：菜单栏「工具」→「附加组件」，选择上述下载的zotero插件（*.xpi）进行安装

  ![](/assets/img/zotero-3.png) 

- 插件设置：

  - Zotfile：「工具」→「ZotFile Preference」，实现在zotero条目中右键选择`Attach New File`后将桌面的pdf文件重命名并移动到ob库的指定文件夹下，以下为我的配置，其中Renaming Rules可参考[官方文档](http://zotfile.com/#renaming-rules)根据自己的喜好修改

    ![](/assets/img/zotero-4.png) 

    ![](/assets/img/zotero-5.png) 

    ![](/assets/img/zotero-6.png) 

  - Mdnotes：「工具」→「Mdnotes首选项 」，实现在zotero条目中右键选择Mdnotes→创建Mdenotes文件后在ob库指定位置创建笔记，以下是我的配置，供参考

    ![](/assets/img/zotero-7.png) 

    ![](/assets/img/zotero-8.png) 

  - Better Bibtex：「工具」→「Better BibTex 」→「打开Better BibTex 首选项」，自动创建zotero与ob联动的citation key，也可在ob中使用`[[citation key]]`实现笔记直接的相互引用

    ![](/assets/img/zotero-9.png) 

    ![](/assets/img/zotero-10.png) 

- 导出文献库到ob库

  - 右键「我的文库」→「导出文献库 」，选择「Better BibLaTeX 」格式并勾选「保持更新」，点击确定后将导出的文件命名为`My-Literature-Library.bib`保存到`X:\…\Ob for Research\Warehouse-库房\Scripts`中

    ![](/assets/img/zotero-11.png) 


至此，zotero与obsidian的联动配置就完成了

#### 2.联动使用

- 选择筛选后需要入库的文献，填写DOI添加条目，也可使用zotero的chrome插件直接一键添加

  ![](/assets/img/zotero-12.png) 

- 下载文献原文pdf保存在桌面后，在新增条目右键选择`Attach New File`，此时会弹窗让你确认是否将pdf文件重命名并保存到指定文件夹，一般会默认选择最新保存到桌面的pdf文件，注意要避免在其他软件打开该pdf文件以避免重命名与移动文件不成功。根据个人习惯也可使用zotero插件[zotero-scihub](https://github.com/ethanwillis/zotero-scihub)实现自动下载pdf文件

  ![](/assets/img/zotero-13.png) 

- 选择需要做笔记的条目创建笔记到ob库

  ![](/assets/img/zotero-14.png) 

- 固定citation key引用，固定后可以看到一个小图钉的图标，这一步骤是防止更改citation key后影响双链

  ![](/assets/img/zotero-15.png) 

其他操作就是点点点，试试就知道了

---

## 高效工具的调用

这一部分我还没想好如何去详细介绍这些工具，但下列提纲是我对这些工具最简单的介绍，如果你感兴趣，你可以自己先探索。

### [flomo](https://flomoapp.com/)——零碎知识收集器

- [PDF.js+Chrome+flomo=构建思想闪光流](https://hyahui.com/pdfjs-flomo)

### [Diigo](https://www.diigo.com/index)——文献纲要提炼器



### [X-mol](https://www.x-mol.com/)——文献入库筛选器



### [TickTick](https://dida365.com/)——任务清单制定器



### [Anki](https://apps.ankiweb.net/)——学术名词积累器

- [PDF.js+Chrome+Anki=构建语境习词库](https://hyahui.com/pdf-js-anki)

  

---

## 如何用此库为自己赋能
