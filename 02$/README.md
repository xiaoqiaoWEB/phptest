#02$
	1.变量类型
	2.变量测试
	3.变量装换
	
#1.php标签
	<?php
		//php代码
	?>

#2.php脚本中允许混编
	<hr>
	<?php
		echo '111';
	?>
	<hr>
	<?php
		echo '222';
	?>

#3.PHP基础语法
	1).变量定义
	2).变量命名
	3).变量输出
	4).变量用法
	5).变量类型
	6).php中字符串连接
	7).单双引号使用
	8).测试变量
	9).删除变量
	10).变量类型测试
	11).php函数分类
	12).预定义变量
	13).运算符
	14).或运算和与运算开关
	15).位运算符
	16).运算符优先级
	
#变量定义:
$x=10;

#变量输出:
echo $x;

#变量命名:
变量名称是区分大小写的.

#变量用法:
	1.普通变量
	$a=10;
	
	2.可变变量
	$hello='world';
	$world='123456';
	echo $$hello;
	echo $world;
	
	3.引用变量
	$a=10;
	$b=&$a;

#变量类型:
	1.整型
	$a=10;
	
	2.浮点型
	$a=10.5;
	
	3.字符串
	$a='hello world!';
	
	4.布尔型
	$a=true;
	$b=false;
	
	5.数组
	$a=array(5,'hello',10.2,true);
	print_r($a);
	
	6.对象
	
	7.资源
	
	8.NULL
	$a=null;
	
#对象类型:
	a.属性(特征)
	b.方法(行为)
	c.使用:
	class Person{
		//特征
		public $name='狗蛋';
		public $age=20;
		public $sex='nan';
	
		//行为
		public function say(){
			echo "今天天气很好，今天心情很不错!<br>";
		}
	
		public function eat(){
			echo "我生下来就会吃饭，我很开心!<br>";
		}
	}
	$user1=new Person();
	$user1->say();

#资源类型:
	a.数据库连接资源
	$conn=mysql_connect('localhost','root','12345678');

#null类型
	$str=null;

#PHP中8种变量类型:
	一.标量
	1.整型
	2.浮点型
	3.字符串
	4.布尔型
	
	二.复合类型
	5.数组
	6.对象
	
	三.特殊类型
	7.资源
	8.NULL

#字符串连接符:.
echo $a.$b;

#单双引号的区别:
	1.双引号中可以解析变量.
	2.单引号中不会解析变量.
	3.双引号中变量尽量用{}括起来.
	4.双引号中只是解析变量并不会执行表达式，要执行用.连接.
	5.单引号和双引号要交叉使用.
	6.单引号用单引号时要在之前加\把特殊性取消掉.
	7.双引号用双引号时要在之前加\把特殊性取消掉.

#测试变量类型:
	1.var_dump();
	2.gettype();
	3.精确判断某种类型:
	is_bool(),is_int(),is_float(),is_string(),is_array(),is_object(),is_resource(),is_null(),is_scalar(),is_callable()

#测试变量是否存在:
	1.isset();
	#不存在:
	1)变量未定义;
	2)$a=null;

	2.empty();
	#为空:
	1)未定义
	2)0
	3)0.0
	4)false
	5)null
	6)''
	7)'0'
	8)array()

#变量类型自动转换:
	1.自动类型转换
	2.强制类型转换

	自动类型转换:
	1.字符串转整型
	2.整型转字符串
	3.所有类型转布尔型，为假的情况:
	1)未定义
	2)0
	3)0.0
	4)false
	5)null
	6)''
	7)'0'
	8)array()

	强制类型转换:
	1.字符串转整型
	$b=(int)$a;
	
	2.整型转字符串
	$b=(string)$a;
	
	3.所有类型转布尔型
	$b=(bool)$a;