> 프로그래머스 - 문자열 내 p와 y의 개수 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/12916)]

# 문자열 내 p와 y의 개수
<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/187076152-3fbe4eb4-23b2-4817-a03e-63834c247557.png">
</details>

### 코드
```java
class Solution {
    boolean solution(String s) {
        boolean answer = true;
        String[] arr = s.split("");
        int numberOfP = 0;
        int numberOfY = 0;
        for (int i = 0; i < arr.length; i++) {
            if (arr[i].equals("p") || arr[i].equals("P")) numberOfP++;
            if (arr[i].equals("y") || arr[i].equals("Y")) numberOfY++;
        }
        if (numberOfP != numberOfY) answer = false;
        return answer;
    }
}
```
