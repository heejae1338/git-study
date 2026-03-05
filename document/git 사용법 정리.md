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
