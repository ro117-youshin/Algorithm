> 프로그래머스 - 있었는데요 없었습니다 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59043)]

# 있었는데요 없었습니다

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186578761-d72a1fc4-928a-478e-a767-c2708d6d6c9d.png">
<img src="https://user-images.githubusercontent.com/86038910/186578809-c589080e-3f00-48a1-98e5-adb2b1d9392a.png">
</details>

### QUERY
```MYSQL
SELECT INS.ANIMAL_ID, INS.NAME
FROM ANIMAL_INS AS INS
LEFT JOIN ANIMAL_OUTS AS OUTS
ON INS.ANIMAL_ID = OUTS.ANIMAL_ID
WHERE INS.DATETIME > OUTS.DATETIME
ORDER BY INS.DATETIME;
```
