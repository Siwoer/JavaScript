## 1.循环

#### 		1.循环的目的

​			可以重复执行某些代码

#### 		2.JavaScript中的循环

​			for循环

​			while循环

​			do...while循环

## 2.for循环

​		1.概述

​			一组被重复执行的语句称之为循环体，能否继续重复执行，取决于循环的终止条件。

​			由循环体及循环的终止条件组成的语句，称为循环语句

​		2.语法结构

​			for循环把某些代码循环若干次，通常和计数有关

​			初始化变量 就是用var 声明的一个普通变量，通常用于作为计数器使用

​			条件表达式 就是用来决定每一次循环是否继续执行 就是终止的条件

​			操作表达式 每次循环最后执行的代码 经常用于我们计数器变量进行更新（递增或者递减）

~~~html
<script>
for(初始化变量;条件表达式;操作表达式){
  	//循环体
}
//代码体验
  for(var i = 1;i <= 100; i++){
    console.log('你好');
  }
</script>
~~~

​		3.执行过程

~~~html
<script>
for(var i = 1; i <= 100; i++){
  //循环体
}
</script>
~~~



​			首先执行里面的计数器变量 var i =1; ,但是这句话在for里面只执行一次

​			其次去 i <= 100 来判断是否满足条件 如果满足条件 就去执行 循环体 不满足条件退出循环

​			最后去执行 i++ i++是单独写的代码 递增 第一轮结束

​			接着去执行 i <= 100 如果满足条件 就去执行 循环体 不满足条件退出循环 第二轮

​		4.断点调试

​			断点调试可以帮助我们观察程序的运行过程

​			浏览器打开控制台 -- sources -- 找到需要调试的文件 -- 在程序的某一行设置断点

​			watch 监视 通过watch可以监视变量的值的变化

​		5.循环执行相同代码

~~~html
<script>
var num = prompt('请输入次数')
for(var i = 1; i < num; i++){
  console.log('Baby')
}
</script>
~~~

​		6.循环执行不同的代码

~~~html
<script>
//1.输出一个人1～100岁
  for(var i = 1; i <= 100; i++){
    console.log(i + '岁了')
  }
</script>
~~~

​		7.案例 求1-100之间所有整数的累加和

~~~html
<script>
  var result = 0;
for(var i = 1; i <= 100; i++){
   result += i;
}
  console.log(result)
</script>
~~~

​		8.练习 

​			1.求1-100之间所有数的平均值

​			2.求1-100之间所有偶数和奇数的和

​			3.求1-100之间所有能被3整除的数字之和

~~~html
<script>
//1.
    var result = 0;
    for(var i = 1; i <= 100; i++){
      result += i;
    }
    console.log(result / 100)
//2.
    var result = 0;
      var jishu = 0;
      for(var i = 1; i <= 100; i++){
        if(i % 2 == 0){
          result = result + i
        } else{
          jishu = jishu + i
        }
      }
      console.log(result)
      console.log(jishu)
//3.
  	var result = 0
        for(var i = 1; i <= 100; i++){
          if(i % 3 == 0){
            result += i
          }
        }
        console.log(result)
</script>
~~~

​		9.练习2 

​			1。求学生成绩

~~~html
<script>
var num = prompt('请输入班级总人数')
    var pj = 0;//平均值
    var he = 0;//求和的变量
    for(var i = 1; i <= num; i++){
      var sum = prompt('请输入第'+ i +'个学生的成绩')
      he = he + Number(sum) 
    }
    pj = he / num
    alert('和是:' + he)
    alert('平均值是:' + pj)
</script>
~~~

​		10.练习3

​			1.一行打印五个星星

~~~html
<script>
  var str = ''
    for(var i = 1; i <= 5; i++){
      str += '☆'
    }
    console.log(str)
</script>
~~~

​		11.练习4

​			1.打印五行五列的星星

~~~html
<script>
 var str = ''
    for (var i = 1; i <= 5; i++) {
      for (var j = 1; j <= 5; j++) {
        str += '☆'
      }
      str += '\n'
    }
    console.log(str)
</script>
~~~

## 3.双重for循环

​	1.双重for循环概述

​		1.嵌套循环 

​			指在一个循环语句中再定义一个循环语句的语法结构 比如：在for循环语句中，可以再嵌套一			个for循环，这样的for循环语句称为双重for循环

​		2.语法结构

