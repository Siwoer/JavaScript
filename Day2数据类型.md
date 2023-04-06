### 1.数据类型简介

##### 	1.1 为什么需要数据类型

​		数据类型就是数据的类别型号。

##### 	1.2 变量的数据类型

​		变量的数据类型根据赋值的值来确定的

​		JavaScript 动态语言 变量的数据类型是可以变化的

~~~html
<script>
var num = 10; //数字类型
var str = 'Siwoer'//字符串类型
console.log(typeof(str))//string
  
var a = 10;//数字类型
  a = 'Siwoer'//字符串类型
</script>
~~~

##### 	1.3 数据类型的分类

​		JavaScript的数据类型分为两类:

​			简单数据类型 (Number,String,Boolean,Undefined,Null,)

​			复杂数据类型 (Object)

### 2.简单数据类型

##### 	2.1 简单数据类型 及 说明

​		Number 数字类型,包含整数型值和浮点型值, 如 21 、0.21

​		Boolean 布尔值类型,如 true、false,等于1和0

​		String 字符串类型,如"张三" JS中 字符串都带引号

​		Undefined 未定义 var a;声明了但未赋值 此时 a = undefined

​		Null 表示空、没有 var a = null; 声明了变量a为空值

#### 	2.2 数字类型( Number )

​		1.数字类型既可以用来保存整数值，也可以保存小数( 浮点数 )

​		2.数字进制

​			 二进制、八进制、十进制、十六进制

​			八进制前面加 0 , 十六进制前面加 0x

​		3.数字类型最大值和最小值 

​			Number.MAX_VALUE Number.MIN_VALUE

​		4.数字类型的三个特殊值

​			Infinity 表示无穷大,大于任何数值

​			-Infinity 表示无穷小,小于任何数值

​			NaN 表示Not a number,代表一个非数值

​		5.isNaN()这个方法用来判断是否为非数字 并返回一个值 如果是数字返回的是false 如果不			是放回true

​			

~~~html
<script>
var age = 21;//整数
var Age = 22.2222;//浮点数
console.log(Number.MAX_VALUE*2)//Infinity 无穷大
console.log(-Number.MAX_VALUE*2)//-Infinity 无穷小
console.log('Siwoer' - 22)//NaN
  
console.log(isNaN(12))//false 不是非数字
console.log(isNaN('Siwoer'))//true 是非数字
</script>
~~~

#### 	2.3 字符串类型( String )

​		1.字符串可以是引号内任意文本，其语法为双引号“”和单引号‘’

​		2.字符串引号嵌套

​			可以用单引号嵌套双引号,或者用双引号嵌套单引号(外双内单,外单内双)

​		3.字符串转义字符

​			\n 换行符、n是newline的意思

​			\\\ 斜杆\

​			\\' 单引号

​			\\" 双引号

​			\t tab缩进

​			\b 空格、b是blank的意思

~~~html
<script>
var a = '123'//字符串类型
var b = 我爱你 // 报错 因为没有加引号
var c = '我"爱"你' 

var str = 'wo\tsi\tni'
console.log(str)//wo	si	ni
</script>
~~~

​		4.案例 弹出警示框

~~~html
<script>
var str = '酷热难耐，火辣的太阳底下，我挺拔的身姿，成为了最为独特的风景。\n我审视四周，这里，是我的舞台，我就是天地间的王者。\n这一刻，我豪气冲天，终于大喊一声："收破烂啦～"'
alert(str);
</script>
~~~

​		5.字符串长度

​			字符串由若干个字符组成这就是字符串长度，可以通过length属性获取整个字符串的长			度

​			检测获取字符串的长度 length

~~~html
<script>
var str = 'Siwoer and Leslie'
console.log(str.length)//17
</script>
~~~

​		6.字符串拼接

​			多个字符串之间可以使用+进行拼接，其拼接方式为字符串+任何类型 = 拼接之后的新字			符串

​			字符串的拼接 + 

​			数字类型的数字和数字类型的数字中间用 + 表示数字相加 (数值相加，字符相连)

​			字符串与变量拼接 变量不能添加引号，因为引号会把变量变成字符串

~~~html
<script>
console.log('我是'+'假的'+110)//我是假的110
console.log('我是'+'大帅哥')//我是大帅哥
console.log('Siwoer'+22)//Siwoer22
console.log('Siwoer'+ true)//Siwoertrue
console.log(12 + 12)//24
console.log('12' + 12)//1212
 //字符串拼接加强
  var age = 22;
  console.log('Siwoer' + age + '岁了')//Siwoer22岁了
</script>
~~~

​		7.案例 显示年龄

​			弹出一个输入框，需要用户输入年龄，之后弹出一个警示框显示“您今年xx岁啦”(xx表			示刚才输入的年龄)

~~~html
<script>
var str = prompt('请输入您的年龄')
var str1 = '您今年已经' + str + '岁了' 
alert(str1)
</script>
~~~

#### 	2.4 布尔值类型

​		1.布尔类型有俩个值 true 和 false ， 其中true 表示真(对),而false表示假(错)

​		2.布尔值类型和数字类型相加时，true的值为1 false的值为0

~~~html
<script>
  console.log(true + 1)//2
  console.log(false + 1)//1
