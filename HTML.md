#HTML

##表单  form开头  属性有action提交的地址/method-get/post提交类型             
##<form   action="网址"  method="get（默认，没有敏感信息）或者post（包含敏感信息用，更安全）"  >
包含下列各种。。。。                      
##</form>
+ input包括   text 普通文本框                               
- password 密码输入框                格式：<input type=""    name="起的任意名字">
- submit提交按钮                   
- checked默认选中（参考单选框、多选框）
- reset         重置按钮                   
- fieldset表单项进行分组（给内容加一个框） legend制定每组名字
- radio        单选框（其name属性必须相同）  
- <fieldset>内容 <legend>内容</legend>内容 </fieldset>
- checkbox  多选框                                                     
+ 下拉列表式用select开头   option为内容
- 格式：<select>
-<option  value=“对应数据代码词典”>内容</option>
- <option>内容</option>
- <option>内容</option> strong加粗
- <option>内容</option>
+ </select>
- 多行输入框用textarea开头   cols可理解为宽  rows为高  具体为一个可输入多行文字的文本框
- 格式：<textarea name="随便起"  cols=""  rows="">
- target="_self/_blank"点击在原有页面跳转/新页面跳转
##表格  
+ table创建          
1.包含border(边)    width(宽)     height（高）cellspacing（单元格间距） 
2.cellpadding(单元格边距)       align(left左  center中  right右)    bgcolor（颜色） border-collapse:collapse(合并边框)
+ 格式：<table  border=""  width=""  height="" cellspacing=""  cellpadding=""   align="左中右" bgcolor=""颜色   ></table>                                           
1.tr行    可包含th td
2.th表头
3.td单元格                rolspan 横合并/rowspan竖合并-------合并单元格
