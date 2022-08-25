> 프로그래머스 - 여러 기준으로 정렬하기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59404)]

# 여러 기준으로 정렬하기

<details markdown="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/185858102-96229d35-7019-405e-ae1d-7b8b6b6004fd.png">
<img src="https://user-images.githubusercontent.com/86038910/185858203-d51b85f9-cacb-44be-9cbd-545f86bf1fc4.png">
</details>

### 코드
```mysql
SELECT ANIMAL_ID, NAME, DATETIME
FROM ANIMAL_INS
ORDER BY NAME ASC, DATETIME DESC;
```
