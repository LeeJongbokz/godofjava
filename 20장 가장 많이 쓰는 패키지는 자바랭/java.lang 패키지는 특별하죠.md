

### java.lang 패키지는 특별하죠

- 이 절의 제목처럼 java.lang 패키지는 아주 특별한 패키지임  
  자바의 패키지 중에서 유일하게 java.lang 패키지에 있는 클래스들은  
  import를 안해도 사용할 수 있기 때문임  
  
- 그만큼 Java에 꼭 필요한 여러 기능들을 제공함  
  java.lang과 java.util 패키지를 제외한 대부분의 java로 시작하는 패키지들은  
  패키지 이름만 보고도 어떤 일을 할 때 사용하는지를 알 수 있음  
  
- 하지만 java.lang과 java.util 패키지 안에는 아주 다양한 일을 하는 클래스와 인터페이스들이  
  혼재 되어 있음  
  
  
- java.lang 패키지에 정의되어 있는 에러 중 알아야 하는 것은 
  바로 OutOfMemoryError(OOME)와 StackOverFlowError임 
  OOME의 경우 메모리가 부족하여 발생하는 에러임.  
  자바는 가상 머신에서 메모리를 관리하지만,
  프로그램을 잘못 작성하거나 설정이 제대로 되어 있지 않을 경우에는 이러한 에러가 발생할 수 있음
  
- StackOverflowError는 호출된 메소드의 깊이가 너무 깊을 때 발생함 
  자바에서는 스택이라는 영역에 어떤 메소드가 어떤 메소드를 호출했는지에 대한 정보를 관리함
  예를 들어, 메소드가 자기 자신을 호출하는 재귀 메소드를 잘못 작성했다면  
  스택에 쌓을 수 있는 메소드 호출 정보의 한계를 넘어설 수 있음
  이 경우에 발생하는 것이 바로 StackOverflowError임  
  
- 그리고 java.lang 패키지에는 앞서 살펴본 자바의 기본 어노테이션이 선언되어 있음  
  (1) Deprecated
  (2) Override
  (3) Suppress Warnings 
  
  
  
