#day4
#指令
 1.‘|’管道符 将一个命令的输出结果交给另一个命令
    	eg. cat access.log | awk '{print $1}' | sort -n | uniq -c
                         显示前端数字      按顺序排列  去重并显示次数

 2.‘>’'>>' 重定向 将一条命令的输出结果写入某文件
	a.‘>’ 覆盖内容
	b.‘>>’追加内容
    标准输出
       tar -xvf zhengchang.tar.gz >> zhengchang.txt
    错误输出 (2>>)
       tar -xvf cuowu.tar.gz 2>> cuowu.txt
    全部输出 (&>>)
       tar -xvf peizhi.tar.gz &>> wanzheng.txt
