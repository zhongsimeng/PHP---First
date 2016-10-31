# PHP---First
the first time for PHP

##PHP简介
PHP脚本在服务器上执行

###什么是PHP？
"PHP Hypertext Preprocessor"的首字母缩略词

一种被广泛使用的开源脚本语言

脚本在服务器上执行

没有成本，可供免费下载和使用

###PHP是一门令人惊叹的流行语言！
它强大到足以成为 在网络上做的的博客系统的核心（WordPress）！

它深邃到足以运行最大的社交网络（Facebook）！

它的易用程度足以成为初学者的首选 服务器端语言！

###什么是PHP文件？
能够包含文本、HTML、CSS、以及PHP代码

PHP代码在服务器上执行，而结果以纯文本返回浏览器

后缀是".php"
 
###PHP能够做什么？
生成动态页面内容

能够创建、打开、读取、写入、删除以及关闭服务器上的文件

能够接受表单数据

能够发送并取回cookies

能够添加、删除、修改数据库中的数据

能够限制用户访问网站中的某些页面

能够对数据进行加密

>通过PHP，您可以不受限于只输出HTML。您还能够输出图像、PDF文件、甚至Flash影片。您也可以输出任何文本，比如XHTML和 XML。
 
###为什么使用PHP？ 
它运行于各种平台（Windows、linux、Unix、Mac OS X等等

它兼容集合所有服务器（Apache、IIS等等）

支持多种数据库

免费的。官网www.php.net

易于学习，并可高效地运行在服务器端
  
  
##PHP安装


##PHP语法
PHP脚本在服务器上执行，然后向 浏览器发送回纯HTML结果。

###基础PHP语法
PHP脚本可放置于文档的任何位置。

PHP脚本以`<?php开头，以?>`结尾：

    <?php
    //此处是PHP代码
    ?>

PHP文件的默认文件扩展名是“.PHP”。

PHP文件通常包含HTML标签以及一些PHP脚本代码。
  
下面 的例子是一个简单的PHP文件，其中包含了使用内建PHP函数“echo”在网页上 输出“Hello World！”的一段PHP脚本：

    <!DOCTYPE html>
    <html>
    <body>

    <h1>我的第一张PHP页面</h1>

    <?php
    echo "Hello World!";
    ?>

    </body>
    </html>

>PHP语句以分号结尾(;)。PHP代码块的关闭标签也会自动表明分号（因此在PHP代码块的最后一行不必使用分号）。
  
###PHP中的注释
PHP代码中的注释不会被作为程序来读取和执行。它唯一的作用是提供给代码编辑者阅读。

注释用于：

* 使他人理解代码工作；

* 提醒自己做过什么，思路。
    
###PHP支持 三种注释：

###PHP大小写敏感
在PHP中，所有用户定义的函数、类、关键词（如if、else、echo等等）都对大小写不敏感。

在下面例子中，三种echo语法都是合法的（等价的）：

    <!DOCTYPE html>
    <html>
    <body>

    <?php
    ECHO "Hello World!<br>";
    echo "Hello World!<br>";
    EcHo "Hello World!<br>";
    ?>

    </body>
    </html>
      
不过在PHP中，所有的变量都对大小写敏感。

在下面的例子中，只有第一条语句会显示 $color 变量的值（这是因为 $color、$COLOR 以及 $coLOR 被视作三个不同的变量）：

    <!DOCTYPE html>
    <html>
    <body>

    <?php
    $color="red";
    echo "My car is " . $color . "<br>";
    echo "My house is " . $COLOR . "<br>";
    echo "My boat is " . $coLOR . "<br>";
    ?>

    </body>
    </html>

##PHP变量
变量是存储信息的容器：

    <?php
    $x=5;
    $y=6;
    $z=$x+$y;
    echo $z;
    ?>

类似代数

    x=5
    y=6
    z=x+y
      
在代数中我们使用字母（比如 x）来保存值（比如 5）。

从上面的表达式 z=x+y，我们能够计算出 z 的值是 11。

在 PHP 中，这三个字母被称为变量。

>注释：请把变量视为存储数据的容器。
  
###PHP变量
正如代数，PHP 变量可用于保存值（x=5）和表达式（z=x+y）。

变量的名称可以很短（比如 x 和 y），也可以取更具描述性的名称（比如 carname、total_volume）。 

###PHP变量规则

* 变量以$符号开头
* 变量名称必须以字母后下划线开头
* 变量名称不能以数字开头
* 变量名称只能保护数字字符和下划线（A-z,0-9以及_)
* 变量名称对 大小写敏感（$y与$Y是两个不同的变量）
  
>PHP变量名称对 大小写敏感
 
###创建PHP变量
PHP没有创建变量的命令。

变量会在收藏为其赋值时被创建。

实例：

    <?php
    $txt="Hello world!";
    $x=5;
    $y=10.5;
    ?>

>注释：如果您为变量赋的值是文本，请用引号包围该值。
  
###PHP是一门类型松散的语言
不必告诉PHP变量的数据类型，PHP根据变量的值，自动把变量转换为正确的数据类型。
  
