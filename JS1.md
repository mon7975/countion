#javascript

##js组成 js是一款运行在客户端的网页编程语言<br>
+ 组成部分
  - ecmascript  Js标准  js基础语法
  - dom 通过JS操作网页元素  网页中的标签都被成为DOM元素
  - bom 通过api操作浏览器
+ 特点
  - 简单易用
  - 解释执行
+ 作用
  - 表单验证
  - 轮播特效
  - 开发游戏

##js书写位置
+ 内嵌式
  - <script type="text/javascript">
       alert('欢迎来到不凡学院');  	
    </script>
+ 外链式
  - <meta charset="utf-8">
  - <title>document</title>
  - <script type="text/javascript"  src="js/main.js"></script>

##用js输出内容
+ alert() 在页面弹出一个对话框，早期js调试使用
+ confirm() 在页面弹出一个对话框，常配合if判断使用
  - if(confirm('你是中国人吗')){
    alert('你好')
   }else{
    alert('对不起，我不是')
   }

+ console.log() 将信息输入到控制台，用于js调试 
+ prompt() 弹出对话框，用于接收用户输入信息(很少用)
+ document.write() 在页面输出消息  几乎不用
  - document.write可输出信息，标签，转义字符，单/双引 换行 回车

##js注释
 + 快捷键 ctrl+/
 + 单行注释  //
 + 多行注释  / *  * /

##变量  <font color="red">变量是用来存储数据的容器</font>
    x=f(a)  y=f(b)  a=5,b=3.3,a=6,a=7   x=f(a)  5=f(3)  a=3 b=5   a=10  b=15  15=f(10)
 + 定义变量
  - var a=5; var b=10; var name='张三';
  - var abc,name,password,sex,age...
  - var name='zhang';  var age=20

 + 给变量赋值
  - "="是赋值运算符

##变量的命名规范、
 + 不能以数字或纯数字开头来定义变量名
 + 不推荐用中文定义变量命
 + 不可使用特殊符号或特殊符号开头(_除外)
 + 不推荐用关键字和保留字来定义变量名
 + 在JS中严格区分大小写

##数据类型
 + 简单数据类型
  - Number 数字类型(包含正数，负数，小数)   var age=10     var mon=9.9
  - 字符串 string(凡是用双引号或单引号引起来的都是字符串)  var name='青年队'
  - 布尔数据类型 Boolean  只有2个值，true/false  实际运算中true=1,false=0  默认男true,女false
  - undefind 变量未初始化(定义了变量，但没给变量赋值)  
  >  var name2;  console.log(name2); 输出undefind
  - Null 变量未引用 值为空  console.log(null); 输出null

##复杂数据类型
 + object对象
  - var xiaoming ={
  "name":"xiaoming","age":20}  ;console.log(xiaoming);  Object{name:"xiaoming", age:20}
 +array数组
  - var ages=[20,21,22,23,24]; console.log(ages); [20,21,22,23,24]；

##判断数据类型 
 + typeof
  - var name="zhangsan"; conlose.log(typeof name);
     输出为string字符串
  - var age=20; conlose.log(typeof age);
     输出为Number数字类型

##比较运算符
  - < 
  - >
  - <=
  - >=
  - ==
  - !=
 + 一个=为赋值运算符，==为比较运算符
  - 对比不能写1=1(程序易出错)
  - >=和<=中间不能有空格

##算术运算符
 + 加号
  - 两数字类型的变量相加，得到的是一个数字类型 1+1;2
  - 一个数字类型和一个字符串相加，得到的是一个字符串(拼接)  1+'asd'; '1asd'
 + 减号
  - 两个号数字类型的变量相减，得到一个数字类型 10-1; 9
  - 一个数字类型和一个一个数字字符串相减，得到的是数字类型(数据类型隐式转换) 10-'1'; 9
  - 一个数字类型和一个非数字字符串相减，得到NaN，为数字类型 10-'你好'; NaN( not a number)
 + /除号
  - 两个数字类型的变量相除，得到数字类型
  - 一个数字类型和一个字符串类型相除，得到数字类型
  - 一个数字类型和一个非数字字符串相除，得到NaN，为数字类型
  - 0为除数时，得到结果 Infinity(无限大),为数字类型
 + %取余数
  - 10/2  5
  - 10/'2' 5
  - 10/'你是' NaN
  - 10/0 Infinity
  - 优先级，有()先算()里的

##带操作的赋值运算
    var age=10 ;   var age=20;
    var a =10; a=a+5; ===>var a=10; a+=5; 在a的基础上+5，并把值赋给a。

 