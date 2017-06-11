# Java-Interview-QnA
자바 면접 질문과 답

### Q0. 자바(java)의 장단점을 설명하시오.
자바의 가장 큰 장점은 JVM을 이용한 플랫폼 독립적이라는 점입니다. 자바에서 코드를 컴파일하면 바이트코드(.class) 형태로 출력됩니다. 이 바이트코드는 JVM에 런타임에 완벽한 기계코드로 변경되어 실행됩니다. 하나의 바이트코드를 가지고 서로다른 기계마다 해당 JVM만 설치되어있으면 다시 컴파일 할 필요 없이 나머지는 JVM에서 해당 기계에 맞도록 실행해줍니다. 그 밖에 C언어 계열에서 지원하는 포인터 연산을 과감하게 배제하여 안정성 있는 코드 작성에 집중할 수 있도록 했습니다. 또한 객체지향 프로그래밍을 완벽하게 지원합니다. 마지막으로 다양한 기본 클래스와 멀티쓰레딩, 네트워킹 API를 지원합니다.

자바의 단점은 JVM을 사용하는데서 발생하는데에 있습니다. 자바 프로그램이 실행되기 위해서는 먼저 JVM이 실행되어야 하는데 JVM 실행과정은 생각보다 많은 메모리를 소모하며 실행속도 또한 빠르지 않습니다. 또한 바이트코드를 완전한 기계코드로 변환하는 과정에서도 일반적인 컴파일 언어로 작성된 프로그램보다 속도가 많이 느립니다.

### Q1. 기본 자료형(primitive data type)과 참조 자료형(reference data type)에 대해 설명하시오.
기본 자료형은 byte, short, int, long, float, double, char, boolean이 존재합니다. 기본 자료형으로 생성한 변수에는 값 자체가 저장됩니다. 사용전에 반드시 선언되어야하며 OS에 따라 자료형의 길이가 변하지 않고 null 값을 갖을수 없는 특징이 있습니다.

참조 자료형은 class, interface, array, enum이 존재합니다. 참조 자료형으로 생성한 변수에는 객체의 주소값이 저장됩니다. 생성자를 이용하여 새로운 객체의 주소를 가리키거나 null 값을 이용하여 해제할 수 있습니다.

### Q2. 객체지향 프로그래밍(object-oriented programming)에 대해 설명하시오.
실세계의 특정 사물을 추상화하여 그에 필요한 멤버 변수와 메소드를 정의하는데서 출발합니다. 캡슐화를 통해 이러한 멤버 변수와 메소드의 이용가능범위를 적절하게 제한하여 안전한 프로그래밍을 지원합니다. 상속의 개념을 이용하여 부모 클래스의 기능을 자식 클래스에서 물려받거나 재정의를 통해 부모와 자식의 다른 기능을 구현하는 다형성까지 포함합니다.

객체지향 프로그래밍을 이용하면 코드의 재사용성을 극대화시켜 개발 및 유지보수 과정에서 효율적입니다. 또한 캡슐화를 통해 클래스 외부에서 불필요한 데이터의 접근을 제한하여 올바른 값을 유지하도록 보호할 수 있습니다. 마지막으로 다형성의 개념을 이용하여 형태는 갖지만 객체에 따라서 서로 다른 기능을 하는 메소드나 이름은 같지만 인자가 다른 메소드를 구현할 경우 간결하게 구현할 수 있습니다.

### Q3. 다형성(polymerphism)에 대해 설명하시오.
객체지향 프로그래밍에서 하나의 메소드나 클래스가 다양한 방법으로 동작하게하는 요소를 말합니다. 대표적으로 메소드 오버라이딩, 오버로딩이 있습니다.

메소드 오버라이딩은 자식 클래스에서 부모 클래스의 메소드를 새롭게 재정의하는 것을 말합니다. 메소드의 선언부는 같은 형태이지만 몸체에서 다른 역할을 수행하도록 합니다. 같은 이름과 형식의 메소드라도 클래스에 따라 다른 기능을 부여하는 기능을 갖습니다.

