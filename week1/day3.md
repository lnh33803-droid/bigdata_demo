#day3
#指令
 1.‘cp’复制
 	a.在本目录下复制 cp wenjian wenjian.bak
	b.复制到别的目录 cp wenjian /root/
	c.复制文件夹 cp -ar /etc /mulu/ ( “-a”为保留原始权限）
	d.复制多个文件 cp wenjian1 wenjian2 /mulu/
 2.‘mv’（move）移动文件or改名文件
 	a.移动（剪切）：mv text /mulu/
	b.改名: mv text ikun
 3.‘rm’ 删除
	rm -r 可以删除目录
	rm -rf 直接删除，无需确认
 4.‘tar’压缩&解压
	压缩
 	  tar -c 打包文件
 	  tar -cz （or tar -cJ压缩能力更强）		
	  格式：tar -czf /yasuo(压缩所至的目录)/peizhi.tar.gz(压缩文件名称) etc(所压缩的文件)
      	解压
	  tar -x
	  格式：tar -zxvf peizhi.tar.gz（解压到当前目录）
	        tar -zxvf peizhi.tar.gz -C /root/bigdata_demo/(解压到指定的目录）
	    （“-v”指查看解压的过程）
 5.‘zip’压缩
	单个or多个文件 zip text.zip file.text file2.jpg
	目录 zip -r txet.zip mulu/
  ‘unzip’解压
	至当前目录 unzip text.zip
	至指定目录 unzip text.zip -d /home/mulu/
#错误指导
 1.minimal未自带tar需下载
	红帽系:yum install tar -y
       	ubuntu: apt-get update &&apt-get install -y tar
 2.zip也需下载
	1.yum install wget(下载工具）
	2.yum install zip unzip -y



