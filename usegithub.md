### 网址
https://github.com/

### 特点
代码管理工具
svn集中式（左图）
git分布式（右图）
![在这里插入图片描述](https://img-blog.csdn.net/20181015200314540?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzMDAzNjI5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### 需下载
git bash

### 指令
打开 git bash
1.**pwd**
显示当前路径
2.**cd /**
进入根目录
3.**ls**
显示该路径下的所有文件和文件夹名
4.**cd~**
进入用户主目录；
5.**cd -**
  返回进入此目录之前所在的目录；
6.**cd ..**
  返回上级目录（若当前目录为“/“，则执行完后还在“/"；".."为上级目录的意思）；
7.**cd ../..**
  返回上两级目录；
8.**mkdir 文件夹名**
创建文件夹
9.**touch 文件名.md**
创建文件

###  复制文件
1.**git clone +地址**
复制文件，注意地址在github的数据库右边绿色按钮Clone or download 点开使用Clone with SSH 然后复制其地址
然后选择yes
跳出如下：

```
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

```
进行下面操作
2.**ssh-keygen -t rsa -C "你的邮箱"**
生成公钥，然后紧跟三次回车显示

```
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/Administrator/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/Administrator/.ssh/id_rsa.
Your public key has been saved in /c/Users/Administrator/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:LeH87cQie97+NTty8ym0Va1+SU7qu6jzZNii//M9qPk 623531383@qq.com
The key's randomart image is:
+---[RSA 2048]----+
|                 |
|                 |
|        .       .|
|       o o      o|
|        S .    ..|
|         ooo ..+ |
|        .oo+=.O.o|
|        .+=*o*oO=|
|       .o=*BXEB=*|
+----[SHA256]-----+

```
根据以上代码第六行 /c/Users/Administrator/.ssh/id_rsa.pub.寻找该文件打开复制粘贴至
github--右上角个人信息--Setting--SSH and GPG keys--右边New SSH Key
3.**git clone +地址**
克隆成功显示

```
$ git clone git@github.com:clarencexiu/clarencexiu.github.io.git
Cloning into 'clarencexiu.github.io'...
remote: Enumerating objects: 14, done.
remote: Counting objects: 100% (14/14), done.
remote: Compressing objects: 100% (12/12), done.
remote: Total 14 (delta 4), reused 3 (delta 0), pack-reused 0
Receiving objects: 100% (14/14), 2.94 KiB | 88.00 KiB/s, done.
Resolving deltas: 100% (4/4), done.

```
（文件出现在当前路径下，注意调整路径控制文件复制位置）
4.**cd 地址**
进入复制文件的地址（可以先用ls确认）
5. **touch 文件名.md**
创建文件
6.**git add 文件名**
 增加需要添加的文件
7.**git status**
显示他的状态
8.**git commit -m "first commit"**
提交
9**git config --global user.email "623531383@qq.com"**
10**git config --global user.name "clarecexiu"**
11.**git push -u origin master**
将本地的master分支推送到origin主机