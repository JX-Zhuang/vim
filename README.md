# vim
### 插入模式
* ctrl+h 删除上一个字符，ctrl+w 删除上一个单词，ctrl+u 删除当前行
### 命令模式
* set nu  显示行号
* syntax on 语法高亮
* set hls 搜索到的高亮
* set incsearch 增量搜索
### normal模式
#### 行内移动
* f{char}跳到{char}字符上。,跳转到上一个搜索位置，;跳转到下一个位置
* t{char}跳到{char}的前一个字符
* F反过来搜索
#### 水平移动
* 0 行首第一个字符，^第一个非空白字符
* $ 移动到行尾，g_移动到行尾非空白字符
#### 垂直移动
* ()在句子间移动，:help(查看帮助
* {}在段落之间移动
#### 页面移动
* gg/G移动到文件开头/结尾，ctrl+o快速返回
* H/M/L跳转到屏幕的开头（Head)、中间（Middle）、结尾（Lower）
* ctrl+u,ctrl+f。上下翻页（upword/forward）。zz把屏幕置为中间
##### 滚动一行
 * `Ctrl + E` 屏幕向下滚动一行
 * `Ctrl + Y` 屏幕向上滚动一行
##### 滚动半屏
 * `Ctrl + D` 屏幕向下滚动半屏
 * `Ctrl + U` 屏幕向上滚动半屏
##### 滚动一屏
 * `Ctrl + F` 屏幕向下滚动一屏
 * `Ctrl + B` 屏幕向上滚动一屏
### vim 快速修改
* r(replace),c(change),s(substitute)
* normal模式下使用r可以替换一个字符，s替换并进入插入模式
* 使用c配合文本对象，我们可以快速进行修改（例如cw）
### vim 查询
* /或者? 进行前向或者后向搜索
* n/N跳转下一个或者上一个匹配
* * 或者 #进行当前单词的前向和后向匹配
#### vim搜索替换
##### substitute
* 命令模式下，:[range]s[substitute]/{pattern}/{string}/[flags]
* range表示范围，比如：10，20表示10-20行，%表示全部
* pattern是要替换的模式，string是替换后文本
* g(global):全局范围内执行；c(confirm):表示确认，可以确认或者拒绝修改；n(number):报告匹配到的次数而不替换，可以用来查询匹配次数
#### vim多文件操作
* Buffer是指打开的一个文件的内存缓冲区
* Window是Buffer可视化的分割区域
* Tab可以组织窗口为一个工作区
#### Buffer
* buffer切换。使用:ls列举当前缓冲区，:bn跳转到第几n的缓冲区
* :bpre :bnext :bfirst :blast
* :b buffer_name 加速tab补全来跳转
* :e 打开某个文件
#### Window
* 一个缓冲区可以分割成多个窗口，每个窗口也可以打开不同缓冲区
* <ctrl+w>s水平分割，<ctrl+w>v垂直分割。或者:sp和:vs
* 可以无限分割
* <ctrl+w>w窗口间循环切换
* <ctrl+w>HJKL移动窗口
#### Tab
* tab是可以容纳一系列窗口的容器(:h tabpage)
* :tabn[ew] {filename}
* :tabe[dit] {filename} 在新标签页打开{filename}
* <c-w>T把当前窗口移动到一个新标签页
* :tabc[close] 关闭当前标签页及其中的所有窗口
* :tabo[only] 只保留活动标签页，关闭所有其他标签页
* :tabn[ext] {N} ，普通模式命令{N}gt 。切换到编号为{N}的标签页
* :tabn[ext] ， 普通模式命令gt 。切换到下一个标签页
* :tabp[revious], 普通模式命令gT。切换到上一个标签页
  
### vim 常用插件
#### Nerd Tree
* autocmd vimenter * NERDTree 
* 自动开启Nerdtree
* 开启/关闭nerdtree快捷键，map <C-n> :NERDTreeToggle<CR>
* Shift + I 隐藏/显示 .文件
* [NERDTree 快捷键辑录](https://yang3wei.github.io/blog/2013/01/29/nerdtree-kuai-jie-jian-ji-lu/)
#### 对文件的操作 
* m
* ma 
* mm
#### kien/ctrlp
* `ctrl + j/k` 进行上下选择
* `ctrl + x`    在当前窗口水平分屏打开文件
* `ctrl + v`    同上, 垂直分屏
* `ctrl + t`    在tab中打开
* [文件搜索 kien/ctrlp](https://github.com/kien/ctrlp.vim)
#### 常用命令  
* term 打开terminal
* Vim 调整窗口大小
 * 调整高度，将当前窗口增加/减少n行 `Ctrl + w, n, +/-`
 * 调整宽度，将当前窗口增加/减少n列 `Ctrl + w, n, >/<`
* 分屏
 * sp 上下分屏
 * vsp 左右分屏
* `Ctrl+r` 反撤销
* [移动光标](https://harttle.land/2015/11/07/vim-cursor.html)

#### 代码补全
Valloric/YouCompleteMe
