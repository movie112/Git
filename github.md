# Github
- https://blog.naver.com/rtyu4236/222481155107
---
## git-github 연결
```
git remote add origin {repository_name}.git
```
---
## Pull
- 최근 버전 local로 가져와 작업
- pull은 fetch, merge 2가지 명령어가 합쳐진 것이라고 볼 수 있다.
- 간단하게 Pull 사용
```
git pull origin
```

- fetch를 통해 github에서 업데이트된 목록은 확인하고 다운받을 수 있다.
```
git fetch origin
```
- 바뀐 부분 확인하고 싶다면
```
git diff origin/master
```
- 다운받은 branch(origin/master)와 현재 branch(master)를 merge
```
git merge origin master
```
---
## Push
- local 에서 작업한 내용 github에 업데이트
```
git commit -a -m {message}
git push origin
```
---
## Clone
```
git clone {repository URL} {디렉토리 이름}
```
---
## Ignore
- 일부 파일 숨기기
```
touch .gitignore  # file 생성
# 설정은 작성규칙 참고
```
---
## Revert
- 이전 commit 버전으로 되돌리기
- 1-2-3-4-5 -> 1-2-3-4-5-6(4)
```
git log --oneline # 우선 로그 기록 간단하게 보기
git revert HEAD --no-edit # 가장 최근 버전으로 되돌리기
git revert HEAD~{N} --no-edit # 가장 최근 버전의 N번 밑의 버전으로 되돌리기
```
---
## Reset
- 1-2-3-4-5 -> 1-2-3-4
```
git reset {commit hash}
```
