---
title: 关于hexo博客的一些小知识
date: 2018-07-30 14:18:29
tags:
---
## 不知道hexo博客能不能支持markdown预览

## hexo博客能不能支持图床
比如极简图床之类的微博图床

## hexo博客的主题是如何设置的？
这个东西其实还挺关键的
-----
1. https://github.com/hexojs/wiki/Themes 上面有主题合集。
2. 在里面找到主题的github主页，然后进入该主页。
3. 复制它的SSH地址
4.  
    ```
        cd ~/Desktop/myBlog/themes
        git clone xxxxx.git
        vim ~/Desktop/myBlog/_config.yml
    ```
5. 把_config.yml的第75行改成`theme: 主题名`（* 注意有空格 *），`:wq`退出保存
6.  
    ```
    hexo generate
    hexo deploy
    ```
7. 等一分钟，刷新博客页面即可。