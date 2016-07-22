Git을 사용하는 데에는 Mac OS과 Windows 환경 모두 작업이 가능하다. 
다만, enter의 기능이 달라 문제가 생기는데, Windows는 line ending으로 CR(Carriage-Return,\r)과 LF(Line feed, \n)을 사용 
Mac OS 혹은 Unix는 LF만을 사용함 

-> 이는 enter차이로 수정 사항이 없음에도 수정된 코드가 있다고 인식하여 commit과정에서 문제가 발생하며, merge마다 발생 가능함.

#1 autocrlf 사용 :처리 설정
- Window 
** git config --global core.autocrlf true

-Mac OS 
** git config -- global core.autocrlf input
