> 프로그래머스 - x만큼 간격이 있는 n개의 숫자 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/12954)]

# x만큼 간격이 있는 n개의 숫자

<details markdown="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/185315984-ae1062c7-a99a-4e57-a4b7-3eb3595c18b5.png">
</details>

### 코드
ex1
```java
class Solution {
    public long[] solution(int x, int n) {
        long[] answer = new long[n];
        for(int i = 0; i < answer.length; i++) {
            answer[i] = (long)x * (i + 1);
        }
        return answer;
    }
}
```