메소드 오버로딩은 하나의 클래스에서 같은 이름을 가졌지만 인자의 종류나 숫자가 다른 메소드를 구현하는 것을 말합니다. 같은 기능을 수행하지만 다른 인자를 수행하는 메소드를 정의할 경우 이름을 동일하게 묶어주는 기능을 수행합니다.

### Q4. 접근제어자(access modifier)에 대해 설명하시오.
접근제어자는 객체지향 프로그래밍에서 클래스의 멤버 변수 또는 메소드에 설정하는 키워드로 접근 영역을 제한하는데 사용합니다. public, default, protected, private이 존재합니다. 접근제어자를 사용하지 않았을 경우에는 기본적으로 default를 갖습니다. public은 접근 제한을 하지 않음을 의미합니다. default는 같은 패키지 내에서만 접근이 가능함을 의미합니다. protected는 같은 패키지 내 혹은 다른 패키지의 자식 클래스에서 접근이 가능함을 의미합니다. private는 같은 클래스 내에서만 접근이 가능함을 의미합니다.

### Q5. 추상 클래스(abstract class)와 인터페이스(interface)에 대해 설명하시오.
추상 클래스는 abstract 키워드를 이용하여 미완성 메소드 즉, 형태만 정의해 놓고 몸체는 없는 상태를 포함하고 있는 클래스를 의미합니다. 추상 클래스는 상속에 큰 의미를 두고 있습니다. 클래스이기 때문에 extends 키워드를 이용하여 상속을 진행하며 이런 추상 클래스를 상속받은 자식 클래스에서는 반드시 미완성 메소드를 재정의해야합니다.

인터페이스는 추상 클래스보다 추상화 정도가 높은 상태를 정의할 때 사용합니다. 인터페이스는 기능의 재정의에 큰 의미를 두고 있습니다. 멤버 변수와 일반 메소드를 가질 수 없으며 오직 상수와 추상 메소드만을 선언할 수 있습니다. implements 키워드를 이용하여 상속을 진행하며 자식 클래스에서 반드시 메소드를 재정의해야합니다. 그 밖에 인터페이스는 클래스에서 지원하지 않는 다중상속이 가능합니다.

### Q6. final 키워드의 다양한 쓰임새를 설명하시오.
변수에 final 키워드를 사용하면 해당 변수를 상수화 할 수 있습니다. final 키워드가 붙어있는 변수는 초기화만 가능하며 이후 새로운 값으로 변경이나 재할당이 불가능합니다.

다음으로 클래스에 final 키워드를 사용하면 해당 클래스를 상속할 수 없습니다. 이 경우 abstract 키워드와 기능적인면에서 충돌이 있기 때문에 함께 사용할 수 없습니다.

마지막으로 클래스의 메소드에 final 키워드를 사용하면 해당 메소드를 오버라이딩 할 수 없습니다.

### Q7. static 키워드의 쓰임새를 설명하시오.
클래스 내부의 메소드나 멤버 변수에 static 키워드를 사용하면 하나의 인스턴스에 속하지 않고 해당 클래스로부터 생성된 모든 인스턴스가 공통으로 공유하는 메소드와 변수로 변경됩니다.

### Q8. 컬렉션(collection) 클래스에서 제네릭을 사용하는 이유를 설명하시오.
컬렉션 클래스에서 제네릭을 사용하면 컴파일러는 특정 타입만 포할될 수 있도록 컬렉션을 제한합니다. 컬렉션 클래스에 저장하는 인스턴스 타입을 제한하여 런타임에 발생할 수 있는 잠재적인 모든 예외를 컴파일타임에 잡아낼 수 있도록 도와줍니다.

### Q9. 컬렉션(collection) 클래스의 대표 인터페이스를 설명하시오.
컬렉션 클래스는 크게 list, set, map이 있습니다.

list는 순차적인 데이터를 저장하며 중복을 허용하는 자료구조입니다. arraylist, linkedlist, stack, vactor가 하위 클래스로 존재합니다.

