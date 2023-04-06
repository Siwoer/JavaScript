## 1.运算符

​	1.介绍: 运算符称为操作符，用于实现赋值，比较和执行算数运算等功能的符号

## 2.算数运算符

​	1.概念 算术运算使用的符号，用于执行两个变量或值的算术运算

​		+(加) -(减) *(乘) /(除) %(取余数/取模)

~~~html
<script>
//1.取模
console.log(5 % 3)//2
console.log(9 % 4)//1
</script>
~~~

​	2.浮点数的精度问题

​		浮点数的最高精度是17位小数，但在进行算术计算时其精度远不如整数

~~~html
<script>
//1.浮点数 算术运算里面会有问题
 console.log(0.1 + 0.2)//0.3000000004
//2.不能直接拿浮点数进行比较 是否相等
  var num = 0.1 + 0.2;
  vonsole.log(num == 0.3);//false
</script>
~~~

​	3.小问题

​		1.怎么判断一个数能够被整除

​			可以通过进行取模运算符来进行判断

​			如果余数为0 说明这个数能被整除

​		2. 1 + 2 * 3 结果是多少

​			结果为7 算术运算符优先级，先乘除后加减，有小括号先算小括号

​	4.表达式和返回值

​		1.表达式 由数字、运算符、变量等组成的式子

​		2.返回值 表达式最终的结果，返回回来的就是返回值

​		3.在程序里面 把右边表达式计算完毕的返回值给左边

~~~html
<script>
console.log(1 + 1)//2 就是返回值
</script>
~~~

## 3.递增和递减运算符

​		1.概述: 如果需要反复给数字变量添加或减1，可以用递增(++)和递减(--)运算符来完成

​		2.递增和递减运算符必须和变量配合使用

#### 	3.2 递增运算符

​		1.前置递增运算符

​			++num 前置递增，就是自加1，类似于num = num + 1，但是++num 写起来简单

~~~html
<script>
  //1.前置递增运算符 ++ 写在前面
var age = 22;
  ++age //等于 age = age + 1 
  console.log(age)
 //2. 先加1 后返回值
  var p = 10;
  console.log(++p + 10);//21
</script>
~~~

​		2.后置递增运算符

​			num++ 后置递增，就是自加1，类似于 num = num + 1，但 num++写起来更简单

​			前置自增和后置自增如果单独使用 效果一样

​			后置自增 口诀: 先返回原值 后自加1

​			表达式先返回原值 后面变量再自加1

~~~html
<script>
var num = 10;
  num++ //num = num + 1
  console.log(num);
  
  var age = 10;
  console.log(age++ + 10)//20
  console.log(age)//11
</script>
~~~

​		3.练习

~~~html
<script>
var a = 10;
  ++a;						//11
  var b = ++a + 2;//12+2
  console.log(b)	//14
  
  var c = 10;
  c++;						  //11
  var d = c++ + 2 ; //11+2
  console.log(d);   //11 + 2 
  
  var e = 10;
  var f = e++ + ++e; //10 + 12
  console.log(f)     // 22
</script>
~~~

​		4.前置递增和后置递增小结

​			前置递增和后置递增运算符可以简化代码的编写，让变量的值+1，比以前写法更简单

​			单独使用时 运行结果相同

​			与其他代码联用时，执行结果会不同

​			后置: 先原值运算，后自加(先人后己)

​			前置: 先自加，后运算(先己后人)

## 4.比较运算符

#### 	4.1 比较运算符概述

​			1.概念: 比较运算符(关系运算符)是俩个数据进行比较时所使用的运算符，比较运算				后，会返回一个布尔值(true/false)作为比较运算符的结果

​			2.程序里面的等于符号 是 = = 比较的是值

​				默认会转换数据类型 

​			3.全等 = = = 比较的是值和值的数据类型

~~~html
<script>
console.log(3 >= 5)//fasle
console.log(3 < 5)//true

