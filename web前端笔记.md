# web前端笔记

## 第一节10.26

**基本结构**：

```html
<!-- 声明文档类型-告诉浏览器我们要是用的html版本 -->
<!DOCTYPE html>
<!-- html网页部分 -->
<html lang="zh">
<!-- 网页头部-声明头信息 -->
<head>
	<!-- 设置字符编码集格式-解决乱码 -->
	<meta charset="UTF-8">
	<!-- 移动端配置 -->
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<!-- 标题 -->
	<title>Document</title>
</head>
<!-- 网页的主题部分-只要想实现在网页中的任何内容，都需要写在body中 -->
<body>
	<div style="width: 100px;height: 100px;color: #aaa;font-size: 50px;background-color: aquamarine;">121</div>
</body>
</html>
```

**文本标记**:

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=b, initial-scale=1.0">
	<title>Document</title>
	<!-- 2. 内部样式表 -->
	<!-- 不符合结构与样式的分离的理念 -->
	<!-- 方便、不需要新建CSS样式文件，并且可以控制多行样式 -->
	<!-- 平时练习中常用（代码量不是很多时使用） -->
	<style type="text/css">
		/* 选择器{
			属性名：属性值；
		} */
		i{
			color: green;
		}
	</style>
	
	<!-- 3. 外部样式表 -->
	<!-- 结构与样式分离，适合写大型项目，不适合平时练习 -->
	
	<link rel="stylesheet" href="要使用的CSS文件路径">
	<link rel="stylesheet" href="index.css">
	
</head>
<body>
	<!-- 1. 内联样式 -->
	<!-- 不符合结构（html）与样式（css）分离的理念 -->
	<!-- 不利于维护 -->
	<!-- 直观、JS中常用 -->
	<b style="color: red;">加粗</b>
	<i>倾斜</i>
	<u>下划线</u>
	<s>删除线</s>
	<sub>下标</sub>
	<sup>上标</sup>
	<span>使用最多的行内元素</span>
	<!-- 行内元素-在默认情况下，可以和其他行内元素在一行显示的元素 -->
</body>
</html>
```

## 第二节10.27

**其他的常用标记**：

```html
<!DOCTYPE html>
<html lang="zh">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Document</title>
</head>
<body>
	<!-- 段落元素P -->
	<!-- 特点
		1.独占一行
		2.上下行间距
		3.p标签中，不能嵌套其他块级元素
		4.p标签常用于页面中的纯文本
	-->
	<p>这是段落1</p>
	<p>这是段落2</p>
	
	<!-- 标题元素h1 - h6 -->
	<!-- 特点
		1.文本加粗
		2.文字尺寸依次减小
		3.独占一行
		4.有上下行间距
	-->
	<h1>这是h1</h1>
	<h2>这是h2</h2>
	<h3>这是h3</h3>
	<h4>这是h4</h4>
	<h5>这是h5</h5>
	<h6>这是h6</h6>
	
	
</body>
</html>
```

**块级元素&行内元素**:

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			b{
				/* 显示为块级元素 */
				display: block;  /* 使行内元素显示成块级元素 */
			}
			p{
				/* 显示为行内元素 */
				display: inline;	/* 使块级元素显示成行内元素 */
			}
			
		</style>
		
	</head>
	<body>
		<!-- 行内元素  -  在默认情况下，可以和其他行内元素在一行显示 -->
			<!-- b i u s sub sup span（没有任何默认样式的行内元素） -->	
		<b>加粗</b>	<!-- 在style中是b变为块级元素 -->
		<i>倾斜</i>
		<u>下划线</u>
		<s>删除线</s>
		<sup>sup</sup>
		<sub>sub</sub>
		
		<!-- 块级元素-在默认情况下，独占一行的元素 -->
			<!-- h1 - h6 ， p  ， div(没用任何默认样式的块级元素) -->	
		<p>段落</p>	<!-- 在style中是p变为行内元素 -->			

		
	</body>
</html>
```

**CSS中常用的样式**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			div{
				/* 1.文本颜色 */
				color: red;
				/* 2.背景颜色 */
				background-color: green;
				/* 3.文本尺寸 */
				font-size: 24px;
				/* 4.文本加粗 */
				/* font-weight: bold/100/200-900; */
				font-weight: bold;
				/* 5.文本修饰 - 是否加下划线 */
				text-decoration: underline;
				/* 6.字体 */
				font-family: "仿宋";
				/* 7.宽度 */
				width: 200px;
				/* 8.高度 */
				height: 200px;
				/* 9.文本排列 */
				/* text-align:left(左)/center（中）/right（右）; */
				text-align: right;
				
				
			}
			span{
				/* 文本颜色 */
				color: red;
				/* 2.背景颜色 */
				background-color: green;
				/* 3.文本尺寸 */
				font-size: 24px;
				/* 4.文本加粗 */
				/* font-weight: bold/100/200-900; */
				font-weight: 100;
				/* 5.文本修饰 - 是否加下划线 */
				text-decoration: underline;
				/* 6.字体 */
				font-family: "幼圆";
				/* 
				 行内元素设置的宽度和高度会失效
					7.宽度
					width: 200px;
					8.高度 
					height: 200px;
				*/
				
				/* 9.文本排列 */
				/* text-align:left/center/right; */
				text-align: center;		
			}
			/* 注： */
				/* 块级元素可以设置宽度高度 - 可以做页面布局 */
				/* 行内元素设置的宽度和高度会失效 - 网页中的细微控制 */
				/* 行内元素不可以设置内容居中 */
				/* 块级元素居中的前提是元素本身大小一定要比内容的宽度 大 */
				
		</style>
	</head>
	<body>
		<div>这是div</div>
		<span>这是span</span>
	</body>