set은 순서를 유지하지 않고 데이터의 중복만 허용하지 않는 자료구조입니다. hashset, treeset이 하위 클래스로 존재합니다.

map은 키와 값으로 이루어진 데이터를 순서를 유지하지 않고 키의 중복만 허용하지 않는 자료구조입니다. hashmap, treemap, hashtable, properties가 하위 클래스로 존재합니다.

### Q10. 객체의 직렬화(serialization)에 대해 설명하시오.
객체에 저장되어있는 데이터를 스트림(파일로 저장 혹은 네트워크를 이용하여 전송)에 바로 쓰기 위해 연속적인 데이터로 변환하는 것을 말합니다. 반대로 스트림으로부터 데이터를 읽어 객체로 변환하는 과정은 역직렬화라고 합니다. io 패키지내에 구현되어있는 Serializable 인터페이스를 상속 받으면 직렬화가 가능한 클래스로 변경할 수 있습니다. 직렬화를 시키고자하는 클래스에 직렬화가 안되는 객체가 포함되어있을 경우 transient 키워드를 이용하여 해당 객체를 직렬화 대상에서 제외시킬수 있습니다.

### Q11. 래퍼 클래스(wrapper class)에 대해 설명하시오.
기본 자료형으로 표현된 데이터를 참조 자료형으로 만들어야 할 경우 래퍼 클래스를 사용합니다. 보통 특정 메소드에서 참조 자료형을 인자로 받거나, 기본 자료형이 아닌 객체 자료형으로 저장해야할 경우, 객체간 비교가 필요할 경우에 사용합니다.

### Q12. 자바에서 쓰레드를 구현하기 위한 2가지 방법을 간단하게 설명하시오.
lang 패키지내에 구현되어있는 Thread 클래스를 상속받거나 Runnable 인터페이스를 상속받아 run 메소드를 재정의하여 구현합니다.

### Q13. 자바에서 쓰레드의 동기화(synchronized)와 데드락(deadlock)을 설명하시오.
2개 이상의 쓰레드가 하나의 공유 자원에 접근하여 값을 변경하려 할 때, 동기화를 적용하지 않으면 값이 올바르지 못하게 변경될 가능성이 있습니다. 따라서 공유 변수에 synchronized 키워드를 사용하거나 블록을 설정하여 하나의 쓰레드가 공유 자원을 점유하고 있을 경우 다른 쓰레드가 잠시 대기상태에 머무르도록 할 수 있습니다.

데드락은 다음과 같은 예를 들어 설명할 수 있습니다. a 쓰레드가 foo라는 공유 변수에 락을 걸어둔 상태로 작업을 진행하고 있고, b 쓰레드가 bar라는 공유 변수에 락을 걸어둔 상태로 작업을 진행하고 있다고 가정합니다. 여기서 a 쓰레드에서 bar 공유 변수가 필요한 코드를 만났지만 bar는 이미 b 쓰레드가 선점하고 있으므로 a 쓰레드는 대기 상태로 변경됩니다. 동시에 b 쓰레드에서도 foo 공유 변수가 필요한 코드를 만났다고 가정하면 foo는 이미 a 쓰레드가 선점하고 있으므로 b 쓰레드도 역시 대기 상태로 변경됩니다. 이렇게 두 쓰레드가 모두 대기 상태 계속 머무르게 되는 현상을 말합니다.

### Q14. String, StringBuffer, StringBuilder에 대해서 설명하시오.
String은 문자열을 처리하는 자바의 대표적인 클래스입니다. String 클래스는 한번 생성되면 변경이 불가능한 immutable 성격을 가지고 있습니다. String 클래스가 immutable한 이유는 변경이 적고 참조만 많은 경우 혹은 여러개의 쓰레드에서 공유하는 문자열일 경우 별다른 동기화를 구현하지 않고 안전하게 공유될 수 있다는 장점있기 때문입니다. 하지만 문자열을 변형하는 경우가 많은 경우(자르거나 이어붙이기) 매번 새로운 String 객체가 생성되기 때문에 메모리와 속도측면에서 비효율적입니다. 따라서 String 클래스는 변경이 적고 단순 참조만 많은 경우에 사용합니다.

