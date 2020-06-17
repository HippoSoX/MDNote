# HTML

超文本标记语言（英语：HyperText Markup Language，简称：HTML）是一种用于创建网页的标准标记语言。

您可以使用 HTML 来建立自己的 WEB 站点，HTML 运行在浏览器上，由浏览器来解析。

在本教程中，您将学习如何使用 HTML 来创建站点。

HTML 很容易学习！相信您能很快学会它！

*注意：对于中文网页需要使用 \<meta charset="utf-8"> 声明编码，否则会出现乱码。有些浏览器(如 360 浏览器)会设置 GBK 为默认编码，则你需要设置为 \<meta charset="gbk">。*

## HTML的后缀名

.htm
.html

都行一样的

## HTML中包括特殊字符

|原义字符|等价字符引用|
|--|--|
|<|&lt;|
|>|&gt;|
|"|&quot;|
|'|&apos;|
|&|&amp;|

## 第一行

```html
<!DOCTYPE html>
```

它是 HTML5 标准网页声明，全称为 Document Type HyperText Mark-up Language，是一条标示语言。支持 HTML5 标准的主流浏览器都认识这个声明。表示网页采用 HTML5，<!DOCTYPE html> 声明位于文档中的最前面的位置，处于 \<html> 标签之前。此标签可告知浏览器文档使用哪种 HTML 或 XHTML 规范。
1. doctype 声明是不区分大小写的，用来告知 Web 浏览器页面使用了哪种 HTML 版本。

## 基础

```html
<h1>这是一个标题</h1>
<h2>这是两个标题</h2>
<h3>这是三个标题</h3>

<p>这是一个段落</p>
<p>尼个系第个段落</p>

<a href = "http://www.runoob.com">点我</a>

<img src = "images/katou_megumi.jpg" alt = "加藤惠" width = 1500 height = 3000>
```

其中标签\<a>中href是属性，\<img>中src，alt，width，height都是属性

>HTML 中的 href 和 src 有什么区别
>href 表示超文本引用（hypertext reference），在 link和a 等元素上使用。src 表示来源地址，在 img、script、iframe 等元素上。
>src 的内容，是页面必不可少的一部分，是引入。href 的内容，是与该页面有关联，是引用。区别就是，引入和引用。
>

这是一个实例：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>测试</title>
	</head>
	<body>
		<h1>圣人惠</h1>
		<p>hhh</p>
		<img src = "images/katou_megumi.jpg" alt = "加藤惠" width = 151.975 height = 214.875 />
	</body>
</html>
```

## HTML元素

**HTML文档由HTML元素定义。**

### HTML元素

|开始标签|元素内容|结束标签|
|--|--|--|
|\<p>|这是一个段落|\</p>|
|\<a href="hhh.html">|这是一个链接|\</a>|
|\<br>|换行||

### 语法

- HTML 元素以开始标签起始
- HTML 元素以结束标签终止
- 元素的内容是开始标签与结束标签之间的内容
- 某些 HTML 元素具有空内容（empty content）
- 空元素在开始标签中进行关闭（以开始标签的结束而结束）
- 大多数 HTML 元素可拥有属性

### 嵌套的 HTML 元素

HTML 文档由嵌套的 HTML 元素构成。

### 实例

```html
<!DOCTYPE html>
<html>

<body>
<p>第一段</p>
</body>

</html>
```

### 实例解析

\<p> 元素:

```html
<p>这是第一个段落。</p>
```
这个 \<p> 元素定义了 HTML 文档中的一个段落。
这个元素拥有一个开始标签 \<p> 以及一个结束标签\ </p>.
元素内容是: 这是第一个段落。

\<body> 元素:

```html
<body>
<p>这是第一个段落。</p>
</body>
```

\<body> 元素定义了 HTML 文档的主体。
这个元素拥有一个开始标签 \<body> 以及一个结束标签 \</body>。
元素内容是另一个 HTML 元素（p 元素）。

\<html> 元素：

```html
<html>

<body>
<p>这是第一个段落。</p>
</body>

