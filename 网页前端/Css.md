# CSS

通过使用 CSS 我们可以大大提升网页开发的工作效率！

在我们的 CSS 教程中，您会学到如何使用 CSS 同时控制多重网页的样式和布局。

## CSS 简介

### 什么是 CSS?

- CSS 指层叠样式表 (Cascading Style Sheets)
- 样式定义如何显示 HTML 元素
- 样式通常存储在样式表中
- 把样式添加到 HTML 4.0 中，是为了解决内容与表现分离的问题
- 外部样式表可以极大提高工作效率
- 外部样式表通常存储在 CSS 文件中
- 多个样式定义可层叠为一个

### 示例

```css
body
{
font-size:75%;
font-family:verdana,arial,'sans serif';
background-color:#FFFFF0;
color:#000080;
margin:10px;
}

h1 {font-size:200%;}
h2 {font-size:140%;}
h3 {font-size:110%;}

th {background-color:#ADD8E6;}

ul {list-style:circle;}
ol {list-style:upper-roman;}

a:link {color:#000080;}
a:hover {color:red;}
```

### 样式解决了一个很大的问题

HTML 标签原本被设计为用于定义文档内容，如下实例：

<h1>这是一个标题</h1>
<p>这是一个段落。</p>

样式表定义如何显示 HTML 元素，就像 HTML 中的字体标签和颜色属性所起的作用那样。样式通常保存在外部的 .css 文件中。我们只需要编辑一个简单的 CSS 文档就可以改变所有页面的布局和外观。

## CSS 语法

### CSS 语法规则

CSS 规则由两个主要的部分构成：选择器，以及一条或多条声明:

```css
h1 {color:bule;font-size:12px;}
```

选择器通常是您需要改变样式的 HTML 元素。

每条声明由一个属性和一个值组成。

属性（property）是您希望设置的样式属性（style attribute）。每个属性有一个值。属性和值被冒号分开。

### CSS 实例

CSS声明总是以分号(;)结束，声明总以大括号({})括起来:

```css
p {color:red;text-align:center;}
```

为了让CSS可读性更强，你可以每行只描述一个属性:

```css
p
{
color:red;
text-align:center;
}
```
### CSS 注释

注释是用来解释你的代码，并且可以随意编辑它，浏览器会忽略它。

CSS注释以 "/*" 开始, 以 "*/" 结束, 实例如下:

```css
/*这是个注释*/
p
{
text-align:center;
/*这是另一个注释*/
color:black;
font-family:arial;
}
```

## CSS Id 和 Class

### id 和 class 选择器

如果你要在HTML元素中设置CSS样式，你需要在元素中设置"id" 和 "class"选择器。

### id 选择器

id 选择器可以为标有特定 id 的 HTML 元素指定特定的样式。

HTML元素以id属性来设置id选择器,CSS 中 id 选择器以 "#" 来定义。

以下的样式规则应用于元素属性 id="para1":

```css
#para1
{
    text-align:center;
    color:red;
}
```

**ID属性不要以数字开头，数字开头的ID在 Mozilla/Firefox 浏览器中不起作用。**

### class 选择器

class 选择器用于描述一组元素的样式，class 选择器有别于id选择器，class可以在多个元素中使用。

class 选择器在HTML中以class属性表示, 在 CSS 中，类选择器以一个点"."号显示：

在以下的例子中，所有拥有 center 类的 HTML 元素均为居中。

```css
.center {text-align:center;}
```

你也可以指定特定的HTML元素使用class。

在以下实例中, 所有的 p 元素使用 class="center" 让该元素的文本居中:

```css
p.center {text-align:center;}
```

**类名的第一个字符不能使用数字！它无法在 Mozilla 或 Firefox 中起作用。**

### css 选择器

如果你要在 html 标签中设置 CSS 样式，那么你有四种方法，即 css 选择器有四种。

除了提到的 id 和 class 选择器外，第三种选择器为标签选择器，即以 html 标签作为 css 修饰所用的选择器。

实例

```html
<style>
h3{
    color:red;
}
</style>
<h3>菜鸟教程</h3>
```

第四种选择器即直接在标签内部写css代码。

实例

```html
<h3 style="color:red;">菜鸟教程</h3>
```

这四种 css 选择器有修饰上的优先级，即：

**style属性 > id > class > 标签**
**(内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式**

### 各种选择器示例

除了教程中的id选择器和class选择器，另还有元素选择器、属性选择器、包含选择器、子选择器和CSS3中新增的兄弟选择器，以下带上ID选择器和类选择器一起举例。

1. **ID 选择器（ID selector，IS）**：使用 # 标识selector，语法格式：#S{...}（S为选择器名）。例：id为name的标签会匹配下面的样式
```html
<style>
#name{
  color:red;
}
</style>
<!--下面文字是红色的-->
<p id="name">red text</p>
```

2. **类选择器（class selector，CS）**：使用 . 标识selector，语法格式：.S{...}（S为选择器名）。例：class属性值为value的标签会匹配下面的样式
```html
<style>
.value{
  text-align:center;
}
</style>
<!--下面的文字是居中对齐的-->
<p class="value">center text</p>
```

3. **元素选择器（element selector，ES）**：又叫标签选择器，使用标签名作为selector名，语法格式：S{...}（S为选择器名）。例：所有的p标签都会匹配以下的样式
```html
<style>
p{
  font-style:italic;
}
</style>
<!--下面的文字是斜体的-->
<p style="font-style:italic">italic text</p>
```

4. **属性选择器（attribute selector，AS）**：ES其实是AS的一个特例，在AS基础上还能对selector描述得更具体，语法格式为 E[attr[~=][|=][^=][$=][*=]VALUE]{...}，是并没有得到所有浏览器支持的选择器，因此不举例

5. **包含选择器（package selector，PS）**：指定目标选择器必须处在某个选择器对应的元素内部，语法格式：A B{...}（A、B为HTML元素/标签，表示对处于A中的B标签有效）。例：以下div内的p标签和div外的p标签分别匹配不同的样式
```html
<style>
p{
  color:red;
}
div p{
  color:yellow;
}
</style>
<p>red text</p><!--文字是红色的-->
<div>
  <p>yellow text</p><!--文字是黄色的-->
</div>
```

补充包含选择器：

包含选择器除了有 A B{...} 的形式外（A和B都是标签），还可以有这种形式：.A B{...} 的形式（A是类名，B是标签）。

作用与上面介绍的相同，会使 class 名为 A 的标签里面所有名为 B 的子代标签的内容按照设定的内容显示。
```html
<style>
.first span{
  color:red;
}
</style>
<body>
<p class="first"><span>内容为红色</span>
<ol>
  <li><span>内容也是红色</span></li>
  <li><span>内容也是红色</span></li>
</ol></p>
</body>
```

6. **子选择器（sub-selector，SS）**：类似于PS，指定目标选择器必须处在某个选择器对应的元素内部，两者区别在于PS允许"子标签"甚至"孙子标签"及嵌套更深的标签匹配相应的样式，而SS强制指定目标选择器作为 包含选择器对应的标签 内部的标签，语法格式：A>B{...}（A、B为HTML元素/标签）。例：以下div内的p标签匹配样式，div内的table内的p不匹配
```html
<style>
div>p{
  color:red;
}
</style>
<div>
  <p>red text</p><!--文字是红色的-->
  <table>
    <tr>
      <td>
        <p>no red text;</p><!--文字是非红色的-->
      </td>
    </tr>
  </table>
</div>
```

补充子选择器

子选择器除了有 A >B{...} 的形式外（A和B都是标签），还可以有这种形式：.A >B{...} 的形式（A是类名，B是标签）。

作用与上面介绍的相同，会使 class 为 A 的标签里面所有名为 B 的直接子代标签的内容按照设定的内容显示。而非直接子代的 B 标签的内容是不会改变的。
```html
<style>
.first>span{
  color:red;
}
</style>
<body>
<p class="first"><span>内容为红色</span>
<ol>
  <li><span>内容不是红色</span></li>
  <li><span>内容不是红色</span></li>
</ol></p>
</body>
```

7. **兄弟选择器（brother selector，BS）**：BS是CSS3.0新增的一个选择器，语法格式：A~B{...}（A、B为HTML元素/标签，表示A标签匹配selector的A，B标签匹配selector的B时，B标签匹配样式）
```html
<style>
div~p{
  color:red;
}
</style>
<div>
  <p>no red text</p><!--文字是非红色的-->
  <div>no red text</div>
  <p>red text</p><!--文字是红色的-->
</div>
```

8. **通用选择器**
语法形式为：\*{属性：属性值}。它的作用是匹配 html 中的所有元素标签。
```html
<!--使用html中任意标签元素字体颜色全部设置为红色：-->
<style>
*{color:red;}
</style>

<body>
<h1>标题为红色</h1>
<p>段落也为红色</p>
</body>
```

9. 相邻选择器

语法形式为：
```css
A+B{
    声明1; 
    声明;
    ...
}
```

实例:
```html
<!--相邻选择器选择每个div紧邻后的一个元素p-->
<style>
   div+p{
     color: red;
   }
</style>
<div>
   <p>not red text</p>
   <p>not red text</p>
</div>
<p>red text</p>
<p>not red text</p>
```

## CSS 创建

当读到一个样式表时，浏览器会根据它来格式化 HTML 文档。

### 如何插入样式表

插入样式表的方法有三种:

- 外部样式表(External style sheet)
- 内部样式表(Internal style sheet)
- 内联样式(Inline style)

### 外部样式表

当样式需要应用于很多页面时，外部样式表将是理想的选择。在使用外部样式表的情况下，你可以通过改变一个文件来改变整个站点的外观。每个页面使用 \<link> 标签链接到样式表。 \<link> 标签在（文档的）头部：

```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

浏览器会从文件 mystyle.css 中读到样式声明，并根据它来格式文档。

外部样式表可以在任何文本编辑器中进行编辑。文件不能包含任何的 html 标签。样式表应该以 .css 扩展名进行保存。下面是一个样式表文件的例子：

```css
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("/images/back40.gif");}
```

*不要在属性值与单位之间留有空格（如："margin-left: 20 px" ），正确的写法是 "margin-left: 20px" 。*

### 内部样式表

当单个文档需要特殊的样式时，就应该使用内部样式表。你可以使用 \<style> 标签在文档头部定义内部样式表，就像这样:
```html
<head>
<style>
hr {color:sienna;}
p {margin-left:20px;}
body {background-image:url("images/back40.gif");}
</style>
</head>
```

### 内联样式

由于要将表现和内容混杂在一起，内联样式会损失掉样式表的许多优势。请慎用这种方法，例如当样式仅需要在一个元素上应用一次时。

要使用内联样式，你需要在相关的标签内使用样式（style）属性。Style 属性可以包含任何 CSS 属性。本例展示如何改变段落的颜色和左外边距：
```html
<p style="color:sienna;margin-left:20px">这是一个段落。</p>
```

### 多重样式

如果某些属性在不同的样式表中被同样的选择器定义，那么属性值将从更具体的样式表中被继承过来。 

例如，外部样式表拥有针对 h3 选择器的三个属性：
```css
h3
{
    color:red;
    text-align:left;
    font-size:8pt;
}
```
而内部样式表拥有针对 h3 选择器的两个属性：
```css
h3
{
    text-align:right;
    font-size:20pt;
}
```
假如拥有内部样式表的这个页面同时与外部样式表链接，那么 h3 得到的样式是：
```css
color:red;
text-align:right;
font-size:20pt;
```
即颜色属性将被继承于外部样式表，而文字排列（text-alignment）和字体尺寸（font-size）会被内部样式表中的规则取代。

### 多重样式优先级

样式表允许以多种方式规定样式信息。样式可以规定在单个的 HTML 元素中，在 HTML 页的头元素中，或在一个外部的 CSS 文件中。甚至可以在同一个 HTML 文档内部引用多个外部样式表。

一般情况下，优先级如下：

**(内联样式）Inline style > （内部样式）Internal style sheet >（外部样式）External style sheet > 浏览器默认样式**
```html
<head>
    <!-- 外部样式 style.css -->
    <link rel="stylesheet" type="text/css" href="style.css"/>
    <!-- 设置：h3{color:blue;} -->
    <style type="text/css">
      /* 内部样式 */
      h3{color:green;}
    </style>
