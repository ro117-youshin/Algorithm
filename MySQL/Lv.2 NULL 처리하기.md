> 프로그래머스 - NULL 처리하기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59410)]

# NULL 처리하기

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186204410-84c41d85-b040-4091-baa3-b4c04726d828.png">
<img src="https://user-images.githubusercontent.com/86038910/186204495-6720cbe9-8eac-4347-b0e6-e8e408376b76.png">
</details>

### QUERY
```MYSQL
SELECT ANIMAL_TYPE, IFNULL(NAME, "No name") AS NAME, SEX_UPON_INTAKE
FROM ANIMAL_INS;
```

#### IFNULL
- IFNULL에 검사할 값을 첫번째 인자로 넣고, 조건에 부합하면 출력 할 내용을 두번째 인자로 넣어준다.
