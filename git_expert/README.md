# Git 자유자재로 활용하기
<br>

### git reset을 하고 나서 돌아오려면?
- git reflog
	- HEAD가 가르켜온 커밋들을 알려줌
<br>

### 커밋 히스토리를 보는 다양한 방법
- --all 
	- 현재 브랜치만이 아닌 모든 브랜치의 히스토리를 보여줌
- --graph
	- 커밋 히스토리가 각 브랜치와의 관계가 잘 드러나도록   그래프 형식으로 출력
<br>

### Git을 GUL환경에서 사용할 수 있게 해주는 프로그램
- sourcetree, GitKraken
<br>

### 깔끔한 커밋 히스토리를 원할 땐 git merge 대신 git rebase
- git rebase [커밋 아이디]
	- 커밋의 베이스를 재배치함
	1. git add .
	2. git rebase --continue
<br>

## 작업 내용 임시 저장하기
- git stash
	- 최근 커밋 이후 작업 내용은 모두 스택에 옮겨지고 working directory 내부는 다시 최근 커밋의 상태로 초기화
- git stash list
	- 저장이 잘 되었는지 조회
- git stash apply
	- 스택에 있는 내용을 다시 워킹 디렉토리로 가져와서 적용
<br>

## 잘못된 브랜치에서 작업하고 있었다면?
1. git stash
2. 올바른 브랜치로 이동
3. git stash apply [업내용의 ID]
4. conflict 해결
5. commit
- git stash drop [ID]
	- 필요없는 스택 지우기
- **git stash pop [작업 내용의 ID]**
	- 작업 내용을 적용하며 스택에서 제거
<br>

## 필요한 커밋만 가져오는 git cherry-pick
- git cherry-pick [커밋 아이디]
	- 자신이 원하는 브랜치에 들어있는 커밋들만 가져와서 현재 브랜치에 추가
<br>

## 여러 커밋을 하나의 커밋으로 만들기
1. git reset --soft / --mixed
2. 그 상태로 커밋
