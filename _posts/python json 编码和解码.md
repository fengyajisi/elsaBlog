---
title: Python Json编码和解码
featured: images/pic03.jpg
layout: post 
---
<!DOCTYPE html>
<html>
<head>
	<title>
		json 编码和解码
	</title>
</head>
<body>
	<p>
		json.dumps()    python to json
    	json.loads()    json to python
	</p>
	<p>
		import json
		dic = {'str': 'this is a string', 'list': [1, 2, 3, 4]}
		type(dic)
		>> dict
		json_obj = json.dumps(dic)
		type(json_obj)
		>> str
		dic1 = json.loads(json_obj)
		type(dic1)
		>> dict
	</p>
	<div>
		ref https://docs.python.org/dev/library/json.html
	</div>
</body>
</html>