###PHP变量的作用域
在PHP中，可以在脚本的任意位置对变量进行声明。

变量的作用域指的是变量能够被引用/使用的那部分脚本。

PHP有三种不同的变量作用域：

* local(局部)
* global(全局)
* static(静态)
    
###Local和Global作用域
函数之外声明的变量拥有Global作用域，只能在函数以外进行访问。

函数内部声明的变量 拥有Local作用域，只能在函数内部进行访问。

实例：

    <?php
    $x=5; // 全局作用域

    function myTest() {
    $y=10; // 局部作用域
    echo "<p>测试函数内部的变量：</p>";
    echo "变量 x 是：$x";
    echo "<br>";
    echo "变量 y 是：$x";
    } 

    myTest();

    echo "<p>测试函数之外的变量：</p>";
    echo "变量 x 是：$x";
    echo "<br>";
    echo "变量 y 是：$x";
    ?>

>在上例中，有两个变量 $x 和 $y，以及一个函数 myTest()。$x 是全局变量，因为它是在函数之外声明的，而 $y 是局部变量，因为它是在函数内声明的。

>如果我们在 myTest() 函数内部输出两个变量的值，$y 会输出在本地声明的值，但是无法 $x 的值，因为它在函数之外创建。

>然后，如果在 myTest() 函数之外输出两个变量的值，那么会输出 $x 的值，但是不会输出 $y 的值，因为它是局部变量，并且在 myTest() 内部创建。

>注释：您可以在不同的函数中创建名称相同的局部变量，因为局部变量只能被在其中创建它的函数识别。
  
###PHP global关键词
global关键词拥有访问函数内的全局变量。

要做到这一点，请在（函数内部）变量前面使用 global 关键词：

实例：

    <?php
    $x=5;
    $y=10;

    function myTest() {
    global $x,$y;
    $y=$x+$y;
    }

    myTest();
    echo $y; // 输出 15
    ?>

>PHP 同时在名为 $GLOBALS[index] 的数组中存储了所有的全局变量。下标存有变量名。这个数组在函数内也可以访问，并能够用于直接更新全局变量。

上面的例子可以这样重写：

实例

    <?php
    $x=5;
    $y=10;

    function myTest() {
      $GLOBALS['y']=$GLOBALS['x']+$GLOBALS['y'];
    } 

    myTest();
    echo $y; // 输出 15
    ?>

###PHP static关键词
通常，当函数完成/执行后，会删除所有的变量。不过，有时我需要不删除某个局部变量。

要完成这一点，要在首次声明变量时使用static关键词：

实例：

    <?php

    function myTest() {
      static $x=0;
      echo $x;
      $x++;
    }

    myTest();
    myTest();
    myTest();

    ?>

> 然后，每当函数被调用时，这个变量所存储的信息 都是函数最后一次被调用时所包含的信息。

> 改变量仍然是函数的局部变量。
  
   
##PHP Echo/Print语句
##在PHP中，有两种基本的输出方法：echo和print

###PHP echo和print语句

* echo-能够输出一个以上的字符串
* print-只能输出一个字符串，并始终返回1

> 提示：echo比print稍快，因为它不返回任何值。
  
###PHP echo语句
echo是一个语言结构，有无括号均可使用：echo或echo().
  
####显示字符串
下面的例子展示如何用 echo 命令来显示不同的字符串（同时请注意字符串中能包含 HTML 标记）：

    <?php
    echo "<h2>PHP is fun!</h2>";
    echo "Hello world!<br>";
    echo "I'm about to learn PHP!<br>";
    echo "This", " string", " was", " made", " with multiple parameters.";
    ?>
      
####显示变量
下面的例子展示如何用 echo 命令来显示字符串和变量：

    <?php
    $txt1="Learn PHP";
    $txt2="W3School.com.cn";
    $cars=array("Volvo","BMW","SAAB");

    echo $txt1;
    echo "<br>";
    echo "Study PHP at $txt2";
    echo "My car is a {$cars[0]}";
    ?>

###PHP print语句
print也是语言结构，有无括号均可使用：print或print()。
  
####显示字符串
下面的例子展示如何用 print 命令来显示不同的字符串（同时请注意字符串中能包含 HTML 标记）：

    <?php
    print "<h2>PHP is fun!</h2>";
    print "Hello world!<br>";
    print "I'm about to learn PHP!";
    ?>
      
####显示变量
下面的例子展示如何用 print 命令来显示字符串和变量：

   <?php
    $txt1="Learn PHP";
    $txt2="W3School.com.cn";
    $cars=array("Volvo","BMW","SAAB");

    print $txt1;
    print "<br>";
    print "Study PHP at $txt2";
    print "My car is a {$cars[0]}";
    ?>
 

##PHP 数据类型
字符串、整数、浮点数、逻辑、数组、对象、NULL
  
###PHP字符串
字符串是字符序列，比如"Hello World!"

字符串可以是引号内的任何文本。你可以使用单引号或双引号。

