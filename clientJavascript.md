
1.getElementsByTagName 
<code>
<html>
	<head></head>
	<body>
		<title>hello</title>
	<ul> 
	<li><a href = "Javascript:window.alert('hello');"> 링크 테스트 </a></li>
	<li><a href = "http://www.naver.com">naver</a><li>
	</ul>

	<script type="text/javascript">
	var list = document.getElementsByTagName('a');
	for (var i = 0, len = list.length; i < len; i++){
		console.log(list.item(i).href);
	}
	</script>
	</body>
	
</html>
</code>


2. getElementsName
<code>
	<form>
	<label for = "time"> 시간 : </label>
	<input id = "time" name = "time" type ="text"/>
	</form>


	<script type="text/javascript">
	var current = new Date();
	var nam = document.getElementsByName('time');
	nam[0].value = current.toLocaleTimeString();
	</script>
  </code>



3. innerHTML
<html>
	<head></head>
	<body>
	<div id = "result_text">
	<p style ="color: Blue;"> 설정됨</p>
	</div>
	<div id = "result_html">
	<p style = "color: Red;"> 설정안됨</p>
	</div>

	<script type="text/javascript">
	document.addEventListener('DOMContentLoaded', function(){
		document.getElementById('result_text').textContent =
		'<a href = "http://www.naver.com">네이버 </a>';
		document.getElementById('result_html').innerHTML =
		'<a href = "http://kakao.com"> 카카오 </a>';
	},false);

	</script>
	</body>
	
</html>
