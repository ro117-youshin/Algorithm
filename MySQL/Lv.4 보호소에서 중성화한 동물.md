> 프로그래머스 - 보호소에서 중성화한 동물 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59045)]

# 보호소에서 중성화한 동물

<details markdown ="1">
<summary>문제 설명 보기</summary>
<img src="https://user-images.githubusercontent.com/86038910/187062811-18bb41aa-16ab-4f0c-825f-f495dbc88977.png">
<img src="https://user-images.githubusercontent.com/86038910/187062894-76838cab-550f-4748-88c5-26a88f23e275.png">
<img src="https://user-images.githubusercontent.com/86038910/187062918-4de5ae70-085a-408c-9924-5383faac7336.png">
</details>

### QUERY
#### ex
```MYSQL
SELECT INS.ANIMAL_ID, INS.ANIMAL_TYPE, INS.NAME
FROM ANIMAL_INS AS INS
JOIN ANIMAL_OUTS AS OUTS
ON INS.ANIMAL_ID = OUTS.ANIMAL_ID
WHERE INS.SEX_UPON_INTAKE LIKE "Intact%" 
AND (OUTS.SEX_UPON_OUTCOME LIKE "Neutered%" OR OUTS.SEX_UPON_OUTCOME LIKE "Spayed%")   
ORDER BY INS.ANIMAL_ID;
```
#### ex2
```MYSQL
SELECT INS.ANIMAL_ID, INS.ANIMAL_TYPE, INS.NAME
FROM ANIMAL_INS AS INS
LEFT JOIN ANIMAL_OUTS AS OUTS
ON INS.ANIMAL_ID = OUTS.ANIMAL_ID
WHERE INS.SEX_UPON_INTAKE NOT LIKE OUTS.SEX_UPON_OUTCOME 
ORDER BY INS.ANIMAL_ID
```

#### reference
- 보호소에 들어올때와 나올때의 성별이 다른 동물을 찾는 방법 <BR>
(중성화가 아니라면 성별이 바뀌지 않는다.)

```MYSQL
SELECT INS.ANIMAL_ID, INS.ANIMAL_TYPE, INS.NAME 
FROM ANIMAL_INS AS INS 
JOIN ANIMAL_OUTS AS OUTS 
WHERE INS.ANIMAL_ID = OUTS.ANIMAL_ID AND INS.SEX_UPON_INTAKE != OUTS.SEX_UPON_OUTCOME
ORDER BY INS.ANIMAL_ID;
```