</script>
~~~

#### 	2.5 Undefined 和 Null

​		1.一个声明后没有被赋值的变量会有一个默认值undefined(如果进行相连或者相加时，注意			结果)

​		2.如果一个变量声明未赋值 就是undefined 未定义数据类型

​		3.一个声明变量给null值,里面存储的值为空

~~~html
<script>
var abb = undefined;
console.log(abb + 'ppp')//abbppp
console.log(abb + 1)//NaN
var pop = null;
console.log(pop + 'pop')//poppop
console.log(pop + 1)//1
</script>
~~~

### 3.获取变量数据类型

#### 	3.1 获取检测变量的数据类型

​		1.typeof 可用来获取检测变量的数据类型

~~~html
<script>
var num = 10;
  console.log(typeof num)//Number
  var str = 'Siwoer'
  console.log(typeof str)//String
  var bl = true;
  console.log(typeof bl)//boolean
  var und = undefined;
  console.log(typeof und)//undefined
  var nul = null;
  console.log(typeof nul)//object
</script>
~~~

#### 	3.2 字面量

​		1.字面量是在源代码中一个固定值的表示法，简单来说，就是字面量表示如何这个值

​			数字字面量 8，9，10

​			字符串字面量 'Siwoer' "发财"

​			布尔值字面量 true false

### 4.数据类型转换

#### 	4.1 什么是数据类型转换

​		1.就是把一种数据类型的变量转换成另外一种数据类型

​			转换为字符串类型

​			转换为数字类型

​			转换为布尔类型

#### 	4.2 转换为字符串

​		1.toString() 和 String()的使用方法不同

​		2.加号拼接字符串转换方式也称之为 隐式转换

~~~html
<script>
// 1.把数字类型转换为字符串类型 变量.toString
	var num = 10;
  var str = num.toString()
  console.log(str) //10
  console.log(typeof str)//string
// 2.利用String(变量)
  var num = 10;
  console.log(String(num));//10 字符串类型
// 3.利用 + 拼接字符串的方法实现转换效果
  var num = 10;
  console.log(num + '')//10 字符串类型  //将num转换为字符串类型再进行拼接
</script>
~~~

#### 	4.3 转换为数字类型

​		1.方式

​			parseInt() 将string类型转成整数的数值型

​				需要识别的第一个字符为数字

​				取整

​			parseFloat() 将string类型转成浮点数的数值型

​				可识别一次小数点

​				需要识别的第一个字符为数字

​			Number() 将string类型转换为数值型

​				

​			隐式转换( - * /) 利用算术运算隐式转换为数值型

~~~html
<script>
var num = '3.14'
var str = '120px'
console.log(parseInt(num))//3 会取整且转换为数字类型
console.log(parseInt(str))//120 会去掉px单位
console.log(parseInt('em12o'))//NaN
console.log('12' - 0)//12
</script>
~~~

#### 	4.5 案例

​			1.计算年龄 要求在页面中弹出一个输入框，我们输入出生年份后，能计算出我们的年龄

~~~html
<script>
var age = prompt('请输入出生年份')
var age1 = 2023 - age
alert('您今年已经'+age1+'岁了')
</script>
~~~

​			2.简单加法器 计算两个数的值，用户输入第一个值后，继续弹出第二个输入框并输入第				二个值，最后通过弹出窗口显示出两次输入值相加的结果

~~~html
<script>
var num = prompt('请输入第一个值:')
var num2 = prompt('请输入第二个值:')
alert(Number(num) + Number(num2))
</script>
~~~

#### 	4.6 转换为布尔型

​			1.方式

​				Boolean() 其他类型转换为布尔型

​			2.代表 空、否定的值会被转换为false，如'' 0 NaN null undefined

​				其余值都会被转换为true

~~~html
<script>
console.log(Boolean(''))//false
console.log(Boolean(0))//false
console.log(Boolean(NaN))//false
console.log(Boolean(null))//false
console.log(Boolean(undefined))//false
console.log(Boolean(12))//true
console.log(Boolean('Siwoer'))//true
</script>
~~~

#### 	4.7 扩展

​		1.解释型语言和编译型语言

​			解释型:JavaScript通过解释器边解释边执行语言

​			编译型:Java通过编译器将语言编译结束完成才开始执行代码

​			解释器:直接执行用编程语言编写的指令程序

​			编译器:把源码转换成低级语言的程序

​		2.标识符、关键词、保留字

​			2.1 标识符:就是指开发人员为变量、属性、函数、参数的名字

​				标识符不能是关键字或者保留字

​			2.2 关键字:就是指JavaScript本身已经使用了的字，不能再用它们充当变量名、方法				名

​			2.3 保留字: 就是指预留的'关键字'，意思是现在虽然还不是关键字，但是未来有可能				成为关键字 也不能当变量名、方法名

#### 	4.8 作业

​		1.依次询问并获取用户的姓名、年龄、性别、并打印出来

~~~html
<script>
 		var name = prompt('请输入您的姓名');
    var age = prompt('请输入您的年龄');
    var sex = prompt('请输入您的性别');
    alert('您的姓名:' + name + '\n您的年龄:' + age + '\n您的性别:' + sex)
</script>
~~~



