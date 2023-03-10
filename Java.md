### 자바

- Call by value vs Call by reference
    - 자바 자료형의 종류를 얘기하고, 각 자료형의 예시를 들어보세요.
        
        자바에는 Primitive Type과 Reference Type이 존재합니다. Primitive Type에는 int, short, long, float, double, char, boolean이 존재하며 Reference Type는 String을 포함해 그 외의 자료형들이 존재합니다. 
        
    - 자바는 Call by value와 Call by reference중 무엇인가요?
        
        Call by value
        
    - 자바에서 타입이 기본형인 경우, 어떤 일이 발생하는지 말해보세요
        
        자바에서는 함수의 인자로 전달되는 타입이 기본형인 경우 값을 넘기게 되어있습니다. 이 경우 메모리에는 함수를 위한 별도의 공간이 생성되고 이는 함수 종료시 사라집니다. 따라서 원본값은 변하지 않습니다.
        
    - 기본형의 특징을 말해보세요
        
        변수에 값 자체를 저장하므로 stack 영역에 생성됩니다. 사용하기 전에 반드시 선언되어야 하고, 초기화를 하지 않으면 자료형에 맞는 기본값이 들어갑니다. OS에 따라 자료의 길이가 변하지 않고, 비객체 타입이므로 NULL을 가질 수 없습니다.
        
    - 자바에서 타입이 참조형인 경우, 어떤 일이 발생하는지 말해보세요
        
        변수가 가지는 값이 주소값이므로, Call by value에 의해 주소값이 전달됩니다. 따라서 함수 안에서 해당 인자의 값을 변경하게 되면 원본 값도 바뀌게 됩니다.
        
        메모리 상에서 객체가 존재하는 주소를 저장하며, heap 영역에 저장합니다. 클래스형, 인터페이스형, 배열형이 있습니다.
        
- String, StringBuilder, StringBuffer
    - String의 장점은 무엇인가요?
        
        불변 객체이기 때문에 멀티스레드 환경에서 동기화를 신경쓰지 않아도 됩니다.
        
    - StringBuilder, StringBuffer의 공통점은 무엇인가요?
        
        String과 다르게 변할 수 있는 객체입니다.
        
    - StringBuilder, StringBuffer의 차이점은 무엇인가요?
        
        StringBuilder는 thread safe하지 않고, StringBuffer는 thread safe합니다.
        
- Wrapper 클래스
    - Wrapper 클래스는 어떨때 사용됩니까?
        
        기본 자료형을 객체 타입의 자료형으로 변환해야 할 때 사용합니다.
        
        예시로 제네릭이나 컬럭센을 사용할 경우 기본형을 쓸 수 없기 때문에 Wrapper 형태를 사용해야 합니다.
        
    - Wrapper 객체의 특징에는 무엇이 있습니까?
        
        산술 연산을 위한 클래스가 아니기에 불변객체 입니다.
        
    - 박싱과 언박싱은 각각 무엇입니까?
        
        박싱은 기본 자료형을 Wrapper class로 변환하는 것이고, 언박싱은 그 반대입니다.
        
    - 박싱과 언박싱의 관점에서 parseInt()와 valueOf()에 관해 설명해보세요
        
        모두 int의 Wrapper 클래스인 Integer의 메서드입니다. parseInt()는 문자열을 기본형으로 변환하고, valueOf()는 문자열을 Wrapper 클래스로 변환합니다.
        
        하지만 JDK 1.5부터 오토 박싱과 오토 언박싱이 지원되기에 두 메서드를 구별하지 않고 사용이 가능합니다.
        
- 인터페이스
    - 인터페이스에 포함될 수 있는 요소는 무엇인가요?
        
        추상메소드와 상수만 멤버로 가질 수 있습니다.
        
        JDK 1.8부터 static 메서드와 디폴트 메서드도 가능합니다.
        
    - 인터페이스에 제약사항이 따로 있나요?
        
        모든 멤버변수는 public static final이어야 하고 생략 가능합니다.
        
        모든 메서드는 public abstract이어야 하고 생략 가능합니다.
        
    - 자바에서는 클래스의 다중 상속이 안되는데, 그 이유가 무엇인가요?
        
        메서드 출처에 모호성이 생기기 때문입니다.
        
    - 그렇다면 왜 인터페이스의 다중 상속은 가능한가요?
        
        여러 인터페이스를 동시에 구현한 클래스 하나에서만 메서드를 재정의하므로, 메서드 출처에 모호성이 사라지기 때문입니다.
        
    - 인터페이스의 디폴트 메서드는 오버라이딩이 가능한가요?
        
        네 가능합니다. 디폴트 메서드는 인터페이스의 공통 부분을 선택적으로 사용할 수 있도록 추가됐습니다.
        
    - 인터페이스에 static 메서드가 추가된 이유는 무엇인가요?
        
        모든 인터페이스가 동일한 구현부를 가지는 메서드를 공유하기에 유틸리티성 인터페이스로 동작할 수 있게 하기 위해서입니다.
        
    - 인터페이스와 추상클래스 중 공유의 목적에 더 가까운 것은 무엇입니까?
        
        추상클래스
        
