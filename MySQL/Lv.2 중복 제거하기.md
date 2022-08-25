> 프로그래머스 - 중복 제거하기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59408)]

# 중복 제거하기

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186555155-7b729892-da1d-4296-8d32-58a33f8c6e08.png">
<img src="https://user-images.githubusercontent.com/86038910/186555204-efb28c5d-dc2b-433f-9cf9-8022b3b69cf6.png">
</details>

### QUERY
```MYSQL
SELECT COUNT(DISTINCT NAME) AS count FROM ANIMAL_INS;
```

-----------------------------------------------------
#### DISTINCT (범주 조회)
- 컬럼 범주 조회
```MYSQL
SELECT DISTINCT 컬럼 FROM 테이블;
```
- 조건 처리 후, 컬럼 범주 조회
```MYSQL
SELECT DISTINCT 컬럼 FROM 테이블 WHERE 조건식;
```
- 컬럼 범주 개수 조회
```MYSQL
SELECT COUNT(DISTINCT 컬럼) FROM 테이블;
```
