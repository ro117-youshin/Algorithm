> 프로그래머스 - [Java]어서와! 자료구조 알고리즘은 처음이지? [[링크](https://school.programmers.co.kr/learn/courses/13577)] 

# List 01.
## 최대값 인덱스 구하기
주어진 입력중 최대값을 구하고, 최대값이 위치하는 index값의 목록을 반환하기
* input : [1, 3, 7, 4, 7, 2, 1]
* output : [2, 4]

### ex1 Array

```java
class solution {

	public int[] solution(int[] arr) {
	    int max = 0; // 최대값 저장
	    for (int a : arr) {
		if (a > max) {
		    max = a;
		}
	    }

	    int count = 0; // 최대값 개수 확인
	      for (int a : arr) {
		  if (a == max) {
		      count++;
		  }
	      }

	    int[] answer = new int[count]; // 배열 생성
	    int index = 0;

	    for (int i = 0; i < arr.length; i++) { // 배열 인덱스로 채우기
		if (arr[i] == max) {
		    answer[index++] = i;
		}
	    } 
	    return answer;
	}
	
}	
```

```java
class Solution {
	public static int[] solution(int[] arr) {
                int max = 0; // 최대값 저장할 변수
		for(int a : arr) if(a > max) max = a;
		int count = 0; // 최대값 개수 확인을 위한 변수
		for(int a : arr) if(a == max) count++;
		int[] answer = new int[count]; // 배열 생성
		int index = 0; // 배열에 인덱스 채우기
		for(int i = 0; i < arr.length; i++) {
			if(arr[i] == max) answer[index++] = i;
		}
		return answer;
	}
}
```

### ex2 List사용

```java
import java.util.*;

class Solution {
	public int[] solution(int[] arr) {
		int max = 0; // 최대값 구하기
		for(int a : arr) if (a > max) = a;
		List<Integer> list = new LinkedList<>(); // 리스트 만들기
		for(int i = 0; i < arr.length; i++) {
			if(arr[i] == max) list.add(i);
		}
		int[] answer = new int[list.size()]; // 리스트를 배열로 변환
		for(int i = 0; i < list.size(); i++) {
			answer[i] = list.get(i);
		}
		
		return answer;
	}
}

```

```java stream() 사용
import java.util.stream.*;

class Solution {
	public int[] solution(int[] arr) {
		int max = Arrays.stream(arr).max().getAsInt();
		return IntStream.range(0, arr.length)
			.filter(i -> arr[i] == max)
			.toArray();
	}
}

```
