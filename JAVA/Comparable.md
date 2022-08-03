# Comparable 과 Comparator의 이해
> Comparable과 Comparator는 모두 인터페이스(interface).
> Comparable 혹은 Comparator을 사용하고자 한다면 인터페이스 내에 선언된 메소드를 '반드시 구현'.
> Comparable 인터페이스를 쓰려면 compareTo 메소드를 구현해야하고, Comparator 인터페이스를 쓰려면 compre 메소드를 구현해야 한다.


### Comparable
> "객체를 비교할 수 있도록 만든다." 로 설명이 끝나는 인터페이스.
> 새로운 클래스 객체를 만들어 비교하고자 한다면 해당 인터페이스를 impl 받아서 사용 해야 한다.
> compareTo method를 override 해서 정렬 기준을 정할 수 있다 ex) 오름차순, 내림차순.

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

