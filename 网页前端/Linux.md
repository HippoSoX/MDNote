# Linux

随手写的笔记，知识体系并不系统。主要内容摘自鸟哥。

## Linux命令

```
command [-options] parameter1 parameter2 ...
```

0. 一行命令开头一定是以“命令”或“可执行文件”
1. `command`是命令的名称
2. `[]`实际输入时不用加，根据具体要求加入选项，有的前面带有`-`，有的有`--`，特殊情况下也会有带`+`的，如`date`命令
3. `parameter`是依附在选项后面的参数，或者是`command`的参数
4. 命令、选项、参数以空格来划分，但无论空几格shell都视为一格
5. 按下回车后立即执行
6. 命令过长时可以用反斜杠`\\`使命令将延续到下一行。（感觉这个没什么必要）
7. Linux区分大小写！！！  

1. 命令的选项或者参数如果输入错误会有提示信息。
2. 在命令行模式下输入命令时，会有两种执行模式：
	- 一种是该命令会直接将结果返回到控制台
	- 另一种是进入该命令的执行环境，直到结束退出才会回到控制台

### 查看错误信息

例如，如果提示：
```
DATE: command not found
```

那么可能的原因会有：

- 这个命令不存在，因为该软件没有安装之故。解决方法就是安装该软件；
- 这个命令所在的目录目前的用户并没有将他加入命令搜寻路径中，请参考bash的PATH说明；
- 很简单！因为你打错字！

### Linux在线求助

#### man page

man是manual的简写，可以在在线求助说明书。

```
man command
```

**Tips**:
进入man命令的功能后，你可以按下『空格键』往下翻页，可以按下『 q 』按键来离开man的环境。 更多在man命令下的功能，本小节后面会谈到的！

man

#### 解读man page

以man date为例

1. 第一行`DATE(1)`，可以知道这是命令的名称。而括号里的数字则代表命令的基本分类。

   |代号|代表内容|
   |--|--|
   |1|使用者在shell环境中可以操作的命令或可运行文件|
   |2|系统核心可呼叫的函数与工具等|
   |3|一些常用的函数(function)与函式库(library)，大部分为C的函式库(libc)|
   |4| 装置文件的说明，通常在/dev下的文件|
   |5|配置文件或者是某些文件的格式|
   |6|游戏(games)|
   |7|惯例与协议等，例如Linux文件系统、网络协议、ASCII code等等的说明|
   |8|系统管理员可用的管理命令|
   |9|跟kernel有关的文件|

上述表格可以用`man 7 man`来更详细的取得说明。

*1 5 8这三个数字代表的特别重要，一定要记住。*

2. man page的主要内容根据标题可以分为这几部分

|代号|内容说明|
|--|--|
|NAME|简短的命令、数据名称说明|
|SYNOPSIS|简短的命令下达语法(syntax)简介|
|DESCRIPTION|较为完整的说明，这部分最好仔细看看！|
|OPTIONS|针对 SYNOPSIS 部分中，有列举的所有可用的选项说明|
|COMMANDS|当这个程序(软件)在运行的时候，可以在此程序(软件)中下达的命令|
|FILES|这个程序或数据所使用或参考或连结到的某些文件|
|SEE ALSO|可以参考的，跟这个命令或数据有相关的其他说明！|
|EXAMPLE|一些可以参考的范例|
|BUGS|是否有相关的臭虫！|

有时候除了这些外，还可能会看到Authors与Copyright等，不过也有很多时候仅有NAME与DESCRIPTION等部分。 通常鸟哥在查询某个数据时是这样来查阅的：

1. 先看NAME，简单了解二命令的信息
2. 再详细看一下DESCRIPTION，这部分详细介绍了命令有关的内容与使用时机
3. 如果这个命令很熟悉了，可以直接看OPTIONS（在DESCRIPTION里面），了解详细的命令选项和参数
4. 最后再看一下还有那些东西值得参考的。例如SEE ALSO
5. 某些page里面还会再FILES里面列出相关的文件供参考

#### 在man page里的辅助操作

|按键|进行工作|
|--|--|
|空格键|向下翻一页|
|[Page Down]|向下翻一页|
|[Page Up]|向上翻一页|
|[Home]|去到第一页|
|[End]|去到最后一页|
|/string|向『下』搜寻 string 这个字符串，如果要搜寻 vbird 的话，就输入 /vbird|
|?string|向『上』搜寻 string 这个字符串|
|n, N| 利用 / 或 ? 来搜寻字符串时，可以用 n 来继续下一个搜寻 (不论是 / 或 ?) ，可以利用 N 来进行『反向』搜寻。举例来说，我以 /vbird 搜寻 vbird 字符串， 那么可以 n 继续往下查询，用 N 往上查询。若以 ?vbird 向上查询 vbird 字符串， 那我可以用 n 继续『向上』查询，用 N 反向查询。|
|q|结束这次的 man page|

#### man page文件数据路径

man page能够读出数据，说明本地上是有一些数据的。通常，DISTRIBUTION是放在`/usr/share/man`这个目录里面的。
我们可以通过修改`/etc/man.config 或 man.conf 或 manpath.conf //Ubuntu是manpath.config`

#### man -f command 搜寻特定命令/文件的man page

```
man -f command
```

例如
```
man -f man
man (1)              - an interface to the on-line reference manuals
man (7)              - macros to format man pages
```

要访问`man(7)`：
```
man 7 man
```

而至于默认情况下，会优先显示哪一个，在`/etc/manpath.config`里面配置。一般是数字较小的那个。

#### man -k command 

## 重要热键

### [tab]

Linux种tab键具有**命令补全**与**文件补齐**的功能，可以避免打错命令或者文件名。根据输入位置的不同会执行不同的命令。

- [tab]接在命令`command`部分，会执行命令补全
- [tab]接在命令的选项`[-option]`或参数`parameter`后面，会执行文件补齐

天秀热键

```
ap[tab][tab]
apm_available         apropos               apt-config            apt-key
apparmor_parser       apt                   apt-extracttemplates  apt-mark
apparmor_status       apt-cache             apt-ftparchive        apt-sortpkgs
applygnupgdefaults    apt-cdrom             apt-get 

ls -a ~/.bash[tab][tab]
.bash_history  .bashrc  
```

### [Ctrl]+c

中断目前正在执行的命令或程序。

### [Ctrl]+d

这个组合按键通常代表着： 『键盘输入结束(End Of File, EOF 或 End Of Input)』的意思！ 另外，他也可以用来取代exit的输入呢！例如你想要直接离开文字接口，可以直接按下[Ctrl]-d就能够直接离开了(相当于输入exit啊！)。


## 基础命令的操作

### date

显示日期与时间

```
date
date +%Y/%m/%d
date +%H:%M
```

### cal

显示日历的命令

```
cal
cal [month] [year]
```

### bc

简单好用的计算器

```
bc
quit //退出
```












