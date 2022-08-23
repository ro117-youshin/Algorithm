> 프로그래머스 - 입양 시각 구하기(1) [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59412)]

# 입양 시각 구하기(1)

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186202561-88ecdc2b-c962-4e4c-8a3c-06459eb38bd5.png">
<img src="https://user-images.githubusercontent.com/86038910/186202687-a30ed4d2-5d27-465b-aea3-0849a3f9326b.png">
</details>

### QUERY
```MYSQL
SELECT HOUR(DATETIME) AS HOUR, COUNT(HOUR(DATETIME)) AS COUNT
FROM ANIMAL_OUTS
WHERE HOUR(DATETIME) >= 9 AND HOUR(DATETIME) <= 19
GROUP BY HOUR(DATETIME)
ORDER BY HOUR(DATETIME);
```
