---
layout: post
title: 'Hello Jekyll'
date: 2019-04-23
author: Gra
cover: ''
tags: jekyll ThemeH2O githubpage
---


 前些日子忽然有人问 前端这么多年你有技术blog吗 
 
 想了想blog是啥 为啥没有 为啥要有 

 再后来看到了知乎上的这篇 
>[为什么你要写博客? -知乎](https://zhuanlan.zhihu.com/p/19743861)

* 不是生活杂记、不是流水账、不是牢骚、不是抱怨、不是心情琐记……；

* 有目的地写，要务实，追求质量；

* 承认真实的自己，不要吹嘘，不要装逼，无需讨好读者；

* 记录自己学习、思考、总结的过程；

* 分享你的故事、所得、感想、经验；

* 提供持续学习的动力 积累更多的知识 提高自己把事情讲清楚的能力 

* 很多东西你以为懂了，但当你在写下来的时候，你就觉得无从下手了。 

那么 今天开始 就写写blog 记录一下自己的学习 总结 所得

看过国内那么多技术blog平台 CSDN 思否 简书 广告挺多 总觉得界面不够清爽 不如还是自己来个Github page 还能学习git的能力



## 搭建Github Page

  在github上 新建一个叫做 username.github.io的库 github默认把这个当作github page setting 打开github page 

## 过程

github 官方使用的是jekyll 那么也用这个吧 [jekyll中文](https://www.jekyll.com.cn)

windows下安装ruby环境 [下载](https://rubyinstaller.org/downloads/)

选择with devkit 下载完安装

命令行 安装jekyll 和bundler gems

```gem install jekyll bundler```


git clone 了 [Theme H2O](https://github.com/kaeyleo/jekyll-theme-H2O)的模板

在目录中 启动本地服务

```bundle exec jekyll serve ```


浏览器中 打开 http://localhost:4000 


