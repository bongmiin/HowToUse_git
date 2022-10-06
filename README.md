## 깃을 사용하는 법을 정리한 폴더

### GIT COMMIT

1. 비어있는 레포지토리 생성
- git init 
 
2. git에게 누군지 알려주기 
- git config user.name "이름"
- git config user.email "이메일"
3.  커밋할 파일 지정하기
- git add calculator.py
4. 커밋하기
- git commit -m "커밋 메세지"

### Git의 세가지 작업 영역

1. working directory
- 작업을 하는 프로젝트 디렉토리
2. staging area
- git add를 한 파일들이 존재하는 영역
3. repository
- working directory의 변경 이력들이 저장되 있는 영역
	- 커밋들이 저장되어 있는 영역


### Git이 보는 파일의 4가지 상태
1. Untracked
- git에 의해 변동사항이 추적되고 있지 않는 상태
2. Tracked
	1. staged
	- 파일의 내용이 수정되고 나서 staging area에 올라와있는 상태
	2. Unmodified
	- 현재 파일의 내용이 최신 커밋과 비교했을 때 전혀 바뀐 게 없는 상태
	3. Modified
	- 최신 커밋과 비교했을 때 조금이라도 바뀐 내용이 있는 상태

### 다양한 Git 명령어

- git reset
	- git add 취소

- git help [알고싶은 커멘드 이름]

- git push
	- 로컬 ------> 리포트

- git pull
	- 로컬 <------ 리포트

- git clone [주소]
	- 다른 사람의 프로젝트를 가져오는 명령어

- git log 
	- 커밋 히스토리 살펴보기      
	
- git log --pretty=oneline
	- 깔끔하게 보기 
                                