# TIL 정리하기

> 파이썬 기초부터 정리하기 -5
>
> \>> 리스트 list 관련 함수들
>



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

- 리스트 확장 --> 한꺼번에 여러 요소들을 삽입하고 싶을 때
- 사용 :  .extend(넣고자 하는 요소들의 리스트)

```python
>>> colors = ['blue', 'pink', 'black', 'red']
>>> colors.extend(['white', 'gold', 'silver'])
>>> colors
['blue', 'pink', 'black', 'red', 'white', 'gold', 'silver']

```



_분명 학습했던 것들인데, 다시금 복습하자니 헷갈리는 부분들도 많고 유용한 기능들을 그동안 쓰지 못했던 것 같아서 억울(?)한 기분이 들었다ㅋㅋ,,,,앞으로 잊지 말고 꼭 사용하자!_

_독서모임에서 새로운 책은 구병모 작가의 파과가 선정되었다. 광기의 역사 같은 철학서를 읽다가 소설책을 읽게 되어 정말 기쁘다......앞으로 책을 선정할 때는, 적어도!! 서문 정도는 읽어보고 선정하자는 중요한 교훈을 얻었다. 휴._



