## 수강대상
- C programming 가능자
  - 연산자와 제어문, 함수, 배열과 포인터, 구조체 등의 개념을 이해하는 개발자
## 실습환경
- g++, visual C++2017
#### 소스 코드 작성 환경
- 1. 소스 코드 편집기
  - visual studio, vi, eclipse, sublime text, notepad++ 등 어떤 편집기를 사용해도 상관없음
- 2. 소스 코드 확장자
  - C언어 : .c
  - C++ 언어 : .cc, .cxx, .cpp
#### 컴파일 방법
- 1. 통합개발환경(IDE)으로 컴파일.
  - visual c++, xCode, Dev-C++,codeblock, eclipse, ...
  - 최신 문법 (C++17)의 지원 여부를 확인할 필요가 있음
- 2. command prompt(termianl)에서 컴파일
  - g++ hello.cpp -std=c++1z -> a.exe 
  - cl hello.cpp /std:c++lated /nologo /EHsc /Za ->hello.exe
## 과정 내용
 - C++ 기본 문법 (c++ 11/14/17 최신 문법 / modern c++)
 - 객체 지향 프로그래밍
 - 각 주제에 대해서 깊이 있기는 힘듬
 - 난이도가 높은 주제는 중급에서 배움
 - template 도 기본만 다루고 별도 과정에서 배움 
 
### Section 1. c보다 좋아진 c++
- 함수, 변수, 구조체, 캐스팅 등 개념은 C에도 존재하지만 C++에서 더욱 발전된 새로운 내용
### Section 2~3. 객체지향 프로그래밍 
- 객체지향 프로그래밍 개념, 클래스 문법, 상속 문법 등
### Section 4. C++ 개발자라면 알아야 하는 것들..
- 연산자 재정의 문법, STL 사용법, 예외 등.. 
## reference 
- cppreference.com
  - cpp 2.0 도 내용 잘 정리 되있음
  - c++ 표준의 내용을 가장 잘 정리한 사이트
  - 최신의 다양한 주제를 깊이 있게 다루고 있는 reference 형식의 사이트
- isocpp.org
  - current is c++ status
  - c++ 표준에 관련된 자료
  - c++ 관련 다양한 기사가 있음
  - c++98/03
    - 1998년 표준화 되고 2003년 수정된 버전
    - c++ 최초 표준화
  - c++ 11/14
    - 2011 표준화 되고 2014년 추가로 개선이 발표된 버전
    - 이후 3년 마다 한번씩 표준을 Update 하기로 결정
  - c++ 17
    - 2017년에 발표된 버전
    - 강좌에서 이 버전까지 다루고 있음
  - c++20/23
    - 현재 표준위원회에서 논의중인 버전 
