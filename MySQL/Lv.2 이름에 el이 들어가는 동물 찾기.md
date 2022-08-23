> 프로그래머스 - 이름에 el이 들어가는 동물 찾기 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59047)]

# 이름에 el이 들어가는 동물 찾기

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186198605-b001ebaa-673b-4d93-818f-d2907ada013d.png">
<img src="https://user-images.githubusercontent.com/86038910/186198744-f695ad9b-d020-4b3a-b619-a68a38f2b062.png">
</details>

### QUERY
```MYSQL
SELECT ANIMAL_ID, NAME 
FROM ANIMAL_INS
WHERE ANIMAL_TYPE = 'Dog' AND NAME LIKE "%EL%"
ORDER BY NAME;
```
