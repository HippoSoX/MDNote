# JavaScript

JavaScript 是 Web 的编程语言。

所有现代的 HTML 页面都使用 JavaScript。

JavaScript 非常容易学。

本教程将教你学习从初级到高级JavaScript知识。

## 简单示例

<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>菜鸟教程(runoob.com)</title>
		<script>
		function displayDate(){
			document.getElementById("demo").innerHTML=Date();
		}
		</script>
	</head>
	<body>
		<h1>我的第一个 JavaScript 程序</h1>
		<p id="demo">这是一个段落</p>
		<button type="button" onclick="displayDate()">显示日期</button>
	</body>
</html>

## JavaScript 简介

JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。

### JavaScript 是脚本语言

JavaScript 是一种轻量级的编程语言。

JavaScript 是可插入 HTML 页面的编程代码。

JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行。

JavaScript 很容易学习。

## JavaScript 用法

HTML 中的脚本必须位于 \<script> 与 \</script> 标签之间。

脚本可被放置在 HTML 页面的 \<body> 和 \<head> 部分中。

### \<script> 标签

如需在 HTML 页面中插入 JavaScript，请使用 \<script> 标签。

\<script> 和 \</script> 会告诉 JavaScript 在何处开始和结束。

\<script> 和 \</script> 之间的代码行包含了 JavaScript:

```html
<script>
alert("我的第一个 JavaScript");
</script>
```
注：那些老旧的实例可能会在 \<script> 标签中使用 type="text/javascript"。现在已经不必这样做了。JavaScript 是所有现代浏览器以及 HTML5 中的默认脚本语言。

### \<body> 中的 JavaScript

在本例中，JavaScript 会在页面加载时向 HTML 的 \<body> 写文本：

```html
<!DOCTYPE html>
<html>
	<body>
		<script>
		document.write("<h1>这是一个标题</h1>");
		document.write("<p>这是一个段落</p>");
		</script>
	</body>
</html>
```

### JavaScript 函数和事件

上面例子中的 JavaScript 语句，会在页面加载时执行。

通常，我们需要在某个事件发生时执行代码，比如当用户点击按钮时。

如果我们把 JavaScript 代码放入函数中，就可以在事件发生时调用该函数。

您将在稍后的章节学到更多有关 JavaScript 函数和事件的知识。

### 在 \<head> 或者 \<body> 的JavaScript

您可以在 HTML 文档中放入不限数量的脚本。

脚本可位于 HTML 的 \<body> 或 \<head> 部分中，或者同时存在于两个部分中。

通常的做法是把函数放入 \<head> 部分中，或者放在页面底部。这样就可以把它们安置到同一处位置，不会干扰页面的内容。

### \<head> 中的 JavaScript 函数

在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 \<head> 部分。

该函数会在点击按钮时被调用：

```html
<!DOCTYPE html>
<html>
	<head>
		<script>
		function myFunction()
		{
			document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
		}
		</script>
	</head>
	<body>
		<h1>我的 Web 页面</h1>
		<p id="demo">一个段落</p>
		<button type="button" onclick="myFunction()">尝试一下</button>
	</body>
</html>
```

### \<body> 中的 JavaScript 函数

在本例中，我们把一个 JavaScript 函数放置到 HTML 页面的 \<body> 部分。

该函数会在点击按钮时被调用：

```html
<!DOCTYPE html>
<html>
	<body>
		<h1>我的 Web 页面</h1>
		<p id="demo">一个段落</p>
		<button type="button" onclick="myFunction()">尝试一下</button>
		<script>
		function myFunction()
		{
			document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
		}
		</script>
	</body>
</html>
```

### 外部的 JavaScript

也可以把脚本保存到外部文件中。外部文件通常包含被多个网页使用的代码。

外部 JavaScript 文件的文件扩展名是 .js。

如需使用外部文件，请在 \<script> 标签的 "src" 属性中设置该 .js 文件：

```html
<!DOCTYPE html>
<html>
	<body>
		<script src="myScript.js"></script>
	</body>
</html>
```

你可以将脚本放置于 \<head> 或者 \<body>中，放在 \<script> 标签中的脚本与外部引用的脚本运行效果完全一致。

myScript.js 文件代码如下：

```Javascript
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
```

### tips

1、在标签中填写 onclick 事件调用函数时，不是 onclick=函数名， 而是 onclick=函数名+()，代码如下：

```html
		<script> 
		function myfunction(){
			document.getElementById("demo").innerHTML="onclick事件触发";
		}
		</script>
	</head>
	<body>
		<h1 id="demo">一个段落</h1>
		<button onclick="myfunction()" type="button">点击这里</button>
	</body>
```

2、外部 javascript 文件不使用 \<script> 标签，直接写 javascript 代码。

3、HTML 输出流中使用 document.write，相当于添加在原有html代码中添加一串html代码。而如果在文档加载后使用（如使用函数），会覆盖整个文档。

使用函数来执行document.write代码如下：

```html
<script>
	function myfunction(){
    	document.write("使用函数来执行doucment.write，即在文档加载后再执行这个操作，会实现文档覆盖");
	}
	document.write("<h1>这是一个标题</h1>");
	document.write("<p>这是一个段落。</p>");
</script>
<p >
	您只能在 HTML 输出流中使用 <strong>document.write</strong>。
	如果您在文档已加载后使用它（比如在函数中），会覆盖整个文档。
</p>
<button type="button" onclick="myfunction()">点击这里</button>
```