</html>
```
\<html> 元素定义了整个 HTML 文档。
这个元素拥有一个开始标签\<html> ，以及一个结束标签\</html>.
元素内容是另一个 HTML 元素（body 元素）。

### 不要忘记结束标签

即使您忘记了使用结束标签，大多数浏览器也会正确地显示 HTML：

```html
<p>这是一个段落
<p>这是一个段落
```

以上实例在浏览器中也能正常显示，因为关闭标签是可选的。

但不要依赖这种做法。忘记使用结束标签会产生不可预料的结果或错误。

### HTML 空元素

没有内容的 HTML 元素被称为空元素。空元素是在开始标签中关闭的。

\<br> 就是没有关闭标签的空元素（\<br> 标签定义换行）。

在 XHTML、XML 以及未来版本的 HTML 中，所有元素都必须被关闭。

在开始标签中添加斜杠，比如\ <br />，是关闭空元素的正确方法，HTML、XHTML 和 XML 都接受这种方式。

即使\<br> 在所有浏览器中都是有效的，但使用\ <br /> 其实是更长远的保障。

### HTML 提示：使用小写标签

HTML 标签对大小写不敏感：\<P> 等同于 \<p>。许多网站都使用大写的 HTML 标签。

菜鸟教程使用的是小写标签，因为万维网联盟（W3C）在 HTML 4 中推荐使用小写，而在未来 (X)HTML 版本中强制使用小写。

### 为文档设定主语言

```html
<html lang="en-US">
```

使用"lang"属性。
主要用途是为了给搜索引擎提高效率。还可以通过这种方式将文档部分设置为不同的语言：

```html
<p>Japanese example: <span lang="jp">ご飯が熱い。</span>.</p>
```

## HTML属性

**属性是HTML元素提供的附加信息。**

### HTML 属性

+ HTML 元素可以设置属性
+ 属性可以在元素中添加附加信息
+ 属性一般描述于开始标签
+ 属性总是以名称/值对的形式出现，比如：name="value"。

### 属性实例
HTML 链接由 <a> 标签定义。链接的地址在 href 属性中指定：

```html
<a href = "http://www.runoob.com">点我</a>
<img src = "images/katou_megumi.jpg" alt = "加藤惠" width = 151.975 height = 214.875 />
```

### HTML 属性常用引用属性值

属性值应该始终被包括在引号内。

双引号是最常用的，不过使用单引号也没有问题。

Remark提示: 在某些个别的情况下，比如属性值本身就含有双引号，那么您必须使用单引号，例如：name='John "ShotGun" Nelson'

### HTML 提示：使用小写属性

属性和属性值对大小写不敏感。

不过，万维网联盟在其 HTML 4 推荐标准中推荐小写的属性/属性值。

而新版本的 (X)HTML 要求使用小写属性。

下面列出了适用于大多数 HTML 元素的属性：

|属性|描述|
|--|--|
|class|为html元素定义一个或多个类名（classname）(类名从样式文件引入)|
|id|定义元素的唯一id|
|style|规定元素的行内样式（inline style）|
|title|描述了元素的额外信息 (作为工具条使用)|

+ 属性和属性值，尽量小写，本来这样做也方便些。
+ class 属性可以多用 class=" " （引号里面可以填入多个class属性）
+ id 属性只能单独设置 id=" "（只能填写一个，多个无效）

## HTML标题

在 HTML 文档中，标题很重要。

### HTML标题

标题（Heading）是通过 \<h1> - \<h6> 标签进行定义的。
\<h1> 定义最大的标题。 \<h6> 定义最小的标题。
注释: 浏览器会自动地在标题的前后添加空行。

<h1>这是一个标题。</h1>
<h2>这是一个标题。</h2>
<h3>这是一个标题。</h3>

### 标题很重要

请确保将 HTML 标题 标签只用于标题。不要仅仅是为了生成粗体或大号的文本而使用标题。

搜索引擎使用标题为您的网页的结构和内容编制索引。

因为用户可以通过标题来快速浏览您的网页，所以用标题来呈现文档结构是很重要的。

应该将 h1 用作主标题（最重要的），其后是 h2（次重要的），再其次是 h3，以此类推。

### HTML 水平线

\<hr> 标签在 HTML 页面中创建水平线。

<hr>

hr 元素可用于分隔内容。

### HTML 注释

可以将注释插入 HTML 代码中，这样可以提高其可读性，使代码更易被人理解。浏览器会忽略注释，也不会显示它们。

注释: 开始括号之后（左边的括号）需要紧跟一个叹号，结束括号之前（右边的括号）不需要，合理地使用注释可以对未来的代码编辑工作产生帮助。

注释写法如下:

```html
<!-- 这是一个注释 -->
```

## HTML段落

HTML 可以将文档分割为若干段落。

### HTML 段落

段落是通过 <p> 标签定义的。
注意：浏览器会自动地在段落的前后添加空行。（</p> 是块级元素）

```html
<p>这是一个段落 </p>
<p>这是另一个段落</p>
```
### 不要忘记结束标签

即使忘了使用结束标签，大多数浏览器也会正确地将 HTML 显示出来：

```html
<p>这是一个段落
<p>这是一个段落
```

上面的例子在大多数浏览器中都没问题，但不要依赖这种做法。忘记使用结束标签会产生意想不到的结果和错误。

注释: 在未来的 HTML 版本中，不允许省略结束标签。

### HTML 折行

如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 \<br> 标签：

<p>这个<br>段落<br>演示了分行的效果</p>

\<br /> 元素是一个空的 HTML 元素。由于关闭标签没有任何意义，因此它没有结束标签。

### HTML 输出- 使用提醒

我们无法确定 HTML 被显示的确切效果。屏幕的大小，以及对窗口的调整都可能导致不同的结果。

对于 HTML，您无法通过在 HTML 代码中添加额外的空格或换行来改变输出的效果。

当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。

尝试一下

（这个例子演示了一些 HTML 格式化方面的问题）

### HTML 文本格式化

<b>加粗文本</b><br><br>
<i>斜体文本</i><br><br>
<code>电脑自动输出</code><br><br>
这是 <sub> 下标</sub> 和 <sup> 上标</sup>

### HTML 格式化标签

HTML 使用标签 \<b>("bold") 与 \<i>("italic") 对输出的文本进行格式, 如：粗体 or 斜体

这些HTML标签被称为格式化标签（请查看底部完整标签参考手册）。

>通常标签 \<strong> 替换加粗标签 \<b> 来使用, \<em> 替换 \<i>标签使用。
>然而，这些标签的含义是不同的：
>\<b> 与\<i> 定义粗体或斜体文本。
>\<strong> 或者 \<em>意味着你要呈现的文本是重要的，所以要突出显示。现今所有主要浏览器都能渲染各种效果的字体。不过，未来浏览器可能会支持更好的渲染效果。

### 示例一 文本格式化

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>菜鸟教程(runoob.com)</title>
	</head>
	<body>
		<b>这个文本是加粗的</b>
		<br />
		<strong>这个文本是加粗的</strong>
		<br />
		<big>这个文本字体放大</big>
		<br />
		<em>这个文本是斜体的</em>
		<br />
		<i>这个文本是斜体的</i>
		<br />
		<small>这个文本是缩小的</small>
		<br />
		这个文本包含
		<sub>下标</sub>
		<br />
		这个文本包含
		<sup>上标</sup>
	</body>
</html>

### 示例2 预格式文本

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<pre>
此例演示如何使用 pre 标签
对空行和    空格
进行控制
		</pre>
	</body>
</html>

### 示例3 “计算机输出”标签

<!DOCTYPE html> 
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<code>计算机输出</code>
		<br />
		<kbd>键盘输入</kbd>
		<br />
		<tt>打字机文本</tt>
		<br />
		<samp>计算机代码样本</samp>
		<br />
		<var>计算机变量</var>
		<br />
		<p>
			<b>注释：</b>这些标签常用于显示计算机/编程代码。
		</p>
	</body>
</html>

### 示例4 地址

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<address>
			Written by <a href="mailto:webmaster@example.com">Jon Doe</a>.<br> 
			Visit us at:<br>
			Example.com<br>
			Box 564, Disneyland<br>
			USA
		</address>
	</body>
</html>

### 示例5 缩写和首字母缩写

<!DOCTYPE html> 
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<abbr title="etcetera">etc.</abbr>
		<br />
		<acronym title="World Wide Web">WWW</acronym>
		<p>在某些浏览器中，当您把鼠标移至缩略词语上时，title 可用于展示表达的完整版本。</p>
		<p>仅对于 IE 5 中的 acronym 元素有效。</p>
		<p>对于 Netscape 6.2 中的 abbr 和 acronym 元素都有效。</p>
		</body>
</html>

### 示例6 文字方向

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head> 
	<body>
		<p>该段落文字从左到右显示。</p>  
		<p><bdo dir="rtl">该段落文字从右到左显示。</bdo></p>  
	</body>
</html>

### 示例7 块引用

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>WWF's goal is to: 
		<q>Build a future where people live in harmony with nature.</q>
		We hope they succeed.</p>
        <!显示效果上仅仅多了一对双引号，唔知有咩用>
	</body>
</html>

### 示例8 删除子效果和插入字效果

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
		</body>
</html>

### HTML文本格式化标签

|标签|描述|
|--|--|
|\<b>|定义粗体文本|
|\<em>|定义着重文字|
|\<i>|定义斜体字|
|\<small>|定义小号字|
|\<strong>|定义加重语气|
|\<sub>|定义下标字|
|\<sup>|定义上标字|
|\<ins>|定义插入字|
|\<del>|定义删除字|

### HTML“计算机输出标签”

|标签|描述|
|--|--|
|\<code>|定义计算机代码|
|\<kbd>|定义键盘码|
|\<samp>|定义计算机代码样本|
|\<var>|定义变量|
|\<pre>|定义预格式文本|

### HTML引文、引用及标签定义

|标签|描述|
|--|--|
|\<abbr>|定义缩写|
|\<address>|定义地址|
|\<bdo>|定义文字方向|
|\<blockquote>|定义长的引用|
|\<q>|定义短的引用语|
|\<cite>|定义引用、引证|
|\<dfn>|定义一个定义项目|

## HTML链接

HTML 使用超级链接与网络上的另一个文档相连。几乎可以在所有的网页中找到链接。点击链接可以从一张页面跳转到另一张页面。

### 示例

<!DOCTYPE html>
<html>
	<head> 
			<meta charset="utf-8"> 
			<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>
		<a href="/index.html">本文本</a> 是一个指向本网站中的一个页面的链接。</p>
		<p><a href="//www.microsoft.com/">本文本</a> 是一个指向万维网上的页面的链接。</p>
	</body>
</html>

### HTML 超链接（链接）

HTML使用标签 <a>来设置超文本链接。

超链接可以是一个字，一个词，或者一组词，也可以是一幅图像，您可以点击这些内容来跳转到新的文档或者当前文档中的某个部分。

当您把鼠标指针移动到网页中的某个链接上时，箭头会变为一只小手。

在标签<a> 中使用了href属性来描述链接的地址。

默认情况下，链接将以以下形式出现在浏览器中：

一个未访问过的链接显示为蓝色字体并带有下划线。
访问过的链接显示为紫色并带有下划线。
点击链接时，链接显示为红色并带有下划线。
注意：如果为这些超链接设置了 CSS 样式，展示样式会根据 CSS 的设定而显示。

### HTML 链接语法

链接的 HTML 代码很简单。它类似这样：

<a href="url">链接文本</a>

href 属性描述了链接的目标。

提示: "链接文本" 不必一定是文本。图片或其他 HTML 元素都可以成为链接。

### HTML 链接 - target 属性
使用 target 属性，你可以定义被链接的文档在何处显示。

下面的这行会在新窗口打开文档：

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<a href="https://www.runoob.com/" target="_blank">访问菜鸟教程!</a>
		<p>如果你将 target 属性设置为 &quot;_blank&quot;, 链接将在新窗口打开。</p>
	</body>
</html>

### HTML 链接- id 属性

id属性可用于创建在一个HTML文档书签标记。

提示: 书签是不以任何特殊的方式显示，在HTML文档中是不显示的，所以对于读者来说是隐藏的。

实例：在HTML文档中插入ID:
<a id="tips">有用的提示部分</a>

在HTML文档中创建一个链接到"有用的提示部分(id="tips"）"：
<a href="#tips">访问有用的提示部分</a>

或者，从另一个页面创建一个链接到"有用的提示部分(id="tips"）"：
<a href="https://www.runoob.com/html/html-links.html#tips">
访问有用的提示部分</a>

注释： 请始终将正斜杠添加到子文件夹。假如这样书写链接：href="https://www.runoob.com/html"，就会向服务器产生两次 HTTP 请求。这是因为服务器会添加正斜杠到这个地址，然后创建一个新的请求，就像这样：href="https://www.runoob.com/html/"。

### 示例一 图片链接

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>创建图片链接:
		<a href="//www.runoob.com/html/html-tutorial.html">
		<img  border="10" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>
		<p>无边框的图片链接:
		<a href="//www.runoob.com/html/html-tutorial.html">
		<img border="0" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>
	</body>
</html>

### 示例二 在当前页面链接到指定位置

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>菜鸟教程(runoob.com)</title>
	</head>
	<body>
		<p>
		<a href="#C4">查看章节 4</a>
		</p>
		<h2>章节 1</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 2</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 3</h2>
		<p>这边显示该章节的内容……</p>
		<h2><a id="C4">章节 4</a></h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 5</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 6</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 7</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 8</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 9</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 10</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 11</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 12</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 13</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 14</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 15</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 16</h2>
		<p>这边显示该章节的内容……</p>
		<h2>章节 17</h2>
		<p>这边显示该章节的内容……</p
	</body>
</html>

### 示例3 跳出框架

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>跳出框架?</p> 
		<a href="//www.runoob.com/" target="_top">点击这里!</a> 
	</body>
</html>

### 示例4 创建电子邮件链接

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>
		这是一个电子邮件链接：
		<a href="mailto:someone@example.com?Subject=Hello%20again" target="_top">
		发送邮件</a>
		</p>
		<p>
		<b>注意:</b> 单词之间空格使用 %20 代替，以确保浏览器可以正常显示文本。
		</p>
	</body>
</html>

### 示例5 创建电子邮件链接2

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>
		这是另一个电子邮件链接：
		<a href="mailto:someone@example.com?cc=someoneelse@example.com&bcc=andsomeoneelse@example.com&subject=Summer%20Party&body=You%20are%20invited%20to%20a%20big%20summer%20party!" target="_top">发送邮件!</a>
		</p>
		<p>
		<b>注意:</b> 单词之间的空格使用 %20 代替，以确保浏览器可以正常显示文本。
		</p>
	</body>
</html>

### 属性：nofollow

nofollow 是 HTML 页面中 a 标签的属性值。这个标签的意义是告诉搜索引擎"不要追踪此网页上的链接或不要追踪此特定链接"。

nofollow 是 HTML 页面中 a 标签的属性值。它的出现为网站管理员提供了一种方式，即告诉搜索引擎"不要追踪此网页上的链接"或"不要追踪此特定链接"。这个标签的意义是告诉搜索引擎这个链接不是经过作者信任的，所以这个链接不是一个信任票。

### 属性：rel

<a href="http://www.runoob.com/" target="_blank" rel="noopener noreferrer">访问菜鸟教程!</a> 
后面最好加上：
`rel="noopener noreferrer"`
意思是不会打开其他的网站，因为恶意病毒可能会修改你的浏览器空白页地址。

## HTML\<head>

\<title> - 定义了HTML文档的标题
使用 \<title> 标签定义HTML文档的标题

\<base> - 定义了所有链接的URL
使用 \<base> 定义页面中所有链接默认的链接目标地址。

\<meta> - 提供了HTML文档的meta标记
使用 \<meta> 元素来描述HTML文档的描述，关键词，作者，字符集等。

### HTML\<head> 元素

\<head> 元素包含了所有的头部标签元素。在 \<head>元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。

可以添加在头部区域的元素标签为: \<title>, \<style>, \<meta>, \<link>, \<script>, \<noscript> 和 \<base>。

### HTML\<title> 元素

\<title> 标签定义了不同文档的标题。

\<title> 在 HTML/XHTML 文档中是必须的。

\<title> 元素:

+ 定义了浏览器工具栏的标题
+ 当网页添加到收藏夹时，显示在收藏夹中的标题
+ 显示在搜索引擎结果页面的标题
```html
<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>文档标题</title>
	</head>
	<body>
		文档内容......
	</body>
