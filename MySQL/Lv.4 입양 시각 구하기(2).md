> 프로그래머스 - 입양 시각 구하기(2) [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59413)]

# 입양 시각 구하기(2)

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186597899-6c4b8826-21b8-4c71-9d99-0a68f0db8922.png">
<img src="https://user-images.githubusercontent.com/86038910/186597951-dec0b968-f84d-4ae7-98b8-b966d41a8cd1.png">
</details>

### QUERY

#### 틀린 문제
- HAVING 조건절 없이 QUERY문을 작성하면 존재하는 시간대의 데이터만 출력되어 오답.
- 조건절 HAVING으로 HOUR컬럼의 출력 데이터는 존재하는 데이터만 출력이 되기 때문에 SET을 해줘야 한다. 
```MYSQL
SELECT HOUR(DATETIME) AS HOUR, COUNT(HOUR(DATETIME)) AS COUNT
FROM ANIMAL_OUTS
GROUP BY HOUR
#HAVING 0 < HOUR AND HOUR < 24
ORDER BY HOUR
```

#### reference SET
```MYSQL
SET @hour := -1; -- 변수 선언

SELECT (@hour := @hour + 1) as HOUR,
(SELECT COUNT(*) FROM ANIMAL_OUTS WHERE HOUR(DATETIME) = @hour) as COUNT
FROM ANIMAL_OUTS
WHERE @hour < 23
```
