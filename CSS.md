#CSS
   
###元素选择器
        {}
###类选择器，根据元素的class属性值选取元素
       .xx{}
###ID选择器，根据元素的id属性值选取元素（id唯一）
       #id{}
###交集选择器，可同时使用多个选择器，可以同时满足多个选择器的元素
      x  x  x{}
###并集选择器同时使用多个选择器,多个选择器将被同时应用指定的样式（用逗号隔开）
       x,x,x{}
###后代选择器，根据标签关系，为处在元素内部的代元素设置样式
       祖先元素  后代元素  后代元素 {}
###通用选择器，可同时选中页面中的所以元素
       *{}吧       

     继承性
         文字的颜色、大小、字体、行高及所有和文字有关的属性都可继承
     特殊性
        <a href="#"></a>  不能继承父元素重点文字颜色
        <h1></h1>  标题标签不能继承父元素中的文字大小
    选择器优先级
        内联样式>ID选择器>类、属性、伪类选择器>元素选择器>通配符
       优先级特点:继承的优先级为0   可叠加
    CSS单位
      px  百分比   em
    CSS常见属性
       width宽   height高    color文本颜色  background-color背景颜色    Text-align(left  center  right)内容的水平对齐方式    
      Text-indent首行缩进    Text-indent:2px;    font-family字体      font-style:Italic斜体/normal正常
       Line-heigt 行高 单位px/倍数/百分比
    CSS背景图片
       background-color背景颜色          background-imge背景图片 url( )       background-repeat平铺方式 repeat | no-repeat
       background-position图片位置 left  right  top  bottom center      background-attachment背景滚动  scroll  fixed
       backhground-size 规定背景图片的尺寸  length设置背景图片的高度宽度  
       background-position属性设置背景图像的起始位置      
       cursor: pointer 鼠标变成小手   pointer |   move |    help  |   default
       outline:none 去掉input输入框获取焦点默认边框
       border:none 去掉默认边框
    盒子模型
       分为： 内容区content     内边距padding     边框border   外边距margin
       
如果没有设置内边距和边框，内容大小和盒子大小一致
       width和height可设置内容区大小 ，但只适用块元素
      
        内容区：指盒子中存放内容的区域

        内边距：内边距指内容区与边框直接的距离（影响盒子宽度）      受border影响宽度
    
        边框：可在元素周围创建边框，是元素可见框的最外部          border:1px solid red  边框宽度  样式  颜色    
             none无边框
             dotted点线
             dashed虚线
             solid实线
             double双线  
        外边距：边框与外围元素的空间
            垂直叠加（重叠） 当两个div垂直局部时，marign没有发生累加，对比marign-bottom和marign-top的值
      
            嵌套情况（坍塌） div发生嵌套时，里面div中的marign-top影响外部div
            解决方法：1.overflow:hidden     2.padding     3.float
        
        display: block设置为块元素
                     inline设置为行内元素
                     inline-block设置为行内块元素
                     none 隐藏元素
            根据标签的表现形式,把标签分类 
		1. 块状标签 
			a) 独占一行
			b) 宽高有效
			比如:  div  p  br hr  table  tr  h1~h6   form   ul  ol dl dd dt
		2. 行内块标签
			a) 可以在同一行展示
			b) 宽高有效
			比如: img th  td  input select  textarea
		3. 行内标签
			a) 可以在同一行展示
			b) 宽高无效
			比如: a  span i  em  strong  sup  sub   del等所有的字体标签 
            visibility元素是否可见    隐藏后位置存在，不会被占用
                   visible可见
                   hidden隐藏      
            overflow标签中内容超出样式的宽高后
                   visble默认值
                   scroll添加滚动条
                   auto根据需要添加滚动条
                   hidden隐藏超出盒子的内容  

        文档：文档中块元素独占一行
                            行内元素在一行上显示，如果排不下就换行
                            自上而下

         浮动：使元素脱离原来的文本流，在父元素中浮动起来
              float:  none不浮动                             块级元素和行内元素可浮动
                        left向左浮动                             块级元素浮动后，宽度会被内容撑开，所以需要为其制定一个宽度
                        right向右浮动                          元素浮动后，下方元素会上移，元素中的内容会环绕在元素周围
                                                                       元素浮动后，会一直向上浮动，直到遇到父元素的边界或其他浮动元素
         清除浮动
               clear: left忽略左侧浮动    
                        right忽略右侧浮动
                        both忽略全部浮动
                        none不忽略浮动，默认值

        定位
            position可以把一个元素放置在网页中的任何位置
                position: staic
                               relative     相对定位（元素在当前文档中的自然位置。相对于这个位置进行的移动就叫相对定位）
                               absolute   绝对定位（元素相对于HTML或其他最近的祖先元素来定位，定位后行内元素变为块元素    同时为其父元素定位相对定位，根据相对定位绝对）
                               fixed         固定定位  (将元素固定在某个位置，使其任何时候保持不变   可使得行内变为行内块 )
               z-index:开启定位后可以设置该属性
               z-index可指定一个整数作为参数，值越大优先级越高，z-index较大的元素会显示在网页的最上层