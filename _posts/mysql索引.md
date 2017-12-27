---
title: Mauris vulputate
featured: images/pic02.jpg
layout: post
---

<!DOCTYPE html>
<html>
<head>
	<title>
		Mysql 索引
	</title>
</head>
<body>
	<div>
		1. 尽量多使用 between and 少使用<, > 	
		SELECT ... WHERE pub_date BETWEEN '2005-01-01' and '2005-03-31';	
	</div>
	<div>
		2. 索引最左匹配原则， mysql一直向右匹配直到遇到范围查询（<,>, between, like）停止匹配。比如a = 1 and b = 2 and c > 3 and d = 4 ； 如果建立(a,b,c,d)顺序的索引，d是用不到索引的，如果建立(a,b,d,c)的索引则都可以用到，a,b,d的顺序可以任意调整。
	</div>
	<div>
		3. 索引列不能参与计算，保持列干净。
	</div>
	<div>
		打开profile ，可以查看duration，时间
		show profiles; 
		set profiling=1; 
	</div>
	<div>
		4. 索引的添加和删除，以及查看
		alter table test add index idx_score(score); 
		select index_name, index_type from information_schema.statistics
           where table_name = 'test';
        alter table test drop index idx_name;
	</div>
	<div>
		5. 不鼓励使用like，要使用的话，like “%aaa%” 不会使用索引而like “aaa%”可以使用索引
	</div>
</body>
</html>