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


# 使用 #