</html>
```

**文本标记练习**：

```html
<!DOCTYPE html>
<html>
<head>
	<title></title>
	<meta charset="utf-8">
	<style>
		span{
			color: red;
		}
		h1{
			text-align: center;
		}
	</style>
</head>
<body>
<!-- 实业字符 -->
<!-- 
	<   &lt;
	>   &gt;
	空格 &nbsp;
	©    &copy;
	￥   &yen;
 -->
 <!-- 在html中所有的空格和换行都会被解析成一个空格 -->
<h1>HTML5<span>&lt;Day01&gt;</span></h1>
<hr> 	<!--分割线hr-->
<h2 id="test">1 HTML 文档片段</h2>   <!-- id="test"是10.29中锚点的测试 -->
<h3>1.1 问题</h3>
<p>创建如图-1所示的HTML页面</p>
<h3>1.2 方案</h3>
<p>使用HTML标记来完成该页面效果</p>
<h3>1.3 实现</h3>
<p>
	建立一个文本文件，并修改文件名称为first.html,然后使用文本编辑器打开该文件，
	并为该文件添加代码，以创建标准格式的HTML文档。
</p>
<p>然后，在body元素中添加代码，以创建居中显示的段落文本。代码如下所示：</p>

<!-- 	<pre>-预格式化 - 保留源文件中代码的格式-->
<pre>
	&lt;p align="center" title="段落"&gt;
		居中显示的文本
	&lt;/p&gt;
</pre>
<div></div>
</body>
</html>
```

## 第三节10.29

**img&超链接**

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
        <style>
           img{
				width:500px;
				/* height:400px; */
				/* 如果只设置图片的宽度或高度其中的一个属性时，另外一个属性也会跟着等比缩放 */
				/* 如果强行设置宽度高度，可能会改变图片原有比例，造成图片拉伸，影响用户体验 */
				/* 圆角图片 */
				border-radius: 50%;/* 50%是圆（方形图片）或者椭圆（长方形图片） */
				
			}
        </style>
	</head>
	<body>
        	<!--常见的图片格式
		 jpg - 压缩比例大， 图片质量低
		 png - 支持透明背景 - 一般在网页的logo都是png的
		 gif - 支持动图
		 webp - 网页中的专用图片格式，质量约为jpg格式的1/3
		 -->
		 <!-- <img src="要使用的图片资源的路径" alt="当图片无法正常加载时的提示文字"> -->
		 <!-- title - 当鼠标移到图片上时的提示文字 -->
		 <img src="images/松树.JPG" alt="松树被砍了....." title="松树">
		 <img src="https://img0.baidu.com/it/u=1472391233,99561733&fm=253&fmt=auto&app=138&f=JPEG?w=889&h=500" alt="">
		 <!-- 路径 -->
		 <!-- 
			相对路径
				从当前文件位置开始找资源的过程
				/ 下一级
				../ 返回上一级
			绝对路径
				从服务器端开始的路径
				从项目根目录开始找的路径
			根相对路径
				从盘符位置开始找的路径
		  -->
		 
		 
		 
		 
        
		<!-- 超链接 - 帮助用户完成点击跳转 -->
		<!-- <a href="要跳转到的资源的地址">提示的文字或图片</a> -->
		<!-- target="_blank" - 新建页面跳转  不加target="_blank"属性将原页面刷新-->
		<a href="https://www.baidu.com/" target="_blank">跳转到百度</a>
		<a href="../10.27/4.文本标记练习.html">文本标记练习</a>
		<a href="images/松树.JPG">跳转到图片</a>
	</body>
</html>
```

**超链接的四种状态**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			/* hover 和 active可以适用于所有元素*/
			a:link{
				/* 当超链接没有被访问过时的样式 */
				color: green;
			}
			a:visited{
				/* 当超链接已经被访问过的样式 */
				color:black;
			}
			a:hover{
				/* 当鼠标移动到超链接上时的样式 */
				color:pink;
			}
			a:active{
				/* 当超链接被选中时的样式 */
				color:red;
			}
			/* 注：如果我们同时设置了多种状态，那么需要按照 l v h a 的顺序静进行编写 */
		</style>
	</head>
	<body>
	<a href="https://www.baidu.com/">跳转</a>
	</body>
