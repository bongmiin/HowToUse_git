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

### 커밋 히스토리 살펴보기

- git log 
	- 커밋 히스토리 살펴보기      
	
- git log --pretty=oneline
	- 깔끔하게 보기 

- git show [커밋의 아이디 앞 4자]
	- 커밋 히스토리 보기

### -m 옵션 없이 커밋 메세지 남기기

1. git commit
2. i를 눌러 입력 모드 진입
3. commit 메세지 자세히 작성
4. esc :wq 를 통해 저장
   *복잡하고 긴 커밋 메세지를 쉽게 남길 수 있다.*

### 최신 커밋 수정하기

1. git add .
2. git commit *--amend*
 - 최신 커밋을 수정하는 커맨드
 [Git에서 권장하는 커밋 메세지 작성 가이드라인](https://git-scm.com/docs/git-commit#_discussion)

### 긴 커맨드에 alias 설정하기

1. git config alias.[커맨드 줄임말] ['git을 제외한 원래의 커맨드']

### 두 커밋 간의 차이 보기

1. git diff [이전 커밋 아이디] [이후 커밋 아이디]

### HEAD의 의미
- 보통 가장 최근에 한 커밋 하나를 가리킴
- HEAD가 가리키는 커밋의 내용대로 워킹 디렉토리가 구성된다.

### 이전 커밋으로 git reset하기
- git reset --hard [가고싶은 커밋의 아이디] 로 HEAD가 이전 커밋을 가리키게 함
  *권장하지 않음*

- git reset --mixed [가고싶은 커밋의 아이디] 워킹 디렉토리 제외

- git reset --mixed [가고싶은 커밋의 아이디] 레포지토리만 리셋

### HEAD를 기준으로 git reset하기

- git reset --hard HEAD^
	- 현재 커밋의 바로 이전 커밋

- git reset --hard HEAD\~x
	- 현재 가리키는 커밋보다 *x단계 전에 있는 커밋*

### 커밋에 tag달기
- git tag [태그 이름][커밋 아이디]
	- 커밋에 tag 달기

- git tag
	- 이 프로젝트 디렉토리 안에 있는 모든 태그 조회

- git show [태그 이름]
	- 각 태그와 연결된 커밋 보기

## 커밋 다루기 정리

- git log : 커밋 히스토리를 출력

- git log --pretty=oneline : --pretty 옵션을 사용하면 커밋 히스토리를 다양한 방식으로 출력할 수 있습니다. --pretty 옵션에 oneline이라는 값을 주면 커밋 하나당 한 줄씩 출력해줍니다. --pretty 옵션에 대해 더 자세히 알고싶으면 [이 링크]{https://git-scm.com/docs/pretty-formats} 를 참고하세요. 

- git show [커밋 아이디] : 특정 커밋에서 어떤 변경사항이 있었는지 확인

- git commit --amend : 최신 커밋을 다시 수정해서 새로운 커밋으로 만듦

- git config alias.[별명] [커맨드] : 길이가 긴 커맨드에 별명을 붙여서 이후로 별명으로 해당 커맨드를 실행할 수 있도록 설정

- git diff [커밋 A의 아이디] [커밋 B의 아이디] : 두 커밋 간의 차이 비교

- git reset [옵션] [커밋 아이디] : 옵션에 따라 하는 작업이 달라짐(옵션을 생략하면 --mixed 옵션이 적용됨) 
		(1) HEAD가 특정 커밋을 가리키도록 이동시킴(--soft는 여기까지 수행)

		(2) staging area도 특정 커밋처럼 리셋(--mixed는 여기까지 수행)

		(3) working directory도 특정 커밋처럼 리셋(--hard는 여기까지 수행)

		그리고 이때 커밋 아이디 대신 HEAD의 위치를 기준으로 한 표기법(예 : HEAD^, HEAD~3)을 사용해도 됨

- git tag [태그 이름] [커밋 아이디] : 특정 커밋에 태그를 붙임




