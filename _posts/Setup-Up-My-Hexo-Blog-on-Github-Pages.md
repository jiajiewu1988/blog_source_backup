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
    - github允许每个account有一个repository作为github page repo，repo的名字必须符合 **<your username>.github.io** 的 format. 比如 jiajiewu1988.github.io
- 安装hexo
    - 首先要安装 **nodejs** 和 **npm**，hexo 由 npm 来管理
    - 安装hexo package: `npm install hexo-cli -g`
- 创建hexo project
    - use command: `hexo init <your_project_name>`
- 设置 Deployment to Github
    - 安装 hexo 的 git plugin:
        - `npm install hexo-deployer-git --save`
    - 修改 hexo config - _config.yml:
        - ```yml
          deploy:
            type: git
            repo: <github repo link>
            branch: <optional>
            message: <optional>
          ```
        - **type** 和 **repo** 是必须的。
        - 如果使用github, branch的值为空，那hexo会自动detect branch.
        - message的默认值是 `Site updated \{\{ now\('YYYY-MM-DD HH:mm:ss'\) \}\}`
- Setup SSH Key with Github
    - 为了方便 deploy, 建议使用 ssh 方式来同步 git repo
    - Follow 以下链接来 setup ssh key
        - [Generating a new SSH key and adding it to the ssh-agent](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)
        - [Adding a new SSH key to your GitHub account](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/)


# 更换 hexo theme

- 找到想要更换的 theme，**git clone** 到hexo下的theme directory中
`git clone https://github.com/hexo-theme-again.git themes/again`
- 到hexo主目录下的_config.yml下修改**theme**的值
`theme: again`

# 管理 media files

[Hexo Official Assets Folder Doc](https://hexo.io/docs/asset-folders.html)