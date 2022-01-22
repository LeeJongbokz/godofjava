
- 자바에서 .class 파일을 만들 수 있는 것에는 클래스만 있는 것이 아님.  
  interface와 abstract 클래스라는 것이 있음.  
  인터페이스와 abstrct 클래스에 대해서 제대로 이해하려면,  
  시스템을 만드는 절차가 어떻게 되는지 알아야 함.  
  
- 어떤 시스템을 개발하든 간에 "방법론"이라는 것을 사용하여 개발함.  
  방법론이라는 것은 시스템을 어떻게 만들 것인지에 대한 절차를 설명함.  
  어떤 문서를 작성해야 하는지를 정리해 놓은 공동 절차라고 보면 됨.  
  
- 일반적인 절차는 다음과 같음.  
  (1) 분석  
  (2) 설계  
  (3) 개발 및 테스트  
  (4) 시스템 릴리즈  
  
  
- 인터페이스와 abstract 클래스를 사용하는 이유는  
  (1) 설계시 선언해 두면 개발할 때 기능을 구현하는데만 집중할 수 있음  
  (2) 개발자의 역량에 따른 메소드의 이름과 매개 변수 선언의 격차를 줄일 수 있음  
  (3) 공통적인 인터페이스와 abstract 클래스를 선언해 놓으면, 선언과 구현을 구분할 수 있음.  
  
  

### 인터페이스 직접 만들기

- 앞 장에서 사용한 MemberDTO를 관리하는, MemberManagerImpl이라는 클래스를 만들어야 한다고 가정함.  
  실제 코드는 만들지 않더라도, 어떤 메소드들이 있어야 하는지를 정의하려고할 때 인터페이스를 사용하면 됨.  
  
- 인터페이스는 다음과 같이 정의함.  여기서는 MemberManager라는 이름으로 만듦.  
  참고로, 이 예제의 패키지는 c.service이므로, c 폴더 하위에 service 폴더를 만들고  
  이 인터페이스 파일을 추가하면 됨.  
  앞에서 사용한 MemberDTO는 c.model 패키지에 복사해 둠.  
  
```
package c.service;

import c.model.MemberDTO;

public interface MemberManager{

    public boolean addMember(MemberDTO member);
    public boolean removeMember(String name, String phone);
    public boolean updateMember(MemberDTO member);
}
```

- 여기서 가장 중요한 것은 인터페이스 선언부는 public class로 시작하지 않고,  
  public interface로 시작한다는 것임.  
  이렇게 interface 내부에 선언된 메소드들은 몸통(body)이 있으면 안됨.  
  즉, 메소드 선언 이후에 중괄호를 열고, 닫거나, 중괄호 안에 한 줄의 코드도 있으면 안됨.  
  
  
- 이렇게 만든 인터페이스를 어떻게 활용할까?  
  다음과 같이 MemberManagerImpl이라는 클래스를 만들어 봄.  
  
```
pakcage c.service;

public class MemberManagerImpl implements MemberManager {
}
```  

- 클래스 선언문을 잘 보면 implements라는 단어 뒤에 MemberManager라고 방금 만든 인터페이스를 추가함.     
  이와 같이 만들어져 있는 인터페이스를 적용한다고 할 때에는 클래스 선언문에서 클래스 이름 뒤에  
  implements라는 예약어를 쓴 후 인터페이스들을 나열하면 됨.  
  
  
- 인터페이스를 구현할 경우에는 반드시 인터페이스에 정의된 메소드들의 몸통을 만들어 주어야만 함.  
  즉, 메소드들을 구현해야만 함.  
  MemberManagerImpl 클래스는 적어도 다음과 같이 구현해야만 함.  

```
package c.service;
import c.model.MemberDTO;
public class MemberManagerImpl implements MemberManager { 

  @Override
  public boolean addMember(MemberDTO member) {
     return false;
  }
  
  @Override
  public boolean removeMember(String name, String phone){
     return false;
  }
  
  @Override
  public boolean updateMember(MemberDTO member){
     return false;
  }

}
```

- MemberManager에 정의된 메소드들을 모두 구현해야만 컴파일이 정상적으로 수행됨.  
  이제 이 클래스를 컴파일하면 정상적으로 컴파일 됨.  
  이제 개발자들이 해야 하는 일은 대충 return false만 적어 놓은 메소드들이  
  실제로 Member 정보를 저장하고, 삭제하고, 수정하는 일을 할 수 있도록 제대로 된 코드를 만드는 것임.  
  바로 이 작업이 개발 프로세스 중에서 "개발"에 해당함.  
  참고로 여기에서 처음 등장하는 @Override는 17장에서 배우는 어노테이션이라는 것임.  
 
 

  

