> 프로그래머스 - 오랜 기간 보호한 동물(1) [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59044)]

# 오랜 기간 보호한 동물(1)

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186577412-85109b30-5087-4367-ac39-313ff08379dc.png">
<img src="https://user-images.githubusercontent.com/86038910/186577466-e7c5ab0e-b930-4190-aafb-f7160fd9869d.png">
</details>

### QUERY
```MYSQL
SELECT INS.NAME, INS.DATETIME
FROM ANIMAL_INS AS INS
LEFT JOIN ANIMAL_OUTS AS OUTS
ON INS.ANIMAL_ID = OUTS.ANIMAL_ID
WHERE OUTS.ANIMAL_ID IS NULL
ORDER BY INS.DATETIME
LIMIT 3;
```