## JavaScript 输出

JavaScript 没有任何打印或者输出的函数。

### JavaScript 显示数据

JavaScript 可以通过不同的方式来输出数据：

+ 使用 window.alert() 弹出警告框。
+ 使用 document.write() 方法将内容写到 HTML 文档中。
+ 使用 innerHTML 写入到 HTML 元素。
+ 使用 console.log() 写入到浏览器的控制台。

### 使用 window.alert()

你可以弹出警告框来显示数据：

```html
<!DOCTYPE html>
<html>
	<body>
		<h1>我的第一个页面</h1>
		<p>我的第一个段落。</p>
		<script>
			window.alert(5 + 6);
		</script>
	</body>
</html>
```

### 操作 HTML 元素

如需从 JavaScript 访问某个 HTML 元素，您可以使用 `document.getElementById(id) `方法。

请使用 "id" 属性来标识 HTML 元素，并 innerHTML 来获取或插入元素内容：
```html
<!DOCTYPE html>
<html>
	<body>
		<h1>我的第一个 Web 页面</h1>
		<p id="demo">我的第一个段落</p>
		<script>
			document.getElementById("demo").innerHTML = "段落已修改。";
		</script>
	</body>
</html>
```

以上 JavaScript 语句（在 \<script> 标签中）可以在 web 浏览器中执行：

`document.getElementById("demo")`是使用 id 属性来查找 HTML 元素的 JavaScript 代码 。

`innerHTML = "段落已修改。"`是用于修改元素的 HTML 内容(innerHTML)的 JavaScript 代码。

### 在本教程中

在大多数情况下，在本教程中，我们将使用上面描述的方法来输出：

上面的例子直接把 id="demo" 的 \<p> 元素写到 HTML 文档输出中：

### 写到 HTML 文档

出于测试目的，您可以将JavaScript直接写在HTML 文档中：

```html
<!DOCTYPE html>
<html>
	<body>
		<h1>我的第一个 Web 页面</h1>
		<p>我的第一个段落。</p>
		<script>
			document.write(Date());
		</script>
	</body>
</html>
```

**请使用 document.write() 仅仅向文档输出写内容。**

**如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖。**

```html
<!DOCTYPE html>
<html>
	<body>
		<h1>我的第一个 Web 页面</h1>
		<p>我的第一个段落。</p>
		<button onclick="myFunction()">点我</button>
		<script>
			function myFunction() {
				document.write(Date());
			}
		</script>
		<!点击按钮后执行document.write()函数时将会覆盖整个页面>
	</body>
</html>
```

### 写到控制台

如果您的浏览器支持调试，你可以使用 console.log() 方法在浏览器中显示 JavaScript 值。

浏览器中使用 F12 来启用调试模式， 在调试窗口中点击 "Console" 菜单。

```html
<!DOCTYPE html>
<html>
	<body>
		<h1>我的第一个 Web 页面</h1>
		<script>
			a = 5;
			b = 6;
			c = a + b;
			console.log(c);
		</script>
	</body>
</html>
```

## JavaScript 语法

JavaScript 是一个程序语言。语法规则定义了语言结构。

### JavaScript 语法

JavaScript 是一个脚本语言。

它是一个轻量级，但功能强大的编程语言。

### JavaScript 字面量

在编程语言中，一般固定值称为字面量，如 3.14。

数字（Number）字面量 可以是整数或者是小数，或者是科学计数(e)。

字符串（String）字面量 可以使用单引号或双引号。

```js
"John Doe";
'John Doe';
```

表达式字面量 用于计算：

数组（Array）字面量 定义一个数组。

对象（Object）字面量 定义一个对象。

