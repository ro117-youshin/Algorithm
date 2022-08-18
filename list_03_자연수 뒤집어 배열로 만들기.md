> 프로그래머스 - [Java]어서와! 자료구조 알고리즘은 처음이지? [[링크](https://school.programmers.co.kr/learn/courses/13577)]  
# List 03.
## 자연수 뒤집어 배열 만들기

### 문제설명
자연수 n을 뒤집어 각 자리 숫자를 원소로 가지는 배열 형태로 리턴해주세요. 예를들어 n이 12345이면 [5,4,3,2,1]을 리턴합니다.

### 제한조건
* n은 10,000,000,000이하인 자연수입니다.

### 입출력 예
|n|result|
|--|--|
|12345|[5,4,3,2,1]|

### 코드

#### ex1
```java
import java.util.*;
class Solution {
    public int[] solution(long n) {
        String[] strArr = String.valueOf(n).split("");
        int[] answer = new int[strArr.length];
        int index = 0;
        for(int i = strArr.length - 1; i >= 0; i--) {
            answer[index++] = Integer.parseInt(strArr[i]);
        }     
        return answer;
    }
}
```

#### Reference
```java
public int[] solution(long n) {
    List<Integer> list = new LinkedList<>();
    while(n > 0) {
        list.add((int)(n % 10));
        n /= 10;
    }
    return list.stream().mapToInt(Integer::intValue).toArray();
}
```
