# 자바의 정규식
> 정규표현식(Regular Expression)이란 컴퓨터 과학의 정규언어로부터 유래한 것으로 특정한 규칙을 가진 문자열의 집합을 표현하기 위해 쓰이는 형식언어. 

### 정규식 기본
![](https://github.com/jj3031/TIL/blob/main/IMG/%EC%A0%95%EA%B7%9C%EC%8B%9D1.png?raw=true)
![](https://github.com/jj3031/TIL/blob/main/IMG/%EC%A0%95%EA%B7%9C%EC%8B%9D.png?raw=true)

* 자주 사용하는 패턴
 * ^[0-9]*$ == \\d == 숫자
 * ^[a-zA-Z]*$ == 알파벳
 * ^[가-힣]*$ == 한글
 * ^[a-zA-Z0-9] == 알파벳이나 숫자
 * ^ 의 경우 문자의 시작을 의미하지만 [] 안에 있을 경우 not 을 의미한다.




### Pattern 클래스
* 정규 표현식에 대한 문자열을 검증하는 기능
* 공개된 생성자를 제공하지 않음
* matches method를 이용해서 패턴 분석 가능
```java
import java.util.regex.Pattern;

public class RegexExample {
	public static void main(String[] args)  {
    
            String pattern = "^[0-9]*$"; //숫자만
            String val = "123456789"; //대상문자열
        
            boolean regex = Pattern.matches(pattern, val);
            System.out.println(regex);
    }
}
```

### 풀어볼 수 있는 문제
* 2021 카카오 블라인드 채용 코딩 테스트의 문제인 신규 아이디 추천 문제를 정규식을 활용하여 풀이 가능
