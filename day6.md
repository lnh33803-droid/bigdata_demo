#day6
#命令
 1.‘find’
	a.根据文件名查找
		find / -name access.log
	b.根据文件大小
		find /var/log/ -size +10M(查找在该位置log中大于10M的文件)
	c.多条件查找
		find /data -type f  -name "*.log" -mtime-7
		(-type f 限定普通文件 非目录)
		（-name "*.log" 以log结尾 '*'表示所有）
		（-mtime-7 最近7天修改过的文件）
 2.'vim'
	普通模式
	     查找文件内容	
		方向键
		0 移动到行首  $ 移动到行尾
		gg 移动到文件第一行  G 移动到文件最后一行 50G 移动到第50行
		Ctrl+f 向下翻页 ctrl+b 向上翻页
	     搜索关键词
   		/xxx 查找含‘xxx’的内容
		‘n’查看下一个‘xxx’ ‘N’查看上一个‘xxx’
	     操作
		‘x’       删除光标处字符
		‘dd’      删除整行
		‘yy’      复制整行
		‘p’       粘贴
		‘u’       撤销
		‘Ctrl+r’  重做
	插入模式
	   'i'在光标处编写  ‘o’新建一行开始编写

   	末行模式（esc+:）
	     保存和退出
	  	 ':w' 保存文件，不退出
	  	 ':q' 退出
          	 ':q!'强制退出
          	 ':wq'保存并退出
	     设置
 		‘:set nu’显示行号         ‘:set nonu’取消行号显示
    		‘:set ic’搜索时忽略大小写 ‘:set noic’搜索时区分大小写
	
