# 国内源 #

sudo vim /etc/apt/sources.list
 在文件最前面添加以下条目(操作前请做好相应备份)

deb http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-proposed main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ bionic-backports main restricted universe multiverse



# Unity Tweak Tool #

	仅适用于Unity环境

    sudo add-apt-repository ppa:freyja-dev/unity-tweak-tool-daily
    sudo apt-get update
    sudo apt-get install unity-tweak-tool


# Flatabulous theme and ultra-flag icons #

	仅适用于Unity环境

	sudo add-apt-repository ppa:noobslab/themes
	sudo add-apt-repository ppa:noobslab/icons
	sudo apt-get update
	sudo apt-get install flatabulous-theme
	sudo apt-get install ultra-flat-icons

# Gnome Tweak Tool #

	仅适用于Gnome环境 (18.04)

	sudo apt-get update
	sudo apt-get install gnome-tweak-tool
	sudo apt-get install gnome-shell-extensions (安完需要重启)
	sudo apt install chrome-gnome-shell

	Appearance:
		Application : Adwaita-dark
		Cursor : Whiteglass
		Icons : Ubuntu-mono-dark

	Extensions:
		Places status indicator : ON
		User themes : ON


	dash to dock:
		1. 到“https://micheleg.github.io/dash-to-dock/releases.html”下载最新版
		2. 将解压缩后的文件夹重命名为“dash-to-dock@micxgx.gmail.com”
		3. 把文件复制到home文件下的.local/share/gnome-shell/extensions/
			sudo mv dash-to-dock@micxgx.gmail.com/ .local/share/gnome-shell/extensions/
		4. 按Alt+F2，然后输入r， 重启gnome
		5. 打开gnome-tweak设置Dash to Dock
			***不要打开Dash to Dock扩展，修改样式直接点击齿轮按钮就好
			Position and size:
					Show on all monitors : Yes.
					Position on screen : Bottom.
					Intelligent autohide : yes
					Panel mode : No
					icon size limit : 64
			Launchers :
					Show Applicationsicon : No
					Customize opacity : Fixed
							Opacity : 0%

# Themes #

	www.gnome-look.org

	主题放到 Home .themes文件夹下。
	在Gnome Tweak Tool中选择。

	icon主题放到 Home .icons文件夹下。
	在Gnome Tweak Tool中选择。

# Git #

	sudo apt-get install git
	git config --global user.name "xxx"
	git config --global user.email "邮箱地址"

# VIM #

Requires Git 1.7+ and Vim 7.3+

	sudo apt-get install vim
	curl https://j.mp/spf13-vim3 -L > spf13-vim.sh && sh spf13-vim.sh
	sudo apt-get install ctags

# zsh #

	zsh.txt

# ag #

	https://github.com/ggreer/the_silver_searcher

	sudo apt-get install silversearcher-ag

# fasd #

	https://github.com/clvv/fasd

	sudo add-apt-repository ppa:aacebedo/fasd
	sudo apt-get update
	sudo apt-get install fasd

	add the follow line in .zshrc
		eval "$(fasd --init auto)"

# cppman #

	C++手册
	sudo apt-get install cppman

# mlocate #

	TODO
