> 프로그래머스 - 중성화 여부 파악하기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59409)]

# 중성화 여부 파악하기

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186206779-78b59fe9-bec0-448a-8ba7-83338c0dd1dd.png">
<img src="https://user-images.githubusercontent.com/86038910/186206851-497d5b2e-9fa7-4f86-b6fd-627d451205c7.png">
</details>

### QUERY
#### ex1 CASE 사용 
```MYSQL
SELECT ANIMAL_ID, NAME, 
CASE 
    WHEN SEX_UPON_INTAKE LIKE "NE%" OR SEX_UPON_INTAKE LIKE "SP%" THEN 'O' 
    ELSE 'X' 
END AS 중성화
FROM ANIMAL_INS;
```
#### ex2 IF 사용
```MYSQL
SELECT ANIMAL_ID, NAME, 
IF(SEX_UPON_INTAKE LIKE '%NEUTERED%' OR SEX_UPON_INTAKE LIKE '%SPAYED%','O','X') AS 중성화
FROM ANIMAL_INS;
```

--------------------------------------------------------------------
#### MySQL CASE Function
Syntax
```MYSQL
CASE
    WHEN condition1 THEN result1
    WHEN condition2 THEN result2
    WHEN conditionN THEN resultN
    ELSE result
END;
```

#### MySQL IF() Function
Syntax
```mysql
IF(condition, value_if_true, value_if_false)
```