实例

    <?php 
    $x = "Hello world!";
    echo $x;
    echo "<br>"; 
    $x = 'Hello world!';
    echo $x;
    ?> 
      
###PHP整数
整数是没有小数的数字。

整数规则：

* 整数必须有至少一个数字（0-9）

* 整数不能包含逗号或者空格

* 整数不能有小数点

* 整数征服均可

* 可以用三种格式规定整数：十进制、十六进制、（前缀是0x）或八进制（前缀是0）
    
实例：

    <?php 
    $x = 5985;
    var_dump($x);
    echo "<br>"; 
    $x = -345; // 负数
    var_dump($x);
    echo "<br>"; 
    $x = 0x8C; // 十六进制数
    var_dump($x);
    echo "<br>";
    $x = 047; // 八进制数
    var_dump($x);
    ?>
  
###PHP浮点数
浮点数是有或者指数形式的数字。

实例：

    <?php 
    $x = 10.365;
    var_dump($x);
    echo "<br>"; 
    $x = 2.4e3;
    var_dump($x);
    echo "<br>"; 
    $x = 8E-5;
    var_dump($x);
    ?>
      
###PHP逻辑
逻辑是true或false。

逻辑常用于条件测试。

    $x=true;
    $y=false;
 
###PHP数组
数组在一个变量中存储多个值。

实例：

    <?php 
    $cars=array("Volvo","BMW","SAAB");
    var_dump($cars);
    ?>
      
###PHP对象
对象是存储数据和有关如何处理数据的信息的数据类型。

在PHP中，必须明确地声明对象。

首先我们必须声明对象的类。对此，我们使用class关键词。类是包含属性和方法的结构。

然后我们在对象类中定义数据类型，然后在该类的实例中使用此数据类型：
  
实例

    <?php
    class Car
    {
      var $color;
      function Car($color="green") {
        $this->color = $color;
      }
      function what_color() {
        return $this->color;
      }
    }
    ?>
      
###PHP NULL值
特殊的NULL值表示变量无值。 NULL是数据 类型NULL唯一可能的值。

NULL值表示变量是否为空。也用于区分空字符串与空值数据库。

可以通过把值设置为NULL，将变量清空。
  
实例

    <?php
    $x="Hello world!";
    $x=null;
    var_dump($x);
    ?>
      
##PHP 字符串函数
字符串是字符序列。比如"Hello world!"
  
###PHP 字符串函数
  
###PHP strlen() 函数
strlen()函数返回字符串的长度，以字符计。

实例：

    <?php
    echo strlen("Hello world!");
    ?>
>strlen()常用于循环和其他函数，在确定字符串何时结束很重要。
  
###PHP strpos()  函数
strpos()函数 用于检索字符串内指定的字符或文本。

如果找到匹配，则会返回首个匹配的字符位置。如果未找到匹配，则返回FALSE.

实例：

    <?php
    echo strpos("Hello world!","world");
    ?>

>以上字符串"world"的位置是6，是6不是7的理由 是，字符串中首字符的位置是0而不是1.
  
###完整的PHP String参考手册

##PHP常量
常量类似变量， 但是常量一旦被定义就无法更改或者撤销定义。
  
###PHP 常量
常量是单个值得标识符（名称），在脚本中 无法改变改值。

有效的常量名以字符或下划线开头（常量名称前面没有$符 号）。

>与变量不同，常量贯穿真个脚本是自动全局的。
  
###设置PHP常量
如需设置常量，请使用define()函数-它使用三个 参数：

  1.首个参数定义常量的名称

  2.第二个参数定义常量的值

  3.可选的第三个参数规定常量名是否对大小写敏感。默认是false。
    
实例

    <?php
    define("GREETING", "Welcome to W3School.com.cn!对大小写敏感的常量");
    echo GREETING;
    ?>

    <?php
    define("GREETING", "Welcome to W3School.com.cn!对大小写不敏感的常量", true);
    echo greeting;
    ?>


##PHP运算符

###PHP算数运算符

    +	加法	$x + $y	$x 与 $y 求和
    -	减法	$x - $y	$x 与 $y 的差数
    *	乘法	$x * $y	$x 与 $y 的乘积
    /	除法	$x / $y	$x 与 $y 的商数
    %	模数	$x % $y	$x 除 $y 的余数

实例：

    <?php 
    $x=10; 
    $y=6;
    echo ($x + $y); // 输出 16
    echo ($x - $y); // 输出 4
    echo ($x * $y); // 输出 60
    echo ($x / $y); // 输出 1.6666666666667
    echo ($x % $y); // 输出 4
    ?>
      
###PHP赋值运算符
PHP赋值运算符用于向变量写值。

PHP中基础的赋值运算符是“=”，这意味着右侧赋值表达式会为左侧运算数设置值。

    x = y	x = y	右侧表达式为左侧运算数设置值。
    x += y	x = x + y	加
    x -= y	x = x - y	减
    x *= y	x = x * y	乘
    x /= y	x = x / y	除
    x %= y	x = x % y	模数

