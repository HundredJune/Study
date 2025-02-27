
JAVA
---
- 자바의 특징
  - OOP(객체 지향 언어, 상속, 캡슐화 등이 가능) : 부품에 해당하는 객체들을 먼저 만들고, 이것들을 하나씩 조립해 전체 프로그램을 완성하는 개발 기법
  - Garbage Collection에 의한 메모리 자동 관리
  - Multi Thread 지원
  - JVM 위에서 동작하기 때문에 특정 OS에 종속적이지 않고 이식성이 좋으며, 보안성이 좋다
  - 다양한 Open 라이브러리들이 존재한다.
  - 클래스 중심으로 프로그래밍. 모든 코드를 클래스에서 짜고 main에서 함수 호출만 함.
  - JAVA는 국제규격의 유니코드 문자집합
  - 소스코드가 줄고, 유지보수가 향상되며 가독성이 좋다.

- 자바를 만든 사람은
  - 제임스 고슬링

- 변수란?
  - 하나의 값을 저장할 수 있는 메모리 공간

- 객체와 클래스의 차이점은?
  - 클래스(Class) : 현실 세계의 객체의 속성과 동작을 추려내 필드와 메서드로 정의한 것으로 "아직 메모리가 할당되지 않은 상태"
  - 객체(Object) : 이 Class라는 설계도를 기반으로 실제 메모리가 잡힌 것을 의미하며 이런 객체를 조합해 전체 프로그램을 완성해 나가는 방식을 OOP(객체지향 프로그래밍)이라고 한다.

- 객체 지향 PG이란? 또 그 특징은?
  - 캡슐화, 은닉화 : 외부 객체에서 구현방식은 알 수 없도록 숨기고 별도로 접근할 수 있는 getter/setter 메서드를 통해 접근하도록 하는 방식
  - 상속 : 부모 Class를 자식이 접근할 수 있도록 물려 받는 방식
  - 다형성 : 부모 클래스 타입으로 해당 부모를 상속받는 여러 자식 class를 대입할 수 있는 성질 등을 들 수 있다.
  - 재사용성이 높다. 

- 다형성이란?
  - 서로 다른 클래스로부터 만들어진 객체지만 같은 부모의 Class 타입으로 이들을 관리할 수 있는 성질

- 자바의 메모리 영역
  - 메서드 영역 : static 변수, 전역변수, 코드에서 사용되는 Class 정보 등이 올라간다.
  - 스택(Stack) : 지역변수, 매개변수, 함수(메서드) 등이 할당되는 LIFO 방식의 메모리
  - 힙(Heap) : new 연산자를 통한 동적할당된 객체들이 저장되며, 가비지 컬렉션에 의해 메모리가 관리되어 진다.

- 추상 메서드? 추상 클래스?
  - 추상 메서드 : 메서드의 정의부만 있고 구현부는 있지 않은 메서드
  - 추상 클래스 : 추상 메서드를 적어도 하나 이상 가지고 있는 클래스로 자식 클래스에서 오버라이딩(재정의)가 필요한 추상메서드를 가지고 있기 때문에 객체화를 할 수 없다.

- 인터페이스란? 왜 사용하나?
  - 인터페이스는 모든 메서드가 구현부가 없는 추상메서드로 이루어진 클래스로, abstract 키워드를 붙이지 않아도 자동으로 모든 메서드는 추상메서드로 정의가 된다. 또한 변수도 자동으로 final static 키워드가 붙게 된다.
  - 팀 작업시 개발코드 부분과 객체가 서로 통신하는 접점 역할을 지원하게 되는데, 이는 개발코드에선 객체의 내부 구조를 모르더라도 인터페이스의 메서드 명만 알고 있으면 되기 때문이다. 이를 통해 얻을 수 있는 장점은 메서드를 통해 나오는 결과물을 알고 이씩 때문에 다른팀의 작업을 기다리지 않아도 되며, 또한 해당 객체가 수정될 경우 개발 코드 부분을 수정하지 않아도 된다.

