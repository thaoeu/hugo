---
title: "Vimer 是如何使用 Htop 的"
date: 2020-02-22T15:25:48+08:00
TableOfContents: true
gitment: true
tags: [vim, linux]
draft: flase
---
Htop 是一款开源的交互式进程管理器，很多 Linux 发行版都内置了它。
但默认的 Htop 是使用方向键进行进程的选择，我这种没有方向键的用户就不便使用。
在 Htop 的仓库里也有人提过这个需求，但官方给的方案是－使用 Alt+hjkl 移动。
但偏偏不巧的是，我还是个 Dwm 用户，我的 Alt 键被占用了。
所以
```
yay -S htop-vim-git
```

htop-vim-git 完美的解决了 Htop 下移动选择进程的问题，但它也占用了诸如：k, l 的一系列按键。
如果你有方向键，或者你能接受 Alt+hjkl 的移动方式，那我建议你使用原版的 Htop.

这里顺带介绍下 Htop 的一些快捷键。

- F1, h, ?		帮助
- F2, Shift+s	设置
- F3, /			搜索
- F4, \			筛选
- F5, t			目录树
- F6, <>		切换排序方式
- F7, ]			提高进程优先级
- F8, [			降低进程有限级
- F9, k			杀死进程
- F10, q		退出

在 htop-vim-git 下快捷键稍有不同。

- F1, h, ?		帮助
- F2, Shift+s	设置
- F3, /			搜索
- F4, \			筛选
- F5, t			目录树
- F6, <>		切换排序方式
- F7, ]			提高进程优先级
- F8, [			降低进程有限级
- F9, Shift+k	杀死进程
- F10, q		退出
- p				切换 Command 简称
- ., o,	,		选择排序方式

