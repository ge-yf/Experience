#### The best editor is neither Emacs nor Vim, it's Emacs *and* Vim! ####


# 安装 #
1. 安装Emacs:

	sudo apt-get install emacs

2. 安装Spacemacs：
	
	git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d


3. 运行Emacs GUI, 之后Spacemacs会提示选择一些信息后，自动开始安装插件。

	*选择Vim兼容模式。
	
	*在安装插件时， 如果有安装不成功的，就关掉Emacs再重开，就会自动重新安装。
	
	*如果提示"Cannot find any of the specified fonts (Source Code Pro)! Font settings may not be correct. "，就需要手动安装Source Code Pro字体。
		
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


| Key | Func |
| :------- | :------- |
| C-x C-c | 退出Emacs |
| C-g | 退出输入了一部分的Command |
| C-v | 向下滚动一屏 |
| M-v | 向上滚动一屏 |
| C-l | 将光标所在行置于屏幕中央(多次按下C-l时， 按照中->上->下->中的顺序循环) |
| C-p | previous 上一行|
| C-n | next 下一行 |
| C-f | forwawrd 向右移动一个字符 |
| C-b | backward 向左移动一个字符 |
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


**字体大小的调整**

- 放大字体: Ctrl-x Ctrl-+ 或 Ctrl-x Ctrl-=
- 缩小字体: Ctrl-x Ctrl–
- 重置字体: Ctrl-x Ctrl-0