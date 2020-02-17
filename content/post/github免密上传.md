---
title: github 免密上传
date: 2020-02-01 08:18:26
tags: [git]
---
## github 免密上传
首先确定 ssh 公钥已上传到 github

###### 设置 Git 邮箱、用户名

	git config --global user.email "example@mail.com"
	git config --global user.name "example"

###### 使 Git Push 时记住密码

	git config --global credential.helper store
	git config --global push.default simple


- 参考地址 [vampire's blood](https://blog.csdn.net/weixin_42216574/article/details/93009417)
