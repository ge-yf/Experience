**Ubuntu 16.04出现：Problem executing scripts APT::Update::Post-Invoke-Success 'if /usr/bin/test -w /var/**

    Reading package lists... Done  
    E: Problem executing scripts APT::Update::Post-Invoke-Success  
    'if /usr/bin/test -w /var/cache/app-info -a -e /usr/bin/appstreamcli;  
     then appstreamcli refresh > /dev/null;  
     fi'  
    E: Sub-process returned an error code  

运行sudo apt-get update时出现如上信息，解决方法如下：

    sudo pkill -KILL appstreamcli  
      
      
    wget -P /tmp https://launchpad.net/ubuntu/+archive/primary/+files/appstream_0.9.4-1ubuntu1_amd64.deb https://launchpad.net/ubuntu/+archive/primary/+files/libappstream3_0.9.4-1ubuntu1_amd64.deb  
      
      
    sudo dpkg -i /tmp/appstream_0.9.4-1ubuntu1_amd64.deb /tmp/libappstream3_0.9.4-1ubuntu1_amd64.deb  
    

执行完上述命令之后再次运行sudo apt-get update就不会再出现上面的错误。

**Error Report com.ubuntu.apport.apport-gtk-root**

vim /etc/init/apport.conf 内容你会发现，控制此服务是否启动的是/etc/default/apport
所以把/etc/default/apport的enabled修改为0就ok了。

    sudo vi /etc/default/apport 