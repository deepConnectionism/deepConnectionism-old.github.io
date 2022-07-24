---
layout: post
title:  "Github Pages+jekyll搭建个人博客"
date:   2022-07-24 19:52:00 +0800--
categories: [工具]
tags: [GAN, interesting]  
---

## Github Pages+jekyll搭建个人博客

### 1. fork 一个喜欢的主题仓库

http://jekyllthemes.org/page4/ 上面有各种可以选择的主题。

我选择了一个：有哪些简洁明快的 Jekyll 模板？ - 知乎用户的回答 - 知乎
https://www.zhihu.com/question/20223939/answer/549634169

直接fork 这个 https://github.com/oukohou/oukohou.github.io

然后修改名字为自己的 用户名.github.io

### 2. git clone 到本机

    git clone git@github.com:deepConnectionism/deepConnectionism.github.io.git
    cd  deepConnectionism.github.io

### 3. 使用VScode 在本地编写 markdown 文件

*_posts* 在文件夹中创建一个 .md 文件。格式命名year-month-day-title.md。

提交，推送即可。

### 4. 本地构建网站

首先，需要安装 Jekyll

安装环境，参考：https://jekyllrb.com/docs/installation/ubuntu/

    sudo apt-get install ruby-full build-essential zlib1g-dev

    echo '# Install Ruby Gems to ~/gems' >> ~/.zshrc
    echo 'export GEM_HOME="$HOME/gems"' >> ~/.zshrc
    echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.zshrc
    source ~/.zshrc

    gem install github-pages

如果报错：可以

    vim Gemfile
    添加 gem "jemoji"

运行

    bundle install
    bundle exec jekyll server --trace

就可以在 http://127.0.0.1:4000/ 看到本地实时编辑的博客了。

我们就可以愉快的在本地写博客，实时用浏览器预览，最后再推送到github 上了。

好了，我可以愉快的抛弃 csdn 了！

#### 其他参考资料：

    https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/

    https://hellolzc.github.io/2016/04/used-jekyll-to-create-my-github-blog/



