# TIL 정리하기

> 파이썬 기초부터 정리하기 -5
>
> \>> 리스트 list 관련 함수들
>
> \+ 오늘의 알고리즘 문제 풀이



#### 리스트 관련 함수들

1. `sort()`

- 리스트 정렬

```python
>>> a = [1, 5, 2, 4]
>>> a.sort()
>>> a
[1, 2, 4, 5]

>>> names = ['차이석', '기시현', '이도', '성현제']
>>> names.sort()
>>> names
['기시현', '성현제', '이도', '차이석']
```



2. `reverse()`

- 리스트 뒤집기

```python
>>> a = [5, 9, 1, 3]
>>> a.reverse()
>>> a
[3, 1, 9, 5]

>>> books = ['자유론', '모모', '정의란 무엇인가', '흠흠신서']
>>> books.reverse()
>>> books
['흠흠신서', '정의란 무엇인가', '모모', '자유론']
```



3. `index()`

- 위치 반환 
- 사용 : .index(위치를 찾고자 하는 요소)

```python
>>> desserts = ['cake', 'jelly', 'pudding', 'cookie']
>>> desserts.index('pudding')
2
>>> desserts.index('cake')
0

# list 내에 없는 요소를 값으로 넣었을 때 : 에러 발생
>>> desserts.index('chocolate')
Traceback (most recent call last):
  File "<pyshell#14>", line 1, in <module>
    desserts.index('chocolate')
ValueError: 'chocolate' is not in list
```



4. `insert()`

- 리스트에 요소 삽입 
- 사용 : .insert(인덱스 위치, 요소)

```python
>>> foods = ['pasta', 'kimbap', 'sushi', 'pizza']
>>> foods.insert(0,'chicken')
>>> foods
['chicken', 'pasta', 'kimbap', 'sushi', 'pizza']

>>> foods.insert(2, 'barbeque')
>>> foods
['chicken', 'pasta', 'barbeque', 'kimbap', 'sushi', 'pizza']
```



5. `remove()`

- 리스트 요소 제거
- 사용 : .remove(제거할 요소)

```python
>>> foods = ['pasta', 'kimbap', 'sushi', 'pizza']
>>> foods.remove('pizza')
>>> foods
['pasta', 'kimbap', 'sushi']

# 중복된 값이 있을 경우, 먼저 오는 값을 하나 삭제함
>>> numbers = [1, 2, 3, 1, 2, 3]
>>> numbers.remove(2)
numbers
[1, 3, 1, 2, 3]
```



6. `pop()`

- 리스트 요소 꺼내기 
- 사용 : .pop(꺼내고자 하는 인덱스 위치) --> 인덱스 위치를 입력하지 않으면 가장 끝의 요소를 빼냄

```python
>>> names = ['성현제', '한유진', '한유현', '송태원']
>>> names.pop() # 인덱스 위치 없이 기본값
'송태원'

# 꺼내어진 요소는 사라짐
>>> names
['성현제', '한유진', '한유현']


>>> names = ['성현제', '한유진', '한유현', '송태원']
>>> names.pop(0) # 인덱스 위치 0인 요소 꺼내기
'성현제'
>>> names
['한유진', '한유현', '송태원']
```



7. `count()`

- 리스트에 포함된 요소 x의 개수 세기
- 사용 : .count(세고자 하는 요소)

```python
>>> num = [1, 2, 3, 3]
>>> num.count(3)
2
```



8. `extend()`

- 리스트 확장
- 사용 : 











