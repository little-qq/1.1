# 1.1
@@ -0,0 +1,113 @@
<!doctype html>
<html>
<head>
<meta charset="utf-8">
<title>逐次显示内容的动效</title>
<style>
*{ padding:0; margin:0}
.header{ height:77px;background-position: center;}
.banner{ height:280px;background-position: center;}
.about{ height:400px; background:#FFFFFF; text-align:center; width:100%; overflow:hidden; padding-bottom: 20px;}
/*.about h1{ padding:60px 0 40px; position:relative; left:-100%; transition:0.5s}
.about p{ padding:0 150px; position:relative; right:-100%; transition:0.5s 0.5s;}
.about.on h1{ left:0;}
.about.on p{ right:0;}
*/
.about h1{ padding:100px 0 30px 0; position:relative; top:350px; font-size: 24px; transition:0.5s}
.about p{ padding:0 200px; position:relative;   top:350px;    line-height: 1.8; font-size: 14px; transition:0.5s 0.5s;}
.about.on h1{ top:0;  }
.about.on p{  top:0}
.news{ height:535px; background:#e0e0e0; margin:0 auto; overflow:hidden;}
.news .left{ width:346px; height:375px;  float:left; position:relative; margin-top: 80px; left:-346px; transition:0.5s;}
.news .right{ width:611px; height:375px; float:right; position:relative; margin-top: 80px;  right:-611px;transition:0.5s;}
.news.on .left{ left:calc(50% - 503px);}
.news.on .right{ right:calc(50% - 503px);;}
.footer{ height:293px; background:#999; background-position: center;}
</style>
<script src="js/jquery.min.js"></script>
<script>
$(function(){
	var newsTop=$(".news").offset().top;
	var abTop=$(".about").offset().top;
	var winH=$(window).height()*0.7;
		$(window).scroll(function(){
		var st=$(this).scrollTop();
		if(st>=newsTop-winH){
			$(".news").addClass("on")	
		}
		if(st>=abTop-winH){
			$(".about").addClass("on")	
		}
		})	
	})
</script>
</head>
<body>
<div class="header" style="background-image:url(images/9.jpg);">
	</div>
 <div class="banner" style="background-image:url(images/32.jpg);">
</div>
<div class="about" >
	<h1>高效率自学平台<br/></h1>
    <p>人生与梦想，是在现实生活中不能脱离的话题。<br/>
在人生的道路上，有人在青春年少时才华横溢，实现自己闪亮的梦想，<br/>
有人则在这一路上跌跌撞撞，迷茫不知所措，<br/>
但无论是哪一种，任何人都无法下定义这是对或者错，<br/>
而改变自己，奋起直追才是最为关键的。<br/>
在如今就业环境复杂，工作也不是能够轻易就如人意的情况下，<br/>
要怎样去做一些改变，才能让自己的青春与梦想不荒废呢？
</p>
</div>
<div class="news">
<div class="left" style="background-image: url(images/36.png);"></div>
    <div class="right"  style="background-image: url(images/37.jpg)"></div>
</div>
<div class="footer" style="background-image:url(images/8.jpg);"></div>
</body>
</html>