实例

    <?php 
    $x=10; 
    echo $x; // 输出 10

    $y=20; 
    $y += 100;
    echo $y; // 输出 120

    $z=50;
    $z -= 25;
    echo $z; // 输出 25

    $i=5;
    $i *= 6;
    echo $i; // 输出 30

    $j=10;
    $j /= 5;
    echo $j; // 输出 2

    $k=15;
    $k %= 4;
    echo $k; // 输出 3
    ?>

###PHP字符串运算符

    .	串接	$txt1 = "Hello" $txt2 = $txt1 . " world!"	现在 $txt2 包含 "Hello world!"
    .=	串接赋值	$txt1 = "Hello" $txt1 .= " world!"	现在 $txt1 包含 "Hello world!"

实例

    <?php
    $a = "Hello";
    $b = $a . " world!";
    echo $b; // 输出 Hello world!

    $x="Hello";
    $x .= " world!";
    echo $x; // 输出 Hello world!
    ?>
      
###PHP递增/递减运算符

    ++$x	前递增	$x 加一递增，然后返回 $x
    $x++	后递增	返回 $x，然后 $x 加一递增
    --$x	前递减	$x 减一递减，然后返回 $x
    $x--	后递减	返回 $x，然后 $x 减一递减

实例

    <?php
    $x=10; 
    echo ++$x; // 输出 11

    $y=10; 
    echo $y++; // 输出 10

    $z=5;
    echo --$z; // 输出 4

    $i=5;
    echo $i--; // 输出 5
    ?>
      
###PHP比较运算符
PHP比较运算符用于比较两个值（数字或字符串）

    ==	等于	$x == $y	如果 $x 等于 $y，则返回 true。
    ===	全等（完全相同）	$x === $y	如果 $x 等于 $y，且它们类型相同，则返回 true。
    !=	不等于	$x != $y	如果 $x 不等于 $y，则返回 true。
    <>	不等于	$x <> $y	如果 $x 不等于 $y，则返回 true。
    !==	不全等（完全不同）	$x !== $y	如果 $x 不等于 $y，且它们类型不相同，则返回 true。
    >	大于	$x > $y	如果 $x 大于 $y，则返回 true。
    <	大于	$x < $y	如果 $x 小于 $y，则返回 true。
    >=	大于或等于	$x >= $y	如果 $x 大于或者等于 $y，则返回 true.
    <=	小于或等于	$x <= $y	如果 $x 小于或者等于 $y，则返回 true。

实例

    <?php
    $x=100; 
    $y="100";

    var_dump($x == $y);
    echo "<br>";
    var_dump($x === $y);
    echo "<br>";
    var_dump($x != $y);
    echo "<br>";
    var_dump($x !== $y);
    echo "<br>";

    $a=50;
    $b=90;

    var_dump($a > $b);
    echo "<br>";
    var_dump($a < $b);
    ?>

###PHP逻辑运算符

    and	与	$x and $y	如果 $x 和 $y 都为 true，则返回 true。
    or	或	$x or $y	如果 $x 和 $y 至少有一个为 true，则返回 true。
    xor	异或	$x xor $y	如果 $x 和 $y 有且仅有一个为 true，则返回 true。
    &&	与	$x && $y	如果 $x 和 $y 都为 true，则返回 true。
    ||	或	$x || $y	如果 $x 和 $y 至少有一个为 true，则返回 true。
    !	非	!$x	如果 $x 不为 true，则返回 true。
      
###PHP数组运算符
PHP数组运算符用于比较数组：

    +	联合	$x + $y	$x 和 $y 的联合（但不覆盖重复的键）
    ==	相等	$x == $y	如果 $x 和 $y 拥有相同的键/值对，则返回 true。
    ===	全等	$x === $y	如果 $x 和 $y 拥有相同的键/值对，且顺序相同类型相同，则返回 true。
    !=	不相等	$x != $y	如果 $x 不等于 $y，则返回 true。
    <>	不相等	$x <> $y	如果 $x 不等于 $y，则返回 true。
    !==	不全等	$x !== $y	如果 $x 与 $y 完全不同，则返回 true。

实例：

    <?php
    $x = array("a" => "red", "b" => "green"); 
    $y = array("c" => "blue", "d" => "yellow"); 
    $z = $x + $y; // $x 与 $y 的联合
    var_dump($z);
    var_dump($x == $y);
    var_dump($x === $y);
    var_dump($x != $y);
    var_dump($x <> $y);
    var_dump($x !== $y);
    ?>

##PHP if...else...elseif语句
条件语句用于基于不同条件执行不同的动作
  
###PHP条件语句
在您编写代码时，经常会希望为不同的决定执行不同的动作。您可以在代码中使用条件语句来实现这一点。

在 PHP 中，我们可以使用以下条件语句：

* if 语句 - 如果指定条件为真，则执行代码
* if...else 语句 - 如果条件为 true，则执行代码；如果条件为 false，则执行另一端代码
* if...elseif....else 语句 - 选择若干段代码块之一来执行
* switch 语句 - 语句多个代码块之一来执行
  
