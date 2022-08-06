> 프로그래머스 - [Java]어서와! 자료구조 알고리즘은 처음이지? [[링크](https://school.programmers.co.kr/learn/courses/13577)] 

# List 01.
## 최대값 인덱스 구하기
주어진 입력중 최대값을 구하고, 최대값이 위치하는 index값의 목록을 반환하기
* input : [1, 3, 7, 4, 7, 2, 1]
* output : [2, 4]

### ex1

```java
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
```

```java
class Solution {
	
    public static int[] solution(int[] arr) {
		// 최대값 저장할 변수
                int max = 0;
		for(int a : arr) if(a > max) max = a;
		// 최대값 개수 확인을 위한 변수
		int count = 0;
		for(int a : arr) if(a == max) count++;
		// 배열 생성
		int[] answer = new int[count];
		// 배열에 인덱스 채우기
		int index = 0;
		for(int i = 0; i < arr.length; i++) {
			if(arr[i] == max) answer[index++] = i;
		}
		
		return answer;
	}
    
}
```
