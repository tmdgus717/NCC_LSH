## day1
  1. 운영체제와 리눅스
  2. 기초사용법
  3. 파일 다루기
  4. vi editor

***
1. 운영체제와 리눅스
* 운영체제의 역할

  사용자와 컴퓨터를 연결하는 다리 역할

  system의 자원관리 (cpu, memory, process, i/o...)

  Kernel, Shell, Application 으로 구성됨

***
2. 기초사용법
* clear
* date : 현재 날짜와 시간
* cal : 이번 달 달력보기 (cal 12 2022)
* logname : 최초 로그인
* hostname
* who, whoami, who am i
* w
* arch : cpu 종류
* uname -r : 커널 버전
* df -h : 파티션 정보
* dpkg -l : 설치된 패키지 목록 
* echo ~ : home?
* echo $HOME
* <strong>ls = 파일 목록 보기</strong> - l(long, 자세히),a(숨긴 파일 보기) , al ...
* ls -F : 파일 종류 함께보기

<STRONG> 파일 내용 보기 </STRONG>
* nl : unmber line (~=cat -b)
* cat (-n : 빈 행에도 줄 번호, -b는 빈 행 줄 번호 X)
* head : 처음부터~ (-5 : 처음~ 5줄)
* tail : 끝부터~

<STRONG> PATH(경로) </STRONG>
* . : 현재
* .. : 부모
* ~ : home
* / : root(최상위)

<STRONG> 경로 이동 </STRONG>
* cd : 절대경로
* cd .. : 이전 디렉토리
* cd ../bin : 상대경로
* pwd : 현재 작업 디렉토리
***
3. 파일 다루기

||파 일|디렉토리|
|---|---|---|
|생성|touch|mkdir|
||vi|mkdir -p|
||cat||
| 복사|cp|cp -r|
|이동,이름바꾸기|mv|mv|
|삭제|rm|rm|
* -i : interactive
* -f : force
* -r : recursive
* -rf
* mkdir {a..k}
* cal > a2 : a2파일로 cal 내용 저장
* date >> a3 : a3파일에 date 내용 추가
* cp -r /etc d20 : 디렉터리 이름 바꾸어 복사
* cp -p : 속성 유지하며 복사
* cp -l : hard link
* cp -s : soft link
* rm a* : a로 시작하는 모든파일 삭제
* rm [b-f]* : b~f 로 시작하는 파일 삭제
* rm -f [^j-c]* : jtbc를 제외하고 삭제
## day2
  5. 홈 디렉터리와 환경설정
  6. 파일 분류 권한의 이해
  7. 압축, ftp client
