---
title: "如何在hugo上搭建博客"
date: 2020-02-06T15:51:16+08:00
draft: false
---
# 搭建博客

1. 首先去官网下载hugo，如果安装成功，在命令行打出：hugo -version会显示版本号信息。
2. 在命令行输入：hugo new site 固定的自己的专属仓库命名
3. 进入这个文件：cd 仓库名，创建一个仓库：git init,然后下载hugo的默认博客主题：git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke，之后将主题放到站点配置：echo 'theme = "ananke"' >> config.toml。
4. 然后新建你的第一个博客：hugo new posts/我的第一个博客 .md，新建好的.md的文件内容有：博客的头部内容：title、时间：date、默认草稿形式：draft(默认为true，你写完博客要把这个改为false，不然就是一个草稿形式)。
5. 写博客的形式跟markdown一样：
    * 标题分6级：#、##、###……
    * 有序：1.2.
    * 无序：*
    * 插入图片：![图片描述](图片链接)
    * 插入链接：[描述](链接)
    * 代码块：用~~~分隔
6. 然后命令行输入：hugo server -D就可以查看你的效果了，它会给你一个链接localhost:1313，然后点击就可以查看。
7. 然后你还可以配置你的主题，打开文件config.toml,文字更改找languageCode，改主题标题找title,主题设置找theme(不过首先你要下载好那个主题，不然你的博客就生成不了，下载主题可以去hugo的官网去看步骤三)
8. 生成静态网页：hugo -D，这时你的文件夹会出现一个public的文件，如果你要上传到GitHub里面。你就需要创建一个.gitignore在里面输入/public/把public隐藏掉。
9. 之后你就在GitHub建一个仓库就可以去上传了。
