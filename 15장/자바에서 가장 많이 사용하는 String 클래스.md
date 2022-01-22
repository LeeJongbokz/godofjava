

- String 관련 객체는 몇 백개의 객체 중에서 상위 5개 안에는 항상 포함됨  
  Java에서 String의 비중은 매우 큼.  
  클래스 중에서 더하기 연산을 제공하는 클래스는 String 밖에 없음.  
  
  
- 가장 먼저 String 클래스가 어떻게 선언되어 있는지 살펴봄.  

```
public final class String extends Object
implements Serializable, Comparable<String>, CharSequence 
```

```
public final class String extends Object
```

- public final로 선언됨. public은 누구나 다 사용할 수 있는 클래스임.  
  그 다음에 final이라고 선언됨.  
  클래스가 final로 선언되어 있으면 더 이상 이 클래스는 확장할 수 없음.  
  다시 말해서 String 클래스는 자식 클래스를 양산할 수 없음.  
  
- 그리고 첫 줄의 마지막을 보면 Object 클래스를 확장한 것을 볼 수 있음.  
  즉, 모든 클래스의 부모 클래스는 Object 클래스이므로 따로 확장한 클래스는 없음.  
  
  
```
implements Serializable, Comparable<String>, CharSequence
```

- implements라고 적어준 뒤 인터페이스들을 나열하면 해당 인터페이스에 선언된 메서드들을  
  이 클래스에서 "구현"한다는 의미임.  
  따라서 String은 Serializable, Comparable, CharSequence라는 인터페이스를 구현한 클래스임.  
  
- 인터페이스에는 기본적으로 메소드들이 선언만 되어 있고,  
  그 인터페이스를 implements한 클래스는 선언되어 있는 메소드의 몸통을 구현해야만 함.  
  
- Serializable 인터페이스는 구현해야 하는 메소드가 하나도 없는 아주 특이한 인터페이스임  
  이 Serializable 인터페이스를 구현한다고 선언해 놓으면, 해당 객체를 파일로 저장하거나  
  다른 서버에 전송 가능한 상태가 됨.  

- Comparable이라는 인터페이스도 구현함. 이 인터페이스는 compareTo()라는 메소드 하나만 선언됨.  
  이 메소드는 매개 변수로 넘어가는 객체와 현재 객체가 같은지를 비교하는데만 사용됨.  
  
- 마지막에 있는 CharSequence 인터페이스는 해당 클래스가 문자열을 다루기 위한 클래스라는 것을 나타내는데 사용  
  이 장의 가장 끝 부분에 설명하는 StringBuilder와 StringBuffer 클래스도 이 CharSequence 인터페이스를 구현해놓음    
  
  

  
  
  
