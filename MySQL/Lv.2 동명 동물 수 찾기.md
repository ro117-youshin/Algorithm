> 프로그래머스 - 동명 동물 수 찾기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59041)]

# 동명 동물 수 찾기

<details markdown="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186182279-5a15deac-9bf4-4264-b8f0-37d731741e0b.png">
<img src="https://user-images.githubusercontent.com/86038910/186182519-b5a144b6-1dbc-4b6e-80fa-bf77a80abd85.png">
</details>

### QUERY
```MYSQL
SELECT NAME, COUNT(NAME) AS COUNT 
FROM ANIMAL_INS 
GROUP BY NAME
HAVING COUNT(NAME) > 1
ORDER BY NAME;
```
