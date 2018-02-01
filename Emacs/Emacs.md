#### The best editor is neither Emacs nor Vim, it's Emacs *and* Vim! ####


# 安装 #
1. 安装Emacs:
	sudo add-apt-repository ppa:kelleyk/emacs
	sudo apt update

	sudo apt-get install emacs

2. 安装Spacemacs：

	git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d


3. 运行Emacs GUI, 之后Spacemacs会提示选择一些信息后，自动开始安装插件。

	*选择Vim兼容模式。

	*在安装插件时， 如果有安装不成功的，就关掉Emacs再重开，就会自动重新安装。

	*如果提示"Cannot find any of the specified fonts (Source Code Pro)! Font settings may not be correct. "，就需要手动安装Source Code Pro字体(zsh)。

		1.下载最新的Source code pro字体(https://github.com/adobe-fonts/source-code-pro/downloads)
		2. unzip SourceCodePro_FontsOnly-1.013.zip
		3. 复制SourceCodePro_FontsOnly-1.013/OTF目录中的所有.otf文件到~/.fonts目录下
		4. 执行命令 “fc-cache -f -v”


# 使用前 #
`<c-h>t`命令, 查看tutorial, 学会基本用法。

# 使用 #

显示行号：
.spacemacs文件中查找dotspacemacs-line-numbers。
默认配置为：
dotspacemacs-line-numbers nil
修改为：
dotspacemacs-line-numbers t
重启就显示行号了。

编辑风格 :
.spacemacs文件中查找dotspacemacs-editing-style.



编辑:
| Key | Func |
| :------- | :------- |
| C-x C-c | 退出Emacs |
| C-g | 退出输入了一部分的Command |
| C-/ (C-_) |  撤销 (Ctrl+Shift+-) |


光标移动:
| Key | Func |
| :------- | :------- |
| C-v | 向下滚动一屏 |
| M-v | 向上滚动一屏 |
| C-l | 将光标所在行置于屏幕中央(多次按下C-l时， 按照中->上->下->中的顺序循环) |
| C-p | previous 上一行|
| C-n | next 下一行 |
| C-f | forwawrd 向右移动一个字符 |
| C-b | backward 向左移动一个字符 |
| M-f | forwawrd 向右移动一个word |
| M-b | backward 向左移动一个word |
| C-e | 移动到行尾 |
| C-a | 移动到行首 |
| M-e | 移动到句尾 |
| M-a | 移动到句首 |
| M-< | 移动到文件首(ALT+SHIFT+,) |
| M-> | 移动到文件尾(ALT+SHIFT+.) |

插入与删除：
| Key | Func |
| :------- | :------- |
| C-d | 删除光标后的第一个字符（如果是矩形光标，就是光标所在处的字符） |
| M-DEL | 删除光标前的第一个Word |
| M-d | 删除光标后的第一个Word |
| C-k | Kill从光标处到行尾的内容 |
| M-k | kill直到句子末尾 |
|  |  |

其它:
| Key | Func |
| :------- | :------- |
| C-u Num Command | 重复Command Num次, 例如[C-u 8 C-n], 向下移动8行 |
| M-x "set-mark-command" + C-w/M-w | M-x后输入"set-mark-command", 选择mark的区域, 之后C-w剪切/M-w复制 |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |
|  |  |


**字体大小的调整**

- 放大字体: Ctrl-x Ctrl-+ 或 Ctrl-x Ctrl-=
- 缩小字体: Ctrl-x Ctrl–
- 重置字体: Ctrl-x Ctrl-0
