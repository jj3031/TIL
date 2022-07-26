# 에라토스테네스의 체(Sieve of Eratosthenes)
> 수학에서 에라토스테네스의 체는 소수를 찾는 방법이다. 고대 그리스 수학자 에라토스테네스가 발견하였다.
> 소수를 구하는 알고리즘 중에 가장 빠른 편


for문 여러번 돌려서도 해결이 가능하나 시간이 부족 할 것.


### 기본 로직
* 2부터 1씩 증가하면서 주어진 숫자까지 반복해서 증가된 수로 나눠지면 배열에서 제외 하는 식의 로직


### 예제
```java
import java.io.IOException;
import java.util.Scanner;

public class Main {
	

	public static void main(String[] args) throws IOException {
		Main T= new Main();
		Scanner kb= new Scanner(System.in);
		int n = kb.nextInt();
		System.out.println(T.solution(n));
	}

	public int solution(int n) {
		int answer=0;
		int[] ch = new int[n+1];
		for(int i=2; i<=n;i++) {
			if(ch[i]==0) {
				answer++;
				for(int j=i; j<=n; j=j+i) {
					ch[j]=1;
				}
			}
		}
				
		return answer;
	}
}
```
### 해당 로직에서 배운것
* 이제는 빠르기도 생각하는 코딩을 할 것
* 문제 해결이 능사가 아님