```js
{firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

函数（Function）字面量 定义一个函数。

```js
function myFunction(a, b) { 
	return a * b;
}
```

### JavaScript 变量

在编程语言中，变量用于存储数据值。

JavaScript 使用关键字 var 来定义变量， 使用等号来为变量赋值：

```js
var x, length;
x = 5;
length = 6;
```

变量可以通过变量名访问。在指令式语言中，变量通常是可变的。字面量是一个恒定的值。

变量是一个名称。字面量是一个值。

### JavaScript 操作符

JavaScript使用 算术运算符 来计算值。

JavaScript使用赋值运算符给变量赋值。

JavaScript语言有多种类型的运算符：

|类型|实例|描述|
|--|--|--|
|赋值，算术和位运算符|=  +  -  *  /|在 JS 运算符中描述|
|条件，比较及逻辑运算符|==  != <  > |在 JS 比较运算符中描述|

### JavaScript 语句

在 HTML 中，JavaScript 语句向浏览器发出的命令。

语句是用分号分隔：

```js
x = 5 + 6;
y = x * 10;
```

### JavaScript 关键字

JavaScript 关键字用于标识要执行的操作。

和其他任何编程语言一样，JavaScript 保留了一些关键字为自己所用。

var 关键字告诉浏览器创建一个新的变量：

```js
var x = 5 + 6;
var y = x * 10;
```

JavaScript 同样保留了一些关键字，这些关键字在当前的语言版本中并没有使用，但在以后 JavaScript 扩展中会用到。

以下是 JavaScript 中最重要的保留字（按字母顺序）：
|||||
| -------- | ---------- | ---------- | ------------ |
| abstract | else       | instanceof | super        |
| boolean  | enum       | int        | switch       |
| break    | export     | interface  | synchronized |
| byte     | extends    | let        | this         |
| case     | false      | long       | throw        |
| catch    | final      | native     | throws       |
| char     | finally    | new        | transient    |
| class    | float      | null       | true         |
| const    | for        | package    | try          |
| continue | function   | private    | typeof       |
| debugger | goto       | protected  | var          |
| default  | if         | public     | void         |
| delete   | implements | return     | volatile     |
| do       | import     | short      | while        |
| double   | in         | static     | with         |

### JavaScript 注释
不是所有的 JavaScript 语句都是"命令"。双斜杠 // 后的内容将会被浏览器忽略：

```js
// 我不会执行
```

### JavaScript 数据类型

JavaScript 有多种数据类型：数字，字符串，数组，对象等等：
```js
var length = 16;                                // Number 通过数字字面量赋值
var points = x * 10;                            // Number 通过表达式字面量赋值
var lastName = "Johnson";                       // String 通过字符串字面量赋值
var cars = ["Saab", "Volvo", "BMW"];            // Array  通过数组字面量赋值
var person = {firstName:"John", lastName:"Doe"};// Object 通过对象字面量赋值
```

### 数据类型的概念

编程语言中，数据类型是一个非常重要的内容。

为了可以操作变量，了解数据类型的概念非常重要。

如果没有使用数据类型，以下实例将无法执行：

```js
16 + "Volvo"
```

16 加上 "Volvo" 是如何计算呢? 以上会产生一个错误还是输出以下结果呢？

```js
"16Volvo"
```

你可以在浏览器尝试执行以上代码查看效果。

在接下来的章节中你将学到更多关于数据类型的知识。

### JavaScript 函数

JavaScript 语句可以写在函数内，函数可以重复引用：

引用一个函数 = 调用函数(执行函数内的语句)。

```js
function myFunction(a, b) {
	return a * b;                                // 返回 a 乘以 b 的结果
}
```

### JavaScript 字母大小写

JavaScript 对大小写是敏感的。

当编写 JavaScript 语句时，请留意是否关闭大小写切换键。

函数 getElementById 与 getElementbyID 是不同的。

同样，变量 myVariable 与 MyVariable 也是不同的。

### JavaScript 字符集

JavaScript 使用 Unicode 字符集。

Unicode 覆盖了所有的字符，包含标点等字符。

JavaScript 中，常见的是驼峰法的命名规则，如 lastName (而不是lastname)。

### 三种变量命名规则：

```js
var firstName='king';//小驼峰
var FirstName='queen';//大驼峰
var first_name='maizi';//下划线法
```

### 判断数据类型

JavaScript是弱类型编程语言,定义变量都使用 var 定义,与 Java 这种强类型语言有区别.

在定义后可以通过 typeof() 来获取JavaScript中变量的数据类型.

// Number 通过数字字面量赋值 
// Number 通过表达式字面量赋值
// String 通过字符串字面量赋值
// Array  通过数组字面量赋值 
// Object 通过对象字面量赋值

有个情况需要特别注意: **typeof 不能用来判断是 Array 还是Object**

```js
var arr = [] typeof(arr) === 'object' // true
```
结果为 true。

当然你可以使用其他方式来判断：

1、使用 isArray 方法

```js
var cars=new Array();
cars[0]="Saab";
cars[1]="Volvo";
cars[2]="BMW";
// 判断是否支持该方法
if (Array.isArray) {
	if(Array.isArray(cars)) {
		document.write("该对象是一个数组。") ;
	}
}
```

2、使用 instanceof 操作符

```js
var cars=new Array();
cars[0]="Saab";
cars[1]="Volvo";
cars[2]="BMW";

