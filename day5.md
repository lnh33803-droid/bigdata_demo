#day5
#命令
 1.‘grep’ 查找关键词的信息
	 ps -aux | grep php
  (查看系统进程）（查找有关“php”的进程）
 	 grep 113.246.111.67 /var/log/nginx/access.log
	（查找该ip的相关日志）
	 grep -i chrome 、var/log/nginx/access.log | wc -l
   	（‘ -i’忽略大小写）                         （数出行数）
 2.' grep "^xxx" '查找以xxx为开头      
 	grep "^Port" /etc/ssh/sshd_config
 3.‘ grep -v "^xxx"’过滤掉以xxx开头
	grep -v "^#" /etc/ssh/sshd_config
	grep -v "^[[:space:]]*#" /etc/ssh/sshd_config
        (-v 反选）（[[:space;]] 表示空格）（* 表示不限次数）
 4.‘ grep "[0-9]" ’查找出所有包含数字的
 	grep "[0-9]" /etc/ssh/sshd_config     

