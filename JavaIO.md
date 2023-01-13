### I/O 개념

* in - read 의 개념  (source)
  1. 키보드
  2. 파일
  3. 네트워크
* out - write 의 개념 (target)
  1. 화면
  2. 파일
  3. 네트워크

### java.io 패키지의 주요 클래스
 * File : 물리적인 파일과 directory처리
 * inputStream 계열 : 외부로부터 읽어들이는 기능 관련 //바이트단위
 * OutputStream 계열 : 외부로 데이터를 전송하는 기능 관련 크래스들
 * Reader : 문자기반으로 읽어들이는 기능
 * Writer : 문자기반으로 출력하는 기능
 * RandomAccessFile

### 파일 클래스
1. new File(파일명)
2. new File(디렉토리명, 파일명)
3. 폴더와 파일의 구분은 없다. // 기능을 통해서 구분
4. File.seperator 를 통해서 OS에 상관없이 디렉토리 구분자로 이용