if (cars instanceof Array) {
	document.write("该对象是一个数组。") ;
}
```
更多内容可以参考：

-  [JavaScript 判断对象是否为数组](https://www.runoob.com/note/26685)
-  [JavaScript 判断该对象是否为数组](https://www.runoob.com/w3cnote/javascript-check-arrayisobject.html)

## JavaScript 语句

JavaScript 语句向浏览器发出的命令。语句的作用是告诉浏览器该做什么。

### JavaScript 语句

JavaScript 语句是发给浏览器的命令。

这些命令的作用是告诉浏览器要做的事情。

下面的 JavaScript 语句向 id="demo" 的 HTML 元素输出文本 "你好 Dolly" ：

```js
document.getElementById("demo").innerHTML = "你好 Dolly";
```

### 分号 ;

分号用于分隔 JavaScript 语句。

通常我们在每条可执行的语句结尾添加分号。

使用分号的另一用处是在一行中编写多条语句。

您也可能看到不带有分号的案例。

**在 JavaScript 中，用分号来结束语句是可选的。**

### JavaScript 代码

JavaScript 代码是 JavaScript 语句的序列。

浏览器按照编写顺序依次执行每条语句。

本例向网页输出一个标题和两个段落：

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<h1>我的 Web 页面</h1>
		<p id="demo">一个段落。</p>
		<div id="myDIV">一个 DIV。</div>
		<script>
			document.getElementById("demo").innerHTML="你好 Dolly";
			document.getElementById("myDIV").innerHTML="你最近怎么样?";
		</script>
	</body>
</html>

### JavaScript 代码块

JavaScript 可以分批地组合起来。

代码块以左花括号开始，以右花括号结束。

代码块的作用是一并地执行语句序列。

本例向网页输出一个标题和两个段落：

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<h1>我的 Web 页面</h1>
		<p id="myPar">我是一个段落。</p>
		<div id="myDiv">我是一个div。</div>
		<p>
		<button type="button" onclick="myFunction()">点击这里</button>
		</p>
		<script>
			function myFunction(){
				document.getElementById("myPar").innerHTML="你好世界！";
				document.getElementById("myDiv").innerHTML="你最近怎么样?";
			}
		</script>
		<p>当您点击上面的按钮时，两个元素会改变。</p>
	</body>
</html>

### JavaScript 语句标识符

JavaScript 语句通常以一个 语句标识符 为开始，并执行该语句。

语句标识符是保留关键字不能作为变量名使用。

下表列出了 JavaScript 语句标识符 (关键字) ：

|语句|描述|
|--|--|
|break|用于跳出循环。|
|catch|语句块，在 try 语句块执行出错时执行 catch 语句块。|
|continue|跳过循环中的一个迭代。|
|do ... while|执行一个语句块，在条件语句为 true 时继续执行该语句块。|
|for|在条件语句为 true 时，可以将代码块执行指定的次数。|
|for ... in|用于遍历数组或者对象的属性（对数组或者对象的属性进行循环操作）。|
|function|定义一个函数|
|if ... else|用于基于不同的条件来执行不同的动作。|
|return|退出函数|
|switch|用于基于不同的条件来执行不同的动作。|
|throw|抛出（生成）错误 。|
|try|实现错误处理，与 catch 一同使用。|
|var|声明一个变量。|
|while|当条件语句为 true 时，执行语句块。|

### 空格

JavaScript 会忽略多余的空格。您可以向脚本添加空格，来提高其可读性。下面的两行代码是等效的：

```js
var person="Hege";
var person = "Hege";
```

### 对代码行进行折行

您可以在文本字符串中使用反斜杠对代码行进行换行。下面的例子会正确地显示：
```js
document.write("你好 \
世界!");
```
不过，您不能像这样折行：
```js
document.write \
("你好世界!");
```

## JavaScript 注释

JavaScript 注释可用于提高代码的可读性。

### JavaScript单行注释
JavaScript 不会执行注释。

我们可以添加注释来对 JavaScript 进行解释，或者提高代码的可读性。

单行注释以 // 开头。

### JavaScript 多行注释
多行注释以 /\* 开始，以 \*/ 结尾。

### 应用注释符号验证浏览器是否支持 JavaScript 脚本功能

如果用户不能确定浏览器是否支持JavaScript脚本，那么可以应用HTML提供的注释符号进行验证。HTML注释符号是以 <-- 开始以 --> 结束的。如果在此注释符号内编写 JavaScrip t脚本，对于不支持 JavaScript 的浏览器，将会把编写的 JavaScript 脚本作为注释处理。

使用 JavaScript 脚本在页面中输出一个字符串，将 JavaScript 脚本编写在 HTML 注释中，如果浏览器支持 JavaScript 将输出此字符串，如果不支持将不输出此字符串，代码如下:

```html
<script>
<!--
document.write("您的浏览器支持JavaScript脚本!");
//-->
</script>
注意：注释行结尾处的两条斜杠 // 是 JavaScript 注释符号。这可以避免 JavaScript 执行 --> 标签。
```

## JavaScript 变量

变量是用于存储信息的"容器"。

```html
<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<script>
			var x=5;
			var y=6;
			var z=x+y;
			document.write(x + "<br>");
			document.write(y + "<br>");
			document.write(z + "<br>");
		</script>
	</body>