###PHP if语句
if语句用于在指定条件为true时执行代码。

语法：

    if (条件) {
      当条件为 true 时执行的代码;
    }

实例：

    <?php
    $t=date("H");

    if ($t<"20") {
      echo "Have a good day!";
    }
    ?>
      
###PHP if..else语句
请使用if...else语句在条件为true时执行代码，在条件为false时执行另一段代码。

语法：

    if (条件) {
      条件为 true 时执行的代码;
    } else {
      条件为 false 时执行的代码;
    }

实例

    <?php
    $t=date("H");

    if ($t<"20") {
      echo "Have a good day!";
    } else {
      echo "Have a good night!";
    }
    ?>
      
###PHP if...elseif...else 语句
请使用if...elseif...else 语句来选择若干代码块之一来执行。

语法：

    if (条件) {
      条件为 true 时执行的代码;
    } elseif (condition) {
      条件为 true 时执行的代码;
    } else {
      条件为 false 时执行的代码;
    }

实例：

    <?php
    $t=date("H");

    if ($t<"10") {
      echo "Have a good morning!";
    } elseif ($t<"20") {
      echo "Have a good day!";
    } else {
      echo "Have a good night!";
    }
    ?>
      
##PHP  Switch语句
switch语句用于基于不同条件执行不同动作。
  
###Switch语句
如果你希望有选择地执行若干代码块之一，请使用 Switch语句。

使用 Switch语句可以避免冗长的if...elseif...else代码块

语法 ：

    switch (expression)
    {
    case label1:
      code to be executed if expression = label1;
      break;  
    case label2:
      code to be executed if expression = label2;
      break;
    default:
      code to be executed
      if expression is different 
      from both label1 and label2;
    }
      
工作原理：

  1.对表达式（通常是变量）进行一次计算

  2.把表达式的值与结构中case的值进行比较

  3.如果存在匹配，则执行与case关联的代码

  4.代码执行后，break语句阻止代码跳入下一个case中继续执行

  5.如果没有case为真，则使用default语句

实例：

    <?php
    switch ($x)
    {
    case 1:
      echo "Number 1";
      break;
    case 2:
      echo "Number 2";
      break;
    case 3:
      echo "Number 3";
      break;
    default:
      echo "No number between 1 and 3";
    }
    ?>

##PHP while循环
PHP while循环在指定条件为true时执行代码块
  
###PHP 循环
在你编写代码时 ，经常需要反复运行同一代码块。我们可以使用循环来执行这样的任务，而不是在脚本中添加若干几乎相等的代码行。

在PHP中，我们有以下循环语句：

* while-只要指定条件为真，则循环代码块
* do...while-先执行一次代码块，然后只要指定条件为真怎重复循环
* for-循环代码块指定次数
* foreach- 遍历数组中的每个元素并循环代码块
    
###PHP while循环
只要指定条件为真， while循环就会执行 代码块

语法：

    while (条件为真) {
      要执行的代码;
    }

实例：

    <?php 
    $x=1; 

    while($x<=5) {
      echo "这个数字是：$x <br>";
      $x++;
    } 
    ?>
      
###PHP do...while循环
do...while循环首先 会执行一次代码块，然后检查条件，如果指定条件为真，怎重复循环。
  
语法：

    do {
      要执行的代码;
    } while (条件为真);

实例：

    <?php 
    $x=1; 

    do {
      echo "这个数字是：$x <br>";
      $x++;
    } while ($x<=5);
    ?>

>请注意，do while循环只在执行循环内的语句之后才对条件进行测试。这意味着do while循环至少会执行一次语句，即使条件测试在第一次就失败了。

实例：
  下面的例子把 $x 设置为 6，然后运行循环，随后对条件进行检查：

      <?php 
      $x=6;

      do {
        echo "这个数字是：$x <br>";
        $x++;
      } while ($x<=5);
      ?>
      
##PHP for循环
PHP for循环执行代码块指定的次数
  
###PHP for循环
如果你已经提前确定脚本运行的次数，可以使用for循环

语法：

    for (init counter; test counter; increment counter) {
      code to be executed;
    }

参数：

* init counter：初始化循环计数器的值
* text counter：评估每个循环迭代。如果值为true，继续循环。如果它的值为false，循环结束。
* increment counter： 增加循环计数器的值
  
实例：

  下面的例子显示了从 0 到 10 的数字：  

      <?php 
      for ($x=0; $x<=10; $x++) {
        echo "数字是：$x <br>";
      } 
      ?>
        
###PHP foreach 循环
foreach循环只适用于数组，并用于遍历数组中的每个键/值对。

每进行一次循环迭代，当前数组元素的值就会被赋值给$value 变量，并且数组指针会逐一地移动，直到到达最后一个数组元素。

下面的例子演示的循环将输出给定数组（$colors）的值：

实例：

    <?php 
    $colors = array("red","green","blue","yellow"); 

    foreach ($colors as $value) {
      echo "$value <br>";
    }
    ?>


