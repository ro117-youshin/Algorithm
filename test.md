> 프로그래머스 - 어린 동물 찾기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59037)]

# 어린 동물 찾기 

<details markdown = "1">
<summary>문제 설명 보기</summary>
<img src ="">
</details>

```MySQL
SELECT ANIMAL_ID, NAME FROM ANIMAL_INS WHERE NOT INTAKE_CONDITION = "Aged" ORDER BY ANIMAL_ID;
```