</head>
<body>
    <h3>测试！</h3>
</body>
```

*如果外部样式放在内部样式的后面，则外部样式将覆盖内部样式。*

## CSS 背景

CSS 背景属性用于定义HTML元素的背景。

CSS 属性定义背景效果:

- background-color
- background-image
- background-repeat
- background-attachment
- background-position

### background-color 背景颜色

background-color 属性定义了元素的背景颜色.

页面的背景颜色使用在body的选择器中:
```css
body {background-color:#b0c4de;}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-color_body)

CSS中，颜色值通常以以下方式定义:

+ 十六进制 - 如："#ff0000"
+ RGB - 如："rgb(255,0,0)"
+ 颜色名称 - 如："red"

以下实例中, h1, p, 和 div 元素拥有不同的背景颜色:
```css
h1 {background-color:#6495ed;}
p {background-color:#e0ffff;}
div {background-color:#b0c4de;}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-color_elements)

### background-image 背景图像

background-image 属性描述了元素的背景图像.

默认情况下，背景图像进行平铺重复显示，以覆盖整个元素实体.

页面背景图片设置实例:
```css
body {background-image:url('paper.gif');}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-image)

下面是一个例子是一个糟糕的文字和背景图像组合。文本可读性差:
```css
body {background-image:url('bgdesert.jpg');}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-image_bad)

### background-repeat 背景图像 - 水平或垂直平铺

默认情况下 background-image 属性会在页面的水平或者垂直方向平铺。

一些图像如果在水平方向与垂直方向平铺，这样看起来很不协调，如下所示: 
```css
body
{
background-image:url('gradient2.png');
}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-image_gradient1)

如果图像只在水平方向平铺 (repeat-x), 页面背景会更好些:
```css
body
{
background-image:url('gradient2.png');
background-repeat:repeat-x;
}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-image_gradient2)

### background-repeat / background-position 背景图像- 设置定位与不平铺

让背景图像不影响文本的排版

如果你不想让图像平铺，你可以使用 background-repeat 属性:

实例
```css
body
{
background-image:url('img_tree.png');
background-repeat:no-repeat;
}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-image_norepeat)

以上实例中，背景图像与文本显示在同一个位置，为了让页面排版更加合理，不影响文本的阅读，我们可以改变图像的位置。

可以利用 background-position 属性改变图像在背景中的位置:
以上实例中，背景图像与文本显示在同一个位置，为了让页面排版更加合理，不影响文本的阅读，我们可以改变图像的位置。