</html>
```

**锚点**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			div{
				height: 600px;
			}
		</style>
	</head>
	<body>
		<!-- 锚点 -->
		<!-- 2.链接到锚点 -->
		<a href="../10.27/4.文本标记练习.html#test">跳转到文本标记练习的第一部分</a>
		<a href="#a1">苍兰诀</a>
		<a href="#a2">弟媳</a>
		<a href="#a3">摸索</a>
		<!-- 1.创建锚点 -->
		<div></div>
		<div id="a1">打架互欧 <a href="#">返回顶部</a></div>
		<div id="a2">haokan <a href="#">返回顶部</a></div>
		<div id="a3">抱歉 <a href="#">返回顶部</a></div>
	</body>
</html>
```



## 第四节11.02

**列表**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			ul{
				list-style-type:none;
			}
			ol{
				list-style-type:none; 
			}
		</style>
	</head>
	<body>
		<!-- 列表 - 将一些具有相似特征对的元素进行一个整齐的排列 -->
		<!-- 有序列表 ol   无序列表 ul -->
		<!-- 列表项 li -->
		
		<!-- 有序列表 -->
		<!-- 前面的数字称之为列表标识 -->
		<ol type="1" start="3">
			<!-- type = 1 a A i I -->
			<!-- start - 控制有序列表的开始位置 写数字 是几就是从第几位开始-->
			<li>水果</li>
			<li>蔬菜</li>
			<ol>
				<li>土豆</li>
				<li>西红柿</li>
				<li>大头菜</li>
				<li>茄子</li>
			</ol>
			<li>粮油</li>
			<ul>
				<li>酱油</li>
				<li>面</li>
			</ul>
			<li>零食</li>
		</ol>
		
		
		<!-- 无序列表 ul -->
		<ul type="square">
			<!-- 默认为实心圆 -->
			<!-- circle - 空心圆 -->
			<!-- square - 实心方块 -->
			<!-- none - 去掉列表项标识 -->
			<li>果汁</li>
			<li>饮料</li>
			<ul>
				<li>雪碧</li>
				<li>可乐</li>
				<li>美年达</li>
				<li>芬达</li>
			</ul>
			<li>奶</li>
			<ol>
				<li>牛奶</li>
				<li>羊奶</li>
			</ol>
			<li>水</li>
		</ul>
	</body>
</html>
```

**浮动**：

````html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			/* * - 选择页面中所有的元素 */
			*{
				/* 外边距 */
				margin: 0;
				/* 内边距 */
				padding: 0;
			}
			ul{
				/* 清空默认的内边距 */
				/* 外边距 */
				margin: 0;
				/* 内边距 */
				padding: 0;
				
				list-style: none;
			}
			li{
				width: 200px;
				height: 200px;
			}
			/* .a1选择页面中class为a1的元素*/
			.a1{
				background-color: red;
				/* 浮动 - 网页布局 */
				/* float: none/left/right; */
				/* 浮动的特点：
					1.浮动的元素脱离文档流，不占据页面空间，后续元素会上前补位
					2.浮动的元素会停靠在包含框的左边或者右边，取决于区域为lift或者是right
					3.浮动元素会失去独占一行的特点
					4.** - 如果浮动的元素前已经有一个浮动的元素，那么会停靠在这个浮动元素的旁边
					5.** - 浮动是专门解决块级元素在一行显示的问题
				 */
				float: left;
			}
			.a2{
				background-color: green;
				float: lift;
			}
			.a3{
				background-color: blue;
				float: left;
			}
		</style>
	</head>
	<body>
		<ul>
			<li class="a1"></li>
			<li class="a2"></li>
			<li class="a3"></li>
		</ul>
	</body>
</html>
````

## 第五节11.04

**浮动可能产生的问题**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				margin: 0;
				padding: 0;
			}
			ul{
				
				list-style: none;
				/* 当一个元素中的元素都设置了浮动，那么这个父元素产生的高度为0的问题 */
				/* 1.直接给父元素加高度 */
					/* height: 200px; */
				/* 2.让父元素也浮动起来,将后续元素设置为清除浮动 */
					/* float: left; */
				/* 4.固定用法 - 溢出隐藏 - 不要再下拉框中使用 */
					/* overflow: hidden; */
			}
			/* 3.使用伪类的方式创建元素并清除浮动 */
			ul:after{
				display: block;
				content: "";
				clear: both;
			}
			li{
				width: 200px;
				height: 200px;
			}
			/* .a1选择页面中class为a1的元素*/
			.a1{
				background-color: red;
				/* 浮动 - 网页布局 */
				/* float: none/left/right; */
				/* 浮动的特点：
					1.浮动的元素脱离文档流，不占据页面空间，后续元素会上前补位
					2.浮动的元素会停靠在包含框的左边或者右边，取决于区域为lift或者是right
					3.浮动元素会失去独占一行的特点
					4.** - 如果浮动的元素前已经有一个浮动的元素，那么会停靠在这个浮动元素的旁边
					5.** - 浮动是专门解决块级元素在一行显示的问题
				 */
				float: left;
			}
			.a2{
				background-color: green;
				float: left;
			}
			.a3{
				background-color: blue;
				float: left;
			}
			
			/* 浮动产生的影响 */
			div{
				width: 200px;
				height: 200px;
				background-color: black;
				/* 清除浮动 */
				/* clear: left（左）/right（右）/none（不）/both（两侧） */
				/* 清除两侧浮动 */
				/* clear: both; */
			}
		</style>
	</head>
	<body>
		<ul>
			<li class="a1"></li>
			<li class="a2"></li>
			<li class="a3"></li>
		</ul>
		<div></div>
	</body>
</html>
```

