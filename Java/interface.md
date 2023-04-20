# 인터페이스(interface)
- 일종의 추상클래스, 추상클래스(미완성 설계도)보다 추상화 정도가 높다.
- 실제 구현된 것이 전혀 없는 기본 설계도(알맹이 없는 껍데기)
- 추상메서드와 상수만을 멤버로 가질 수 있다.
- 인스턴스를 생성할 수 없고, 클래스 작성에 도움을 줄 목적으로 사용된다.
- 미리 정해진 규칙에 맞게 구현하도록 표준을 제시하는 데 사용된다.


```java
interface 인터페이스이름 {
    public static final 타입 상수이름 = 값;
    public abstract 메서드이름(매개변수목록);
}
```
```java
interface PlayCard {
    public static final int SPADE = 4;
    final int DIAMOND = 3; // public static final int DIAMOND = 3;
    static int HEART = 2; // public static final int HEART = 2;
    int CLOVER = 1; //  public static final int CLOVER = 1;

    public abstract String getCardNumber();
    String getCardKind(); // public abstract String getCardKind();

}
```

# 인터페이스 상속
- 인터페이스도 클래스처럼 상속이 가능하다.(클래스와 달리 다중상속 허용)

```java
interface movable {
    
    void move(int x, int y);
}

interface attackable {
    
    void attack(Unit u);
}

interface Fightable extends Movable, Attackable {}
```
- 인터페이스는 Object클래스와 같은 최고 조상이 없다.

<br>

# 인터페이스의 구현
- 인터페이스를 구현하는 것은 클래스를 상속받는 것과 같다.
다만 extends 대신에 implements를 사용한다.
```java
class 클래스이름 implements 인터페이스이름 {
    // 인터페이스에 정의된 추상메서드를 구현해야한다.
}
```

<br>

# 인터페이스를 이용한 다형성
- 인터페이스 타입의 변수로 인터페이스를 구현한 클래스의 인스턴스를 참조할 수 있다.
```java
class Fighter extends Unit implements Fightable {
    public void move (int x, int y) { /* 내용 생략 */}
    public void attack (Fightable f) {/* 내용 생략 */} 

   // Fighter f = new Fighter();
   // Fightable f = new Fightable();
}
```
- 인터페이스를 메서드의 매개변수 타입으로 지정할 수 있다.
```java
void attack (Fightable f) {
    // fightable인터페이스를 구현한 클래스의 인스턴스를 매개변수로 받는 메서드
}
```
- 인터페이스를 메서드의 리턴타입으로 지정할 수 있다.
```java
Fightable method() {
    // fightable 인터페이스를 구현한 클래스의 인스턴스를 반환
    return new Fighter();
}
```

<br>

# 인터페이스 장점
1. 개발 시간을 단축시킬 수 있다.

2. 표준화가 가능하다.

3. 서로 관계없는 클래스들에게 관계를 맺어 줄 수 있다.

4. 독립적인 프로그래밍이 가능하다.




