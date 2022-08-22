> 프로그래머스 - Lv.2 고양이와 개는 몇 마리 있을까 [[링크](https://school.programmers.co.kr/learn/courses/30/lessons/59040)]

# 고양이와 개는 몇 마리 있을까
<details markdown="1">
<summary>문제 설명 보기</summary>
<img src ="https://user-images.githubusercontent.com/86038910/185874969-a5d9b8bd-3a95-4a67-a6f2-d31df13936f6.png">
<img src ="https://user-images.githubusercontent.com/86038910/185875101-78cc7f68-44f5-4fb0-a9fd-3a6f1e7ad3fe.png">
</details>

### 코드
```mysql
SELECT ANIMAL_TYPE, COUNT(ANIMAL_TYPE) as count FROM ANIMAL_INS WHERE ANIMAL_TYPE = "Cat" OR ANIMAL_TYPE = "Dog" GROUP BY ANIMAL_TYPE ORDER BY ANIMAL_TYPE;
```
