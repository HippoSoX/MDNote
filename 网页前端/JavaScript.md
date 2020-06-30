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

## 示例

### 示例一：[简单的计算器](https://c.runoob.com/codedemo/2815)

### 示例二：[最简单的模拟计算器](https://c.runoob.com/codedemo/3015)

### 示例三：[js模拟计算器](https://c.runoob.com/codedemo/4026)

### 示例四：[简单的计算器应用](https://c.runoob.com/codedemo/4721)

### 示例五：[js实现计算器](https://c.runoob.com/codedemo/3654)

### 示例六：[自制计算器](https://c.runoob.com/codedemo/4786)

### 示例七：[html css js计算器](https://c.runoob.com/codedemo/3124)

### 示例八：[计算器](https://c.runoob.com/codedemo/3880)

## JavaScript 作用域

作用域是可访问变量的集合。

### JavaScript 作用域

在 JavaScript 中, 对象和函数同样也是变量。

**在 JavaScript 中, 作用域为可访问变量，对象，函数的集合。**

JavaScript 函数作用域: 作用域在函数内修改。

### JavaScript 局部作用域

变量在函数内声明，变量为局部作用域。

局部变量：只能在函数内部访问。

因为局部变量只作用于函数内，所以不同的函数可以使用相同名称的变量。

局部变量在函数开始执行时创建，函数执行完后局部变量会自动销毁。

### JavaScript 全局变量

变量在函数外定义，即为全局变量。

全局变量有**全局作用域**: 网页中所有脚本和函数均可使用。 

如果变量在函数内没有声明（没有使用 var 关键字），该变量为全局变量。

### JavaScript 变量生命周期

JavaScript 变量生命周期在它声明时初始化。

局部变量在函数执行完毕后销毁。

全局变量在页面关闭后销毁。

### 函数参数

函数参数只在函数内起作用，是局部变量。

### HTML 中的全局变量

在 HTML 中, 全局变量是 window 对象: 所有数据变量都属于 window 对象。

### tips

你的全局变量，或者函数，可以覆盖 window 对象的变量或者函数。
局部变量，包括 window 对象可以覆盖全局变量和函数。

### ES6 中的 let 关键字

let 允许你声明一个作用域被限制在块级中的变量、语句或者表达式。与var关键字不同的是，它声明的变量只能是全局或者整个函数块的。

let 语法：

```js
let var1 [= value1] [, var2 [= value2]] [, ..., varN [= valueN]];
```

**let 声明的变量只在其声明的块或子块中可用**，这一点，与 var 相似。二者之间最主要的区别在于 **var 声明的变量的作用域是整个封闭函数**。

let 和 var 的区别代码实例：

```js
function varTest() {
  var x = 1;
  if (true) {
    var x = 2;  // 同样的变量!
    console.log(x);  // 2
  }
  console.log(x);  // 2
}

function letTest() {
  let x = 1;
  if (true) {
    let x = 2;  // 不同的变量
    console.log(x);  // 2
  }
  console.log(x);  // 1
}
```

### let 和 var的区别

#### 基本用法

ES6 新增了let命令，用来声明变量。它的用法类似于var，但是所声明的变量，只在let命令所在的代码块内有效。

```js
{
  let a = 10;
  var b = 1;
}

a // ReferenceError: a is not defined.
b // 1
```

上面代码在代码块之中，分别用let和var声明了两个变量。然后在代码块之外调用这两个变量，结果let声明的变量报错，var声明的变量返回了正确的值。这表明，let声明的变量只在它所在的代码块有效。

for循环的计数器，就很合适使用let命令。

```js
for (let i = 0; i < 10; i++) {
  // ...
}

console.log(i);
// ReferenceError: i is not defined
```

上面代码中，计数器i只在for循环体内有效，在循环体外引用就会报错。

下面的代码如果使用var，最后输出的是10。

```js
var a = [];
for (var i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6](); // 10
```

上面代码中，变量i是var命令声明的，在全局范围内都有效，所以全局只有一个变量i。每一次循环，变量i的值都会发生改变，而循环内被赋给数组a的函数内部的console.log(i)，里面的i指向的就是全局的i。也就是说，所有数组a的成员里面的i，指向的都是同一个i，导致运行时输出的是最后一轮的i的值，也就是 10。

如果使用let，声明的变量仅在块级作用域内有效，最后输出的是 6。

```js
var a = [];
for (let i = 0; i < 10; i++) {
  a[i] = function () {
    console.log(i);
  };
}
a[6](); // 6
```

上面代码中，变量i是let声明的，当前的i只在本轮循环有效，所以每一次循环的i其实都是一个新的变量，所以最后输出的是6。你可能会问，如果每一轮循环的变量i都是重新声明的，那它怎么知道上一轮循环的值，从而计算出本轮循环的值？这是因为 JavaScript 引擎内部会记住上一轮循环的值，初始化本轮的变量i时，就在上一轮循环的基础上进行计算。

另外，for循环还有一个特别之处，就是设置循环变量的那部分是一个父作用域，而循环体内部是一个单独的子作用域。

```js
for (let i = 0; i < 3; i++) {
  let i = 'abc';
  console.log(i);
}
// abc
// abc
// abc
```

上面代码正确运行，输出了 3 次abc。这表明**函数内部的变量i与循环变量i不在同一个作用域，有各自单独的作用域**。

## JavaScript 事件

HTML 事件是发生在 HTML 元素上的事情。

当在 HTML 页面中使用 JavaScript 时， JavaScript 可以触发这些事件。

### HTML 事件

HTML 事件可以是浏览器行为，也可以是用户行为。

以下是 HTML 事件的实例：

- HTML 页面完成加载
- HTML input 字段改变时
- HTML 按钮被点击

通常，当事件发生时，你可以做些事情。

在事件触发时 JavaScript 可以执行一些代码。

HTML 元素中可以添加事件属性，使用 JavaScript 代码来添加 HTML 元素。

```html
<some-HTML-element some-event='JavaScript 代码'><!--单引号-->
<some-HTML-element some-event="JavaScript 代码"><!--双引号-->
```

在以下实例中，按钮元素中添加了 onclick 属性 (并加上代码):

```html
<button onclick="getElementById('demo').innerHTML=Date()">现在的时间是?</button>
```

以上实例中，JavaScript 代码将修改 id="demo" 元素的内容。

在下一个实例中，代码将修改自身元素的内容 (使用 this.innerHTML):

```html
<button onclick="this.innerHTML=Date()">现在的时间是?</button>
```

*JavaScript代码通常是几行代码。比较常见的是通过事件属性来调用：*

```html
<button onclick="displayDate()">现在的时间是?</button>
```

### 常见的HTML事件

下面是一些常见的HTML事件的列表:

| 事件        | 描述                         |
| :---------- | :--------------------------- |
| onchange    | HTML 元素改变                |
| onclick     | 用户点击 HTML 元素           |
| onmouseover | 用户在一个HTML元素上移动鼠标 |
| onmouseout  | 用户从一个HTML元素上移开鼠标 |
| onkeydown   | 用户按下键盘按键             |
| onload      | 浏览器已完成页面的加载       |

## JavaScript 可以做什么?

事件可以用于处理表单验证，用户输入，用户行为及浏览器动作:

- 页面加载时触发事件
- 页面关闭时触发事件
- 用户点击按钮执行动作
- 验证用户输入内容的合法性
- 等等 ...

可以使用多种方法来执行 JavaScript 事件代码：

- HTML 事件属性可以直接执行 JavaScript 代码
- HTML 事件属性可以调用 JavaScript 函数
- 你可以为 HTML 元素指定自己的事件处理程序
- 你可以阻止事件的发生。
- 等等 ...

### js中设置事件

注意，当在 JS 文件中为相关元素设置事件时，其写法与 HTML 事件属性写法相同，例如：

```html
<button id="test" onclick="changeContent()">更换内容</button>
```

在 JS 中则需要这样写：

```js
var test = document.getElementById("test");
test.onclick = changeContent(){
    //......
}
```

注：不推荐使用 HTML 元素中可以**添加事件属性**的方式来添加属性。

例子：

```html
<button onclick="getElementById('demo').innerHTML=Date()">现在的时间是?</button>
```

因为遵从“高内聚，低耦合”的编程原则。

高内聚是说模块内部要高度聚合，低耦合是说模块与模块之间的藕合度要尽量低。前者是说模块内部的关系，后者是说模块与模块间的关系。

注意：在为元素添加事件句柄或者删除元素事件句柄的过程中，不要将 event 参数设置为 onclick，而必须写成 click，去掉事件名称中的 on 即可。

添加事件句柄函数原型:

```js
element.addEventListener(event, function, [useCapture])
```

删除事件句柄的函数原型:

```js
element.removeEventListener(event, function, [useCapture])
```

## JavaScript 字符串

JavaScript 字符串用于存储和处理文本。

### JavaScript 字符串

字符串可以存储一系列字符，如 "John Doe"。

字符串可以是插入到引号中的任何字符。你可以使用单引号或双引号：
```js
var carname = "Volvo XC60";//双引号
var carname = 'Volvo XC60';//单引号
```

你可以使用索引位置来访问字符串中的每个字符：
```js
var character = carname[7];//相当于字符数组
```

字符串的索引从 0 开始，这意味着第一个字符索引值为 [0],第二个为 [1], 以此类推。

你可以在字符串中使用引号，字符串中的引号不要与字符串的引号相同:
```js
var answer = "It's alright";
var answer = "He is called 'Johnny'";
var answer = 'He is called "Johnny"';
```

你也可以在字符串添加转义字符来使用引号：
```js
var x = 'It\'s alright';
var y = "He is called \"Johnny\"";
```

双引号" " 中用单引号 ' ' 可以不用加反斜杠，例如：
```js
var x="my name 'is' xxx"  // 此处不需要加反斜杠
```

双引号" " 中用双引号 " " 需要加反斜杠，例如：
```js
var x="my name \"is\" xxx"  // 此处需要在两个上引号前各加一个加反斜杠
```

单引号 ' ' 中用双引号" " 不需要加反斜杠，当然加了也可以，例如：
```js
var x1 ='my name "is" xxx'     // 此处不需要加反斜杠（推荐）
var x2 ='my name \"is\" xxx'   // 添加反斜杠效果也一样（不推荐）
```

### 字符串长度

可以使用内置属性 length 来计算字符串的长度：
```js
var txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
var sln = txt.length;
```

### 特殊字符

在 JavaScript 中，字符串写在单引号或双引号中。

因为这样，以下实例 JavaScript 无法解析：
```
 "We are the so-called "Vikings" from the north."
```
字符串 "We are the so-called " 被截断。

如何解决以上的问题呢？可以使用反斜杠 (\) 来转义 "Vikings" 字符串中的双引号，如下:
```
 "We are the so-called \"Vikings\" from the north."
```
 反斜杠是一个**转义字符**。 转义字符将特殊字符转换为字符串字符：

转义字符 (\) 可以用于转义撇号，换行，引号，等其他特殊字符。

下表中列举了在字符串中可以使用转义字符转义的特殊字符：

| 代码 | 输出        |
| :--- | :---------- |
| \'   | 单引号      |
| \"   | 双引号      |
| \\   | 反斜杠      |
| \n   | 换行        |
| \r   | 回车        |
| \t   | tab(制表符) |
| \b   | 退格符      |
| \f   | 换页符      |

### 字符串可以是对象

通常， JavaScript 字符串是原始值，可以使用字符创建：
```js
var firstName = "John"
```

但我们也可以使用 new 关键字将字符串定义为一个对象：
```js
var firstName = new String("John")
```

*不要创建 String 对象。它会拖慢执行速度，并可能产生其他副作用：*

```js
var x = "John";             
var y = new String("John");
(x === y) // 结果为 false，因为 x 是字符串，y 是对象
```
*=== 为绝对相等，即数据类型与值都必须相等。*

### 字符串属性和方法

原始值字符串，如 "John", 没有属性和方法(因为他们不是对象)。

原始值可以使用 JavaScript 的属性和方法，因为 JavaScript 在执行方法和属性时可以把原始值当作对象。

字符串方法我们将在下一章节中介绍。

## 字符串属性

| 属性        | 描述                       |
| :---------- | :------------------------- |
| constructor | 返回创建字符串属性的函数   |
| length      | 返回字符串的长度           |
| prototype   | 允许您向对象添加属性和方法 |

## 字符串方法

