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
  
  PHP文件的默认文件扩展名是“。PHP”。
  
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
  
    使他人理解代码工作；
    
    提醒自己做过什么，思路。
    
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
  
    *整数必须有至少一个数字（0-9）
    
    *整数不能包含逗号或者空格
    
    *整数不能有小数点
    
    *整数征服均可
    
    *可以用三种格式规定整数：十进制、十六进制、（前缀是0x）或八进制（前缀是0）
    
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
  
  手续我们必须声明对象的类。对此，我们使用class关键词。类是包含属性和方法的结构。
  
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
