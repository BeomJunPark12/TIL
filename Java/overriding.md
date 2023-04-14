# 오버라이딩
- 상속받은 조상의 메서드를 자신에 맞게 변경하는것

## 조건
1. 선언부가 조상과 일치
2. 접근제어자를 조상보다 좁은 범위로 변경할 수 없음
3. 예외는 조상메서드보다 많이 선언할 수 없음

# 오버라이딩 vs 오버로딩
- 오버라이딩 : 상속받은 메서드의 내용을 변경하는 것, 가져다 씀
- 오버로딩 : 하나의 클래스 안에서 같은 이름의 메서드를 여러개 정의하는 것을 뜻한다
- 조건
    
    1. 매개변수의 개수가 달라야한다
    2. 매개변수의 타입이 달라야한다

오버라이딩
```java
public class Parent {
	
	public void overridingTest() {
		System.out.println("부모 메서드입니다.");
	}
}

class Child extends Parent {

	@Override
	public void overridingTest() {
		System.out.println("상속받은 부모 메서드의 내용을 수정하여 자식메서드의 내용으로 재사용");
	}
}
```

오버로딩

1. 매개변수 개수가 다른 경우
```java
public int overloadTest() {
		return 0;
	}
	
	public int overloadTest(String test) {
		return 1;
	}
```

2. 매개변수 타입이 다른 경우
```java
public int overloadTest(int test) {
		return 1;
	}
	
	public int overloadTest(String test) {
		return 1;
	}
```