更多方法实例可以参见：[JavaScript String 对象](https://www.runoob.com/jsref/jsref-obj-string.html)。

| 方法                | 描述                                                         |
| :------------------ | :----------------------------------------------------------- |
| charAt()            | 返回指定索引位置的字符                                       |
| charCodeAt()        | 返回指定索引位置字符的 Unicode 值                            |
| concat()            | 连接两个或多个字符串，返回连接后的字符串                     |
| fromCharCode()      | 将 Unicode 转换为字符串                                      |
| indexOf()           | 返回字符串中检索指定字符第一次出现的位置                     |
| lastIndexOf()       | 返回字符串中检索指定字符最后一次出现的位置                   |
| localeCompare()     | 用本地特定的顺序来比较两个字符串                             |
| match()             | 找到一个或多个正则表达式的匹配                               |
| replace()           | 替换与正则表达式匹配的子串                                   |
| search()            | 检索与正则表达式相匹配的值                                   |
| slice()             | 提取字符串的片断，并在新的字符串中返回被提取的部分           |
| split()             | 把字符串分割为子字符串数组                                   |
| substr()            | 从起始索引号提取字符串中指定数目的字符                       |
| substring()         | 提取字符串中两个指定的索引号之间的字符                       |
| toLocaleLowerCase() | 根据主机的语言环境把字符串转换为小写，只有几种语言（如土耳其语）具有地方特有的大小写映射 |
| toLocaleUpperCase() | 根据主机的语言环境把字符串转换为大写，只有几种语言（如土耳其语）具有地方特有的大小写映射 |
| toLowerCase()       | 把字符串转换为小写                                           |
| toString()          | 返回字符串对象值                                             |
| toUpperCase()       | 把字符串转换为大写                                           |
| trim()              | 移除字符串首尾空白                                           |
| valueOf()           | 返回某个字符串对象的原始值                                   |

### JavaScript == 与 === 区别

1、对于 string、number 等基础类型，== 和 === 是有区别的

- a）不同类型间比较，== 之比较 "转化成同一类型后的值" 看 "值" 是否相等，=== 如果类型不同，其结果就是不等。
-  b）同类型比较，直接进行 "值" 比较，两者结果一样。

2、对于 Array,Object 等高级类型，== 和 === 是没有区别的

进行 "指针地址" 比较

3、基础类型与高级类型，== 和 === 是有区别的

- a）对于 ==，将高级转化为基础类型，进行 "值" 比较
-  b）因为类型不同，=== 结果为 false

4、!= 为 == 的非运算，!== 为 === 的非运算

```js
var num=1；

var str="1"；

var test=1；

test == num   //true　相同类型　相同值 

test === num  //true　相同类型　相同值 

test !== num  //false test与num类型相同，其值也相同,　非运算肯定是false 

num == str   //true 　把str转换为数字，检查其是否相等。 

num != str   //false  == 的 非运算 

num === str  //false  类型不同，直接返回false 

num !== str  //true   num 与 str类型不同 意味着其两者不等　非运算自然是true啦
```

## JavaScript 运算符

运算符 = 用于赋值。

运算符 + 用于加值。

运算符 = 用于给 JavaScript 变量赋值。

算术运算符 + 用于把值加起来。

### JavaScript 算术运算符

y=5，下面的表格解释了这些算术运算符：

|运算符|描述|例子|x 运算结果|y 运算结果|
|:--|:--|:--|:--|:--|
|+|加法|x=y+2|7|5|
|-|减法|x=y-2|3|5|
|\*|乘法|x=y\*2|10|5|
|/|除法|x=y/2|2.5|5|
|%|取模（余数）|x=y%2|1|5|
|++|自增|x=++y|6|6|
| | |x=y++|5|6|
|--|自减|x=--y|4|4|
| | |x=y--|5|4|

### JavaScript 赋值运算符

赋值运算符用于给 JavaScript 变量赋值。

| 运算符 | 例子 | 等同于 |
| :----- | :--- | :----- |
| =      | x=y  |        |
| +=     | x+=y | x=x+y  |
| -=     | x-=y | x=x-y  |
| \*=     | x\*=y | x=x\*y  |
| /=     | x/=y | x=x/y  |
| %=     | x%=y | x=x%y  |

取模运算的结果符号只与左边值的符号有关：

```js
var x = 7 % 3; // 结果为 1
var y = 7 % (-3); // 结果为 1
var z = (-7) % 3; // 结果为 -1
```

-  如果 % 左边的操作数是正数，则模除的结果为正数或零；
-  如果 % 左边的操作数是负数，则模除的结果为负数或零。

### 用于字符串的 + 运算符

+ 运算符用于把文本值或字符串变量加起来（连接起来）。

如需把两个或多个字符串变量连接起来，请使用 + 运算符。

要想在两个字符串之间增加空格，需要把空格插入一个字符串之中：或者把空格插入表达式中：

### 对字符串和数字进行加法运算

两个数字相加，返回数字相加的和，如果数字与字符串相加，返回字符串，如下实例：
```js
var result1=5+5+"abc"; //结果将是"10abc"

var result2= ""+5+5+"abc"; //结果将是"55abc"
```

常见的不同类型运算的转换方式：

1. 字符串和数字相加，数字转成字符串.
```js
var one="This is a test";
var two=123;
var three=one+two;

// 结果：three:This is a test123
```

2. 数字和布尔值相加，布尔值 false 转成 0，true 转成 1

```js
var one=13;
var two=true;
var three=one+two;
// 结果 three:14
```

3. 字符串与布尔值相加，布尔值转化成字符串。

4. 数字与 null(空值) 相加，null 转化为数字 0：
```js
var car=null+3+4;    // 结果为7
```

字符串与 null(空值) 相加，null 转化为字符串：
```js
var car=null+"a";    // 结果为 nulla
```

## JavaScript 比较 和 逻辑运算符

比较和逻辑运算符用于测试 *true* 或者 *false*。

### 比较运算符

比较运算符在逻辑语句中使用，以测定变量或值是否相等。

x=5，下面的表格解释了比较运算符：

| 运算符 | 描述                                               | 比较    | 返回值  |
| :----- | :------------------------------------------------- | :------ | :------ |
| ==     | 等于                                               | x==8    | *false* |
| | | x==5   | *true*                                             |
| ===    | 绝对等于（值和类型均相等）                         | x==="5" | *false* |
| | | x===5  | *true*                                             |
| !=     | 不等于                                             | x!=8    | *true*  |
| !==    | 不绝对等于（值和类型有一个不相等，或两个都不相等） | x!=="5" | *true*  |
| | | x!==5  | *false*                                            |
| >      | 大于                                               | x>8     | *false* |
| <      | 小于                                               | x<8     | *true*  |
| >=     | 大于或等于                                         | x>=8    | *false* |
| <=     | 小于或等于                                         | x<=8    | *true*  |

### 逻辑运算符

逻辑运算符用于测定变量或值之间的逻辑。

给定 x=6 以及 y=3，下表解释了逻辑运算符：

| 运算符 | 描述 | 例子                        |
| :----- | :--- | :-------------------------- |
| &&     | and  | (x < 10 && y > 1) 为 true   |
| \|\|   | or   | (x\==5 \|\| y\==5) 为 false |
| !      | not  | !(x==y) 为 true             |

逻辑运算符用于测定变量或值之间的逻辑。除了常用的返回布尔值，也可以利用运算符的逻辑来获得我们想要的数字或枚举变量：
```js
0||3 : 3

1||3 : 1

0&&3 : 0

1&&3 : 3
```
其他数据类型转换为布尔类型的规则: null、undefined、0、NaN、空字符串转换为false，其他转化为 true。

**JavaScript 中有三种逻辑运算符：**

1. 取反 !

首先把数据转化为布尔值，然后取反，结果为 true 或 false。

2. 逻辑与 &&

JavaScript 中逻辑与和其他语言不太一样，如果第一个操作数是 true(或者能够转为 true)，计算结果就是第二个操作数，如果第一个操作数是 false，结果就是 false（短路计算），对于一些特殊数值不遵循以上规则。(个人理解为:如果运算的第一个操作数为true,则返回第二个操作数,反之则返回第一个操作数)

3. 逻辑或 ||

如果第一个操作数不是 false，结果就是第一个操作数，否则结果是第二个操作数。如果第一个操作数能够转为 true，结果就是第一个操作数(个人理解为:如果运算的第一个操作数为 true,则返回第一个操作数,反之则返回第二个操作数)

### 条件运算符

JavaScript 还包含了基于某些条件对变量进行赋值的条件运算符（三目运算符）。
```js
variablename=(condition)?value1:value2 
```

## JavaScript if...Else 语句
条件语句用于基于不同的条件来执行不同的动作。

### 条件语句
通常在写代码时，您总是需要为不同的决定来执行不同的动作。您可以在代码中使用条件语句来完成该任务。

在 JavaScript 中，我们可使用以下条件语句：

if 语句 - 只有当指定条件为 true 时，使用该语句来执行代码
if...else 语句 - 当条件为 true 时执行代码，当条件为 false 时执行其他代码
if...else if....else 语句- 使用该语句来选择多个代码块之一来执行
switch 语句 - 使用该语句来选择多个代码块之一来执行

## JavaScript switch 语句

switch 语句用于基于不同的条件来执行不同的动作。
```js
switch(n)
{
    case 1:
        执行代码块 1
        break;
    case 2:
        执行代码块 2
        break;
    default:
        与 case 1 和 case 2 不同时执行的代码
}
```

## JavaScript for 循环

循环可以将代码块执行指定的次数。

### JavaScript 循环

如果您希望一遍又一遍地运行相同的代码，并且每次的值都不同，那么使用循环是很方便的。

### 不同类型的循环

JavaScript 支持不同类型的循环：

1. for - 循环代码块一定的次数
2. for/in - 循环遍历对象的属性
3. while - 当指定的条件为 true 时循环指定的代码块
4. do/while - 同样当指定的条件为 true 时循环指定的代码块

### For/In 循环

JavaScript for/in 语句循环遍历对象的属性：

```js
var person={fname:"John",lname:"Doe",age:25}; 
 
for (x in person)  // x 为属性名
{
    txt=txt + person[x];
}
```
for in 循环不仅可以遍历对象的属性，还可以遍历数组。
```js
var x
var nums = [1, 3, 5];
for (x in nums)
{
    document.write(nums[x]+ "<br />");  // x 为数组索引
}
```
### For/Of循环

for 循环除了使用 in 方式来循环数组，还提供了一个方式： of , 遍历数组时更加方便。

for...of 是 ES6 新引入的特性。它既比传统的for循环简洁，同时弥补了forEach和for-in循环的短板。

for-of的语法：
```js
for (var value of myArray) {
  console.log(value);
}
```

for-of 的语法看起来跟 for-in 很相似，但它的功能却丰富的多，它能循环很多东西。

**for-of 循环使用例子：**

循环一个数组(Array):

```js
let iterable = [10, 20, 30];

for (let value of iterable) {
  console.log(value);
}
// 10
// 20
// 30
```

我们可以使用const来替代let，这样它就变成了在循环里的不可修改的静态变量。

```js
let iterable = [10, 20, 30];

for (const value of iterable) {
  console.log(value);
}
// 10
// 20
// 30
```

循环一个字符串：

```js
let iterable = "boo";

for (let value of iterable) {
  console.log(value);
}
// "b"
// "o"
// "o"
```

循环一个类型化的数组(TypedArray)：

```js
let iterable = new Uint8Array([0x00, 0xff]);

for (let value of iterable) {
  console.log(value);
}
// 0
// 255
```

循环一个Map:

```js
let iterable = new Map([["a", 1], ["b", 2], ["c", 3]]);

for (let [key, value] of iterable) {
  console.log(value);
}
// 1
// 2
// 3

for (let entry of iterable) {
  console.log(entry);
}
// [a, 1]
// [b, 2]
// [c, 3]
```

循环一个 Set:

```js
let iterable = new Set([1, 1, 2, 2, 3, 3]);

for (let value of iterable) {
  console.log(value);
}
// 1
// 2
// 3
```

循环一个 DOM collection

循环一个DOM collections，比如NodeList，之前我们讨论过如何循环一个NodeList，现在方便了，可以直接使用for-of循环：

```js
// Note: This will only work in platforms that have
// implemented NodeList.prototype[Symbol.iterator]
let articleParagraphs = document.querySelectorAll("article > p");

for (let paragraph of articleParagraphs) {
  paragraph.classList.add("read");
}
```

循环一个拥有enumerable属性的对象

for–of循环并不能直接使用在普通的对象上，但如果我们按对象所拥有的属性进行循环，可使用内置的Object.keys()方法：

```js
for (var key of Object.keys(someObject)) {
  console.log(key + ": " + someObject[key]);
}
```

循环一个生成器(generators)

我们可循环一个生成器(generators):

```js
function* fibonacci() { // a generator function
  let [prev, curr] = [0, 1];
  while (true) {
    [prev, curr] = [curr, prev + curr];
    yield curr;
  }
}

for (let n of fibonacci()) {
  console.log(n);
  // truncate the sequence at 1000
  if (n >= 1000) {
    break;
  }
}
```

## JavaScript while 循环

只要指定条件为 true，循环就可以一直执行代码块。

### while 循环

while 循环会在指定条件为真时循环执行代码块。

语法
```js
while (条件)
{
    需要执行的代码
}
```

### do/while 循环

do/while 循环是 while 循环的变体。该循环会在检查条件是否为真之前执行一次代码块，然后如果条件为真的话，就会重复这个循环。

语法
```js
do
{
    需要执行的代码
}
while (条件);
```

## JavaScript break 和 continue 语句

break 语句用于跳出循环。

continue 用于跳过循环中的一个迭代。

### break 语句

我们已经在本教程之前的章节中见到过 break 语句。它用于跳出 switch() 语句。

break 语句可用于跳出循环。

continue 语句跳出循环后，会继续执行该循环之后的代码（如果有的话）：

### continue 语句

continue 语句中断循环中的迭代，如果出现了指定的条件，然后继续循环中的下一个迭代。 

### JavaScript 标签

正如您在 switch 语句那一章中看到的，可以对 JavaScript 语句进行标记。

如需标记 JavaScript 语句，请在语句之前加上冒号：
```js
label:
statements
```

break 和 continue 语句仅仅是能够跳出代码块的语句。

语法:
```js
break labelname; 
 
continue labelname;.
```

continue 语句（带有或不带标签引用）只能用在循环中。

break 语句（不带标签引用），只能用在循环或 switch 中。

通过标签引用，break 语句可用于跳出任何 JavaScript 代码块：

## JavaScript typeof, null, undefined, valueOf()

### typeof 操作符

你可以使用 typeof 操作符来检测变量的数据类型。
```js
typeof "John"                // 返回 string
typeof 3.14                  // 返回 number
typeof false                 // 返回 boolean
typeof [1,2,3,4]             // 返回 object
typeof {name:'John', age:34} // 返回 object
//	 在JavaScript中，数组是一种特殊的对象类型。 因此 typeof [1,2,3,4] 返回 object。
```

### null

在 JavaScript 中 null 表示 "什么都没有"。

null是一个只有一个值的特殊类型。表示一个空对象引用。

*用 typeof 检测 null 返回是object。*

你可以设置为 null 来清空对象:
你可以设置为 undefined 来清空对象:
```js
var person = null;           // 值为 null(空), 但类型为对象
var person = undefined;     // 值为 undefined, 类型为 undefined
```

### undefined

在 JavaScript 中, undefined 是一个没有设置值的变量。

typeof 一个没有值的变量会返回 undefined。
任何变量都可以通过设置值为 undefined 来清空。 类型为 undefined.
```js
var person;                  // 值为 undefined(空), 类型是undefined
person = undefined;          // 值为 undefined, 类型是undefined
```

### undefined 和 null 的区别

null 和 undefined 的值相等，但类型不等：
```js
typeof undefined             // undefined
typeof null                  // object
null === undefined           // false
null == undefined            // true
```

1. 定义

- （1）undefined：是所有没有赋值变量的默认值，自动赋值。
- （2）null：主动释放一个变量引用的对象，表示一个变量不再指向任何对象地址。

undefined 与 null 的区别：

表面上 undefined 与 null 都是什么都没有的意思，但是实际上 undefined 是未定义（就是变量没有初始化），null 是一个变量初始化了，但是什么值都没给，只给了一个空对象；进一步说，undefined 与 null是值相等，类型不相等。

2. 何时使用null?

当使用完一个比较大的对象时，需要对其进行释放内存时，设置为 null。

3. null 与 undefined 的异同点是什么呢？

共同点：都是原始类型，保存在栈中变量本地。

不同点：

（1）undefined——表示变量声明过但并未赋过值。

它是所有未赋值变量默认值，例如：
```js
var a;    // a 自动被赋值为 undefined
```

（2）null——表示一个变量将来可能指向一个对象。

一般用于主动释放指向对象的引用，例如：
```js
var emps = ['ss','nn'];
emps = null;     // 释放指向数组的引用
```
4. 延伸——垃圾回收站

它是专门释放对象内存的一个程序。

- （1）在底层，后台伴随当前程序同时运行；引擎会定时自动调用垃圾回收期；
- （2）当有一个对象不再被任何变量引用时，才释放。

## JavaScript 类型转换

Number() 转换为数字， String() 转换为字符串， Boolean() 转化为布尔值。

### JavaScript 数据类型

在 JavaScript 中有 6 种不同的数据类型：

- string
- number
- boolean
- object
- function
- symbol

3 种对象类型：

- Object
- Date
- Array

2 个不包含任何值的数据类型：

- null
- undefined

### typeof 操作符

你可以使用 typeof 操作符来查看 JavaScript 变量的数据类型。

请注意：

- NaN 的数据类型是 number
- 数组(Array)的数据类型是 object
- 日期(Date)的数据类型为 object
- null 的数据类型是 object
- 未定义变量的数据类型为 undefined

如果对象是 JavaScript Array 或 JavaScript Date ，我们就无法通过 **typeof** 来判断他们的类型，因为都是 返回 object。

### constructor 属性

constructor 属性返回所有 JavaScript 变量的构造函数。

```js
"John".constructor                 // 返回函数 String()  { [native code] }
(3.14).constructor                 // 返回函数 Number()  { [native code] }
false.constructor                  // 返回函数 Boolean() { [native code] }
[1,2,3,4].constructor              // 返回函数 Array()   { [native code] }
{name:'John', age:34}.constructor  // 返回函数 Object()  { [native code] }
new Date().constructor             // 返回函数 Date()    { [native code] }
function () {}.constructor         // 返回函数 Function(){ [native code] }
```

你可以使用 constructor 属性来查看对象是否为数组 (包含字符串 "Array"):
```js
function isArray(myArray) {
    return myArray.constructor.toString().indexOf("Array") > -1;
}
```

`return myArray.constructor.toString().indexOf("Array") > -1;`这句话怎么解释?

1、myArray 是函数 isArray 的参数，这里调用函数的时候，会传来数组 fruits。

2、constructor 是一个属性，构造函数属性，不同类型的数据，会得到相应不同的值。因为 myArray 是个数组，这里的 myArray.constructor 的值就是 `function Array() { [native code] }`。(如果 myArray 是个字符串，myArray.constructor 的值就是`function String() { [native code] }`。还有 number，boolean，object，等等。)
3、toString() 是个方法，变字符串的方法，这里把 `function Array() { [native code] }` 变成字符串，为了后面好检索。

4、indexOf("Array") 是个方法，检索字符串，这里看字符串 `function Array() { [native code] }` 里有没有Array，有就返回首次出现的位置，是一个数值，这里是 9。如果出现在第一个字符，会返回 0。空格参与计数。如果没有找到，就返回 -1。只要 >-1，就说明有 Array，就能判断原来那个函数调用传来的 fruits 是一个数组。如果 `myArray.constructor.toString().indexOf("Object")>-1`，那么 myArray 就是一个 Object 对象。不过那样地话，这个参数的名字就没取好了，应该叫做 myObject。

你可以使用 constructor 属性来查看对象是否为日期 (包含字符串 "Date"):
```js
function isDate(myDate) {
    return myDate.constructor.toString().indexOf("Date") > -1;
}
```

### JavaScript 类型转换

JavaScript 变量可以转换为新变量或其他数据类型：

- 通过使用 JavaScript 函数
- 通过 JavaScript 自身自动转换

### 一元运算符 +
Operator + 可用于将变量转换为数字：
```js
var y = "5";      // y 是一个字符串
var x = + y;      // x 是一个数字
```

如果变量不能转换，它仍然会是一个数字，但值为 NaN (不是一个数字):
```js
var y = "John";   // y 是一个字符串
var x = + y;      // x 是一个数字 (NaN)
```

### 自动转换类型

当 JavaScript 尝试操作一个 "错误" 的数据类型时，会自动转换为 "正确" 的数据类型。

以下输出结果不是你所期望的：
```js
5 + null    // 返回 5         null 转换为 0
"5" + null  // 返回"5null"   null 转换为 "null"
"5" + 1     // 返回 "51"      1 转换为 "1" 
"5" - 1     // 返回 4         "5" 转换为 5
```

### instanceof

判断某个变量是否是某个对象的实例则要选择使用另一个关键语法 instanceof。

可通过 instanceof 操作符来判断对象的具体类型，语法格式:
```js
var result = objectName instanceof objectType
```
返回布尔值，如果是指定类型返回 true，否则返回 false：

例：
```js
arr = [1,2,3];
if(arr instanceof Array){
    document.write("arr 是一个数组");
} else {
    document.write("arr 不是一个数组");
}
```

### NaN

NaN 是一个特殊的数值，NaN 即非数值（Not a Number），这个数值用于本来要返回数值的操作数未返回数值的情况。

NaN 与任何值都不相等，包括 NaN 本身。

可以通过 isNaN() 方法来判断某个数值是否是NaN这个特殊的数，使用 isNaN() 方法会将传入的数值如果是非数值的会将其自动转换成数值类型，若能转换成数值类型，那么这个函数返回 false，若不能转换成数值类型，则这个数就是 NaN，即返回 true。

## JavaScript 正则表达式

正则表达式（英语：Regular Expression，在代码中常简写为regex、regexp或RE）使用单个字符串来描述、匹配一系列符合某个句法规则的字符串搜索模式。

搜索模式可用于文本搜索和文本替换。

[正则表达式](正则表达式.md)

## JavaScript 错误/异常处理机制

- try 语句测试代码块的错误。

- catch 语句处理错误。

- throw 语句创建自定义错误。

- finally 语句在 try 和 catch 语句之后，无论是否有触发异常，该语句都会执行。

### JavaScript 错误

当 JavaScript 引擎执行 JavaScript 代码时，会发生各种错误。

可能是语法错误，通常是程序员造成的编码错误或错别字。

可能是拼写错误或语言中缺少的功能（可能由于浏览器差异）。

可能是由于来自服务器或用户的错误输出而导致的错误。

当然，也可能是由于许多其他不可预知的因素。

### JavaScript 抛出（throw）错误

当错误发生时，当事情出问题时，JavaScript 引擎通常会停止，并生成一个错误消息。

描述这种情况的技术术语是：JavaScript 将**抛出**一个错误。

### JavaScript try 和 catch

try 语句允许我们定义在执行时进行错误测试的代码块。

catch 语句允许我们定义当 try 代码块发生错误时，所执行的代码块。

JavaScript 语句 try 和 catch 是成对出现的。

语法
```js
try {
    ...    //异常的抛出
} catch(e) {
    ...    //异常的捕获与处理
} finally {
    ...    //结束处理
}
```

### 实例

在下面的例子中，我们故意在 try 块的代码中写了一个错字。

catch 块会捕捉到 try 块中的错误，并执行代码来处理它。
```js
var txt=""; 
function message() 
{ 
    try { 
        adddlert("Welcome guest!"); 
    } catch(err) { 
        txt="本页有一个错误。\n\n"; 
        txt+="错误描述：" + err.message + "\n\n"; 
        txt+="点击确定继续。\n\n"; 
        alert(txt); 
    } 
}
```

### finally 语句

finally 语句不论之前的 try 和 catch 中是否产生异常都会执行该代码块。
```js
function myFunction() {
  var message, x;
  message = document.getElementById("p01");
  message.innerHTML = "";
  x = document.getElementById("demo").value;
  try { 
    if(x == "") throw "值是空的";
    if(isNaN(x)) throw "值不是一个数字";
    x = Number(x);
    if(x > 10) throw "太大";
    if(x < 5) throw "太小";
  }
  catch(err) {
    message.innerHTML = "错误: " + err + ".";
  }
  finally {
    document.getElementById("demo").value = "";
  }
}
```

### Throw 语句

throw 语句允许我们创建自定义错误。

正确的技术术语是：创建或**抛出异常**（exception）。

如果把 throw 与 try 和 catch 一起使用，那么您能够控制程序流，并生成自定义的错误消息。

语法
```
throw exception
```
异常可以是 JavaScript 字符串、数字、逻辑值或对象。

### 实例

本例检测输入变量的值。如果值是错误的，会抛出一个异常（错误）。catch 会捕捉到这个错误，并显示一段自定义的错误消息：
```js
function myFunction() {
    var message, x;
    message = document.getElementById("message");
    message.innerHTML = "";
    x = document.getElementById("demo").value;
    try { 
        if(x == "")  throw "值为空";
        if(isNaN(x)) throw "不是数字";
        x = Number(x);
        if(x < 5)    throw "太小";
        if(x > 10)   throw "太大";
    }
    catch(err) {
        message.innerHTML = "错误: " + err;
    }
}
```

*请注意，如果 getElementById 函数出错，上面的例子也会抛出一个错误。*

## JavaScript 调试

在编写 JavaScript 时，如果没有调试工具将是一件很痛苦的事情。

### JavaScript 调试

没有调试工具是很难去编写 JavaScript 程序的。

你的代码可能包含语法错误，逻辑错误，如果没有调试工具，这些错误比较难于发现。

通常，如果 JavaScript 出现错误，是不会有提示信息，这样你就无法找到代码错误的位置。

*通常，你在编写一个新的 JavaScript 代码过程中都会发生错误。*

### JavaScript 调试工具

在程序代码中寻找错误叫做代码调试。

调试很难，但幸运的是，很多浏览器都内置了调试工具。

内置的调试工具可以开始或关闭，严重的错误信息会发送给用户。

有了调试工具，我们就可以设置断点 (代码停止执行的位置), 且可以在代码执行时检测变量。

浏览器启用调试工具一般是按下 F12 键，并在调试菜单中选择 "Console" 。

### console.log() 方法

如果浏览器支持调试，你可以使用 console.log() 方法在调试窗口上打印 JavaScript 值：
```js
a = 5;
b = 6;
c = a + b;
console.log(c);
```

### 设置断点

在调试窗口中，你可以设置 JavaScript 代码的断点。

在每个断点上，都会停止执行 JavaScript 代码，以便于我们检查 JavaScript 变量的值。

在检查完毕后，可以重新执行代码（如播放按钮）。

### debugger 关键字

debugger 关键字用于停止执行 JavaScript，并调用调试函数。

这个关键字与在调试工具中设置断点的效果是一样的。

如果没有调试可用，debugger 语句将无法工作。

开启 debugger ，代码在第三行前停止执行。
```js
var x = 15 * 5;
debugger;
document.getElementbyId("demo").innerHTML = x;
```

### 主要浏览器的调试工具

通常，浏览器启用调试工具一般是按下 F12 键，并在调试菜单中选择 "Console" 。

## JavaScript 变量提升

JavaScript 中，函数及变量的声明都将被提升到函数的最顶部。

JavaScript 中，变量可以在使用后声明，也就是变量可以先使用再声明。

以下两个实例将获得相同的结果：
```js
x = 5; // 变量 x 设置为 5

elem = document.getElementById("demo"); // 查找元素
elem.innerHTML = x;                     // 在元素中显示 x

var x; // 声明 x
```

```js
var x; // 声明 x
x = 5; // 变量 x 设置为 5

elem = document.getElementById("demo"); // 查找元素
elem.innerHTML = x;  
```

要理解以上实例就需要理解 "hoisting(变量提升)"。

**变量提升：函数声明和变量声明总是会被解释器悄悄地被"提升"到方法体的最顶部。**

### JavaScript 初始化不会提升

JavaScript 只有声明的变量会提升，初始化的不会。

以下两个实例结果结果不相同：
```js
var x = 5; // 初始化 x
var y = 7; // 初始化 y

elem = document.getElementById("demo"); // 查找元素
elem.innerHTML = x + " " + y;           // 显示 x 和 y
```

```js
var x = 5; // 初始化 x

elem = document.getElementById("demo"); // 查找元素
elem.innerHTML = x + " " + y;           // 显示 x 和 y

var y = 7; // 初始化 y
```

实例 2 的 y 输出了 **undefined**，这是因为变量声明 (var y) 提升了，但是初始化(y = 7) 并不会提升，所以 y 变量是一个未定义的变量。

实例 2 类似以下代码:
```js
var x = 5; // 初始化 x
var y;     // 声明 y

elem = document.getElementById("demo"); // 查找元素
elem.innerHTML = x + " " + y;           // 显示 x 和 y

y = 7;    // 设置 y 为 7
```

### 在头部声明你的变量

//这tm不是废话吗。。。js也太自由奔放了吧

对于大多数程序员来说并不知道 JavaScript 变量提升。

如果程序员不能很好的理解变量提升，他们写的程序就容易出现一些问题。

为了避免这些问题，通常我们在每个作用域开始前声明这些变量，这也是正常的 JavaScript 解析步骤，易于我们理解。

JavaScript 严格模式(strict mode)不允许使用未声明的变量。
在下一个章节中我们将会学习到 "严格模式(strict mode)" 。

## JavaScript 严格模式(use strict)

JavaScript 严格模式（strict mode）即在严格的条件下运行。

### 使用 "use strict" 指令

"use strict" 指令在 JavaScript 1.8.5 (ECMAScript5) 中新增。

它不是一条语句，但是是一个字面量表达式，在 JavaScript 旧版本中会被忽略。

"use strict" 的目的是指定代码在严格条件下执行。

严格模式下你不能使用未声明的变量。

*支持严格模式的浏览器:
Internet Explorer 10 +、 Firefox 4+ Chrome 13+、 Safari 5.1+、 Opera 12+。*

### 严格模式声明

严格模式通过在脚本或函数的头部添加 `"use strict";` 表达式来声明。

实例中我们可以在浏览器按下 F12 (或点击"工具>更多工具>开发者工具") 开启调试模式，查看报错信息。
```js
"use strict";
x = 3.14;       // 报错 (x 未定义)
```

```js
"use strict";
myFunction();

function myFunction() {
    y = 3.14;   // 报错 (y 未定义)
}
```

在函数内部声明是局部作用域 (只在函数内使用严格模式):
```js
x = 3.14;       // 不报错
myFunction();

function myFunction() {
   "use strict";
    y = 3.14;   // 报错 (y 未定义)
}
```

### 为什么使用严格模式:

- 消除Javascript语法的一些不合理、不严谨之处，减少一些怪异行为;
- 消除代码运行的一些不安全之处，保证代码运行的安全；
- 提高编译器效率，增加运行速度；
- 为未来新版本的Javascript做好铺垫。

"严格模式"体现了Javascript更合理、更安全、更严谨的发展方向，包括IE 10在内的主流浏览器，都已经支持它，许多大项目已经开始全面拥抱它。

另一方面，同样的代码，在"严格模式"中，可能会有不一样的运行结果；一些在"正常模式"下可以运行的语句，在"严格模式"下将不能运行。掌握这些内容，有助于更细致深入地理解Javascript，让你变成一个更好的程序员。

### 严格模式的限制

//也就是说，在原来非严格模式下这些都是允许的咯。。。js是真的自由奔放

1. 不允许使用未声明的变量：*对象也是一个变量。*
2. 不允许删除变量或对象。
3. 不允许删除函数。
4. 不允许变量重名:
5. 不允许使用八进制:
6. 不允许使用转义字符:
7. 不允许对只读属性赋值:
8. 不允许对一个使用getter方法读取的属性进行赋值
9. 不允许删除一个不允许删除的属性：
10. 变量名不能使用 "eval" 字符串:
11. 变量名不能使用 "arguments" 字符串:
12. 不允许使用以下这种语句:
13. 由于一些安全原因，在作用域 eval() 创建的变量不能被调用：
14. 禁止this关键字指向全局对象。因此，使用构造函数时，如果忘了加new，this不再指向全局对象，而是报错。

### 保留关键字

为了向将来Javascript的新版本过渡，严格模式新增了一些保留关键字：

- implements
- interface
- let
- package
- private
- protected
- public
- static
- yield

***"use strict" 指令只允许出现在脚本或函数的开头。***

## JavaScript 表单

### JavaScript 表单验证

HTML 表单验证可以通过 JavaScript 来完成。

以下实例代码用于判断表单字段(fname)值是否存在， 如果不存在，就弹出信息，阻止表单提交：
```js
function validateForm() {
    var x = document.forms["myForm"]["fname"].value;
    if (x == null || x == "") {
        alert("需要输入名字。");
        return false;
    }
}
```

以上 JavaScript 代码可以通过 HTML 代码来调用：
```html
<form name="myForm" action="demo_form.php" onsubmit="return validateForm()" method="post">
名字: <input type="text" name="fname">
<input type="submit" value="提交">
</form>
```

**onsubmit="return validateForm()"** 为什么不是 **onsubmit="validateForm()"** ？？

**onsubmit="validateForm()"** 能够调用 **validateForm()** 对表单进行验证，但是在验证不通过的情况下，并不能阻止表单提交。

**onsubmit="return validateForm()"** 当验证不通过时，返回 false，可以阻止表单提交。

为何？

原来 onsubmit 属性就像是 \<form> 这个 html 对象的一个方法名，其值（一字符串）就是其方法体，默认返回 true；

```
onsubmit="return validateForm()"
```

相当于:

```
Form.prototype.onsubmit = function() {
    return validateForm()
};
```

这样复写了 onsubmit 的默认方法（默认返回 true），根据 validateForm() 的结果返回 true 或 false，当验证不通过时，返回 false，onsubmit="return false;" 阻止表单提交。

### JavaScript 验证输入的数字

JavaScript 常用于对输入数字的验证：
```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
    </head>
    <body>
        <h1>JavaScript 验证输入</h1>
        <p>请输入 1 到 10 之间的数字：</p>
        <input id="numb">
        <button type="button" onclick="myFunction()">提交</button>
        <p id="demo"></p>
        <script>
            function myFunction() {
                var x, text;
                // 获取 id="numb" 的值
                x = document.getElementById("numb").value;
                // 如果输入的值 x 不是数字或者小于 1 或者大于 10，则提示错误 Not a Number or less than one or greater than 10
                if (isNaN(x) || x < 1 || x > 10) {
                	text = "输入错误";
                } else {
                	text = "输入正确";
                }
                document.getElementById("demo").innerHTML = text;
            }
        </script>
    </body>
</html>
```

### HTML 表单自动验证

HTML 表单验证也可以通过浏览器来自动完成。

如果表单字段 (fname) 的值为空, required 属性会阻止表单提交：
```html
<form action="demo_form.php" method="post">
  <input type="text" name="fname" required="required">
  <input type="submit" value="提交">
</form>
```

*Internet Explorer 9 及更早 IE 浏览器不支持表单自动验证。*

**用户体验提示**

表单验证 html 属性 required 有几个缺陷。

就是当一个 input 设置为 required 的时候，在初始化时，因为其本身是空的，所以 invalid 伪类会对它起作用，这不是我们想看到的，此时我们什么还都没有做。

我们可以统一在这些伪类前加上父选择器 .invalid，这时只有在父元素具有 invalid 类时，这些伪类才会起作用。可以设置一个 submit 事件，在表单提交因验证失败后，会触发 input 的 invalid 事件，给 form 添加 invalid 类：

```
form.addEventListener('invalid'， function() {this.className = 'invalid'}， true)
```

因为 invaild 是 Input 的事件，而不是 form 的事件，所以这里我们设置第三个参数为 true 采用事件捕获的方式处理，另外 css 选择器的使用对 this.className 影响需要提前处理。

### 数据验证

数据验证用于确保用户输入的数据是有效的。

典型的数据验证有：

- 必需字段是否有输入?
- 用户是否输入了合法的数据?
- 在数字字段是否输入了文本?
- 
大多数情况下，数据验证用于确保用户正确输入数据。

数据验证可以使用不同方法来定义，并通过多种方式来调用。

**服务端数据验证**是在数据提交到服务器上后再验证。

**客户端数据验证**是在数据发送到服务器前，在浏览器上完成验证。

### HTML 约束验证

HTML5 新增了 HTML 表单的验证方式：约束验证（constraint validation）。

约束验证是表单被提交时浏览器用来实现验证的一种算法。

HTML 约束验证基于：

- HTML 输入属性
- CSS 伪类选择器
- DOM 属性和方法

#### 约束验证 HTML 输入属性

| 属性     | 描述                     |
| :------- | :----------------------- |
| disabled | 规定输入的元素不可用     |
| max      | 规定输入元素的最大值     |
| min      | 规定输入元素的最小值     |
| pattern  | 规定输入元素值的模式     |
| required | 规定输入元素字段是必需的 |
| type     | 规定输入元素的类型       |

完整列表，请查看 [HTML 输入属性](https://www.runoob.com/html/html5-form-attributes.html)。

#### 约束验证 CSS 伪类选择器

| 选择器    | 描述                                    |
| :-------- | :-------------------------------------- |
| :disabled | 选取属性为 "disabled" 属性的 input 元素 |
| :invalid  | 选取无效的 input 元素                   |
| :optional | 选择没有"required"属性的 input 元素     |
| :required | 选择有"required"属性的 input 元素       |
| :valid    | 选取有效值的 input 元素                 |

完整列表，请查看 [CSS 伪类](https://www.runoob.com/css/css-pseudo-classes.html)。

## JavaScript 表单验证

### JavaScript 表单验证

JavaScript 可用来在数据被送往服务器前对 HTML 表单中的这些输入数据进行验证。

表单数据经常需要使用 JavaScript 来验证其正确性：

- 验证表单数据是否为空？
- 验证输入是否是一个正确的email地址？
- 验证日期是否输入正确？
- 验证表单输入内容是否为数字型？

### 必填（或必选）项目

下面的函数用来检查用户是否已填写表单中的必填（或必选）项目。假如必填或必选项为空，那么警告框会弹出，并且函数的返回值为 false，否则函数的返回值则为 true（意味着数据没有问题）：

```js
function validateForm()
{
  var x=document.forms["myForm"]["fname"].value;
  if (x==null || x=="")
  {
    alert("姓必须填写");
    return false;
  }
}
```

以上函数在 form 表单提交时被调用:
```html
<form name="myForm" action="demo-form.php" onsubmit="return validateForm()" method="post">
姓: <input type="text" name="fname">
<input type="submit" value="提交">
</form>
```

### E-mail 验证

下面的函数检查输入的数据是否符合电子邮件地址的基本语法。

意思就是说，输入的数据必须包含 @ 符号和点号(.)。同时，@ 不可以是邮件地址的首字符，并且 @ 之后需有至少一个点号：
```js
function validateForm(){
  var x=document.forms["myForm"]["email"].value;
  var atpos=x.indexOf("@");
  var dotpos=x.lastIndexOf(".");
  if (atpos<1 || dotpos<atpos+2 || dotpos+2>=x.length){
    alert("不是一个有效的 e-mail 地址");
    return false;
  }
}
```

下面是连同 HTML 表单的完整代码：
```html
<form name="myForm" action="demo-form.php" onsubmit="return validateForm();" method="post">
    Email: <input type="text" name="email">
    <input type="submit" value="提交">
</form>
```

## JavaScript 验证 API

约束验证 DOM 方法

| Property            | Description                                                  |
| :------------------ | :----------------------------------------------------------- |
| checkValidity()     | 如果 input 元素中的数据是合法的返回 true，否则返回 false。   |
| setCustomValidity() | 设置 input 元素的 validationMessage 属性，用于自定义错误提示信息的方法。使用 setCustomValidity 设置了自定义提示后，validity.customError 就会变成true，则 checkValidity 总是会返回false。如果要重新判断需要取消自定义提示，方式如下：`setCustomValidity('')  setCustomValidity(null)  setCustomValidity(undefined)` |

以下实例如果输入信息不合法，则返回错误信息：
```html
<input id="id1" type="number" min="100" max="300" required> <button onclick="myFunction()">验证</button>
<p id="demo"></p>
<script>
	function myFunction() {
		var inpObj = document.getElementById("id1");
		if (inpObj.checkValidity() == false) {
			document.getElementById("demo").innerHTML = inpObj.validationMessage;    
		} 
	}
</script>
```

### 约束验证 DOM 属性

| 属性              | 描述                                  |
| :---------------- | :------------------------------------ |
| validity          | 布尔属性值，返回 input 输入值是否合法 |
| validationMessage | 浏览器错误提示信息                    |
| willValidate      | 指定 input 是否需要验证               |

### Validity 属性

input 元素的 **validity 属性**包含一系列关于 validity 数据属性:

| 属性            | 描述                                                       |
| :-------------- | :--------------------------------------------------------- |
| customError     | 设置为 true, 如果设置了自定义的 validity 信息。            |
| patternMismatch | 设置为 true, 如果元素的值不匹配它的模式属性。              |
| rangeOverflow   | 设置为 true, 如果元素的值大于设置的最大值。                |
| rangeUnderflow  | 设置为 true, 如果元素的值小于它的最小值。                  |
| stepMismatch    | 设置为 true, 如果元素的值不是按照规定的 step 属性设置。    |
| tooLong         | 设置为 true, 如果元素的值超过了 maxLength 属性设置的长度。 |
| typeMismatch    | 设置为 true, 如果元素的值不是预期相匹配的类型。            |
| valueMissing    | 设置为 true，如果元素 (required 属性) 没有值。             |
| valid           | 设置为 true，如果元素的值是合法的。                        |

### 实例

如果输入的值大于 100，显示一个信息：

rangeOverflow 属性
```html
<input id="id1" type="number" max="100">
<button onclick="myFunction()">验证</button>
 
<p id="demo"></p>
 
<script>
function myFunction() {
    var txt = "";
    if (document.getElementById("id1").validity.rangeOverflow) {
       txt = "输入的值太大了";
    }
    document.getElementById("demo").innerHTML = txt;
}
</script>
```

如果输入的值小于 100，显示一个信息：

rangeUnderflow 属性
```html
<input id="id1" type="number" min="100" required>
<button onclick="myFunction()">OK</button>
 
<p id="demo"></p>
 
<script>
function myFunction() {
    var txt = "";
    var inpObj = document.getElementById("id1");
    if(!isNumeric(inpObj.value)) {
        txt = "你输入的不是数字";
    } else if (inpObj.validity.rangeUnderflow) {
        txt = "输入的值太小了";
    } else {
        txt = "输入正确";
    }
    document.getElementById("demo").innerHTML = txt;
}
 
// 判断输入是否为数字
function isNumeric(n) {
    return !isNaN(parseFloat(n)) && isFinite(n);
}
</script>
```

## JavaScript 保留关键字

在 JavaScript 中，一些标识符是保留关键字，不能用作变量名或函数名。

### JavaScript 标准

所有的现代浏览器完全支持 ECMAScript 3（ES3，JavaScript 的第三版，从 1999 年开始）。

ECMAScript 4（ES4）未通过。

ECMAScript 5（ES5，2009 年发布），是 JavaScript 最新的官方版本。

随着时间的推移，我们开始看到，所有的现代浏览器已经完全支持 ES5。

### JavaScript 保留关键字

Javascript 的保留关键字不可以用作变量、标签或者函数名。有些保留关键字是作为 Javascript 以后扩展使用。

| | | | | |
| -------- | --------- | ---------- | --------- | ------------ |
| abstract | arguments | boolean    | break     | byte         |
| case     | catch     | char       | class*    | const        |
| continue | debugger  | default    | delete    | do           |
| double   | else      | enum*      | eval      | export*      |
| extends* | false     | final      | finally   | float        |
| for      | function  | goto       | if        | implements   |
| import*  | in        | instanceof | int       | interface    |
| let      | long      | native     | new       | null         |
| package  | private   | protected  | public    | return       |
| short    | static    | super*     | switch    | synchronized |
| this     | throw     | throws     | transient | true         |
| try      | typeof    | var        | void      | volatile     |
| while    | with      | yield      |           |              |

\* 标记的关键字是 ECMAScript5 中新添加的。

### JavaScript 对象、属性和方法

您也应该避免使用 JavaScript 内置的对象、属性和方法的名称作为 Javascript 的变量或函数名：

| Array     | Date     | eval     | function      | hasOwnProperty |
| --------- | -------- | -------- | ------------- | -------------- |
| Infinity  | isFinite | isNaN    | isPrototypeOf | length         |
| Math      | NaN      | name     | Number        | Object         |
| prototype | String   | toString | undefined     | valueOf        |

### Java 保留关键字

JavaScript 经常与 Java 一起使用。您应该避免使用一些 Java 对象和属性作为 JavaScript 标识符：

| getClass | java | JavaArray | javaClass | JavaObject | JavaPackage |
| -------- | ---- | --------- | --------- | ---------- | ----------- |
| | | | |

### Windows 保留关键字

JavaScript 可以在 HTML 外部使用。它可在许多其他应用程序中作为编程语言使用。

在 HTML 中，您必须（为了可移植性，您也应该这么做）避免使用 HTML 和 Windows 对象和属性的名称作为 Javascript 的变量及函数名：

| alert          | all                | anchor      | anchors            | area               |
| -------------- | ------------------ | ----------- | ------------------ | ------------------ |
| assign         | blur               | button      | checkbox           | clearInterval      |
| clearTimeout   | clientInformation  | close       | closed             | confirm            |
| constructor    | crypto             | decodeURI   | decodeURIComponent | defaultStatus      |
| document       | element            | elements    | embed              | embeds             |
| encodeURI      | encodeURIComponent | escape      | event              | fileUpload         |
| focus          | form               | forms       | frame              | innerHeight        |
| innerWidth     | layer              | layers      | link               | location           |
| mimeTypes      | navigate           | navigator   | frames             | frameRate          |
| hidden         | history            | image       | images             | offscreenBuffering |
| open           | opener             | option      | outerHeight        | outerWidth         |
| packages       | pageXOffset        | pageYOffset | parent             | parseFloat         |
| parseInt       | password           | pkcs11      | plugin             | prompt             |
| propertyIsEnum | radio              | reset       | screenX            | screenY            |
| scroll         | secure             | select      | self               | setInterval        |
| setTimeout     | status             | submit      | taint              | text               |
| textarea       | top                | unescape    | untaint            | window             |

### HTML 事件句柄

除此之外，您还应该避免使用 HTML 事件句柄的名称作为 Javascript 的变量及函数名。

实例：

| onblur    | onclick    | onerror     | onfocus     |
| --------- | ---------- | ----------- | ----------- |
| onkeydown | onkeypress | onkeyup     | onmouseover |
| onload    | onmouseup  | onmousedown | onsubmit    |

### 非标准 JavaScript

除了保留关键字，在 JavaScript 实现中也有一些非标准的关键字。

一个实例是 **const** 关键字，用于定义变量。 一些 JavaScript 引擎把 const 当作 var 的同义词。另一些引擎则把 const 当作只读变量的定义。

Const 是 JavaScript 的扩展。JavaScript 引擎支持它用在 Firefox 和 Chrome 中。但是它并不是 JavaScript 标准 ES3 或 ES5 的组成部分。**建议：不要使用它**。

## JavaScript this 关键字

面向对象语言中 this 表示当前对象的一个引用。

但在 JavaScript 中 this 不是固定不变的，它会随着执行环境的改变而改变。

- 在方法中，this 表示该方法所属的对象。
- 如果单独使用，this 表示全局对象。
- 在函数中，this 表示全局对象。
- 在函数中，在严格模式下，this 是未定义的(undefined)。
- 在事件中，this 表示接收事件的元素。
- 类似 call() 和 apply() 方法可以将 this 引用到任何对象。

```js
var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

### 方法中的 this

在对象方法中， this 指向调用它所在方法的对象。

在上面一个实例中，this 表示 person 对象。

fullName 方法所属的对象就是 person。

### 单独使用 this

单独使用 this，则它指向全局(Global)对象。

在浏览器中，window 就是该全局对象为 [object Window]:
```js
var x = this;
```

严格模式下，如果单独使用，this 也是指向全局(Global)对象。
```js
"use strict";
var x = this;
```

### 函数中使用 this（默认）
在函数中，函数的所属者默认绑定到 this 上。

在浏览器中，window 就是该全局对象为 [object Window]:
```js
function myFunction() {
  return this;
}
```

### 函数中使用 this（严格模式）

严格模式下函数是没有绑定到 this 上，这时候 this 是 undefined。
```js
"use strict";
function myFunction() {
  return this;
}
```

### 事件中的 this

在 HTML 事件句柄中，this 指向了接收事件的 HTML 元素：
```html
<button onclick="this.style.display='none'">
点我后我就消失了
</button>
```

### 对象方法中绑定

下面实例中，this 是 person 对象，person 对象是函数的所有者：
```js
var person = {
  firstName  : "John",
  lastName   : "Doe",
  id         : 5566,
  myFunction : function() {
    return this;
  }
};
```

```js
var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```
*说明: this.firstName 表示 this (person) 对象的 firstName 属性。*

### 显式函数绑定

在 JavaScript 中函数也是对象，对象则有方法，apply 和 call 就是函数对象的方法。这两个方法异常强大，他们允许切换函数执行的上下文环境（context），即 this 绑定的对象。

在下面实例中，当我们使用 person2 作为参数来调用 person1.fullName 方法时, this 将指向 person2, 即便它是 person1 的方法：
```js
var person1 = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
var person2 = {
  firstName:"John",
  lastName: "Doe",
}
person1.fullName.call(person2);  // 返回 "John Doe"
```
### 总结

this 的多种指向:

1. 在对象方法中， this 指向调用它所在方法的对象。
2. 单独使用 this，它指向全局(Global)对象。
3. 函数使用中，this 指向函数的所属者。
4. 严格模式下函数是没有绑定到 this 上，这时候 this 是 undefined。
5. 在 HTML 事件句柄中，this 指向了接收事件的 HTML 元素。
6. apply 和 call 允许切换函数执行的上下文环境（context），即 this 绑定的对象，可以将 this 引用到任何对象。

## JavaScript let 和 const

**ECMAScript 2015(ECMAScript 6)**

ES2015(ES6) 新增加了两个重要的 JavaScript 关键字: **let** 和 **const**。

let 声明的变量只在 let 命令所在的代码块内有效。

const 声明一个只读的常量，一旦声明，常量的值就不能改变。

在 ES6 之前，JavaScript 只有两种作用域：**全局变量**与**函数内的局部变量**。

### 全局变量

在函数外声明的变量作用域是全局的：
```js
var carName = "Volvo";
 
// 这里可以使用 carName 变量
 
function myFunction() {
    // 这里也可以使用 carName 变量
}
```
全局变量在 JavaScript 程序的任何地方都可以访问。

### 局部变量

在函数内声明的变量作用域是局部的（函数内）：
```js
// 这里不能使用 carName 变量
 
function myFunction() {
    var carName = "Volvo";
    // 这里可以使用 carName 变量
}
 
// 这里不能使用 carName 变量
```

函数内使用 var 声明的变量只能在函数内容访问，如果不使用 var 则是全局变量。

### JavaScript 块级作用域(Block Scope)

使用 var 关键字声明的变量不具备块级作用域的特性，它在 {} 外依然能被访问到。
```js
{ 
    var x = 2; 
}
// 这里可以使用 x 变量
```
在 ES6 之前，是没有块级作用域的概念的。

ES6 可以使用 let 关键字来实现块级作用域。

let 声明的变量只在 let 命令所在的代码块 {} 内有效，在 {} 之外不能访问。
```js
{ 
    let x = 2;
}
// 这里不能使用 x 变量
```

### 重新定义变量

使用 var 关键字重新声明变量可能会带来问题。

在块中重新声明变量也会重新声明块外的变量：
```js
var x = 10;
// 这里输出 x 为 10
{ 
    var x = 2;
    // 这里输出 x 为 2
}
// 这里输出 x 为 2
```

let 关键字就可以解决这个问题，因为它只在 let 命令所在的代码块 {} 内有效。
```js
var x = 10;
// 这里输出 x 为 10
{ 
    let x = 2;
    // 这里输出 x 为 2
}
// 这里输出 x 为 10
```

### 循环作用域

使用 var 关键字：
```js
var i = 5;
for (var i = 0; i < 10; i++) {
    // 一些代码...
}
// 这里输出 i 为 10
```

使用 let 关键字：
```js
let i = 5;
for (let i = 0; i < 10; i++) {
    // 一些代码...
}
// 这里输出 i 为 5
```

在第一个实例中，使用了 var 关键字，它声明的变量是全局的，包括循环体内与循环体外。

在第二个实例中，使用 let 关键字， 它声明的变量作用域只在循环体内，循环体外的变量不受影响。

### 局部变量

在函数体内使用 var 和 let 关键字声明的变量有点类似。

它们的作用域都是 局部的:
```js
// 使用 var
function myFunction() {
    var carName = "Volvo";   // 局部作用域
}

// 使用 let
function myFunction() {
    let carName = "Volvo";   //  局部作用域
}
```

### 全局变量

在函数体外或代码块外使用 var 和 let 关键字声明的变量也有点类似。

它们的作用域都是 全局的:
```js
// 使用 var
var x = 2;       // 全局作用域

// 使用 let
let x = 2;       // 全局作用域
```

### HTML 代码中使用全局变量

在 JavaScript 中, 全局作用域是针对 JavaScript 环境。

在 HTML 中, 全局作用域是针对 window 对象。

使用 var 关键字声明的全局作用域变量属于 window 对象:
```js
var carName = "Volvo";
// 可以使用 window.carName 访问变量
```

使用 let 关键字声明的全局作用域变量不属于 window 对象:
```jd
let carName = "Volvo";
// 不能使用 window.carName 访问变量
```

### 重置变量

使用 var 关键字声明的变量在任何地方都可以修改：
```js
var x = 2;
 
// x 为 2
 
var x = 3;
 
// 现在 x 为 3
```

在相同的作用域或块级作用域中，不能使用 let 关键字来重置 var 关键字声明的变量:
```js
var x = 2;       // 合法
let x = 3;       // 不合法

{
    var x = 4;   // 合法
    let x = 5   // 不合法
}
```

在相同的作用域或块级作用域中，不能使用 let 关键字来重置 let 关键字声明的变量:
```js
let x = 2;       // 合法
let x = 3;       // 不合法

{
    let x = 4;   // 合法
    let x = 5;   // 不合法
}
```

在相同的作用域或块级作用域中，不能使用 var 关键字来重置 let 关键字声明的变量:
```js
let x = 2;       // 合法
var x = 3;       // 不合法

{
    let x = 4;   // 合法
    var x = 5;   // 不合法
}
```

let 关键字在不同作用域，或不同块级作用域中是可以重新声明赋值的:
```js
let x = 2;       // 合法

{
    let x = 3;   // 合法
}

{
    let x = 4;   // 合法
}
```

### 变量提升

JavaScript 中，var 关键字定义的变量可以在使用后声明，也就是变量可以先使用再声明（[JavaScript 变量提升](https://www.runoob.com/js/js-hoisting.html)）。

```js
// 在这里可以使用 carName 变量

var carName;
```

let 关键字定义的变量则不可以在使用后声明，也就是变量需要先声明再使用。

```js
// 在这里不可以使用 carName 变量

let carName;
```

### const 关键字

const 用于声明一个或多个常量，声明时必须进行初始化，且初始化后值不可再修改：
```js
const PI = 3.141592653589793;
PI = 3.14;      // 报错
PI = PI + 10;   // 报错
```

`const`定义常量与使用`let` 定义的变量相似：

- 二者都是块级作用域
- 都不能和它所在作用域内的其他变量或函数拥有相同的名称

两者还有以下两点区别：

- `const`声明的常量必须初始化，而`let`声明的变量不用
- const 定义常量的值不能通过再赋值修改，也不能再次声明。而 let 定义的变量值可以修改。

```js
var x = 10;
// 这里输出 x 为 10
{ 
    const x = 2;
    // 这里输出 x 为 2
}
// 这里输出 x 为 10
```

### const的本质：并非真正的常量

const 的本质: const 定义的变量并非常量，并非不可变，它定义了一个常量引用一个值。使用 const 定义的对象或者数组，其实是可变的。下面的代码并不会报错：

//感觉一定程度上可以理解为指向变量的常指针

```js
// 创建常量对象
const car = {type:"Fiat", model:"500", color:"white"};
 
// 修改属性:
car.color = "red";
 
// 添加属性
car.owner = "Johnson";
```

//js真是自由奔放

但是我们不能对常量对象重新赋值：
```js
const car = {type:"Fiat", model:"500", color:"white"};
car = {type:"Volvo", model:"EX60", color:"red"};    // 错误
```

以下实例修改常量数组：
```js
// 创建常量数组
const cars = ["Saab", "Volvo", "BMW"];
 
// 修改元素
cars[0] = "Toyota";
 
// 添加元素
cars.push("Audi");
```

但是我们不能对常量数组重新赋值：
```js
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Toyota", "Volvo", "Audi"];    // 错误
```

### 重置变量

使用 **var** 关键字声明的变量在任何地方都可以修改：

#### 实例
```js
var x = 2;    //  合法 
var x = 3;    //  合法 
x = 4;        //  合法
```

在相同的作用域或块级作用域中，不能使用 **const** 关键字来重置 **var** 和 **let**关键字声明的变量:

```js
var x = 2;         // 合法
const x = 2;       // 不合法
{
    let x = 2;     // 合法
    const x = 2;   // 不合法
}
```

在相同的作用域或块级作用域中，不能使用 **const** 关键字来重置 **const** 关键字声明的变量:

```js
const x = 2;       // 合法
const x = 3;       // 不合法
x = 3;             // 不合法
var x = 3;         // 不合法
let x = 3;         // 不合法

{
    const x = 2;   // 合法
    const x = 3;   // 不合法
    x = 3;         // 不合法
    var x = 3;     // 不合法
    let x = 3;     // 不合法
}
```

**const** 关键字在不同作用域，或不同块级作用域中是可以重新声明赋值的:

```js
const x = 2;       // 合法

{
    const x = 3;   // 合法
}

{
    const x = 4;   // 合法
}
```

### 变量提升

JavaScript var 关键字定义的变量可以在使用后声明，也就是变量可以先使用再声明（[JavaScript 变量提升](https://www.runoob.com/js/js-hoisting.html)）。

```js
carName = "Volvo";    // 这里可以使用 carName 变量 
var carName;
```
const 关键字定义的变量则不可以在使用后声明，也就是变量需要先声明再使用。

```js
carName = "Volvo";    // 在这里不可以使用 carName 变量
const carName = "Volvo";
```

## JavaScript JSON

JSON 是用于存储和传输数据的格式。

JSON 通常用于服务端向网页传递数据 。

### 什么是 JSON?

- JSON 英文全称 JavaScript Object Notation
- JSON 是一种轻量级的数据交换格式。
- JSON是独立的语言 \*
- JSON 易于理解。

***JSON 使用 JavaScript 语法，但是 JSON 格式仅仅是一个文本。
文本可以被任何编程语言读取及作为数据格式传递。***

### JSON 实例

以下 JSON 语法定义了 sites 对象: 3 条网站信息（对象）的数组:
```json
{"sites":[
    {"name":"Runoob", "url":"www.runoob.com"}, 
    {"name":"Google", "url":"www.google.com"},
    {"name":"Taobao", "url":"www.taobao.com"}
]}
```

### JSON 格式化后为 JavaScript 对象

JSON 格式在语法上与创建 JavaScript 对象代码是相同的。

由于它们很相似，所以 JavaScript 程序可以很容易的将 JSON 数据转换为 JavaScript 对象。

### JSON 语法规则

- 数据为 键/值 对。
- 数据由逗号分隔。
- 大括号保存对象
- 方括号保存数组

### JSON 数据 - 一个名称对应一个值

JSON 数据格式为 键/值 对，就像 JavaScript 对象属性。

键/值对包括字段名称（在双引号中），后面一个冒号，然后是值：
```json
"name":"Runoob"
```

### JSON 对象

JSON 对象保存在大括号内。

就像在 JavaScript 中, 对象可以保存多个 键/值 对：

```json
{"name":"Runoob", "url":"www.runoob.com"}
```

### JSON 数组

JSON 数组保存在中括号内。

就像在 JavaScript 中, 数组可以包含对象：

```json
"sites":[
    {"name":"Runoob", "url":"www.runoob.com"}, 
    {"name":"Google", "url":"www.google.com"},
    {"name":"Taobao", "url":"www.taobao.com"}
]
```

在以上实例中，对象 "sites" 是一个数组，包含了三个对象。

每个对象为站点的信息（网站名和网站地址）。

### JSON 字符串转换为 JavaScript 对象

通常我们从服务器中读取 JSON 数据，并在网页中显示数据。

简单起见，我们网页中直接设置 JSON 字符串 (你还可以阅读我们的 JSON 教程):

首先，创建 JavaScript 字符串，字符串为 JSON 格式的数据：

```json
var text = '{ "sites" : [' +
'{ "name":"Runoob" , "url":"www.runoob.com" },' +
'{ "name":"Google" , "url":"www.google.com" },' +
'{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
```

然后，使用 JavaScript 内置函数 JSON.parse() 将字符串转换为 JavaScript 对象:

```js
var obj = JSON.parse(text);
```

最后，在你的页面中使用新的 JavaScript 对象：
```js
var text = '{ "sites" : [' +
    '{ "name":"Runoob" , "url":"www.runoob.com" },' +
    '{ "name":"Google" , "url":"www.google.com" },' +
    '{ "name":"Taobao" , "url":"www.taobao.com" } ]}';
    
obj = JSON.parse(text);
document.getElementById("demo").innerHTML = obj.sites[1].name + " " + obj.sites[1].url;
```

### 相关函数

| 函数                                                         | 描述                                           |
| :----------------------------------------------------------- | :--------------------------------------------- |
| [JSON.parse()](https://www.runoob.com/js/javascript-json-parse.html) | 用于将一个 JSON 字符串转换为 JavaScript 对象。 |
| [JSON.stringify()](https://www.runoob.com/js/javascript-json-stringify.html) | 用于将 JavaScript 值转换为 JSON 字符串。       |

更多 JSON 信息，你可以阅读我们的 [JSON 教程](https://www.runoob.com/json/json-tutorial.html)。

# JavaScript HTML DOM

## JavaScript HTML DOM 简介

通过 HTML DOM，可访问 JavaScript HTML 文档的所有元素。

### HTML DOM (文档对象模型)

当网页被加载时，浏览器会创建页面的文档对象模型（Document Object Model）。

HTML DOM 模型被构造为对象的树：

![](pic_htmltree.gif)

通过可编程的对象模型，JavaScript 获得了足够的能力来创建动态的 HTML。

- JavaScript 能够改变页面中的所有 HTML 元素
- JavaScript 能够改变页面中的所有 HTML 属性
- JavaScript 能够改变页面中的所有 CSS 样式
- JavaScript 能够对页面中的所有事件做出反应

### 查找 HTML 元素

通常，通过 JavaScript，您需要操作 HTML 元素。

为了做到这件事情，您必须首先找到该元素。有三种方法来做这件事：

- 通过 id 找到 HTML 元素
- 通过标签名找到 HTML 元素
- 通过类名找到 HTML 元素

### 通过 id 查找 HTML 元素

在 DOM 中查找 HTML 元素的最简单的方法，是通过使用元素的 id。

本例查找 id="intro" 元素：[示例](https://www.runoob.com/try/try.php?filename=try_dom_getelementbyid)

```js
var x=document.getElementById("intro");
```

如果找到该元素，则该方法将以对象（在 x 中）的形式返回该元素。

如果未找到该元素，则 x 将包含 null。

### 通过标签名查找 HTML 元素

本例查找 id="main" 的元素，然后查找 id="main" 元素中的所有 \<p> 元素：[示例](https://www.runoob.com/try/try.php?filename=try_dom_getelementsbytagname)

```js
var x=document.getElementById("main");
var y=x.getElementsByTagName("p");
```

### 通过类名找到 HTML 元素

本例通过 getElementsByClassName 函数来查找 class="intro" 的元素：[实例](https://www.runoob.com/try/try.php?filename=try_dom_getelementsbyclassname)

```js
var x=document.getElementsByClassName("intro");
```

### HTML DOM 教程

在本教程接下来的篇幅中，您将学到：

+ 如何改变 HTML 元素的内容 (innerHTML)
+ 如何改变 HTML 元素的样式 (CSS)
+ 如何对 HTML DOM 事件做出反应
+ 如何添加或删除 HTML 元素

## JavaScript HTML DOM - 改变 HTML

HTML DOM 允许 JavaScript 改变 HTML 元素的内容。

### 改变 HTML 输出流

JavaScript 能够创建动态的 HTML 内容：

今天的日期是： Sun Jun 28 2020 07:36:17 GMT+0800 (中国标准时间)

在 JavaScript 中，document.write() 可用于直接向 HTML 输出流写内容。

```html
<!DOCTYPE html>
<html>
	<body>
		<script>
			document.write(Date());
		</script>
	</body>
</html>
```

***绝对不要在文档(DOM)加载完成之后使用 document.write()。这会覆盖该文档。***

### 改变 HTML 内容

修改 HTML 内容的最简单的方法是使用 innerHTML 属性。

如需改变 HTML 元素的内容，请使用这个语法：

```js
document.getElementById(id).innerHTML=新的 HTML;
```

本例改变了 \<p>元素的内容：

```html
<html>
	<body>
		<p id="p1">Hello World!</p>
		<script>
			document.getElementById("p1").innerHTML="新文本!";
		</script>
	</body>
</html>
```

本例改变了 \<h1> 元素的内容：

```html
<!DOCTYPE html>
<html>
	<body>
		<h1 id="header">Old Header</h1>
		<script>
			var element=document.getElementById("header");
			element.innerHTML="新标题";
		</script>
	</body>
</html>
```

实例讲解：

- 上面的 HTML 文档含有 id="header" 的 \<h1> 元素

- 我们使用 HTML DOM 来获得 id="header" 的元素

- JavaScript 更改此元素的内容 (innerHTML)

### 改变 HTML 属性

如需改变 HTML 元素的属性，请使用这个语法：

```js
document.getElementById(id).attribute=新属性值;
```

本例改变了 \<img> 元素的 src 属性：

```html
<!DOCTYPE html>
<html>
	<body>
		<img id="image" src="smiley.gif">
		<script>
			document.getElementById("image").src="landscape.jpg";
		</script>
	</body>
</html>
```

实例讲解：

- 上面的 HTML 文档含有 id="image" 的 \<img> 元素
- 我们使用 HTML DOM 来获得 id="image" 的元素
- JavaScript 更改此元素的属性（把 "smiley.gif" 改为 "landscape.jpg"）

## JavaScript HTML DOM - 改变CSS

HTML DOM 允许 JavaScript 改变 HTML 元素的样式。

### 改变 HTML 样式

如需改变 HTML 元素的样式，请使用这个语法：

```js
document.getElementById(id).style.property=新样式;
```

下面的例子会改变 \<p> 元素的样式：

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>菜鸟教程(runoob.com)</title>
	</head>
	<body>
		<p id="p1">Hello World!</p>
		<p id="p2">Hello World!</p>
		<script>
			document.getElementById("p2").style.color="blue";
			document.getElementById("p2").style.fontFamily="Arial";
			document.getElementById("p2").style.fontSize="larger";
		</script>
		<p>以上段落通过脚本修改。</p>
	</body>
</html>
```

### 使用事件

HTML DOM 允许我们通过触发事件来执行代码。

比如以下事件：

- 元素被点击。
- 页面加载完成。
- 输入框被修改。
- ……
- 
在接下来的章节，你会学到更多关于事件的知识。

本例改变了 id="id1" 的 HTML 元素的样式，当用户点击按钮时：[示例](https://www.runoob.com/try/try.php?filename=trydhtml_dom_color2)

```html
<!DOCTYPE html>
<html>
	<body>
		<h1 id="id1">我的标题 1</h1>
		<button type="button"
		onclick="document.getElementById('id1').style.color='red'">
		点我!</button>
	</body>
</html>
```

## JavaScript HTML DOM 事件

HTML DOM 使 JavaScript 有能力对 HTML 事件做出反应。

### 对事件做出反应

我们可以在事件发生时执行 JavaScript，比如当用户在 HTML 元素上点击时。

如需在用户点击某个元素时执行代码，请向一个 HTML 事件属性添加 JavaScript 代码：
```
onclick=JavaScript;
```

HTML 事件的例子：

- 当用户点击鼠标时
- 当网页已加载时
- 当图像已加载时
- 当鼠标移动到元素上时
- 当输入字段被改变时
- 当提交 HTML 表单时
- 当用户触发按键时

在本例中，当用户在 \<h1> 元素上点击时，会改变其内容：

```html
<!DOCTYPE html>
<html>
	<body>
		<h1 onclick="this.innerHTML='Ooops!'">点击文本!</h1>
	</body>
</html>
```

本例从事件处理器调用一个函数：

```html
<!DOCTYPE html>
<html>
	<head>
		<script>
		function changetext(id)
		{
			id.innerHTML="Ooops!";
		}
		</script>
	</head>
	<body>
		<h1 onclick="changetext(this)">点击文本!</h1>
	</body>
</html>
```

### HTML 事件属性

如需向 HTML 元素分配 事件，您可以使用事件属性。[示例](https://www.runoob.com/try/try.php?filename=tryjs_events1)

```html
<button onclick="displayDate()">点这里</button>
```

在上面的例子中，名为 displayDate 的函数将在按钮被点击时执行。

### 使用 HTML DOM 来分配事件

HTML DOM 允许您使用 JavaScript 来向 HTML 元素分配事件：

[向 button 元素分配 onclick 事件：](https://www.runoob.com/try/try.php?filename=tryjs_events2)
```html
<script>
document.getElementById("myBtn").onclick=function(){displayDate()};
</script>
```

在上面的例子中，名为 displayDate 的函数被分配给 id="myBtn" 的 HTML 元素。

按钮点击时Javascript函数将会被执行。

### onload 和 onunload 事件

onload 和 onunload 事件会在用户进入或离开页面时被触发。

onload 事件可用于检测访问者的浏览器类型和浏览器版本，并基于这些信息来加载网页的正确版本。

onload 和 onunload 事件可用于处理 cookie。[示例](https://www.runoob.com/try/try.php?filename=tryjs_events_onload)

```html
<body onload="checkCookies()">
```

### onchange 事件

onchange 事件常结合对输入字段的验证来使用。

下面是一个如何使用 onchange 的例子。当用户改变输入字段的内容时，会调用 upperCase() 函数。[示例](https://www.runoob.com/try/try.php?filename=tryjsref_onchange)
```html
<input type="text" id="fname" onchange="upperCase()">
```

### onmouseover 和 onmouseout 事件

onmouseover 和 onmouseout 事件可用于在用户的鼠标移至 HTML 元素上方或移出元素时触发函数。[示例](https://www.runoob.com/try/try.php?filename=tryjs_events_mouseover)

### onmousedown、onmouseup 以及 onclick 事件

onmousedown, onmouseup 以及 onclick 构成了鼠标点击事件的所有部分。首先当点击鼠标按钮时，会触发 onmousedown 事件，当释放鼠标按钮时，会触发 onmouseup 事件，最后，当完成鼠标点击时，会触发 onclick 事件。[示例](https://www.runoob.com/try/try.php?filename=trydhtml_event_onmousedown)

### 示例一：onload

```html
<body onload="mymessage()"></body>
```

[onload](https://www.runoob.com/try/try.php?filename=trydhtml_event_onload)
当页面完成加载时，显示一个提示框。

### 示例二：onfocus

```html
<input type="text" onfocus="myFunction(this)">
```

[onfocus](https://www.runoob.com/try/try.php?filename=tryjsref_onfocus)
当输入字段获得焦点时，改变其背景色。

### 示例三：onmouseover-onmouseout

```html
<h1 onmouseover="style.color='red'"onmouseout="style.color='black'">将鼠标移至文部上</h1>
```

[鼠标事件](https://www.runoob.com/try/try.php?filename=trydhtml_event_onmouse)
当指针移动到元素上方时，改变其颜色；当指针移出文本后，会再次改变其颜色。

## JavaScript HTML DOM EventListener

### addEventListener() 方法

```js
document.getElementById("myBtn").addEventListener("click", displayDate);
```

addEventListener() 方法用于向指定元素添加事件句柄。

addEventListener() 方法添加的事件句柄不会覆盖已存在的事件句柄。

你可以向一个元素添加多个事件句柄。

你可以向同个元素添加多个同类型的事件句柄，如：两个 "click" 事件。

你可以向任何 DOM 对象添加事件监听，不仅仅是 HTML 元素。如： window 对象。

addEventListener() 方法可以更简单的控制事件（冒泡与捕获）。

当你使用 addEventListener() 方法时, JavaScript 从 HTML 标记中分离开来，可读性更强， 在没有控制HTML标记时也可以添加事件监听。

你可以使用 removeEventListener() 方法来移除事件的监听。

### 语法

```js
element.addEventListener(event, function, useCapture);
```

第一个参数是事件的类型 (如 "click" 或 "mousedown").

第二个参数是事件触发后调用的函数。

第三个参数是个布尔值用于描述事件是冒泡还是捕获。该参数是可选的。

*注意:不要使用 "on" 前缀。 例如，使用 "click" ,而不是使用 "onclick"。*

### 向原元素添加事件句柄

当用户点击元素时弹出 "Hello World!" :[示例](https://www.runoob.com/try/try.php?filename=tryjs_addeventlistener_add)
```js
element.addEventListener("click", function(){ alert("Hello World!"); });
```

你可以使用函数名，来引用外部函数:
```js
element.addEventListener("click", myFunction);

function myFunction() {
    alert ("Hello World!");
}
```

### 向同一个元素中添加多个事件句柄

addEventListener() 方法允许向同一个元素添加多个事件，且不会覆盖已存在的事件：
```js
element.addEventListener("click", myFunction);
element.addEventListener("click", mySecondFunction);
```

你可以向同个元素添加不同类型的事件：
```js
element.addEventListener("mouseover", myFunction);
element.addEventListener("click", mySecondFunction);
element.addEventListener("mouseout", myThirdFunction);
```

### 向 Window 对象添加事件句柄

addEventListener() 方法允许你在 HTML DOM 对象添加事件监听， HTML DOM 对象如： HTML 元素, HTML 文档, window 对象。或者其他支出的事件对象如: xmlHttpRequest 对象。

当用户重置窗口大小时添加事件监听：
```js
window.addEventListener("resize", function(){
	document.getElementById("demo").innerHTML = sometext;
});
```

### 传递参数

当传递参数值时，使用"匿名函数"调用带参数的函数：
```js
element.addEventListener("click", function(){ myFunction(p1, p2); });
```

### 事件冒泡或事件捕获？

事件传递有两种方式：冒泡与捕获。

事件传递定义了元素事件触发的顺序。 如果你将 \<p> 元素插入到 \<div> 元素中，用户点击\<p> 元素, 哪个元素的 "click" 事件先被触发呢？

- 在*冒泡*中，内部元素的事件会先被触发，然后再触发外部元素，即： \<p> 元素的点击事件先触发，然后会触发 \<div> 元素的点击事件。为默认值false。

- 在*捕获*中，外部元素的事件会先被触发，然后才会触发内部元素的事件，即： \<div> 元素的点击事件先触发 ，然后再触发 \<p> 元素的点击事件。值为true。

addEventListener() 方法可以指定 "useCapture" 参数来设置传递类型：

```js
addEventListener(event, function, useCapture);
```

默认值为 false, 即冒泡传递，当值为 true 时, 事件使用捕获传递。

```js
document.getElementById("myDiv").addEventListener("click", myFunction, true);
```

### removeEventListener() 方法

removeEventListener() 方法移除由 addEventListener() 方法添加的事件句柄:

```js
element.removeEventListener("mousemove", myFunction);
```

### 浏览器支持

注意： IE 8 及更早 IE 版本，Opera 7.0及其更早版本不支持 addEventListener() 和 removeEventListener() 方法。但是，对于这类浏览器版本可以使用 detachEvent() 方法来移除事件句柄:

```js
element.attachEvent(event, function);
element.detachEvent(event, function);
```

[跨浏览器解决方法:](https://www.runoob.com/try/try.php?filename=tryjs_addeventlistener_crossbrowser)
```
var x = document.getElementById("myBtn");
if (x.addEventListener) {                    // 所有主流浏览器，除了 IE 8 及更早版本
    x.addEventListener("click", myFunction);
} else if (x.attachEvent) {                  // IE 8 及更早版本
    x.attachEvent("onclick", myFunction);
}
```

### HTML DOM 事件

HTML DOM 事件允许Javascript在HTML文档元素中注册不同事件处理程序。

事件通常与函数结合使用，函数不会在事件发生前被执行！ (如用户点击按钮)。

提示： 在 W3C 2 级 DOM 事件中规范了事件模型。

### HTML DOM 事件列表：

DOM： 指明使用的 DOM 属性级别

#### 鼠标事件

| 属性                                                         | 描述                                   | DOM  |
| :----------------------------------------------------------- | :------------------------------------- | :--- |
| [onclick](https://www.runoob.com/jsref/event-onclick.html)   | 当用户点击某个对象时调用的事件句柄。   | 2    |
| [oncontextmenu](https://www.runoob.com/jsref/event-oncontextmenu.html) | 在用户点击鼠标右键打开上下文菜单时触发 |      |
| [ondblclick](https://www.runoob.com/jsref/event-ondblclick.html) | 当用户双击某个对象时调用的事件句柄。   | 2    |
| [onmousedown](https://www.runoob.com/jsref/event-onmousedown.html) | 鼠标按钮被按下。                       | 2    |
| [onmouseenter](https://www.runoob.com/jsref/event-onmouseenter.html) | 当鼠标指针移动到元素上时触发。         | 2    |
| [onmouseleave](https://www.runoob.com/jsref/event-onmouseleave.html) | 当鼠标指针移出元素时触发               | 2    |
| [onmousemove](https://www.runoob.com/jsref/event-onmousemove.html) | 鼠标被移动。                           | 2    |
| [onmouseover](https://www.runoob.com/jsref/event-onmouseover.html) | 鼠标移到某元素之上。                   | 2    |
| [onmouseout](https://www.runoob.com/jsref/event-onmouseout.html) | 鼠标从某元素移开。                     | 2    |
| [onmouseup](https://www.runoob.com/jsref/event-onmouseup.html) | 鼠标按键被松开。                       | 2    |

#### 键盘事件

| 属性                                                         | 描述                       | DOM  |
| :----------------------------------------------------------- | :------------------------- | :--- |
| [onkeydown](https://www.runoob.com/jsref/event-onkeydown.html) | 某个键盘按键被按下。       | 2    |
| [onkeypress](https://www.runoob.com/jsref/event-onkeypress.html) | 某个键盘按键被按下并松开。 | 2    |
| [onkeyup](https://www.runoob.com/jsref/event-onkeyup.html)   | 某个键盘按键被松开。       | 2    |

#### 框架/对象（Frame/Object）事件

| 属性                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [onabort](https://www.runoob.com/jsref/event-onabort.html)   | 图像的加载被中断。 ( \<object>)                               | 2    |
| [onbeforeunload](https://www.runoob.com/jsref/event-onbeforeunload.html) | 该事件在即将离开页面（刷新或关闭）时触发                     | 2    |
| [onerror](https://www.runoob.com/jsref/event-onerror.html)   | 在加载文档或图像时发生错误。 ( \<object>, \<body>和 \<frameset>) |      |
| [onhashchange](https://www.runoob.com/jsref/event-onhashchange.html) | 该事件在当前 URL 的锚部分发生修改时触发。                    |      |
| [onload](https://www.runoob.com/jsref/event-onload.html)     | 一张页面或一幅图像完成加载。                                 | 2    |
| [onpageshow](https://www.runoob.com/jsref/event-onpageshow.html) | 该事件在用户访问页面时触发                                   |      |
| [onpagehide](https://www.runoob.com/jsref/event-onpagehide.html) | 该事件在用户离开当前网页跳转到另外一个页面时触发             |      |
| [onresize](https://www.runoob.com/jsref/event-onresize.html) | 窗口或框架被重新调整大小。                                   | 2    |
| [onscroll](https://www.runoob.com/jsref/event-onscroll.html) | 当文档被滚动时发生的事件。                                   | 2    |
| [onunload](https://www.runoob.com/jsref/event-onunload.html) | 用户退出页面。 ( \<body> 和 \<frameset>)                       | 2    |

#### 表单事件

| 属性                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [onblur](https://www.runoob.com/jsref/event-onblur.html)     | 元素失去焦点时触发                                           | 2    |
| [onchange](https://www.runoob.com/jsref/event-onchange.html) | 该事件在表单元素的内容改变时触发( \<input>, \<keygen>, \<select>, 和 \<textarea>) | 2    |
| [onfocus](https://www.runoob.com/jsref/event-onfocus.html)   | 元素获取焦点时触发                                           | 2    |
| [onfocusin](https://www.runoob.com/jsref/event-onfocusin.html) | 元素即将获取焦点时触发                                       | 2    |
| [onfocusout](https://www.runoob.com/jsref/event-onfocusout.html) | 元素即将失去焦点时触发                                       | 2    |
| [oninput](https://www.runoob.com/jsref/event-oninput.html)   | 元素获取用户输入时触发                                       | 3    |
| [onreset](https://www.runoob.com/jsref/event-onreset.html)   | 表单重置时触发                                               | 2    |
| [onsearch](https://www.runoob.com/jsref/event-onsearch.html) | 用户向搜索域输入文本时触发 ( <input="search">)               |      |
| [onselect](https://www.runoob.com/jsref/event-onselect.html) | 用户选取文本时触发 ( \<input> 和 \<textarea>)                  | 2    |
| [onsubmit](https://www.runoob.com/jsref/event-onsubmit.html) | 表单提交时触发                                               | 2    |

#### 剪贴板事件

| 属性                                                       | 描述                           | DOM  |
| :--------------------------------------------------------- | :----------------------------- | :--- |
| [oncopy](https://www.runoob.com/jsref/event-oncopy.html)   | 该事件在用户拷贝元素内容时触发 |      |
| [oncut](https://www.runoob.com/jsref/event-oncut.html)     | 该事件在用户剪切元素内容时触发 |      |
| [onpaste](https://www.runoob.com/jsref/event-onpaste.html) | 该事件在用户粘贴元素内容时触发 |      |

#### 打印事件

| 属性                                                         | 描述                                                 | DOM  |
| :----------------------------------------------------------- | :--------------------------------------------------- | :--- |
| [onafterprint](https://www.runoob.com/jsref/event-onafterprint.html) | 该事件在页面已经开始打印，或者打印窗口已经关闭时触发 |      |
| [onbeforeprint](https://www.runoob.com/jsref/event-onbeforeprint.html) | 该事件在页面即将开始打印时触发                       |      |

#### 拖动事件

| 事件                                                         | 描述                                 | DOM  |
| :----------------------------------------------------------- | :----------------------------------- | :--- |
| [ondrag](https://www.runoob.com/jsref/event-ondrag.html)     | 该事件在元素正在拖动时触发           |      |
| [ondragend](https://www.runoob.com/jsref/event-ondragend.html) | 该事件在用户完成元素的拖动时触发     |      |
| [ondragenter](https://www.runoob.com/jsref/event-ondragenter.html) | 该事件在拖动的元素进入放置目标时触发 |      |
| [ondragleave](https://www.runoob.com/jsref/event-ondragleave.html) | 该事件在拖动元素离开放置目标时触发   |      |
| [ondragover](https://www.runoob.com/jsref/event-ondragover.html) | 该事件在拖动元素在放置目标上时触发   |      |
| [ondragstart](https://www.runoob.com/jsref/event-ondragstart.html) | 该事件在用户开始拖动元素时触发       |      |
| [ondrop](https://www.runoob.com/jsref/event-ondrop.html)     | 该事件在拖动元素放置在目标区域时触发 |      |

#### 多媒体（Media）事件

| 事件                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [onabort](https://www.runoob.com/jsref/event-onabort-media.html) | 事件在视频/音频（audio/video）终止加载时触发。               |      |
| [oncanplay](https://www.runoob.com/jsref/event-oncanplay.html) | 事件在用户可以开始播放视频/音频（audio/video）时触发。       |      |
| [oncanplaythrough](https://www.runoob.com/jsref/event-oncanplaythrough.html) | 事件在视频/音频（audio/video）可以正常播放且无需停顿和缓冲时触发。 |      |
| [ondurationchange](https://www.runoob.com/jsref/event-ondurationchange.html) | 事件在视频/音频（audio/video）的时长发生变化时触发。         |      |
| onemptied                                                    | 当期播放列表为空时触发                                       |      |
| [onended](https://www.runoob.com/jsref/event-onended.html)   | 事件在视频/音频（audio/video）播放结束时触发。               |      |
| [onerror](https://www.runoob.com/jsref/event-onerror-media.html) | 事件在视频/音频（audio/video）数据加载期间发生错误时触发。   |      |
| [onloadeddata](https://www.runoob.com/jsref/event-onloadeddata.html) | 事件在浏览器加载视频/音频（audio/video）当前帧时触发触发。   |      |
| [onloadedmetadata](https://www.runoob.com/jsref/event-onloadedmetadata.html) | 事件在指定视频/音频（audio/video）的元数据加载后触发。       |      |
| [onloadstart](https://www.runoob.com/jsref/event-onloadstart.html) | 事件在浏览器开始寻找指定视频/音频（audio/video）触发。       |      |
| [onpause](https://www.runoob.com/jsref/event-onpause.html)   | 事件在视频/音频（audio/video）暂停时触发。                   |      |
| [onplay](https://www.runoob.com/jsref/event-onplay.html)     | 事件在视频/音频（audio/video）开始播放时触发。               |      |
| [onplaying](https://www.runoob.com/jsref/event-onplaying.html) | 事件在视频/音频（audio/video）暂停或者在缓冲后准备重新开始播放时触发。 |      |
| [onprogress](https://www.runoob.com/jsref/event-onprogress.html) | 事件在浏览器下载指定的视频/音频（audio/video）时触发。       |      |
| [onratechange](https://www.runoob.com/jsref/event-onratechange.html) | 事件在视频/音频（audio/video）的播放速度发送改变时触发。     |      |
| [onseeked](https://www.runoob.com/jsref/event-onseeked.html) | 事件在用户重新定位视频/音频（audio/video）的播放位置后触发。 |      |
| [onseeking](https://www.runoob.com/jsref/event-onseeking.html) | 事件在用户开始重新定位视频/音频（audio/video）时触发。       |      |
| [onstalled](https://www.runoob.com/jsref/event-onstalled.html) | 事件在浏览器获取媒体数据，但媒体数据不可用时触发。           |      |
| [onsuspend](https://www.runoob.com/jsref/event-onsuspend.html) | 事件在浏览器读取媒体数据中止时触发。                         |      |
| [ontimeupdate](https://www.runoob.com/jsref/event-ontimeupdate.html) | 事件在当前的播放位置发送改变时触发。                         |      |
| [onvolumechange](https://www.runoob.com/jsref/event-onvolumechange.html) | 事件在音量发生改变时触发。                                   |      |
| [onwaiting](https://www.runoob.com/jsref/event-onwaiting.html) | 事件在视频由于要播放下一帧而需要缓冲时触发。                 |      |

#### 动画事件

| 事件                                                         | 描述                            | DOM  |
| :----------------------------------------------------------- | :------------------------------ | :--- |
| [animationend](https://www.runoob.com/jsref/event-animationend.html) | 该事件在 CSS 动画结束播放时触发 |      |
| [animationiteration](https://www.runoob.com/jsref/event-animationiteration.html) | 该事件在 CSS 动画重复播放时触发 |      |
| [animationstart](https://www.runoob.com/jsref/event-animationstart.html) | 该事件在 CSS 动画开始播放时触发 |      |

#### 过渡事件

| 事件                                                         | 描述                          | DOM  |
| :----------------------------------------------------------- | :---------------------------- | :--- |
| [transitionend](https://www.runoob.com/jsref/event-transitionend.html) | 该事件在 CSS 完成过渡后触发。 |      |

#### 其他事件

| 事件                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| onmessage                                                    | 该事件通过或者从对象(WebSocket, Web Worker, Event Source 或者子 frame 或父窗口)接收到消息时触发 |      |
| onmousewheel                                                 | 已废弃。 使用 [onwheel](https://www.runoob.com/jsref/event-onwheel.html) 事件替代 |      |
| [ononline](https://www.runoob.com/jsref/event-ononline.html) | 该事件在浏览器开始在线工作时触发。                           |      |
| [onoffline](https://www.runoob.com/jsref/event-onoffline.html) | 该事件在浏览器开始离线工作时触发。                           |      |
| onpopstate                                                   | 该事件在窗口的浏览历史（history 对象）发生改变时触发。       |      |
| [onshow](https://www.runoob.com/jsref/event-onshow.html)     | 该事件当 \<menu> 元素在上下文菜单显示时触发                   |      |
| onstorage                                                    | 该事件在 Web Storage(HTML 5 Web 存储)更新时触发              |      |
| [ontoggle](https://www.runoob.com/jsref/event-ontoggle.html) | 该事件在用户打开或关闭 \<details> 元素时触发                  |      |
| [onwheel](https://www.runoob.com/jsref/event-onwheel.html)   | 该事件在鼠标滚轮在元素上下滚动时触发                         |      |

#### 事件对象

##### 常量

| 静态变量        | 描述                                 | DOM  |
| :-------------- | :----------------------------------- | :--- |
| CAPTURING-PHASE | 当前事件阶段为捕获阶段(1)            | 1    |
| AT-TARGET       | 当前事件是目标阶段,在评估目标事件(1) | 2    |
| BUBBLING-PHASE  | 当前的事件为冒泡阶段 (3)             | 3    |

##### 属性

| 属性                                                         | 描述                                           | DOM  |
| :----------------------------------------------------------- | :--------------------------------------------- | :--- |
| [bubbles](https://www.runoob.com/jsref/event-bubbles.html)   | 返回布尔值，指示事件是否是起泡事件类型。       | 2    |
| [cancelable](https://www.runoob.com/jsref/event-cancelable.html) | 返回布尔值，指示事件是否可拥可取消的默认动作。 | 2    |
| [currentTarget](https://www.runoob.com/jsref/event-currenttarget.html) | 返回其事件监听器触发该事件的元素。             | 2    |
| eventPhase                                                   | 返回事件传播的当前阶段。                       | 2    |
| [target](https://www.runoob.com/jsref/event-target.html)     | 返回触发此事件的元素（事件的目标节点）。       | 2    |
| [timeStamp](https://www.runoob.com/jsref/event-timestamp.html) | 返回事件生成的日期和时间。                     | 2    |
| [type](https://www.runoob.com/jsref/event-type.html)         | 返回当前 Event 对象表示的事件的名称。          | 2    |

##### 方法

| 方法              | 描述                                     | DOM  |
| :---------------- | :--------------------------------------- | :--- |
| initEvent()       | 初始化新创建的 Event 对象的属性。        | 2    |
| preventDefault()  | 通知浏览器不要执行与事件关联的默认动作。 | 2    |
| stopPropagation() | 不再派发事件。                           | 2    |

#### 目标事件对象

##### 方法

| 方法                  | 描述                                                    | DOM  |
| :-------------------- | :------------------------------------------------------ | :--- |
| addEventListener()    | 允许在目标事件中注册监听事件(IE8 = attachEvent())       | 2    |
| dispatchEvent()       | 允许发送事件到监听器上 (IE8 = fireEvent())              | 2    |
| removeEventListener() | 运行一次注册在事件目标上的监听事件(IE8 = detachEvent()) | 2    |

#### 事件监听对象

##### 方法

| 方法          | 描述                         | DOM  |
| :------------ | :--------------------------- | :--- |
| handleEvent() | 把任意对象注册为事件处理程序 | 2    |

#### 文档事件对象

##### 方法

| 方法          | 描述 | DOM  |
| :------------ | :--- | :--- |
| createEvent() |      | 2    |

#### 鼠标/键盘事件对象

##### 属性

| 属性                                                         | 描述                                                         | DOM  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :--- |
| [altKey](https://www.runoob.com/jsref/event-altkey.html)     | 返回当事件被触发时，"ALT" 是否被按下。                       | 2    |
| [button](https://www.runoob.com/jsref/event-button.html)     | 返回当事件被触发时，哪个鼠标按钮被点击。                     | 2    |
| [clientX](https://www.runoob.com/jsref/event-clientx.html)   | 返回当事件被触发时，鼠标指针的水平坐标。                     | 2    |
| [clientY](https://www.runoob.com/jsref/event-clienty.html)   | 返回当事件被触发时，鼠标指针的垂直坐标。                     | 2    |
| [ctrlKey](https://www.runoob.com/jsref/event-ctrlkey.html)   | 返回当事件被触发时，"CTRL" 键是否被按下。                    | 2    |
| [Location](https://www.runoob.com/jsref/event-key-location.html) | 返回按键在设备上的位置                                       | 3    |
| [charCode](https://www.runoob.com/jsref/event-key-charcode.html) | 返回onkeypress事件触发键值的字母代码。                       | 2    |
| [key](https://www.runoob.com/jsref/event-key-key.html)       | 在按下按键时返回按键的标识符。                               | 3    |
| [keyCode](https://www.runoob.com/jsref/event-key-keycode.html) | 返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码。 | 2    |
| [which](https://www.runoob.com/jsref/event-key-which.html)   | 返回onkeypress事件触发的键的值的字符代码，或者 onkeydown 或 onkeyup 事件的键的代码。 | 2    |
| [metaKey](https://www.runoob.com/jsref/event-metakey.html)   | 返回当事件被触发时，"meta" 键是否被按下。                    | 2    |
| [relatedTarget](https://www.runoob.com/jsref/event-relatedtarget.html) | 返回与事件的目标节点相关的节点。                             | 2    |
| [screenX](https://www.runoob.com/jsref/event-screenx.html)   | 返回当某个事件被触发时，鼠标指针的水平坐标。                 | 2    |
| [screenY](https://www.runoob.com/jsref/event-screeny.html)   | 返回当某个事件被触发时，鼠标指针的垂直坐标。                 | 2    |
| [shiftKey](https://www.runoob.com/jsref/event-shiftkey.html) | 返回当事件被触发时，"SHIFT" 键是否被按下。                   | 2    |

##### 方法

| 方法                | 描述                   | W3C  |
| :------------------ | :--------------------- | :--- |
| initMouseEvent()    | 初始化鼠标事件对象的值 | 2    |
| initKeyboardEvent() | 初始化键盘事件对象的值 | 3    |

## JavaScript HTML DOM 元素 (节点)

本章节介绍如何向文档中添加和移除元素(节点)。

### 创建新的 HTML 元素 (节点) - appendChild()

要创建新的 HTML 元素 (节点)需要先创建一个元素，然后在已存在的元素中添加它。

```html
<div id="div1">
	<p id="p1">这是一个段落。</p>
	<p id="p2">这是另外一个段落。</p>
</div>
<script>
	var para = document.createElement("p");
	var node = document.createTextNode("这是一个新的段落。");
	para.appendChild(node);
	var element = document.getElementById("div1");
	element.appendChild(para);
</script>
```

### 实例解析

以下代码是用于创建 \<p> 元素:
```js
var para = document.createElement("p");
```

为 \<p> 元素创建一个新的文本节点：
```js
var node = document.createTextNode("这是一个新的段落。");
```

将文本节点添加到 \<p> 元素中：
```js
para.appendChild(node);
```

最后，在一个已存在的元素中添加 p 元素。

查找已存在的元素：
```js
var element = document.getElementById("div1");
```

添加到已存在的元素中:
```js
element.appendChild(para);
```

### 创建新的 HTML 元素 (节点) - insertBefore()

以上的实例我们使用了 appendChild() 方法，它用于添加新元素到尾部。

如果我们需要将新元素添加到开始位置，可以使用 insertBefore() 方法:
```html
<div id="div1">
	<p id="p1">这是一个段落。</p>
	<p id="p2">这是另外一个段落。</p>
</div>
<script>
	var para = document.createElement("p");
	var node = document.createTextNode("这是一个新的段落。");
	para.appendChild(node);
	var element = document.getElementById("div1");
	var child = document.getElementById("p1");
	element.insertBefore(para, child);
</script>
```

### 移除已存在的元素

要移除一个元素，你需要知道该元素的父元素。

```html
<div id="div1">
	<p id="p1">这是一个段落。</p>
	<p id="p2">这是另外一个段落。</p>
</div>
<script>
	var parent = document.getElementById("div1");
	var child = document.getElementById("p1");
	parent.removeChild(child);
</script>
```

*注意：早期的 Internet Explorer 浏览器不支持 node.remove() 方法。*

#### 实例解析

HTML 文档中 \<div> 元素包含两个子节点 (两个 \<p> 元素):

```html
<div id="div1">
<p id="p1">这是一个段落。</p>
<p id="p2">这是另外一个段落。</p>
</div>
```

查找 id="div1" 的元素:

```js
var parent = document.getElementById("div1");
```

查找 id="p1" 的 \<p> 元素:

```js
var child = document.getElementById("p1");
```

从父元素中移除子节点：

```js
parent.removeChild(child);
```

*如果能够在不引用父元素的情况下删除某个元素，就太好了。
不过很遗憾。DOM 需要清楚您需要删除的元素，以及它的父元素。*

以下代码是已知要查找的子元素，然后查找其父元素，再删除这个子元素（删除节点必须知道父节点）：

```js
var child = document.getElementById("p1");
child.parentNode.removeChild(child);
```

### 替换 HTML 元素 - replaceChild()

我们可以使用 replaceChild() 方法来替换 HTML DOM 中的元素。

```html
<div id="div1">
	<p id="p1">这是一个段落。</p>
	<p id="p2">这是另外一个段落。</p>
</div>
<script>
	var para = document.createElement("p");
	var node = document.createTextNode("这是一个新的段落。");
	para.appendChild(node);
	var parent = document.getElementById("div1");
	var child = document.getElementById("p1");
	parent.replaceChild(para, child);
</script>
```

### HTML DOM 教程

在我们的 JavaScript 教程的 HTML DOM 部分，您已经学到了：

- 如何改变 HTML 元素的内容 (innerHTML)
- 如何改变 HTML 元素的样式 (CSS)
- 如何对 HTML DOM 事件作出反应
- 如何添加或删除 HTML 元素

如果您希望学到更多有关使用 JavaScript 访问 HTML DOM 的知识，请访问我们完整的 [HTML DOM 教程](https://www.runoob.com/htmldom/htmldom-tutorial.html)。

## JavaScript HTML DOM 集合(Collection)

本章节介绍 DOM 集合的使用。

### HTMLCollection 对象

getElementsByTagName() 方法返回 HTMLCollection 对象。

HTMLCollection 对象类似包含 HTML 元素的一个数组。

以下代码获取文档所有的 \<p> 元素：

```js
var x = document.getElementsByTagName("p");
```

集合中的元素可以通过索引(以 0 为起始位置)来访问。

访问第二个 \<p> 元素可以是以下代码:

```js
y = x[1];
```

### HTMLCollection 对象 length 属性

HTMLCollection 对象的 length 属性定义了集合中元素的数量。

```js
var myCollection = document.getElementsByTagName("p");
document.getElementById("demo").innerHTML = myCollection.length;
```

#### 实例解析

获取 \<p> 元素的集合：
```js
var myCollection = document.getElementsByTagName("p");
```

显示集合元素个数：
```js
document.getElementById("demo").innerHTML = myCollection.length;
```

集合 length 属性常用于遍历集合中的元素。

#### 实例

修改所有 \<p> 元素的背景颜色:

```js
var myCollection = document.getElementsByTagName("p");
var i;
for (i = 0; i < myCollection.length; i++) {
    myCollection[i].style.backgroundColor = "red";
}
```

### 注意

**HTMLCollection 不是一个数组！**

HTMLCollection 看起来可能是一个数组，但其实不是。

你可以像数组一样，使用索引来获取元素。

HTMLCollection 无法使用数组的方法： valueOf(), pop(), push(), 或 join() 。

## JavaScript HTML DOM 节点列表

NodeList 对象是一个从文档中获取的节点列表 (集合) 。

NodeList 对象类似 [HTMLCollection](https://www.runoob.com/js/js-htmldom-elements.html) 对象。

一些旧版本浏览器中的方法（如：getElementsByClassName()）返回的是 NodeList 对象，而不是 HTMLCollection 对象。

所有浏览器的 childNodes 属性返回的是 NodeList 对象。

大部分浏览器的 querySelectorAll() 返回 NodeList 对象。

以下代码选取了文档中所有的 \<p> 节点：
```js
var myNodeList = document.querySelectorAll("p");
```

NodeList 中的元素可以通过索引(以 0 为起始位置)来访问。

访问第二个 \<p> 元素可以是以下代码:
```js
y = myNodeList[1];
```

### NodeList 对象 length 属性

NodeList 对象 length 属性定义了节点列表中元素的数量。
```js
var myNodelist = document.querySelectorAll("p");
document.getElementById("demo").innerHTML = myNodelist.length;
```

#### 实例解析

获取 \<p> 元素的集合：
```js
var myNodelist = document.querySelectorAll("p");
```

显示节点列表的元素个数：
```js
document.getElementById("demo").innerHTML = myNodelist.length;
```

length 属性常用于遍历节点列表。

修改节点列表中所有 \<p> 元素的背景颜色:
```js
var myNodelist = document.querySelectorAll("p");
var i;
for (i = 0; i < myNodelist.length; i++) {
    myNodelist[i].style.backgroundColor = "red";
}
```

### HTMLCollection 与 NodeList 的区别
[HTMLCollection](https://www.runoob.com/js/js-htmldom-collections.html) 是 HTML 元素的集合。

NodeList 是一个文档节点的集合。

NodeList 与 HTMLCollection 有很多类似的地方。

NodeList 与 HTMLCollection 都与数组对象有点类似，可以使用索引 (0, 1, 2, 3, 4, ...) 来获取元素。

NodeList 与 HTMLCollection 都有 length 属性。

HTMLCollection 元素可以通过 name，id 或索引来获取。

NodeList 只能通过索引来获取。

只有 NodeList 对象有包含属性节点和文本节点。

### 注意

**节点列表不是一个数组！**

节点列表看起来可能是一个数组，但其实不是。

你可以像数组一样，使用索引来获取元素。

节点列表无法使用数组的方法： valueOf(), pop(), push(), 或 join() 。

### querySelectorAll()和getElementsByTagName()的区别

querySelectorAll()和getElementsByTagName()两者的主要区别就是返回值。前者返回的是NodeList集合，后者返回的是HTMLCollection集合。其前者是一个静态集合，后者是一个动态集合。

其中动态集合和静态集合的最大区别在于：动态集合指的就是元素集合会随着DOM树元素的增加而增加，减少而减少；静态集合则不会受DOM树元素变化的影响。

使用getElementsByTagName方法我们得到的结果就像是一个对象的索引，而通过querySelectorAll方法我们得到的是一个对象的克隆；所以当这个对象数据量非常大的时候，显然克隆这个对象所需要花费的时间是很长的。