- 프로세스와 쓰레드의 차이점은?
  - 프로세스 : OS가 메모리 등의 자원을 할당해준 실행중인 프로그램을 가리킨다. 이때 각각의 프로세스는 서로 메모리 공간을 독자적으로 갖기 때문에 서로 메모리 공간을 공유하지 못한다. 공유하기 위해서는 IPC 같은 방식이 필요하다.
  - 쓰레드 : 쓰레드는 프로세스 내에서 프로세스의 자원을 가지고 실제로 일하는 "일꾼"과 같으며 각 쓰레드는 독자적인 Stack 메모리를 갖고 그 외의 자원은 프로세스 내에서 공유하게 된다.

- CollectionFramework에 대해 말해보세요.
  - List 인터페이스 : 배열과 유사하되, 추가할때 마다 자동으로 Boundary를 늘려주는 구조로, 중복된 데이터를 허용하며, 순서가 존재한다.
    - ArrayList : 배열로 구현되었으며, 인접해 있기 때문에 데이터 조회가 매우 빠르다 하지만, 빈번한 삽입, 삭제시 새로 배열을 만들고 옮겨야 하기 때문에 LinkedList에 비하여 속도가 느리다.
    - LinkedList : 링크 구조로 되어 있기 때문에 조회는 ArrayList에 비해 느리지만, 삽입 삭제시 링크를 끊고 새로 추가되는 데이터에 링크만 연결하면 되기 때문에 삽입, 삭제에 유리하다.
    - Vector : 구현 방식은 ArrayList와 유사하지만 Vector를 개선한 것이 ArrayList이다. 또한 Vector의 경우에는 ArrayList와 달리 Synchronized가 걸려 있어 여러 쓰레드에서 동시에 접근할 수 없다.
  - Set 인터페이스 : 집합처럼 중복된 데이터를 허용하지 않으며, 순서가 없다. 또한, 객체 내부의 중복된 데이터를 배제하고 싶은 경우 Object 클래스의 equals 메서드와 hashCode 메서드의 재정의가 반드시 필요하다.
      - HashSet
      - TreeSet : 순서가 있는 HashSet으로 이진 트리 구조로 만들어 졌다. 순서에 맞게 정렬되어 저장되기 위해서 Comparable을 구현해야 한다.
      - LinkedHashSet : set에 대해서 순서를 보장한다.
   - Map 인터페이스 : key와 value 쌍으로 데이터를 저장하며, key는 중복될 수 없고, value는 중복 저장이 가능하다.
      - HashSet
      - TreeSet
      - Properties : key value 쌍으로 저장되지만 value의 타입이 String만 가능하다.
      - Hashtable : HashMap과 구조는 같으며, 단지 Synchronized(동기화) 되어져 있따는 점이 다른점이다.
      - LinkedHashMap : key에 대해서 순서를 보장한다.
    - Stack과 Queue
      - Stack 객체는 직접 new 키워드로 사용할 수 있으며, Queue인터페이스는 JDK 1.5부터 LinkedList에 new 키워드를 적용하여 사용 할 수 있다.

- 쿠키와 세션의 공통점과 차인점은?
  - 공통점 : 둘 다 사용자의 데이터를 저장한다.
  - 차이점
    - 쿠키 : 쿠키는 Client 컴퓨터에 저장했다 서버 요청시 네트워크를 타고 서버로 전달되기 때문에 보안에 취약하다. 속도가 빠르다. 파일로 저장되기 때문에 브라우저를 종료해도 계속해서 정보가 남아 있을 수 있다.
    - 세션 : 세션은 서버에 저장되고 부라우저 단위로 관리된다. 캐시에 비해 보안성이 좋다. 브라우저가 종료되면 삭제된다. 
    
- Final keyword
  - final class : 다른 클래스에서 상속하지 못한다.
  - final method : 다른 메소드에서 오버라이딩하지 못한다.
  - fianl variable : 변하지 않는 상수값이 되어 새로 할당할 수 없는 변수가 된다.
  - 혼동 할 수 있는 두 가지
    - finally : try-catch 구문을 사용할 때, 마무리 해줘야하는 작업이 존재하는 경우에 해당하는 코드를 작성해주는 코드 블록이다.
    - finalize() : 메소드로써 GC에 의해 호출되는 함수로 절대 호출해서는 안 되는 함수이다.