## 第六节11.09

**尺寸和单位**:

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			h1{
				font-size: 20px;
			}
			div{
				width: 10em;
				/* 尺寸
				 px 像素
				 % 百分比 （相对定位，相对于父元素）
				 mm 毫米
				 cm 厘米
				 in 英寸
				 pt 磅
				 em 相对单位（相对于父元素）
				 rem 相对单位(相对于根元素 html)
				 */
				height: 200px;
				background-color: rgba(203, 77, 34, 0.4);
				/* 颜色单位 - 合法的颜色值
					1.直接使用英文单词
					2.#rrggbb; #六位十六进制数字
					0-9 a-f
					如果rgb的值两两一样，可以简写为#rgb
					#aabbcc == #abc
					#000000 == #000
					#fff 白色
					#f00 红色
					#0f0 绿色
					#00f 蓝色
					如果rgb的值相同，则为灰色，越接近0，颜色越深，越接近f，颜色越浅
					#333
					#666
					#999
					#aaa
					#eee
				属性：透明度
				
				opacity：0 - 1；
				越接近0，越透明
				 越接近1，越不透明
				3. rgb(r,g,b); - 比较适用于js中随机生成颜色
				0-255
				rgba(r,g,b,a)
					a - 通道(透明度) - 取值范围：0-1
					越接近0，越透明
					越接近1，越不透明
				 */
			
			}
		</style>
	</head>
	<body>
		<h1>
		<div></div>	
		</h1>
	</body>
</html>
```

## 第七节11.11

**过渡**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				padding: 0px;
				margin: 0px;
			}
			div{
				width: 200px;
				height: 200px;
				background-color: red;
				font-size: 150px;
				text-align: center;
				/* line-height 行高 */
				line-height: 200px;
				color: #fff;
				
				
				/* 过渡  - 注 写在发生变化的元素中 */
				/* transition: 过渡属性 过渡时间 过渡速度函数 过渡的延时; */
				/* transition: background-color 2s; */
					/* 过渡属性 - 取值为数值的属性基本都可以 */
					/* 过渡速度函数 - 默认值为 先快后慢 */
						/* linear - 匀速 */
					/* 延时 - 默认值是不延时 */
					
				/*注： 一个元素只能设置一个transition过渡 当两个过渡出现会执行第二个*/
				/* 单独写color，前面的 background-color会被覆盖 而两个一起写也会只出现一个 */
				/* transition: background-color,color 2s; */
				/* transition: all 3s; */
					/* all - 所有发生变化的属性都过渡 */
					/* 0.3 - 0.5 之间时用户体验最好的过渡时间 */
					
				/* 如果发生变化的属性中只有部分属性发生过渡，就不能使用简写方式了 */
				/* 过渡属性 */
				transition-property: width,height,line-height;
				/* 过渡时间 */
				transition-duration: 2s;
				/* 过渡速度函数 */
				/* transition-timing-function: ; */
				/* 过渡延迟 */
				/* transition-delay: ; */
			}
			div:hover{
				background-color: green;
				color: #000;
				width: 300px;
				height: 300px;
				line-height: 300px;
			}
		</style>
	</head>
	<body>
		<!-- 过渡 -->
		<!-- 简写方式 -->
		<div>帅</div>
	</body>
</html>
```

