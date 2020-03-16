---
title: "Ranger 使用"
date: 2020-02-14T09:22:51+08:00
draft: flase
---
## Ranger 特性

Ranger 是一个终端下的文件管理器，提供了一个类 Vim 的操作环境。
[Ranger 的项目代码](https://github.com/ranger/ranger)


## 查看 ranger 可选依赖
`pacman -Qi ranger`

	pacman -Qi ranger

如使用 Aur

	`yay -Qi ranger`

确认安装 w3m 或 python-ueberzug

修改 range 配置文件：~/.config/ranger/rc.conf

如无则生成默认配置文件`ranger --copy-config=all`

找到配置文件中的`set preview_images` 行

修改为`set preview_images true`

在`set preview_images_method w3m` 选择想要预览图片的依赖，默认 w3m

在 ranger 窗口内按`zi` 开启预览

![](https://raw.githubusercontent.com/thaoeu/Mypic/master/title.png?token=AIDRQMWW4DFW7G5FCYGVOZC6IYXKE)




![Hatsune.Miku.jpg](https://i.loli.net/2020/02/25/yYglxvULAOrWJSb.jpg)


## Ranger 配置文件：rc.conf

Ranger 的使用方法都包含在配置文件中了，这里我直接从配置文件