~~~html
<script>
for(外层的初始化变量;外层的条件表达式;外层的操作表达式){
  for(里层的初始化变量;里层的条件表达式;里层的操作表达式){
    //执行语句;
  }
}
</script>
~~~

​		3.外层循环一次，里面的循环执行全部

​		4.案例 打印 n 行 n 列的星星

~~~html
<script>
var str = ''
    var num = prompt('请输入您想打印几行星星')
    var num1 = prompt('请输入您想打印几列星星')
    for (var i = 1; i <= num; i++) {
      for (var j = 1; j <= num1; j++) {
        str += '☆'
      }
      str += '\n'
    }
    console.log(str)
</script>
~~~

​		5.案例 打印倒三角形

~~~html
<script>
//1.
	var str = ''
    for (var i = 1; i <= 10; i++ ){//打印10行
      for(var j = 10; j >= i; j-- ){//第一行10个星 逐行递减 一行中最少不能少于i
        str = str + '☆'
      }
      str += '\n'
    }
    console.log(str)
//2.
   var str = ''
    for (var i = 1; i <= 10; i++) { //打印10行
      for (var j = i; j <= 10; j++) {// 第一行从 1 - 10 ，第二行从 2 - 9
        str = str + '☆'
      }
      str += '\n'
    }
    console.log(str)
</script>
~~~

​		6.案例 打印正三角形

~~~html
<script>
	var str = ''
    for (var i = 1; i <= 10; i++) {
      for (var j = 1; j <= i; j++) {
        str = str + '☆'
      }
      str = str + '\n'
    }
    console.log(str)
</script>
~~~

​		7.案例 九九乘法表

~~~html
<script>
for (var i = 1; i <= 9; i++) {
      document.write('<br>')
      for (var j = 1; j <= i; j++) {
        document.write(j + 'X' + i + '=' + i * j + '\t')
      }
    }
</script>
~~~

​		8.小结

​			1.for循环可以重复执行莫呕血相同的代码

​			2.for循环可以重复执行些许不同的代码 因为我们有计数器

​			3.for循环可以重复执行某些操作，比如算术符加法

​			4.双重for循环，外层循环一次，内层for循环全部执行

​			5.for循环是循环条件和数字直接相关的循环

## 4.while循环

​		1.概述

​			while(当...的时候)语句可以在条件表达式为真的前提下，循环执行指定的一段代码，直到表达式				不为真时结束循环

​		2.语法结构

~~~html
<script>
while (条件表达式){
  //循环体代码
}
</script>
~~~

​		3.执行思路

​			1.先执行条件表达式，如果结果为true，则执行循环体代码。如果为false，则退出循环，执行后面				代码

​			2.执行循环体代码

​			3.循环体代码执行完毕后，程序会继续判断执行条件表达式，如条仍为true，则继续执行循环体，直				到循环体条件为false时，整个循环过程才会结束

​			4.代码验证

~~~html
<script>
  var num  = 1
while(num <= 100){
  console.log('咋可能')
  num++
}
</script>
~~~

​		5.里面应该也有计数器，初始化变量

​		6.里面应该也有操作表达式 完成计数器的更新 防止死循坏

​		7.案例 

~~~html
<script>
//1.打印人的一生 从1岁到100岁
  var num = 1;
  while(num <= 100){
    console.log(num);
    num++
  }
//2.计算 1-100之间所有整数的和
  var num = 1;
  var result = 0;
  while(num <= 100){
   	result += num
    num++
  }
  console.log(result)
//3.弹出一个提示框，你爱我吗？如果我爱你，就提示结束，否则，一直询问
  var num = prompt('你爱我吗？')
  while(num !== '我爱你'){
    prompt('你爱我吗？')
  }
  alert('我也爱你')
</script>
~~~

## 5.do...while循环

​		1.do...while 语句其实是while语句的一个变体，该循环会先执行一次代码块，然后对条件表达式进行			判断，如果条件为真，就会重复执行循环体，否则退出循环

​		2.语法结构

~~~html
<script>
do{
  //循环体
} while(条件表达式)
</script>
~~~

​		3.执行思路

​			跟while不同的地方在于do...while 先执行一次循环体 在判断条件 如果条件表达式结果为真，则				继续执行循环体，否则退出循环

​			1.先执行一次循环体

~~~html
<script>
var num = 1;
  do{
    console.log('22')
  } while(num <= 100)
