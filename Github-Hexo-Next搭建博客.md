---
title: Github+Hexo+Next搭建博客
comments: true
date: 2020-09-17 22:16:10
tags:
    - hexo
    - next
    - github
---

## 什么是Hexo？

[Hexo](https://hexo.io/zh-cn/) 是高效的静态站点生成框架，她基于 [Node.js](https://nodejs.org/) 。 通过 Hexo 你可以轻松地使用 Markdown 编写文章，除了 Markdown 本身的语法之外，还可以使用 Hexo 提供的 [标签插件](https://hexo.io/zh-cn/docs/tag-plugins.html) 来快速的插入特定形式的内容。

<!--more-->

---------------------------------------

## 安装Hexo

### 安装前提

安装 Hexo 非常简单。但在安装之前，您必须检查电脑中是否已安装下列应用程序:

{% note default %}

- **Node.js**
- **Git**

{% endnote %}

### 安装 Git

{% note info %}

**Windows** 用户 直接在 [官网](https://git-scm.com/download/win) 下 ```Git``` 很慢, 可以通过 [这个网页](https://github.com/waylau/git-for-win) 下载

{% endnote %}

安装完 ```Git``` 后，右键打开 ```Git Bash Here``` ，输入 ```git --version``` ,出现版本信息就说明安装成功了。

``` bash
zhixuan@DESKTOP-2MMI2OK MINGW64 /d/desktop
$ git --version
git version 2.28.0.windows.1
```

### 安装Node.js

接下来安装 ```Node.js``` ，在 [官网](http://nodejs.cn/download/) 下载即可。

在命令行输入 ```node -v``` 和 ```npm -v``` ，出现以下信息说明成功了。

``` cmd
Microsoft Windows [版本 10.0.18363.1082]
(c) 2019 Microsoft Corporation。保留所有权利。

C:\Users\zhixuan>node -v
v12.18.3

C:\Users\zhixuan>npm -v
6.14.6
```

### 安装Hexo

如果你的电脑中已经安装上述必备程序，那么恭喜你！只需要使用 ```npm``` 即可完成 ```Hexo``` 的安装。

``` bash 
$ npm install -g hexo-cli
```

安装 Hexo 完成后，我们首先需要为我们的项目创建一个 ```指定文件夹``` (例如我在 D 盘目录下创建了一个文件夹 blog ```D:\blog``` )，在指定文件夹中执行下列命令， Hexo 将会在指定文件夹中新建所需要的文件。

``` bash
$ hexo init
```

等待安装，安装后，```blog``` 的目录如下。
```
.
├── _config.yml
├── package.json
├── scaffolds
├── source
|   ├── _drafts
|   └── _posts
└──
```

我们继续执行命令

```bash
$ hexo g
$ hexo s --debug
```

{% note success %}

```Hexo``` 将 ```source``` 文件夹中除 ```posts``` 文件夹之外，开头命名为 (下划线)的文件 ```/``` 文件夹和隐藏的文件将会被忽略。```Markdown``` 和 ```HTML``` 文件会被解析并放到 ```public``` 文件夹，而其他文件夹会被拷贝过去。
这个时候，我们在浏览器中访问 http://localhost:4000/ ，就可以看到基于 Hexo 的默认主题的原型：

![预览](https://cdn.jsdelivr.net/gh/zhixuan666/gh-blog@master/photo/Github-Hexo-Next搭建博客/hexo-next-one-1.png)

{% endnote %}

## 安装Next主题

### 下载Next主题

依旧是在当前目录下，使用 ```Git``` 来 ```checkout``` 代码:

```bash
$ hexo g
$ hexo s --debug
```