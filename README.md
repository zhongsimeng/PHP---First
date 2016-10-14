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
  * 变量名称只能保护数字字符和下划线（A-z,0-9以及_）
  * 变量名称对 大小写敏感（$y与$Y是两个不同的变量）
  
 >PHP变量名称对 大小写敏感
  
