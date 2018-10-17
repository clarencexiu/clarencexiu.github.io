- 根目录(/)下的一些常用目录
	- 1.bin(binaries) 存放二进制可执行文件
	- 2.etc(etcetera) 存放系统配置文件
	- 3.usr(unix shared resources) 用于存放共享的系统资源
	- 4.home 存放用户文件的根目录
	- 5.root 超级用户目录
- Linux系统的关机与重启
	- 重启命令
		- reboot
		- shutdown -r now 立刻重启(root用户使用)
		- shutdown -r 10 过10分钟自动重启(root用户使用)
		- shutdown -r 20:35 在时间为20:35时候重启(root用户使用)		
		- 如果是通过shutdown命令设置重启的话，可以用shutdown -c命令取消重启
	- 关机命令
		- halt 立刻关机、
		- poweroff 立刻关机
		- shutdown -h now 立刻关机(root用户使用)
		- shutdown -h 10 10分钟后自动关机
- linux运行级别
配置文件：/etc/inittab  

|运行级别 |级别说明                       |  
|---------|-------------------------------|  
|0        |所有进程将被终止,机器将有序的停止,关机时系统处于这个运行级别|  
|1        |单用户模式,用于系统维护,只有少数进程运行,同时所有服务也不启用|  
|2        |多用户模式，和运行级别3一样，只是网络问卷系统（NFC）服务没有启动|    
|3        |多用户模式，和运行级别3一样，只是网络问卷系统（NFC）服务没有启动|  
|4        |未用|  
|5        |多用户模式，并且在系统启动后运行X Windwos，给出一个图形化d登陆窗口|  
|6        |所有进程被终止，重新启动系统|  

	- 查看 runlevel  (N表示之前未切换过运行级别)_
	- 切换 init 3  (填数字表示级别)

- 网络配置
	- 主机名
		- hostname (查看主机名)
		- hostname 主机名   (临时修改主机名)
		- 永久修改主机名
			- vi /etc/hostname (进入列表,按i,进行修改,ESC退出修改,:wq保存退出)(vi编辑的意思)
	- 查看所有活动网络接口的信息
		- 执行 ifconfig命令
		- 查看指定网络接口信息
		- 格式：ifconfig网络接口名
		- Ifconfig不能用，使用yum命令
		- yum install net-tools
	- 设置防火墙
		- 查看防火墙状态  service firewalld status
		- centos7关闭防火墙
			- 临时关闭   systemctl stop firewalld
			- 禁止开机启动   systemctl disable firewalld
	- 本地主机映射文件
		- cat /etc/hosts   (cat查看的意思)
	用途：保存主机名与IP地址的映射记录 	
	
	查看网络信息 
		- cat /etc/sysconfig/network-scripts/ifcfg-ens33

		
	- SELinux 增强型的 美国国家安全局开发的
当前有效 setenforce	[ Enforcing | Permissive| 1| 0 ]
该命令可以立即改变SELinux运行状态，在Enforcing 和Permissive 之间切换，关机重启之后失效。
		- 永久有效 修改配置文件
vi /etc/selinux/config (将SELINUX=enforcing修改为SELINUX=disabled重启生效)

[返回首页](https://clarencexiu.github.io)