StringBuffer 클래스와 StringBuilder 클래스는 새로운 객체를 생성하지 않고 기존 문자열을 변경합니다. 단, StringBuilder의 경우 쓰레드의 동기화를 지원하지 않기 때문에 쓰레드에서 사용하기 위해서는 StringBuffer 클래스를 이용해야합니다. 하지만 속도는 동기화를 처리하지 않는 StringBuilder 클래스가 동기화를 처리하는 StringBuffer 클래스보다 빠르기 때문에 쓰레드를 사용하지 않는 환경에서는 StringBuilder 클래스를 사용하는편이 유리합니다.

### Q15. JVM(java virtual machine)의 메모리 구조와 가비지 컬렉션(garbage collection)을 설명하시오.
JVM의 메모리 구조는 크게 class, stack, heap, native 메소드, PC 레지스터로 나뉩니다.

class 영역에는 클래스, 변수, 메소드, 상수, static 변수에 대한 정보가 저장됩니다.

stack 영역에는 메소드 호출에 따른 메소드를 위한 공간인 프레임(frame)이 생성되어 메소드 안에서 필요한 각종 값이 임시로 저장됩니다. 메소드의 수행이 끝나면 프레임별로 삭제가 진행됩니다.

heap 영역에는 new 연산자로 생성된 객체와 배열이 저장되는 공간입니다. 크게 permanent geration, new, old 영역으로 나뉩니다. permanent geration 영역에 생성된 객체들의 주소값이 저장됩니다. new 영역은 다시 eden, survivor 영역으로 나뉘어있습니다. eden에는 객체들이 최초로 생성되는 영역이며 suvivor는 eden 영역에서 참조되는 객체들이 저장되는 영역입니다. 마지막으로 old 영역은 new 영역에서 일정 시간 참조되고 있는 객체들이 저장되는 공간입니다.

native 메소드 영역은 자바 이외의 다른 언어에서 제공되는 메소드가 저장되는 영역입니다.

PC 레지스터 영역은 쓰레드가 생성될 때마다 생성되는 영역으로 쓰레드가 어떤 명령(현재 실행되는 부분의 명령과 주소)을 실행할지 저장합니다.

가비지 컬렉션은 크게 minor, major로 나뉩니다. minor에서는 new 영역을 대상으로 실행됩니다. 첫째로 new 영역 안의 eden 영역이 가득 차면 survivor1 영역으로 이동시킨 후 나머지 영역의 객체를 삭제합니다. 둘째로 eden 영역과 survivor1 영역이 기준치 이상으로 찼을경우 참조가 실제로 되고 있는지 검사 후 참조되는 객체만 survivor2 영역에 복사 후 나머지 영역의 객체를 삭제합니다. 마지막으로 일정시간 참조되고 있는 객체들을 old 영역으로 이동시킵니다.

major에서는 old 영역을 대상으로 실행됩니다. minor에 비해 시간이 오래 걸리며 old 영역이 가득 차, 프로세스가 정지될 가능성이 있는 경우 실행됩니다. old 영역에 있는 모든 객체를 검사하여 참조되지 않은 객체들을 한꺼번에 삭제합니다.

### Q16. NIO(new input-output)을 설명하시오.
기존의 자바 IO(input-output)의 단점을 보완한 새로운 IO 패키지를 의미하며 non-blocking IO를 지원하는 특징이 있습니다. blocking이란 IO 작업에서 주로 사용되는 메소드의 경우 실행 속도가 느려 잠시 멈춰있는 상태를 말합니다. 이 문제를 해결하기 위해 보통 쓰레드를 구현했습니다. 하지만 이런 작업이 수 만개가 동시에 진행할 가능성이 있는 서버 프로그램 일 경우 쓰레드가 너무 많아져 생기는 문제(CPU contexted switching, memory allocation)가 발생합니다. 그런데 실제로는 이런 수 많은 쓰레드가 모두 작업을 하지 않고 대부분은 자원만 낭비하는 상태로 유지되는 경우가 많기 때문입니다.