</script>
~~~

​		4.代码验证

~~~html
<script>
 var num = 1;
    do {
      console.log('22')
      num++
    } while (num <= 100)
</script>
~~~

​		5.案例

​			1.打印人的一生 从1-100岁

​			2.计算1-100之间所有整数的和

​			3.弹出一个提示框 你爱我吗？如果输入我爱你，就提示结束，否则 一直询问

~~~html
<script>
//1.
var num = 1;
    do{
      console.log('你今年'+ num + '岁了')
      num++
    } while(num <= 100)
//2.
    var num = 1;
    var result = 0;
    do{
      result += num
      num++
    } while(num <= 100)
    console.log(result)
//3.
  do{
    var num = prompt('你爱我吗？')
    } while(num !== '我爱你')
    alert('我也爱你')
</script>
~~~

​		6.循环小结

​			1. JavaScript循环中有 for while do...while

​			2. 三个循环很多情况可以相互替代使用

​			3. 如果用来记次数，和数字相关的，三种使用基本相同

​			4. while 和 do...while 可以做更复杂的判断条件，比for灵活一些

​			5. while 和 do...while 执行次数不一样，do...while 至少会执行一次循环体，而while可能一				次也不执行

## 6.continue 和 break

​		1.continue 用于立即跳出本次循环，继续下一次循环

​		2.break 立即跳出整个循环 （循环结束）

~~~html
<script>
//1.continue 案例 求1-100之间，除了能被7整除之外的整数和
  var result = 0;
    for (var i = 1; i <= 100; i++){
      if(i % 7 == 0){
        continue;
      }
      result += i
    }
    console.log(result)
//2. break 案例 

</script>
~~~

## 7.案例 练习

​		1.求1-100之间所有数的总和与平均值

​		2.求1-100之间所有偶数的和

​		3.求100以内7的倍数的总和

​		4.使用for循环打印矩形，要求每次只输出一个星

​		5.使用for循环打印三角形

​		6.使用for循环打印99乘法表

​		7.接收用户输入的用户名和密码，若用户名为“admin”，密码为“123456”，则提示用户登入成功！否则，			让用户一直输入

​		8.求整数1-100的累加值，但要求跳过所有个位位3的数（用continue实现）

​		9.简易ATM

~~~html
<script>
//1.求1-100之间所有数的总和与平均值
   var sum = 0;//总和
    var pj = 0;//平均值
    for(var i =1;i<=100;i++){
      sum += i;
      pj = sum / 100
    }
    console.log(sum)
    console.log(pj)
//2.求1-100之间所有偶数的和
  var sum = 0;
    for(var i = 1;i<=100;i++){
      if(i % 2 == 0){
        sum += i
      }
    }
    console.log(sum)
//3.求100以内7的倍数的总和
  var sum = 0;
    for(var i =1;i<=100;i++){
      if(i % 7 == 0 ){
        sum += i
      }
    }console.log(sum)
 //4.使用for循环打印矩形，要求每次只输出一个星
  var str = ''
    for (var i = 1; i <= 5; i++) {
      for (var j = 1; j <= 5; j++) {
        str += '☆'
      }
      str += '\n'
    }
    console.log(str)
//5.使用for循环打印三角形
  var str = ''
      for(var i =1;i<=5;i++){
        for(var j = 1; j<=i;j++){
          str += '☆'
        }
        str += '\n'
      }
      console.log(str)
//6.使用for循环打印99乘法表
	var str = ''
    for (var i = 1; i <= 9; i++) {
      for (var j = 1; j <= i; j++) {
        str += j + 'X' + i + '=' + i * j + '\t'
      }
      str += '\n'
    }
    console.log(str)
//7.接收用户输入的用户名和密码，若用户名为“admin”，密码为“123456”，则提示用户登入成功！否则，			让用户一直输入
 	var str = ''
    for (var i = 1; i <= 9; i++) {
      for (var j = 1; j <= i; j++) {
        str += j + 'X' + i + '=' + i * j + '\t'
      }
       str += '\n'
    	}
    	console.log(str)
//8.求整数1-100的累加值，但要求跳过所有个位位3的数（用continue实现）
  var sum = 0;
    for(var i =1;i<=100;i++){
      if(i % 10 == 3){
        continue;
      }
      sum += i
    }
    console.log(sum)
</script>
~~~

