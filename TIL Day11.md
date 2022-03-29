# TIL 정리하기

>파이썬 기초부터 정리하기 -7
>
>\>> 딕셔너리 Dictionary 
>



### 딕셔너리 자료형

> 딕셔너리 구조

- { Key1: Value1, Key2: Value2, Key3: Value3, ....}

```python
>>> information = {'name': '이준혁', 'job': '배우', 'gender': '남성'}

>>> dic1 = {1: 'BeBe', 2: 'Rexha'}

>>> dic2 = {'S': ['한유진', '한유현', '성현제']}
```



- 딕셔너리 쌍 추가하기

```python
>>> a = {1: 'one'}
>>> a[2] = 'two'
>>> a
{1: 'one', 2: 'two'}

>>> a['name'] = '강동원'
>>> a
{1: 'one', 2: 'two', 'name': '강동원'}
```

- 딕셔너리 요소 삭제하기

```python
>>> some = {'이름': '이제훈', '직업': '배우', '성별': '남성'}
>>> del some['이름']
>>> some
{'직업': '배우', '성별': '남성'}
```



#### 딕셔너리 제어

- 딕셔너리에서 Key 사용하여 Value 얻기

```python
>>> grade = {'성현제': 100, '한유진': 77, '한유현': 100}
>>> grade['한유진'] 
>>> 77
>>> grade['성현제']
>>> 100
```



#### 딕셔너리 생성 시 주의사항

- 딕셔너리의 key값이 될 수 있는 것은 오직 변경이 불가한 자료 타입!
  - 즉, 변경이 가능한 리스트는 key값이 될 수 없다 >> 대신 튜플을 사용!

```python
>>> a = {[1, 2, 3]: 'one, two, three'}
Traceback (most recent call last):
  File "<pyshell#0>", line 1, in <module>
    a = {[1, 2, 3]: 'one, two, three'}
TypeError: unhashable type: 'list'
```

- key값은 고유해야 한다. 즉, 중복된 key 값을 사용할 수 없다. 가장 뒤의 것만이 저장됨!

```python
>>> a = {'이우연': '가수', '이준혁': '배우', '이우연': '배우'}
>>> a
{'이우연': '배우', '이준혁': '배우'}
```



#### 딕셔너리 관련 함수들

1. `keys()`

- Key 리스트 만들기 

```python
>>> grade = {'이우연': 100, '성현제': 99, '유중혁': 88}
>>> grade.keys()
dict_keys(['이우연', '성현제', '유중혁'])

# for문을 이용해 출력하기
>>> for k in grade.keys():
    print(k)
    
이우연
성현제
유중혁

# key 값으로 리스트 생성
>>> list(grade.keys())
['이우연', '성현제', '유중혁']
```



2. `values()`

- Value 리스트 만들기

```python
>>> grade = {'이우연': 100, '성현제': 99, '유중혁': 88}
>>> grade.values()
dict_values([100, 99, 88])
```



3. `items()`

- Key, Value 쌍 얻기

```python
>>> grade = {'이우연': 100, '성현제': 99, '유중혁': 88}
>>> grade.items()
dict_items([('이우연', 100), ('성현제', 99), ('유중혁', 88)])

# 리스트로 생성 시, key와 value가 튜플로 묶여 들어감
>>> list(grade.items())
[('이우연', 100), ('성현제', 99), ('유중혁', 88)]
```



4. `clear()`

- Key: Value 쌍 모두 지우기

```python
>>> grade = {'이우연': 100, '성현제': 99, '유중혁': 88}
>>> grade.clear()
>>> grade
{}
```



5. `get()`

- Key로 Value 얻기
- key값이 없을 때, get() 함수의 두 번째 인자로 특정값을 정해주면 해당 값을 대신 반환

```python
>>> grade = {'성현제': 'S', '한유진': 'F', '한유현': 'S', '박예림': 'S'}
>>> grade.get('한유진')
'F'
>>> grade.get('박예림')
'S'

# 없는 key값을 불러올 경우 None을 반환
>>> print(grade.get('송태원'))
None

# key값이 없을 때, get() 함수의 두 번째 인자로 특정값을 정해주면 해당 값을 대신 반환
>>> grade.get('송태원', '없음')
'없음'

# 반면 get() 함수가 아닌, '딕셔너리이름[key값]'의 방법으로 없는 key 값을 불러올 경우, Error 발생
>>> grade['송태원']
Traceback (most recent call last):
  File "<pyshell#20>", line 1, in <module>
    grade['송태원']
KeyError: '송태원'
```



6. `in`

- 해당 Key가 딕셔너리 안에 있는지 조사하기

```python
>>> dessert = {1: 'cake', 2: 'macaron', 3: 'pudding'}
>>> 3 in dessert
True

>>> 5 in dessert
False
```





_새로운 책 파과를 읽기 시작했다. 역시 소설이 최고인 것 같다....... 건조한 문체가 매우 마음에 든다. 인물들의 성격도 과장없이 적당히 현실적이고 입체적으로 묘사되어 내 취향에 굉장히 들어맞는 글이다. 묘한 분위기를 가진 주인공 '조각'은 악인이 맞지만, 자꾸 호감이 든다. 작가가 '악의 평범성'을 의도했을 것이라고 생각하지만, 뭐......진짜 정답일지는 알 수 없다. 저자의 인터뷰가 있다면 책을 다 읽은 후 찾아봐야 겠다._



---







