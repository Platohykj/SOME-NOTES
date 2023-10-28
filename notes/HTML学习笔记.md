***
***本文兼容HTML5***
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

![[Pasted image 20231028210430.jpg]]就这样，一个文件头就写好了喵
***
**代码示例**
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
## 3.1 对代码头的进一步阐释
### 3.1.1 HTML`<head>`元素

***`<head>`元素包含了所有头部标签元素***

>其中我们可以插入

- 脚本（scripts）
- 样式文件（CSS)
- 各种mata信息
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

### 3.1.4HTML`<link>`元素
- 本***HTML***笔记不对其进行过多阐述

>本标签定义了文档与外部资源的关系
>其通常用于链接样式表

- 下面是一个实例
~~~
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
~~~
### 3.1.5HTML`<style>`元素

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
