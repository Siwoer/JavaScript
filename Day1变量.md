## 第一天

### JavaScript的引入方式

​	1.行内式 写在html标签内部

~~~html
<input type="button" value"唐伯虎" onclick="alert('秋香')">
~~~

​	2.内嵌式 通过在script标签内操作

~~~html
 <script>
   alert('沙漠骆驼')
</script>
~~~

​	3.外链式 引入外部文件夹my.js

~~~html
<script src="my.js">
  //此处不允许写任何代码
</script>
~~~

### JavaScript的注释

​	1.单行注释 

​		window: ctrl + /   mac: command + /

​	2.多行注释

​		window: shift + alt + a Mac: shift + option + a

### JavaScript的输出语句

​	1.prompt 输入框

~~~html
<script>
  prompt('我是输入框')
</script>
~~~

​	2.alert  警示框

~~~html
<script>
  alert('我是警示框')
</script>
~~~

​	3.console 控制台输出

~~~html
<script>
  console.log('我是控制台输出')
</script>
~~~

### JavaScript变量

##### 	1.变量的概述

​		1.1 什么是变量

​			变量是用于存放数据的容器。我们通过变量名获取数据，甚至数据可以修改。

​		1.2 变量在内存中的存储

​			变量是程序在内存中申请的一块用来存放数据的空间，通过变量的名字来找到变量

​			白话解释: 在一个行李箱内放入你想放在行李箱内东西，每个放进去的东西都有一个名字

##### 	2.变量的使用

​		2.1 声明变量

​			通过 var 关键字来进行声明变量，使用该关键字声明变量后，计算机会自动为变量分配内			存空间不需要程序员管			

​			age 是定义的变量名字，通过age这个变量名字来访问内存中分配的空间

~~~html
<script>
  //声明变量
  var age;//声明一个名字为age的变量
</script>
~~~

​		2.2 赋值

​			通过 = 来进行变量赋值

​			变量值是保存到变量空间内的值

~~~html
<script>
  //变量赋值
  var age = 22;//给age这个变量赋值为22
</script>
~~~

​		2.3 变量的初始化

​			声明一个变量并赋值，为变量初始化

~~~html
<script>
  //变量初始化
  var age = 22 // 初始化
</script>
~~~

##### 	3.案例：变量的使用

​		1.

​		有个叫卡卡西的人在旅店登记的时候前台让他填一张表，这张表里的内容要存到电脑上，表内有 		姓名 年龄 邮箱 家庭住址和工资 存储之后需要把些信息显示出来，所显示的内容如下：

​		我叫旗木卡卡西，我住在火影村，我今年30岁了，我的邮箱是1679708458@qq.com，我的工资		是1200

~~~html
<script>
  var xming = 'Siwoer'
  var nling = 22
  var yxiang = '1679708458@qq.com'
  var dzhi = '杨岐路39号'
  var gzi = 1200
  alert('我叫'+ xming + ',我住在' + dzhi + ',我今年'+ nling + '岁了' + ',我的邮箱是' + yxiang + ',我的工资' + gzi) 
</script>
~~~

​		2.

​		弹出一个输入框，提示用户输入姓名。

​		弹出一个对话框，输出用户刚才输入的姓名

~~~html
<script>
  var result = prompt('请输入姓名')//把用户输入的姓名赋值给result
  alert(result) 
</script>
~~~

##### 	4.变量语法拓展

​		1.更新变量

​			一个变量被重新赋值后，它原有的值就会被覆盖，变量值将以最后一个赋的值为准

~~~html
<script>
var myname = 'Siwoer'
	console.log(myname)//Siwoer
		myname = 'Leslie'
  console.log(myname)//Leslie 通过变量名字 将变量空间内的值进行改变
</script>
~~~

​		2.声明多个变量

​			同时声明多个变量时，只需写一个var，多个变量名之间使用英文逗号隔开

~~~html
<script>
var age = 22,
    name = 'Siwoer',
    gzi = 1200;
</script>
~~~

​		3.声明变量的特殊情况

​			3.1 只声明不赋值 结果是？

​				计算机也不知道里面存的是啥 所以结果是 undefined 未定义

~~~html
<script>
	var sex;
  console.log(sex)//undefined
</script>
~~~

​			3.2 不声明 不赋值 直接调用会报错

~~~html
<script>
console.log(sex)
</script>
~~~

##### 			3.3 不声明直接赋值使用

~~~html
<script>
  age = 22;
  console.log(age)//可以使用 全局变量
</script>
~~~

##### 	5.变量命名规则

​			1.由字母(a-z)(A-Z)、数字(0-9)、下划线(_)、美元符号($)组成

​			2.严格区分大小写。var app 和 var APP 是两个变量

​			3.不能数字开头

​			4.不能是关键字 保留字 var for while 之类的

​			5.变量名必须有意义 nl 　--age

​			6.遵守驼峰命名法。首字母小写,后面单词的首字母需要大写 myName

##### 	6.交换俩个变量的值

​			案例 将b的值和a的值进行交换

~~~html
<script>
  var temp;
  var a = 1;
  var b = 2;
  temp = a;
  a = b;
  b = temp;
  console.log(a)
  console.log(b)
</script>
~~~

##### 	7.总结

​		1.为什么需要变量

​			因为我们有一些数据需要保存,所以需要变量

​		2.变量是什么

​			变量就是个容器用来存放数据的，方便以后使用里面的数据

​		3.变量的本质是什么

​			变量是内存里的一块空间，用来存储数据

​		4.变量怎么使用的

​			使用变量的时候进行声明变量然后赋值

​				声明变量的本质就是去内存中申请一个空间

​		5.什么是变量的初始化

​			声明变量并且赋值 为变量的初始化

​		6.变量命名的规范有哪些

​			由大小写字母、数字、$、_组成

​			不能是数字开头，不能是关键字 保留字，还要严格区分大小写

​			要见名知意 驼峰命名法

​			

​				