awk 行读取
#### awk的基本格式 
awk options选项 'command' file
NR 行号
NF 列数
$1,$n
-F 设置分隔符 默认情况下是使用空格来进行分割
print
printf
要使用正则: ~/正则匹配规则/
如果用!~就是对正则匹配的内容取非 
#### awk的扩展格式
awk [-f|-f|-v] 'BEGIN{} 站位列~/正则/{代码块} END{}' filepath
- 例子
	- awk -F ':' '{if($3>150) printf("Line:%2s Col:%s User:%15s UserId\n",NR,NF,$1,$3)}' /etc/passwd
	- awk -F ':' 'BEGIN{print "Line Col  UserID User"} {prinf("%4s %3s %7s %s\n",NR,NF,$3,$1)} END{print"------FILENAME-----"} /etc/passwd