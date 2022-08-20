# String 에서 char 를 이용해서 숫자 한개씩 읽어올 때
> String 에서 charAt 으로 숫자 한개씩 읽어와야 할 경우
> 이 경우에 당연하게도 읽어들이는 문자는 숫자가 아닌 character 형 데이터이다.


### char -> int 형변환
> 이걸 int형으로 변환시키면 아스키코드값인 49가 나오게 된다.
> 49에서 1이 되기 위해서는 48을 빼줘야 하는데. 래서 - '0'을 해주는 것. '0'은 아스키코드 48.


```java
public static void main(String[] args) {
 
    int sum = 0; //숫자의 합을 저장할 변수
    String str = "123"
        
    for(int i=0; i<3; i++) {
        sum += (str.charAt(i) - '0'); //string형을 char형으로 문자 하나하나씩 받고 그걸 숫자형으로 변환하여 sum에 더함.
    }
        
    System.out.println(sum); //출력결과: 6
 
}
```
