# gRPC 란?
> gRPC는 구글에서 만든 RPC 시스템. gRPC를 설명하기에 앞서 RPC가 무엇인지 알아볼 필요가 있다.


### RPC
> RPC는 Remote Procedure Call로 프로세스간 통신 기법 중 하나. 다른 프로세스에 있는 함수를 호출할때, 마치 같은 프로세스 내에 있는 것처럼 호출할 수 있다. 
> 클라이언트는 일반 로컬 메소드를 호출하는 것처럼 사용하면 된다. RPC는 다양한 환경, 플랫폼에 제약없이 사용할 수 있어 분산 시스템 기법에 효과적.

```java
import java.io.IOException;
import java.util.ArrayList;
import java.util.Collections;
import java.util.LinkedList;
import java.util.List;
import java.util.Queue;
import java.util.Scanner;
import java.util.Stack;


class Point implements Comparable<Point>{
	public int x, y;
	Point(int x, int y){
		this.x =x;
		this.y=y;
	}
	@Override
	public int compareTo(Point o) {
		if(this.x==o.x) return this.y-o.y; //음수가 return 되면, 즉 o.y 가 this.y 보다 크면 o.y가 this.y보다 뒤에 위치한다. => 오름차순
		else return this.x-o.x;
	}
}

public class Main {
	


	public static void main(String[] args) throws IOException {
		Main T= new Main();
		Scanner kb= new Scanner(System.in);
		int n= kb.nextInt();
		ArrayList<Point> arr= new ArrayList<>(); // Point 는 객체지만 compareTo method 를 override 했기 때문에 정렬이 가능해진다.
		for(int i=0; i<n; i++) {
			int x=kb.nextInt();
			int y=kb.nextInt();
			arr.add(new Point(x,y));
		}

		Collections.sort(arr);
		for(Point o : arr) {
			System.out.println(o.x+" "+o.y);
		}
		
	}

}
```
