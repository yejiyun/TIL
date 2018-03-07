


1.클릭 시, 다른 페이지 로드 
<html>
	<head></head>
	<body>
	<input type ="button" value ="확인" onclick = "btn_click()"/>

	<script type="text/javascript">
	function btn_click(){
		location.href = "http://www.naver.com";
	}
	</script>
	</body>
	
</html>

2. 참가자 번호 입력과 console에 찍힘 
<html>
<form>
 <label for ="participant"> 참가자 번호: </label>
 <input id = "participant" participant ="participant" type ="text" size ="30"/>
 <input id = "btn" type ="button" value ="확인"/>
</form>
<div id = "startpoint"></div>


<script type="text/javascript">
document.addEventListener('DOMContentLoaded', function(){
 document.getElementById('btn').addEventListener('click', function(){
 var participant = document.getElementById('participant');
 console.log(participant.value);
 },false);
},false);
</script>

</html>
