

- 이번에는 인터페이스도 아닌 그렇다고 클래스라고도 하기 힘든 abstract 클래스에 대해서 알아봄.  
  abstract라는 단어는 앞 절의 참고에서 말했듯이 사전적으로 "추상적인"의 의미임.  
  abstract 클래스는 자바에서 마음대로 초기화하고 실행할 수 없도록 되어 있음.  
  그 abstract 클래스를 구현해 놓은 클래스로 초기화 및 실행이 가능함.  
  

- 인터페이스는 선언시 class라는 예약어를 사용하지 않고 바로 interface라는 예약어를 사용함.  
  그리고 각 메소드 선언문은 일반 메소드 선언문과 동일하지만,  
  메소드의 몸통이 없음.  
  이제 abstract 클래스의 예제를 봄.  
  
 
```
package c.service;

import c.model.MemberDTO;

public abstract class MemberManagerAbstract {
   public abstract boolean addMember(MemberDTO member);
   public abstract boolean removeMember(String name, String phone);
   public abstract boolean updateMember(MemberDTO member);
   public void printLog(String data){
     System.out.println("Data="+data);
   }
}
```

- abstract 클래스는 선언시 class라는 예약어 앞에 abstract라는 예약어를 사용함  
  그리고 몸통이 없는 메소드 선언문에는 abstract라는 예약어를 명시한 것을 볼 수 있음.  
  이와 같이 abstracㅅ 클래스는 abstract로 선언한 메소드가 하나라도 있을 때 선언함.  
  게다가, 인터페이스와 달리 구현되어 있는 메소드가 있어도 상관 없음.  
  
  

