> 프로그래머스 - 아픈 동물 찾기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59036)]

# 아픈 동물 찾기

<details markdown="1">
<summary>문제 설명 보기</summary>
<img src ="https://user-images.githubusercontent.com/86038910/185856187-d5664ff4-30a5-4e32-99c6-c0160dc47e89.png">
<img src ="https://user-images.githubusercontent.com/86038910/185856291-1f4d5153-bbaf-470c-adef-155b96f4522d.png">
</details>

### 코드
```mysql
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION = 'Sick'
ORDER BY ANIMAL_ID
```