**边框&边框倒角**

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				margin: 0;
				padding: 0;
			}
			div{
				width: 200px;
				height: 200px;
				background-color: pink;
				/* 边框 */
				/* 边框宽度 */
				/* border-width: n px; */
				/* 边框样式 */
				/* border-style: solid; */
					/* solid - 实线 */
				/* 边框颜色 */
				/* border-color: 合法颜色值; */
				
				/* border-width: 10px; */
					/* 默认是2px的边框 */
				/* border-style: solid; */
					/* 必须的条件 */
						/* dashed - 虚线 */
						/* dotted - 点状边框 */
						/* double - 双线 */
				/* border-color: red; */
					/* 默认是黑色的边框 */
					
				/* 边框的简写方式 */
				/* border: 宽度 样式 颜色; */
				/* border: 10px solid red; */
				/* 常用边框用法 */
					/* 1个像素的灰色的实线边框 */
				/* border: 1px solid #ccc; */
				/* 边框的单边定义 */
				/* border-方向: n px; */
					/* 方向: top、right、bottom、left; */
				border-left: 2px solid #f00;
				border-bottom: 10px double orange;
				border-right: 5px dotted purple;
				border-left: 3px dashed darksalmon;
				
				/* 单独定义元素某个方向的某个属性 */
				/* border-方向-属性: 属性值; */
				border-bottom-style: solid;
				border-top-width: 10px;
			}

			div{
				width: 200px;
				height: 200px;
				background-color: pink;
				/* 边框倒角 */
				/* border-radius: px / %; */
				border-radius: 50px;
				/* border-radius: 50%; */
				/* 注意: 当元素为正方形时 取值为元素边长的1/2时相当于50% */
				/* 注意: 当元素本身不是正方形的时候,注意取值为px和%的区别 */
				border-radius: 20px 40px 60px 80px;
				/* 
					取值为1个值
						值1 四个角的倒角
					取值为2个值
						值1 左上角 右下角
						值2 右上角 左下角
					取值为3个值
						值1 左上角
						值2 右上角 左下角
						值3 右下角
					取值为4个值
						值1 左上角
						值2 右上角
						值3 右下角
						值4 左下角
				 */
				/* 可读性差，如果只是其中的一个角或者俩个角发生了倒角，不建议使用这种方式 */
				
				/* 边框倒角的单边定义 */
				/* border-上下方向-左右方向-radius: ; */
				
				
			}
			
		</style>
	</head>
	<body>
		<div></div>
	</body>
</html>
```



## 第八节11.12

**边框的特殊用法**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			div{
				width: 0px;
				height: 0px;
				border: 100px double transparent;
					/* transparent - 透明色 */
				border-top-color: #f00;
				border-right-color: #0f0;
				border-bottom-color: #00f;
				border-left-color: #ff0;
				
				/* border-radius: 50%; */
				border-radius: 50% 50% 50% 0px ;
			}
		</style>
	</head>
	<body>
		<div></div>
	</body>
</html>
```

## 第九节11.16

**框模型**:

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				margin: 0;
				padding: 0;
			}
			div{
				width: 200px;
				height: 200px;
				border: 2px solid purple;
			}
			.a1{
				background-color: green;
				/* 框模型（盒子模型） */
				/* 外边距 - margin - 围绕在元素周围的空白区域 */
				/* 主要用来调整元素与元素之间距离 */
				/* 上外边距/左外边距会控制元素本身移动 */
				/* 下外边距/右外边距会控制后续的元素进行位置的移动 */
				margin: 20px 40px;
				/* 取值
					margin: 值1;
						上下左右四个方向的外边距
					margin: 值1 值2;
						值1代表上下外边距
						值2代表左右外边距
					margin: 值1 值2 值3;
						值1代表上外边距
						值2代表左右外边距
						值3代表下外边距
					magrin: 值1 值2 值3 值4;
						分别带边上右下左四个方向的外边距						
					*/	
				 /* 可读性差 */
				 /* margin:0px 0px 0px 50px; */
				 /* 外边距的单边定义 */
				 		/* margin-方向: n px; */
				 		/* 方向: top/right/bottom	 */
						  
				/* 特殊的取值 auto
					控制块级元素在当前行左右居中显示
					注意: 当前元素必须有宽度 
					*/
				/* 大多使用方法  - 结合使用不单独使用*/
				/* margin: 0px auto;
				margin: 10px aauto 30px; */	
				
				/* 居中的方式总结
					1. txt-align: center;
						控制块级元素中内容左右居中
					2. line-height: 当前元素高度;
						控制块级元素中内容垂直居中
					3. margin: 0px auto;
						控制块级元素本身水平居中
				 */
				
				/* 内边距 - padding - 边框和内容之间的距离 */
				/* 内边距会将元素撑大 */
				/* 背景颜色是从边框位置开始绘制，内边距上也会有背景颜色 */
				padding: 20px 0px 50px;
				/* 取值
				padding: 值1;
				 	上下左右四个方向的内边距
				padding: 值1 值2;
				 	值1代表上下内边距
				 	值2代表左右内边距
				padding: 值1 值2 值3;
				 	值1代表上内边距
				 	值2代表左右内边距
				 	值3代表下内边距
				padding: 值1 值2 值3 值4;
				 	分别带边上右下左四个方向的内边距
				 */
				/* 可读性差 */
				/* padding:0px 0px 0px 50px; */
				/* 内边距的单边定义 */
						/* padding-方向: n px; */
						/* 方向: top/right/bottom	 */
			}
			.a2{
				background-color: red;
			}
		</style>
	</head>
	<body>
		<div class="a1">A1</div>
		<div class="a2">A2</div>
	</body>