- Request 전송 방식에는 어떤 것들이 있는지 아시나요?
  - Get 방식 : URL의 쿼리문자열에 데이터를 같이 전달하는 방식으로 데이터 길이에 제한이 있고, 보안에 취약하다.
  - Post 방식 : 헤더에 데이터를 넣어 보내기 때문에 보안에 조금 더 유리하고 데이터 길이에 제한이 없다. 하지만 Get에 비해 다소 느리다.
  - DELETE 방식 : RESTFUL에서 삭제 기능을 할 때 주로 사용된다.
  - PUT/PUSH 방식 : RESTFUL에서 수정 작업을 할 때 주로 사용된다.

- RESTFUL이란?
  - 해당 URL만 보더라도 바로 어떤 작업을 하는지를 알 수 있도록 하나의 데이터는 하나의 URL을 갖도록 작업하는 방식
  - 리소스는 URL로 표현되는데 리소스가 가리키는 것은 명사로 표현되어야 한다.
  - 행위는 HTTP Method로 표현하고, Get(조회), POST(생성), PUT(기존 entity 전체 수정), PATCH(기존 entity 일부 수정), DELETE(삭제)을 분명한 목적으로 사용한다.
  - Open API를 제공하기 쉽다. 멀티플랫폼 지원 및 연동이 용이하다. 원하는 타입으로 데이터를 주고 받을 수 있다. 기존 웹 인프라를 그대로 사용할 수 있다.
  - 사용할 수 있는 메소드가 4가지 밖에 없다.

- Spring에서 DI란?
  - DI는 의존성 주입이라는 말로, 객체들 간의 의존성을 줄이기 위해 사용되는 Spring의 IOC 컨테이너의 구체적인 구현 방식입니다. DI는 기존처럼 개발코드 부분에서 객체를 생성하는 것이 아니라, 팩토리 패턴처럼 객체의 생성과, 데이터를 주입만 담당하는 Factory에 해당 하는 별도의 공간에서 객체를 생성하고 데이터간의 의존성을 주입해 개발코드에서는 이를 가져다 씀으로써 의존성을 줄이는 방식입니다. Factory 패턴의 Factory Class의 역할을 스프링의 환경설정 파일이 담당합니다. 

- Spring에서 AOP란?
  - AOP는 Aspect Oriented Programming 관점 지향 프로그래밍의 약자로, 기존 OOP(객체 지향 프로그래밍)에서 기능별로 class를 분리했음에도 불구하고, 여전히 로그, 트랜잭션, 자원해제, 성능테스트 메서드 처럼 공통적으로 반복되는 중복코드가 여전히 발생하는 단점을 해결하고자 나온 방식으로 이러한 공통 코드를 "횡단 관심사"라 표현하며 개발코드에서는 비니스 로직에 집중하고 실행시에 비즈니스 로직 앞, 뒤 등 원하는 지점에 해당 공통 관심사를 수행할 수 있게 함으로서 중복 코드를 줄일 수 있는 방식입니다.
  
- Filter와 Interceptor 방식의 차이?
  - 싱글톤(SingleTone Pattern) : 대표적으로 Calender 객체나 dataSource 객체처럼 객체가 하나만 생성되어야 하는 경우 전체 코드에서 하나의 객체만 존재할 수 있도록 이미 생성된 객체가 있으면 그 객체를 사용하도록 하는 방식입니다.
  - 팩토리 패턴(Factory Pattern) : 객체간 의존성을 줄이기 위해 객체의 생성과 데이터 주입만 담당하는 Factory Class를 정의하는 개발 코드 부분에서는 생성된 객체를 가져다 사용함으로서 의존성을 줄이는 방식입니다.
  - 옵저버 패턴(Observer Pattern) : 기후 정보처럼 RSS 수신시 하나의 객체가 변하면 다른 객체에 객체가 변했다는 사항을 알려주어야 할 경우에 주로 사용합니다.
  
- MVC 패턴이란?
  - Model : data 처리와 접근을 담당
  - View : Client에 보여지는 화면을 담당
  - Controller : Model과 View를 제어
  - 세가지 부분으로 나눔으로서, 데이터와 화면간의 의존관계를 벗어날 수 있게 하는 개발 기법입니다.
  
