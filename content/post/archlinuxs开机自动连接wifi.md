
---
title: archlinux开机自动连接wifi
date: 2020-02-02 08:18:26
tags:
---
archlinux开机自动连接wifi
--------
使用wifi-menu命令选择wifi输入密码。
这里系统没有安装gui使用了netctl.
#### 一、安装必须管理工具
`pacman -S dialog netctl` 
#### 二、查看/etc/netctl/下文件
该目录下会有wifi-menu留下的配对文件。root账户可查看文件内容，包含网卡名、ssid、密码等。
#### 三、启动netctl服务
`systemctl start netctl-auto@wlp100s0.service` 
`systemctl enable netctl-auto@wlp100s0.service` 
wlp100s0是网卡名，按上述文件内容填写，重启即可。