</html>
```

### 就像代数那样

x=5
y=6
z=x+y

在代数中，我们使用字母（比如 x）来保存值（比如 5）。

通过上面的表达式 z=x+y，我们能够计算出 z 的值为 11。

在 JavaScript 中，这些字母被称为变量。

您可以把变量看做存储数据的容器。

### JavaScript 变量

与代数一样，JavaScript 变量可用于存放值（比如 x=5）和表达式（比如 z=x+y）。

变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

+ 变量必须以字母开头
+ 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
+ 变量名称对大小写敏感（y 和 Y 是不同的变量）

JavaScript 语句和 JavaScript 变量都对大小写敏感。

### JavaScript 数据类型

JavaScript 变量还能保存其他数据类型，比如文本值 (name="Bill Gates")。

在 JavaScript 中，类似 "Bill Gates" 这样一条文本被称为字符串。

JavaScript 变量有很多种类型，但是现在，我们只关注数字和字符串。

**当您向变量分配文本值时，应该用双引号或单引号包围这个值。**

**当您向变量赋的值是数值时，不要使用引号。如果您用引号包围数值，该值会被作为文本来处理。**

### 声明（创建） JavaScript 变量

在 JavaScript 中创建变量通常称为"声明"变量。

我们使用 var 关键词来声明变量：
```js
var carname;
```

变量声明之后，该变量是空的（它没有值）。

如需向变量赋值，请使用等号：
```js
carname="Volvo";
```

不过，您也可以在声明变量时对其赋值：
```js
var carname="Volvo";
```

### 一条语句，多个变量

您可以在一条语句中声明很多变量。该语句以 var 开头，并使用逗号分隔变量即可：
```js
var lastname="Doe", age=30, job="carpenter";
```

声明也可横跨多行：
```js
var lastname="Doe",
age=30,
job="carpenter";
```

一条语句中声明的多个不可以赋同一个值:
```js
var x,y,z=1;
```
x,y 为 undefined， z 为 1。

### Value = undefined

在计算机程序中，经常会声明无值的变量。未使用值来声明的变量，其值实际上是 undefined。

在执行过以下语句后，变量 carname 的值将是 undefined：
```js
var carname;
```

### 重新声明 JavaScript 变量

如果重新声明 JavaScript 变量，该变量的值不会丢失：

在以下两条语句执行后，变量 carname 的值依然是 "Volvo"：

var carname="Volvo";
var carname;

### let变量

介绍JS中的let变量:

let var1\[= value1]\[, var2\[= value2]] [, ..., varN [= valueN]];
let允许你声明一个作用域被限制在块级中的变量、语句或者表达式。在Function中局部变量推荐使用let变量，避免变量名冲突。

### 作用域规则

let 声明的变量只在其声明的块或子块中可用，这一点，与var相似。二者之间最主要的区别在于var声明的变量的作用域是整个封闭函数。

```js
function varTest() {
    var x = 1;
    if (true) {
        var x = 2;       // 同样的变量!
        console.log(x);  // 2
    }
    console.log(x);  // 2
}

function letTest() {
    let x = 1;
    if (true) {
        let x = 2;       // 不同的变量    
        console.log(x);  // 2  
    }
    console.log(x);  // 1
}
```
### 不使用var

Javascript声明变量的时候，虽然用var关键字声明和不用关键字声明，很多时候运行并没有问题，但是这两种方式还是有区别的。可以正常运行的代码并不代表是合适的代码。

```js
// num1为全局变量，num2为window的一个属性
var num1 = 1;
num2 = 2;
// delete num1;  无法删除
// delete num2;  删除
function model(){
var num1 = 1; // 本地变量
num2 = 2;     // window的属性
    // 匿名函数
    (function(){
        var num = 1; // 本地变量
        num1 = 2; // 继承作用域（闭包）
        num3 = 3; // window的属性
    }())
}
```

### const

const 关键字用来声明 JavaScript中的常量（与变量相对，不可修改，但同样是用于存储信息的"容器"。），常量的值不能通过重新赋值来改变，并且不能重新声明。

代码：
```js
//定义常量a并赋值为0
const a = 0;

//报错（不能重新赋值）
a = 1;

//报错（不能重新声明）
const a = 2;

//输出0
console.log("a is: " + a);
```
### 重复声明变量

JavaScript 允许重复声明变量，后声明的覆盖之前的

```js
var a = 1;
var a = 'x';
console.log(a);
// 输出 'x'
```

楼上有句话是觉得欠妥当的 —— “JavaScript 允许重复声明变量，后声明的覆盖之前的”。

JavaScript 允许变量被重复声明，在声明变量时 JavaScript 会自行判断这个变量是否已经被声明了，如果已经被声明（即已经存在），那么重复声明（即除了变量的非首次声明）会被跳过，不再执行声明的操作。

JavaScript 变量的值是可以被重复赋值的，最后的赋值是这个变量最后的结果。

```js
var a=1;
var a=2;

//赋值覆盖相当于：
var a;
//a=1;
a=2;

//声明覆盖相当于：
//var a=1;
var a=2;
```

这个笔记所说的覆盖，其实是赋值的覆盖。如果说后声明的会覆盖已声明的，那么后声明的应该是 undefined 而不是第一次声明时候的赋值，也就是说如果是声明覆盖的话，相当于没有 var a=1 那么一个只有声明没有赋值的变量，它的值就是 undefined。

我们如何验证这个覆盖是声明的覆盖还是赋值的覆盖呢？看下面的代码：

```js
var a=1;
var a;

//赋值覆盖相当于：
var a;
//a=1;
a;

//声明覆盖相当于：
//var a=1;
var a;
```
我们再输出a的值，验证下是 undefined 还是 1 就知道了。

console.log(a);

### 重复定义函数

JavaScript 允许重复定义函数

JavaScript **没有重载**这个概念，它仅依据函数名来区分函数。

后定义的同名函数覆盖之前的，与参数无关。

```js
function test() {
    console.log("test");
}
test();     //输出 "test arg0 + undefined"

