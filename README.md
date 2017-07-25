# HTML5-CSS3-新特性
新增的 标签 属性 方法

#HTML5—CSS3新特性
###HTML的新特性15个常用的

####1.新的文档类型  (New Doctype)

目前许多网页还在使用XHTML 1.0 并且要在第一行像这样声明文档类型：

	<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
	"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

在HTML5中，上面那种声明方式将失效。下面是HTML5中的声明方式：

	<!DOCTYPE html>

####2.脚本和链接无需type  (No More Types for Scripts and Links)

在HTML4或XHTML中，你需要用下面的几行代码来给你的网页添加CSS和JavaScript文件。

	<link rel="stylesheet" href="path/to/stylesheet.css" type="text/css">
	<script type="text/javascript" src="path/to/script.js">

而在HTML5中，你不再需要指定类型属性。因此，代码可以简化如下：

	<link rel="stylesheet" href="path/to/stylesheet.css">
	<script src="path/to/script.js">

####3.语义Header和Footer (The Semantic Header and Footer)

在HTML4或XHTML中，你需要用下面的代码来声明"Header"和"Footer"。

	<div id="header"></div>
	<div id="footer"></div>

在HTML5中，有两个可以替代上述声明的元素，这可以使代码更简洁。

	<header></header>
	<footer></footer>

####4.Hgroup


在HTML5中，有许多新引入的元素，hgroup就是其中之一。假设我的网站名下面紧跟着一个子标题，我可以用< h1>和< h2>标签来分别定义。然而，这种定义没有说明这两者之间的关系。而且，h2标签的使用会带来更多问题，比如该页面上还有其他标题的时候。
在HTML5中，我们可以用hgroup元素来将它们分组，这样就不会影响文件的大纲。
	
	<header>
		<hgroup>  <== 这里加
			<h1>Recall Fan Page </h1>  
			<h2>Only for people who want the memory of a lifetime. </h2>
		</hgroup> 
	</header>
 
####5.标记元素 (Mark Element)

你可以把它当做高亮标签。被这个标签修饰的字符串应当和用户当前的行动相关。比如说，当我在某博客中搜索“Open your Mind”时，我可以利用一些JavaScript将出现的词组用<mark>修饰一下。

		<h3>Search Results</h3>
	<p>
	They were interrupted, just after Quato said, 
		<mark>"Open your Mind"</mark>   <== 这里
	</p>
	 
####6.图形元素 (Figure Element)

在HTML4或XHTML中，下面的这些代码被用来修饰图片的注释。

	<img src="path/to/image" alt="About image">
	<p>Image of Mars.</>

然而，上述代码没有将文字和图片内在联系起来。因此，HTML5引入了<figure>元素。当和<figcaption>结合起来后，我们可以语义化地将注释和相应的图片联系起来。

	<figure>
			<img src="path/to/image" alt="About image"> 
		<figcaption> 
			<p>This is an image of something interesting. </p> 
		</figcaption>
	</figure>

####7.重新定义<small> (Small Element redefined)

在HTML4或XHTML中，< small>元素已经存在。然而，却没有如何正确使用这一元素的完整说明。在HTML5中，< small>被用来定义小字。试想下你网站底部的版权状态，根据对此元素新的HTML5定义，< small>可以正确地诠释这些信息。

####8.占位符 (Placeholder)

在HTML4或XHTML中，你需要用JavaScript来给文本框添加占位符。比如，可以提前设置好一些信息，当用户开始输入时，文本框中的文字就消失。
而在HTML5中，新的“placeholder”就简化了这个问题。

	<form action="demo_form.asp" method="get">
	  <input type="search" name="user_search" placeholder="Search W3School" />
	  <input type="submit" />
	</form>

####9.必要属性 (Required Attribute)

HTML5中的新属性“required”指定了某一输入是否必需。有两种方法声明这一属性。

	<input type="text" name="someInput" required>

	<input type="text" name="someInput" required="required">

