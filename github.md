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
