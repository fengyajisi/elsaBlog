---
title: Lorem Ipsum Dolor Sit Amet
featured: images/pic04.jpg
layout: post
---

<!DOCTYPE html>
<html>
<head>
	<title>
		mysql优化
	</title>
</head>
<body>
	<div>
		事务： Begin；
			  sql command；
			  commit；
		锁定数据库；
	</div>
	<div>
		锁定表: lock tables tablename write;
				sql command;
				unlock tables;
		锁定表；
	</div>
	<div>
		外键：
		CREATE  TABLE   customerinfo( customerid   int primary key) engine = innodb;
		create table salesinfo (salesid int not NULL, customerid int not null, PRIMARY KEY(customerid, salesid)
		, FOREIGN KEY (customerid) REFERENCES customerinfo(customerid) on DELETE CASCADE )engine = innodb;
	</div>
</body>
</html>