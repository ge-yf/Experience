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

		任何模式下，按下Esc键即可返回正常模式

## 快捷键 ##
*命令前加‘n’，表示命令重复n次

| Key | Function |
| :------------- |:-------------|
| hjkl | 正常模式下，使用hjkl可以移动Cursor(左下右上) |
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
| ce | 将光标处到单词末尾删除，并切换到插入模式 |
| cw | 将光标处到下一个单词的开头前删除，并切换到插入模式 |
| c$ | 删除从光标处到行末的所有字符，并切换到插入模式 |
| CTRL + g | 显示当前光标所在位置和文件状态 |
| gg | 跳转到文件开头 |
| G | 跳转到我文件末尾 |
| nG | 跳转到文件的第N行 |
| / | 正常模式下，输入‘/’，之后输入单词，可以搜索输入的单词，在搜索结果中，按n可以继续搜索下一个，按N可以反方向搜索 |
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
|  |  |
|  |  |

TODO Lesson6.1


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
