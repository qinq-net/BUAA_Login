# BUAA_Login
Shell script for BUAA network login

## How to execute如何运行
To execute this script, you should download it, change its content and authority, and then execute it.  
你应当下载这个脚本，更改脚本中的一些内容，改变脚本的权限，然后再执行它。

```
mkdir ~/scripts
cp ~/Downloads/BUAA_Login.sh ~/scripts/BUAA_Login.sh #move the script to desired directory
#Edit the scripts, change the username and the password on line 5
#更改脚本第五行的username与password
chmod +x ~/scripts/BUAA_Login.sh
~/scripts/BUAA_Login.sh
```


The scripts should be up and running. It will re-login every 2 hours.  
现在脚本应当开始运行了，它会每隔两小时自动重新登录一次。
## How to make this script a startup service 如何让脚本开机启动

Insert line `~/scripts/BUAA_Login.sh &` into file `etc/rc.local` above the final line `exit 0`.  
在`/etc/rc.local`文件的最后一行`exit 0`上方插入一行：`~/scripts/BUAA_Login.sh &`。

Then reboot, use `ps -A | grep BUAA_Login.sh` to see if the scripts is running.  
然后重启，用`ps -A | grep BUAA_Login.sh` 看看脚本是不是在运行。
