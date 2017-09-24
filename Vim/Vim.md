# Vim #

## 4种模式 ##
- 命令模式(command-mode)

		正常模式下，按下"SHIFT + ;"      
- 插入模式(insert-mode)

		正常模式下，按下以下命令可以进入插入模式：
		i	在光标所在字符前开始输入文字并进入插入模式
		a	在光标所在字符后开始输入文字并进入插入模式
		o	在光标所在行的下面单独开一新行来输入文字并进入插入模式
		s	删除光标所在的字符并进入插入模式
		I	在行首开始输入文字并进入插入模式。(第一个非空白字符处)		
		A	在行尾开始输入文字并进入插入模式
		O	在光标所在行的上面单独开一新行来输入文字并进入插入模式
		S	删除光标所在行并进入插入模式
- 可视模式(visual-mode)

		正常模式下，按V进入可视模式，按V进入可视块模式。
- 正常模式(normal-mode)

		任何模式下，按下Esc(Ctrl + [)键即可返回正常模式

## 快捷键 ##
*命令前加‘n’，表示命令重复n次

*按下“.”可以重复上一次的命令

*在命令模式，输入“help + 关键字”可以打开帮助

| Key | Function |
| :------------- |:-------------|
| hjkl | 正常模式下，使用hjkl可以移动Cursor(左下右上) |
| w | 正常模式下，使用w可以移动到下一个单词的词首 |
| e | 正常模式下，使用e可以移动到词尾 |
| x | 正常模式下，按下x可以删除光标处的字符 |
| dw | 正常模式下，将光标移动到单词首字母处，输入dw可以删除一个单词(到下一个单词的开头) |
| de | 正常模式下，将光标移动到单词首字母处，输入de可以删除一个单词(到当前单词的末尾) |
| d$ | 正常模式下，删除从光标处到行末的所有字符 |
| dd | 删除光标所在行 |
| u | Undo the last commands |
| U | Undo all the changes on a line |
| CTRL + R | Redo the commands |
| p | 将上一次删除的字符串插入到光标的后边 |
| rx | 将光标处的字符替换为‘x’ |
| R | 从光标处的字符开始替换，直到按下ESC(Ctrl+[)退出替换模式 |
| ce | 将光标处到单词末尾删除，并切换到插入模式 |
| cw | 将光标处到下一个单词的开头前删除，并切换到插入模式 |
| c$ | 删除从光标处到行末的所有字符，并切换到插入模式 |
| CTRL + g | 显示当前光标所在位置和文件状态 |
| gg | 跳转到文件开头 |
| G | 跳转到我文件末尾 |
| nG | 跳转到文件的第N行 |
| / | 正常模式下，输入‘/’，之后输入单词，可以搜索输入的单词，在搜索结果中，按n可以继续搜索下一个，按N可以反方向搜索 |
| :set ic | (全局设置)在搜索时， 忽略大小写 |
| :set noic | (全局设置)取消忽略大小写 |
| :set hls | (全局设置)将所有匹配的搜索结果高亮显示 |
| :set nohls | (全局设置)取消高亮显示 |
| noh | (仅针对当前搜索结果)取消搜索后的高亮显示 |
| :set is | 不完全匹配搜索 |
| :set nois | 取消不完全匹配搜索 |
| CTRL + o | 后退 |
| CTRL + i | 前进 |
| % | 在匹配的两个括号之间跳转 |
| :s/oldString/newString/g | 命令模式下，输入“s/oldString/newString/” ，可以将当前行的第一个oldString替换为newString。结尾加“/g”的话，会替换当前行所有的oldSring|
| :#,#s/oldString/newString/g | 将#行和#行之间的oldString替换为newString |
| :%s/oldString/newString/g | 将整个文件中所有的oldString替换为newString |
| :%s/oldString/newString/gc | 查找当前文件中所有的oldString，由用户决定是否删除数据 |
| :! | 命令模式下，！后面可以输入外部Command，用来执行Shell命令 |
| :w FILENAME | 作用一：将当前正在编辑的文件保存到当前目录下的FILENAME中。 作用二：在Visual模式下选择一段代码后，输入“w FLIENAME”， 可以将选中的内容保存到FILENAME中。|
| :r FILENAME | 可以将FILENAME中的内容，插入到当前光标处 |
| o | 在光标所在行的下面，插入一行，并进入编辑模式 |
| O | 在光标所在行的上面，插入一行，并进入编辑模式 |
| a | 在光标之后， 进入编辑模式 |
| A | 在行尾进入编辑模式 |
| zc | 关闭文件中的折叠 |

----tmp---

在buffers之间切换：
Ctrl+6—下一个buffer
:bf    第一个缓冲区
:bl    最后一个缓冲区
:bn    下一个文件(buffer next)
:bp    上一个文件(buffer previous)
:bn    切换到第n个缓冲区(如果不清楚缓冲区的number，可以通过buffers查询)

查看缓冲区列表：
:buffers(与ls相同)

删除打开的缓冲区：
bdn    删除第n个缓冲区(buffer delete n)

----------
tab切换相关：
:tabnew [++opt选项] ［＋cmd］ 文件            建立对指定文件新的tab
:tabc       关闭当前的tab
:tabo       关闭所有其他的tab
:tabs       查看所有打开的tab
:tabp      前一个
:tabn      后一个

标准模式下：
gt , gT 可以直接在tab之间切换。

----------

翻页：

整页翻页 ctrl-f ctrl-b
f就是forword b就是backward

翻半页
ctrl-d ctlr-u
d=down u=up

滚一行  
ctrl-e ctrl-y

zz 让光标所杂的行居屏幕中央
zt 让光标所杂的行居屏幕最上一行 t=top
zb 让光标所杂的行居屏幕最下一行 b=bottom


----------

## 插件 ##

> **< leader >在spf13中代表','** 

#### NERDTree ####

| Key | Function |
| :------------- |:-------------|
| ? | 将光标移动到NERDTree中，输入？即可打开快速帮助 |
| CTRL+E | 以当前文件所在目录为根目录，启动NERDTREE |
| < leader >e | 在正常模式下，输入“,e”, 作用与CTRL+E相同，但是输入较方便 |
| Bookmark 书签名 | 将光标所在的路径添加为书签 |
| D | 将光标移动到想要删除的书签上，输入‘D’ ，在屏幕下方会提示是否删除该书签，输入y即可删除|
| NERDTree + 书签名 | 在Vim命令模式下如入。可以打开NERDTree中的书签 |
| o | 打开一个目录或者打开文件，创建的是buffer，也可以用来打开书签 |
| x | 收起当前打开的目录 |
| X | 收起所有打开的目录 |
| I | 显示或者不显示隐藏文件 |
| q | 关闭NERDTree |

#### CtrlP ####

| Key | Function |
| :------------- |:-------------|
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |


#### ctags ####

安装(Exuberant Ctags):
sudo apt-get install ctags

1. 在代码根目录执行(每次): 
	[ctags -R --c++-kinds=+px --fields=+iaS --extra=+q 目录], 之后会在当前目录生成所有代码的tag文件.
2. 在.vimrc文件中添加:
	set tags=./tags,tags;

| Key | Function |
| :------------- |:-------------|
| Ctrl + [ | 跳转到定义(如果结果有多个的话, 仅会跳转到第一个,这时就要使用ts来搜索了) |
| ts name | 列出所有name的定义 |
|  |  |
|  |  |
|  |  |


#### Tagbar ####

如果TagBar无法使用，则需要安装ctags(Exuberant Ctags)：
    

    sudo apt-get install ctags

之后重新BundleInstall， TagBar就可以使用了。

| Key | Function |
| :------------- |:-------------|
| ,tt | 启动Tagbar |
| o | 打开或关闭光标所在位置的目录																																																																																																																										 |
| p | 光标在选定的Tag上时，按下p可以跳转到指定tag，但是光标仍停留在TagBar中 |
| 回车 | 光标在选定的Tag上时，按下p可以跳转到指定tag，光标也跟随 |


#### Ag ####
首先需要安装：

	sudo apt-get install silversearcher-ag

搜索字符串：

	:Ag[!] [options] {pattern} [{directory}] 	在给定的directory中搜索pattern

	:AgBuffer[!] [options] {pattern} 			在打开的buffers中搜索pattern

	:AgFromSearch [{directory}]					以上一次搜索的pattern，再次在directory中搜索 

	:AgFile [options] {pattern} [{directory}]	在directory中搜索复合pattern的文件名。 

| Key | Function |
| :------------- |:-------------|
|e |   to open file and close the quickfix window|
|o |   to open (same as enter)|
|go |  to preview file (open but maintain focus on ag.vim results)|
|t |   to open in new tab|
|T |   to open in new tab silently|
|h |   to open in horizontal split|
|H |   to open in horizontal split silently|
|v |   to open in vertical split|
|gv |  to open in vertical split silently|
|q |   to close the quickfix window|
