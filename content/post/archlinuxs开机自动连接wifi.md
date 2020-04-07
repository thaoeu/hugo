
---
title: Archlinux 开机自动连接 wifi
date: 2020-02-02 08:18:26
tags: [linux]
---

使用 wifi-menu 命令选择 wifi 输入密码。

这里使用的是 netctl.
##### 一、安装必需管理工具


```
pacman -S dialog netctl
```

##### 二、查看 /etc/netctl/ 文件

该目录下会有 wifi-menu 留下的配对文件。root 账户可查看文件内容，包含网卡名、ssid、密码等。

##### 三、启动 netctl 服务

	systemctl start netctl-auto@wlp100s0.service
	systemctl enable netctl-auto@wlp100s0.service

wlp100s0 是网卡名，按上述文件内容填写，重启即可。
