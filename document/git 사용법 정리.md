# 코딩 정리노트

- git(버전 관리 시스템), github 사용법

작업한 코드 기록 및 보관 가능(백업, 열람 가능)

작업폴더에 git 사용 희망 시

git init

- 파일 현재 상태 기록(버전 생성)은

git add 파일명

git commit -m '내가 원하는 제목'

git add로 기록할 파일 선택하고

git commit으로 저장소에 저장

동시처리도 가능

git status(상태창)

git log

git difftool '커밋아이디' 하면 현재파일, 특정커밋 비교 가능

git difftool '커밋아이디' '두개' 하면 커밋된 코드 둘을 비교 분석 가능

branch 기능으로 복사본 생성

switch 브랜치 이름으로 이동

main branch와 서브 branch 변경 내용이 같고 merge로 병합 시 충돌이 일어남(직접 수정)

원하는 코드만 남기고 -> git add -> git commit

merge 완료한 브랜치 삭제는 git branch -d 브랜치명

merge 안한 브랜치 삭제는 git branch -D 브랜치명

rebase 쓰는 이유: 간단하고 짧은 브랜치는 이거 쓰면 깔끔해짐

브랜치의 시작점을 다른 commit으로 이동

rebase 이용해서 신규브랜치의 시작점을 main 브랜치 최근 commit으로 옮긴 다음

fast-forward merge 함

일반 merge는 중심브랜치로 이동해서 git merge 새로운브랜치명

rebase, merge 하고 싶으면 새로운브랜치로 이동해서 git rebase 중심브랜치명

squash and merge 하면 git merge --squash 새브랜치 하면 메인 브랜치의 로그 출력 시 깔끔함

commit 고유 id를 통해 시간여행 가능

파일 하나를 되돌리려면 git restore 파일명

최근 commit 된 상태로 현재 파일의 수정 내역을 되돌릴 수 있음

git restore --source 커밋아이디 파일명

이러면 입력한 파일이 특정 커밋아이디 시점으로 복구

git restore --staged 파일명

특정 파일을 stagigng 취소 가능

commit 취소하고 싶으면 git revert 사용

git revert 커밋아이디 입력 시 해당 커밋아이디에서 일어난 일만 취소

git reset --hard 커밋아이디 입력 시 그 커밋이 생성될 때로 시간 여행 시켜줌

프로젝트 망하거나 짧은 거리 돌아갈 때 사용하면 됨

\*여러명이서 협업하는 리포지토리에는 reset 사용 금지\*

git reset --soft 커밋아이디 하면 a, c 파일은 남아있고 b 파일은 staging area(commit 가능)

git reset --mixed 커밋아이디 하면 a, c 파일은 남아있고 b 파일은 staging 되지 않은 상태가 됨.
(git add하고 commit)

기본 브랜치 이름을 main으로 설정

git branch -M main

로컬저장소에서 원격저장소로 폴더를 업로드하고 싶다면

git push -u 원격저장소주소 main 하면 됨

-u는 방금 입력한 주소를 기억해두라는 뜻. 주소 길게 입력 안 하고 git push만 입력해도 동작

주소는 변수로 저장 가능

git remote add 변수명 저장소주소 입력하면 변수로 지정

원격저장소에 있던 소스코드 그대로 내려받으려면 git clone https: //원격저장소주소


\*저장소에 올리지 않는 파일들은 .gitignore에 명시

git push 시 팀원이 push한 상태에서 push가 동작하지 않을 수 있음

원격저장소에 새로운게 생기면 push 못함

- TypeScript

async/await 존재 이유

동기적일 때 데이터가 크면 프로그램은 대기상태. 사용자 및 서버 모두 비효율적

-> 멀티 스레드를 사용한 비동기 방식 사용, 하지만 매우 어렵고 데드락도 많이 걸림

자바스크립트는 이벤트 루프를 통해 비동기 처리-> 콜백지옥 가능

js 이벤트는 3가지 요소

Event Target

Event Type

Event Listener

- firebase

firebase 사용 시 getAdminDb 함수를 임포트 해온다.

const db = await getAdminDb(); 활용해서 파이어스토어에 데이터 저장한다.
