


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

<code>
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
</code>



3. 라디오 버튼 답변에 대한 alert window로 출력 
<div>
 시선을 주로 주었다고 생각하는 지점은?:
<form>
<label><input type = "radio" name = "survey" value ="위" > 위 </label>
 <label><input type = "radio" name = "survey" value ="아래" > 아래</label>
 <label> <input type = "radio" name = "survey" value ="중간"> 중간</label>
 <input id = "btn" type ="button" value ="확인"/>
</form>
</div>

<script>
document.addEventListener('DOMContentLoaded', function(){
  var getRadioValue = function(name) {
  var result ='';
  var elems = document.getElementsByName(name);

  for(var i =0, len =elems.length; i < len; i++){
   var elem = elems.item(i)
      if (elem.checked) {
          result = elem.value;
      break;
   }
  }
   return result;
  };

 document.getElementById('btn').addEventListener('click', function(){
  window.alert(getRadioValue('survey'));
 },false);
},false);
</script>
