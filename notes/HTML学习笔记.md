***
***本文兼容HTML5***

***HTML十分简单,是八股文喵***

***对初学者而言,如果有看不懂的地方可以多查查资料,或者跳过喵***

# 第零章——前端技术浅谈


>***前端开发是创建WEB页面或APP界面呈现给用户的过程，通过HTML、CSS以及JavaScript以及衍生出来的各种技术、框架、解决方案，来实现互联网产品的用户界面交互。***

>***前端开发的基本技术***

|HTML|CSS|JavaScript|
|-------|-----|-------|
|结构层|表示层|行为层|

>***衍生技术***

- **TypeScript**
- **Vue.js**
- **Node.js**
- **AJAX**

>***前端与后端的关系***

- ***后端***
	- **在后台发生的各种进行工作的逻辑,又称"服务器端"**
***
- ***web系统的简要实现逻辑***
	- **前端网页通过与用户交互,在用户处获取请求.**
	- **前端系统向后端(服务器端)发出请求***
	- **服务器端对请求进行处理**
	- **服务器向前端响应请求**
	- **通过前端系统,回答在浏览器上呈现,完成交互**
	- **实现功能**
***
- ***web系统的具体实现***
	- **导航-用户输入url-点击链接-提交表单**
	- **导航到某地址-HTML-定位某IP为服务器**
	- **如果没有访问过-DNS查询-IP地址(可缓存)**      ***(DNS缓存)***
	- **获取IP地址-TCP三次握手-与服务器建立链接**
	- **发送HTTP请求-按照HTTP协议组装数据,按TCP/IP协议将HTTP协议格式的数据发送到服务器端**
	- **接受HTTP响应-按照HTTP协议组装数据,按TCP/IP协议将HTTP协议格式的数据传回浏览器**
	- **接收后解析HTML文件,构建DOM树-进行渲染**
	- **遇到Script,下载并解析,执行命令对DOM和CSSOM进行操作**
***
- ***浏览器渲染过程浅析***
	- ![浏览器渲染过程](/img/{EDB8EE10-8CA9-4c01-9AE8-87B1F6A2B654}.png)
	- ***如图***
	- **将HTML以及CSS分别解析为DOM树和CSSOM树**
	- ![DOM树结构](/img/{7E84BAED-5D1D-4d37-A090-3BDCBC33ACC6}.png)
	- **将DOM树和CSSOM树合并为渲染树**
	- **绘制渲染树**
	- DISPLAY




***
# 第一章——HTML环境配置    
## 1.1 软件准备
>以下软件择其一安装
- ***vscode***
- ***vim***
- ***webstorm***
## 1.2插件配置
>下面以***vscode***为例进行阐述

**请安装以下插件**
- ***open in browser***
- ***Auto-Save on Window Change***
***
*下面你就可以编辑你的网页啦！*
# 第二章——文件头格式
>下面是一个简单的文件头的示例  
>![文件头示例](/img/head_example.jpg)
>就这样，一个文件头就写好了喵
***

>**代码示例**
~~~
<!-- 在vscode中，本代码通过键入'!'字符来生成 -->


<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
	<!-- 在这里键入网页主体 -->
</body>
</html>
~~~


# 第三章——HTML代码细则
***
## 3.0 前置知识——HTML元素

>***HTML文档由HTML元素定义***