##PHP 函数
PHP的真正力量来自它的函数：它拥有超过1000个内建的函数。
  
###PHP用户定义函数
除了内建的PHP函数，我们可以创建我们自己的函数。

函数是可以在程序中重复使用的语句块。

页面加载时函数不会立即执行。

函数只有在被调用时才会执行。
  
###在PHP创建用户定义函数
用户定义的函数声明以关单"function"开头：

语法：

    function functionName(){
       被执行的代码;
    }

>注释：函数名能够以字母或下划线开头（而非数字）。

>注释：函数名对大小写不敏感

>提示：函数名应该能够反映函数所执行的任务。
  
在下面的例子中，我们创建名为 "writeMsg()" 的函数。打开的花括号（{）指示函数代码的开始，而关闭的花括号（}）指示函数的结束。此函数输出 "Hello world!"。如需调用该函数，只要使用函数名即可：

实例：

    <?php
    function writeMsg(){
      echo "Hello world!";
    }

    writeMsg();//调用函数
    ?>
      
###PHP  函数参数
可以通过参数向函数传递信息。参数类似变量。

参数被定义在函数名之后，括号内部。你可以添加任意多参数，只要用逗号隔开即可。

下面的例子中的函数有一个参数（$fname）。当调用 familyName() 函数时，我们同时要传递一个名字（例如 Bill），这样会输出不同的名字，但是姓氏相同：
  
实例：

    <?php
    function familyName($fname) {
      echo "$fname Zhang.<br>";
    }

    familyName("Li");
    familyName("Hong");
    familyName("Tao");
    familyName("Xiao Mei");
    familyName("Jian");
    ?>
      
下面的例子中的函数有两个参数（$fname 和 $year）：

实例

    <?php
    function familyName($fname,$year) {
      echo "$fname Zhang. Born in $year <br>";
    }

    familyName("Li","1975");
    familyName("Hong","1978");
    familyName("Tao","1983");
    ?>
      
###PHP 默认参数值
下面的例子展示了如何使用默认参数。如果我们调用没有参数的 setHeight() 函数，它的参数会取默认值：

实例：

    <?php
    function setHeight($minheight=50) {
      echo "The height is : $minheight <br>";
    }

    setHeight(350);
    setHeight(); // 将使用默认值 50
    setHeight(135);
    setHeight(80);
    ?>
      
###PHP函数-返回值
如果使用函数返回值，请使用return语句；

实例：

    <?php
    function sum($x,$y) {
      $z=$x+$y;
      return $z;
    }

    echo "5 + 10 = " . sum(5,10) . "<br>";
    echo "7 + 13 = " . sum(7,13) . "<br>";
    echo "2 + 4 = " . sum(2,4);
    ?>
      
      
###PHP数组
数组能够在单独的变量名中存储一个或多个值

实例：

    <?php
    $cars=array("Volvo","BMW","SAAB");
    echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
    ?>

###什么是数组
数组是特殊的变量，它可以同时保存一个以上的值。

如果你有一个项目列表，在单个变量中存储这些内容是这样的

$cars1="Volvo";
$cars2="BMW";
$cars3="SAAB";

不过，假如您希望对变量进行遍历并找出特定的那个值？或者如果您需要存储 300 个汽车品牌，而不是 3 个呢？

解决方法是创建数组！

数组能够在单一变量名中存储许多值，并且您能够通过引用下标号来访问某个值。

###在PHP中创建数组
在PHP中，array()函数用于创建数组：

    array()
    
在PHP中，有三种数组类型：

* 索引数组-带有数字索引的数组
* 关联数组-带有指定键的数组
* 多维数组-包含一个或多个数组的数组

###PHP索引数组
有两种创建索引数组的方法：

索引是自动分配的（索引从 0 开始）：

    $cars=array("Volvo","BMW","SAAB");
    
或者也可以手动分配索引：

    $cars[0]="Volvo";
    $cars[1]="BMW";
    $cars[2]="SAAB";
    
下面的例子创建名为 $cars 的索引数组，为其分配三个元素，然后输出包含数组值的一段文本：

实例

    <?php
    $cars=array("Volvo","BMW","SAAB");
    echo "I like " . $cars[0] . ", " . $cars[1] . " and " . $cars[2] . ".";
    ?>
    
###获得数组的长度-count()函数
count()函数用于返回数组的长度（元素数）：

实例

    <?php
    $cars=array("Volvo","BMW","SAAB");
    echo count($cars);
    ?>
    
###遍历索引数组
如需遍历并输出索引数组的所有值，你可以使用for循环，如：

实例：

    <?php
    $cars=array("Volvo","BMW","SAAB");
    $arrlength=count($cars);

    for($x=0;$x<$arrlength;$x++) {
      echo $cars[$x];
      echo "<br>";
    }
    ?>
    
###PHP关联数组
关联数组是使用你分配给数组的指定键的数组。

有两种创建关联数组的方法：

    $age=array("Peter"=>"35","Ben"=>"37","Joe"=>"43");
    
