# TIL 정리하기

> 파이썬 기초부터 정리하기 -8
>
> \>> 집합 Set
>
> \+ 파이썬 기초 100제 문제풀이



### 집합 Set 자료형



#### 집합 구조

- 중괄호 `{}` 로 둘러싸인 형태
- set() 함수로 집합을 생성
- 특징
  - 중복을 허용하지 않는다
  - 순서가 없다 Unordered

```python
>>> s1 = set([1, 2, 3])
>>> s1
{1, 2, 3}

>>> s2 = set('전지적독자시점')
>>> s2
{'지', '시', '독', '전', '적', '점', '자'}

>>> s2 = set('전지적 독자 시점')
>>> s2
{'지', '시', ' ', '독', '전', '적', '점', '자'}

```

- __교집합__ 구하기
  - `&` 사용
  - `intersection()` 사용

```python
>>> s1 = {1, 2, 3, 5}
>>> s2 = {2, 3, 4}

>>> s1 & s2
{2, 3}

>>> s1.intersection(s2)
{2, 3}
```

- __합집합__ 구하기
  - `|` 사용
  - `union()` 사용

```python
>>> s1 = {'사과', '복숭아', '망고', '체리'}
>>> s2 = {'복숭아', '리치', '수박', '망고'}

>>> s1 | s2
{'리치', '복숭아', '체리', '망고', '수박', '사과'}

>>> s1.union(s2)
{'리치', '복숭아', '체리', '망고', '수박', '사과'}
```

- __차집합__ 구하기
  - `-` 사용
  - `difference()` 사용

```python
>>> s1 = {'고양이', '강아지', '기린', '사자', '호랑이'}
>>> s2 = {'강아지', '기린', '사과'}

>>> s1 - s2
{'호랑이', '사자', '고양이'}

>>> s1.difference(s2)
{'호랑이', '사자', '고양이'}

>>> s2.difference(s1)
{'사과'}
```



_오늘의 느낀 점_





---





```python
5. 기초 출력 5

# "Hello World" 큰 따옴표 포함하여 출력하기

print('"Hello World"')

# 혹은

print("\"Hello World\"")

```

```python
6. 출력하기 6

# "!@#$%^&*()' 출력하기 (따옴표 모두 포함)

print('"!@#$%^&*()\'')

```

```python
7. 출력하기 7

# "C:\Download\'hello'.py" (단, 따옴표도 함께 출력한다.)

print('"C:\\Download\\\'hello\'.py"')

```

```python
8. 출력하기 8

# print("Hello\nWorld") 그대로 출력하기 



```




















