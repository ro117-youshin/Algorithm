> 프로그래머스 - 올바른 괄호 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/12909)]

# Stack_01_올바른 괄호

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186638654-db740072-5466-46d3-9014-6044f14e8eb9.png">
</details>

### 코드
#### ex1 Stack 사용
```java
import java.util.Stack;
class Solution {
    boolean solution(String s) {
        Stack<Character> stack = new Stack<>();
        for (char c : s.toCharArray()) {
            if (c == '(') { 
                stack.push(c);
            } else {
                if (stack.isEmpty()) return false;
                stack.pop();
            }
        }
        return stack.isEmpty() == true;
    }
}
```

#### ex2 Stack의 성질을 정수로 대체하여 풀기
- 위의 예제에서 괄호를 push하고 pop하는 간단한 Stack의 성질을 이용, 간단한 Stack의 성질을 정수로 대체.
```java
class Solution {
    boolean solution(String s) {
        int stack = 0;
        for (char c : s.toCharArray()) {
            if (c == '(') {
                stack++;
            } else {
                if (stack == 0) return false;
                stack--;
            }
        }
        return stack == 0;
    }
}
```
