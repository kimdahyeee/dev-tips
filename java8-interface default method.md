### interface default method
----

```java
public interface A {
	default void a() {
		// 구현 가능
	}
}
```

- java8 에서부터 사용할 수 있는 `default method` (java7 까지는 `추상 메서드`로만 선언 가능했다.)
- `interface`에서도 `method` 구현이 가능하다
- `implements`한 클래스에서도 `@override`를 통해 재정의 가능하다

#### 🙋‍♀ `interface default method`를 쓰며 얻을 수 있는 이점은 무엇인가 ?

`interface`에 신규 기능을 추가한다고 가정해보자.

이미 구현되어 있는 `interface`에 변경이 없으면서, 새롭게 개발하는 클래스에 `default method`를 활용해 새로운 기능을 만들 수 있다.

💁‍♀ 기존 `interface`

```java
public interface AImpl {
	public void a();
}

public class A implements AImpl {
	public void a() {
		// 구현
	}
}
```

💁‍♀ `default method` 사용 하지 않는 경우

```java
// AImpl에 새로운 b라는 method를 추가해야 함
public interface AImpl {
	public void a();
	public void b(); // 신규 추가
}

public class A implements AImpl {
	public void a() {
	}
	
    public void b() {
		/**
		* todo 구현해 주어야 함
		* (AImpl을 구현한 구현체들이 많을 경우 변경 사항이 더욱 많아진다.)
        */

    }	
}
```

💁‍♀ `default method` 사용 하는 경우

```java
// AImpl에 새로운 b라는 method를 추가해야 함
public interface AImpl {
	public void a();
	public default void b() {
		
	}
}

public class A implements AImpl {
	public void a() {
	}
	//추가 변경사항이 없음
}

public class B implements AImpl {
	public void a() {
	}
	
	@Override
	public void b() {
		// 메서드 재정의
	}
}
```