- 프로젝트 개발 순서?
  1. 요구사항 분석
      - 기획 및 스토리 보드 작성
  2. WBS(Work Breakdown Structure) 작성 : 작업 분해도로 프로젝트 범위와 최종산출물을 세부요소로 분할한 계층적 구조도
  3. 논리 ERD 작성
  4. 물리 ERD 작성
  5. 개발
  6. Testing
  7. 유지보수
 
- 오버로딩과 오버라이딩의 차이?
  - 오버로딩 : 메서드명은 동일하지만. 매개 변수 타입과 개수를 다르게 해 선언하는 방식
  - 오버라이딩 : 상속한 자식에서 부모의 메서드를 재정의하는 방식

- Servelt vs JSP
  - Servlet : 자바 언어로 웹 개발을 위해 만들어진 것으로, Container가 이해할 수 있게 구성된 순수 자바 코드로만 이루어진 것
  - JSP : html 기반에 JAVA 코드를 블록화하여 삽입한 것으로 Servlet을 좀 더 쉽게 접근할 수 있또록 만들어 진 것
  
- Wrapper Class의 사용 이유를 아나요?
  - 기본 data 타입은 객체가 아니어서 Object로 받는 다형성을 지원할 수가 없다. 하지만, 메서드에서 실제로 기본데이터 타입을 다형성으로 넘겨주어야 하는 경우가 빈번히 발생하는데 이때, 기본 데이터 타입을 객체로 변환시켜 전달하기 위해 사용된다.
  - Integer, Float, Boolean 등이 Wrapper class의 예이다. 
  - null 값을 반환해야만 하는 경우에는 return type을 Wrapper Class로 지정하여 null을 반환하도록 할 수 있다.
  
- Field member
  - 필드란 클래스에 변수를 정의하는 공간을 의미한다. 이곳에 변수를 만들어두면 메소드 끼리 변수를 주고 받는 데 있어서 참조하기 쉽다. 하지만 객체가 여러 스레드가 접근하는 싱글톤 객체라면 field에서 상태값을 갖고 있으면 안된다. 모든 변수는 parameter로 넘겨받고 return 하는 방식으로 코드를 구성해야 한다.
  
- 동기화(Synchronized)
  - 스레드 간 race condition을 통제한다.
  - List를 대신하여 Vector를 사용할 수 있고, Map을 대신하여 HashTable을 사용할 수 있다.
  - Collections라는 util클래스에서 제공되는 static 메소드를 통해 이를 해결할 수 도 있다.
  
- DB에서 Index란?
  - Table에 대한 동작 속도를 높여주는 자료구조로서 빠른 검색을 가능하게 해준다.
  
- Private, Protected, Public, Default 제어자에 대해 설명해 보시오
  - private : 같은 class 내부에서"만" 접근이 가능하다.
  - public : 어디서든 자유롭게 접근이 가능하다.
  - protected : 같은 class 내부 + 상속받은 자식에서는 부모 class에 접근이 가능하다.
  - default : 아무 것도 선언하지 않은 경우로 같은 패키지 내부에서만 접근이 가능하다.

- SW 개발시 가장 비중을 크게 두어야 할 부분은 어디라고 생각하나요?
  - Testing 부분입니다.
  
- 자바의 제네릭이란?
  - 클래스 내부에서 사용할 데이터 타입을 인스턴스(객체) 생성시에 결정짓는 방식
  - 객체의 타입 안정성을 높이고 형변환의 번거로움을 줄여준다. 코드도 더 간결해진다.
  - 예를 들면. Collection에 특정 개체만 추가될 수 있도록, 또는 특정한 클래스의 특징을 갖고 있는 경우에만 추가 될 수 있도록 하는 것이 제네릭이다.
  
- CVS나 SVN에 대해서 아는대로 설명해 보시오.

- 64bit CPU와 32bit CPU의 OS적 관점에서의 차이를 설명해 보시오.

- '데드락'이란 무엇이고 이를 해결하기 위한 방법을 설명해 보시오.

- 변수 명명법이 중요한 이유에 대해서 설명하고 예를 들어 보시오.

- 자바 JVM의 역할에 대해서 설명해 보시오.