</html>
```

**框模型注意事项&特殊使用**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				margin: 0;
				padding: 0;
			}
			div{
				background-color: red;
				height: 30px;
				/* 固定用法 - 解决外边距溢出的问题 */
				overflow: hidden;
			}
			/* 注意：如果两个元素的外边距发生重叠，则优先使用较大的外边距 */
			.a1{
				margin-botton: 20px;
			}
			.a2{
				margin-top: 15px;
			}
			/* 注意： 给行内元素设置上下外边距会失效 */
			/* span{
				background-color: green;
				margin: 20px;
				padding: 10px;
			} */
			p{
				margin-top: 20px;
			}
            
            	/* 框模型的特殊用法 */
				box-sizing: border-box;
				/* 改变盒子模型的计算方式 */
					/* 设置的尺寸包含(如200px) = 内容（会被压缩）+内边距+边框 */
			}
			/* 元素在页面中实际所占的宽度 = 内容宽度 + 左右内边距 + 左右边框 + 左右外边距*/
			/* 元素在页面中实际所占的宽度 = 内容宽度 + 上下内边距 + 上下边框 + 上下外边距*/
		</style>
	</head>
	<body>
		<div class="a1">A1</div>
		<div class="a2">
			<p>这是a2中的p</p>
		</div>
		<span>SPAN</span>
	</body>
</html>
```



## 第十节11.18

**相对定位**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				padding: 0;
				margin: 0;
			}
			div{
				width: 200px;
				height: 200px;
			}
			.a1{
				background-color: red;
				/* 定位 - 移动元素位置 */
				/* 定位的分类
					1. 普通流定位 - 文档流
					2. 浮动定位
					3. 相对定位
					4. 绝对定位
					5. 固定定位
				 */
				/* 相对定位 */
				/* 特点
					1. 配合偏移属性使用（top/right/left/bottom）,距离哪个方向有多少距离的意思
					2. 相对定位的元素不会脱离文档流，依然会占据页面空间，后续的元素不会上前补位
					3. 相对于自己本身之前的位置进行定位
					4. 相对定位适用于页面中元素位置的微调
					5. 经常配合绝对定位一起出现（常用）
				 */
				position: relative;
				left: 100px;
				/* top: 100hpx; */
				
			}
			.a2{
				background-color: green;
			}
			h1{
				width: 400px;
				height: 400px;
				border: 1px solid #000;
				margin: 100px auto;
				padding-left: 100px;
			}
		</style>
	</head>
	<body>
		<h1>
			<div class="a1"></div>
			<div class="a2"></div>
		</h1>
	</body>
</html>
```



**绝对定位**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			*{
				padding: 0;
				margin: 0;
			}
			div{
				width: 200px;
				height: 200px;
			}
			.a1{
				background-color: red;
				/* 绝对定位 */
				/* 特点
					1. 配合偏移属性使用（top/right/left/bottom）,距离哪个方向有多少距离的意思
					2. 绝对定位的元素会脱离文档流，不会占据页面空间，后续的元素上前补位
					3. 绝对定位的元素会相对于已经定位的祖先元素进行定位，如果没有已经定位的祖先元素，则会相对于最初的包含框，进行定位 
					4. 绝对定位的块级元素会失去独占一行的特点。absolute和auto冲突
					5. 子绝父相（祖先元素均可）
						子元素是绝对定位，父元素相对定位解决absolute和auto冲突
					6. 绝对定位常用与页面中图文混排，下拉框的实现
					7. 如果一个元素中的子元素都设置了绝对定位，那么这些子元素的位置会是初始化，后续的元素会压在前面元素的上边
				 
				 */
				position: absolute;
				/* top: 100px;
				left: 100px; */
				
				
			}
			.a2{
				background-color: green;
				position: absolute;
			}
			.a3{
				background-color: black;
				position: absolute;
			}
			h1{
				width: 400px;
				height: 400px;
				border: 1px solid #000;
				margin: 100px auto;
				padding-left: 100px;
				position: relative;
			}
		</style>
	</head>
	<body>
		<h1>
			<div class="a1"></div>
			<div class="a2"></div>
			<div class="a3"></div>
		</h1>
	</body>
</html>
```

## 第十一节11.23

