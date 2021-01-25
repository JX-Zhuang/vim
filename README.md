# vim
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
* 滚动一行
 * `Ctrl + E` 屏幕向下滚动一行
 * `Ctrl + Y` 屏幕向上滚动一行
* 滚动半屏
 * `Ctrl + D` 屏幕向下滚动半屏
 * `Ctrl + U` 屏幕向上滚动半屏
* 滚动一屏
 * `Ctrl + F` 屏幕向下滚动一屏
 * `Ctrl + B` 屏幕向上滚动一屏
* `Ctrl+r` 反撤销
* [移动光标](https://harttle.land/2015/11/07/vim-cursor.html)

#### 代码补全
Valloric/YouCompleteMe
