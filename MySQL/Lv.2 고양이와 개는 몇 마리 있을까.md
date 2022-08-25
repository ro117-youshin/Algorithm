> 프로그래머스 - Lv.2 고양이와 개는 몇 마리 있을까 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59040)]

# 고양이와 개는 몇 마리 있을까
<details markdown="1">
<summary>문제 설명 보기</summary>
<img src ="https://user-images.githubusercontent.com/86038910/185874969-a5d9b8bd-3a95-4a67-a6f2-d31df13936f6.png">
<img src ="https://user-images.githubusercontent.com/86038910/185875101-78cc7f68-44f5-4fb0-a9fd-3a6f1e7ad3fe.png">
</details>

### QUERY
#### ex
```mysql
SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE) AS count 
FROM ANIMAL_INS 
WHERE ANIMAL_TYPE = "Cat" OR ANIMAL_TYPE = "Dog" 
GROUP BY ANIMAL_TYPE 
ORDER BY ANIMAL_TYPE;
```

#### reference
- 기존 풀이에서 WHERE절을 넣을 필요 X. (TYPE 자체가 Cat과 Dog만 있기 때문)
- ANIMAL_TYPE 컬럼의 유형별 개수를 알고 싶기 때문에 GROUP BY로 그룹화 필요.
- 고양이를 개보다 먼저 조회하라는 조건이 있기 때문에 ORDER BY로 정렬 필요.
```MYSQL
SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE) AS count 
FROM ANIMAL_INS
GROUP BY ANIMAL_TYPE
ORDER BY ANIMAL_TYPE
```