따라서, 모든 IO에 대해 쓰레드를 생성하는 방식이 아닌 채널관리자(selector)를 사용하여 실제 IO가 발생한 채널만 쓰레드를 생성하여 관리하는 방식입니다. 하지만 채널을 이용한 프로그래밍은 기존의 다중쓰레드를 이용한 방식보다 구현하기 어려운 단점이 있습니다.

### Q17. 자바의 call-by-value에 대해서 예를 들어 설명하시오.

### Q18. 자바의 형변환 규칙은 어떻게 되는지 예를 들어 설명하시오.
형변환에는 크게 2가지가 존재합니다. 첫번째로 묵시적 형변환으로 자바에서는 작은 단위를 큰 단위로 바꾸는 경우 묵시적 형변환을 지원합니다. 예를들어 상속관계에서 하위 객체를 상위 객체로 변환하거나 int형 변수를 double형 변수로 변환할 수 있습니다. 두번째로 명시적 형변환으로 큰 단위에서 작은 단위로 바꾸는 경우 명시적 형변환을 프로그래머가 정의해주어야 합니다. 이 경우 데이터의 일부가 유실될 수 있습니다. 예를들어 long 변수에 저장되어 있는 값을 int 변수로 변환하는 경우 (int) 키워드를 사용하는 방식입니다. 기타 산술, 논리, 참조 자료형 사이에서는 형변환이 불가능합니다.

### Q19. String 클래스의 intern 메소드와 상수 풀(constant pool)에 대해 설명하시오.
자바에서 쓰이는 모든 String 객체는 상수 풀에서 관리됩니다. 상수 풀은 객체가 생성되는 영역인 heap의 permanent generation 영역에 생성되어 자바 프로세스가 종료될 때 까지 함께합니다. 상수 풀을 이용하여 String을 관리하는 이유는 중복 문자열에 대한 효율적인 메모리 관리 때문입니다. 같은 문자열이 이미 존재하는데 다시 동일한 문자열이 상수 풀에 삽입되려는 경우 삽입을 위해 heap에 생성되었던 문자열을 해제하고 상수 풀에서 관리하는 래퍼런스로 반환해줍니다. 이렇게 함으로서 동일한 문자열로 인해 메모리가 낭비되는 현상을 해결합니다.

String 클래스의 intern 메소드는 heap 영역에 있는 문자열 객체를 상수 풀로 이전시키는 메소드입니다. intern 메소드는 실행 후 해당 문자열과 동일한 문자열이 없다면 해당 객체를 상수 풀에 등록하고 heap 영역에서 해제 후 래퍼런스 값을 반환합니다. 만약 해당 문자열과 동일한 문자열이 있다면 해당 객체를 heap 영역에서 해제 후 상수 풀에 있는 해당 문자열의 래퍼런스 값을 반환해줍니다.

String 객체를 생성하는 방법에는 크게 2가지가 있습니다. 첫번째로 리터럴("")을 이용한 방법입니다. 이 경우 내부적으로 String 생성자로 객체를 heap 영역에 생성한 후 intern 메소드가 호출되어 상수 풀에 해당 객체를 등록하는 과정을 거칩니다. 두번째로 String 생성자를 이용하는 방법이 있습니다. 이 경우 heap의 어떤 영역에 단순한 인스턴스로 저장합니다. 이 경우 상수 풀에 등록되지 않습니다. 후에 명시적으로 intern 메소드를 호출하여 상수 풀로 옮겨줄 수 있습니다.

상수 풀에 등록되어있는 문자열 객체의 경우 == 연산자를 이용하면 바로 두 문자열이 같은지 boolean 값으로 확인할 수 있습니다. 하지만 String 생성자를 이용해 heap의 한 영역에 생성된 문자열 객체의 경우 == 연산자를 이용하여 바로 두 문자열이 같은지 비교할 수 없습니다. 두 문자열 객체의 래퍼런스 값이 다르기 때문입니다. 이 경우 String 클래스의 equals를 이용하여 두 문자열의 값을 비교할 수 있습니다.
