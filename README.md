# Priority Queue

## Example : 1

```java
import java.util.PriorityQueue;

public class App {

	public static void main(String[] args) {
		PriorityQueue<Integer> pq = new PriorityQueue<Integer>();
		pq.add(5);
		pq.add(10);
		pq.add(1);
		pq.add(9);
		pq.add(0);
		pq.add(-1);
		while(!pq.isEmpty()) {
			System.out.println(pq.poll());
		}
	}
}
```


## Example : 2

```java
import java.util.Comparator;
import java.util.PriorityQueue;

public class App {

	public static void main(String[] args) {
		Comparator<Integer> pqComparator = new Comparator<Integer>() {
            public int compare(Integer i1, Integer i2) {
                return i2 - i1;
            }
        };
        
		PriorityQueue<Integer> pq = new PriorityQueue<Integer>(pqComparator);
		pq.add(5);
		pq.add(10);
		pq.add(1);
		pq.add(9);
		pq.add(0);
		pq.add(-1);
		while(!pq.isEmpty()) {
			System.out.println(pq.poll());
		}
	}
}
```
