# LinkedHashSet
> HashSet과 동일한 구조를 가지지만 HashSet은 순서를 관리하지 않아 값을 출력할 때마다 다른 순서대로 출력이 된다.
> 하지만 LinkedHashSet은 삽입된 순서대로 반복한다.
> HashSet과 동일한 특징들이 있는데 마찬가지로 중복 값을 허용하지 않는다.

### LinkedHashSet 선언
> set의 하위 이므로 Set 클래스로 선언해도 무관


```java
import java.util.Arrays;
import java.util.LinkedHashSet;

public class RegexExample {
	public static void main(String[] args)  {
   LinkedHashSet hs = new LinkedHashSet(); // 타입 설정x Object 입력
		 LinkedHashSet<LinkedHashSetDemo> demo = new LinkedHashSet<LinkedHashSetDemo>(); // 클래스로 타입 설정
		 LinkedHashSet<Integer> i = new LinkedHashSet<Integer>(); // Integer 타입 선언
		 LinkedHashSet<Integer> i2 = new LinkedHashSet(); // 뒷부분 타입 선언 생략 가능
		 LinkedHashSet<Integer> i3 = new LinkedHashSet<Integer>(10); // 크기 10으로 선언
		 LinkedHashSet<Integer> i4 = new LinkedHashSet<Integer>(Arrays.asList(1, 2, 3, 4)); // 선언과 동시에 초기 값 설정
		 LinkedHashSet<String> str = new LinkedHashSet<String>(); // String 타입 선언
		 LinkedHashSet<Character> ch = new LinkedHashSet<Character>(); // Char 타입 선언
    }
}
```

add, remove 등 set에서 사용하던 method를 그대로 사용해서 값을 추가하거나 제거하거나
clear 로 초기화가 가능 하다.

