---
title: Mauris vulputate
featured: images/pic02.jpg
layout: post
---

<!DOCTYPE html>
<html>
<head>
	<title>
		find命令的 xargs 和-exec 区别
	</title>
</head>
<body>
	<div>
		find命令的 xargs 和-exec 区别：
		-exec ： find命令将所有匹配到的文件一起传给 exec执行，有些系统对能够传给exec命令长度有限制，在find命令运行几分钟后，出现溢出错误。如“参数列太长”， “参数列溢出”； 
		处理每一个匹配到的文件发起一个进程，出现进程过多，系统性能下降；
 		| xargs： find命令将匹配到的文件传递给xargs命令，xargs命令每次只取一部分文件，接着下一批；
		只有一个进程；
		>> find . -type f -print | xargs grep “login”
	</div>
</body>
</html>