当文本框被指定必需时，如果空白的话表格就不能提交(和非空验证差不多形状)。下面是一个如何使用的例子

	<form action="/example/html5/demo_form.asp" method="get">
		<input type="search" name="user_search" placeholder="Search W3School" />
		<input type="submit" />
	</form>

在上面那个例子中，如果输入内容空且表格被提交，输入框将被高亮显示。

####10.Autofocus 属性 (Autofocus Attribute)

同样，HTML5的解决方案消除了对JavaScript的需要。如果一个特定的输入应该是“选择”或聚焦，默认情况下，我们现在可以利用自动聚焦属性。

	<input type="text" name="someInput" placeholder="Douglas Quaid" required autofocus>

autofocus 属性规定当页面加载时 input 元素应该自动获得焦点。
如果使用该属性，则 input 元素会获得焦点。

####11.Audio 支持 (Audio Support)

目前我们需要依靠第三方插件来渲染音频。然而在HTML5中，<audio>元素被引进来了。

	<audio src="/i/horse.ogg" controls="controls">
		Your browser does not support the audio element.
	</audio>

当使用<audio>元素时请记得包含两种音频格式。FireFox想要.ogg格式的文件，而Webkit浏览器则需要.mp3格式的。和往常一样，IE是不支持的，且Opera 10及以下版本只支持.wav格式。

####12.Video 支持 (Video Support)

HTML5中不仅有<audio>元素，而且还有<video>。然而，和<audio>类似，HTML5中并没有指定视频解码器，它留给了浏览器来决定。虽然Safari和Internet Explorer9可以支持H.264格式的视频，Firefox和Opera是坚持开源Theora 和Vorbis格式。因此，指定HTML5的视频时，你必须提供这两种格式。 

	<video controls preload>
		<source src="cohagenPhoneCall.ogv" type="video/ogg; codecs='vorbis, theora'" />
		<source src="cohagenPhoneCall.mp4" type="video/mp4; 'codecs='avc1.42E01E, mp4a.40.2'" />
		<p>
		 	Your browser is old. 
			<a href="cohagenPhoneCall.mp4">
				Download this video instead.
			</a>
		</p> 
	</video>

####13.视频预载 (Preload attribute in Videos element)

当用户访问页面时这一属性使得视频得以预载。为了实现这个功能，可以在<video>元素中加上preload="preload"或者只是preload。

	<video preload>

####14.显示控制条 (Display Controls)

如果你使用过上面的每一个提到的技术点，你可能已经注意到，使用上面的代码，视频仅仅显示的是张图片，没有控制条。为了渲染出播放控制条，我们必须在video元素内指定controls属性。 
 
	<video preload controls>

####15.正规表达式 (Regular Expressions)

在HTML4或XHTML中，你需要用一些正规表达式来验证特定的文本。而HTML5中新的pattern属性让我们能够在标签处直接插入一个正规表达式。

	<form action="" method="post"> 
		<label for="username">
			Create a Username: 
		</label>   
		<input type="text" name="username" id="username" placeholder="4 <> 10" pattern="[A-Za-z]{4,10}" autofocus required> 
		<button type="submit">
			Go 
		</button>
	</form>

###HTML5 新元素

	HTML5提供了新的元素来创建更好的页面结构：
	标签/描述
	<article>
	定义页面独立的内容区域。

	<aside>
	定义页面的侧边栏内容。

	<bdi>
	允许您设置一段文本，使其脱离其父元素的文本方向设置。

	<command>
	定义命令按钮，比如单选按钮、复选框或按钮

	<details>
	用于描述文档或文档某个部分的细节

	<dialog>
	定义对话框，比如提示框

	<summary>
	标签包含 details 元素的标题

	<figure>
	规定独立的流内容（图像、图表、照片、代码等等）。

	<figcaption>
	定义 <figure> 元素的标题

	<footer>
	定义 section 或 document 的页脚。

	<header>
	定义了文档的头部区域

	<mark>
	定义带有记号的文本。

	<meter>
	定义度量衡。仅用于已知最大和最小值的度量。

	<nav>
	定义导航链接的部分。

	<progress>
	定义任何类型的任务的进度。

	<ruby>
	定义 ruby 注释（中文注音或字符）。

	<rt>
	定义字符（中文注音或字符）的解释或发音。

	<rp>
	在 ruby 注释中使用，定义不支持 ruby 元素的浏览器所显示的内容。

	<section>
	定义文档中的节（section、区段）。

	<time>
	定义日期或时间。

	<wbr>
	规定在文本中的何处适合添加换行符。

	<canvas>
	html5 <canvas> 元素用于图形的绘制，通过脚本 (通常是JavaScript)来完成.

