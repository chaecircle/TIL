# TIL 정리하기

> 파이썬 기초부터 정리하기 -3 
>
> \>> 문자열 관련 함수들
>
> \+ 오늘의 알고리즘 문제 풀이



## 문자열 관련 함수들

1. `count()`

- __문자 개수 세기__

```python
>>> a = 'carat'
>>> a.count('a')
2
```



2. `find()`

- __위치 알려주기 1__

```python
>>> a = "I love Dokja."
>>> a.find('D')
7

# 문자열 내에 없는 문자의 경우 -1을 반환
>>> a.find('S')
-1
```

- __문자열 내에 없는 문자의 경우 -1을 반환한다!__



3. `index()`

- __위치 알려주기 2__

```python
>>> k = 'Sejin is beautiful.'
>>> k.index('j')
2

# 문자열 내에 없는 문자의 경우 에러 발생!
>>> k.index('A')
Traceback (most recent call last):
  File "<pyshell#1>", line 1, in <module>
    k.index('A')
ValueError: substring not found
```

- __find와 달리 문자열 내에 없는 문자의 경우 에러가 발생한다!__



4. `join()`

- __문자열 삽입__

```python
>>> ','.join('carat')
'c,a,r,a,t'

>>> "!".join(['c','a','r','a','t'])
'c!a!r!a!t'
```



5. `upper()`

- 소문자를 대문자로 바꾸기

```python
>>> s = 'iseock'
>>> s.upper()
'ISEOCK'
```



6. `lower()`

```python
>>> s = 'MICHAEL'
>>> s.lower()
'michael'

>>> a = 'TKfkdGO'
>>> a.lower()
'tkfkdgo'

```



7. `strip()`

- 공백 지우기

```python
# 양쪽 공백 지우기 
>>> a = '   go away!   '
>>> a.strip()
'go away!'

# 왼쪽 공백 지우기
>>> a = '   go away!   '
>>> a.lstrip()
'go away!   '

# 오른쪽 공백 지우기
>>> a = '   go away!   '
>>> a.rstrip()
'   go away!'

```



8. `replace()`

- __문자열 바꾸기__

```python
>>> a = 'I love Healer.'
>>> a.replace("Healer", "Carat")
'I love Carat.'

# 없는 문자를 대상으로 하면 그대로 출력
>>> a.replace("Yujin", "Hyunjae")
'I love Helaer.'
```



9. `split()`

- 문자열 나누기 : 나눈 값을 하나의 리스트로 반환

```python
>>> t = 'We would pop champagne and raise a toast.'

# 기본값은 "공백"을 기준으로 문자열을 split 시킴!
>>> t.split()
['We', 'would', 'pop', 'champagne', 'and', 'raise', 'a', 'toast.']

# 무엇을 기준으로 split 할 지 정해줄 수 있음
>>> a = 'Adele,Ava,Taylor,Avril,Bebe'
>>> a.split(',')
['Adele', 'Ava', 'Taylor', 'Avril', 'Bebe']
```



__번외: print()에 대해__

- print() 는 출력의 명령어. 여러 문자열을 출력할 때, 그 사이에 들어갈 값을 정하는 `sep`과 문자열 출력이 끝나고 입력될 값을 정하는`end` 인자의 값을 지정하여 다양하게 활용할 수 있다. 

```python
# default 값 수정 없이 사용
>>> print('Ilhyun', 'Wuyeon', 'Wujin')
Ilhyun Wuyeon Wujin


# 기본값 sep = ' '(공백) --> sep = '\n' (줄 바꿈) 으로 변경
>>> print('Ilhyun', 'Wuyeon', 'Wujin', sep = '\n')
Ilhyun
Wuyeon
Wujin


# end 의 기본값 수정 없이 사용 (디폴트 값은 줄바꿈이므로 한 줄 한 줄 출력됨)
>>> for i in range(1):
    print('Ilhyun')
    print('Wuyeon')
    print('Wujin')
Ilhyun
Wuyeon
Wujin


# 기본값 end = '\n' --> end = ' ' (공백) 으로 변경
>>> for i in range(1):
    print('Ilhyun', end = ' ')
    print('Wuyeon', end = ' ')
    print('Wujin', end = ' ')
Ilhyun Wuyeon Wujin 

```









