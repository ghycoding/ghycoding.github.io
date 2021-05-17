---
title: 搭建Blog的初步体验
cover: 'https://wallroom.io/img/3840x2160/thumb/bg-97789d2.jpg'
copyright: false
abbrlink: 5fc84f8a
top: 10
categories:
  - hexo
---

## Hexo搭建步骤   
1.安装Git
2.安装Node.js
3.安装Hexo
4.GitHub创建个人仓库
5.生成SSH添加到GitHub
6.将hexo部署到GitHub
7.设置个人域名
8.发布文章


## 安装git
windows：到git官网上下载,Download git,下载后会有一个Git Bash的命令行工具，以后就用这个工具来使用git。
&emsp;&emsp;&emsp;&emsp;&emsp;安装完成之后git --version 查看当前版本，如果没有需要查看是否添加到环境变量


## 安装node
Hexo是基于nodeJS编写的，所以需要安装一下nodeJs和里面的npm工具。
1、[nodejs](https://nodejs.org/en/)选择LTS版本就行了（稳定版本）。
2、安装完成之后 
```
node -v  // 查看 node版本号
npm -v  // 查看npm 版本号  npm是node的包管理工具，用来下载node插件
```
3、安装cnpm （淘宝镜像），安装完成之后需要添加环境变量然后cnpm -v 查看版本
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```


## 安装hexo
安装好环境之后可以直接使用[hexo](https://hexo.io/zh-cn/)命令来创建blog
```
npm install -g hexo-cli
```
使用hexo -v 查看版本
cd 到根目录下
```
cd blog //进入这个blog文件夹
cnpm install
```
安装完成之后我们来看看对应的目录
![图一](https://z3.ax1x.com/2021/05/11/gULm1x.png)
+ node_modules: 依赖包
+ public：存放生成的页面
+ scaffolds：生成文章的一些模板
+ source：用来存放你的文章 （自己定义目录）
+ themes：主题 （我的博客是用的[hexo-theme-butterfly](https://github.com/jerryc127/hexo-theme-butterfly)）
+  _config.yml: 博客的配置文件
```
hexo g
hexo s
```
启动hexo 服务，在浏览器访问localhost:4000即可