- ***HTML元素语法***
	- HTML元素以***开始标签***起始
	- HTML元素以***结束标签***终止
	- ***元素的内容***是开始标签与结束标签之间的内容
	~~~
	<!-- 这是一个开始标签和结束标签的示例 -->
	
	<p>这是第一个段落。</p>
	~~~
	
	- 某些HTML标签具有***空内容***
	- 空元素可以在***开始标签***中进行***关闭***
	~~~
	<!-- 这是一个在开始标签中关闭的空元素 -->
	
	<br />
	
	<!-- 这个元素的含义是换行 -->
	~~~
	- 大多数HTML元素可以拥有***属性***
		- 属性可以在元素中附加信息
		- 属性一般描述于开始标签
		- 属性总是以名称/值的形式出现,如` name="value" `
		- 值用\" \"引出
		- [HTML标签参考手册](https://www.runoob.com/tags/html-reference.html)
		- [HTML全局属性参考手册](https://www.runoob.com/tags/ref-standardattributes.html)
	~~~
	<!-- 这是一个拥有属性的元素 -->
	
	<img decoding="async" src="/images/logo.png" width="258" height="39" />
	~~~

>***HTML中不要忘记结束标签***

>***HTML元素支持嵌套***
>***即一个元素可以包含其他元素***

***
## 3.1 对代码头的进一步阐释
### 3.1.1 HTML`<head>`元素

***`<head>`元素包含了所有头部标签元素***

>其中我们可以插入

- ***脚本（scripts）***
- ***样式文件（CSS)***
- ***各种mata信息***
~~~
<title>
<style>
<meta>
<link>
<script>
<noscript>
<base>
~~~
### 3.1.2 HTML\<title>元素

- ***请注意***
>***代码头中的`<title>`元素定义的是显示在搜索引擎结果页面的标题***
>
>***`<title>`元素在HTML以及XHTML中是必须的***

~~~
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
------------------------------------
<title>文档标题</title>
------------------------------------
</head>
 <body>
文档内容......
</body>
 
</html>
~~~

### 3.1.3 HTML \<base> 元素

>`<base>`标签描述了本HTML文件中最基本的***链接地址***和***链接目标***
>且这种设置是***全局***的

- 下面是此标签的使用方法

~~~
<head>
<base href="http://www.runoob.com/images/" target="_blank">
</head>
~~~

- 下面是一个代码示例

~~~
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
<base href="https://www.runoob.com/images/" target="_blank">
</head>

<body>
<img src="logo.png"> - 注意这里我们设置了图片的相对地址。能正常显示是因为我们在 head 部分设置了 base 标签，该标签指定了页面上所有链接的默认 URL，所以该图片的访问地址为 "https://www.runoob.com/images/logo.png"
<br><br>
<a href="https://www.runoob.com">菜鸟教程</a> - 注意这个链接会在新窗口打开，即便它没有 target="_blank" 属性。因为在 base 标签里我们已经设置了 target 属性的值为 "_blank"。

</body>
</html>
~~~

如上面的代码示例所示

***`<base>`元素定义了网页主体所有链接定义的缺失属性***

***即网页主体中链接属性可以被重新定义,若不重新定义,默认使用`<base>`所定义的链接属性***

### 3.1.4 HTML`<link>`元素
- 本***HTML***笔记不对其进行过多阐述

>**本标签定义了文档与外部资源的关系**
>**其通常用于链接样式表**

- 下面是一个实例
~~~
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
~~~
### 3.1.5 HTML`<style>`元素

***本元素全局控制页面的样式***
***样式文件通常用CSS完成***
>***与`<base>`元素相同***
>***网页主体中样式属性可以被重新定义,若不重新定义,默认使用`<style>`所定义的样式属性***

- 下面是一个代码示例
~~~
<head>
<style type="text/css">
body {
    background-color:yellow;
}
p {
    color:blue
}
</style>
</head>
~~~
### 3.1.6 HTML`<mata>`元素

>***本标签描述了一些基本的元数据***
>***在客户端中`<mata>`元素所定义的元数据不会被显示,但会作为网页的属性被浏览器解析***

>***元数据是数据的数据信息***
>***通俗的讲,元数据就是对本网页的描述、关键词、文件的修改时间、作者等属性进行阐释***

- 下面是此元素的具体用法示例

~~~

<meta charset="utf-8" />

<meta name="description" content="Free Web tutorials on HTML and CSS">


<!-- Redirect page after 3 seconds -->
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org" />

~~~

>**如例**
- **文件头中每一个元数据应该***单独***用`<mata>`标签进行声明**

 >**注意**
- **在***HTML***中`<meta>`没有结束标签**
- **在***XHTML***中`<mata>`标签必须包含结束标签**

***
#### 附录_一些元数据的名称

>1 . `charset`

- ***该属性定义了文档的字符编码***

	***其值必须为不区分大小写的`UTF-8`***
	***`UTF-8`是HTML5文档的唯一有效编码***

- ***声明该元数据的`<mata>`元素必须位于文档的前1024个字节内***

- 代码示例
~~~
<meta charset="utf-8" />
~~~

>2 . `content`

- ***该属性定义了`http-equiy`或`name`属性的值***

- 代码示例
~~~
<meta name="description" content="Free Web tutorials on HTML and CSS">


<!-- Redirect page after 3 seconds -->
<meta http-equiv="refresh" content="3;url=https://www.mozilla.org" />

~~~

>3 . `http-equiv`

- ***该属性定义了一个编译指示命令***
- ***其允许的值都是特定HTTP标头的名称***

- ***下面是此属性可以定义的一些值***
	- `content-security-policy`
		***允许作者定义此页面的[内容策略](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Headers/Content-Security-Policy)***
		
		**内容策略常用来指定允许的服务器源和脚本端点,有助于防止跨站点脚本攻击**

	- `content-type`
		***声明[MIME类型](https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Basics_of_HTTP/MIME_types)和文档的字符编码***
		
		***与`charset`属性类似***
		***`content-type`属性的值同样必须是`text/html; charset=UTF-8`***
		
		~~~
		<mata http-equive="content-type" content="text/html; charset=UTF-8" />
		~~~
		
		- **注意**
			- ***同样的,声明该元数据的`<mata>`元素必须位于文档的前1024个字节内***
			- ***该属性只能用于 MIME 类型为 `text/html` 的文档，不能用于 MIME 类型为 XML 的文档。***
	
	- `default-style`
		
		***设置默认[CSS样式表](https://developer.mozilla.org/zh-CN/docs/Web/CSS)组的名称***
		
	- `x-ua-compatible`
		***定义浏览器的渲染方式***
		- 示例
			IE=edge      *选择IE最高版本进行渲染*
			chrome=1  *选择Chrome Frame(谷歌框架)进行渲染*
		~~~
		<meta content="IE=edge,chrome=1" http-equiv="X-UA-Compatible">
		~~~
	- `refresh`
		- ***`content`包含非负整数时——页面重新加载的秒数***
		- ***`content`包含非负整数后跟字符串`;url=`时——页面重定向到指定链接的秒数***
		~~~
		<!-- 3喵后刷新 -->
		<meta http-equiv="refresh" content="3" />
		
		<!-- 3喵后刷新,并重定向到"https://www.mozilla.org"这个链接 -->
		<meta http-equiv="refresh" content="3;url=https://www.mozilla.org" />
		~~~

>4 . `name`

- ***`name`可以定义的属性请在[标准元数据名称](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/meta/name)中查看***

***


### 3.1.7 HTML`<stript>`元素

>***该标签用于加载脚本文件,如JavaStript***
>
>***关于具体使用,在以后的章节进行阐述***

***


## 3.2代码主体基础

### 3.2.1 HTML`<body>`元素

>***`<body>`标签定义了HTML代码主体内容***

- **代码示例**
~~~
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
	<!-- 在这里键入网页主体 -->
</body>
</html>

~~~

>***通常的,我们在`<body>`标签内编辑HTML代码主体从而通过浏览器进行渲染***

### 3.2.2 HTML基本元素

#### 3.2.2.1 HTML`<h>`元素

>***该元素定义了网页正文的标题***

>***`<h1>~<h6>`标签定义了标题的层级***

>代码示例
~~~
<h1>这是一个标题</h1>
<h2>这是一个标题</h2>
<h3>这是一个标题</h3>
~~~

>***其中`<h1>`定义了最大的标题,`<h2>`定义了最小的标题***

- 注意
>请确保***HTML标题标签仅用于标题***,不要仅仅为了生成粗体或大号的文本使用标题
>搜索引擎使用***标题***为你的网页结构编制索引
>***标题是呈现文章结构的重要标签,请务必合理使用标题***
#### 3.2.2.2 HTML`<p>`元素

>***该元素定义了网页的段落***

>代码示例

~~~
<p>这是一个段落。</p>
<p>这是另外一个段落。</p>
~~~
- ***HTML`<br>`标签***
>***该元素在你不希望产生鑫段落的情况下进行换行***

- ***HTML`<hr>`标签***
>***该元素在HTML页面中创建水平线***

- ***HTML注释***
```
<!-- 这是一个注释 -->
```
#### 3.2.2.3 HTML`<a>`元素

>***该元素定义了网页中某文本执行的跳转链接***

>代码示例

~~~
<a href="https://www.runoob.com">这是一个链接</a>
~~~

>***HTML链接语法***
- `href`***指定链接的URL,可以是网页链接、文件的链接或其他资源的链接***
```
<a href="url">链接文本</a>
```
- `target`***指定链接如何在浏览器打开***
	- `_blank`***在新标签或窗口中打开链接***
	```
	<a href="http://www.runoob.com" target="_blank">访问菜鸟教程！</a>
	```
	- `_self`***在当前标签或窗口中打开链接***
	- `_parent`***在父框架集中打开被链接文档***
	- `_top`***在整个窗口中打开被链接文档。***
	- `frame name`***在指定的框架中打开被链接文档***
	```
	<frameset cols="100,*">
  <frame src="toc.html">
  <frame src="pref.html" name="view_frame">
  </frameset>


	<h3>Table of Contents</h3>
	<ul>
  <li><a href="pref.html" ==target="view_frame"==>Preface</a></li>
  <li><a href="chap1.html" ==target="view_frame"==>Chapter 1</a></li>
  <li><a href="chap2.html" ==target="view_frame"==>Chapter 2</a></li>
  <li><a href="chap3.html" ==target="view_frame"==>Chapter 3</a></li>
	</ul>
	```
- `title`***提供对链接的额外信息,鼠标悬停在链接上显示提示***]     
- `rel`***指定与链接目标的关系***

#### 3.2.2.4 HTML`<img>`元素

>***该元素在网页中插入图像***

>代码示例

~~~
<img decoding="async" src="/images/logo.png" width="258" height="39" />
~~~

### 3.2.3 HTML文本格式化