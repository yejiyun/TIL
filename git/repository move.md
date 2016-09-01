#Repository에서 다시 repository로 코드를 이관하고 싶을 때 사용 하는 방법

1. git remote add new_repo_name new_repo_url //To add the new repo location(새 repo 생성)
2. git push new_repo_name master // push the content to the new location
3. git remote rm origin // Remove previous one(이전 repo 삭제) 

- 위 방법을 실행하는 도중에 발생한 에러 
![rejected] master -> master <fetch first> 
error: failed to push some refs to '.....git'

- 에러 발생 원인 : 새로운 repo 형성 시, 생성되는 readme.md 파일은 기존의 commit에 포함되어 있지 않았기 때문에, 
local repo는 이를 인지하지 못해 fetch를 요청함. 

#1. git pull을 통해 다시 change를 merge하는 방법
 git pull 
 git push -u origin master
 
#2. git push -f origin master   (-f = force)
  강제로 진행하는 방법은 위와 같다. 
  
  
Ref : http://stackoverflow.com/questions/1484648/how-to-migrate-git-repository-from-one-server-to-a-new-one
