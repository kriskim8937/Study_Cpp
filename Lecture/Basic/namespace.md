## namespace.md
#### namespace의 필요성
- 하나의 프로그램은 **수십 수백개**의 파일로 구성될 수 있고 수십명의 개발자가 같이 작업 할 수도있다.
- 함수 및 구조체 등의 **이름 충돌** 이 발생할 수 있다.
#### namespace의  장점
- 프로그램의 **다양한 요소(함수, 구조체 등)을 연관된 요소끼리 묶어서 관리** 할 수 있다.
- 기능별로 다른 이름 공간을 사용함으로써 **함수/구조체 등의 이름 충돌을 막을 수** 있다.
#### namespcae에 있는 요소에 접근하는 3가지 방법
- 1 **한정된 이름(qulified name)**을 사용하는 방법
  - Audio::init();
- 2 **Using 선언(declaration)**을 사용한 접근
  - using Audio::init;
  - init 함수는 Audio 이름 없이 사용 가능 
- 3 **Using 지시어(directive)**을 사용한 접근
  - using namespace Audio; 
  - Audio namespace의 모든 요소를 Audio 이름 없이 사용가능.
  - 함수 안에 있으면 그 함수 안에서만 init을 쓸 수 있고, 함수 밖이면 그 밑에 있는 모든 함수들에서 사용가능
- using 선언이나 지시어는 **함수 안 또는 밖**에 만들 수 있다.
- global과 함수 안에 같은 함수가 다른 namespace로 정의되면 이름 충돌(ambiguos error) 발생, 1번 방법이 가장 안전하다. 
  - ::init(); 하면 무조건 글로벌, 에러 안남 
#### 함수를 선언 파일과 구현 파일로 분리할 때 
- 보통 .h에 함수 선언하고, 구현 파일 .cpp 에  #include해서 사용함 
- 함수의 **선언부와 구현부를 모두 namespace로 묶어야 한다.**
``` Audio.cpp
//Audio.cpp
#include "Audio.h"
#include <stdio.h>
namespace Audio{
    void init()
    {
        printf("Audio\n");        
    }
    void reset(){

    }
}
```
```Audio.h
//Audio.h
namespace Audio
{
    void init();
    void reset();
}
```
```main.cpp
//main.cpp
#include "Audio.h"
int main()
{
    Audio::init();
}
```
#### Java package와의 공통점과 차이점
- 공통점
  - naming conflict를 막는다.
- 차이점
  - 한 파일에 namespace를 여러개 더하는 것이 가능하지만 package는 하나에만 속할 수 있다.
  - Java에서 package structure과 directory structure은 동일해야 하지만, namespace는 그럴 필요 없다.
  - Java package는 namespace 역할 뿐만 아니라 access를 control하고, class, interface, enum을 searching/ loacating 한다.