- Linux에서 톰캣 환경설정을 잡는 것에 대해 설명해 보시오.

- WAS와 웹서버의 차이점은?

- Jquery와 Ajax에 대해 아는가?

- 비동기와 동기 방식의 차이점에 대해 말해보시오.

- 개발시에 중요하다 생각하는 요소를 3가지 기술해 보시오.

- 스프링 MVC에 대해서 설명하시오.

- '에자일'방법론에 대해서 아는가?

- 스프링 환결설정 혼자 잡을 수 있는가? 대강 어떻게 해야하는지 설명해 보시오.

- 웹서버 내부 구동 방식에 대해 설명할 수 있는가?

- UML 그려본 적 있는가?

- Node.js나 Angular JS를 사용해 본 적이 있는가?

- 크롬이나 파이어폭스에서 개발도구를 사용해 디버깅을 해보았는가?

- JDBC는 무엇인가?

- 스프링을 사용하지 않고 MVC를 JSP에서 만들어 보았는가?

- DB 옵티마이저에 대해 아는가?

자료구조
---
- Array Vs LinkedList
  - Array
    - random access 가능
    - 삭제, 삽입 과정에서 shift해줘야 하는 비용이 발생하고 이 경우의 시간 복잡도는 O(n)가 된다. 
  
  - LinkedList
    - 삭제와 삽입을 O(1)만에 해결할 수 있다.
    - search를 하는데 O(n)의 시간이 걸린다.
  
- Stack & Queue
  - Stack : LIFO
  - Queue : FIFO, Priority queue

- Tree
  - Node : 트리를 구성하고 있는 각각의 요소를 의미한다.
  - Edge : 트리를 구성하기 위해 노드와 노드를 연결하는 선을 의미한다.
  - Root Node : 트리 구조에서 최상위에 있는 노드를 의미한다.
  - Terminal Node : 하위에 다른 노드가 연결되지 않은 노드를 의미한다.
  - Internal Node : 단말 노드를 제외한 모든 노드로 루트 노드를 포함한다.

  - BST(Binary Search Tree)
    1. 이진 탐색 트리의 노드에 저장된 키는 유일하다.
    2. 루트 노드의 키가 왼쪽 서브 트리를 구성하는 어떠한 노드의 키보다 크다.
    3. 루트 노드의 키가 오른쪽 서브 트리를 구성하는 어떠한 노드의 키보다 작다.
    4. 왼쪽과 오른쪽 서브트리도 이진 탐색 트리이다.
    5. O(log n)의 시간 복잡도를 갖는다. 
    6. 편향트리를 가지는 Worst Case의 경우 시간 복잡도는 O(n)이 된다.

  - Binary Heap
    - Max Heap
       - 각 노드의 값이 해당 children의 값보다 크거나 같은 tree
    - Min Heap
      - 각 노드의 값이 해당 children의 값보다 크거나 같은 tree
  
  - Red Black Tree
    - BST를 기반으로 하는 트리 형식의 자료구조이다. Search, Insert, Delete에 O(log n)의 시간 복잡도가 소요된다. 동일한 노드의 개수일 떄, depth를 최소하하여 시간 복잡도를 줄이는 것이 핵심 아이디어이다.
    - 각 노드는 Red or Black이라는 색깔을 갖는다.
    - Root node의 색깔은 Balck이다.
    - 각 leaf node는 black이다.
    - 어떤 노드의 색깔이 red라면 두 개의 children의 색깔은 모두 balck이다.
    - 각 노드에 대해 노드로부터 descendant leaves 까지의 단순 경로는 모두 같은 수의 black nodes 들을 포함하고 있다.
    - BST의 삽입과 삭제 연산 과정에서 문제점을 해결하고 크기 비율이 2미만으로 유지된다.  
    
  - DFS는 미로찾기 / BFS 최단 경로
  
  - 최소 비용 신장 트리(Kruskal Algorithm & Prim Algorithm)
    - Kruskal : 전체에서 가장 작은 것을 선택하고 써클이 생기는지 안생기는지 확인
    - Prim : 한개의 Vertex에서 가장 최선의 선택을 통하여 찾아가는 알고리즘