HTML5 语义元素

	 HTML5提供了新的语义元素来明确一个Web页面的不同部分:
	<header>
	<nav>
	<section>
	<article>
	<aside>
	<figcaption>
	<figure>
	<footer>

![](http://images2015.cnblogs.com/blog/801509/201607/801509-20160711082959467-525706727.png)

还有html5中拖放draggable属性、地理定位、Web 存储（sessionStorage、localStorage）等等


###CSS3新特性

CSS3选择器

	选择器					  示例					示例说明							  CSS
	.class					.intro				选择所有class="intro"的元素		 		1
	#id     				#firstname			选择所有id="firstname"的元素		 		1
	*							*				选择所有元素								2
	element						p				选择所有<p>元素							1
	element,element			div,p				选择所有<div>元素和<p>元素					1
	element element			div p				选择<div>元素内的所有<p>元素				1
	element>element			div>p				选择所有父级是 <div> 元素的 <p> 元素		2
	element+element			div+p				选择所有紧接着<div>元素之后的<p>元素		2
	[attribute]				[target]			选择所有带有target属性元素					2
	[attribute=value]		[target=-blank]		选择所有使用target="-blank"的元素			2
	[attribute~=value]		[title~=flower]		选择标题属性包含单词"flower"的所有元素		2
	[attribute|=language]	[lang|=en]			选择一个lang属性的起始值="EN"的所有元素		2
	:link					a:link				选择所有未访问链接							1
	:visited				a:visited			选择所有访问过的链接						1
	:active					a:active			选择活动链接								1
	:hover					a:hover				选择鼠标在链接上面时						1
	:focus					input:focus			选择具有焦点的输入元素						2
	:first-letter			p:first-letter		选择每一个<P>元素的第一个字母				1
	:first-line				p:first-line		选择每一个<P>元素的第一行					1
	:first-child			p:first-child		指定只有当<p>元素是其父级的第一个子级的样式。	2
	:before					p:before			在每个<p>元素之前插入内容					2
	:after					p:after				在每个<p>元素之后插入内容					2
	:lang(language)			p:lang(it)			选择一个lang属性的起始值="it"的所有<p>元素	2
	element1~element2		p~ul				选择p元素之后的每一个ul元素				3
	[attribute^=value]		a[src^="https"]		选择每一个src属性的值以"https"开头的元素	3
	[attribute$=value]		a[src$=".pdf"]		选择每一个src属性的值以".pdf"结尾的元素		3
	[attribute*=value]		a[src*="44lan"]		选择每一个src属性的值包含子字符串"44lan"的元素	3
	:first-of-type			p:first-of-type		选择每个p元素是其父级的第一个p元素			3
	:last-of-type			p:last-of-type		选择每个p元素是其父级的最后一个p元素			3
	:only-of-type			p:only-of-type		选择每个p元素是其父级的唯一p元素			3
	:only-child				p:only-child		选择每个p元素是其父级的唯一子元素			3
	:nth-child(n)			p:nth-child(2)		选择每个p元素是其父级的第二个子元素			3
	:nth-last-child(n)		p:nth-last-child(2)	选择每个p元素的是其父级的第二个子元素，从最后一个子项计数	3
	:nth-of-type(n)			p:nth-of-type(2)	选择每个p元素是其父级的第二个p元素			3
	:nth-last-of-type(n)	p:nth-last-of-type(2)	选择每个p元素的是其父级的第二个p元素，从最后一个子项计数	3
	:last-child				p:last-child		选择每个p元素是其父级的最后一个子级。		3
	:root					:root				选择文档的根元素							3
	:empty					p:empty				选择每个没有任何子级的p元素（包括文本节点）	3
	:target					#news:target		选择当前活动的#news元素（包含该锚名称的点击的URL）	3
	:enabled				input:enabled		选择每一个已启用的输入元素					3
	:disabled				input:disabled		选择每一个禁用的输入元素					3
	:checked				input:checked		选择每个选中的输入元素						3
	:not(selector)			:not(p)				选择每个并非p元素的元素					3
	::selection				::selection			匹配元素中被用户选中或处于高亮状态的部分		3
	:out-of-range			:out-of-range		匹配值在指定区间之外的input元素				3
	:in-range				:in-range			匹配值在指定区间之内的input元素				3
	:read-write				:read-write			用于匹配可读及可写的元素					3
	:read-only				:read-only			用于匹配设置 "readonly"（只读） 属性的元素	3
	:optional				:optional			用于匹配可选的输入元素						3
	:required				:required			用于匹配设置了 "required" 属性的元素		3
	:valid					:valid				用于匹配输入值为合法的元素					3
	:invalid				:invalid			用于匹配输入值为非法的元素


####CSS3 边框（Borders）

用CSS3，你可以创建圆角边框，添加阴影框，并作为边界的形象而不使用设计程序

	属性·············	说明	····································CSS
	border-image	设置所有边框图像的速记属性。					3
	border-radius	一个用于设置所有四个边框- *-半径属性的速记属性	3
	box-shadow		附加一个或多个下拉框的阴影							3

	div
	{
	  border:2px solid;
	  border-radius:25px;
	  box-shadow:10px10px5px#888888;
	  border-image:url(border.png)3030 round;
	}

####CSS3 背景

css3中包含几个新的背景属性，提供更大背景元素控制。

	顺序··················	描述	···············CSS
	background-clip		规定背景的绘制区域。			3
	background-origin	规定背景图片的定位区域。	    3
	background-size		规定背景图片的尺寸。			3

	div
	{
	  background:url(img_flwr.gif);
	  background-repeat:no-repeat;
	  background-size:100%100%;
	  background-origin:content-box;
	}

多背景

	body
	{
	  background-image:url(img_flwr.gif),url(img_tree.gif);
	}

####CSS3 渐变

CSS3 定义了两种类型的渐变（gradients）：

	线性渐变（Linear Gradients）- 向下/向上/向左/向右/对角方向
	 background: linear-gradient(direction, color-stop1, color-stop2,...);
	
	径向渐变（Radial Gradients）- 由它们的中心定义
	 background: radial-gradient(center, shape size, start-color,...,last-color);

####CSS3 文本效果

	 
	属性·····················	描述······································	CSS
	hanging-punctuation		规定标点字符是否位于线框之外。						3
	punctuation-trim		规定是否对标点字符进行修剪。						3
	text-align-last			设置如何对齐最后一行或紧挨着强制换行符之前的行。		3
	text-emphasis			向元素的文本应用重点标记以及重点标记的前景色。		3
	text-justify			规定当 text-align 设置为 "justify" 时所使用的对齐方法。	3
	text-outline			规定文本的轮廓。									3
	text-overflow			规定当文本溢出包含元素时发生的事情。					3
	text-shadow				向文本添加阴影。									3
	text-wrap				规定文本的换行规则。								3
	word-break				规定非中日韩文本的换行规则。						3
	word-wrap				允许对长的不可分割的单词进行分割并换行到下一行。		3

####CSS3 转换和变形

 
2D新转换属性

	以下列出了所有的转换属性:
	Property				描述					CSS
	transform			适用于2D或3D转换的元素		3
	transform-origin	允许您更改转化元素位置

2D 转换方法

	函数							描述
	matrix(n,n,n,n,n,n)		定义 2D 转换，使用六个值的矩阵。
	translate(x,y)			定义 2D 转换，沿着 X 和 Y 轴移动元素。
	translateX(n)			定义 2D 转换，沿着 X 轴移动元素。
	translateY(n)			定义 2D 转换，沿着 Y 轴移动元素。
	scale(x,y)				定义 2D 缩放转换，改变元素的宽度和高度。
	scaleX(n)				定义 2D 缩放转换，改变元素的宽度。
	scaleY(n)				定义 2D 缩放转换，改变元素的高度。
	rotate(angle)			定义 2D 旋转，在参数中规定角度。
	skew(x-angle,y-angle)	定义 2D 倾斜转换，沿着 X 和 Y 轴。
	skewX(angle)			定义 2D 倾斜转换，沿着 X 轴。
	skewY(angle)			定义 2D 倾斜转换，沿着 Y 轴。
 
3D转换属性

	下表列出了所有的转换属性：
	属性							描述									CSS
	transform				向元素应用 2D 或 3D 转换。					3
	transform-origin		允许你改变被转换元素的位置。					3
	transform-style			规定被嵌套元素如何在 3D 空间中显示。			3
	perspective				规定 3D 元素的透视效果。						3
	perspective-origin		规定 3D 元素的底部位置。						3
	backface-visibility		定义元素在不面对屏幕时是否可见。				3

3D 转换方法

	函数									描述
	matrix3d(n,n,n,n,n,n,
	n,n,n,n,n,n,n,n,n,n)		定义 3D 转换，使用 16 个值的 4x4 矩阵。
	translate3d(x,y,z)			定义 3D 转化。
	translateX(x)				定义 3D 转化，仅使用用于 X 轴的值。
	translateY(y)				定义 3D 转化，仅使用用于 Y 轴的值。
	translateZ(z)				定义 3D 转化，仅使用用于 Z 轴的值。
	scale3d(x,y,z)				定义 3D 缩放转换。
	scaleX(x)					定义 3D 缩放转换，通过给定一个 X 轴的值。
	scaleY(y)					定义 3D 缩放转换，通过给定一个 Y 轴的值。
	scaleZ(z)					定义 3D 缩放转换，通过给定一个 Z 轴的值。
	rotate3d(x,y,z,angle)		定义 3D 旋转。
	rotateX(angle)				定义沿 X 轴的 3D 旋转。
	rotateY(angle)				定义沿 Y 轴的 3D 旋转。
	rotateZ(angle)				定义沿 Z 轴的 3D 旋转。
	perspective(n)				定义 3D 转换元素的透视视图。

####CSS3 过渡

 
过渡属性

	下表列出了所有的过渡属性:
	属性									描述										CSS
	transition						简写属性，用于在一个属性中设置四个过渡属性。		3
	transition-property				规定应用过渡的 CSS 属性的名称。					3
	transition-duration				定义过渡效果花费的时间。默认是 0。				3
	transition-timing-function		规定过渡效果的时间曲线。默认是 "ease"。			3
	transition-delay				规定过渡效果何时开始。默认是 0。				3

	div
	{
	 transition-property: width;
	 transition-duration:1s;
	 transition-timing-function: linear;
	 transition-delay:2s;
	/* Safari */
	 -webkit-transition-property:width;
	 -webkit-transition-duration:1s;
	 -webkit-transition-timing-function:linear;
	 -webkit-transition-delay:2s;
	}


####CSS3 动画

要创建CSS3动画，你需要了解@keyframes规则。@keyframes规则是创建动画。 @keyframes规则内指定一个CSS样式和动画将逐步从目前的样式更改为新的样式。

<h1>实例</h1>
当动画为 25% 及 50% 时改变背景色，然后当动画 100% 完成时再次改变：

	@keyframes myfirst
	{
	 0%{background: red;}
	 25%{background: yellow;}
	 50%{background: blue;}
	 100%{background: green;}
	}

	下面的表格列出了 @keyframes 规则和所有动画属性：
	属性								描述												CSS
	@keyframes					规定动画。												3
	animation					所有动画属性的简写属性，除了 animation-play-state 属性。		3
	animation-name				规定 @keyframes 动画的名称。								3
	animation-duration			规定动画完成一个周期所花费的秒或毫秒。默认是 0。				3
	animation-timing-function	规定动画的速度曲线。默认是 "ease"。							3
	animation-delay				规定动画何时开始。默认是 0。								3
	animation-iteration-count	规定动画被播放的次数。默认是 1。							3
	animation-direction			规定动画是否在下一周期逆向地播放。默认是 "normal"。			3
	animation-play-state		规定动画是否正在运行或暂停。默认是 "running"。				3
	
 
	div
	{
	 animation-name: myfirst;
	 animation-duration:5s;
	 animation-timing-function: linear;
	 animation-delay:2s;
	 animation-iteration-count: infinite;
	 animation-direction: alternate;
	 animation-play-state: running;
	/* Safari and Chrome: */
	 -webkit-animation-name: myfirst;
	 -webkit-animation-duration:5s;
	 -webkit-animation-timing-function: linear;
	 -webkit-animation-delay:2s;
	 -webkit-animation-iteration-count: infinite;
	 -webkit-animation-direction: alternate;
	 -webkit-animation-play-state: running;
	}

####CSS3 盒模型

 在 CSS3 中, 增加了一些新的用户界面特性来调整元素尺寸，框尺寸和外边框，主要包括以下用户界面属性：


	resize：none | both | horizontal | vertical | inherit
	box-sizing: content-box | border-box | inherit
	outline:outline-color outline-style outline-width outine-offset

resize属性指定一个元素是否应该由用户去调整大小。

box-sizing 属性允许您以确切的方式定义适应某个区域的具体内容。

outline-offset 属性对轮廓进行偏移，并在超出边框边缘的位置绘制轮廓。


####CSS3伸缩布局盒模型(弹性盒)

CSS3 弹性盒（ Flexible Box 或 flexbox），是一种当页面需要适应不同的屏幕大小以及设备类型时确保元素拥有恰当的行为的布局方式。

引入弹性盒布局模型的目的是提供一种更加有效的方式来对一个容器中的子元素进行排列、对齐和分配空白空间。

	 下表列出了在弹性盒子中常用到的属性:
	属性						描述
	display				指定 HTML 元素盒子类型。
	flex-direction		指定了弹性容器中子元素的排列方式
	justify-content		设置弹性盒子元素在主轴（横轴）方向上的对齐方式。
	align-items			设置弹性盒子元素在侧轴（纵轴）方向上的对齐方式。
	flex-wrap			设置弹性盒子的子元素超出父容器时是否换行。
	align-content		修改 flex-wrap 属性的行为，类似 align-items, 但不是设置子元素对齐，而是设置行对齐
	flex-flow			flex-direction 和 flex-wrap 的简写
	order				设置弹性盒子的子元素排列顺序。
	align-self			在弹性子元素上使用。覆盖容器的 align-items 属性。
	flex				设置弹性盒子的子元素如何分配空间。

####CSS3 多媒体查询

从 CSS 版本 2 开始，就可以通过媒体类型在 CSS 中获得媒体支持。如果您曾经使用过打印样式表，那么您可能已经使用过媒体类型。清单 1 展示了一个示例。

	清单 1. 使用媒体类型
	<linkrel="stylesheet"type="text/css"href="site.css"media="screen"/>
	<linkrel="stylesheet"type="text/css"href="print.css"media="print"/>

	清单 2. 媒体查询规则
	@media all and(min-width:800px){...}
	@media all 是媒体类型，也就是说，将此 CSS 应用于所有媒体类型。
	(min-width:800px) 是包含媒体查询的表达式，如果浏览器的最小宽度为 800 像素，则会告诉浏览器只运用下列 CSS。

	清单 3. and 条件
	@media(min-width:800px)and(max-width:1200px)and(orientation:portrait){...}
	
	清单 4. or 关键词
	@media(min-width:800px)or(orientation:portrait){...}
	
	清单 5. 使用 not
	@media(not min-width:800px){...}
