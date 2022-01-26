# TIL (Today I Learned)

## 1. CLI 기초

### (1) GUI와 CLI의 정의

- GUI (Graphic User Interface) : 그래픽을 통해 사용자와 컴퓨터가 상호 작용하는 방식
- CLI (Command Line Interface) : 터미널을 통해 사용자와 컴퓨터가 상호 작용하는 방식

### (2) 경로

- 루트 디렉토리 (Root Directory, /)
  - 모든 파일과 폴더를 담고 있는 최상위 폴더
  - Windows의 경우 보통은 C 드라이브를 의미
- 홈 디렉토리 (Home Directory, ~)
  - Tilde(틸드)라고도 부르며, 현재 로그인 된 사용자의 홈 폴더를 의미
  - Windows의 경우 C:/사용자(Users)/현재 사용자 계정을 의미
- 절대 경로 : 루트 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것
- 상대 경로 : 현재 작업하고 있는 디렉토리를 기준으로 계산된 상대적 위치를 작성한 것

### (3) 터미널 명령어

- start/open : 폴더/파일을 여는 명령어
- touch : 파일을 생성하는 명령어, 띄어쓰기로 구분하여 여러 파일을 한꺼번에 생성 가능
- mkdir : make directory, 새 폴더를 생성하는 명령어, 띄어쓰기로 구분하여 여러 폴더를 한꺼번에 생성 가능, 폴더 이름 사이에 공백을 넣고 싶다면 따옴표로 묶어서 입력
- ls : list segments, 현재 작업 중인 디렉토리의 폴더/파일 목록을 보여주는 명령어
- ls -a : all 옵션. 숨김 파일까지 모두 보여주는 명령어
- ls -l : long 옵션. 용량, 수정 날짜 등 파일 정보를 자세히 보여주는 명령어
- ls -al : 여러 옵션 축약
- mv : move, 폴더/파일을 다른 폴더 내로 이동 하거나 이름을 변경하는 명령어
- cd : hange directory, 현재 작업 중인 디렉토리를 변경하는 명령어
- cd .. : 부모 디렉토리로 이동 (위로 가기)
- rm : remove, 폴더/파일 지우는 명령어
- clear/ctrl + l : 터미널 화면 청소
- 위, 아래 방향키 : 과거에 작성했던 명령어 조회
- tab : 폴더/파일 이름 자동 완성
- ctrl + a : 커서가 맨 앞으로 이동
- ctrl + e : 커서가 맨 뒤로 이동
- ctrl + insert : 복사
- shift + insert` : 붙여넣기



## 2. Visual Studio Code

- 



## 3. Markdown

- 제목 (Headings) : h1 ~ h6 에 해당하는 제목을 표현, \#을 사용
- 목록 (List) : 순서가 없는 목록과 순서가 있는 목록을 표현
  - 순서가 없는 목록 :  - * +
  - 순서가 있는 목록 : 1. 2. 3.
  - 들여쓰기 : Tab
  - 내어쓰기 : Shift + Tab
- 강조 (Emphasis) : 글자의 스타일링을 표현
  - 기울임 : `*글자*` or `_글자_`
  - 굵게 : `**글자**` or `__글자__`
  - 취소 :  `~~글자~~`
- 코드 (Code)
  - 인라인(Inline) 코드 : `inline code`처럼 백틱을 통해 코드를 감싸줌
  - 블록(Block) 코드 : ```python 처럼 백틱을 3번 입력하고 코드의 종류를 작성
- 링크 (Links) : 클릭하면 해당 주소로 이동할 수 있는 링크를 표현
  - `[표시할 글자](이동할 주소)` 형태로 작성
- 이미지 (Images) : 마크다운 문서에 이미지 삽입
  - `![대체 텍스트](이미지주소)`형태로 작성
  - 대체 텍스트란 이미지를 정상적으로 불러오지 못했을 때 표시되는 문구
  - Typora에서는 이미지 파일을 끌어와서 놓아도 자동 업로드
- 인용 (Blockquote)
  - 주석이나 인용 문구를 표현
  - `>` 를 사용, 갯수에 따라 중첩이 가능
- 표 (Table)
  - 테이블(표)를 생성
  - 행과 열 구분 : 파이프( | )와 하이픈( - )을 이용
  - 테이블 양쪽 끝의 파이프( | )는 생략 가능
  - 헤더 셀 구분 : 3개 이상의 하이픈( - )이 필요
  - Typora에서 표 생성 단축키 : ctrl + T
  - 행 늘리기  :  ctrl + enter
- 수평선 (Horizontal Rule)
  - 구분 선을 생성
  - \- * _ 을 3번 이상 연속으로 작성



## 4. Git 기초

### (1) Git 초기 설정

- 누가 커밋 기록을 남겼는지 확인할 수 있도록 이름과 이메일을 설정

- ```bash
  $ git config --global user.name "이름"
  $ git config --global user.email "메일 주소"
  ```

- ```bash
  # 설정 확인
  $ git config --global -l
  
  or
  
  $ git config --global --list
  ```

### (2) Git 명령어

- git init
  - 현재 작업 중인 디렉토리를 Git으로 관리한다는 명령어
  - .git 이라는 숨김 폴더를 생성하고, 터미널에는 (master)라고 표기

- git status

  - Working Directory와 Staging Area에 있는 파일의 현재 상태를 알려주는 명령어
  - Untracked : Git이 관리하지 않는 파일 (한번도 Staging Area에 올라간 적 없는 파일)
  - Tracked : Git이 관리하는 파일
    - Unmodified : 최신 상태
    - Modified : 수정되었지만 아직 Staging Area에는 반영하지 않은 상태
    - Staged : Staging Area에 올라간 상태

- git add

  - Working Directory에 있는 파일을 Staging Area로 올리는 명령어

  - Git이 해당 파일을 추적(관리)할 수 있도록 함

  - ```bash
    #특정 파일
    $git add a.txt
    
    #특정 폴더
    $git add my_folder/
    
    #현재 디렉토리에 속한 파일/폴더 전부
    $git add .
    ```

- git commit

  - Staging Area에 올라온 파일의 변경 사항을 하나의 버전(커밋)으로 저장하는 명령어

  - ```bash
    git commit -m "first commit"

- git log

  - 커밋의 내역(ID, 작성자, 시간, 메세지 등)을 조회할 수 있는 명령어

  - ```bash
    $ git log
    
    #한 줄로 축약
    $ git log --oneline
    
    #브랜치와 머지 내역을 그래프로 시각화
    $ git log --graph
    
    #현재 브랜치를 포함한 모든 브랜치의 내역
    $ git log --all
    
    #커밋 내역의 순서를 반대로 (최신이 가장 아래)
    $ git log --reverse
    
    #파일의 변경 내용도 같이 보고 싶을때
    $ git log -p
    
    #원하는 갯수(n) 만큼의 내역을 보고싶을때 (n에 숫자 입력)
    $ git log -n
    ```

- git checkout

  - 해당 저장 기록으로 가기

  - ```bash
    # 해쉬값 위치로 가기
    $ git checkout 해쉬값
    
    # n번째로 가기(HEAD -> master)기준
    $ git checkout head ~n
    
    #돌아오기
    $ git checkout master
    ```