或者：

    $age['Peter']="35";
    $age['Ben']="37";
    $age['Joe']="43";
    
随后可以在脚本中使用指定键：

实例

    <?php
    $age=array("Bill"=>"35","Steve"=>"37","Peter"=>"43");
    echo "Peter is " . $age['Peter'] . " years old.";
    ?>
    
###遍历关联数组
如需遍历并输出关联数组的所有值，您可以使用foreach循环，如：

实例

    <?php
    $age=array("Bill"=>"35","Steve"=>"37","Peter"=>"43");

    foreach($age as $x=>$x_value){
      echo "Key=".$x. ",Value=".$x_value;
      echo "<br>";
    }
    ?>
    
###多维数组

##PHP数组排序
数组中的元素能够以字母或者数字顺序进行升序或降序排列。

###PHP-数组的排序函数
有一下几种PHP数组排序函数：

* sort() - 以升序对数组排序
* rsort() - 以降序对数组排序
* asort() - 根据值，以升序对关联数组进行排序
* ksort() - 根据键，以升序对关联数组进行排序
* arsort() - 根据值，以降序对关联数组进行排序
* krsort() - 根据键，以降序对关联数组进行排序

###对数组进行升序排序-sort()
下面的例子按照字母升序对数组 $cars 中的元素进行排序：

实例

    <?php
    $cars=array("Volvo","BMW","SAAB");
    sort($cars);
    ?>

下面的例子按照数字升序对数组 $numbers 中的元素进行排序：

实例

    <?php
    $numbers=array(3,5,1,22,11);
    sort($numbers);
    ?>
    
###对数组进行降序排序-rsort()
下面的例子按照字母降序对数组 $cars 中的元素进行排序：

实例

    <?php
    $cars=array("Volvo","BMW","SAAB");
    rsort($cars);
    ?>
    
下面的例子按照数字降序对数组 $numbers 中的元素进行排序：

实例

    <?php
    $numbers=array(3,5,1,22,11);
    rsort($numbers);
    ?>
    
###根据值对数组进行升序排序-asort()
下面的例子根据值对关联数组进行升序排序：

实例

    <?php
    $age=array("Bill"=>"35","Steve"=>"37","Peter"=>"43");
    asort($age);
    ?>

###根据键对数组进行升序排序 - ksort()
下面的例子根据键对关联数组进行升序排序：

实例

    <?php
    $age=array("Bill"=>"35","Steve"=>"37","Peter"=>"43");
    ksort($age);
    ?>
       
###根据值对数组进行降序排序 - arsort()
下面的例子根据值对关联数组进行降序排序：

实例

    <?php
    $age=array("Bill"=>"35","Steve"=>"37","Peter"=>"43");
    arsort($age);
    ?>

###根据键对数组进行降序排序 - krsort()
下面的例子根据键对关联数组进行降序排序：

实例

    <?php
    $age=array("Bill"=>"35","Steve"=>"37","Peter"=>"43");
    krsort($age);
    ?>
    
    
##PHP全局变量-超全局变量
超全局简历在PHP 4.1.0 中引入，是在全部作用域中始终可用的内置变量。

###PHP全局变量-超全局变量
PHP 中的许多预定义变量都是“超全局的”，这意味着它们在一个脚本的全部作用域中都可用。在函数或方法中无需执行 global $variable; 就可以访问它们。

这些超全局变量是：

* $GLOBALS
* $_SERVER
* $_REQUEST
* $_POST
* $_GET
* $_FILES
* $_ENV
* $_COOKIE
* $_SESSION
    
###$GLOBALS-引用全局作用域中可用的全部变量
$GLOBALS这种全局变量用于在PHP脚本中的任意位置访问全局变量（从函数或方法中均可）。

PHP在名为$GLOBALS[index]的数组中存储了所以全局变量。变量的名字就是数组的键。

下面的例子展示了如何使用超级全局变量 $GLOBALS：

实例

    <?php 
    $x = 75; 
    $y = 25;

    function addition() { 
      $GLOBALS['z'] = $GLOBALS['x'] + $GLOBALS['y']; 
    }

    addition(); 
    echo $z; 
    ?>

在上面的例子中，由于 z 是 $GLOBALS 数组中的变量，因此在函数之外也可以访问它。
    
###PHP $_SERVER
$_SERVER 这种超全局变量保存关于报头、路径和脚本位置的信息。

下面的例子展示了如何使用 $_SERVER 中的某些元素：

实例

    <?php 
    echo $_SERVER['PHP_SELF'];
    echo "<br>";
    echo $_SERVER['SERVER_NAME'];
    echo "<br>";
    echo $_SERVER['HTTP_HOST'];
    echo "<br>";
    echo $_SERVER['HTTP_REFERER'];
    echo "<br>";
    echo $_SERVER['HTTP_USER_AGENT'];
    echo "<br>";
    echo $_SERVER['SCRIPT_NAME'];
    ?>
    