</html>
```
HTML\<title>元素不仅可以显示文本，也可以在左侧显示logo等图片。

显示时，要将\<link>标签放入\<head>里。

举例：
```html
<!doctype HTML>
	<html>
		<head>
		<link rel="shortcut icon" href="图片url">
		<title>这是一个带图片的标签</title>
	</head>
	<body>
    ……
    ……
    ……
	</body>
</html>
```
### HTML\<base> 元素

\<base> 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接:

```html
<head>
<base href="http://www.runoob.com/images/" target="_blank">
</head>
```

### HTML\<link> 元素
\<link> 标签定义了文档与外部资源之间的关系。

\<link> 标签通常用于链接到样式表:

```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

更为常用的用法是将\<link>标签放入\<head>里，用来显示网页图标（图标现在也支持.gif或.png格式，但为了在老古董浏览器中正常显示，最好用.ico）。

举例：
```html
<!doctype HTML>
	<html>
		<head>
		<link rel="shortcut icon" href="图片url">
		<title>这是一个带图片的标签</title>
	</head>
	<body>
    ……
    ……
    ……
	</body>
</html>
```

### HTML\<meta> 元素

meta标签描述了一些基本的元数据。

\<meta> 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。

META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。

元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。

\<meta> 一般放置于 \<head> 区域

