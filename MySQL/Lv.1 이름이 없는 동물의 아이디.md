> 프로그래머스 - 이름이 없는 동물의 아이디 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59039)]

# 이름이 없는 동물의 아이디

<details markdown="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/185864405-a366f9c0-f42b-429a-b087-238317ec000b.png">
<img src="https://user-images.githubusercontent.com/86038910/185864520-07e8d25e-200e-4fb2-857f-369044f5b7db.png">
</details>

### 코드
```mysql
SELECT ANIMAL_ID
FROM ANIMAL_INS
WHERE NAME IS NULL
ORDER BY ANIMAL_ID
```