可以利用 background-position 属性改变图像在背景中的位置:
```css
body
{
background-image:url('img_tree.png');
background-repeat:no-repeat;
background-position:right top;
}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_background-image_position)

### background 背景- 简写属性

在以上实例中我们可以看到页面的背景颜色通过了很多的属性来控制。

为了简化这些属性的代码，我们可以将这些属性合并在同一个属性中.

背景颜色的简写属性为 "background":
```css
body {background:#ffffff url('img_tree.png') no-repeat right top;}
```

当使用简写属性时，属性值的顺序为：:
```
background-color
background-image
background-repeat
background-attachment
background-position
```

以上属性无需全部使用，你可以按照页面的实际需要使用。

### 示例：固定背景

如何设置固定的背景图像

本例演示如何设置固定的背景图像。图像不会随着页面的其他部分滚动。

[示例](https://www.runoob.com/try/try.php?filename=trycss_background-attachment)

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title>
		<style>
			body 
			{
				background-image:url('smiley.gif');
				background-repeat:no-repeat;
				background-attachment:fixed;
			}
		</style>
	</head>
	<body>
		<p>背景图片是固定的。尝试向下滚动页面。</p>
		<p>背景图片是固定的。尝试向下滚动页面。</p>
		<p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
        <p>背景图片是固定的。尝试向下滚动页面。</p>
	</body>
</html>
```

### CSS 背景属性

|Property|描述|
|--|--|
|background|简写属性，作用是将背景属性设置在一个声明中。|
|background-attachment|背景图像是否固定或者随着页面的其余部分滚动。|
|background-color|设置元素的背景颜色。|
|background-image|把图像设置为背景。|
|background-position|设置背景图像的起始位置。|
|background-repeat|设置背景图像是否及如何重复。|

## CSS 文本格式

### color 文本颜色

颜色属性被用来设置文字的颜色。

颜色是通过CSS最经常的指定：

- 十六进制值 - 如: ＃FF0000
- 一个RGB值 - 如: RGB(255,0,0)
- 颜色的名称 - 如: red

参阅 CSS 颜色值 查看完整的颜色值。

一个网页的背景颜色是指在主体内的选择：
```css
body {color:red;}
h1 {color:#00ff00;}
h2 {color:rgb(255,0,0);}
```

对于W3C标准的CSS：如果你定义了颜色属性，你还必须定义背景色属性。

### text-align 文本的对齐方式

文本排列属性是用来设置文本的水平对齐方式。

文本可居中或对齐到左或右,两端对齐.

当text-align设置为"justify"，每一行被展开为宽度相等，左，右外边距是对齐（如杂志和报纸）。
```css
h1 {text-align:center;}
p.date {text-align:right;}
p.main {text-align:justify;}
```

### text-decoration 文本修饰

text-decoration 属性用来设置或删除文本的装饰。

从设计的角度看 text-decoration属性主要是用来删除链接的下划线：
```css
a {text-decoration:none;}
```

也可以这样装饰文字：
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			h1 {text-decoration:overline;}
			h2 {text-decoration:line-through;}
			h3 {text-decoration:underline;}
		</style>
	</head>
	<body>
		<h1>This is heading 1</h1>
		<h2>This is heading 2</h2>
		<h3>This is heading 3</h3>
	</body>
</html>
```

*我们不建议强调指出不是链接的文本，因为这常常混淆用户。*

### text-transform 文本转换

文本转换属性是用来指定在一个文本中的大写和小写字母。

可用于所有字句变成大写或小写字母，或每个单词的首字母大写。
```css
p.uppercase {text-transform:uppercase;}
p.lowercase {text-transform:lowercase;}
p.capitalize {text-transform:capitalize;}
```

### text-indent 文本缩进

文本缩进属性是用来指定文本的第一行的缩进。
```css
p {text-indent:50px;}
```

### 示例一：letter-spacing 指定字符之间的空间

这个例子演示了如何增加或减少字符之间的空间。
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>菜鸟教程</title>
		<style>
			h1 {letter-spacing:2px;}
			h2 {letter-spacing:-3px;}
		</style>
	</head>
	<body>
		<h1>This is heading 1</h1>
		<h2>This is heading 2</h2>
	</body>
</html>
```

### 示例二：line-height 指定行与行之间的空间

这个例子演示了如何指定在一个段落中行之间的空间

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			p.small {line-height:70%;}
			p.big {line-height:200%;}
		</style>
	</head>
	<body>
		<p>
			这是一个标准行高的段落。<br>
			这是一个标准行高的段落。<br>
			大多数浏览器的默认行高约为110%至120%。<br>
		</p>
		<p class="small">
			这是一个更小行高的段落。<br>
			这是一个更小行高的段落。<br>
			这是一个更小行高的段落。<br>
			这是一个更小行高的段落。<br>
		</p>
		<p class="big">
			这是一个更大行高的段落。<br>
			这是一个更大行高的段落。<br>
			这是一个更大行高的段落。<br>
			这是一个更大行高的段落。<br>
		</p>
	</body>
</html>
```
### 示例三：direction 设置元素的文本方向

这个例子演示了如何改变元素的文本方向。

```html
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style type="text/css">
			div.ex1 {direction:rtl;}
		</style>
	</head>
	<body>
		<div>一些文本。 默认书写方向</div>
		<div class="ex1">一些文本。从右到左的书写方向。</div>
	</body>
</html>
```

### 示例四：word-spacing 增加单词之间的空白空间

这个例子演示了如何增加一个段落中的单词之间的空白空间。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style type="text/css">
			p
			{ 
				word-spacing:30px;
			}
		</style>
	</head>
	<body>
		<p>
			This is some text. This is some text.
		</p>
	</body>
</html>
```

### 示例五：white-space 在元素内禁用文字环绕

这个例子演示了如何禁用一个元素内的文字环绕。
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style type="text/css">
			p
			{
				white-space:nowrap;
			}
		</style>
	</head>
	<body>
		<p>
			这是一些文本。这是一些文本。这是一些文本。这是一些文本。这是一些文本。
			这是一些文本。这是一些文本。这是一些文本。这是一些文本。这是一些文本。
			这是一些文本。这是一些文本。这是一些文本。这是一些文本。这是一些文本。
			这是一些文本。这是一些文本。这是一些文本。这是一些文本。这是一些文本。
			这是一些文本。这是一些文本。这是一些文本。这是一些文本。这是一些文本。
		</p>
	</body>
</html>
```

### 示例六：vertical-align 垂直对齐图像

这个例子演示了如何设置文本的垂直对齐图像。

[示例](https://www.runoob.com/try/try.php?filename=trycss_vertical-align)

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			img.top {vertical-align:text-top;}
			img.bottom {vertical-align:text-bottom;}
		</style>
	</head>
	<body>
		<p>一个<img src="logo.png" alt="w3cschool" width="270" height="50" />默认对齐的图像。</p> 
		<p>一个<img class="top" src="logo.png" alt="w3cschool" width="270" height="50" />  text-top 对齐的图像。</p> 
		<p>一个<img class="bottom" src="logo.png" alt="w3cschool" width="270" height="50" /> text-bottom 对齐的图像。</p>
	</body>
</html>
```

### 示例七：text-shadow 添加文本阴影

这个例子演示了如何设置文本阴影。
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			h1 {text-shadow:2px 2px #FF0000;}
		</style>
	</head>
	<body>
		<h1>Text-shadow 效果</h1>
		<p><b>注意：</b> Internet Explorer 9 以及更早的浏览器不支持 text-shadow 属性。</p>
	</body>
</html>
```

### 所有CSS文本属性。

|属性|描述|
|--|--|
|color|设置文本颜色|
|direction|设置文本方向。|
|letter-spacing|设置字符间距|
|line-height|设置行高|
|text-align|对齐元素中的文本|
|text-decoration|向文本添加修饰|
|text-indent|缩进元素中文本的首行|
|text-shadow|设置文本阴影|
|text-transform|控制元素中的字母|
|unicode-bidi|设置或返回文本是否被重写 |
|vertical-align|设置元素的垂直对齐|
|white-space|设置元素中空白的处理方式|
|word-spacing|设置字间距|

### letter-spacing 与 word-spacing：
```html
<style>
h1{
    letter-spacing:30px;
}
</style>
...
<h1>letter spacing</h1>
```

letter-spacing 这个样式使用在英文单词时，是设置字母与字母之间的间距。

如果想设置英文单词之间的间距，可以使用 word-spacing 来实现。如下代码：
```html
<style>
h1{
    word-spacing:30px;
}
</style>
...
<h1>word spacing</h1>
```

汉字的间隔调节也是用 letter-spacing 来实现的。

因为中文段落里字与字之间没有空格，因而 word-spacing 通常起不到调整间距的作用。

### CSS 字体

CSS字体属性定义字体，加粗，大小，文字样式。

### serif和sans-serif字体之间的区别

Serif vs. Sans-serif
![](serif.gif)
在计算机屏幕上，sans-serif字体被认为是比serif字体容易阅读

### CSS字型

在CSS中，有两种类型的字体系列名称：

+ 通用字体系列 - 拥有相似外观的字体系统组合（如 "Serif" 或 "Monospace"）
+ 特定字体系列 - 一个特定的字体系列（如 "Times" 或 "Courier"）

| Generic family | 字体系列 | 说明 |
| -------------- | -------- | ---- |
|Serif|Times New Roman <br> Georgia|Serif字体中字符在行的末端拥有额外的装饰|
|Sans-serif|Arial <br> Verdana|"Sans"是指无 - 这些字体在末端没有额外的装饰|
|Monospace|Courier New <br> Lucida Console|所有的等宽字符具有相同的宽度|

### font-family 字体系列

font-family 属性设置文本的字体系列。

font-family 属性应该设置几个字体名称作为一种"后备"机制，如果浏览器不支持第一种字体，他将尝试下一种字体。

注意: 如果字体系列的名称超过一个字（word），它必须用引号，如Font Family："宋体"。

多个字体系列是用一个逗号分隔指明：
```css
p{font-family:"Times New Roman", Times, serif;}
```

对于较常用的字体组合，看看我们的 [Web安全字体组合](https://www.runoob.com/cssref/css-websafe-fonts.html)。

### font-style 字体样式

主要是用于指定斜体文字的字体样式属性。

这个属性有三个值：

+ 正常 - 正常显示文本
+ 斜体 - 以斜体字显示的文字
+ 倾斜的文字 - 文字向一边倾斜（和斜体非常类似，但不太支持）

```css
p.normal {font-style:normal;}
p.italic {font-style:italic;}
p.oblique {font-style:oblique;}
```

#### italic 和 oblique 的区别

一种字体有粗体、斜体、下划线、删除线等诸多属性。

但是并不是所有字体都做了这些，一些不常用的字体，或许就只有个正常体，如果你用 italic，就没有效果了~

这时候你就要用 oblique，可以理解成 italic 是使用文字的斜体，oblique 是让没有斜体属性的文字倾斜！

另 CSS2.0 上边的解释你参考下：italic 和 oblique 都是向右倾斜的文字, 但区别在于 italic 是指斜体字，而 oblique 是倾斜的文字，对于没有斜体的字体应该使用 oblique 属性值来实现倾斜的文字效果。

### font-size 字体大小

font-size 属性设置文本的大小。

能否管理文字的大小，在网页设计中是非常重要的。但是，你不能通过调整字体大小使段落看上去像标题，或者使标题看上去像段落。

请务必使用正确的HTML标签，就\<h1> - \<h6>表示标题和\<p>表示段落：

字体大小的值可以是绝对或相对的大小。

绝对大小：

+ 设置一个指定大小的文本
+ 不允许用户在所有浏览器中改变文本大小
+ 确定了输出的物理尺寸时绝对大小很有用

相对大小：

+ 相对于周围的元素来设置大小
+ 允许用户在浏览器中改变文字大小

*如果你不指定一个字体的大小，默认大小和普通文本段落一样，是16像素（16px=1em）。*

### font-size 设置字体大小像素

设置文字的大小与像素，让您完全控制文字大小：
```css
h1 {font-size:40px;}
h2 {font-size:30px;}
p {font-size:14px;}
```
[示例](https://www.runoob.com/try/try.php?filename=trycss_font-size_px)

上面的例子可以在 Internet Explorer 9, Firefox, Chrome, Opera, 和 Safari 中通过缩放浏览器调整文本大小。

虽然可以通过浏览器的缩放工具调整文本大小，但是，这种调整是整个页面，而不仅仅是文本

### font-size:em 用em来设置字体大小

为了避免Internet Explorer 中无法调整文本的问题，许多开发者使用 em 单位代替像素。

em的尺寸单位由W3C建议。

1em和当前字体大小相等。在浏览器中默认的文字大小是16px。

因此，1em的默认大小是16px。可以通过下面这个公式将像素转换为em：**px/16=em**

```css
h1 {font-size:2.5em;} /* 40px/16=2.5em */
h2 {font-size:1.875em;} /* 30px/16=1.875em */
p {font-size:0.875em;} /* 14px/16=0.875em */
```

在上面的例子，em的文字大小是与前面的例子中像素一样。不过，如果使用 em 单位，则可以在所有浏览器中调整文本大小。

不幸的是，仍然是IE浏览器的问题。调整文本的大小时，会比正常的尺寸更大或更小。

### font-size:% 使用百分比和EM组合

在所有浏览器的解决方案中，设置 \<body>元素的默认字体大小的是百分比：

```css
body {font-size:100%;}
h1 {font-size:2.5em;}
h2 {font-size:1.875em;}
p {font-size:0.875em;}
```

我们的代码非常有效。在所有浏览器中，可以显示相同的文本大小，并允许所有浏览器缩放文本的大小。

### 示例一：font-weight 设置字体加粗

这个例子演示了如何设置字体的加粗。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title>
		<style>
			p.normal {font-weight:normal;}
			p.light {font-weight:lighter;}
			p.thick {font-weight:bold;}
			p.thicker {font-weight:900;}
		</style>
	</head>
	<body>
		<p class="normal">This is a paragraph.</p>
		<p class="light">This is a paragraph.</p>
		<p class="thick">This is a paragraph.</p>
		<p class="thicker">This is a paragraph.</p>
	</body>
</html>
```

### 示例二：font-variant 可以设置字体的转变

这个例子演示了如何设置字体的转变。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title>
		<style>
			p.normal {font-variant:normal;}
			p.small {font-variant:small-caps;}
		</style>
	</head>
	<body>
		<p class="normal">My name is Hege Refsnes.</p>
		<p class="small">My name is Hege Refsnes.</p>
	</body>
</html>
```

### 示例三：font 在一个声明中的所有字体属性

本例演示如何使用简写属性将字体属性设置在一个声明之内。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title>
		<style>
			p.ex1
			{
				font:15px arial,sans-serif;
			}

			p.ex2
			{
				font:italic bold 12px/30px Georgia,serif;
			}
		</style>
	</head>
	<body>
		<p class="ex1">This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph.</p>
		<p class="ex2">This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph. This is a paragraph.</p>
	</body>
</html>
```

### 所有CSS字体属性

|Propert|描述|
|--|--|
|font|在一个声明中设置所有的字体属性|
|font-family|指定文本的字体系列|
|font-size|指定文本的字体大小|
|font-style|指定文本的字体样式|
|font-variant|以小型大写字体或者正常字体显示文本。|
|font-weight|指定字体的粗细。|

## CSS 链接

不同的链接可以有不同的样式。

### a: 链接样式

链接的样式，可以用任何CSS属性（如颜色，字体，背景等）。

特别的链接，可以有不同的样式，这取决于他们是什么状态。

这四个链接状态是：

- a:link - 正常，未访问过的链接
- a:visited - 用户已访问过的链接
- a:hover - 当用户鼠标放在链接上时
- a:active - 链接被点击的那一刻

```css
a:link {color:#000000;}      /* 未访问链接*/
a:visited {color:#00FF00;}  /* 已访问链接 */
a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
a:active {color:#0000FF;}  /* 鼠标点击时 */
```

当设置为若干链路状态的样式，也有一些顺序规则：

a:hover 必须跟在 a:link 和 a:visited后面
a:active 必须跟在 a:hover后面

### text-decoration 常见的链接样式
根据上述链接的颜色变化的例子，看它是在什么状态。

让我们通过一些其他常见的方式转到链接样式：

文本修饰
text-decoration 属性主要用于删除链接中的下划线：

```css
a:link {text-decoration:none;}
a:visited {text-decoration:none;}
a:hover {text-decoration:underline;}
a:active {text-decoration:underline;}
```

### background-color 背景颜色

背景颜色属性指定链接背景色：

```css
a:link {background-color:#B2FF99;}
a:visited {background-color:#FFFF85;}
a:hover {background-color:#FF704D;}
a:active {background-color:#FF704D;}
```

### 示例一：添加不同样式的超链接

这个例子演示了如何为超链接添加其他样式。

[示例](https://www.runoob.com/try/try.php?filename=trycss_link2)

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8"> 
        <title>菜鸟教程(runoob.com)</title> 
        <style>
            a.one:link {color:#ff0000;}
            a.one:visited {color:#0000ff;}
            a.one:hover {color:#ffcc00;}
            
            a.two:link {color:#ff0000;}
            a.two:visited {color:#0000ff;}
            a.two:hover {font-size:150%;}
            
            a.three:link {color:#ff0000;}
            a.three:visited {color:#0000ff;}
            a.three:hover {background:#66ff66;}
            
            a.four:link {color:#ff0000;}
            a.four:visited {color:#0000ff;}
            a.four:hover {font-family:Georgia, serif;}
            
            a.five:link {color:#ff0000;text-decoration:none;}
            a.five:visited {color:#0000ff;text-decoration:none;}
            a.five:hover {text-decoration:underline;}
        </style>
    </head>
    <body>
        <p>将鼠标移至链接上改变样式.</p>
        <p><b><a class="one" href="/css/" target="_blank">这个链接改变颜色</a></b></p>
        <p><b><a class="two" href="/css/" target="_blank">这个链接改变字体大小</a></b></p>
        <p><b><a class="three" href="/css/" target="_blank">这个链接改变背景颜色</a></b></p>
        <p><b><a class="four" href="/css/" target="_blank">这个链接改变字体类型</a></b></p>
        <p><b><a class="five" href="/css/" target="_blank">这个链接改变文字修饰</a></b></p>
    </body>
</html>
```

### 示例二：高级 - 创建链接框

这个例子演示了一个更高级的例子，我们结合若干CSS属性显示为方框。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			a:link,a:visited
			{
				display:block;
				font-weight:bold;
				color:#FFFFFF;
				background-color:#98bf21;
				width:120px;
				text-align:center;
				padding:4px;
				text-decoration:none;
			}
			a:hover,a:active
			{
				background-color:#7A991A;
			}
		</style>
	</head>
	<body>
		<a href="/css/" target="_blank">这是一个链接</a>
	</body>
</html>
```

## CSS 列表

CSS列表属性作用如下：

- 设置不同的列表项标记为有序列表
- 设置不同的列表项标记为无序列表
- 设置列表项标记为图像

### 列表

在HTML中，有两种类型的列表：

- 无序列表 - 列表项标记用特殊图形（如小黑点、小方框等）
- 有序列表 - 列表项的标记有数字或字母
- 
使用CSS，可以列出进一步的样式，并可用图像作列表项标记。

### list-style-type 不同的列表项标记

list-style-type属性指定列表项标记的类型是：

```css
ul.a {list-style-type: circle;}
ul.b {list-style-type: square;}
 
ol.c {list-style-type: upper-roman;}
ol.d {list-style-type: lower-alpha;}
```

一些值是无序列表，以及有些是有序列表。

###  list-style-image作为列表项标记的图像

要指定列表项标记的图像，使用列表样式图像属性：

```css
ul
{
    list-style-image: url('sqpurple.gif');
}
```

上面的例子在所有浏览器中显示并不相同，IE和Opera显示图像标记比火狐，Chrome和Safari更高一点点。

如果你想在所有的浏览器放置同样的形象标志，就应使用浏览器兼容性解决方案，过程如下

#### 浏览器兼容性解决方案

同样在所有的浏览器，下面的例子会显示的图像标记：

```css
ul
{
    list-style-type: none;
    padding: 0px;
    margin: 0px;
}
ul li
{
    background-image: url(sqpurple.gif);
    background-repeat: no-repeat;
    background-position: 0px 5px; 
    padding-left: 14px; 
}
```

例子解释：

- ul:
	+ 设置列表类型为没有列表项标记
	+ 设置填充和边距0px（浏览器兼容性）
- ul中所有li:
	+ 设置图像的URL，并设置它只显示一次（无重复）
	+ 您需要的定位图像位置（左0px和上下5px）
	+ 用padding-left属性把文本置于列表中

### list-style 列表 -简写属性

在单个属性中可以指定所有的列表属性。这就是所谓的简写属性。

为列表使用简写属性，列表样式属性设置如下：

```css
ul
{
    list-style: square url("sqpurple.gif");
}
```

可以按顺序设置如下属性：

+ list-style-type
+ list-style-position (有关说明，请参见下面的CSS属性表)
+ list-style-image

如果上述值丢失一个，其余仍在指定的顺序，就没关系。

### 示例：所有不同的列表项标记

这个例子演示了所有不同的CSS列表项标记。

[全部的标记](https://www.runoob.com/try/try.php?filename=trycss_list-style-type_all)

### 所有的CSS列表属性

|属性|描述|
|--|--|
|list-style|简写属性。用于把所有用于列表的属性设置于一个声明中|
|list-style-image|将图像设置为列表项标志。|
|list-style-position|设置列表中列表项标志的位置。|
|list-style-type|设置列表项标志的类型。|

## CSS 表格

使用 CSS 可以使 HTML 表格更美观。

### border 表格边框

指定CSS表格边框，使用border属性。

下面的例子指定了一个表格的Th和TD元素的黑色边框：
```css
table, th, td
{
    border: 1px solid black;
}
```

请注意，在上面的例子中的表格有双边框。这是因为表和th/ td元素有独立的边界。

为了显示一个表的单个边框，使用 border-collapse属性。

### border-collapse 折叠边框

border-collapse 属性设置表格的边框是否被折叠成一个单一的边框或隔开：
```css
table
{
    border-collapse:collapse;
}
table,th, td
{
    border: 1px solid black;
}
```

### width / height表格宽度和高度

Width和height属性定义表格的宽度和高度。

下面的例子是设置100％的宽度，50像素的th元素的高度的表格：

```css
table 
{
    width:100%;
}
th
{
    height:50px;
}
```

### text-align 表格文字对齐

表格中的文本对齐和垂直对齐属性。

text-align属性设置水平对齐方式，向左，右，或中心：
```css
td
{
    text-align:right;
}
```

### 表格填充

如果在表的内容中控制空格之间的边框，应使用td和th元素的填充属性：
```css
td
{
    padding:15px;
}
```

### 表格颜色

下面的例子指定边框的颜色，和th元素的文本和背景颜色：
```css
table, td, th
{
    border:1px solid green;
}
th
{
    background-color:green;
    color:white;
}
```

## CSS 盒子模型

CSS 盒子模型(Box Model)

所有HTML元素可以看作盒子，在CSS中，"box model"这一术语是用来设计和布局时使用。

CSS盒模型本质上是一个盒子，封装周围的HTML元素，它包括：边距，边框，填充，和实际内容。

盒模型允许我们在其它元素和周围元素边框之间的空间放置元素。

下面的图片说明了盒子模型(Box Model)：

![](box-model.gif)

不同部分的说明：

+ **Margin(外边距)** - 清除边框外的区域，外边距是透明的。
+ **Border(边框)** - 围绕在内边距和内容外的边框。
+ **Padding(内边距)** - 清除内容周围的区域，内边距是透明的。
+ **Content(内容)** - 盒子的内容，显示文本和图像。

为了正确设置元素在所有浏览器中的宽度和高度，你需要知道的盒模型是如何工作的。

### 元素的宽度和高度

Remark重要: 当您指定一个 CSS 元素的宽度和高度属性时，你只是设置内容区域的宽度和高度。要知道，完整大小的元素，你还必须添加内边距，边框和边距。

下面的例子中的元素的总宽度为300px：
```css
div {
    width: 300px;
    border: 25px solid green;
    padding: 25px;
    margin: 25px;
}
```

让我们自己算算：
300px (宽)
+ 50px (左 + 右填充)
+ 50px (左 + 右边框)
+ 50px (左 + 右边距)
= 450px

试想一下，你只有250像素的空间。让我们设置总宽度为250像素的元素:
```css
div {
    width: 220px;
    padding: 10px;
    border: 5px solid gray;
    margin: 0; 
}
```

最终元素的总宽度计算公式是这样的：

**总元素的宽度=宽度+左填充+右填充+左边框+右边框+左边距+右边距**

元素的总高度最终计算公式是这样的：

**总元素的高度=高度+顶部填充+底部填充+上边框+下边框+上边距+下边距**

### 浏览器的兼容性问题

一旦为页面设置了恰当的 DTD，大多数浏览器都会按照上面的图示来呈现内容。然而 IE 5 和 6 的呈现却是不正确的。根据 W3C 的规范，元素内容占据的空间是由 width 属性设置的，而内容周围的 padding 和 border 值是另外计算的。不幸的是，IE5.X 和 6 在怪异模式中使用自己的非标准模型。这些浏览器的 width 属性不是内容的宽度，而是内容、内边距和边框的宽度的总和。

虽然有方法解决这个问题。但是目前最好的解决方案是回避这个问题。也就是，不要给元素添加具有指定宽度的内边距，而是尝试将内边距或外边距添加到元素的父元素和子元素。

IE8 及更早IE版本不支持设置填充的宽度和边框的宽度属性。

解决IE8及更早版本不兼容问题可以在HTML页面声明 <!DOCTYPE html>即可。

## CSS 边框

### CSS 边框属性

CSS边框属性允许你指定一个元素边框的样式和颜色。

### border-style 边框样式

边框样式属性指定要显示什么样的边界。

border-style属性用来定义边框的样式

border-style 值:

+ none: 默认无边框
+ dotted: 定义一个点线边框
+ dashed: 定义一个虚线边框
+ solid: 定义实线边框
+ double: 定义两个边框。 两个边框的宽度和 border-width 的值相同
+ groove: 定义3D沟槽边框。效果取决于边框的颜色值
+ ridge: 定义3D脊边框。效果取决于边框的颜色值
+ inset:定义一个3D的嵌入边框。效果取决于边框的颜色值
+ outset: 定义一个3D突出边框。 效果取决于边框的颜色值

尝试一下: [设置边框样式](https://www.runoob.com/try/try.php?filename=trycss_border-style)

### border-width 边框宽度
您可以通过 border-width 属性为边框指定宽度。

为边框指定宽度有两种方法：可以指定长度值，比如 2px 或 0.1em(单位为 px, pt, cm, em 等)，或者使用 3 个关键字之一，它们分别是 thick 、medium（默认值） 和 thin。

注意：CSS 没有定义 3 个关键字的具体宽度，所以一个用户可能把 thick 、medium 和 thin 分别设置为等于 5px、3px 和 2px，而另一个用户则分别设置为 3px、2px 和 1px。

```css
p.one
{
    border-style:solid;
    border-width:5px;
}
p.two
{
    border-style:solid;
    border-width:medium;
}
```

### border-color 边框颜色
border-color属性用于设置边框的颜色。可以设置的颜色：

+ name - 指定颜色的名称，如 "red"
+ RGB - 指定 RGB 值, 如 "rgb(255,0,0)"
+ Hex - 指定16进制值, 如 "#ff0000"

您还可以设置边框的颜色为"transparent"。

注意： *border-color单独使用是不起作用的，必须得先使用border-style来设置边框样式。*
```css
p.one
{
    border-style:solid;
    border-color:red;
}
p.two
{
    border-style:solid;
    border-color:#98bf21;
}
```

### 边框-单独设置各边

在CSS中，可以指定不同的侧面不同的边框：
```css
p
{
    border-top-style:dotted;
    border-right-style:solid;
    border-bottom-style:dotted;
    border-left-style:solid;
}
```

上面的例子也可以设置一个单一属性：
```css
border-style:dotted solid;
```

border-style属性可以有1-4个值：

- **border-style:dotted solid double dashed;**
  - 上边框是 dotted
  - 右边框是 solid
  - 底边框是 double
  - 左边框是 dashed
- **border-style:dotted solid double;**
  - 上边框是 dotted
  - 左、右边框是 solid
  - 底边框是 double
- **border-style:dotted solid;**
  - 上、底边框是 dotted
  - 右、左边框是 solid
- **border-style:dotted;**
  - 四面边框是 dotted

上面的例子用了border-style。然而，它也可以和border-width 、 border-color一起使用。

+ **border-style：属性1，属性2，属性3，属性4**
	- 上->右->下->左
+ **border-style：属性1，属性2，属性3**
	- 上->左右->下
+ **border-style：属性1，属性2**
	- 上下->左右
+ **border-style：属性1**
	- 上下左右属性相同

### border 边框-简写属性

上面的例子用了很多属性来设置边框。

你也可以在一个属性中设置边框。

你可以在"border"属性中设置：

+ border-width
+ border-style (required)
+ border-color

```css
border:5px solid red;
```

### CSS 边框属性

|属性|描述|
|--|--|
|border|简写属性，用于把针对四个边的属性设置在一个声明。|
|border-style|用于设置元素所有边框的样式，或者单独地为各边设置边框样式。|
|border-width|简写属性，用于为元素的所有边框设置宽度，或者单独地为各边边框设置宽度。|
|border-color|简写属性，设置元素的所有边框中可见部分的颜色，或为 4 个边分别设置颜色。|
|border-bottom|简写属性，用于把下边框的所有属性设置到一个声明中。|
|border-bottom-color|设置元素的下边框的颜色。|
|border-bottom-style|设置元素的下边框的样式。|
|border-bottom-width|设置元素的下边框的宽度。|
|border-left|简写属性，用于把左边框的所有属性设置到一个声明中。|
|border-left-color|设置元素的左边框的颜色。|
|border-left-style|设置元素的左边框的样式。|
|border-left-width|设置元素的左边框的宽度。|
|border-right|简写属性，用于把右边框的所有属性设置到一个声明中。|
|border-right-color|设置元素的右边框的颜色。|
|border-right-style|设置元素的右边框的样式。|
|border-right-width|设置元素的右边框的宽度。|
|border-top|简写属性，用于把上边框的所有属性设置到一个声明中。|
|border-top-color|设置元素的上边框的颜色。|
|border-top-style|设置元素的上边框的样式。|
|border-top-width|设置元素的上边框的宽度。|

## CSS 轮廓（outline）

轮廓（outline）是绘制于元素周围的一条线，位于边框边缘的外围，可起到突出元素的作用。

轮廓（outline）属性指定元素轮廓的样式、颜色和宽度。

![](box_outline.gif)

### 所有CSS 轮廓（outline）属性

"CSS" 列中的数字表示哪个CSS版本定义了该属性(CSS1 或者CSS2)。

|属性|说明|值|CSS|
|:--|:--|:--|:--|
|outline|在一个声明中设置所有的轮廓属性|*outline-color <br> outline-style <br> outline-width <br> *inherit|2|
|outline-color|设置轮廓的颜色|*color-name <br> hex-number <br> rgb-number <br> *invert inherit|2|
|outline-style|设置轮廓的样式|none <br> dotted <br> dashed <br> solid <br> double <br> groove <br> ridge <br> inset <br> outset <br> inherit|2|
|outline-width|设置轮廓的宽度|thin <br> medium <br> thick <br> *length <br> *inherit|2|

### tips

1.outline是不占空间的，既不会增加额外的width或者height（这样不会导致浏览器渲染时出现reflow或是repaint）

2.outline有可能是非矩形的（火狐浏览器下）

## CSS margin(外边距)

CSS margin(外边距)属性定义元素周围的空间。

### margin

margin 清除周围的（外边框）元素区域。margin 没有背景颜色，是完全透明的。

margin 可以单独改变元素的上，下，左，右边距，也可以一次改变所有的属性。

![](VlwVi.png)

### 可能的值

|值|说明|
|--|--|
|auto|设置浏览器边距。这样做的结果会依赖于浏览器|
|length|定义一个固定的margin（使用像素，pt，em等）|
|%|定义一个使用百分比的边距|

*Margin可以使用负值，重叠的内容。*

### Margin - 单边外边距属性

在CSS中，它可以指定不同的侧面不同的边距：

```css
margin-top:100px;
margin-bottom:100px;
margin-right:50px;
margin-left:50px;
```

### Margin - 简写属性

为了缩短代码，有可能使用一个属性中margin指定的所有边距属性。这就是所谓的简写属性。

所有边距属性的简写属性是 `margin` :

实例
```css
margin:100px 50px;
```

margin属性可以有一到四个值。

- margin:25px 50px 75px 100px;
	+ 上边距为25px
	+ 右边距为50px
	+ 下边距为75px
	+ 左边距为100px

- margin:25px 50px 75px;
	+ 上边距为25px
	+ 左右边距为50px
	+ 下边距为75px

- margin:25px 50px;
	+ 上下边距为25px
	+ 左右边距为50px

- margin:25px;
	+ 所有的4个边距都是25px

### 所有的CSS边距属性

|属性|描述|
|--|--|
|margin|简写属性。在一个声明中设置所有外边距属性。|
|margin-bottom|设置元素的下外边距。|
|margin-left|设置元素的左外边距。|
|margin-right|设置元素的右外边距。|
|margin-top|设置元素的上外边距。|

## CSS padding（填充）

CSS padding（填充）是一个简写属性，定义元素边框与元素内容之间的空间，即上下左右的内边距。

### padding（填充）

当元素的 padding（填充）内边距被清除时，所释放的区域将会受到元素背景颜色的填充。

单独使用 padding 属性可以改变上下左右的填充。

![](VlwVi1.png)

### 可能的值

|值|说明|
|--|--|
|length|定义一个固定的填充(像素, pt, em,等)|
|%|使用百分比值定义一个填充|

### 填充- 单边内边距属性

在CSS中，它可以指定不同的侧面不同的填充：

```css
padding-top:25px;
padding-bottom:25px;
padding-right:50px;
padding-left:50px;
```

- 上内边距是 25px
- 右内边距是 50px
- 下内边距是 25px
- 左内边距是 50px

### 填充 - 简写属性

为了缩短代码，它可以在一个属性中指定的所有填充属性。

这就是所谓的简写属性。所有的填充属性的简写属性是 padding :

```css
padding:25px 50px;
```

Padding属性，可以有一到四个值。

- padding:25px 50px 75px 100px;
	+ 上填充为25px
	+ 右填充为50px
	+ 下填充为75px
	+ 左填充为100px
  
- padding:25px 50px 75px;
	+ 上填充为25px
	+ 左右填充为50px
	+ 下填充为75px

- padding:25px 50px;
	+ 上下填充为25px
	+ 左右填充为50px

- padding:25px;
	+ 所有的填充都是25px

### 所有的CSS填充属性

|属性|说明|
|--|--|
|padding|使用简写属性设置在一个声明中的所有填充属性|
|padding-bottom|设置元素的底部填充|
|padding-left|设置元素的左部填充|
|padding-right|设置元素的右部填充|
|padding-top|设置元素的顶部填充|

## CSS 分组 和 嵌套 选择器

### 分组选择器

在样式表中有很多具有相同样式的元素。

```css
h1
{
    color:green;
}
h2
{
    color:green;
}
p
{
    color:green;
}
```

为了尽量减少代码，你可以使用分组选择器。

每个选择器用逗号分隔。

在下面的例子中，我们对以上代码使用分组选择器：

```css
h1,h2,p
{
    color:green;
}
```

### 嵌套选择器

它可能适用于选择器内部的选择器的样式。

在下面的例子设置了三个样式：

- `p{ }`: 为所有 p 元素指定一个样式。
- `.marked{ }`: 为所有 class="marked" 的元素指定一个样式。
- `.marked p{ }`: 为所有 class="marked" 元素内的 p 元素指定一个样式。
- `p.marked{ }`: 为所有 class="marked" 的 p 元素指定一个样式。

```css
p
{
    color:blue;
    text-align:center;
}
.marked
{
    background-color:red;
}
.marked p
{
    color:white;
}
p.marked{
    text-decoration:underline;
}
```

## CSS 尺寸 (Dimension)

CSS 尺寸 (Dimension) 属性允许你控制元素的高度和宽度。同样，它允许你增加行间距。

### 所有CSS 尺寸 (Dimension)属性

|属性|描述|
|--|--|
|height|设置元素的高度。|
|line-height|设置行高。|
|max-height|设置元素的最大高度。|
|max-width|设置元素的最大宽度。|
|min-height|设置元素的最小高度。|
|min-width|设置元素的最小宽度。|
|width|设置元素的宽度。|

## CSS Display(显示) 与 Visibility（可见性）

display属性设置一个元素应如何显示，visibility属性指定一个元素应可见还是隐藏。

### 隐藏元素 - display:none或visibility:hidden

隐藏一个元素可以通过把display属性设置为"none"，或把visibility属性设置为"hidden"。但是请注意，这两种方法会产生不同的结果。

`visibility:hidden`可以隐藏某个元素，但隐藏的元素仍需占用与未隐藏之前一样的空间。也就是说，该元素虽然被隐藏了，但仍然会影响布局。

`display:none`可以隐藏某个元素，且隐藏的元素不会占用任何空间。也就是说，该元素不但被隐藏了，而且该元素原本占用的空间也会从页面布局中消失。

对于 CSS 里的 visibility 属性，通常其值被设置成 visible 或 hidden。

visibility: hidden 相当于 display:none，能把元素隐藏起来，但两者的区别在于：

1. display:none 元素不再占用空间。
2. visibility: hidden 使元素在网页上不可见，但仍占用空间。
然而，visibility 还可能取值为 collapse 。

当设置元素 visibility: collapse 后，一般的元素的表现与 visibility: hidden 一样，也即其会占用空间。但如果该元素是与 table 相关的元素，例如 table row、table column、table column group、table column group 等，其表现却跟 display: none 一样，也即其占用的空间会释放。

在不同浏览器下，对 visibility: collapse 的处理方式不同：

1. visibility: collapse 的上述特性仅在 Firefox 下起作用。
2. 在 IE 即使设置了 visibility: collapse，还是会显示元素。
3. 在 Chrome 下，即使会将元素隐藏，但无论是否是与 table 相关的元素，visibility: collapse 与 visibility: hidden 没有什么区别，即仍会占用空间。

### CSS Display - 块和内联元素

块元素是一个元素，占用了全部宽度，在前后都是换行符。

块元素的例子：
- \<h1>
- \<p>
- \<div>

内联元素只需要必要的宽度，不强制换行。

内联元素的例子：
- \<span>
- \<a>

### 如何改变一个元素显示

可以更改内联元素和块元素，反之亦然，可以使页面看起来是以一种特定的方式组合，并仍然遵循web标准。

下面的示例把列表项显示为内联元素：
```css
li {display:inline;}
```

下面的示例把span元素作为块元素：
```css
span {display:block;}
```

**注意**：变更元素的显示类型看该元素是如何显示，它是什么样的元素。例如：一个内联元素设置为display:block是不允许有它内部的嵌套块元素。

### 块级元素(block)特性：

- 总是独占一行，表现为另起一行开始，而且其后的元素也必须另起一行显示;

- 宽度(width)、高度(height)、内边距(padding)和外边距(margin)都可控制;

### 内联元素(inline)特性：

- 和相邻的内联元素在同一行;

- 宽度(width)、高度(height)、内边距的top/bottom(padding-top/padding-bottom)和外边距的top/bottom(margin-top/margin-bottom)都不可改变，就是里面文字或图片的大小;

### 块级元素主要有：

- address , blockquote , center , dir , div , dl , fieldset , form , h1 , h2 , h3 , h4 , h5 , h6 , hr , isindex , menu , noframes , noscript , ol , p , pre , table , ul , li

### 内联元素主要有：

- a , abbr , acronym , b , bdo , big , br , cite , code , dfn , em , font , i , img , input , kbd , label , q , s , samp , select , small , span , strike , strong , sub , sup ,textarea , tt , u , var

### 可变元素(根据上下文关系确定该元素是块元素还是内联元素)：

- applet ,button ,del ,iframe , ins ,map ,object , script

### CSS中块级、内联元素的应用：

利用CSS我们可以摆脱上面表格里HTML标签归类的限制，自由地在不同标签/元素上应用我们需要的属性。

主要用的CSS样式有以下三个：

- display:block  -- 显示为块级元素
- display:inline  -- 显示为内联元素
- display:inline-block -- 显示为内联块元素，表现为同行显示并可修改宽高内外边距等属性

我们常将所有\<li>元素加上display:inline-block样式，原本垂直的列表就可以水平显示了。

## CSS Position(定位)

position 属性指定了元素的定位类型。

position 属性的五个值：

- static
- relative
- fixed
- absolute
- sticky

元素可以使用的顶部，底部，左侧和右侧属性定位。然而，这些属性无法工作，除非是先设定position属性。他们也有不同的工作方式，这取决于定位方法。

### static 定位

HTML 元素的默认值，即没有定位，遵循正常的文档流对象。

静态定位的元素不会受到 top, bottom, left, right影响。

[示例](https://www.runoob.com/try/try.php?filename=trycss_position_static)

```css
div.static {
    position: static;
    border: 3px solid #73AD21;
}
```

### fixed 定位

元素的位置相对于浏览器窗口是固定位置。

即使窗口是滚动的它也不会移动：

[示例](https://www.runoob.com/try/try.php?filename=trycss_position_fixed)

```css
p.pos_fixed
{
    position:fixed;
    top:30px;
    right:5px;
}
```

*注意： Fixed 定位在 IE7 和 IE8 下需要描述 !DOCTYPE 才能支持。
Fixed定位使元素的位置与文档流无关，因此不占据空间。
Fixed定位的元素和其他元素重叠。*

### relative 定位

相对定位元素的定位是相对其正常位置。

**relative**：定位是相对于自身位置定位（设置偏移量的时候，会相对于自身所在的位置偏移）。设置了 relative 的元素仍然处在文档流中，元素的宽高不变，设置偏移量也不会影响其他元素的位置。最外层容器设置为 relative 定位，在没有设置宽度的情况下，宽度是整个浏览器的宽度。

[示例](https://www.runoob.com/try/try.php?filename=trycss_position_relative)

```css
h2.pos_left
{
    position:relative;
    left:-20px;
}
h2.pos_right
{
    position:relative;
    left:20px;
}
```

移动相对定位元素，但它原本所占的空间不会改变。

[示例](https://www.runoob.com/try/try.php?filename=trycss_position_relative2)

```css
h2.pos_top
{
    position:relative;
    top:-50px;
}
```

相对定位元素经常被用来作为绝对定位元素的容器块。

### absolute 定位

绝对定位的元素的位置相对于最近的已定位父元素，如果元素没有已定位的父元素，那么它的位置相对于\<html>:

**absolute**：定位是相对于离元素最近的设置了绝对或相对定位的父元素决定的，如果没有父元素设置绝对或相对定位，则元素相对于根元素即 html 元素定位。设置了 absolute 的元素脱了了文档流，元素在没有设置宽度的情况下，宽度由元素里面的内容决定。脱离后原来的位置相当于是空的，下面的元素会来占据位置。

[示例](https://www.runoob.com/try/try.php?filename=trycss_position_absolute)

```css
h2
{
    position:absolute;
    left:100px;
    top:150px;
}
```

absolute 定位使元素的位置与文档流无关，因此不占据空间。

absolute 定位的元素和其他元素重叠。

### sticky 定位

sticky 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。

`position: sticky`; 基于用户的滚动位置来定位。

粘性定位的元素是依赖于用户的滚动，在`position:relative`与`position:fixed`定位之间切换。

它的行为就像`position:relative`;而当页面滚动超出目标区域时，它的表现就像`position:fixed`，它会固定在目标位置。

元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。

这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。

注意: Internet Explorer, Edge 15 及更早 IE 版本不支持 sticky 定位。 Safari 需要使用 -webkit- prefix (查看以下实例)。

[示例](https://www.runoob.com/try/try.php?filename=trycss_position_sticky)

```css
div.sticky {
    position: -webkit-sticky; /* Safari */
    position: sticky;
    top: 0;
    background-color: green;
    border: 2px solid #4CAF50;
}
```

### 重叠的元素

元素的定位与文档流无关，所以它们可以覆盖页面上的其它元素

z-index属性指定了一个元素的堆叠顺序（哪个元素应该放在前面，或后面）

**层级问题（谁高）**

**总结：**标准流盒子，低于浮动的盒子，浮动的盒子又低于定位的盒子。

定位高于浮动，浮动高于标准流。（高低和占不占位置无关）

用法：

1、必须有定位。（除去static之外）。

2、给定 z-index 的值为层级的值。（不给默认为0）

- a. 层级为0的盒子，也比标准流和浮动高。
- b. 层级为负数的盒子，比标准流和浮动低。
- c. 层级不取小数）
- d. 层级一样，后面的盒子比前面的层级高。
- e. 浮动或者标准流的盒子，后面的盒子比前面的层级高。
- f. abselute是不占位置的，relative是站位的的。而层级的高低，是和占不占位置没有关系的。

一个元素可以有正数或负数的堆叠顺序：

[示例](https://www.runoob.com/try/try.php?filename=trycss_zindex)

```css
img
{
    position:absolute;
    left:0px;
    top:0px;
    z-index:-1;
}
```

具有更高堆叠顺序的元素总是在较低的堆叠顺序元素的前面。

**注意**： 如果两个定位元素重叠，没有指定z - index，最后定位在HTML代码中的元素将被显示在最前面。

### 示例一：[裁剪元素的外形](https://www.runoob.com/try/try.php?filename=trycss_clip)

此示例演示如何设置元素的外形。该元素被剪裁成这种形状，并显示出来。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			img 
			{
				position:absolute;
				clip:rect(0px,60px,200px,0px);
			}
		</style>
	</head>
	<body>
		<img src="w3css.gif" width="100" height="140" />
	</body>
</html>
```

### 示例二：[如何使用滚动条来显示元素内溢出的内容](https://www.runoob.com/try/try.php?filename=trycss_overflow)

这个例子演示了overflow属性创建一个滚动条，当一个元素的内容在指定的区域过大时如何设置以适应。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			div.ex1 {
			    background-color: lightblue;
			    width: 110px;
			    height: 110px;
			    overflow: scroll;
			}
			div.ex2 {
			    background-color: lightblue;
 				width: 110px;
 				height: 110px;
			    overflow: hidden;
			}
			div.ex3 {
    			background-color: lightblue;
			    width: 110px;
			    height: 110px;
			    overflow: auto;
			}
			div.ex4 {
			    background-color: lightblue;
			    width: 110px;
			    height: 110px;
			    overflow: visible;
			}
		</style>
	</head>
	<body>
		<h1>overflow 属性</h1>
		<p>如果元素中的内容超出了给定的宽度和高度属性，overflow 属性可以确定是否显示滚动条等行为。</p>
		<h2>overflow: scroll:</h2>
		<div class="ex1">菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！</div>
		<h2>overflow: hidden:</h2>
		<div class="ex2">菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！</div>
		<h2>overflow: auto:</h2>
		<div class="ex3">菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！</div>
		<h2>overflow: visible (默认):</h2>
		<div class="ex4">菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！菜鸟教程 -- 学的不仅是技术，更是梦想！！！</div>
	</body>
</html>
```

### 示例三：[如何设置浏览器自动溢出处理](https://www.runoob.com/try/try.php?filename=trycss_pos_overflow_auto)

这个例子演示了如何设置浏览器来自动处理溢出。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
		<style>
			div 
			{
				background-color:#00FFFF;
				width:150px;
				height:150px;
				overflow:auto;
			}
		</style>
	</head>
	<body>
		<p>overflow 属性规定当内容溢出元素框时发生的事情。</p>
		<div>
			当你想更好的控制布局时你可以使用 overflow 属性。尝试修改 overflow 属性为: visible, hidden, scroll, 或 inherit 并查看效果。 默认值为 visible。
		</div>
	</body>
</html>
```

### 示例四：[更改光标](https://www.runoob.com/try/try.php?filename=trycss_cursor)

这个例子演示了如何改变光标。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>请把鼠标移动到单词上，可以看到鼠标指针发生变化：</p>
		<span style="cursor:auto">auto</span><br>
		<span style="cursor:crosshair">crosshair</span><br>
		<span style="cursor:default">default</span><br>
		<span style="cursor:e-resize">e-resize</span><br>
		<span style="cursor:help">help</span><br>
		<span style="cursor:move">move</span><br>
		<span style="cursor:n-resize">n-resize</span><br>
		<span style="cursor:ne-resize">ne-resize</span><br>
		<span style="cursor:nw-resize">nw-resize</span><br>
		<span style="cursor:pointer">pointer</span><br>
		<span style="cursor:progress">progress</span><br>
		<span style="cursor:s-resize">s-resize</span><br>
		<span style="cursor:se-resize">se-resize</span><br>
		<span style="cursor:sw-resize">sw-resize</span><br>
		<span style="cursor:text">text</span><br>
		<span style="cursor:w-resize">w-resize</span><br>
		<span style="cursor:wait">wait</span><br>
	</body>
</html>
```

### 所有的CSS定位属性

"CSS" 列中的数字表示哪个CSS(CSS1 或者CSS2)版本定义了该属性。

|属性|说明|值|CSS|
|:--|:--|:--|:--|
|[bottom](https://www.runoob.com/cssref/pr-pos-bottom.html)|定义了定位元素下外边距边界与其包含块下边界之间的偏移。|auto<br/>*length*<br/>%<br/>*inherit*|2|
|[clip](https://www.runoob.com/cssref/pr-pos-clip.html)|剪辑一个绝对定位的元素|*shape*<br/>*auto*<br/>inherit|2|
|[cursor](https://www.runoob.com/cssref/pr-class-cursor.html)|显示光标移动到指定的类型|*url*<br/>auto<br/>crosshair<br/>default<br/>pointer<br/>move<br/>e-resize<br/>ne-resize<br/>nw-resize<br/>n-resize<br/>se-resize<br/>sw-resize<br/>s-resize<br/>w-resize<br/>text<br/>wait <br/>help|2|
|[left](https://www.runoob.com/cssref/pr-pos-left.html)|定义了定位元素左外边距边界与其包含块左边界之间的偏移。|auto<br/>*length*<br/>%<br/>*inherit*|2|
|[overflow](https://www.runoob.com/cssref/pr-pos-overflow.html)|设置当元素的内容溢出其区域时发生的事情。|auto<br/>hidden<br/>scroll<br/>visible<br/>inherit|2|
|[overflow-y](https://www.runoob.com/css/cssref/css3-pr-overflow-y.html)|指定如何处理顶部/底部边缘的内容溢出元素的内容区域|auto<br/>hidden<br/>scroll<br/>visible<br/>no-display<br/>no-content|2|
|[overflow-x](https://www.runoob.com/css/cssref//cssref/css3-pr-overflow-x.html)|指定如何处理右边/左边边缘的内容溢出元素的内容区域|auto<br/>hidden<br/>scroll<br/>visible<br/>no-display<br/>no-content|2|
|[position](https://www.runoob.com/cssref/pr-class-position.html)|指定元素的定位类型|absolute<br/>fixed<br/>relative<br/>static<br/>inherit|2|
|[right](https://www.runoob.com/cssref/pr-pos-right.html)|定义了定位元素右外边距边界与其包含块右边界之间的偏移。|auto<br/>*length*<br/>%<br/>*inherit*|2|
|[top](https://www.runoob.com/cssref/pr-pos-top.html)|定义了一个定位元素的上外边距边界与其包含块上边界之间的偏移。|auto<br/>*length*<br/>%<br/>*inherit*|2|
|[z-index](https://www.runoob.com/cssref/pr-pos-z-index.html)|设置元素的堆叠顺序|*number*<br/>*auto*<br/>inherit|2|

## CSS 布局 - Overflow

CSS overflow 属性用于控制内容溢出元素框时显示的方式。

### CSS Overflow

CSS overflow 属性可以控制内容溢出元素框时在对应的元素区间内添加滚动条。

overflow属性有以下值：

|值|描述|
|:--|:--|
|visible|默认值。内容不会被修剪，会呈现在元素框之外。|
|hidden|内容会被修剪，并且其余内容是不可见的。|
|scroll|内容会被修剪，但是浏览器会显示滚动条以便查看其余的内容。|
|auto|如果内容被修剪，则浏览器会显示滚动条以便查看其余的内容。|
|inherit|规定应该从父元素继承 overflow 属性的值。|

## CSS Float(浮动)

### 什么是 CSS Float（浮动）？

CSS 的 Float（浮动），会使元素向左或向右移动，其周围的元素也会重新排列。

Float（浮动），往往是用于图像，但它在布局时一样非常有用。

### 元素怎样浮动

元素的水平方向浮动，意味着元素只能左右移动而不能上下移动。

一个浮动元素会尽量向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。

浮动元素之后的元素将围绕它。

浮动元素之前的元素将不会受到影响。

如果图像是右浮动，下面的文本流将环绕在它左边：[示例](https://www.runoob.com/try/try.php?filename=trycss_float)

```css
img
{
    float:right;
}
```

### 彼此相邻的浮动元素

如果你把几个浮动的元素放到一起，如果有空间的话，它们将彼此相邻。

在这里，我们对图片廊使用 float 属性：[示例](https://www.runoob.com/try/try.php?filename=trycss_float_elements)

```css
.thumbnail 
{
    float:left;
    width:110px;
    height:90px;
    margin:5px;
}
```

### 清除浮动 - 使用 clear

元素浮动之后，周围的元素会重新排列，为了避免这种情况，使用 clear 属性。

clear 属性指定元素两侧不能出现浮动元素。

使用 clear 属性往文本中添加图片廊：[示例](https://www.runoob.com/try/try2.php?filename=trycss_float_clear)

```css
.text_line
{
    clear:both;
}
```

### 示例一：[为图像添加边框和边距并浮动到段落的右侧](https://www.runoob.com/try/try.php?filename=trycss_float2)

让我们为图像添加边框和边距并浮动到段落的右侧

### 示例二：[标题和图片向右侧浮动](https://www.runoob.com/try/try.php?filename=trycss_float3)

让标题和图片向右侧浮动。

### 示例三：[让段落的第一个字母浮动到左侧](https://www.runoob.com/try/try.php?filename=trycss_float4)

改变样式，让段落的第一个字母浮动到左侧。

### 示例四：[创建一个没有表格的网页](https://www.runoob.com/try/try.php?filename=trycss_float6)

使用 float 创建一个网页页眉、页脚、左边的内容和主要内容。

### CSS 中所有的浮动属性

"CSS" 列中的数字表示不同的 CSS 版本（CSS1 或 CSS2）定义了该属性。

|属性|描述|值|CSS|
|:--|:--|:--|:--|
|[clear](https://www.runoob.com/cssref/pr-class-clear.html)|指定不允许元素周围有浮动元素。|left<br/>right<br/>both<br/>none<br/>inherit|1|
|[float](https://www.runoob.com/cssref/pr-class-float.html)|指定一个盒子（元素）是否可以浮动。|left<br/>right<br/>none<br/>inherit|1|

## CSS 布局 - 水平 & 垂直对齐

水平 & 垂直居中对齐

### 元素居中对齐

要水平居中对齐一个元素(如 \<div>), 可以使用`margin: auto;`。

设置到元素的宽度将防止它溢出到容器的边缘。

元素通过指定宽度，并将两边的空外边距平均分配：[示例](https://www.runoob.com/try/try.php?filename=trycss_align_container)

```html
<!DOCTYPE html>
<html>
	<head>
        <meta charset="utf-8"> 
        <title>菜鸟教程(runoob.com)</title> 
        <style>
            .center {
                margin: auto;
                width: 60%;
                border: 3px solid #73AD21;
                padding: 10px;
            }
        </style>
	</head>
	<body>
        <h2>元素居中对齐</h2>
        <p>水平居中块级元素 (如 div), 可以使用 margin: auto;</p>
        <div class="center">
        <p><b>注意: </b>使用 margin:auto 无法兼容 IE8, 除非 !DOCTYPE 已经声明。</p>
        </div>
	</body>
</html>
```

### 文本居中对齐

如果仅仅是为了文本在元素内居中对齐，可以使用`text-align: center;`

[示例](https://www.runoob.com/try/try.php?filename=trycss_align_text)

```css
.center {
	text-align: center;
	border: 3px solid green;
}
```

提示: 更多文本对齐实例，请参阅 [CSS 文本](https://www.runoob.com/css/css-text.html) 章节。

### 图片居中对齐

要让图片居中对齐, 可以使用`margin: auto;` 并将它放到 块 元素中:

[示例](https://www.runoob.com/try/try.php?filename=trycss_align_image)

```css
img {
    display: block;
    margin: auto;
    width: 40%;
}
```

### 左右对齐 - 使用定位方式

我们可以使用 position: absolute; 属性来对齐元素:[示例](https://www.runoob.com/try/try.php?filename=trycss_align_pos)

```css
.right {
    position: absolute;
    right: 0px;
    width: 300px;
    border: 3px solid #73AD21;
    padding: 10px;
}
```

注释：绝对定位元素会被从正常流中删除，并且能够交叠元素。

提示: 当使用 position 来对齐元素时, 通常 \<body> 元素会设置 margin 和 padding 。 这样可以避免在不同的浏览器中出现可见的差异。

当使用 position 属性时，IE8 以及更早的版本存在一个问题。如果容器元素（在我们的案例中是 \<div class="container">）设置了指定的宽度，并且省略了 !DOCTYPE 声明，那么 IE8 以及更早的版本会在右侧增加 17px 的外边距。这似乎是为滚动条预留的空间。当使用 position 属性时，请始终设置 !DOCTYPE 声明：