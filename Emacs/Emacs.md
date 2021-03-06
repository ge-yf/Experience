

# Spacemacs

The best editor is neither Emacs nor Vim, it's Emacs *and* Vim!

## 安装

### 安装Emacs

sudo add-apt-repository ppa:kelleyk/emacs
sudo apt update	
sudo apt-get install emacs

### 安装Spacemacs

1. git clone https://github.com/syl20bnr/spacemacs ~/.emacs.d

2. 添加国内源：   
.spacemacs文件   
在 dotspacemacs/user-init 中添加 melpa 中国镜像 

	;; melpa china mirrors
	(setq configuration-layer--elpa-archives
	  '(("melpa-cn" . "http://mirrors.tuna.tsinghua.edu.cn/elpa/melpa/")
	    ("org-cn"   . "http://mirrors.tuna.tsinghua.edu.cn/elpa/org/")
	    ("gnu-cn"   . "http://mirrors.tuna.tsinghua.edu.cn/elpa/gnu/")))

3. 运行Emacs GUI, 之后Spacemacs会提示选择一些信息后，自动开始安装插件。

	*在安装插件时， 如果有安装不成功的，就关掉Emacs再重开，就会自动重新安装。

	*如果提示"Cannot find any of the specified fonts (Source Code Pro)! Font settings may not be correct. "，就需要手动安装Source Code Pro字体(zsh)。

		1.下载最新的Source code pro字体(https://github.com/adobe-fonts/source-code-pro/downloads)
		2. unzip SourceCodePro_FontsOnly-1.013.zip
		3. 复制SourceCodePro_FontsOnly-1.013/OTF目录中的所有.otf文件到~/.fonts目录下
		4. 执行命令 “fc-cache -f -v”



#### 使用 cnfonts 配置中英文对齐

使用 org-table 时中英文混排时字体需要对齐, 使用 [cnfonts ](https://github.com/tumashu/cnfonts) 项目可以解决这一问题.

1. dotspacemacs-additional-packages` 中添加 `cnfonts

```
dotspacemacs-additional-packages
'(
    cnfonts
)
```

2. `dotspacemacs/user-config` 中添加

```
(defun dotspacemacs/user-config ()
  "Configuration function for user code.
This function is called at the very end of Spacemacs initialization after
layers configuration.
This is the place where most of your configurations should be done. Unless it is
explicitly specified that a variable should be set before a package is loaded,
you should place your code here."
  ;; Chinese and English fonts alignment
  (use-package cnfonts
    :config
    (cnfonts-enable)
    (setq cnfonts-use-face-font-rescale t)
    )
  )
```

## 使用前

`<c-h>t`命令, 查看tutorial, 学会基本用法。

## 使用



参考博客：

http://mpwang.github.io/2019/02/06/productivity/



显示行号：
.spacemacs文件中查找dotspacemacs-line-numbers。
默认配置为：
dotspacemacs-line-numbers nil
修改为：
dotspacemacs-line-numbers t
重启就显示行号了。

编辑风格 :
.spacemacs文件中查找dotspacemacs-editing-style.

字体大小：
.spacemacs文件中查找dotsspacemacs-default-font, 将大小修改为18

切换Emacs自带输入法:
c+\ 然后输入chinese-py, 可以输入了。
c-\ 可以切换回去。

修改缩进：
在setq-default的最后追加：
indent-tabs-mode nil
default-tab-width 4
c-default-style "k&r"
c-basic-offset 4

添加必须的Layer:
.spacemacs文件中查找dotspacemacs-configuration-layers, 将git， auto-completion的注释删掉。
然后执行<SPC f e R>


自动补全：
https://github.com/syl20bnr/spacemacs/tree/master/layers/%2Bcompletion/auto-completion

To use this configuration layer, add it to your ~/.spacemacs. 
You will need to add auto-completion to the existing dotspacemacs-configuration-layers list in this file.

;; 全局auto-complete：
;; 安装：
;; https://github.com/auto-complete/auto-complete

;; 使用：
;; Add the following contents to .emacs.d/init.el:
;; --
;; (require 'auto-complete)
;; (global-auto-complete-mode t)
;; --

文件操作:
| Key | Func |
| :------- | :------- |
| C-x C-c | 退出Emacs |
| C-g | 退出输入了一部分的Command |
| C-/ (C-_) |  撤销 (Ctrl+Shift+-) |
| C-x C-f | 打开（新建）文件 |
| C-x C-s | 保存文件 |
| C-x s | 保存buffer |
| C-x C-b | 列出所有buffer |
| C-x b | 在buffer之间切换 |
| M-x "recover-file" | 在crash之后恢复之前编辑的文件 |
| C-x 0 | 关闭窗口 |

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
| M-数字     | 切换光标到指定窗口                                                              |

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

# 插件 #

Neo Tree:
| Key      | Func                                |
| :------- | :-------                            |
| M-M f t  | 打开Neo Tree窗口                    |
| SPC      | 在Neo Tree窗口中,打开指定目录或文件 |
| n        | 下一行                              |
| p        | 上一行                              |
| g        | Refresh                             |
| H        | show/hide hidden files/directory    |
| -        | horizontal-split                    |
| |        | vertical-split    	                 |
