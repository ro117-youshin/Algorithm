> 프로그래머스 - 어린 동물 찾기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59037)]

# 어린 동물 찾기 

<details markdown = "1">
<summary>문제 설명 보기</summary>
<img src ="https://user-images.githubusercontent.com/86038910/185854701-db411619-a144-4bf5-b2b4-e03bcb6916bb.png">
<img src ="https://user-images.githubusercontent.com/86038910/185854771-0ad3a098-c2bf-408a-8e79-5710af8f37a7.png">
</details>

### 코드
#### ex WHERE NOT
```MySQL
SELECT ANIMAL_ID, NAME 
FROM ANIMAL_INS 
WHERE NOT INTAKE_CONDITION = 'Aged' 
ORDER BY ANIMAL_ID;
```

#### ex WHERE ~ NOT LIKE
```MYSQL
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION NOT LIKE 'Aged'
ORDER BY ANIMAL_ID
```