- 변수의 종류와 메모리 구조
    - 하나의 메모리에 대해 낮은 주소부터 높은 주소까지 순차적으로 어떤 영역이 위치하는지 말해보세요
        
        메서드 영역, 힙 영역, 스택 영역이 위치합니다
        
    - 메서드 영역에는 어떤 데이터가 위치하나요?
        
        클래스에 대한 정보와 함께 클래스 변수, 즉 static 변수가 위치합니다.
        
        JVM은 자바 프로그램에서 특정 클래스가 사용되면 해당 클래스의 클래스 파일을 읽어들여 클래스에 대한 정보를 메서드 영역에 저장합니다.
        
    - 힙 영역에는 어떤 데이터가 위치하나요?
        
        모든 인스턴스 변수가 위치합니다. 
        
        new 키워드를 사용해 인스턴스가 생성되면 해당 인스턴스의 정보를 힙 영역에 저장합니다.
        
        힙 영역은 메모리의 낮은 주소에서 높은 주소의 방향으로 할당된다는 특징이 있습니다.
        
    - 스택 영역에는 어떤 데이터가 위치하나요?
        
        메서드, 지역변수, 매개변수가 위치합니다. 메서드 호출 시 메서드 호출과 관계되는 매개변수와 지역 변수를 스택에 저장합니다. 이를 스택 프레임이라고 부릅니다.
        
        후입 선출의 구조를 갖고 있으며 메모리의 높은 주소에서 낮은 주소의 방향으로 할당됩니다.
        
