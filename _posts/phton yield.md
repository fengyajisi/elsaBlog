---
title: Mauris vulputate
featured: images/pic02.jpg
layout: post
---
<!DOCTYPE html>
<html>
<head>
	<title>
		
	</title>

</head>
<body>
	<p>
		To understand what yield does, you must understand what generators are. And before generators come iterables.
		理解yield， 先理解generator，要理解generator，先理解iterable
	</p>
	<div>
		list is an iterable. When you use a list comprehension, you create a list, and so an iterable:
		如:
			mylist = [x * x for x in range(3)]
		    for l in mylist:
		    	print(l)
	</div>
	<div>
		Everything you can use "for... in..." on is an iterable; lists, strings, files...
		所有能用for..in..的都是iterable; 如 list, string, file
	</div>
	<div>
		Generators are iterators, a kind of iterable you can only iterate over once. Generators do not store all the values in memory, they generate the values on the fly
		Generator是iterator，但是不是在内存中存储所有的值，只在需要时计算
	</div>
	<div>
		 geratator used () instead of []. BUT, you cannot perform for i in mygenerator a second time since generators can only be used once
	</div>
	<div>
		yield: when you call the function, the code you have written in the function body does not run. The function only returns the generator object
		只返回一个generator 对象；
	</div>
	<div>
		每一次for call generator object, return 循环内的值，直到empty
	</div>
</body>
</html>
