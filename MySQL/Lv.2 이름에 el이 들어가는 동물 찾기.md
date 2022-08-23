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
-------------------------------------
특정 부분이 일치하는 데이터를 찾고싶을때는 <STRONG>LIKE</STRONG>를 이용하게 된다. 이때 _ 혹은 %를 이용하게 됩니다.

### _는  _ 의 개수만큼 데이터가 있다는 뜻이다.

#### __ EL __ 
- EL앞에 2글자 뒤에 2글자가 있어야 한다.

### %는 글자수와 상관없이 찾게 된다.

#### %EL 
- 끝자리가 EL인 데이터 찾기.
#### EL%
- 처음이 EL인 데이터 찾기.
#### %EL%
- 어딘가에 EL이 들어있는 데이터 찾기.
