> 프로그래머스 - 없어진 기록 찾기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59042)]

# 없어진 기록 찾기

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186558810-636c4666-ce10-46fe-891e-e2f0f633b40f.png">
<img src="https://user-images.githubusercontent.com/86038910/186558847-34954c55-9985-4208-9497-a11a73359fa6.png">
</details>

### QUERY
```MYSQL
SELECT OUTS.ANIMAL_ID, OUTS.NAME
FROM ANIMAL_OUTS AS OUTS
LEFT JOIN ANIMAL_INS AS INS
ON OUTS.ANIMAL_ID = INS.ANIMAL_ID
WHERE INS.ANIMAL_ID IS NULL;
```
------------------------------------------------------------------------------------------------------------------

### JOIN

<img src = "https://velog.velcdn.com/images%2Fpm1100tm%2Fpost%2Faad30135-f344-4aa9-9bea-0e89cf7535e1%2FScreen%20Shot%202021-01-15%20at%202.09.40%20PM.png">
