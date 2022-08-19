> 프로그래머스 - 완주하지 못한 선수 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/42576)]

# Map 02.
## 완주하지 못한 선수
<details markdown="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/185528640-f37cdcf4-3ca6-4463-b43f-372781d8069d.png">
<img src="https://user-images.githubusercontent.com/86038910/185528771-b76a3e45-c267-4415-9248-27e42d1a3d45.png">
</details>

### 코드

ex1 시간복잡도 O(nlongn)
```java
import java.util.*;
class Solution {
    public String solution(String[] participant, String[] completion) {
        Arrays.sort(participant);
        Arrays.sort(completion);
        for (int i = 0; i = completion.length; i++) {
            if (!participant[i].equals(completion[i])) return participant[i];
        }
        return participant[participant.length - 1];
    }
} 

```

Reference 시간복잡도 O(n)
```java
class Solution {
    public String solution(String[] participant, String[] completion) {
        Map<String, Integer> players = new HashMap<>();
        for (String p : participant) {
            players.put(p, players.getOrDefault(p, 0) + 1);
        }
        for (String c : completion) {
            int n = players.get(c) - 1;
            if (n == 0) players.remove(c);
            else players.put(c, n);
        }
        return players.keySet().iterator().next();
    }
}
```
