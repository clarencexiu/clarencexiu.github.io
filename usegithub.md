### ��ַ
https://github.com/

### �ص�
���������
svn����ʽ����ͼ��
git�ֲ�ʽ����ͼ��
![���������ͼƬ����](https://img-blog.csdn.net/20181015200314540?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3FxXzQzMDAzNjI5/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)

### ������
git bash

### ָ��
�� git bash
1.**pwd**
��ʾ��ǰ·��
2.**cd /**
�����Ŀ¼
3.**ls**
��ʾ��·���µ������ļ����ļ�����
4.**cd~**
�����û���Ŀ¼��
5.**cd -**
  ���ؽ����Ŀ¼֮ǰ���ڵ�Ŀ¼��
6.**cd ..**
  �����ϼ�Ŀ¼������ǰĿ¼Ϊ��/������ִ������ڡ�/"��".."Ϊ�ϼ�Ŀ¼����˼����
7.**cd ../..**
  ����������Ŀ¼��
8.**mkdir �ļ�����**
�����ļ���
9.**touch �ļ���.md**
�����ļ�

###  �����ļ�
1.**git clone +��ַ**
�����ļ���ע���ַ��github�����ݿ��ұ���ɫ��ťClone or download �㿪ʹ��Clone with SSH Ȼ�������ַ
Ȼ��ѡ��yes
�������£�

```
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

```
�����������
2.**ssh-keygen -t rsa -C "�������"**
���ɹ�Կ��Ȼ��������λس���ʾ

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
�������ϴ�������� /c/Users/Administrator/.ssh/id_rsa.pub.Ѱ�Ҹ��ļ��򿪸���ճ����
github--���ϽǸ�����Ϣ--Setting--SSH and GPG keys--�ұ�New SSH Key
3.**git clone +��ַ**
��¡�ɹ���ʾ

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
���ļ������ڵ�ǰ·���£�ע�����·�������ļ�����λ�ã�
4.**cd ��ַ**
���븴���ļ��ĵ�ַ����������lsȷ�ϣ�
5. **touch �ļ���.md**
�����ļ�
6.**git add �ļ���**
 ������Ҫ��ӵ��ļ�
7.**git status**
��ʾ����״̬
8.**git commit -m "first commit"**
�ύ
9**git config --global user.email "623531383@qq.com"**
10**git config --global user.name "clarecexiu"**
11.**git push -u origin master**
�����ص�master��֧���͵�origin����