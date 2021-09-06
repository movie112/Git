<https://blog.naver.com/rtyu4236/222474823748>
## Starting git

- 설치가 되었는지 확인한다. 설치가 되었다면 version이 출력
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


---
## Add
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
---
## Commit
- commit을 하면 하나의 버전이 생성되어 프로그램의 버전을 관리할 수 있다.
- 작업을 완료하고 모든 file을 stage했을 때 commit을 한다.
- 변화된 부분을 설명하는 message를 포함한다.
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
---
## Help
- 명령어에 대한 설명
```
git {명령어} -help   // 간단한 설명
git {명령어} --help  // Git manual page로 이동하여 자세한 설명  
git help --all      //  전체 명령어에 대한 설명
```
---

