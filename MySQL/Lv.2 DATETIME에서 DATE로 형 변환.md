> 프로그래머스 - DATETIME에서 DATE로 형 변환 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59414)]

# DATETIME에서 DATE로 형 변환

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/186556675-736e5172-6a47-42f8-ab9c-48c91e0c0048.png">
<img src="https://user-images.githubusercontent.com/86038910/186556776-37f113c3-b0b5-4656-8a59-f7492ff9fbef.png">
</details>

### QUERY
```MYSQL
SELECT ANIMAL_ID, NAME, DATE_FORMAT(DATETIME, '%Y-%m-%d') AS 날짜 
FROM ANIMAL_INS
ORDER BY ANIMAL_ID;
```

----------------------------------
#### DATE_FORMAT

```MYSQL
'%Y' (4자리 연도)
'%y' (2자리 연도)
'%m' (2자리 월, 00 - 12)
'%M' (월 이름, January, February ...)
'%b' (월 줄인 이름)
'%d' (일)
'%H' (24시간)
'%h' (12시간)
'%i' (분)
'%s' / '%S' (초)
```
