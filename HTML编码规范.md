###说明
前端编码规范,借鉴了百度EFE、ElemeFE、airbnb、bootstarp等

###1. 代码风格

####1.1 基本设置
- 使用 <!DOCTYPE html> 作为唯一的 DTD,建议使用大写的DOCTYPE
- [建议]启动IE Edge模式
- [建议]在 html 标签上设置正确的 lang 属性
- [建议]考虑到移动端的问题，建议加入viewport,并设置content为width=device-width,initial-scale=1
- 统一编码为UTF-8, 使用 <meta charset="UTF-8" /> 指定文件编码
- 所有页面必须有 "<title>"
- 考虑到SEO优化问题,页面尽量加入keywords和description
- 引入CSS时必须指明rel="stylesheet"
- [建议] 引入 CSS 和 JavaScript 时无须指明 type 属性
- [建议] CSS和JS尽量独立成单独文件
- [建议] JS应当放在页面末尾
- [强制] favicon必须加
比较好的页面处理方式:
```
<!DOCTYPE html>
<html lang="zh-CN">
<head>
	<meta charset="UTF-8">
	<title></title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<meta http-equiv="X-UA-Compatible" content="IE=Edge,chrome=1">
	<meta name="Keywords" content="摄影,互联网O2O,拍照/">
	<meta name="description" content="喔图——最专业的摄影预约平台 ">
	<link rel="shortcut icon" href="path/to/favicon.ico">
	<link rel="stylesheet" href="css/common.css">
	<link rel="stylesheet" href="css/global.css">
	<link rel="stylesheet" href="css/style.css">
</head>
<body>
	<img src="images/logo.png" alt="logo">
	<h1 class="world">world</h1>
	<script src="js/util.js"></script>
	<script src="js/demo.js"></script>
</body>
</html>
```

####1.2 缩进与换行
- [强制]使用 4 个空格做为一个缩进层级，不允许使用 2 个空格 或 tab 字符

```
<ul>
    <li>first</li>
    <li>second</li>
</ul>
```

####1.3 命名
- 所有标签和属性名一律小写
- 在HTML中得所有class类名统一使用   例如: header-logo   横线在中间
- 元素id单词全部小写,与class一样,单词之间统一以 - 为分割。如: navbar-right

####1.4 标签
**标签使用务必符合标签嵌套规则**
- p 段落
- h1,h2,h3,h4,h5,h6 层级标题
- strong,em 强调
- ins 插入
- del 删除
- abbr 缩写
- code 代码标识
- cite 引述来源作品的标题
- q 引用
- blockquote 一段或者长篇引用
- ul 无序列表
- ol 有序列表
- dl,dt,dd 定义列表

####1.5 属性
- **属性值必须使用双引号包围**
- 属性值必须小写
- 布尔类型的属性,建议不加属性值
	
	```
		<input type="text" disabled>
		<input type="checkbox" value="1" checked>
	```

- [强制]HTML属性应当按照以下顺序进行书写排列,确保代码的易读性
	- class
	- id,name
	- data-*
	- src、for、type、href
	- title,alt
	- aria-*,role
 	说明: class用于标识高度可复用组件,应当排在首位,id用于标识具体组件,因此排在第二位。
 	```
		<a class="..." id="..." data-modal="toggle" href="#">xxxx</a>
		<input class="form-control" type="text">
		<input src="..." alt="...">
 	```

- 布尔型属性不用赋值
	```
		<input type="text" disabled>
		<input type="checkbox" value="1" checked>
		<select>
			<option value="1" selected>1</option>
		</select>
	```
