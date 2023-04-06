## 1.数组对象

#### 		1.数组的概述 ( Array )

​			1.数组可以把一组相关的数据一起存放，并提供方便的访问方式

​			2.数组是指 一组数据的集合，其中每个数据被称为 元素 ，在数组中可以存放 任意类型的元素，数组				是一种将 一组数据存储在单个变量名下的方式

#### 		2.创建数组

##### 			2.1 数组的创建方式

​				1.利用 new 创建数组

​				2.利用数组字面量创建数组

​					var 数组名 = [];

​					var 数组名 = [1,2,3,4,5,'S','i','w','o','e','r']  数组初始化

​				3.数组内的数据要用逗号分隔

​				4.数组里面的数据 称为数组元素

##### 			2.2 数组元素的类型

​				1.数组内可以存放任意类型的数据

#### 		3.获取数组元素

##### 			1.数组的索引

​				1.索引下标 用来访问数组的序号(数组下标从0开始)

​					var arr = ['小白','小黑','小粉','小蓝']

​					索引号        0      1     2     3 

##### 			2.获取数组元素 

​				1. 格式 数组名[索引号]

​					var arr = [1,2,3,4,5,6]//获取 3

​					console.log(arr[2])	//3

​				2.没有数组元素 输出的结果为 undefined

​				3.练习 数组练习

​						定义一个数组，里面存放星期一，星期二...直到星期日（共7天），在控制台输出：							星期日

~~~html
<script>
var arr = ['星期一','星期二','星期三','星期四','星期五','星期六','星期日']
console.log(arr[6])
</script>
~~~

#### 		4.遍历数组

##### 			1.遍历

​				把数组中的每个元素从头到尾都访问一次

~~~html
<script>
var arr = ['a', 'b', 'c']
    for (var i = 0; i < 3; i++){
      console.log(arr[i])
    }
  //因为数组索引从0 开始 所以i必须从0开始 i<3
  
</script>
~~~

##### 			2.案例 遍历数组

​					请将['关羽','张飞','马超','赵云','黄忠','刘备','姜维'];数组里的元素依次打						印到控制台

~~~html
<script>
var arr = ['关羽','张飞','马超','赵云','黄忠','刘备','姜维'];
  for(var i = 0; i < 7; i++){
    console.log(arr[i])
  }
</script>
~~~

##### 			3.数组的长度

​				1.使用 数组名.length 可以访问数组元素的数量(数组长度)

​				2.数组的长度是元素个数 不要和索引混淆

​				3.arr.length 动态监测数组元素的个数

##### 			4.案例 数组求和及平均值

​				求数组[2,3,1,7,4]里面所有元素的和以及平均值

~~~html
<script>
 var arr = [2,3,1,7,4];
    var sum = 0;
    var pjun = 0;
    for(var i = 0; i < arr.length; i++){
      sum += arr[i]
    }
    pjun = sum / arr.length
    console.log(pjun)
    console.log(sum)
  //console.log(可以输出多个用逗号分隔)
  //console.log(pjun,sum)
</script>
~~~

##### 			5.案例 求数组最大值

​				求数组[2,6,1,77,52,25,7]

~~~html
<script>
  //1.
 var arr = [2, 6, 1, 77, 52, 25, 7];
    var max = 0;
    for (var i = 0; i < arr.length; i++){
      if (arr[i] < arr[i+1]){
        max = arr[i+1]
      }
    }
    console.log(max)
  //2.
  var arr = [2, 6, 1, 77, 52, 25, 7];
    var max = arr[0];
    for(var i =1 ; i < arr.length; i++){
      if(arr[i] > max){
        max = arr[i]
      }
    } 
    console.log(max)
</script>
~~~

##### 			6.案例 数组转换为分割字符串

​				将数组['red','green','blue','pink']转换为字符串，并且用｜或其他符号分割

​					输出: 'red|green|blue|pink|'

~~~html
<script>
var sum = ''
    var arr = ['red', 'green', 'blue', 'pink']
    for (var i = 0; i < arr.length; i++) { 
      sum += arr[i] + '|'
    }
    console.log(sum)
</script>
~~~

#### 			7.数组中新增元素

​					1.通过修改length长度新增数组元素

​						length属性是可读写的

~~~html
<script>
var arr = [1,2,3,4,5,6]
arr.length = 9 
  console.log(arr)
  console.log(arr[5])
  console.log(arr[8])
//声明变量未给值 默认是undefined
</script>
~~~



​					2.通过修改数组索引新增数组元素

​						不要直接给数组名赋值，否则会覆盖掉以前的数据

~~~html
<script>
var arr = [1,2,3,4,5]
arr[5] = 6;//[1,2,3,4,5,6]
  console.log(arr)

 var arr = [1,2,3,4,5]
 arr[2] = 7;
  console.log(arr)//[1,2,7,4,5]
</script>

~~~

​				3.案例 数组新增元素

​					新建一个数组 里面存放10个整数（1-10）

~~~html
<script>
var arr = [];
    for (var i = 0; i <= 9; i++) {
      arr[i] = i + 1
    }
    console.log(arr)
</script>
~~~

​				4.案例 筛选数组

​					将数组[2,0,6,1,77,0,52,0,25,7]

~~~html
<script>
//1.
  var arr = [2,0,6,1,77,0,52,0,25,7];
    var Arr = [];
    var j = 0;
    for(var i = 0; i < arr.length; i++){
      if(arr[i] >= 10){
        Arr[j] = arr[i]
        j++
      }
    }
    console.log(Arr)
 //2.
  var arr = [2,0,6,1,77,0,52,0,25,7];
    var newarr = [];
    for(var i = 0; i < arr.length; i++){
      if (arr[i] > 10 ){
        newarr[newarr.length] = arr[i]
      }
    }
    console.log(newarr)
</script>
~~~

#### 			8.案例

##### 				1.删除指定数组元素

​					将数组[2,0,6,1,77,0,52,0,25,7]中的0去掉，形成一个不包含0 的新数组

~~~html
<script>
var arr = [2,0,6,1,77,0,52,0,25,7];
    var newarr = [];
    for(var i = 0; i < arr.length; i++){
      if(arr[i] !== 0 ){
        newarr[newarr.length] = arr[i]
      }
    }
    console.log(newarr)
</script>
~~~

##### 				2.翻转数组

​					将数组['red','green','blue','pink','purple']的内容反过来存放

~~~html
<script>
var arr = ['red','green','blue','pink','purple']
    var newarr = [];
    for(var i = arr.length - 1 ; i >= 0;i--){
      newarr[newarr.length] = arr[i]
    }
    console.log(newarr)
</script>
~~~

##### 				3.数组排序（冒泡排序）

​					1.是一种算法 把一系列的数据按照一定的顺序进行排列显示（从小到大或从大到小）

​						一次比较俩个元素 如果顺序错误就把他们交换过来

~~~html
<script>
var arr = [5, 4, 3,9,7, 2, 1]
    for (var i = 0; i <= arr.length-1;i++){
      for(var j = 0; j <= arr.length - i -1; j++){
        if(arr[j] > arr[j + 1]){
          [arr[j],arr[j + 1]] = [arr[j + 1],arr[j]]
        }
      }
    }
    console.log(arr)
</script>
~~~

​					