**基础选择器**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			/* 1. 通用选择器 - 选择页面中所有元素 */
			*{
				
			}
			/* 2. 元素选择器 - 以标签名称作为选择器 */
				/* 很多样式具有继承性 */
				/* 选择页面中的div*/
			div{
				
			}
			/* 3. 类选择器 - 给元素添加class属性， 并设置类名，通过，类名的方式选择页面中的元素 */
			/* 选择页面这中class 为a1的元素 */
			/* 灵活性 - 没有限制次数 */
			/* 常用于页面中写样式 */
			.a1{
				
			}
			/* 3.1 多类选择器 - 同时使用多个类的样式，类名和类名之间用空格隔开 */
			/* 例： <div class="a a1"></div> */
			.a{
				
			}
			/* 3.2 分类选择器 - 对元素的细分控制 */
			/* 选择页面中class为a1的h1元素 */
			h1.a1{
				
			}
			
			/* 4. id选择器 - 给元素添加id属性，并设置id名，通过 #id名选择页面中元素 */
			/* 唯一性 - 同一个id值在一个页面中只能出现一次 */
			/* 在js中使用的频率更高，常用于布局 */
			#aaa{}
			
			/* 5. 群组选择器 - 为多个元素设置相同样式 */
			/* 选择器1，选择器2,选择器3,...{} */
			/* .a1,#aaa,div{} */
			
			/* 6. 后代选择器 */
			/* 祖先元素 后代元素{}  - 后代 - 儿子孙子... */
			/* 选择class为a的元素下所有div */
			.a div{}
			
			/* 7. 子代选择器  */
			/* 父代选择器>子代选择器{} */
			/* 选择class为a的元素下所有儿子div */
			.a>div{}
			
			/* 8. 伪类选择器 - 给元素添加一些特殊效果 */
			/* 选择器：伪类{} */
			/* :link :visited :active : after :before */
			div:hover{}
			
			
		</style>
	</head>
	<body>
		
	</body>
</html>
```

**高级选择器**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			/*1. 兄弟选择器 */
			/* 选择页面中class为axl元素后的第一个兄弟li元素 */
			/* .axl+li{
				color: red;
			} */
			
			/* 选择页面中class为axl元素后的所有兄弟li元素 */
			/* .axl~li{
				color: red;
			} */
			
			/* 2. 属性选择器 */
				/* [属性]  */
			/* 选择页面中带有class属性的元素 */
			/* [class]{
				color: red;
			} */
			/* 选择页面中带有class属性的li元素 */
			/* li[class]{
				color: red;
			} */
			
			/* 3. 选择第一个子元素 */
			/* ul li:first-child{
				color: red;
			} */
			
			/* 4. 选择最后一个子元素 */
			/* ul li:last-child{
				color: red;
			} */
			
			/* 5. 选择任意一个子元素 */
			/* ul li:nth-child(2){
				color: red;
				取值：
					n 选择第几个
					2n 选择偶数的li
					2n-1 选择奇数的li
					n+6 从第六个开始到最后一个
					-n+6 前六个
					3n 选择3的倍数
			} */
			
			/* 6. 非选择器 */
			/* :not(选择器){} */
			ul li:not([class]){
				color: red;
			}
			
		</style>
	</head>
	<body>
	<ul>
		<li>你</li>
		<li>好</li>
		<li class="axl">啊</li>
		<li>猪</li>
		<li class="jy">！！</li>
		<li>1</li>
		<li>2</li>
		<li>3</li>
		<li>4</li>
		<li>5</li>
		<li>6</li>
	</ul>
	</body>
</html>
```

## 第十二节11.25

**背景属性**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			div{
				width: 600px;
				height: 600px;
				border: 1px solid #000;
				/* 1. 背景颜色 */
				background-color: red;
				/* 2. 背景图片 */
				background-image: url(DSC_3947.JPG);
				/* 3. 背景图片 */
				/* background-size: w h; */
				background-size: 230px 300px;
				/* 4. 背景平铺 */
				/* no-repeat 不平铺 */
				background-repeat: no-repeat;
				/* 注意： 当背景图片和背景颜色同时设置时，背景图片会压在背景颜色的上边 */
			}
			
			
		</style>
	</head>
	<body>
		<div></div>
	</body>
</html>
```

**精灵图的使用方法**：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title></title>
		<style>
			div{
				width: 34px;
				height: 26px;
				/* 将精灵图作为背景图像引入到元素中，并且通过背景图像定位的方式移动背景图像，以便显示小图 */
				background-image: url(Icl.jpg);
				background-repeat: no-repeat;
				/* 背景图像定位 - 移动背景图像位置 */
				/* background-position: x y; */
					/* x 取值为正 向右移动 */
					/* x 取值为负 向左移动 */
					/* y 取值为正 向下移动 */
					/* y 取值为负 向上移动 */
					/* 如果要取精灵图中的某个小图，取值一定小于零 */
					background-position: -36px -231px;
			}
		</style>
	</head>
	<body>
		<div></div>
	</body>
</html>
```



## 练习

**画图**：

