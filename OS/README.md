# [뇌를 자극하는 윈도우즈 시스템 프로그래밍 - 인프런](https://www.inflearn.com/course/%EC%8B%9C%EC%8A%A4%ED%85%9C-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)

## 1장 
* [시스템 프로그래밍의 이해와 접근/컴퓨터 하드웨어의 구성/CPU에 대한 이해](https://github.com/ejxzhn22/TIL/tree/main/OS#%EC%8B%9C%EC%8A%A4%ED%85%9C-%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D%EC%9D%98-%EC%9D%B4%ED%95%B4%EC%99%80-%EC%A0%91%EA%B7%BC-%EC%BB%B4%ED%93%A8%ED%84%B0-%ED%95%98%EB%93%9C%EC%9B%A8%EC%96%B4%EC%9D%98-%EA%B5%AC%EC%84%B1cpu%EC%97%90-%EB%8C%80%ED%95%9C-%EC%9D%B4%ED%95%B4)
  * 시스템(컴퓨터 시스템)의 범위
  * 시스템 프로그래밍
  * 응용 소프트웨어 개발과의 차이점
  * 컴퓨터 시스템의 주요 구성요소
  * 컴퓨터 하드웨어 구성
  * CPU에 대한 이해
  * 클럭 신호(Clock Pulse)
* [프로그램의 실행과정/하드웨어 구성의 재접근](https://github.com/ejxzhn22/TIL/tree/main/OS#%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%A8%EC%9D%98-%EC%8B%A4%ED%96%89%EA%B3%BC%EC%A0%95-%ED%95%98%EB%93%9C%EC%9B%A8%EC%96%B4-%EA%B5%AC%EC%84%B1%EC%9D%98-%EC%9E%AC%EC%A0%91%EA%B7%BC) 
  * 프로그램 실행 과정
  * Stored Program Concept

## 2장
* [Windows에서의 유니코드(UNICODE)](https://github.com/ejxzhn22/TIL/tree/main/OS#windows%EC%97%90%EC%84%9C%EC%9D%98-%EC%9C%A0%EB%8B%88%EC%BD%94%EB%93%9Cunicode)
  * 문자셋의 종류와 특성

## 5장
* [프로세스와 스케줄러의 이해](https://github.com/ejxzhn22/TIL/tree/main/OS#%ED%94%84%EB%A1%9C%EC%84%B8%EC%8A%A4%EC%99%80-%EC%8A%A4%EC%BC%80%EC%A4%84%EB%9F%AC%EC%9D%98-%EC%9D%B4%ED%95%B4)
  * 프로세스
  * 프로세스의 범위

<br>

---

## 시스템 프로그래밍의 이해와 접근, 컴퓨터 하드웨어의 구성/CPU에 대한 이해

### 시스템(컴퓨터 시스템)의 범위

=> 하드웨어 + 운영체제
ex) CPU가 intel기반이고 운영체제는 windows다.

### 시스템 프로그래밍

* 컴퓨터 시스템을 활용하는 소프트웨어 개발
* windows 운영체제의 기능을 십분 활용하는 프로그래밍

### 응용 소프트웨어 개발과의 차이점

* 시스템 프로그래밍은 모든 응용 프로그램에 포함되는 요소

### 컴퓨터 시스템의 주요 구성요소

* CPU, 캐쉬
  * 컴퓨터 하드웨어 구조
* 운영체제
  * 메인 메모리
* 하드디스크 
  * 파일I/O (다양한 I/O포함)

### 컴퓨터 하드웨어 구성

* CPU ( Central Processing Unit)
  * 중앙 처리 장치
  * 연산이 이루어지는 원리는 무엇인가? => 연산은 프로그램 실행과정의 일부분이다.

* 메인 메모리 
  * 램(RAM)
  * 프로그램 실행 방식을 이해하는 것

* 입출력 버스
  * 데이터 송수신이 이루어지는 원리 

### CPU에 대한 이해(전체 구성)

* ALU(Arithmetic Logic Unit)
  * 연산 담당 

* 컨트롤 유닛
  * CPU를 총괄하여 신호를 주는, 가장 많은 컨트롤을 하는 요소
  * 명령어 해석, CPU 행동 결정 
  
* 버스 인터페이스
  * 버스가 어덯게 데이터를 주고 받는지 알고 있다.
  * 들어온 데이터를 레지스터에 저장 

### 클럭 신호(Clock Pulse)

* 동작 타이밍
  * 클럭 발생기의 클럭

* 필요성
  * 요소들의 동기화

* 시스템을 안정적으로, 데이터를 분실하는 것을 막기 위해 클럭 신호를 제공한다.

<br>

## 프로그램의 실행과정, 하드웨어 구성의 재접근

### 프로그램 실행 과정

전처리기 -> 컴파일러 -> 어셈블러 -> 링커

* 전처리기에 의한 치환 작업
 * #으로 시작하는 지시자

* 컴파일러에 의한 번역
 * CPU의 명령어로 번역

* 어셈블러에 의한 바이너리 코드 생성
 * CPU의 명령어를 바이너리 코드로 번역

* 링커에 의한 연결과 결합
 * 라이브러리와의 결합
 * 실행 파일을 만드는 것


### Stored Program Concept

* 명령어는 메모리에 저장되어서 cpu에 의해 1.fetch되고 2.decode되고 3.execution 되어야 한다.

* Fetch
 * CPU 내부로 명령어 이동(버스 인터페이스를 통해서) 

* Decode
 * 명령어 해석
 * 컨트롤 유닛에 의해 해석

* Execution
 * 연산을 진행
 * 보통은 ALU를 생각 => 연산이라는 건 CPU가 하는 궁극적인 일, Execution이 더 큰 의미
 * => ALU가 중심이 되어서 요소들이 협력하여 execution 된다.

* 명령어가 메모리에 저장되있는 상태에서 명령어를 cpu로 하나씩 가져와서 명령어가 어떤 의미를 가지는지 decode(해석)하고 execution(실행)을 시킨다.


## Windows에서의 유니코드(UNICODE)

### 문자셋의 종류와 특성

* SBCS(Single Byte Character Set)
 * 문자를 표현하는데 1byte 사용
 * 아스키 코드

* MBSC(Multi Byte Character Set)
 * 한글은 2byte , 영문은 1byte 사용 => 효율적이라고 생각할 수 있지만, 발전하면서 문자표현으로는 부담X

* WBCS(Wide Byte Character Set)
 * 문자를 표현하는데 2byte 사용 => 안정적, 메모리 차이 별로 없음
 * 유니코드 


## 프로세스와 스케줄러의 이해

### 프로세스

* 메인 메모리로 이동하여 실행 중인 프로그램 -> 일반적인 정의

### 프로세스의 범위

* 메모리 구조 + 레지스터 Set
* 프로세스 별 독립적인 대상은 프로세스의 범주에 포함시킬 수 있다.
