---
title: HappyNewYear
date: 2020-01-01 08:18:26
tags:
---
# 新年快乐!生日快乐！
## 第一篇文章
`刚开始用，还不大会用Markdown` 
--------
原计划是在一九年最后一天，也就是昨天上线的，结果由于脑子不在线导致没办法上线。 
# 二零一九年度总结
## 技术方面
### Vim
经过一大段深坑浅坑的试探，终于确定了现在使用的Vim配置，中途出了不少小问题，尝试SpaceVim那次更是损失惨重，昨天完全删除了SpaceVim，不能说是不好，只能说是不适合我，下面贴个Vimrc展示下。
```let mapleader = ","
set nu
set autoindent

call plug#begin('~/.vim/plugged')
Plug 'mhinz/vim-startify'
Plug 'easymotion/vim-easymotion'
call plug#end()
nmap <leader>f <Plug>(easymotion-s2)


nnoremap <leader>w :w<Cr>
nnoremap <leader>s <Esc>:
nnoremap <leader>ve :vsplit $MYVIMRC<Cr>
nnoremap <leader>vs :source $MYVIMRC<Cr>

noremap <leader>i <Esc>:q<Cr>

inoremap <leader>w <Esc>:w<Cr>
inoremap <c-u> <Esc> viwU



"autocmd Filetype markdown map <leader>w yiWi[<esc>Ea](<esc>pa)
autocmd Filetype markdown inoremap ,h <Esc>/<(_ _)><CR>:nohlsearch<CR>c7l
autocmd Filetype markdown inoremap ,s <Esc>/ <(_ _)><CR>:nohlsearch<CR>c5l<CR>
autocmd Filetype markdown inoremap ,n ---<Enter><Enter>
autocmd Filetype markdown inoremap ,b **** <(_ _)><Esc>F*hi
autocmd Filetype markdown inoremap ,s ~~~~ <(_ _)><Esc>F~hi
autocmd Filetype markdown inoremap ,z <sup></sup><(_ _)><Esc>F/hi
autocmd Filetype markdown inoremap ,v <sub></sub><(_ _)><Esc>F/hi
autocmd Filetype markdown inoremap ,t ** <(_ _)><Esc>F*i
autocmd Filetype markdown inoremap ,d `` <(_ _)><Esc>F`i
autocmd Filetype markdown inoremap ,c ```<Enter><(_ _)><Enter>```<Enter><Enter><(_ _)><Esc>5kA
autocmd Filetype markdown inoremap ,m - [ ] <Enter><(_ _)><ESC>kA
autocmd Filetype markdown inoremap ,p ![](<(_ _)>) <(_ _)><Esc>F[a
autocmd Filetype markdown inoremap ,a [](<(_ _)>) <(_ _)><Esc>F[a
autocmd Filetype markdown inoremap ,0 #<Space><Enter><(_ _)><Esc>kA
autocmd Filetype markdown inoremap ,9 ##<Space><Enter><(_ _)><Esc>kA
autocmd Filetype markdown inoremap ,8 ###<Space><Enter><(_ _)><Esc>kA
autocmd Filetype markdown inoremap ,7 ####<Space><Enter><(_ _)><Esc>kA
autocmd Filetype markdown inoremap ,l --------<Enter>``` 
```
使用了Neovim应该不叫Vimrc了，但还是改不了习惯。
--------

### OS
各个操作系统的配置基本也摸清定型，以后要做的就是小打小闹，老了~不想搞太多花里胡哨的东西。 
目前使用的是Win10Ltsc+Manjaro双系统，移动设备还是万年不变的Miui+IpadOS，看了别人搞 的单片机项目心水，打算趁年假期间完善下这方面的技术。
--------

### 键盘
这一年里搞的最多的就是键盘了，从客制化到量产，再从量产回归客制化，最后用Ydkb的配置完成养老需求，也算是完满了，目前主力Just60+Bggpad，Bggpad的双旋钮加Oled屏幕特性还是尝试，Qmk虽然文档完善，但奈何我是个四级都没过的渣渣，~~这Markdown中英文切换是真的恶心，有时间得考虑下英文写作~~
--------

### 其他外设
这块毫无进展，从耳机坑里跳出来了，以后任它玄学吹上天，我自一毛不拔！
年中听说G502出了无线版，本想换但考虑到换掉了重滚轮，重心变化太大最后不了了之。~~才不是因为没钱~~ 
### 好像这个标题下技术方面来着
我在写些什么鬼东西~~算了不管了，破罐破摔~~ 
### 桌面环境
Linux下被I3wm圈粉，现在使用体验舒适，基本实现预期目标，Windows下打算搞出类似操作，本以为bug.n可以作为替代，但不精于AutoHotKey，无奈作罢。
--------

### 身体

真的是老了，前些天胸口疼，外加多日睡眠期间打呼噜，可能哪里出什么问题，赶假期要去检查一下，最近有几次长时间敲键盘，左臂刺痛，右手虎口也有症状，不能在高强度工作了。
--------

### 一些遗憾
稍微表示了下自己的心意，无奈被拒绝了，犯浑啊。
