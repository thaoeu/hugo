---
title: "Markdown 格式预览"
date: 2020-02-17T21:50:15+08:00
TableOfContents: true
tags: [markdown]
draft: flase
---
# 标题 1
## 标题 2
### 标题 3
#### 标题 4
##### 标题 5
###### 标题 6
> 对应语法及热键
vimscript
```
#		<leader>9
##		<leader>8
###		<leader>7
####	<leader>6
#####	<leader>5
######	<leader>4
```

# 加粗、斜体、删除线

**加粗**

*斜体*

~~删除线~~

> 对应语法及热键
vimscript
```
****	<leader>b
**		<leader>i
~~~~	<leader>s
```

# 引用

> With great power comes great responsibility.
markdown
```
>
```

# 代码块
golang
```

package main

import (
    "fmt" // 导入 fmt 包，调用其中的 Println() 函数
)

func main() {
    fmt.Println("Hello，world！")
}
```

`sudo pacman -S vim`


> 对应语法及热键
vimscript
```
```		<leader>c
``		<leader>d
```

# 序号列表

* list
1. list
2. list

* list
	1. list
	2. list


> 对应语法及热键
markdown
```
* list
1. list
2. list

* list
	1. list
	2. list

```

# 链接

[感谢淡淡忧愁的主题模版](https://github.com/timzzx)

> 对应语法及热键
```
[]()	<leader>u
```


# 图片
!『这是图片无法加载时显示的文字』()

> 对应语法及热键
```
![]()	<leader>p
```

# 分隔线
--------
---


> 对应语法及热键
```
---			<leader>n

--------	<leader>l

讲真我不知道这两者的区别
```

# 表格

| 水果     | 价格    |  数量  |
| ------- | -----:   | :----: |
| 香蕉    | $1      |   5    |
| 苹果    | $1      |   6    |
| 草莓    | $1      |   7    |

> 对应语法及热键
```
| 水果     | 价格    |  数量  |
| ------- | -----:   | :----: |
| 香蕉    | $1      |   5    |
| 苹果    | $1      |   6    |
| 草莓    | $1      |   7    |
```

1. 要增加菜单在 md 文件中加入 type: standalone

2. 文章要有评论在 md 文件中加入 gitment: true

3. 文章要有目录在 md 文件中加入 TableOfContents: true

```
---
title: "博客开通"
date: 2018-07-04T17:44:01+08:00
categories: 『其他』
tags: 『其他』
gitment: true
TableOfContents: true
---
```
4. 配置 gitment 在 config.toml 加入以下配置
```
[params]
    clientID=''
    clientSecret=''
    owner=''
    repo=''
    admin=''
```
