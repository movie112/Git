# Tmux 명령어 
https://knackin.tistory.com/4

## 설치
- for MacOS
  - `brew install tmux`
- for Ubuntu
  - `sudo apt-get install tmux`
## Session
- 새 session 생성
  - `tmux`
  - `tmux new -s (session_name)`
- session 이름 수정
  - `ctrl + b, $` # 원하는 이름 적고 Enter
- sesstion 종료 (session 없어짐)
  - `exit` or `ctrl + d` # pane -> window 순으로 하나 씩 닫힘
- session 닫기 (detach, 백그라운드 지속)
  - `ctrl + b, d`
- session 열기
  - `tmux at -t` {session name}
  - `tmux a` # 최근 session 열기
- session 목록
  - `tmux ls`

  ## Window
  - 새 window 생성
    - `ctrl + b, c`
  - window 이름 수정
    - `ctrl + b ????`
  - 
