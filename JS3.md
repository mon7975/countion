#JS第三部分

##Switch语句
 - Switch(变量 n){
    -  case 1:
    -  执行的代码;
    - break;
    - case 5:
    -  执行的代码;
    - break;
    - default:
    - 执行的代码;
    - break;
 - }
 + Switch 语句后变量根据数据类型必须和case后的数据类型保持一致(适合较少的种类判断，且知道有多少种)
 > swith(frult){
 >   case 1:
 >    alert('苹果')；
 >   break;
 >   case 2:
 >    alert('香蕉')；
 >   break;
 >   case 3:
 >    alert('葡萄')；
 >   break;
 >   default:
 >    alert('找不到');
 >   break;
 > }
 +  字符串转化为Number类型
  +  3-'0'=3;
  +  parseInt('3') ==>3;  int整数类型
  +  parseFloat('3.3') ==>3.3 ； Float小数类型

##自增自减

 i++         ++i
 - 变量没有参与运行时，i++和++i表示在原来值的基础上加1
 - 变量参与运行：
   1.  i++， i先运算，再执行++  
   2.  ++i， ++先执行，i再参与运算

##While循环    

- while(条件表达式){
   当条件表达式结果为true，会一直执行while循环中的代码； 当条件表达式结果为false时，while循环不再执行.
}      
> var n = 1;
> while(n<=10){
>   console.log(n);
>   n++;
> }
+ while循环中，先在while循环外部定义变量，后判断条件。

## Do.while循环

> do{

>  循环体

> }

>while(条件表达式);
- do while循环开始时，之间进入循环内部，执行完第一遍循环代码后，进行while条件判断。如果while条件结果为true，将继续执行do中的代码。结果为false将不在执行
- do while循环再条件不满足时比while多执行一次代码

##For循环
> fot(var i=0; i<=10; i++){

>  循环代码

> }
- 执行顺序 
  - 先进行变量初始化，并进行条件判断
  - 条件结果为true，将执行循环代码，后执行i++
  - 判断条件是否为true，继续执行循环内代码，否则跳出循环

##Break语句

 - 当循环内，代码遇到break时，程序立刻结束循环
 - 当前循环指break语句所在的循环

 > var num =10;

 > for(var i=0; i<100; i++){

 >  console.log((i);

 > if(num== i){

 > console.log('结束循环');
 -  一旦break循环结束，当前循环内部break后的代码不会执行  
 > break;

 > } console.log('么么哒');

 >}

 > console.log('end for...')；

 ##Continue语句

 - Continue指跳出本次循环，该语句后面代码不再执行
> for(var i=1; i<=100; i++){

> if(i%7==0){
   
   > console.log(i);

   > continue;
  - 一旦continue跳出，后面代码不再执行
 > }

>  if(i%17==0;){

   > console.log(i);

 > } 

>}

###9x9乘法表
> for(var i =1; i<=9; i++){

   >var ht='';

   >for(var h=1; h<=9;h++){
      if(h>i){
         break;
      }
   >ht=ht+(i+'*'+h+'='+i*h+'');

   >}

   >console.log(ht);
}

##数组
 - 定义
   - var arr=new Array(); 通过对象方式创建数组
   - var arr=[]  直接创建数组
 - 赋值
   - 数组通过下标方式赋值，下标从0开始
 - 属性
   - 数组中元素数量，通过数组名.length获得数组元素个数
 - 数组两种遍历方式
  > var arr = [1,3,12,34,7];
  
  > for(var i = 0 ; i < arr.length ; i++)
  
  >{
		console.log('下标为'+i,arr[i]);
		}
   
   >var arr = [1,3,12,34,7];

   >for(var a in arr)
   
   >{
			console.log(arr[a])
		}

 - concat()数组合并
  > var arr = [1,2,3];
		var arr2 = [4,5,6];
   
   >var arr3 = arr.concat(arr2);
		
   > console.log(arr);
	
   >	console.log(arr3);

 - join()把数组转换为字符串
   -  join()将数组各个元素通过指定的分隔符进行连接成为一个字符串 
   >var arr4 = ['a','b','c'];
	
   >	console.log(arr4.join(','));其结果为a,b,c
 - split()字符串转换为数组
   - split()可把字符串分割成字符串数组 
   >var str = 'it is a fineday today';
	
   > var arr5 = str.split(' ');
	
   > console.log(arr5); 结果: ['it', 'is', 'a', 'fineday', 'today']
 
 - 添加数组元素
   - push() 从尾巴添加一个或多个元素
   - unshift()从数组前面放入一个或多个元素
 - 删除数组元素
   - pop()删除数组最后一个元素
   - shift()删除数组第一个元素
 - 冒泡算法和选择顺序
   - 冒泡排序（Bubble Sort），是一种计算机科学领域的较简单的排序算法。
   -  它重复地走访过要排序的元素列，依次比较两个相邻的元素，如果他们的顺序（如从大到小、首字母从A到Z）错误就把他们交换过来。走访元素的工作是重复地进行直到没有相邻元素需要交换，也就是说该元素已经排序完成。
   >var arr = [8,5,4,3,2];

		// 第一轮
		for(var i = 0 ; i < arr.length-1 ; i++){
			if(arr[i]>arr[i+1]){
				//交换位置
				var temp = arr[i];
				arr[i] = arr[i+1];
				arr[i+1] = temp;
			}
			console.log(arr);
		}        (每轮length多减1)
 - 平均值
      <!-- //...  -->
        var arr = [33,21,1,40,12,5] 
		  var sum = 0 ;
		for(var i = 0 ; i < arr.length ; i++){
			sum += arr[i];
		}
		console.log(sum/arr.length);
##函数
 - 函数的声明方式分为自定义函数声明和匿名函数声明

  -  // 基本数据类型: string  number  boolean  undefined  null 
  -	// 复杂数据类型  对象类型   数组  
		// 1.声明函数的方式  函数如果不调用是不会执行的
		// 2.为什么需要函数? 可以封装一部分功能,帮我解决重复问题
		// 3.科学编程  面向对象编程  继承  封装  多态  ,函数本身就是封装的体现
	<!--  -->
		function say(){
			alert('Hello,world!');
		}
		say();
  - 函数是一种封装。将语句封装到函数中，通过调用的形式，执行语句
  - 函数的基本语法
   - function 函数名字(){
      ...内容
   }
 - 函数的参数
   - 实际参数必须和形式参数个数相同
   - 函数的重载(js中不支持,不存在过载方法)：
   如果函数名重复的话,后面会覆盖前面的方法,但是这个在java中是可以被当做两个方法正常使用过的,那么称为方法的重载.
 - 函数的返回值
   - return (返回)，返回函数执行后，后续代码不再执行，且函数中只存在一个return

##变量的作用域
 - 1. 在window对象里声明的变量,在函数里都可以使用
	2. 函数内部不能调用其他函数内部的变量
	3. 在window作用域不能调用函数内部的变量
 - 可分为全局变量和局部变量
   - 全局变量，在最外层声明的变量；函数内部没有var的变量也是全局变量
   - 局部变量，在函数内部声明的变量