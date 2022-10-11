# 🌈 Git 명령어 정리
## ✏️ Starting git

- 설치 확인     
  - 설치가 되었다면 version 출력
```
git --version
```

- 사용자 등록
```
git config --global user.name "user-name"
git config --global user.email "user@email.com"
```

- git 초기화
```
git init
```

- 현재 git 상태(파일의 상태)
  - Tracked: repository에 added된 file
  - Untracked: directory에 저장되어 있으나 아직 repository에 add하지 않은 file
```
git status
```

## ✏️ Add
- 일정 작업을 끝내면 반드시 파일들을 staging environment에 올려야 하고, 올려진 파일들을 repository에 commit한다.
- - staging environment에 놀리는 명령어
- `git status`로 상태를 확인하면 __file__들과 __No commits yet__이라고 뜰 것
```
git add {파일명}
```

- 새로 생성, 수정, 삭제된 여러 파일을 한 번에 stage
```
git add --all
```

## ✏️ Commit
- commit을 하면 하나의 버전이 생성되어 프로그램의 버전 관리 가능
- 작업을 완료하고 모든 file을 stage했을 때 commit
- 변화된 부분을 설명하는 message를 포함
```
git commit -m "First release!"  // -m: message를 작성하기 위한 옵션
```

```
git commit -a -m "message"   // -a : 자동으로 stage한 후 commit
```
- 자잘한 변화들을 stage한 후 commit하는 것이 귀찮다면 __-a__옵션으로 변화들을 stage없이 commit하는 것도 가능하지만 비추

- commit 기록 확인
```
git log
```

## ✏️ Help
- 명령어에 대한 설명
```
git {명령어} -help   // 간단한 설명
git {명령어} --help  // Git manual page로 이동하여 자세한 설명  
git help --all      //  전체 명령어에 대한 설명
```

## ✏️ Branch
- branch: 메인 프로젝트의 새로운 버전, 메인 파일에는 영향을 끼치지 않으면서 여러 가지 branch를 만들어 시도
```
git branch {name}
```

- 현재 생성되어 있는 branch들 확인 가능
- * 이 현재 작업하고 있는 branch
```
git branch
```

- 다른 branch로 이동해서 작업
```
git checkout {name}
git checkout -b {name2}  // branch 바로 생성하고 이동
```

## ✏️ Branch Merge
```
git merge {name}
git branch -d {name}  // 변경사항이 master에 반영되어 branch 삭제
```

## ✏️ git-github 연결
```
git remote add origin {repository_name}.git
```

## ✏️ Pull
- 최근 버전 local로 가져와 작업
- pull은 fetch, merge 2가지 명령어가 합쳐진 것
- 간단하게 Pull 사용
```
git pull origin
```

- fetch를 통해 github에서 업데이트된 목록은 확인하고 다운 가능
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

## ✏️ Push
- local 에서 작업한 내용 github에 업데이트
```
git commit -a -m {message}
git push origin
```

## ✏️ Clone
```
git clone {repository URL} {디렉토리 이름}
```

## ✏️ Ignore
- 일부 파일 숨기기
```
touch .gitignore  # file 생성
# 설정은 작성규칙 참고
```

## ✏️ Revert
- 이전 commit 버전으로 되돌리기
- 1-2-3-4-5 -> 1-2-3-4-5-6(4)
```
git log --oneline # 우선 로그 기록 간단하게 보기
git revert HEAD --no-edit # 가장 최근 버전으로 되돌리기
git revert HEAD~{N} --no-edit # 가장 최근 버전의 N번 밑의 버전으로 되돌리기
```

## ✏️ Reset
- 1-2-3-4-5 -> 1-2-3-4
```
git reset {commit hash}
```

---
## Reference
<https://blog.naver.com/rtyu4236/222474823748>
