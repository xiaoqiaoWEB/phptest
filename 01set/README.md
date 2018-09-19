#01set
	1.PHP环境搭建和调试
	2.PHP变量定义和使用

#PHP环境搭建:(LAMP和LNMP)
#1.LAMP
	L linux服务器
	A apache web服务器
	M mysql数据库
	P php动态程序

#2.LNMP
	L linux服务器
	N nginx web服务器
	M mysql数据库
	P php动态程序

#3.WAMP
	W windows服务器
	A apache web服务器
	M mysql数据库
	P php动态程序

#4.WNMP
	W windows服务器
	N nginx web服务器
	M mysql数据库
	P php动态程序

#apache和nginx web服务器:
	#1.apache优点
	1)稳定好
	2)并发量少(3000)
	3)配置简单

	#2.nginx优点
	1)稳定差
	2)并发性高(30000)
	3)配置复杂

#企业架构师课程课程地址:
http://www.yzmedu.com/course/45
1.网络工程师
2.服务器运维
3.PHP开发工程师
4.mysql数据库
5.mongodb数据库
6.sphinx搜索引擎
7.服务器cacti监控技术
8.服务器高并发技术

#linux下PHP环境(lamp):
1.源代码分别安装: apache、mysql和php软件包(gz,zip或bz2)

2.lamp集成包
phpstudy

#amp作用机制:
	1.客户端通过浏览器去访问服务器.
	2.访问apache web服务器.
	3.apache去寻找html文件，则apache直接把该文件返回给客户端浏览器即可.
	4.apache去寻找php文件，则apache会利用php解析器去先解析该php脚本，然后把解析后的html返回给客户端浏览器.
	5.apache去寻找php文件，并且其中含有mysql动态数据，则apache会利用php解析器去解析该php脚本，同时php脚本会连接mysql数据库并获取动态数据，然后再解析成html文件返回给客户端浏览器.

#静态网页和动态网页区别:
	1.直接访问html文件并返回给客户端.
	2.需要利用php、asp或jsp解析器先解析php、asp或jsp动态脚本的为动态网页.

#安装window下AMP集成环境:(appserv)
安装appserv-8.6.0

#调试appserv集成软件:
	1.常规方法
	1)计算机->右键->管理->服务:
	a.apache24是否启动
	b.mysql57是否启动

	2)任务管理器
	a.http
	b.mysql

	#2.dos方法
	1)win+r输入cmd进入dos环境.
	2)tasklist | find "http"
	3)tasklist | find "mysql"

	#3.如何关闭apache和mysql服务
		1)常规方法
		在计算机服务列表进行关闭

		2)dos命令
		net stop apache24
		net stop mysql57

	#4.如何开启apache和mysql服务
		1)常规方法
		在计算机服务列表进行开启

		2)dos命令
		net start apache24
		net start mysql57

	写第一段php程序:(index.php)
	<?php
		echo phpinfo();
	?>

#如何在appserv下切换php版本:
	1.查找apache配置文件
	C:\AppServ\Apache24\conf\httpd.conf

	2.设置php7解析器
	#LoadModule php5_module C:/AppServ/php5/php5apache2_4.dll
	LoadModule php7_module C:/AppServ/php7/php7apache2_4.dll

3.设置php7的配置文件
	#PHPIniDir "C:/AppServ/php5/"
	PHPIniDir "C:/AppServ/php7/"