**\<meta> 标签- 使用实例：**


```html
<! name是元素类型，content指定了元数据的内容 >
为搜索引擎定义关键词:
<meta name="keywords" content="HTML, CSS, XML, XHTML, JavaScript">

为网页定义描述内容:
<meta name="description" content="免费 Web & 编程 教程">
<! description会显示在搜索引擎的结果上 >

定义网页作者:
<meta name="author" content="Runoob">

每30秒钟刷新当前页面:
<meta http-equiv="refresh" content="30">
```

### HTML\<script> 元素
\<script>标签用于加载脚本文件，如： JavaScript。

\<script> 元素在以后的章节中会详细描述。

### HTML head 元素

|标签|描述|
|--|--|
|\<head>|定义了文档的信|
|\<title>|定义了文档的标题|
|\<base>|定义了页面链接标签的默认链接地址|
|\<link>|定义了一个文档和外部资源之间的关系|
|\<meta>|定义了HTML文档中的元数据|
|\<script>|定义了客户端的脚本文件|
|\<style>|定义了HTML文档的样式文件|


### head 标签和 header 标签的不同

head 标签用于定义文档头部，它是所有头部元素的容器。\<head> 中的元素可以引用脚本、指示浏览器在哪里找到样式表、提供元信息等等。
如：

```html
<html>
  <head>
     <title>文档标题</title>
  </head>
</html>
```

header 标签用于定义文档的页眉（介绍信息）。
如：

```html
<html>
  <body>
    <header>
        <p>段落</p>
        <h1>一级标题</h1>
    </header>
  </body>
</html>
```

**注意千万不要弄混。**

## HTML样式- CSS

CSS (Cascading Style Sheets) 用于渲染HTML元素标签的样式。

一个示例：

<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>
<div style="opacity:0.5;position:absolute;left:50px;width:300px;height:150px;background-color:#40B3DF"></div>
<div style="font-family:verdana;padding:20px;border-radius:10px;border:10px solid #EE872A;">
<div style="opacity:0.3;position:absolute;left:120px;width:100px;height:200px;background-color:#8AC007"></div>
<h3>Look! Styles and colors</h3>
<div style="letter-spacing:12px;">Manipulate Text</div>
<div style="color:#40B3DF;">Colors
<span style="background-color:#B4009E;color:#ffffff;">Boxes</span>
</div>
<div style="color:#000000;">and more...</div>
</div>
</body>
</html>

说明：
1. \<div>元素将被单独分割，作为一个块元素。
2. 在HTML元素中可以使用“style”属性来使用CSS
3. \<span>标签相当于给行内的一部分独立出来给予某些属性，本身没有语义。

|属性|描述|
|--|--|
|background-color|背景颜色|
|font-family|字体|
|color|颜色|
|font-size|字体大小|
|text-align|文字对齐（取代了旧的\<center>）|

### 如何使用CSS

1. 内联样式——在HTML元素中使用"style"属性
2. 内部样式表——在HTML文档头部\<head>区域使用\<style>元素来包含CSS
3. 外部引用——使用外部CSS文件（优选），使用\<link包含进来>

