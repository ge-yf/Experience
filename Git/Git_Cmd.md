# TLDR(Too Long; Didn't Read.) #
在使用Git的过程中，最好养成如下习惯：

1. 随时使用 `git status` ！
2. 只更改那些真正想更改的文件。
3. `git add .` 会是你真正的朋友。
4. 随时使用命令 git commit -m “meaningful messages”。
5. 在push前先fetch, pull。
6. 最后， `git push`推送提交的更改。


#### 将错误的修改恢复： ####

恢复单个文件：

    git checkout -- fileName


恢复当前目录中的所有文件（抛弃自上次提交以来的所有更改）：

    git reset --hard


#### 生成和使用patch ####

获取修改前和修改后文件的两种方法：

1. `git stash`备份当前工作区内容，将工作区恢复到上一次提交的状态，同时将当前工作区内容保存到Git栈中。  -> 取得变更前文件。

	`git stash pop`将暂存的内容恢复到工作区， 取得变更后的文件。  -> 取得变更后文件。

2. 有时候修改完代码后，不想马上提交，可以另外建立一个分支，在这个分支上提交，结束之后再切回原来的分支。
	`git checkout -b name`


**UNIX下的patch**

 	`git diff  > patch`
    `git diff  --cached > patch`
    `git diff  branchname --cached > patch`

以上3中方法都能生成一个unix风格的patch文件。

在应用时， 使用`git apply patch`来应用patch。

