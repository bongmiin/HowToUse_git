## Branch
- 나무의 가지 같은 깃의 성질

- git branch [branch 이름]
	- branch 만들기

- git checkout [가고싶은 branch의 이름]

### branch 다뤄보기
- git -d [브랜치 이름]
	- 브랜치 삭제

- git checkout -b [브랜치 이름]
	- 브랜치를 만들며 그 브랜치로 이동

### 브랜치 merge하기
- git merge [브랜치 이름]
	- 현재 branch에 다른 branch를 합침

### merge시 conflict에러 해결 방법
1. 컨플릭트가 발생한 파일을 연다
2. 머지의 결과가 되었으면 하는 모습대로 코드를 수정
3. 커밋하기
- *git merge --abort*
	- 머지 작업 취소
### 파일 여러개에서 coflict
1. 파일 하나씩 conflict를 해결하고 하나씩 staging area에 올리거나
2. 모든 파일들의 conflict를 다 해결하고 git add . 커맨드로 한번에 커밋

### HEAD와 브랜치의 관계
- Branch
	- 어떤 커밋을 가리키는 포인터
	- 어떤 코드의 관리 흐름
- HEAD
	- Branch를 가리키는 포인터
	- 해당 Branch를 보여줌


## 심화

### git reset과 git checkout의 차이점

- git checkout
	- git checkout [커밋 이름]
		- *Detached HEAD*
		- 헤드가 직접 커밋을 포인팅함 
		- 과거의 특정 커밋에서 새로운 브랜치를 만들때 사용
- git reset
	- HEAD가 가리키던 브랜치가 다른 커밋을 가리키도록 한다
	- HEAD도 결국 간접적으로 다른 커밋을 가리키는 효과가 생긴다.

### 새로운 커밋을 만들지 않는 merge
- Fast-forward merge
	- 커밋 히스토리에서 같은 선에 있는 브랜치를 머지

- 3-way merge
	- base의 내용과 비교했을 때 달라진 부분이 있는 것이 우선
	- 두 브랜치에서 변화가 일어났을 때, Conflict를 발생시킴


## 브랜치 정리 노트

- git branch [새 브랜치 이름] : 새로운 브랜치를 생성

- git checkout -b [새 브랜치 이름] : 새로운 브랜치를 생성하고 그 브랜치로 바로 이동

- git branch -d [기존 브랜치 이름] : 브랜치 삭제

- git checkout [기존 브랜치 이름] : 그 브랜치로 이동

- git merge [기존 브랜치 이름] : 현재 브랜치에 다른 브랜치를 머지

- git merge --abort : 머지를 하다가 conflict가 발생했을 때, 일단은 머지 작업을 취소하고 이전 상태로 돌아감