```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

|标签|描述|
|--|--|
|\<style>|定义文本样式|
|\<link>|定义资源引用地址|

### 已弃用的标签和属性

在HTML 4, 原来支持定义HTML元素样式的标签和属性已被弃用。这些标签将不支持新版本的HTML标签。

不建议使用的标签有: \<font>, \<center>, \<strike>

不建议使用的属性: color 和 bgcolor.

### 父子标签样式

CSS修饰标签的样式，有 "内联" 和 "外引" 两种方式。

对于大部分标签，以上两种方法均可，且修改父级标签，子级标签特性也会改变。但某些标签确无法通过修改父级标签来改变子级标签特性，如a标签，修改其颜色特性，必须直接修改 a 标签的特性才可。

实例：

```html
<a href="#" style="color:red;" rel="nofollow">只能使用"内联"方式</a>
```

## HTML图像

HTML 图像- 图像标签（ \<img>）和源属性（Src）
在 HTML 中，图像由\<img> 标签定义。

\<img> 是空标签，意思是说，它只包含属性，并且没有闭合标签。

要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。

定义图像的语法是：

```
<img src="url" alt="some_text">
```

URL 指存储图像的位置。如果名为 "pulpit.jpg" 的图像位于 www.runoob.com 的 images 目录中，那么其 URL 为 http://www.runoob.com/images/pulpit.jpg。

浏览器将图像显示在文档中图像标签出现的地方。如果你将图像标签置于两个段落之间，那么浏览器会首先显示第一个段落，然后显示图片，最后显示第二段。

### HTML 图像- Alt属性

alt 属性用来为图像定义一串预备的可替换的文本。

替换文本属性的值是用户定义的。
```
<img src="boat.gif" alt="Big Boat">
```
在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。此时，浏览器将显示这个替代性的文本而不是图像。为页面上的图像都加上替换文本属性是个好习惯，这样有助于更好的显示信息，并且对于那些使用纯文本浏览器的人来说是非常有用的。

### HTML 图像- 设置图像的高度与宽度

height（高度） 与 width（宽度）属性用于设置图像的高度与宽度。

属性值默认单位为像素:

```
<img src="pulpit.jpg" alt="Pulpit rock" width="304" height="228">
```

提示: 指定图像的高度和宽度是一个很好的习惯。如果图像指定了高度宽度，页面加载时就会保留指定的尺寸。如果没有指定图片的大小，加载页面时有可能会破坏HTML页面的整体布局。

### 示例一：浮动图片

本例演示如何使图片浮动至段落的左边或右边。

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>
		<img src="smiley.gif" alt="Smiley face" style="float:left" width="32" height="32"> 一个带图片的段落，图片浮动在这个文本的左边。
		</p>
		<p>
		<img src="smiley.gif" alt="Smiley face" style="float:right" width="32" height="32"> 一个带图片的段落，图片浮动在这个文本的右边。
		</p>
		<p><b>注意:</b> 在这里我们使用了 CSS "float" 属性，在HTML 4中 align 属性已废弃，HTML5 已不支持该属性，可以使用 CSS 代替。</p>
	</body>
</html>
### 示例二：图片链接

本例演示如何将图像作为一个链接使用。

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>创建图片链接:
		<a href="//www.runoob.com/html/html-tutorial.html">
		<img  border="10" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>
		<p>无边框的图片链接:
		<a href="//www.runoob.com/html/html-tutorial.html">
		<img border="0" src="smiley.gif" alt="HTML 教程" width="32" height="32"></a></p>
	</body>
</html>
### 示例三：创建图像映射

本例显示如何创建带有可供点击区域的图像地图。其中的每个区域都是一个超级链接。

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>菜鸟教程(runoob.com)</title>
	</head>
	<body>
		<p>点击太阳或其他行星，注意变化：</p>
		<img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">
		<map name="planetmap">
			<area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
			<area shape="circle" coords="90,58,3" alt="Mercury" href="mercur.htm">
			<area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
		</map>
	</body>
</html>

该段代码中的shape指的是点击区域的形状，coords指的应该是链接区域在图片中的坐标（像素为单位）

1、矩形：(左上角顶点坐标为(x1,y1)，右下角顶点坐标为(x2,y2))
<area shape="rect" coords="x1,y1,x2,y2" href=url>
2、圆形：(圆心坐标为(X1,y1)，半径为r)
<area shape="circle" coords="x1,y1,r" href=url>
3、多边形：(各顶点坐标依次为(x1,y1)、(x2,y2)、(x3,y3) ......)
<area shape="poly" coords="x1,y1,x2,y2 ......" href=url>

## HTML表格

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>
		每个表格从一个 table 标签开始。 
		每个表格行从 tr 标签开始。
		每个表格的数据从 td 标签开始。
		</p>
		<h4>一列:</h4>
		<table border="1">
		<tr>
			<td>100</td>
		</tr>
		</table>
		<h4>一行三列:</h4>
		<table border="1">
		<tr>
			<td>100</td>
			<td>200</td>
			<td>300</td>
		</tr>
		</table>
		<h4>两行三列:</h4>
		<table border="1">
		<tr>
			<td>100</td>
			<td>200</td>
			<td>300</td>
		</tr>
		<tr>
			<td>400</td>
			<td>500</td>
			<td>600</td>
		</tr>
		</table>
	</body>
</html>

### HTML 表格

表格由 \<table> 标签来定义。每个表格均有若干行（由 \<tr> 标签定义），每行被分割为若干单元格（由 \<td> 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。

表格实例

<table border="1">
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>

### HTML 表格和边框属性

如果不定义边框属性，表格将不显示边框。有时这很有用，但是大多数时候，我们希望显示边框。

使用边框属性来显示一个带有边框的表格：

<table border="1">
    <tr>
        <td>Row 1, cell 1</td>
        <td>Row 1, cell 2</td>
    </tr>
</table>

### HTML 表格表头

表格的表头使用 \<th> 标签进行定义。

大多数浏览器会把表头显示为粗体居中的文本：

实例
<table border="1">
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>
### 示例一：带有标题的表格

本例演示一个带标题 (caption) 的表格

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<table border="1">
			<caption>Monthly savings</caption>
		<tr>
			<th>Month</th>
			<th>Savings</th>
		</tr>
		<tr>
			<td>January</td>
			<td>$100</td>
		</tr>
		<tr>
			<td>February</td>
			<td>$50</td>
		</tr>
		</table>
	</body>
</html>

### 示例二：跨行或跨列的表格单元格

本例演示如何定义跨行或跨列的表格单元格。（rowspan和colspan属性）

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<h4>单元格跨两列:</h4>
		<table border="1">
		<tr>
			<th>Name</th>
			<th colspan="2">Telephone</th>
		</tr>
		<tr>
			<td>Bill Gates</td>
			<td>555 77 854</td>
			<td>555 77 855</td>
		</tr>
		</table>
		<h4>单元格跨两行:</h4>
		<table border="1">
		<tr>
			<th>First Name:</th>
			<td>Bill Gates</td>
		</tr>
		<tr>
			<th rowspan="2">Telephone:</th>
			<td>555 77 854</td>
		</tr>
		<tr>
			<td>555 77 855</td>
		</tr>
		</table>
	</body>
</html>

### 示例三：表格内的标签

本例演示如何显示在不同的元素内显示元素。

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<table border="1">
		<tr>
			<td>
				<p>这是一个段落</p>
				<p>这是另一个段落</p>
			</td>
			<td>这个单元格包含一个表格:
				<table border="1">
				<tr>
					<td>A</td>
					<td>B</td>
				</tr>
				<tr>
					<td>C</td>
					<td>D</td>
				</tr>
				</table>
			</td>
		</tr>
		<tr>
			<td>这个单元格包含一个列表
				<ul>
					<li>apples</li>
					<li>bananas</li>
					<li>pineapples</li>
				</ul>
			</td>
			<td>HELLO</td>
		</tr>
		</table>
	</body>
</html>

### 示例四：单元格边距(Cell padding)

本例演示如何使用 Cell padding 来创建单元格内容与其边框之间的空白

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<h4>没有单元格边距:</h4>
		<table border="1">
		<tr>
  			<td>First</td>
  			<td>Row</td>
		</tr>   
		<tr>
  			<td>Second</td>
  			<td>Row</td>
		</tr>
		</table>
		<h4>有单元格边距:</h4>
		<table border="1" cellpadding="10">
		<tr>
  			<td>First</td>
  			<td>Row</td>
		</tr>   
		<tr>
 			 <td>Second</td>
 			 <td>Row</td>
		</tr>
		</table>
	</body>
</html>

### 示例五：单元格间距(Cell spacing)

本例演示如何使用 Cell spacing 增加单元格之间的距离。

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<h4>没有单元格间距:</h4>
		<table border="1">
		<tr>
  			<td>First</td>
  			<td>Row</td>
		</tr>
		<tr>
 		 <td>Second</td>
 		 <td>Row</td>
		</tr>
		</table>
		<h4>单元格间距="0":</h4>
		<table border="1" cellspacing="0">
		<tr>
  			<td>First</td>
  			<td>Row</td>
		</tr>
		<tr>
 			 <td>Second</td>
 			 <td>Row</td>
		</tr>
		</table>
		<h4>单元格间距="10":</h4>
		<table border="1" cellspacing="10">
		<tr>
  			<td>First</td>
  			<td>Row</td>
		</tr>
		<tr>
  			<td>Second</td>
  			<td>Row</td>
		</tr>
		</table>
	</body>
</html>

### HTML 表格标签

| 标签 | 描述 |
| :-- | :-- |
| \<table> | 定义表格 |
| \<th> | 定义表格的表头 |
| \<tr> | 定义表格的行 |
| \<td> | 定义表格单元 |
| \<caption> | 定义表格标题 |
| \<colgroup> | 定义表格列的组 |
| \<col> | 定义用于表格列的属性 |
| \<thread> | 定义表格的页眉 |
| \<tbody> | 定义表格的主体 |
| \<tfoot> | 定义表格的页脚 |

### 常用属性

跨列：colspan
跨行：rowspan
单元格内边距：cellpadding
单元格外边距：cellspacing
col 和 colgroup 用于便捷定义表格指定列的样式。

### 表格三要素 table、tr、td 常用属性

表格三要素 table、tr、td 缺一不可。

\<table> 标签常用属性：

border="1"   表格边框的宽度
bordercolor="#fff"   表格边框的颜色
cellspacing="5"   单元格之间的间距
width="500"   表格的总宽度
height="100"   表格的总高度
align="right"   表格整体对齐方式    (参数有  left、center、right)
bgcolor="#fff"   表格整体的背景色

\<tr> 标签的常用属性:

bgcolor="#fff"    行的颜色
align="right"    行内文字的水平对齐方式    (参数有left、center、right)
valign="top"     行内文字的垂直对齐方式    (参数有top、middle、bottom)

\<td>、\<th> 标签的常用属性:

width="500"    单元格的宽度，设置后对当前一列的单元格都有影响
height="100"   单元格的高度，设置后对当前一行的单元格都有影响
bgcolor="fff"  单元格的背景色
align="right"  单元格文字的水平对齐方式    (参数left、center、right)
rowspan="3"    合并垂直水平方向的单元格
colspan="3"    合并水平方向单元格
valign="top"   单元格文字的垂直对齐方式    (参数middle、bottom、top) 

**引号里的数字和颜色代码均可以更改。**

## HTML列表

### HTML无序列表

无序列表是一个项目的列表，此列项目使用粗体圆点（典型的小黑圆圈）进行标记。

无序列表使用 \<ul> 标签

<ul>
<li>Coffee</li>
<li>Milk</li>
</ul>

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head> 
	<body>
	<h4>无序列表:</h4>
	<ul>
  		<li>Coffee</li>
      	<li>Tea</li>
  		<li>Milk</li>
	</ul>
	</body>
</html>

### HTML 有序列表

同样，有序列表也是一列项目，列表项目使用数字进行标记。 有序列表始于 \<ol> 标签。每个列表项始于\<li> 标签。

列表项使用数字来标记。

<ol>
<li>Coffee</li>
<li>Milk</li>
</ol>

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<h4>有序列表:</h4>
	<ol>
  		<li>Coffee</li>
  		<li>Tea</li>
  		<li>Milk</li>
	</ol>
	<ol start="50">
  		<li>Coffee</li>
 		 <li>Tea</li>
 		 <li>Milk</li>
	</ol>
	</body>
</html>

### HTML 自定义列表

自定义列表不仅仅是一列项目，而是项目及其注释的组合。

自定义列表以 \<dl> 标签开始。每个自定义列表项以 \<dt> 开始。每个自定义列表项的定义以 \<dd> 开始。

<dl>
<dt>Coffee</dt>
<dd>- black hot drink</dd>
<dt>Milk</dt>
<dd>- white cold drink</dd>
</dl>

### 注意事项 - 有用提示

提示: 列表项内部可以使用段落、换行符、图片、链接以及其他列表等等

### 示例一：不同类型的有序列表

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<h4>编号列表：</h4>
	<ol>
 		<li>Apples</li>
		 <li>Bananas</li>
		 <li>Lemons</li>
		 <li>Oranges</li>
	</ol>  
	<h4>大写字母列表：</h4>
	<ol type="A">
		 <li>Apples</li>
		 <li>Bananas</li>
		 <li>Lemons</li>
		 <li>Oranges</li>
	</ol>  
	<h4>小写字母列表：</h4>
	<ol type="a">
		 <li>Apples</li>
		 <li>Bananas</li>
		 <li>Lemons</li>
		 <li>Oranges</li>
	</ol>  
	<h4>罗马数字列表：</h4>
	<ol type="I">
		 <li>Apples</li>
         <li>Bananas</li>
		 <li>Lemons</li>
 		<li>Oranges</li>
	</ol>  
	<h4>小写罗马数字列表：</h4>
	<ol type="i">
         <li>Apples</li>
 		<li>Bananas</li>
		 <li>Lemons</li>
		 <li>Oranges</li>
	</ol>  
	</body>
</html>

### 示例二：不同类型的无序列表

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<p><b>注意：</b> 在 HTML 4中 ul 属性已废弃，HTML5 已不支持该属性，因此我们使用 CSS 代替来定义不同类型的无序列表如下：</p>
	<h4>圆点列表：</h4>
	<ul style="list-style-type:disc">
		<li>Apples</li>
		<li>Bananas</li>
		<li>Lemons</li>
		<li>Oranges</li>
	</ul> 
	<h4>圆圈列表：</h4>
	<ul style="list-style-type:circle">
 		<li>Apples</li>
 		<li>Bananas</li>
 		<li>Lemons</li>
		 <li>Oranges</li>
	</ul>
	<h4>正方形列表：</h4>
	<ul style="list-style-type:square">
 		<li>Apples</li>
 		<li>Bananas</li>
 		<li>Lemons</li>
 		<li>Oranges</li>
	</ul>
	</body>
</html>

### 示例三：嵌套列表

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<h4>嵌套列表：</h4>
	<ul>
		<li>Coffee</li>
		<li>Tea
		<ul>
			<li>Black tea</li>
			<li>Green tea
			<ul>
				<li>China</li>
				<li>Africa</li>
			</ul>
			</li>
		</ul>
		</li>
		<li>Milk</li>
	</ul>
	</body>
</html>

### HTML 列表标签

|标签|描述|
|:--|--|
|\<ol>|定义有序列表|
|\<ul>|定义无序列表|
|\<li>|定义列表项|
|\<dl>|定义列表|
|\<dt>|自定义列表项目|
|\<dd>|定义自定列表项的描述|

## HTML \<div> 和 \<span>

HTML 可以通过\<div> 和\<span>将元素组合起来。

### HTML 区块元素

大多数 HTML 元素被定义为块级元素或内联元素。

块级元素在浏览器显示时，通常会以新行来开始（和结束）。

实例: \<h1>, \<p>, \<ul>, \<table>

### HTML 内联元素

内联元素在显示时通常不会以新行开始。

实例: \<b>, \<td>, \<a>, \<img>

### HTML \<div> 元素

HTML \<div> 元素是块级元素，它可用于组合其他 HTML 元素的容器。

\<div> 元素没有特定的含义。除此之外，由于它属于块级元素，浏览器会在其前后显示折行。

如果与 CSS 一同使用，\<div> 元素可用于对大的内容块设置样式属性。

\<div> 元素的另一个常见的用途是文档布局。它取代了使用表格定义布局的老式方法。使用 \<table> 元素进行文档布局不是表格的正确用法。\<table> 元素的作用是显示表格化的数据。

### HTML \<span> 元素

HTML \<span> 元素是内联元素，可用作文本的容器

\<span> 元素也没有特定的含义。

当与 CSS 一同使用时，\<span> 元素可用于为部分文本设置样式属性。

### HTML 分组标签

|标签|描述|
|:--|:--|
|\<div>|定义了文档的区域，块级 (block-level)|
|\<span>|用来组合文档中的行内元素，内联元素(inline)|

## HTML布局

网页布局对改善网站的外观非常重要。

请慎重设计您的网页布局。

### 网站布局

大多数网站会把内容安排到多个列中（就像杂志或报纸那样）。

大多数网站可以使用 \<div> 或者 \<table> 元素来创建多列。CSS 用于对元素进行定位，或者为页面创建背景以及色彩丰富的外观。

**虽然我们可以使用HTML table标签来设计出漂亮的布局，但是table标签是不建议作为布局工具使用的 - 表格不是布局工具。**

### 示例一：用\<div>布局

div 元素是用于分组 HTML 元素的块级元素。

下面的例子使用五个 div 元素来创建多列布局

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<div id="container" style="width:500px">
	<div id="header" style="background-color:#FFA500;">
	<h1 style="margin-bottom:0;">主要的网页标题</h1></div>
	<div id="menu" style="background-color:#FFD700;height:200px;width:100px;float:left;">
	<b>菜单</b><br>
	HTML<br>
	CSS<br>
	JavaScript</div>
	<div id="content" style="background-color:#EEEEEE;height:200px;width:400px;float:left;">
	内容在这里</div>
	<div id="footer" style="background-color:#FFA500;clear:both;text-align:center;">
版权 © runoob.com</div>
	</div>
	</body>
</html>

### 示例二： 使用表格

使用 HTML \<table> 标签是创建布局的一种简单的方式。

大多数站点可以使用 \<div> 或者 \<table> 元素来创建多列。CSS 用于对元素进行定位，或者为页面创建背景以及色彩丰富的外观。

**即使可以使用 HTML 表格来创建漂亮的布局，但设计表格的目的是呈现表格化数据 - 表格不是布局工具！**

下面的例子使用三行两列的表格 - 第一和最后一行使用 colspan 属性来横跨两列：

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<table width="500" border="0">
	<tr>
		<td colspan="2" style="background-color:#FFA500;">
		<h1>主要的网页标题</h1>
	</td>
	</tr>
	<tr>
		<td style="background-color:#FFD700;width:100px;">
		<b>菜单</b><br>
		HTML<br>
		CSS<br>
		JavaScript
		</td>
		<td style="background-color:#eeeeee;height:200px;width:400px;">
		内容在这里</td>
	</tr>
	<tr>
		<td colspan="2" style="background-color:#FFA500;text-align:center;">
版权 © runoob.com</td>
	</tr>
	</table>
	</body>
</html>

### HTML 布局 - 有用的提示

Tip: 使用 CSS 最大的好处是，如果把 CSS 代码存放到外部样式表中，那么站点会更易于维护。通过编辑单一的文件，就可以改变所有页面的布局。如需学习更多有关 CSS 的知识，请访问我们的CSS 教程。

Tip: 由于创建高级的布局非常耗时，使用模板是一个快速的选项。通过搜索引擎可以找到很多免费的网站模板（您可以使用这些预先构建好的网站布局，并优化它们）。

### HTML 布局标签

|标签|描述|
|\<div>|定义文档区块，块级(block-level)|
|\<span>|定义 span，用来组合文档中的行内元素。|

### tips

在 css 里面定义：

```css
p {margin:0; padding:0}
```

即可，用全局样式把 p 的边距给归零。

不过这样的副作用是网页所有的 p 都被重置了，所以你也可以指定专门标签下的 p。例如，如果这个 p 是在一个 class 为 content 的 div 下的，想去掉它的边距，就这么定义：

```css
.content p {margin:0; padding:0;}
```

## HTML表单和输入

HTML 表单用于收集不同类型的用户输入。

### HTML 表单

表单是一个包含表单元素的区域。

表单元素是允许用户在表单中输入内容,比如：文本域(textarea)、下拉列表、单选框(radio-buttons)、复选框(checkboxes)等等。

表单使用表单标签 \<form> 来设置:

<form>
.
input 元素
.
</form>

### HTML 表单 - 输入元素

多数情况下被用到的表单标签是输入标签（<input>）。

输入类型是由类型属性（type）定义的。大多数经常被用到的输入类型如下：

### 文本域（Text Fields）

文本域通过\<input type="text"> 标签来设定，当用户要在表单中键入字母、数字等内容时，就会用到文本域。

<form>
First name: <input type="text" name="firstname"><br>
Last name: <input type="text" name="lastname">
</form>

**注意**:表单本身并不可见。同时，在大多数浏览器中，文本域的默认宽度是 20 个字符

### 密码字段

密码字段通过标签\<input type="password"> 来定义:

<form>
Password: <input type="password" name="pwd">
</form>
**注意**:密码字段字符不会明文显示，而是以星号或圆点替代。

### 单选按钮（Radio Buttons）

\<input type="radio"> 标签定义了表单单选框选项

<form>
<input type="radio" name="sex" value="male">Male<br>
<input type="radio" name="sex" value="female">Female
</form>

### 复选框（Checkboxes）

<input type="checkbox"> 定义了复选框. 用户需要从若干给定的选择中选取一个或若干选项。

<form>
<input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
<input type="checkbox" name="vehicle" value="Car">I have a car
</form>

### 提交按钮(Submit Button)

\<input type="submit"> 定义了提交按钮.

当用户单击确认按钮时，表单的内容会被传送到另一个文件。表单的动作属性定义了目的文件的文件名。由动作属性定义的这个文件通常会对接收到的输入数据进行相关的处理。:

<form name="input" action="html_form_action.php" method="get">
Username: <input type="text" name="user">
<input type="submit" value="Submit">
</form>

### 示例：下拉列表

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="">
	<select name="cars">
	<option value="volvo">Volvo</option>
	<option value="saab">Saab</option>
	<option value="fiat">Fiat</option>
	<option value="audi">Audi</option>
	</select>
	</form>
	</body>
</html>

带有预选值的

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="">
	<select name="cars">
	<option value="volvo">Volvo</option>
	<option value="saab">Saab</option>
	<option value="fiat" selected>Fiat</option>
	<option value="audi">Audi</option>
	</select>
	</form>
	</body>
</html>

### 示例：文本域（Textarea）

本例演示如何创建文本域（多行文本输入控件）。用户可在文本域中写入文本。可写入字符的字数不受限制。

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<textarea rows="10" cols="30">
我是一个文本框。
	</textarea>
	</body>
</html>

### 示例：按钮（button）

本例演示如何创建按钮。你可以对按钮上的文字进行自定义。

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="">
	<input type="button" value="Hello world!">
	</form>
	</body>
</html>

### 表单示例一：带边框的表单

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="">
	<fieldset>
	<legend>Personal information:</legend>
	Name: <input type="text" size="30"><br>
	E-mail: <input type="text" size="30"><br>
	Date of birth: <input type="text" size="10">
	</fieldset>
	</form>
</body>
</html>

### 表单示例二：带有输入框和确认按钮的表单

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="demo-form.php">
	First name: <input type="text" name="FirstName" value="Mickey"><br>
	Last name: <input type="text" name="LastName" value="Mouse"><br>
	<input type="submit" value="提交">
	</form>
	<p>点击"提交"按钮，表单数据将被发送到服务器上的“demo-form.php”。</p>
	</body>
</html>

### 表单示例三：带有复选框的表单

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="demo-form.php" method="get">
		<input type="checkbox" name="vehicle[]" value="Bike"> I have a bike<br>
		<input type="checkbox" name="vehicle[]" value="Car" checked="checked"> I have a car<br>
		<input type="submit" value="提交">
	</form>
	</body>
</html>

### 表单示例四：带有单选按钮的表单

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<form action="demo-form.php" method="get">
		<input type="radio" name="sex" value="Male"> Male<br>
		<input type="radio" name="sex" value="Female" checked="checked"> Female<br>
		<input type="submit" value="提交">
	</form>
	</body>
</html>

### 表单示例五：从表单发送电子邮件

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
	<h3>发送邮件到 someone@example.com:</h3>
	<form action="MAILTO:someone@example.com" method="post" enctype="text/plain">
		Name:<br>
		<input type="text" name="name" value="your name"><br>
		E-mail:<br>
		<input type="text" name="mail" value="your email"><br>
		Comment:<br>
		<input type="text" name="comment" value="your comment" size="50"><br><br>
		<input type="submit" value="发送">
		<input type="reset" value="重置">
	</form>
	</body>
</html>

### HTML 表单标签

New : HTML5新标签

|标签|描述|
|:--|--|
|\<form>|定义供用户输入的表单|
|\<input>|定义输入域|
|\<textarea>|定义文本域(一个多行的输入控件)|
|\<label>|定义了\<input> 元素的标签，一般为输入标题|
|\<fieldset>|定义了一组相关的表单元素，并使用外框包含起来|
|\<legend>|定义了\<fieldset> 元素的标题|
|\<select>|定义了下拉选项列表|
|\<optgroup>|定义选项组|
|\<option>|定义下拉列表中的选项|
|\<button>|定义一个点击按钮|
|\<datalist>New|指定一个预先定义的输入控件选项列表|
|\<keygen>New<br>(该标签在新的 Web 标准中已废弃)|定义了表单的密钥对生成器字段|
|\<output>New|定义一个计算结果|

### 重置按钮reset button

\<input type="reset">定义重置按钮

<form>
<input type="reset" name="button" id="button" value="重置">
</form>

点击之后会将重置按钮所在的表单中填写的内容重新设置为默认值。

### 表单属性

表单中的单选按钮可以设置以下几个属性：value、name、checked

- value：提交数据到服务器的值（后台程序PHP使用）
- name：为控件命名，以备后台程序 ASP、PHP 使用
- checked：当设置 checked="checked" 时，该选项被默认选中

<form>
<p>你生活在哪个国家？</p>
<input type="radio" name="country" value="China" checked="checked">中国<br />
<input type="radio" name="country" value="the USA">美国
</form>

注意：同一组的单选按钮，name 取值一定要一致，比如上面例子为同一个名称“country”，这样同一组的单选按钮才可以起到单选的作用。

## HTML框架

通过使用框架，你可以在同一个浏览器窗口中显示不止一个页面。

### \<iframe>

iframe语法:

<iframe src="URL"></iframe>

该URL指向不同的网页。

### Iframe - 设置高度与宽度

height 和 width 属性用来定义iframe标签的高度与宽度。

属性默认以像素为单位, 但是你可以指定其按比例显示 (如："80%")。

<iframe src="https://www.runoob.com/" width="200" height="200"></iframe>

### Iframe - 移除边框

frameborder 属性用于定义iframe表示是否显示边框。

设置属性值为 "0" 移除iframe的边框:

<iframe src="https://www.runoob.com/" frameborder="0"></iframe>

### 使用iframe来显示目标链接页面

iframe可以显示一个目标链接的页面

目标链接的属性必须使用iframe的属性，如下实例:

<iframe src="https://www.runoob.com/" name="iframe_a"></iframe>
<p><a href="https://www.runoob.com/" target="iframe_a">RUNOOB.COM</a></p>

### HTML iframe 标签

|标签|说明|
|--|--|
|\<iframe>|定义一个内联的ifram|

## HTML颜色

HTML 颜色由红色、绿色、蓝色混合而成。

### 颜色值

HTML 颜色由一个十六进制符号来定义，这个符号由红色、绿色和蓝色的值组成（RGB）。

每种颜色的最小值是0（十六进制：#00）。最大值是255（十六进制：#FF）。

这个表格给出了由三种颜色混合而成的具体效果：

详情点下列链接看：

[HTML颜色](https://www.runoob.com/html/html-colors.html)

[HTML颜色名](https://www.runoob.com/html/html-colornames.html)

[HTML颜色值](https://www.runoob.com/html/html-colorvalues.html)

## HTML脚本

JavaScript 使 HTML 页面具有更强的动态和交互性。

### HTML\<script> 标签

\<script> 标签用于定义客户端脚本，比如 JavaScript。

\<script> 元素既可包含脚本语句，也可通过 src 属性指向外部脚本文件。

JavaScript 最常用于图片操作、表单验证以及内容动态更新。

### HTML\<noscript> 标签

\<noscript> 标签提供无法使用脚本时的替代内容，比方在浏览器禁用脚本时，或浏览器不支持客户端脚本时。

\<noscript>元素可包含普通 HTML 页面的 body 元素中能够找到的所有元素。

只有在浏览器不支持脚本或者禁用脚本时，才会显示 \<noscript> 元素中的内容：

### 示例一：将脚本插入HTML文档

如何将脚本插入 HTML 文档。

```html
<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<script>
		document.write("Hello World!")
		</script> 
	</body>