- 리플렉션
    - 자바의 리플렉션이란 무엇인가요?
        
        컴파일 타임이 아니라 런타임에 동적으로 특정 클래스의 정보를 객체화하여 분석 및 추출할 수 있는 프로그래밍 기법입니다. 자바에서는 기본적으로 api로 제공하고 있습니다.
        
        리플렉션을 통해 클래스, 생성자, 메서드, 멤버변수에 대한 정보를 얻을 수 있고 이 정보를 가져와서 객체를 생성하거나 메서드를 호출하거나 변수의 값을 변경할 수 있습니다.
        
        ```java
        Class clazz = Class.forName("test.Child");
        Constructor constructor = clazz.getDeclaredConstructor();
        System.out.println("Constructor: " + constructor.getName());
        ```
        
        [https://codechacha.com/ko/reflection/](https://codechacha.com/ko/reflection/)
        
    - 리플렉션을 사용할 때의 장점은 무엇인가요?
        
        런타임에 다른 클래스에 접근할 수 있습니다. 물론 리플렉션이 필수적인 것은 아니지만 조금 더 유연한 코드를 만들 수 있습니다.
        
    - 리플렉션을 사용할 때 주의할 점은 무엇인가요?
        
        private 멤버도 특정 메서드를 통해 true로 지정하면 접근과 조작이 가능하기 때문에 주의해서 사용해야 합니다. 또한 동적인 부분이 포함되므로 특정 JVM 최적화를 수행할 수 없습니다. 따라서 성능에 민감한 애플리케이션에서 자주 호출되는 곳엔 사용하지 않아야 합니다.
        
- 가비지 컬렉션
    - 자바 GC의 전체적인 동작 방식에 대해 말해보세요
        
        우선 새로 생성된 대부분의 객체는 Eden 영역에 위치합니다. Eden 영역이 꽉 차게 되면 GC가 발생하고, 이 이후 살아남은 객체는 Survivor 영역 중 하나로 이동합니다. 이 과정을 반복하다가 계속해서 살아남은 객체는 일정 시간 참조되고 있다는 뜻이므로 Old 영역으로 이동합니다.
        
        이후 Old 영역에 있는 모든 객체들을 검사하여 참조되고 있지 않은 객체들을 한꺼번에 삭제합니다. 이는 시간이 오래 걸리고 실행 중 프로세스가 정지되는데, GC를 실행하는 스레드를 제외한 나머지 스레드는 모두 작업을 멈춥니다. GC의 튜닝이란 이 시간을 줄이는 것입니다.
        
    - GC는 어떤 원리로 소멸시킬 대상을 선정하나요?
        
        알고리즘에 따라 동작 방식이 매우 다양하지만 공통적인 원리가 있습니다. GC는 힙 내의 객체 중 가비지를 찾아내고 이를 처리해 힙의 메모리를 회수합니다. 빈번한 GC의 실행은 시스템에 부담이 될 수 있기 때문에 GC의 실행 타이밍을 정하는 것에 여러 알고리즘이 사용됩니다.
        
    - 가비지란 무엇인가요?
        
        참조되고 있지 않은 객체를 가비지라고 합니다. 이를 판단하기 위해서 Reachability라는 개념을 사용합니다. 객체 참조는 사슬로 연결될 수 있기에 사슬 전체를 확인합니다.
        
    - 객체가 가비지 컬렉션의 대상이 될 경우 바로 소멸되나요?
        
        아니요. 빈번한 가비지 컬렉션의 실행은 시스템에 부담이 될 수 있기 때문에 가비지 컬렉션의 실행 타임밍은 별도의 알고리즘을 기반으로 계산이 됩니다. 
        
- 스레드
    - 멀티 태스킹이 무엇이고 진행 과정을 프로세스와 연결지어 말해주세요
        
        멀티 태스킹이란 두 가지 이상의 작업을 동시에 하는 것을 말합니다. 이를 위해선 프로세스가 필요한데, 실제로 동시에 처리될 수 있는 프로세스의 개수는 CPU 코어의 개수와 동일합니다. 하지만 이보다 많은 개수의 프로세스가 존재하기 때문에 각 코어들을 아주 짧은 시간 동안 여러 프로세스를 번갈아가며 처리하는 방식을 통해 동시에 동작하게 보이게 합니다.
        
    - 자바에서 스레드를 구현하는 방법과 각각의 특징에 대해 모두 말해보세요
        
        우선 Runnable 인터페이스를 구현하는 방법이 있습니다. 이는run() 메서드를 오버라이드합니다. 하지만 이는 start() 메서드가 없기 때문에 Runnable 인터페이스를 구현한 클래스의 객체를 만들어 스레드를 생성할 때, 생성자의 매겨변수로 넘겨주고 스레드 객체의 start() 메서드를 수행해야 합니다.
        
        다음으로는 Thread 클래스를 상속받는 방법이 있습니다. 이는 run() 메서드를 직접 구현해야 합니다. 또한 Thread 클래스를 상속받으면 스레드 클래스의 메서드를 바로 사용할 수 있지만 Runnable 구현의 경우 Thread 클래스의 static 메서드인 currentThread()를 호출해 현재 스레드에 대한 참조를 얻어와야만 호출이 가능합니다.
        
    - 스레드는 어떻게 실행하나요?
        
        run() 호출이 아닌 start() 호출로 해야합니다. 
        
        자바에는 Call Stack이라는 실질적인 명령을 담고 있는 메모리가 있는데 명령을 하나씩 꺼내서 실행시키는 역할을 합니다. 만약 동시에 두 가지 작업을 한다면 두 개 이상의 콜 스택이 필요하게 됩니다. 즉, 스레드를 이용한다는 건 JVM이 다수의 콜 스택을 번갈아가며 일처리를 하고 사용자에게는 동시에 작업을 하는 것처럼 보여주는 것입니다.
        
        즉, run() 메서드를 사용한다는 것은 main()의 콜 스택 하나만 이용하는 것으로 스레드 활용이 아닙니다. 이와 달리 start() 메서드를 호출하면 JVM은 알아서 스레드를 위한 Call Stack을 새롭게 만들어주고, 컨텍스트 스위칭을 통해 스레드답게 동작하도록 해줍니다. 
        
        결국 새로운 콜 스택을 만들어 작업을 해야 스레드 일처리가 되는 것이기에 start()를 써야 실행이 가능한 것입니다.
        
    - 스레드의 상태들에 대해 말해주세요
        
        스레드는 총 5가지 상태를 갖고 있습니다.
        
        NEW란 스레드가 생성되고 아직 start()가 호출되지 않은 상태입니다.
        
        RUNNABLE란 start()가 호출되어 스레드가 실행중이거나 실행 가능한 상태입니다.
        
        BLOCKED란 동기화 블록에 의해 일시정지된 상태로 lock이 풀릴 때까지 기다리는 상태입니다.
        
        WAITING/TIME_WAITING란 실행이 가능하지 않은 일시정지 상태를 의미합니다.
        
        TERMINATED란 스레드 작업이 종료된 상태입니다.
        
    - 스레드의 스케쥴링과 관련된 메서드에는 어떤 것들이 있나요?
        
        sleep(), join(), yield(), interrupt()가 있습니다.
        
- String
    - 자바에서 String을 생성하는 방식과 각각의 차이점에 대해 모두 말해보세요
        
        new 연산자를 이용한 방식과 리터럴을 이용한 방식이 있습니다. new를 통해 String 객체를 생성하면 Heap 영역에 존재하게 됩니다.리터럴을 이용할 경우 String Constant Pool이라는 영역에 존재하게 됩니다. 
        
    - new를 이용했을 때와 리터럴을 이용했을 때 각 ==, equals()로 비교를 할 경우 결과가 어떻게 나타나나요?
        
        ==로 비교했을 때는 다름, equals()로 비교했을 때는 같음으로 나타납니다.
        
    - 왜 == 로 비교했을때는 다른가요?
        
        String을 리터럴로 선언할 경우 내부적으로 String의 intern()이라는 메서드가 호출됩니다. intern()은 주어진 문자열이 String Constant Pool에 존재하는지 검색하고 있다면 그 주소값을 반환하고 없다면  String Constant Pool에 넣고 새로운 주소값을 반환하게 됩니다.
        
    - String Constant Pool은 그럼 메모리상에 어디에 위치하는 건가요?
        
        Perm 영역에 위치했습니다. 하지만  Perm은 고정된 사이즈이며 실행시 사이즈가 확장되지 않기 때문에 String의 intern() 메서드를 호출할 경우 OOM을 발생시킬 수 있었습니다. 따라서 힙 영역으로 위치가 변경되었고, 이를 통해 String Constant Pool의 모든 문자열도 가비지 컬렉션의 대상이 될 수 있다는 이점을 얻었습니다.
        
- JVM
    - JVM이란 무엇인지 설명해보세요
        
        자바 애플리케이션을 클래스 로더를 통해 읽어들여 자바 API와 함께 실행하게 하는 스택 기반의 가상 머신입니다.
        
    - 왜 자바 프로그램은 JVM 위에서 돌아가나요?
        
        JVM은 자바와 OS 사이에서 중개자 역할을 수행하여 자바가 OS에 구애받지 않고 재사용을 할 수 있게 합니다. 즉, 자바 바이트 코드를 실행할 수 있는 주체입니다. 또한 메모리 관리, GC등을 수행해 자바 프로그램 실행 과정의 전반을 관리합니다.
        
    - 왜 JVM을 알아야 하나요?
        
        메모리는 한정되어있기 때문에 JVM을 이해함으로써 이를 최적화 할 수 있습니다.
        
    - 자바 프로그램 실행 과정에 대해 설명해보세요
        
        프로그램이 실행되면 JVM은 OS로부터 이 프로그램이 필요로 하는 메모리를 할당받습니다. JVM은 이 메모리를 용도에 따라 여러 영역으로 나누어 관리합니다.
        
        자바 컴파일러(javac)가 자바 소스코드를 읽어들여 자바 바이트 코드(.class)로 변환시킵니다.
        
        클래스 로더를 통해 클래스 파일들을 JVM으로 로딩합니다.
        
        로딩된 클래스 파일들은 Execution Engine을 통해 해석됩니다.
        
        해석된 바이트코드는 런타임 데이터 영역에 배치되어 실질적인 수행이 이루어지게 됩니다. 이러한 실행 과정 속에서 JVM은 필요에 따라 스레드 동기화와 가비지 컬렉션 같은 관리 작업을 수행합니다.
        
    - 클래스 로더란 어떤 역할을 하나요?
        
        런타임시 즉 클래스를 처음으로 참조할 때, JVM내로 .class 파일을 로드하고 링크를 통해 배치하는 작업을 수행합니다.
        
        사용하지 않는 클래스들은 메모리에서 삭제하는 등의 동적 로드를 담당합니다.
        
    - 실행엔진이란 어떤 역할을 하나요?
        
        클래스를 실행시키는 역할을  합니다. 클래스 로더가 JVM내의 런타임 데이터 영역에 바이트 코드를 배치시키고 이것은 실행 엔진에 의해 실행됩니다. 자바 바이트코드란 비교적 인간이 보기 편한 형태로 기술된 것인데, 실행 엔진은 이같은 바이트코드를 실제로 JVM 내부에서 기계가 실행할 수 있는 형태로 변경합니다. 이는 바이트코드를 명령어 단위로 읽어서 실행하여 수행됩니다.
        
        이는 한줄씩 실행하여 속도가 느린 인터프리터 방식과 이 방식을 보완하기 위해 등장한 JIT(just in time) 컴파일러 방식으로 나뉩니다. jit는 인터프리터 방식으로 실행하다가 적절한 시점에 바이트코드 전체를 컴파일하여 네이티브 코드로 변환하고 이를 캐시에 보관해 한번 컴파일된 코드를 빠르게 수행하는 방식입니다. 따라서 해당 메서드가 얼마나 자주 수행되는지에 따라 컴파일을 실행하는 것이 좋습니다.
        
    
    (참고 : 가비지 컬렉터도 여기 존재)
    
    - 런타임 데이터 영역의 역할과 구성 요소에 대해 말해주세요
        
        JVM이 프로그램을 수행하기 위해 OS로부터 할당받은 메모리 공간으로, 용도에 따라 여러 영역으로 나누어 관리합니다.
        
        크게 나눠보자면 스레드, 힙, 메서드 영역으로 나뉩니다. 
        
    - 스레드 영역에는 어떤 것들이 있고, 각각의 역할은 무엇인가요?
        
        스레드 영역에는 PC 레지스터, JVM 스택 영역, Native Method Stack이 존재합니다. PC 레지스터는 스레드가 시작될 때 각각의 스레드별로 생성되는 공간으로 현재 수행중인 JVM 명령어 주소를 가지게 됩니다. JVM 스택 영역은 프로그램의 실행 과정에서 임시로 할당되었다가 메서드를 빠져 나가면 바로 소멸되는 특성의 데이터를 담기 위한 영역입니다. 예시로 메서드의 매개변수, 지역 변수 등 메서드의 정보가 담깁니다. Native Method Stack은 자바외의 언어로 작성된 네이티브 코드를 위한 영역입니다. 자바 프로그램이 컴파일되어 생성되는 바이트 코드가 아닌 실제 실행할 수 있는 기계어로 작성된 프로그램을 실행시키는 영역입니다.
        
    - 메서드 영역의 역할은 무엇인가요?
        
        클래스 정보를 처음 메모리 공간에 올릴 때, 초기화 되는 대상을 담기 위한 메모리 공간입니다. 모든 쓰레드가 공유하는 메모리 영역으로 클래스, 인터페이스, 메서드, 필드, Static 변수 등의 바이트코드를 보관합니다. Runtime Constant Pool이라는 것이 존재하며 이는 별도의 관리 영역으로 상수 자료형을 담아 참조하고 중복을 막는 역할을 수행합니다. 하지만 자바 7부터 이는 메서드 영역이 아닌 힙으로 변경되었습니다.
        
    - 힙 영역의 역할은 무엇인가요?
        
        힙 영역은 런타임시 동적으로 할당하여 사용하는 영역으로, new 연산자로 생성된 객체와 배열을 담는 가상 메모리 공간입니다. 클래스 영역에 올라온 클래스들만 객체로 생성할 수 있고, new/young 영역, old 영역, permanent generation 영역으로 나뉩니다. 
        
    - permanent generation는 어떤 역할을 하나요?
        
        Old 영역에서 살아남은 객체가 영원히 남아있는 곳이 아닌, 리플렉션을 사용해 동적으로 클래스가 로딩되는 경우 사용됩니다.
        
- 자료형
    - char, short 형이 연산의 효율이 떨어지는 이유는 무엇인가요?
        
        int 형보다 작은 크기의 데이터로 연산을 진행할 경우 int 형으로 타입 캐스팅되기 때문입니다. 
        
    - Integer와 int를 size 측면에서 비교해보세요
        
        Object는 8 바이트, Integer는 16 바이트, int는 4 바이트, Integer를 참조하는데 4 바이트가 사용됩니다.
        
- equals()
    - 최적의 방법으로 equals 메서드를 구현해보세요
        
        매개변수로 객체가 들어오기에 우선 같은 객체인지 비교합니다. 이는 = 연산자가 주소를 비교하기에 가능합니다.
        
        같은 객체가 아닐 경우 String을 구성하는 char[]로 바꾸기 위해 매개변수로 들어온 객체가 String 타입인지 확인하고, 아닐 경우 형변환을 진행합니다.
        
        이후 두 char[]의 길이가 같을 경우 1 바이트씩 비교합니다.
