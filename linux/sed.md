# sed 选项 动作 filename
- 选项 
	-n
- 动作
	- a 新增往下增加
	- i 往上一行增加
	- d 删除
	- c 改变  1,5c会将这一块区域整个替代,不会每行都替换
	- p 输出
	- s 替换 经常配合正则进行操作
	- w 写入 sed 'w 修改的文件' 新写入的文件
w前可以有参数,nw指从修改文件的第n行开始写入
    - r 读取 sed 'nr 插入的文件' 被插入的文件
从第n行后插入
- 高级操作
	- | 使用管道符配合其他命令
	- {} 可以让sed执行多个动作,只是动作之间要用";"分好隔开
	- & 替换,相当于替换前的内容的替身
	- \u 转换成大写可以配合&来实现将匹配内容转成大写操作
	- () 分组功能
sed 's/\([a-z0-9_-]*\):x:\([0-9]*\):	\([0-9]*\):.*$/user:\1 userid:\2 groupid:\3/' /etc/passwd

	