function test(arg1) {
    console.log("test arg" + arguments.length + " + " + arg1);
}
test(1,2);  //输出 "test arg2 + 1"
```

实参个数如果比形参少，那么剩下的默认赋值为 undefined，如果实参传的比形参数量多，那么是全部都会被传进去的，只不过没有对应的形参可以引用（但可以用 arguments 来获取剩下的参数）。

```js
function test(arg1) {
    for(var i=0; i<arguments.length; i++) {
        console.log(arguments[i]);
    }
}
test(1,2); //输出 1 2
```

### 变量与函数重名

**变量与函数重名的时候，变量生效**

这涉及到了变量和函数的预解析：

变量声明会被顶置，函数声明也会被顶置且比变量更先声明。

变量的声明和赋值语句一起写时，JS引擎在解析时，会将其拆成声明和赋值2部分，声明置顶，赋值保留在原来位置。

声明过的变量不会再重复声明。

```js
var a = 100;
function a() {
    return "function";
}
console.log(a);     //输出 100
console.log(a());   
/*
报错
Uncaught TypeError: a is not a function
    (anonymous function) @test.html:9
*/
```
JS 中有两种函数，一种是普通函数，一种是函数对象。下面的这种就是“函数对象”，它实际上是声明一个匿名函数，然后将该函数的 init 方法赋值给该变量。
```js
var a = 100;
var a = function() {
    return "function";
}
console.log(a);
/* 
输出
function() {
    return "function";
}
*/
console.log(a());   //输出 "function"
```

### 函数与内部变量重名

定义普通函数，即在 window 变量下，定义一个 key，它的名字为该函数名，值为该函数的地址。函数内部的 this 指向 window 对象。

```js
function a() {
    console.log(this);  //输出 window{...}
    this.a = 1;         //即 window.a = 1，此时window下的function a已经被该变量覆盖了。
    var a = 5;          //下面的这几个变量都是局部变量，仅在花括号范围内有效。  
    a = 10;
    var v = "value"
    return "function";
}
console.log(a);         //输出 function a {...}
console.log(a());       //输出 "function"
console.log(a);         //输出 1
console.log(v);
/*
输出
Uncaught ReferenceError: v is not defined
    (anonymous function) @ mycolor.html:15
*/
```

## JavaScript 数据类型

值类型(基本类型)：字符串（String）、数字(Number)、布尔(Boolean)、对空（Null）、未定义（Undefined）、Symbol。

引用数据类型：对象(Object)、数组(Array)、函数(Function)。

注：Symbol 是 ES6 引入了一种新的原始数据类型，表示独一无二的值。

### JavaScript 拥有动态类型

JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型：

```js
var x;               // x 为 undefined
var x = 5;           // 现在 x 为数字
var x = "John";      // 现在 x 为字符串
```

### JavaScript 字符串

字符串是存储字符（比如 "Bill Gates"）的变量。

字符串可以是引号中的任意文本。您可以使用单引号或双引号：

```js
var carname="Volvo XC60";
var carname='Volvo XC60';
```

您可以在字符串中使用引号，只要不匹配包围字符串的引号即可：

```js
var answer="It's alright";
var answer="He is called 'Johnny'";
var answer='He is called "Johnny"';
```

### JavaScript 数字

JavaScript 只有一种数字类型。数字可以带小数点，也可以不带：

```js
var x1=34.00;      //使用小数点来写
var x2=34;         //不使用小数点来写
```

极大或极小的数字可以通过科学（指数）计数法来书写：

```js
var y=123e5;      // 12300000
var z=123e-5;     // 0.00123
```

### JavaScript 布尔

布尔（逻辑）只能有两个值：true 或 false。

```js
var x=true;
var y=false;
```

### JavaScript 数组

下面的代码创建名为 cars 的数组：

```js
var cars=new Array();
cars[0]="Saab";
cars[1]="Volvo";
cars[2]="BMW";
```
或者 (condensed array):

```js
var cars=new Array("Saab","Volvo","BMW");
```
或者 (literal array):

```js
var cars=["Saab","Volvo","BMW"];
```

数组下标是基于零的，所以第一个项目是 [0]，第二个是 [1]，以此类推。

数组有四种方式：
```js
var arr1 = new Array('a', 'b', 'c');    //这是一个预定义的数组，在创建时初始化
var arr2 = ['a', 'b', 'c' ];       //同样是在创建时初始化，但是这种创建更为简洁直观
var arr3 = new Array( );   var arr4 = [ ];     //这两种是创建空的数组
```
在数组操作中，最值得注意的是下标的使用，容易出错

对象的创建，一般推荐使用

```js
var people = {name : 'Tom', age : 21 , eat : function(){  }    }
```

也可先创建对象再追加属性和方法

```js
var people = new Object();
people.name = 'Tom';   
people.age = 21;  
people.eat = function(){  }
```

### JavaScript 对象

对象由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔：

```js
var person={firstname:"John", lastname:"Doe", id:5566};
```

上面例子中的对象 (person) 有三个属性：firstname、lastname 以及 id。

空格和折行无关紧要。声明可横跨多行：

```js
var person={
firstname : "John",
lastname  : "Doe",
id        :  5566
};
```

对象属性有两种寻址方式：

```js
name=person.lastname;
name=person["lastname"];
```

最常用的对象创建方式:

第一种：

```js
function Demo(){
    var obj=new Object();
    obj.name="张思";
    obj.age=12;
    obj.firstF=function(){
    }
    obj.secondF=function(){
    }
    return obj;
}