下表列出了您能够在 $_SERVER 中访问的最重要的元素：

    元素/代码	描述
    $_SERVER['PHP_SELF']	返回当前执行脚本的文件名。
    $_SERVER['GATEWAY_INTERFACE']	返回服务器使用的 CGI 规范的版本。
    $_SERVER['SERVER_ADDR']	返回当前运行脚本所在的服务器的 IP 地址。
    $_SERVER['SERVER_NAME']	返回当前运行脚本所在的服务器的主机名（比如 www.w3school.com.cn）。
    $_SERVER['SERVER_SOFTWARE']	返回服务器标识字符串（比如 Apache/2.2.24）。
    $_SERVER['SERVER_PROTOCOL']	返回请求页面时通信协议的名称和版本（例如，“HTTP/1.0”）。
    $_SERVER['REQUEST_METHOD']	返回访问页面使用的请求方法（例如 POST）。
    $_SERVER['REQUEST_TIME']	返回请求开始时的时间戳（例如 1577687494）。
    $_SERVER['QUERY_STRING']	返回查询字符串，如果是通过查询字符串访问此页面。
    $_SERVER['HTTP_ACCEPT']	返回来自当前请求的请求头。
    $_SERVER['HTTP_ACCEPT_CHARSET']	返回来自当前请求的 Accept_Charset 头（ 例如 utf-8,ISO-8859-1）
    $_SERVER['HTTP_HOST']	返回来自当前请求的 Host 头。
    $_SERVER['HTTP_REFERER']	返回当前页面的完整 URL（不可靠，因为不是所有用户代理都支持）。
    $_SERVER['HTTPS']	是否通过安全 HTTP 协议查询脚本。
    $_SERVER['REMOTE_ADDR']	返回浏览当前页面的用户的 IP 地址。
    $_SERVER['REMOTE_HOST']	返回浏览当前页面的用户的主机名。
    $_SERVER['REMOTE_PORT']	返回用户机器上连接到 Web 服务器所使用的端口号。
    $_SERVER['SCRIPT_FILENAME']	返回当前执行脚本的绝对路径。
    $_SERVER['SERVER_ADMIN']	该值指明了 Apache 服务器配置文件中的 SERVER_ADMIN 参数。
    $_SERVER['SERVER_PORT']	Web 服务器使用的端口。默认值为 “80”。
    $_SERVER['SERVER_SIGNATURE']	返回服务器版本和虚拟主机名。
    $_SERVER['PATH_TRANSLATED']	当前脚本所在文件系统（非文档根目录）的基本路径。
    $_SERVER['SCRIPT_NAME']	返回当前脚本的路径。
    $_SERVER['SCRIPT_URI']	返回当前页面的 URI。
    
###PHP $_REQUEST
PHP $_REQUEST 用于收集 HTML 表单提交的数据。

下面的例子展示了一个包含输入字段及提交按钮的表单。当用户通过点击提交按钮来提交表单数据时, 表单数据将发送到 form 标签的 action 属性中指定的脚本文件。在这个例子中，我们指定文件本身来处理表单数据。如果您需要使用其他的 PHP 文件来处理表单数据，请修改为您选择的文件名即可。然后，我们可以使用超级全局变量 $_REQUEST 来收集 input 字段的值：

实例

    <html>
    <body>

    <form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">
    Name: <input type="text" name="fname">
    <input type="submit">
    </form>

    <?php 
    $name = $_REQUEST['fname']; 
    echo $name; 
    ?>

    </body>
    </html>
    
    
###PHP $_POST
PHP $_POST 广泛用于收集提交 method="post" 的 HTML 表单后的表单数据。$_POST 也常用于传递变量。

下面的例子展示了一个包含输入字段和提交按钮的表单。当用户点击提交按钮来提交数据后，表单数据会发送到 `form `标签的 action 属性中指定的文件。在本例中，我们指定文件本身来处理表单数据。如果您希望使用另一个 PHP 页面来处理表单数据，请用更改为您选择的文件名。然后，我们可以使用超全局变量 $_POST 来收集输入字段的值：

实例

    <html>
    <body>

    <form method="post" action="<?php echo $_SERVER['PHP_SELF'];?>">
    Name: <input type="text" name="fname">
    <input type="submit">
    </form>

    <?php 
    $name = $_POST['fname']; 
    echo $name; 
    ?>

    </body>
    </html>
    
    
###PHP $_GET
PHP $_GET 也可用于收集提交 HTML 表单 (method="get") 之后的表单数据。

$_GET 也可以收集 URL 中的发送的数据。

假设我们有一张页面含有带参数的超链接：

    <html>
    <body>

    <a href="test_get.php?subject=PHP&web=W3school.com.cn">测试 $GET</a>

    </body>
    </html>
    
当用户点击链接 "Test $GET"，参数 "subject" 和 "web" 被发送到 "test_get.php"，然后您就能够通过 $_GET 在 "test_get.php" 中访问这些值了。

下面的例子是 "test_get.php" 中的代码：

实例

    <html>
    <body>

    <?php 
    echo "Study " . $_GET['subject'] . " at " . $_GET['web'];
    ?>

    </body>
    </html>
