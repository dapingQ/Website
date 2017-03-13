# Ji Lab 网站运维指南


### 储备知识

1. Git与GitHub常识
2. HTML基础
3. Linux常用命令（Windows下安装GitHub客户端的可忽略）

推荐的阅读材料有[廖雪德的Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/)以及[w3cschool HTML教程](http://www.w3school.com.cn/html/index.asp)

## 介绍

网站所采用的是 [Jekyll](jekyll.com.cn) + [GitHhub Pages](pages.github.com)的模式，代码在本地修改，通过测试直接部署到GitHub上，建议阅读以下章节前可以先熟悉以上两个工具，如果不能理解，本指南力求解释到位。

## 文件构成

文件构成大致如下（来自Jekyll中文网，与官网略有出入）
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
|
├── _includes
|   ├── footer.html
|   └── header.html
|   └── head.html
|   └── sidebar.html
|
├── _layouts
|   ├── default.html
|   └── post.html
|   └── page.html
|   
├── _posts
|   ├── 2007-10-29-why-every-programmer-should-play-nethack.textile
|   └── 2009-04-26-barcamp-boston-4-roundup.textile

├── _data
|   └── members.yml
|
├── _site
|
└── index.html


