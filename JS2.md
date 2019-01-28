#JS基础第二部分

##Date和Math对象使用
+ Date用法                 // Date  日期对象 用于获取年月日时分秒
		                  // new是面向对象才能解释的东西,这里就记下来.
 - Date() 返回当前时间日期   var date= new Date();
 - getDate() 返回一个月中的某一天
 - getMonth() 返回月份(以数组形式存储，返回0到11)  var mon = date.getMonth()+1;
 - getFullYear() 返回年
 - getHours() 返回小时部分  var hou =date.getHours();
 - getMinutes() 返回分钟部分
 - getSeconds() 返回秒数
 - getDay() 返回一周中的某一天(返回值为0周日到6周六之间的一个整数)
 - document.write(year+'年'+month+'月'+day+'日 '+hour+':'+min+':'+sec);

 + Math对象
  - Math.ceil()天花板函数  console.log(Math.ceil(1.1)); 为2
    返回一个数字的整数部分，对其进行向上舍人。
  - Math.floor() 地板函数
    返回一个数字的整数部分，对其进行向下舍人。 
  - Math.max(x,y) 返回x,y之间的最大值  console.log(Math.max(2,3)); 为3
  - Math.min(x,y) 返回x,y之间的最小值
  - Math.random() 伪随机   //  任意区间 比如  15-31?     *个数+最小值
 	console.log('15-31之间随机值: ',Math.floor(Math.random()*17+15));
    Math.floor(Math.random()*数量+min) 任意范围内的随机数
  - Math.pow(x,y)  Math.pow(3,3)  3的三次方为27
    返回x的值的y次方   10/0为Infinity(无限大)
  - Math.round(x)四舍五入求整数(容易出错，不推荐使用)

##关系运算符
  + 隐式转换
   - 1+'123'='1123' 数字转换为字符串
   - 10-'2'=8  字符串转换为数字
   - Js为弱类型语言，执行时出错将停止进行
   - 声明变量，因变量为容器
   - >  <   >=   <= ==  ===全等于  !=不等于 !==不全等于
   -console.log(5>6) 关系运算符结果都为布尔值 ，true/false
   - JS中=只有表示赋值这一个意思，判断两个东西是否相等用==

##逻辑运算符
 + &&与   ||或  ！非
  - &&与  console.log(3>5 && 2>1); // false  两个都为真，结果才是真
  - ||或  console.log(3>2 || 1>2); // true   两个有一个为真，结果为真
  - ！ 取反

 + 连比
  - 中间用&&连接 console.log(3<2&&2<4);

##if语句
 + if语句初步认识
  - if为"如果"意思，else为"否则"^[footnote text]
  -if(不下雨){
      出去玩；
   }else{
     不出去;
   }
> Blockquote
> 用户输入年龄，判断是否在18-70岁，如果在，弹出对话框，否则弹出失败对话框。
>  < script>
>    var age = prompt('请输入年龄');
>      if(age>=18&&age<=70){
>        alert('恭喜，可以考驾照')；
>      } else{
>        alert('年龄不符合要求‘)；
>       }
>  </script>

+ 多分支if语句和跳楼现象
  -  if( 条件表达式1){
  -     条件1为真时...
  -  } else if（条件表达式2）{
  -    条件1不满足，条件2满足时...
  -  } else if(条件表达式3) {
  -    条件1、2不满足，条件3满足时...
  -  } else{
  -     全都不满足时....
  -  }

+ if语句的嵌套    
  -  var sd= prompt();
  -  var add = prompt();
  -  if( 条件1){
  -    if(shang>=20){
  -    var pri =shang*数值；
     } else {
       var pri =shang*数值； }
  -  }  else if(条件2){
  -    if(shang>=30){
  -      var pri =shang*数值；
    } else{
      var pri=shang*数值；
     }
    } else{
      alert('.......')
      } 