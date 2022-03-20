# TIL 정리하기

> 파이썬 기초부터 정리하기 -6
>
> \>> 튜플 tuple 자료형



#### 튜플 tuple의 구조

- `(  )`로 둘러싸인 형태

```python
>>> t1 = ()
>>> t2 = (1, )
>>> t3 = (1, 2, 3)
>>> t4 = 1, 2, 3
>>> t5 = ('a','b', ('dd','gg'))
```

- 튜플은 __변형이 불가__

```python
# 튜플 요소를 삭제하려 할 때
>>> t = (1, 2, 'a')
>>> del t[0]
Traceback (most recent call last):
  File "<pyshell#3>", line 1, in <module>
    del t[0]
TypeError: 'tuple' object doesn't support item deletion
    
# 튜플 요소를 변경하려 할 때
>>> t2 = (1, 2, 3)
>>> t2[0] = 'c'
Traceback (most recent call last):
  File "<pyshell#5>", line 1, in <module>
    t2[0] = 'c'
TypeError: 'tuple' object does not support item assignment
```



#### 튜플 조작하기

- 인덱싱하기

```python
>>> t1 = (1, 2, 'a', 'z')
>>> t1[1]
2
```

- 슬라이싱하기

```python
>>> names = ('유중혁', '김독자', '한수영', '제천대성')
>>> names[1:]
('김독자', '한수영', '제천대성')
```

- 튜플 더하기

```python
>>> stars1 = ('우리엘', '하데스', '페르세포네')
>>> stars2 = ('이순신', '디오니소스', '흑염룡')
>>> stars1 + stars2
('우리엘', '하데스', '페르세포네', '이순신', '디오니소스', '흑염룡')
```

- 튜플 곱하기

```python
>>> names = ('차일현', '권제혁', '윤승호')
>>> names * 2
('차일현', '권제혁', '윤승호', '차일현', '권제혁', '윤승호')
```

- 튜플 길이 구하기

```python
>>> t1 = (1, 2, 3, 4, 5)
>>> len(t1)
5
```



#### 튜플 패킹과 언패킹

- 튜플 생성과 할당의 또 다른 방법들!

- 패킹 Packing

```python
>>> names = '나뭇가지', '가지가지'
>>> names
('나뭇가지', '가지가지')
>>> type(names)
<class 'tuple'>
```

- 언패킹 Unpacking

```python
>>> wood, stick = names
>>> wood
'나뭇가지'
>>> stick
'가지가지'
```

```python
# 이런 방식으로 다수의 변수 할당을 한 줄로 작성할 수 있다!
>>> name, age, job = '성현제', 38, 'sesung master'
>>> name
'성현제'
>>> age
38
>>> job
'sesung master'
```



_튜플은 리스트에 비해 직접적으로 사용해본 적이 많지 않은데, 앞으로 좀 더 사용하여 익숙해지는 과정을 밟아야겠다._







