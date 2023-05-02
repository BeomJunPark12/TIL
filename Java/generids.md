# 제네릭스
- 제네릭스는 다양한 타입의 객체들을 다루는 메서드나 컬렉션 클래스에 컴파일 시의 타입 체크를 해주는 기능이다.
- 객체의 타입을 컴파일 시에 체크하기 때문에 객체의 타입 안정성을 높이고 형변환의 번거로움이 줄어든다.

```java
// 객체만 저장할 수 있는 ArrayList를 생성
ArrayList<Tv> tvList = new ArrayList<Tv>();

tvList.add(new Tv());   // OK
tvList.add(new Audio());    // 컴파일 에러, Tv외에 다른 타입은 저장 불가
```

```
제네릭스 장점
1. 타입 안정성을 제공한다.
2. 타입체크와 형변환을 생략할 수 있어서 코드가 간결해진다.
```

# 제네릭 다형성
```java
import java.util.*;

class Product{}
class Tv extends Product{}
class Audio extends Product{}

class ex {
    public static void main(String[] args) {
        ArratList<Product> productList = new ArrayList<Product>();
        list.add(new Product());
        list.add(new Tv()); // ok
        list.add(new Audio()); // ok


    }
}

```

