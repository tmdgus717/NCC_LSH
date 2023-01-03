# Java Fundamental
## day1

<strong>system 개발</strong>

1. 모델링 => system 구축 시 구현 전 결정하는 모든 활동
2. 구축할 system 정의
3. 요구사항 정의
4. 계획(분석,설계)
5. 결과물 => 모델
6. 표기법(Notation) : UML (Unified Modeling Language) // UML Notation 으로 모델 생성

<strong>구현</strong>
1. 시스템 실제 구현
2. 소스코드, 컴파일, 디버깅
3. 결과물 => 코드를 포함한 system
4. 프로그래밍 언어: Java

<strong>system 개발 절차</strong>
1. 요구사항 정의
2. 분석
3. 설계
4. 구현

<strong>*Java 개발환경 구축 => JDK(java development kit)</strong>
<strong>Java 특징</strong>
* OOPL (Object Oriented Programming Language)
* 플랫폼 독립적 (JDK = JAVA 플랫폼 = J2SE 플랫폼 : JAVA 플랫폼은 O/S에 독립적이다. O/S와 ~.class중간에 JDK를 이용
* JDK = 개발 툴과 JRE(Java Runtime Environment)를 포함하고 있다. JAVA 컴파일러 보유 ( .java -> .class(자바 바이트 코드))
* JRE 안의 JVM의 자바 인터프리터가 실행
* JDK > JRE > JVM
 
//용어 정리
* 플랫폼 : O/S의 플랫폼 = H/W , APP의 플랫폼 = O/S, ~.hwp의 플랫폼 = HWP
* End User = 사용자
* url = Uniform Resource Locator : 리소스의 위치를 가리키는 문자열
          
 ## day2
 //용어정리
 * csv = 구분자 : command seperated value
 * snake case : csv = _ (언더바)
 * camel case : csv = 대문자
 * cmd = command = console
 * utf-8 : Unicode Transformation Format - 8bit
 * ANSI : American National Standards Institute : 8bit 문자표현 방식
 * console 명령어 : %~% : 변수로 해석합니다. :
 
<strong>환경변수설정</strong>
* 컴퓨터가 자바가 설치된 경로를 자동으로 찾지 못하기 때문에 path로 자바 응용프로그램(ex.jdk,jre)가 환경변수 설정 path 를 통해 설치된 폴더 위치를 가리켜야한다.

 JAVA_HOME = C:\Program Files\Java\jdk1.8.0_181
 
 path : %JAVA_HOME%\bin
 
 echo %path%
 
<strong>헷갈리는 내용정리</strong>
* casting
묵시적(implicit): 자동형변환 
명시적(explicit): 프로그래머가 형변환

```java
byte 1 = 100;
byte b2 = 20;

//byte b3 = b1+b2 (error) ->b1과 b2는 int로 연산 후 int 값을 byte 넣기 불가능 
byte b4 = (byte)(b1+b2); //명시적 형변환
byte b5 = (byte)(b1+b4); // 쓰레기값 출력 byte보다 큰값 대입

int i1 = b1+b2; // 묵시적 형변환
double test01 = 100 + 0.5; //=> data type 이 큰쪽으로 묵시적 형변환

//int test02 = 100 + 0.5; compile error double to int

int i3 = 201/2; // 100
double d1 = 201/2; // 100.0
double d2 = (double)201/2; // 100.5
double d3 = (double)(201/2); // 100.0


```
