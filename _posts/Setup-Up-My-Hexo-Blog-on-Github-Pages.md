---
title: Setup Up My Hexo Blog on Github Pages
date: 2016-11-11 14:55:33
tags:
---

Github Pages给用户提供了很方便的Blog Hosting的解决方案，可以非常方便的用诸如hexo, jekyll等的 Static Page CRM来管理Blog。

因为题主对node.js和npm熟悉一点，就选用了hexo，来管理个人的github Pages
<br /><br />

# Blog Initiation

- Create Git Repo on Github
    - github允许每个account有一个repository作为github page repo，repo的名字必须符合 **\<your username\>.github.io** 的 format. 比如 jiajiewu1988.github.io
- 安装hexo
    - 首先要安装nodejs和npm，hexo由npm来管理
    - 安装hexo package: `npm install hexo-cli -g`
    