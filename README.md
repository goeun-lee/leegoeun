<!DOCTYPE html>
<html lang="ko">
 <head>
  <meta charset="utf-8" />
  <title> popup </title>


</head>

 <body>
	<h2>모달팝업 VS 팝업창</h2>
	<p>
		1) 모달팝업 : 주소줄이 없고, 사용자가 직접 창을 만들어서 사용하는 기능<br/>
		2) 팝업창 : 주소줄이 있고, window창이 뜨는 형태<br/>
	</p>
	<h2>window_open1</h2>
	<a href="http://www.naver.com" title="네이버" onclick="windowOpen1(); return false;">네이버로 이동</a>
	<script>
		function windowOpen1(){
			/* 
				기본 사용방법 : window.open(url, name, spec) 
				spec은 창의 크기나, 창의 위치

				+ 스타일 영역이 아닐 경우, 단위제외
				+ name부분에 글자 대신 _blank를 설정하면 새 창으로 계속 열림
			*/

			window.open("http://www.naver.com", "네이버", "width=250, height=250");

			alert(1);
		};
	</script>
	<!-- 위와 같은 방법으로 구글로 넘기기 -->
	<a href="#none" title="구글" onclick="windowOpen2();">구글로 이동</a>
	<script>
		function windowOpen2(){
			window.open("http://www.google.com", "_blank","width=250,  height=250");
		}
	</script>
	<!-- 위와 같은 방법으로 다음 연결하기 -->
	<a href="#none" title="다음" onclick="windowOpen3();">다음으로 이동</a>
	<script>
		function windowOpen3(){
			window.open("http://daum.net","_blank","width=250, height=250, left=100, top=100");
		}
	</script>
 </body>
</html>
