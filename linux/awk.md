awk �ж�ȡ
#### awk�Ļ�����ʽ 
awk optionsѡ�� 'command' file
NR �к�
NF ����
$1,$n
-F ���÷ָ��� Ĭ���������ʹ�ÿո������зָ�
print
printf
Ҫʹ������: ~/����ƥ�����/
�����!~���Ƕ�����ƥ�������ȡ�� 
#### awk����չ��ʽ
awk [-f|-f|-v] 'BEGIN{} վλ��~/����/{�����} END{}' filepath
- ����
	- awk -F ':' '{if($3>150) printf("Line:%2s Col:%s User:%15s UserId\n",NR,NF,$1,$3)}' /etc/passwd
	- awk -F ':' 'BEGIN{print "Line Col  UserID User"} {prinf("%4s %3s %7s %s\n",NR,NF,$3,$1)} END{print"------FILENAME-----"} /etc/passwd