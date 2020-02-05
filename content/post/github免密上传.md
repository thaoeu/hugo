---
title: github免密上传
date: 2020-02-01 08:18:26
tags: 
---
## github免密上传
参考地址[vampire's blood](https://blog.csdn.net/weixin_42216574/article/details/93009417) 
首先确定ssh公钥以上传到github

`git config --global credential.helper store ` 

 git push 时记住密码

`git config --global push.default simple` 