var one=Demo();
// 调用输出
document.write(one.age);
```

第二种：

```js
function Demo(){
    this.name="张思";
    this.age=12;
    this.firstF=function(){
    }
    this.secondF=function(){
    }
}

var one=new Demo

// 调用输出
document.write(one.age);
```

### Undefined 和 Null

Undefined 这个值表示变量不含有值。

可以通过将变量的值设置为 null 来清空变量。

```js
cars=null;
person=null;
```

注意 undefined 和 null 都是小写，并且。

```js
var x,y;
if(x == null){
    document.write(x);
}
if(y == undefined){
    document.write(y);
}
```

二者都会输出 undefined

### 声明变量类型

当您声明新变量时，可以使用关键词 "new" 来声明其类型：

```js
var carname=new String;
var x=      new Number;
var y=      new Boolean;
var cars=   new Array;
var person= new Object;
```

### 数字与字符串间的转换

利用 toString() 方法可以把数值转换为字符串。

```html
<script>
var a=100;
var c=a.toString();
alert(typeof(c));      //typeof()方法验证转换后的数据类型
</script>
```

使用 parseInt() 和 parseFloat() 方法可以把字符串转换为数值。

```html
<script>
var str="123.30";
var a=parseInt(str);    //parseInt()方法把字符串转换为整数，parseFloat()方法把字符串转换为浮点数
var b=parseFloat(str);
</script>
```

要把任何值转换为布尔型数据，在值的前面增加两个`!!` 感叹号即可，`!!0` 为** False**，其余的均为 **True**。

## JavaScript 对象

JavaScript 对象是拥有属性和方法的数据。

### JavaScript 对象

在 JavaScript中，几乎所有的事物都是对象。

**在 JavaScript 中，对象是非常重要的，当你理解了对象，就可以了解 JavaScript 。**

你已经学习了 JavaScript 变量的赋值。

以下代码为变量 car 设置值为 "Fiat" :

```js
var car = "Fiat";
```

对象也是一个变量，但对象可以包含多个值（多个变量）。
```js
var car = {type:"Fiat", model:500, color:"white"};
```

在以上实例中，3 个值 ("Fiat", 500, "white") 赋予变量 car。

在以上实例中，3 个变量 (type, model, color) 赋予变量 car。

**JavaScript 对象是变量的容器。**

### 对象定义

你可以使用字符来定义和创建 JavaScript 对象:

<!DOCTYPE html>
<html>
	<head> 
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>创建 JavaScript 对象。</p>
		<p id="demo"></p>
		<script>
			var person = {
				firstName : "John",
				lastName  : "Doe",
				age       : 50,
				eyeColor  : "blue"
			};
			document.getElementById("demo").innerHTML =
			person.firstName + " 现在 " + person.age + " 岁。";
		</script>
	</body>
</html>

### 对象属性

可以说 "JavaScript 对象是变量的容器"。

但是，我们通常认为 "JavaScript 对象是键值对的容器"。

键值对通常写法为 name : value (键与值以冒号分割)。

键值对在 JavaScript 对象通常称为 对象属性。

**JavaScript 对象是属性变量的容器。**

对象键值对的写法类似于：

+ PHP 中的关联数组
+ Python 中的字典
+ C 语言中的哈希表
+ Java 中的哈希映射
+ Ruby 和 Perl 中的哈希表

### 访问对象属性

你可以通过两种方式访问对象属性:

```js
person.lastName;
person["lastName"];
```

### 对象方法

对象的方法定义了一个函数，并作为对象的属性存储。

对象方法通过添加 () 调用 (作为一个函数)。

该实例访问了 person 对象的 fullName() 方法:

```js
name = person.fullName();
//如果你要访问 person 对象的 fullName 属性，它将作为一个定义函数的字符串返回：
name = person.fullName;
```
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8"> 
		<title>菜鸟教程(runoob.com)</title> 
	</head>
	<body>
		<p>创建和使用对象方法。</p>
		<p>对象方法是一个函数定义,并作为一个属性值存储。</p>
		<p id="demo1"></p>
		<p id="demo2"></p>
		<script>
			var person = {
				firstName: "John",
				lastName : "Doe",
				id : 5566,
				fullName : function() 
				{
					return this.firstName + " " + this.lastName;
				}
			};
			document.getElementById("demo1").innerHTML = "不加括号输出函数表达式："  + person.fullName;
			document.getElementById("demo2").innerHTML = "加括号输出函数执行结果："  +  person.fullName();
		</script>
	</body>
</html>
```

输出结果

>创建和使用对象方法。
>对象方法是一个函数定义,并作为一个属性值存储。
>不加括号输出函数表达式：function() { return this.firstName + " " + this.lastName; }
>加括号输出函数执行结果：John Doe

**JavaScript 对象是属性和方法的容器。**

### 访问对象方法

你可以使用以下语法创建对象方法：

```js
methodName : function() { code lines }
```

你可以使用以下语法访问对象方法：

```js
objectName.methodName()
```

通常 fullName() 是作为 person 对象的一个方法， fullName 是作为一个属性。

有多种方式可以创建，使用和修改 JavaScript 对象。

同样也有多种方式用来创建，使用和修改属性和方法。

### 逗号,

