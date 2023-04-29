# 제어자
## 멤버의 접근지정자
- public : 동일 패키지의 모든 클래스 + 다른 패키지의 모든 클래스 사용 가능
- protected   : 동일 패키지의 모든 클래스 + 다른패키지의 [자식] 클래스에서 사용가능
		
- default	    : 동일 패키지의 모든 클래스에서 사용가능  = 내 패키지에서만 사용가능
		
- private     : 자신 클래스내에서만 사용가능
<br><br>

# 클래스의 접근지정자
- public : 다른 패키지에서 import 가능
- default : 다른 패키지에서 import 불가능, 동일 패키지내에서 객체 생성 가능
<br><br>

# 생성자의 접근 지정자 = 클래스의 접근지정자와 동일
public, default 클래스가 import 가능하다면 생성자도 가능, 그러나 생성자가 default가 아닐 시 

public 클래스의 [자동추가]생성자는 public생성자

default클래스의 [자동추가]생성자는 default생성자
		
public클래스의 default생성자는 다른패키지에서 import를 할 수 있지만 객체생성 불가능

A a = new A();
		

