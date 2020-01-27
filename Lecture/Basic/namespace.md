## namespace.md
#### namespace의 필요성
- 하나의 프로그램은 **수십 수백개**의 파일로 구성될 수 있고 수십명의 개발자가 같이 작업 할 수도있다.
- 함수 및 구조체 등의 **이름 충돌** 이 발생할 수 있다.
#### namespace의  장점
- 프로그램의 **다양한 요소(함수, 구조체 등)을 연관된 요소끼리 묶어서 관리** 할 수 있다.
- 기능별로 다른 이름 공간을 사용함으로써 **함수/구조체 등의 이름 충돌을 막을 수** 있다.
#### namespcae에 있는 요소에 접근하는 3가지 방법
- 1. **한정된 이름(qulified name)**을 사용하는 방법
  - Audio::init();
- 2. Using 선언(declaration)을 사용한 접근
  - using Audio::init;
- 3. Using 지시어(directive)을 사용한 접근
  - using namespace Audio; 
#### Java package와의 공통점과 차이점
- 공통점
  - naming conflict를 막는다.
- 차이점
  - 한 파일에 namespace를 여러개 더하는 것이 가능하지만 package는 하나에만 속할 수 있다.
  - Java에서 package structure과 directory structure은 동일해야 하지만, namespace는 그럴 필요 없다.
  - Java package는 namespace 역할 뿐만 아니라 access를 control하고, class, interface, enum을 searching/ loacating 한다.
