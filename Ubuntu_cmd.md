#### 删除目录及目录下所有文件 ####
rm -rf 目录

---

#### 可读可写可执行权限 ####
chmod -R 777 XXX

---

#### 解压缩命令 ####


1.分卷压缩
tar cvzpf - eclipse | split -d -b 50m
上面的命令是将eclipse这个文件夹分卷压缩，每卷50m，注意eclipse 前面有空格.压缩完之后，会被命名为x00,x01,x02。。。
2.解压
首先需要合并： 合并的命令是：
cat x*>eclipse.tar.gz
然后解压：
tar xzvf eclipse.tar.gz



1、*.tar 用 tar -xvf 解压
2、*.gz 用 gzip -d或者gunzip 解压
3、*.tar.gz和*.tgz 用 tar -xzvf 解压
4、*.bz2 用 bzip2 -d或者用bunzip2 解压
5、*.tar.bz2用tar -xjvf 解压
6、*.Z 用 uncompress 解压
7、*.tar.Z 用tar -xZf 解压
8、*.rar 用 unrar e解压
9、*.zip 用 unzip 解压

---

#### find命令 ####
find [dir] -iname "*dab*"
搜索dir目录下， 所有包含dab的文件名，忽略大小写。


---

#### fasd命令 ####

GitHub: https://github.com/clvv/fasd

安装:
$ sudo add-apt-repository ppa:aacebedo/fasd
$ sudo apt-get update
$ sudo apt-get install fasd

配置:
在.zshrc文件中追加:
eval "$(fasd --init auto)"

使用:




---

#### apt-get ####
apt-get purge / apt-get –purge remove
删除已安装包（不保留配置文件)。
如软件包a，依赖软件包b，则执行该命令会删除a，而且不保留配置文件

apt-get autoremove
删除为了满足依赖而安装的，但现在不再需要的软件包（包括已安装包），保留配置文件。

apt-get remove
删除已安装的软件包（保留配置文件），不会删除依赖软件包，且保留配置文件。

apt-get autoclean
APT的底层包是dpkg, 而dpkg 安装Package时, 会将 *.deb 放在 /var/cache/apt/archives/中，apt-get autoclean 只会删除 /var/cache/apt/archives/ 已经过期的deb。

apt-get clean
使用 apt-get clean 会将 /var/cache/apt/archives/ 的 所有 deb 删掉，可以理解为 rm /var/cache/apt/archives/*.deb。

---

#### linux 局域网内文件传送(scp 命令) ####
(一)从 远程 复制到 本地
文件：
scp remote_username@remote_ip:remote_file local_file(local_folder)

目录(加 -r 参数)：
scp -rv remote_username@remote_ip:remote_folder local_folder   #在命令执行后需要输入密码
或
scp -rv remote_ip:remote_folder local_folder    #没有指定用户名，在命令执行后需要输入用户名和密码;


(二)从 本地 复制到 远程:
文件：
scp local_file remote_username@remote_ip:remote_folder
或
scp local_file remote_username@remote_ip:remote_file
或
scp local_file remote_ip:remote_folder
或
scp local_file remote_ip:remote_file

目录(加 -r 参数)：
scp -r local_folder remote_username@remote_ip:remote_folder  #在命令执行后需要输入密码
或
scp -r local_folder remote_ip:remote_folder   #没有指定用户名，在命令执行后需要输入用户名和密码;

---


#### 添加或删除一个PPA源 ####

添加PPA源的命令为：
sudo add-apt-repository ppa:user/ppa-name

添加好更新一下：
sudo apt-get update

删除命令格式则为：

sudo add-apt-repository -r ppa:user/ppa-name

然后进入 /etc/apt/sources.list.d 目录，将相应 ppa 源的保存文件删除。
最后同样更新一下。
