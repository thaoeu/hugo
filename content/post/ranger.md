---
title: "Ranger"
date: 2020-02-14T09:22:51+08:00
draft: flase
---
## 查看ranger可选依赖
`pacman -Qi ranger` 

	pacman -Qi ranger

如使用aur

	`yay -Qi ranger` 

确认安装w3m或python-ueberzug

修改range配置文件:~/.config/ranger/rc.conf

如无则生成默认配置文件`ranger --copy-config=all` 

找到配置文件中的`set preview_images` 行

修改为`set perview_images true` 

在`set preview_images_method w3m` 选择想要预览图片的依赖，默认w3m

在ranger窗口内按`zi` 开启预览

![](https://raw.githubusercontent.com/thaoeu/Mypic/master/title.png?token=AIDRQMWW4DFW7G5FCYGVOZC6IYXKE)
