# 에라토스테네스의 체(Sieve of Eratosthenes)
> 수학에서 에라토스테네스의 체는 소수를 찾는 방법이다. 고대 그리스 수학자 에라토스테네스가 발견하였다.
> 소수를 구하는 알고리즘 중에 가장 빠른 편.
> for문 여러번 돌려서도 해결이 가능하나 시간이 부족 할 것.
> timeout도 생각해가면서 코딩 해야 함





### 기본 로직
* 2부터 1씩 증가하면서 주어진 숫자까지 반복해서 증가된 수로 나눠지면 배열에서 제외 하는 식의 로직


### 예제
```java
public class Eratos {
	public static void main(String[] args) {
		// ArrayList로 구현
		ArrayList<Boolean> primeList;

		// 사용자로부터의 콘솔 입력
		Scanner scan = new Scanner(System.in);
		int n = scan.nextInt();

		// n <= 1 일 때 종료
		if(n <= 1) return;

		// n+1만큼 할당
		primeList = new ArrayList<Boolean>(n+1);
		// 0번째와 1번째를 소수 아님으로 처리
		primeList.add(false);
		primeList.add(false);
		// 2~ n까지 소수로 설정
		for(int i=2; i<=n; i++ )
			primeList.add(i, true);

		// 2부터  ~ i*i <= n
		// 각각의 배수들을 지워간다.
		for(int i=2; (i*i)<=n; i++){
			if(primeList.get(i)){
				for(int j = i*i; j<=n; j+=i) primeList.set(j, false);
				//i*i 미만은 이미 처리되었으므로 j의 시작값은 i*i로 최적화할 수 있다.
			}
		}
		StringBuffer sb = new StringBuffer();
		sb.append("{");
		for(int i=0; i<=n; i++){
			if(primeList.get(i) == true){
				sb.append(i);
				sb.append(",");
			}
		}
		sb.setCharAt(sb.length()-1, '}');

		System.out.println(sb.toString());

	}
}
```
### 해당 로직에서 배운것
* 이제는 빠르기도 생각하는 코딩을 할 것
* 문제 해결이 능사가 아님



