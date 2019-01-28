##对象和Json
 + 对象的表示方法
 <!--  -->
    var name= '张';
    st = {
       name: '稍等',
       age: 20,
       say：function(){
           console.log(name+'说话，我今年'+this.age+'岁')；
       }
    }
 + Json
   + 是一种轻量级的数据交换格式
 + Json语法规则
   + 字符串、数组、对象、数字等支持的类型都可用Json表示
     + 对象表示为键值对(键值对中的键名写在前面并用双引号包裹，且使用冒号分割  "age":20 
     )
     + 数据由逗号分隔
     + 花括号保存对象
     + 方括号保持数组
 + JSON和JS对象
   + JSON是JS对象的字符串表示法，它使用文本表示一个JS对象的信息。其本质是一个字符串
   <!--  -->
        对象  var user = {name:'zhangsan',age:20 }
        json  var user = '{"name":"zhangsan","age":20}'
    + json和js对象的相互转化
      + 从对象转化为字符串，JSON.stringify()
      <!--  -->
          var json =JSON.stringify({name:'zhangsan',age:20});
      + JSON转化为对象，JSON。parse()
      <!--  -->
          var user = JSON.parse('{"name":"zhangsan","age":20}');
##数组高级API
 + Array的内置方法
   + toString() 把数组转换为字符串
   + reverse()翻转数组
   + sort()数组排序，返回排序后的数组
     + 无参：按照数组元素的首字符队友的Unicode编码值从小到大排列数组
     + 带参:必须为函数。函数中的两个形参如计算后(a-b)，返回值为负数，a在b前面；返回值为正数，b在a前面
   + slice()从当前数组中截取一个新的数组，不影响原来的数组，参数start从0开始，end从1开始
   + splice()删除或替换当前数组的某些项目
 + 清空数组
   + array.length= 0；length可以赋值
   + array=[]; 推荐使用
##字符串对象的常用方法
 + 常用方法
   + charAt()获取相应位置字符
     <!--  -->
         var str = 'how are you ,and you?';
         var char =str.charAt(5);
         alert(char);
    + charCodeAt()可返回指定位置的字符的编码
    + indexOf返回字符在字符串中的位置
    + concat()连接字符串
    <!--  -->
         var a='hellow';
         var b='world';
         console.log(a.concat(b));
    + slice()可提取字符串的某个部分，并以新字符串返回被提取部分
    + substr(起始位置，[取的个数])用的很多
    <!--  -->
         var str = 'abcdefaasdfsdfas';
         var str2 = str.substr(0,str.length-1);
		 console.log(str2);
    + toUpperCase()字符串大写
    + toLowerCase()字符串小写
    + 保留小数位数 Math.fixed();

