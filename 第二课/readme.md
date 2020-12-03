# 课堂作业
作业要求
花20~30分钟时间，
练习 JQuery 深入部分的内容，并保存练习代码，提交；
对“一个在线CAT工具系统”进行初步需求分析。下节课以小组形式进行汇报。

JQuery HTML练习
text() - 设置或返回所选元素的文本内容
html() - 设置或返回所选元素的内容（包括 HTML 标记）
val() - 设置或返回# 表单字段的值
attr() - 方法用于获取属性值。
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<script src="https://cdn.staticfile.org/jquery/1.10.2/jquery.min.js">
</script>
<script>
$(document).ready(function(){
  $("#btn1").click(function(){
    alert("Text: " + $("#test").text());
  });
  $("#btn2").click(function(){
    alert("HTML: " + $("#test").html());
  });
  $("#btn3").click(function(){
    alert("Val: " + $("#test2").val());
  });
   $("#btn4").click(function(){
    alert($("#runoob").attr("href"));
  });
});
</script>
</head>

<body>
<p><a href="https://www.baidu.com/" id="runoob">jQuery测试attribute</a></p>
<p>名称: <input type="text" id="test2" value="JQuery测试"></p>
<p id="test">这是段落中的 <b>粗体</b> 文本。</p>
<button id="btn1">显示文本</button>
<button id="btn2">显示 HTML</button>
<button id="btn3">显示Val </button>
<button id="btn4">显示属性 </button>
</body>
</html>
```

# 课后作业
作业要求
练习使用bootstrap框架设计编写自己的在线CAT系统的宣传首页（不作为最终成果,仅练习，下周检查）
根据自己小组归纳的一个完善的CAT工具的功能列表，设计本小组的在线CAT系统的需求，形成文档。