JavaScript对象:属性和方法的容器;

对象的属性之间一定要用逗号隔开;

对象的方法定义了一个函数，并作为对象的属性存储。

对象方法通过添加 () 调用 (作为一个函数)。

比如:

```js
var person={
"name":"小明",
"age":"18",
"like":function(){
            return "喜欢打篮球,弹吉他";
      }
}
```

### 先创建再添加属性和属性值

javaScript对象也可以先创建，再添加属性和属性值，比如：

```js
var person=new Object();
person.name='小明'；
person.sex='男'；
person.method=function(){
  return this.name+this.sex;
}
```

### 属性的唯一性

javaScript对象中属性具有唯一性（这里的属性包括方法），如果有两个重复的属性，则以最后赋值为准。比如同时存在两个play:

```js
var person = {
    name: "小明",
    age: 18,
    sex: "男",
    play: "football",
    play: function () {
        return "like paly football";
    }
};
```

### 键值

JavaScript 对象是键值对的容器，“键”必须为字符串，“值”可以是 JavaScript 中除 null 和 undefined 以外的任意数据类型。

代码实例：

```js
var bird = {
    "name" : "Amy",
    "age" : 1,
    "color" : "white",
    "skill" : function () {
        console.log("Fly");
    },
    "nickname" : null //非法
}
```

## JavaScript 函数

函数是由事件驱动的或者当它被调用时执行的可重复使用的代码块。

### JavaScript 函数语法

函数就是包裹在花括号中的代码块，前面使用了关键词 function：

```js
function functionname()
{
    // 执行代码
}
```
当调用该函数时，会执行函数内的代码。

可以在某事件发生时直接调用函数（比如当用户点击按钮时），并且可由 JavaScript 在任何位置进行调用。

**JavaScript 对大小写敏感。关键词 function 必须是小写的，并且必须以与函数名称相同的大小写来调用函数。**

### 调用带参数的函数
在调用函数时，您可以向其传递值，这些值被称为参数。

这些参数可以在函数中使用。

您可以发送任意多的参数，由逗号 (,) 分隔：
```js
myFunction(argument1,argument2)
```
当您声明函数时，请把参数作为变量来声明：
```js
function myFunction(var1,var2)
{
代码
}
```
变量和参数必须以一致的顺序出现。第一个变量就是第一个被传递的参数的给定的值，以此类推。

### 带有返回值的函数

有时，我们会希望函数将值返回调用它的地方。

通过使用 return 语句就可以实现。

在使用 return 语句时，函数会停止执行，并返回指定的值。

语法
```js
function myFunction()
{
    var x=5;
    return x;
}
```
上面的函数会返回值 5。

注意： 整个 JavaScript 并不会停止执行，仅仅是函数。JavaScript 将继续执行代码，从调用函数的地方。

函数调用将被返回值取代：

```js
var myVar=myFunction();
```
myVar 变量的值是 5，也就是函数 "myFunction()" 所返回的值。

即使不把它保存为变量，您也可以使用返回值：
```js
document.getElementById("demo").innerHTML=myFunction();
```
"demo" 元素的 innerHTML 将成为 5，也就是函数 "myFunction()" 所返回的值。

您可以使返回值基于传递到函数中的参数：

```js
function myFunction(a,b)
{
    return a*b;
}
 
document.getElementById("demo").innerHTML=myFunction(4,3);

```
### 局部 JavaScript 变量

在 JavaScript 函数内部声明的变量（使用 var）是局部变量，所以只能在函数内部访问它。（该变量的作用域是局部的）。

您可以在不同的函数中使用名称相同的局部变量，因为只有声明过该变量的函数才能识别出该变量。

只要函数运行完毕，本地变量就会被删除。

### 全局 JavaScript 变量

在函数外声明的变量是全局变量，网页上的所有脚本和函数都能访问它。

### JavaScript 变量的生存期

JavaScript 变量的生命期从它们被声明的时间开始。

局部变量会在函数运行以后被删除。

全局变量会在页面关闭后被删除。

### 向未声明的 JavaScript 变量分配值

如果您把值赋给尚未声明的变量，该变量将被自动作为 window 的一个属性。

这条语句：

```js
carname="Volvo";
```

将声明 window 的一个属性 carname。

非严格模式下给未声明变量赋值创建的全局变量，是全局对象的可配置属性，可以删除。

```js
var var1 = 1; // 不可配置全局属性
var2 = 2; // 没有使用 var 声明，可配置全局属性

console.log(this.var1); // 1
console.log(window.var1); // 1

delete var1; // false 无法删除
console.log(var1); //1

delete var2; 
console.log(delete var2); // true
console.log(var2); // 已经删除 报错变量未定义
```

### JavaScript 多选框多选与取消多选实例：

```js
function checkboxed(objName){
    var objNameList=document.getElementsByName(objName);    

    if(null!=objNameList){
        alert("全选操作");
        for(var i=0;i<objNameList.length;i++){
            objNameList[i].checked="checked";
        }
    }
}

function uncheckboxed(objName){
    var objNameList=document.getElementsByName(objName);    

    if(null!=objNameList){
        alert("取消全选操作");
        for(var i=0;i<objNameList.length;i++){
            objNameList[i].checked="";
        }
    }
}
```