console.log(3 == 5)//false
console.log('Siwoer' == 'Leslie')//false
console.log(18 == 18)//true
console.log(18 == '18')//true 把字符串的数据类型转换为数字类型
  
console.log(18 != 18) //false
</script>
~~~

#### 	4.2 = 小结

​			1. = 表示 赋值 把右边的给左边

​			2. = = 表示 判断 两边的值是否相等(此时有隐式转换)

​			3. = = = 表示 全等 判断两边的值和数据类型是否完全相等

#### 	4.3 练习

​			var num1 = 10;

​			var num2 = 100;

​			var res1 = num1 > num2 //false

​			var res2 = num1 == 11; //false

​			var res3 = num1 != num2;//true

## 5.逻辑运算符

#### 	5.1 逻辑运算符概述

​		1.概念: 逻辑运算符是用来进行布尔值运算的运算符，其返回值也是布尔值，后面开发中经常			用于多个条件的判断

​		2. && 简称: 与 and   || 简称: 或 or   ！ 简称: 非 not

~~~html
<script>
	//1.&&  //只有两侧都为true 结果才为true
  console.log(3 > 5 && 3 > 2) //3>5为false，3>2为true。 //false
  console.log(3 < 5 && 3 > 2) //3 < 5 为true，3 > 2 为true。 //true
  //2.||   //只要有一个成立就为true
  console.log(3 > 5 || 3 > 2) // true 
  //3.!
  console.log(!true) //false
</script>
~~~

​		3.练习

~~~html
<script>
		var num = 7;
    var str = '我爱你～中国～'
    console.log(num > 5 && str.length >= num);//true
    console.log(num < 5 && str.length >= num);//false
    console.log(!(num < 10));//false
    console.log(!(num < 10 || str.length == num));//false
</script>
~~~

​		4. 逻辑  与  短路运算 （逻辑中断）	

​			如果表达式1结果为真 则返回表达式2，如果表达式1为假 那么返回表达式1

​			如果有空的或者否定的为假 其余是真的 0 '' NaN null undefined

~~~html
<script>
console.log(123&&456)//456
console.log(0&&123)//0
console.log(0&&1+2&&456)//0
</script>
~~~

​		5.逻辑  或  短路运算 （逻辑中断）

​			如果表达式1 结果为真 则返回的是表达式1，如果表达式1 结果为假 则返回表达式2

~~~html
<script>
console.log(123 || 456)//123
console.log(0 || 123)//123
  console.log(0 || 123 || 456)//123
  var num = 0;
  
  console.log(123 || num++)//123
  console.log(num)//0 因为上面代码执行到123就结束了
</script>
~~~

## 6.赋值运算符

​		1.概念: 用来把数据赋值给变量的运算符。

​		2. = 表示 直接赋值 ，+= -= 表示 加 减一个数后在赋值 ，*= /= %= 表示乘 除 取模			后在赋值

~~~html
<script>
var num = 10;
  num += 2
  console.log(num)//12
var num = 2;
  num *= 3;
  console.log(num)
var num = 16;
    num %= 3;
    console.log(num)
</script>
~~~

## 7.运算符优先级

​		1.小括号 > 一元运算符 > 算数运算符 > 关系运算符 > 相等运算符 > 逻辑运算符 >赋值			运算符 > 逗号运算符

​		2. 练习1

~~~html
<script>
console.log(4 >= 6 || '人' != '阿凡达' && !(12 * 2 == 144) && true)//true
  var num = 10;
  console.log(5 == num / 2 && (2 + 2 * num).tostring()==='22') //true
</script>
~~~

​		3.练习2

~~~html
<script>
var a = 3 > 5 && 2 < 7 && 3 == 4
console.log(a) //false 有一个为假 则为假
  
var b = 3 <= 4 || 3 > 1 || 3 != 2
console.log(b) // true
  
var c = 2 === '2'
console.log(c) // false
  
var d = !c || b && a 
console.log(d) // true
</script>
~~~

