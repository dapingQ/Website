# Ji Lab 网站运维指南


### 储备知识

* Git与GitHub常识
* HTML基础
* Linux常用命令（Windows下安装GitHub客户端的可忽略）

推荐的阅读材料有[廖雪峰的Git教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/) [w3cschool HTML教程](http://www.w3school.com.cn/html/index.asp) 以及 [Jekyll中文网](jekyll.com.cn)

## 介绍

网站所采用的是 Jekyll + [GitHhub Pages](pages.github.com)的模式，代码在本地修改，通过测试直接部署到GitHub上，建议阅读以下章节前可以先熟悉以上两个工具，如果不能理解，本指南力求解释到位。

## 文件构成

文件构成大致如下（来自Jekyll中文网，与官网略有出入）

```
.
├── _config.yml
├── _drafts
|   ├── begin-with-the-crazy-ideas.textile
|   └── on-simplicity-in-technology.markdown
|
├── _includes
|   ├── footer.html #底部链接
|   └── header.html #头部导航栏
|   └── head.html #头文件
|   └── sidebar.html #新闻与学术报告页面的侧边栏
|
├── _layouts
|   ├── default.html
|   └── post.html
|   └── page.html
|   └── event.html
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
```
## 基础功能——更新与发布
### 修改内容

#### 首页大图

控制首页滚动栏的图片的文件在`./_data`下，

1. 上传照片至`./images/slider`目录下
2. 修改`./_data/slider.yml`，按照文件内的既有格式增加或删除对应元素

#### 研究方向

目前Research下只有一个页面，在`./research/index.html`，可以根据需求自行修改。

#### 增改实验室人员

如首页大图，控制文件在`./_data/member***`中，请按照既有字段修改姓名、邮箱、学位等信息。

#### 增加发表论文
控制文件为`./_data/paper.yml`，其中已经按照年份排序。

### 发布更新

```
$ git add --all
$ git commit -m "your  commit"
$ git push origin master
```

## 进阶功能——启用新功能

在最初的版本中，几个页面布局相比现在更为复杂，如需启用，请去除页面中的注释。完整版的功能在`dev`这一分支中，可在本地部署后查看。
