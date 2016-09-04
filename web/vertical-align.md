- vertical align을 하고 싶지만, container안에서 content vertical을 아직 제대로 제공하지 못함
 그래서, 비슷하게 만들 수 있는 방법들이 몇 가지 있어, 정리함 
 
1. Absolute positioning
  - position property를 이용함 
  - container div안에 content div가 들어가도록 함 
  - 이 때, container position : relative; content position: absolute;
  - 여기서 자식 div에 margin-top: -1.5em;을 하여, container height에서 절반을 top으로부터 움직일 수 있다
 
  ```div
  .container{
   position: relative; 
   margin: auto;
   }
   
   .content{
   position: absolute;
   margin-top: -1.5em;
   }
   ```
2. CSS3 Transform 
  - 자식 element에 top 50%을 하면 중간에 오지 않는 경우, transform을 사용한다.
  - 단, transform은 IE8 이하 버전에서는 적용 불가능하다.
  ```
  .content{
  position: relative;
	top: 50%;
	-webkit-transform: translateY(-50%);
	-o-transform: translateY(-50%);
	transform: translateY(-50%);
	}
	```
	
	3. Use padding
	- padding을 사용하여, 중간에 있는 것처럼 만들 수 있다.
	- top과 bottom에 padding을 똑같이 주고 조정하는 것이다.
	
	4. Line Height 사용용
	- content가 한줄의 텍스트인 경우 사용할 수 있는 방법으로 text를 중앙정렬할때 line-height를 사용
	- 텍스트를 중심에 두고 height를 결정하는 방법
	- 단점은 텍스트가 여러줄인 경우, 줄 간격이 넓어질 수 있음음
	
	5. CSS Table 사용
	- IE8과 같이 구버전에서 사용가능한 방법으로 display를 table로 설정한 방법이다 
	```
	.container{
	display : table;
	}
	
	.content{
	display: table-cell;
	}
	
	6. --Flex Box-- 사용용
	- CSS3에서 새로이 나온 개념(IE 10, safari 6, chrom 27 사용 가능)
	- 이전과 달리 텍스트가 content로 자식 관계가 아닌 <p>태그 사용
	```
	.container{
	display: flex;
	align-items: center;
	}
