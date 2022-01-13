# TIL 정리하기

> 깃허브 특강 3일 중 1일차 기록. 송채원.



## Github 깃허브 특강



### Why Git and Github?

1. 깃Git 과 깃허브Github 란 무엇인가?

 깃Git은 분산 버전 관리 프로그램이다. 어떠한 작업을 할 때, 원본과 수정사항을 반영한 수정본들을 체계적으로 관리해줌으로써 사용자에게 편의를 제공한다. 

 여기서 분산이 가리키는 말은 그 반댓말을 먼저 알면 쉽다. 중앙 집중식이 그 반댓말인데, 파일의 원본과 그 변경사항들을 특정 중앙에서 관리하는 것이 바로 그것이다. 분산은 이와 반대로 모든 사용자들에게 분산되어 각각 원본과 변경사항들이 저장되는 방식인데, 블록체인과 유사하게 어느 한곳에 문제가 생기더라도 분산되어 저장되므로 안정성이 뛰어나다는 장점이 있다. 

 깃허브는 마치 개발자들의 인스타그램과도 같다. 자신의 개발 경험과 행적들을 모두 기록하고 담을 수 있는 공간이다. 따라서 포트폴리오를 쌓기에 아주 좋은 플랫폼이라고 할 수 있다. 



## CLI이란

> Command Line Interface의 약자

 오늘날의 퍼스널 컴퓨터(PC)를 탄생시킨 GUI의 이전 컴퓨터들을 작동했던 기본적인 인터페이스 방식으로, 한 줄 한 줄 명령어로 컴퓨터를 다루는 방식이다.



> UNIX 운영 체제에서 개발된 프로그램이 많기에, 기존에 존재하는 윈도우의 powershell이나 명령 크롬프트가 아닌, UNIX 운영 체제로 번역해주는 Git Bash를 사용하여 CLI를 익혀보자. 



##### 1. 루트, 홈 디렉토리

< 루트 디렉토리 >

- 모든 파일/폴더를 담고 있는 폴더. 가장 상위의 폴더를 말한다. 
- windows 같은 경우, 보통 C 드라이브를 의미한다. 

< 홈 디렉토리 >

- Tilde틸드 라고도 칭하며, 현재 로그인 된 사용자의 홈 폴더를 의미한다.



##### 2. 절대 경로와 상대 경로

< 절대 경로 >

- 루트 디렉토리부터 목적 지점까지 거치는 모든 경로를 전부 작성한 것



< 상대 경로 >

- 현재 워킹 디렉토리를 기준으로 계산된 경로를 말함. 
- 절대 경로의 반대어.



상대 경로로 쓰이는 명령어들의 예시는 다음과 같다. 

(1) . : 현재 워킹 디렉토리

(2) .. : 현재 워킹 디렉토리의 바로 상위 폴더



##### 3. 터미널 명령어

1. `touch`

- 파일을 생성하는 명령어

- 띄어쓰기로 구분하여 여러 파일을 한 번에 생성 가능

  `touch 일기장.txt 과제1.txt 과제2.txt`

- 숨김 파일을 만들기 위해서는 파일 앞에 `.`을 붙이면 된다.



2. `mkdir`

- make directory 의 약자로, 새 폴더를 생성하는 명령어

- 띄어쓰기로 구분하여 여러 폴더 생성 가능

- 폴더 이름 사이에 공백이 있다면, 따옴표로 이름을 묶어준다

  ```
  mkdir 이화여자대학교
  mkdir '제37대 심리학과 학생회 SYM;PHONY'
  ```



3. `ls`

- list segment의 약자로, 현재 작업 중인 디렉토리의 폴더/파일 목록을 보여주는 명령어.
- `-a` : all 옵션. 숨김 파일까지 모두 보여준다. 
- `-l` : long 옵션. 용량, 수정 날짜 등 파일 정보를 자세히 보여준다. 
- 






































