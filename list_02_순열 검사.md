> 프로그래머스 - [Java]어서와! 자료구조 알고리즘은 처음이지? [[링크](https://school.programmers.co.kr/learn/courses/13577)] 
# List 02.
## 순열 검사
길이가 n인 배열에 1부터 n까지 숫자가 중복 없이 한 번씩 들어 있는지를 확인하려고 한다.
1부터 n까지 숫자가 중복 없이 한 번씩 들어 있는 경우 true를, 아닌 경우 false를 반환하도록 solution완성.
### 제한사항
* 배열의 길이는 10만 이하
* 배열의 원소는 0 이상 10만 이하인 정수이다.
### 입출력 예
|arr|result|
|--|--|
|[4, 1, 3, 2]|true|
|[4, 1, 3]|false|

### 입출력 설명
* 입출력 예 #1<br>
입력이 [4, 1, 3, 2]가 주어진 경우, 배열의 길이가 4이므로 배열에는 1부터 4까지 숫자가 모두 들어 있어야 합니다. [4, 1, 3, 2]에는 1부터 4까지의 숫자가 모두 들어 있으므로 true를 반환하면 됩니다.

* 입출력 예 #2<br>
[4, 1, 3]이 주어진 경우, 배열의 길이가 3이므로 배열에는 1부터 3까지 숫자가 모두 들어 있어야 합니다. [4, 1, 3]에는 2가 없고 4가 있으므로 false를 반환하면 됩니다.

### 시간복잡도
* O(nlogn)

### 코드
### ex1
```java
import java.util.*;
class Solution{
    public boolean solution(int[] arr) {
        int[] answer = new int[arr.length];
        for(int i = 0; i < arr.length; i++) answer[i] = i + 1; // O(n)
        Arrays.sort(arr); // O(nlongn)
        return Arrays.equals(answer, arr); // O(n)
    }
}
```
### ex2
```java
import java.util.Arrays;
class Solution {
    public boolean solution(int[] arr) {
        boolean answer = true;
        Arrays.sort(arr);
        for(int i = 0; i < arr.length; i++) {
            if(arr[i] != i + 1) {
                answer = false;
                break;
            }
        }
    }
}

```