</html>
```
### 示例二：使用\<noscripts>

如何应对不支持脚本或禁用脚本的浏览器。

```html
<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head> 
	<body>
		<script>
		document.write("Hello World!")
		</script>
		<noscript>抱歉，你的浏览器不支持 JavaScript!</noscript>
		<p>不支持 JavaScript 的浏览器会使用 &lt;noscript&gt; 元素中定义的内容（文本）来替代。</p>
	</body>
</html>
```
更多内容请看Javascript教程

### HTML脚本标签

|标签|描述|
|--|--|
|\<script>|定义了客户端脚本|
|\<noscript>|定义了不支持脚本浏览器输出的文本|

## HTMLURL

URL 是一个网页地址。

URL可以由字母组成，如"runoob.com"，或互联网协议（IP）地址： 192.68.20.50。大多数人进入网站使用网站域名来访问，因为 名字比数字更容易记住。

### URL - 统一资源定位器

Web浏览器通过URL从Web服务器请求页面。

当您点击 HTML 页面中的某个链接时，对应的 \<a> 标签指向万维网上的一个地址。

一个统一资源定位器(URL) 用于定位万维网上的文档。

一个网页地址实例: http://www.runoob.com/html/html-tutorial.html 语法规则:

**scheme://host.domain:port/path/filename**

说明:

- scheme - 定义因特网服务的类型。最常见的类型是 http
- host - 定义域主机（http 的默认主机是 www）
- domain - 定义因特网域名，比如 runoob.com
- :port - 定义主机上的端口号（http 的默认端口号是 80）
- path - 定义服务器上的路径（如果省略，则文档必须位于网站的根目录中）。
- filename - 定义文档/资源的名称

### 常见的 URL Scheme

以下是一些URL scheme：

|Scheme|访问|用于...|
|--|--|--|
|http|超文本传输协议|以 http:// 开头的普通网页。不加密。|
|https|安全超文本传输协议|安全网页，加密所有信息交换。|
|ftp|文件传输协议|用于将文件下载或上传至网站。|
|file||您计算机上的文件。|

### URL 字符编码

URL 只能使用 ASCII 字符集.

来通过因特网进行发送。由于 URL 常常会包含 ASCII 集合之外的字符，URL 必须转换为有效的 ASCII 格式。

URL 编码使用 "%" 其后跟随两位的十六进制数来替换非 ASCII 字符。

URL 不能包含空格。URL 编码通常使用 + 来替换空格。

### HTML 速查列表

HTML 速查列表. 你可以打印它，以备日常使用。

https://www.runoob.com/html/html-quicklist.html

