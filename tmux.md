# Tmux 명령어 

## 설치
- for MacOS
  - `brew install tmux`
- for Ubuntu
  - `sudo apt-get install tmux`
## Session
- 새 session 생성
  - `tmux`
  - `tmux new -s {session_name}` # 이름
- session 이름 수정
  - `ctrl+b`, `$` # 원하는 이름 적고 Enter
- sesstion 종료 (session 없어짐)
  - `exit` or `ctrl+d` # pane -> window 순으로 하나 씩 닫힘
- session 닫기 (detach, 백그라운드 지속)
  - `ctrl+b`, `d`
- session 열기 (attach)
  - `tmux at -t {session_name}`
  - `tmux a` # 최근 session 열기
- session 목록
  - `tmux ls`

  ## Window
  - 새 window 생성
    - `ctrl+b`, `c`
  - window 이름 수정
    - `ctrl+b`, `,`
  - 하단 바에서 다음 window로 이동
    - `ctrl+b`, `n`
  - 하단 바에서 이전 window로 이동
    - `ctrl+b`, `p`
  - 특정 window로 이동
    - `ctrl+b`, `{name}`
  - 모든 session의 hierarchy를 tree 구조로 보여줌
    - `ctrl+b`, `w` # 종료는 esc

## Pane
- 화면 새로 분할(좌우)
  - `ctrl+b`, `%`
- 화면 가로 분할(상하)
  - `ctrl+b`, `"`
- pane 이동
  - `ctrl+b`, `q`, `{num}`
  - `ctrl+b`, `{방향키}`
- 현재 pane을 zoom in/out
  - `ctrl+b`, `z`
- pane layout 변경
  - `ctrl+b`, `space_bar`
 
---
Reference : https://knackin.tistory.com/4

