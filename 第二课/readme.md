# 课堂作业
作业要求
花20~30分钟时间，
练习 JQuery 深入部分的内容，并保存练习代码，提交；
对“一个在线CAT工具系统”进行初步需求分析。下节课以小组形式进行汇报。

JQuery HTML练习
- text() - 设置或返回所选元素的文本内容
- html() - 设置或返回所选元素的内容（包括 HTML 标记）
- val() - 设置或返回# 表单字段的值
- attr() - 方法用于获取属性值。
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
# 添加元素
```
append() - 在被选元素的结尾插入内容----------------尾部插入--$("p").append("追加文本");
prepend() - 在被选元素的开头插入内容--------开头插入--$("p").prepend("在开头追加文本");
after() - 在被选元素之后插入内容---具体在哪个元素后插入$("img").after("在后面添加文本");
before() - 在被选元素之前插入内容---------------------$("img").after("在后面添加文本");
后两个可以插入多个元素：
function afterText()
{
    var txt1="<b>I </b>";                    // 使用 HTML 创建元素
    var txt2=$("<i></i>").text("love ");     // 使用 jQuery 创建元素
    var txt3=document.createElement("big");  // 使用 DOM 创建元素
    txt3.innerHTML="jQuery!";
    $("img").after(txt1,txt2,txt3);          // 在图片后添加文本
}

```
## 测试代码
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
<script src="https://cdn.staticfile.org/jquery/1.10.2/jquery.min.js">
</script>
<script>
$(document).ready(function(){
	$("#btn1").click(function(){
		$("#p0").prepend("<b>用prepend在开头追加文本</b>。 ");
	});
	$("#btn4").click(function(){
		$("#p1").append("<b>用append在结尾追加文本</b>。 ");
	});
	$("#btn2").click(function(){
		$("ol").prepend("<li>用prepend在开头添加列表项</li>");
	});
	$("#btn3").click(function(){
		$("ol").append("<li>用prepend在开头添加列表项</li>");
	});
	$("#btn5").click(function(){
		$("#p2 b").before("<b>成功</b> ");
	});
	$("#btn6").click(function(){
		$("#p3 b").after("<b>成功</b> ");
	});
	$("#btn7").click(function(){
		$("ol li#l2").after("<b>成功</b>");
	});
	$("#btn8").click(function(){
		$("ol li#l2").before("<b>成功</b>。 ");
	});
});
</script>
</head>
<body>
	
<p id="p0">这是测试prepend的段落。</p>
<p id="p1">这是测试append的段落。</p>
<p id="p2">这是测试<b>before</b>的段落。点击按钮before前会出现“成功”字样</p>
<p id="p3">这是测试<b>after</b>的段落。点击按钮after后会出现“成功”字样</p>
<ol>
<li id="l1">列表 1</li>
<li id="l2">列表 2</li>
<li>列表 3</li>
</ol>
<button id="btn1">prepend添加文本</button>
<button id="btn4">append添加文本</button>
<button id="btn2">prepend添加列表项</button>
<button id="btn3">append添加列表项</button>
<button id="btn5">after</button>
<button id="btn6">before</button>
<button id="btn7">after添加列表项</button>
<button id="btn8">before添加列表项</button>
	
</body>
</html>


```


# 课后作业
作业要求
练习使用bootstrap框架设计编写自己的在线CAT系统的宣传首页（不作为最终成果,仅练习，下周检查）
根据自己小组归纳的一个完善的CAT工具的功能列表，设计本小组的在线CAT系统的需求，形成文档。