```vue
<script setup>

</script>

<template>
  <div class="contain">
    <figure class="panda">
    </figure>
  </div>
  
</template>



<style scoped>
.contain {
    width: 31em;
    height: 26em;
    background-color: rgb(24, 145, 135);
    border-radius: 5%;
    margin-top: 100px;
    margin-left: 40%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
 
  .panda {
    width: 21em;
    height: 16em;
    background-color: white;
    border-width: 3px 3px 6px 6px;
    border-style: solid;
    border-color: black;
    border-radius: 11em 11em 11em 11em/11em 11em 6em 6em;
    position: relative;
    background-image: radial-gradient(ellipse at 50% 60%, #333 1.2em, transparent 1.2em),
      radial-gradient(ellipse at 50% 80%, #333 0.6em, transparent 0.6em);
    box-shadow: inset 1em -1em 0#eee;
  }
 
  .panda::before {
    width: 7em;
    height: 4em;
    content: '';
    position: absolute;
    background-color: #333;
    top: 5.5em;
    left: 2.9em;
    border-radius: 50% 50% 42% 42%;
    transform: rotate(314deg);
    background-image: radial-gradient(circle at 5.1em 2em, white 0.3em, transparent 0.3em), radial-gradient(circle at 4.6em 2em, #333 0.7em, transparent 0.7em),
      radial-gradient(circle at 4.5em 2em, white 1em, transparent 1em);
    box-shadow: -1em -7.2em 0 -0.4em #333;
  }
 
  .panda::after {
    width: 7em;
    height: 4em;
    content: '';
    position: absolute;
    background-color: #333;
    top: 5.5em;
    left: 11.5em;
    border-radius: 50% 50% 42% 42%;
    transform: rotate(45deg);
    background-image: radial-gradient(circle at 1.6em 2em, white 0.3em, transparent 0.3em), radial-gradient(circle at 2.1em 2em, #333 0.7em, transparent 0.7em),
      radial-gradient(circle at 2.2em 2em, white 1em, transparent 1em);
    box-shadow: 0.8em -6.8em 0 -0.4em #333;
  }

</style>
```

**小米**

```vue
<script setup>
import { reactive } from '@vue/reactivity'
let GoodsData = reactive([
  {imgUrl:'src/assets/chazuo.png',descripe:'小米智能插座，基础版',solgen:'手机远程遥控，让普通电器变智',price:'49元'},
  {imgUrl:'src/assets/jinghuaqi.png',descripe:'小米空气净化器2',solgen:'净化能力高达310m3/h',price:'699元'},
  {imgUrl:'src/assets/chaban.png',descripe:'小米智能插线板',solgen:'手机远程控制家中电器，智能节电',price:'69元'},
  {imgUrl:'src/assets/erji.png',descripe:'小米圈铁耳机',solgen:'动圈+动铁，双发声单元',price:'69元'}
])

</script>
<template>
    <ul>
      <li v-for="(goods, index) in GoodsData" :key=index>
        <div class="img-box">
        <img :src="goods.imgUrl" alt="">
         </div>
          
          <h4>{{goods.descripe}}</h4>
          <p>{{goods.solgen}}</p>
          <div class="price">{{goods.price}}</div>
       
      </li>
  </ul>
</template>



<style scoped>
*{
  margin: 0;
  padding: 0;
}

ul{
  list-style: none;
  width: 1000px;
  margin: 100px auto;
}
li{
  width: 200px;
  height: 320px;
  background-color: #fafafa;
  text-align: center;
  float: left;
  margin: 0 10px;
  border-top: 1px solid transparent;
}

ul li:nth-child(1){
  border-color: #ffac13;
}
ul li:nth-child(2){
  border-color: #83c44e;
}
ul li:nth-child(3){
  border-color: #2196f3;
}
ul li:nth-child(4){
  border-color: #e53935;
}
.img-box{
  width: 100%;
  height: 200px;
  text-align: center;
  line-height: 200px;
}
.img-box img{
  vertical-align: middle;
}
li h4{
  font-weight: 400;
  margin-top: 10px;
}
li p{
  font-size: 14px;
  color: #aaa;
  margin: 10px 0px;

}
.price{
  font-size: 14px;
  color: orange;
}


</style>
```

**淘宝**：

```vue
<script setup>
import { reactive } from "@vue/reactivity";

let showData = reactive([
  "充话费",
  "旅行",
  "车险",
  "游戏",
  "彩票",
  "电影",
  "酒店",
  "理财",
]);
</script>

<template>
  <ul>
    <li v-for="(data, index) in showData" :key="index">
      <div :style="{ backgroundPositionY: -index * 45 + index + 'px' }"></div>
      <p>{{ data }}</p>
    </li>
  </ul>
</template>

<style scoped>
*{
    margin: 0;
    padding: 0;
}
ul{
    list-style: none;
    width: 320px;
    margin: 0px auto;
}
ul li {
  width: 80px;
  height: 100px;
  text-align: center;
  box-sizing: border-box;
  float: left;
  margin-left: -1px;
  margin-top: -1px;
  border: 1px solid #ccc;
  list-style: none;
}
ul div {
  width: 24px;
  height: 30px;
  background-image: url(../assets/a1.png);
  background-position-x: 0px;
  margin: 20px auto 10px;
}
ul p {
  text-align: center;
  font-size: 14px;
}
</style>
```



