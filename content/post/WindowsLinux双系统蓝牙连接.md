---
title: Windows、Linux 双系统蓝牙连接
date: 2020-01-01 09:06:12
tags: [linux]
---
 一般笔记本安装实体 Linux 双系统后，切换系统后蓝牙设备总有这样那样的问题，这里将使用修改 key 值的方法实现双系统连接蓝牙设备。
--------
#### Windows 下连接设备
转至 Linux，连接设备后切换至 su 账户
执行`cd /var/lib/bluetooth/`
当前目录下会有电脑的蓝牙地址，进入该地址，ls 查看已连接的设备
选定已确定的蓝牙设备，使用文本编辑器查看 info 文件
按照简书上的教程，在这里找到 [LinkKey] 值即可，但我使用的键盘 info 文件却不是这样构成的
```
[IdentityResolvingKey]
Key=FD79B32764A287D4AC210ABD9EFE2844

[LongTermKey]
Key=5D5F5EC78589D2882F5142FE86D0455E
Authenticated=0
EncSize=16
EDiv=57930
Rand=13493215272868294029

```
### 如果类似我这种情况，需要记录 IdentityResolvingKey 和 LongTermKey 两项数值
## 回到 Windows，下载 PSTools 工具，这里请自行百度，目前还不会插入链接……

执行`PsExec.exe -s -i regedit`
## 找到 HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\BTHPORT\Parameters\Keys\
由于这里我并不能使用 [LinkKey]，所以操作稍有不同
## 在左侧目录找到蓝牙设备地址，双击进入，分别修改 [IRK][LTK] 两项
## reboot


F2:CE:2F:54:C9:52
