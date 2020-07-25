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
--------

好！现在回想一下你在终端下的文件操作吧

当你想要对文件进行增删改查

你需要用 cd 命令进入目录，执行 ls 来列举目录下的文件名

或许你想了解更多，那么你还要在 ls 后面加上一系列的参数

如果目录里有海量的文件让你无法一眼看到目标

那么恭喜你，Find 命令可以帮助你

但是！不带参数的 Find 命令是无法模糊搜索的，如果想要支持模糊搜索，那么你还要加上 `-name '*.txt"`

这还没完，找到目标文件后，想要复制

你要运行 cp 并且至少要知道你目标位置的相对路径

剪切则用 mv, 或者复制后将目标文件删除

删除一个文件还好，但如果你想对一个文件夹下手

那么你还要添加 -r 参数

在这个过程中，是不会进行递归删除的

你的终端会一次次地问你：你确定删除这个吗？你确定吗？你真的确定吗？

哪怕你是一个熟练的 Linux 用户，经过这么一套操作也肯定身心俱疲

如果你不满足现状，希望从这些繁杂的操作中解放出来

那么这个开源的工具 **Ranger**, 就是为你量身定做的！

Ranger 是一款轻量的命令行文件管理器，类 vim 操作，支持强大的自定义配置
项目地址：`https://github.com/ranger/ranger`

稍微配置一下后，长这样
![](~/Pictures/CL/ranger/code.png)
![](~/Pictures/CL/ranger/picture.png)
Ranger 支持图片预览、语法高亮，并且能匹配文件类型图标

## Ranger 安装
几乎所有的 Linux 包管理器都可以直接找到 Ranger.
但我更推荐的是通过 github 源码安装
克隆 Ranger
```shell
git clone https://github.com/ranger/ranger
```
这时就可以通过下面的命令运行 Raner
```shell
cd ranger && ./ranger.py
```
当然安装是必须的
```shell
sudo make clean install
```


## Ranger 配置

到这里 Ranger 就已经安装好了，但默认的 Ranger 没有图片预览和代码高亮

现在就要开始配置 Ranger, 来实现这些功能


Ranger 支持相当多的可选依赖，如果你像我一样使用 pacman 作包管理器，只要在终端执行
``` shell
pacman -Qi ranger
```

可知
```

名字           : ranger
版本           : 1.9.3.4.gd8c363c9-1
描述           : A simple, vim-like file manager.
架构           : any
URL            : https://ranger.github.io/
软件许可       : GPL
组             : 无
提供           : ranger
依赖于         : python
可选依赖       : atool: for previews of archives 『已安装』
                 file: for determining file types 『已安装』
                 highlight: for syntax highlighting of code 『已安装』
                 libcaca: for ASCII-art image previews 『已安装』
                 mediainfo: for viewing information about media files
                 perl-image-exiftool: for viewing information about media files
                 poppler: for pdf previews 『已安装』
                 python-bidi: for bidi algorithm support
                 python-chardet: in case of encoding detection problems 『已安装』
                 python-ueberzug: w3mimgdisplay alternative 『已安装』
                 sudo: to use the "run as root"-feature 『已安装』
                 transmission-cli: for viewing bittorrent information
                 w3m: for previews of images and html pages 『已安装』
                 python-ueberzug: for previews of images and html pages 『已安装』
依赖它         : 无
被可选依赖     : 无
与它冲突       : ranger
取代           : 无
安装后大小     : 1899.65 KiB
打包者         : Matti Hyttinen <matti@manjaro.com>
编译日期       : 2020 年 02 月 03 日 星期一 02 时 55 分 52 秒
安装日期       : 2020 年 02 月 24 日 星期一 15 时 01 分 52 秒
安装原因       : 单独指定安装
安装脚本       : 否
验证者         : 数字签名

```
图片预览这里我使用的是 ueberzug

装好依赖到配置文件修改 preview_images_method 行为
```
set preview_images_method ueberzug
```

Ranger 的配置文件为 `~/.config/ranger/rc.conf`

代码高亮需要安装 highlight, 这些都能在包管理器中安装

文件类型图标插件我已经上传到了 github

下载好放到 Ranger 的 plugins 目录下即可

```
https://github.com/thaoeu/ranger/tree/master/plugins
```

这篇到这里就结束了

关于 Ranger 的其他操作留到下篇

~~写太长自己都看不下去~~
