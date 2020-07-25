---
title: "Linux Fcitx 挂载小鹤音形"
date: 2020-05-30T15:46:04+08:00
TableOfContents: true
gitment: true
tags: [Fcitx]
draft: flase
---
网上说码表挂接几乎是最简单的 Linux 任务<(_ _)>

然而我每次安装都磕磕绊绊

这次特意翻看了下 Fcitx-rime 文档，才发现一直以来我都在走弯路

码表挂接确实非常简单
--------

安装软件包

`pacman -S fcitx fcitx-configtool fcitx-im fcitx-rime`

--------
前往[小鹤网盘](flypy.ys168.com) 下载码表

位于网盘：小鹤音形挂接第三方目录下：Rime 平台鼠须管 for macOS.zip

文件名是 macOS，Linux 挂接完全可用

下载后解压

将 Rime 文件夹内容添加到~/.config/fcitx/rime

执行 fcitx-configtool 在面板添加输入法

完毕
