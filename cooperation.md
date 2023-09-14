## 1. fork
- Original Repository를 fork한다.
## 2. clone
```
git clone {링크.git}
```
## remote
```
# 원본 repository 원격 저장소로 추가 / fork한 local은 'origin'으로 추가되어 있다.
git remote add {remote 별명} {링크}

# 원격 저장소 설정 상태 확인
git remote -v
```
## branch 생성
- local에서 branch를 추가한다.
```
# branch 생성 및 이동
git checkout -b {branch name}

# branch 확인
git branch
```
## 작업 후 add, commit, push
```
git add .

git commit -m ~

# branch 이름 명시 요구됨
git push origin {branch name}
```
## Pull Request
- Compare & Pull request 버튼
- 메시지 작성
## branch 삭제
```
# 코드 동기화
git pull {remote 별명} main

# branch 삭제
git branch -d {branch name}
```

## + git pull Already up to date
```
git fetch --all
git reset --hard origin/master
```
