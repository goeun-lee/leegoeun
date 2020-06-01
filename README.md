<!DOCTYPE html>
<html lang="ko">
 <head>
  <meta charset="utf-8" />
  <title> template5 </title>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<style>
	*{margin:0; padding:0;}
	li{list-style:none;}
	body{background-color:#333;}

	h2{text-align:center; padding:50px 0; text-transform:uppercase; font-size:26px; color:#aa0;}

	div{width:1200px; height:450px; margin:50px auto 0; outline:5px solid #1a1d43; overflow:hidden; position:relative;}

	ul{width:100%;}
	ul li{
		width:300px; height:450px; background-color:rgba(250,0,0,1); position:absolute; left:0; top:0; outline:1px solid #1a1d43; background-size:100% 100%; transition:all .7s ease .2s;
		/* jQuery의 mouseover 와 연결되어 있음 */
	}

	.w0{background-image:url("img/joker.jpg"); z-index:3;}
	.w1{background-image:url("img/harleyQuinn.jpg"); z-index:2;}
	.w2{background-image:url("img/deadshot.jpg"); z-index:1;}
	.w3 img{
		width:100%; height:100%; transition:all 0.7s ease 0.2s;
		/* jQuery의 퍼지는 효과와 연결*/
	}

</style>
<script>
	$(function(){
		/*
			중요 ) offset().top,	offset().left의 경우
			부모요소에 상속받는 거리만큼 움직이기 때문에 문제가 발생함!

			offset().top	and     offset().left의 경우 브라우저를 따라다니도록
			설정해주어야 함!
		*/
		
		$(".w0").mouseover(function(){
			$("h2").text("joker");
			$(".w1").css({"left":$(this).width()});
		});
		$(".w1").mouseover(function(){
			$("h2").text("harleyQuinn");
			$(".w2").css({"left":$(this).width()*2});
		});
		$(".w2").mouseover(function(){
			$("h2").text("deadshot");
			$(".w3").css({"left":$(this).width()*3});
		});

		$(".w3 img").mouseover(function(){
			$("h2").text("diablo");
			$("div").css({"overflow":"visible"});
			$(this).css({"transform":"scale(1.5)","opacity":"0"});
			$(this).parent().css({"backgroundImage":"url('img/diablo.jpg')"});
		});
	});
</script>
</head>

 <body>
	<h2>image diablo</h2>
	<div>
		<ul>
			<li class="w0"></li>
			<li class="w1"></li>
			<li class="w2"></li>
			<li class="w2"></li>
			<li class="w3">
				<img src="img/diablo.jpg" alt="디아블로 이미지"/>
			</li>
		</ul>
	</div>
 </body>
</html>
