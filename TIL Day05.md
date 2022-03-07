# TIL 정리하기

> 파이썬 기초부터 정리하기 -2
>
> \+ 알고리즘 문제 풀이



### 문자열 자료형 

> 이어서 



#### 문자열 포매팅

1. __`%` 를 활용한 포매팅__

> 문자열 포맷 코드

- `%s` : 문자열 String
- `%c` : 문자 1개 character
- `%d` : 정수 integer
- `%f` : 부동소수 floating-point
- `%o` : 8진수
- `%x` : 16진수
- `%%` : 문자 % 자체

```python
>>> "I have %s peaches." % 5
'I have 5 peaches.'

>>> number1 = 10
>>> number2 = 5
>>> "She has %d apples and %d oranges." % ( number1, number2)
'She has 10 apples and 5 oranges.'

>>> "Probability is %d%%." % 95
'Probability is 95%.'
```

> 포맷 코드와 숫자 함께 사용하기 

- __정렬과 공백__

```python
>>> "%10s" % "run"
'       run' (공백과 'run' 합쳐서 10자리가 되도록 공백 생성하여 오른쪽 정렬)

>>> "%-10sYujin" % "run"
'run       Yujin' (왼쪽 정렬)
```

- __소수점 표현하기__

```python
>>> "%0.4f" % 9.76539
'9.7654'

>>> "%10.4f" % 9.76539
'    9.7654'
```

---



2. __`format` 함수를 활용한 포매팅__

- __대입하기__

```python
>>> "I ate {0} peaches".format(3)
'I ate 3 peaches'

>>> number = 9
>>> "She ate {0} apples.".format(number)
'She ate 9 apples.'

# 두 개 이상의 값 넣기
>>> number = 3
>>> name = 'Sejin'
>>> "He has {0} brothers and he's name is {1}".format(number, name)
"He has 3 brothers and he's name is Sejin."

# 이름으로 넣기 
>>> "She ate {number} apples, so I was sick for {day} days.".format(number=10, day=3)
'I ate 10 apples, so I was sick for 3 days.'
```

- __정렬과 공백__

```python
# 왼쪽 정렬
>>> "{0:<10}".format('hello')
'hello     '

# 오른쪽 정렬
>>> "{0:>10}".format('hello')
'     hello'

# 가운데 정렬
>>> "{0:^10}".format('hello')
'  hello   '

# 공백 채우기
>>> "{0:=^10}".format('blue')
'===blue==='

>>> "{0:!<10}".format('blue')
'blue!!!!!!'
```

- __소수점 표현하기__

```python
>>> y = 5.56789
>>> "{0:.4f}".format(y)
'5.5679'

>>> "{0:10.4f}".format(5.56789)
'    5.5679'

# { 또는 } 문자 그대로 표현하기
>>> "{{ and }}".format()
'{ and }'
```

---



3. __`f` 포매팅 (파이썬 버전 3.6부터 사용 가능)__

   - __대입하기__

   ``` python
   >>> name = '성현제'
   >>> age = 38
   >>> f'나의 이름은 {name}입니다. 나이는 {age}입니다.'
   '나의 이름은 성현제입니다. 나이는 38입니다.'
   
   >>> age = 30
   >>> f'나는 내년이면 {age+1}살이 된다.'
   '나는 내년이면 31살이 된다.'
   
   # 딕셔너리 활용
   >>> d = {'name': '이준혁', 'age': '34'}
   >>> f'그의 이름은 {d["name"]}입니다. 나이는 {d["age"]}입니다.'
   '그의 이름은 이준혁입니다. 나이는 34입니다.'
   ```

   - __정렬과 공백__

   ```python
   >>> f'{"carat":<10}'
   'carat     '
   
   >>> f'{"carat":>10}'
   '     carat'
   
   >>> f'{"carat":^10}'
   '  carat   '
   
   >>> f'{"fish":*^10}'
   '***fish***'
   
   >>> f'{"fish":!<10}'
   'fish!!!!!!'
   ```

   - __소수점 표현__

   ```python
   >>> s = 5.7894999
   >>> f'{s:.4f}'
   '5.7895'
   
   >>> f'{0.7933:.3f}'
   '0.793'
   ```

   

   _헷갈렸던 점이 많았던 부분이었는데, 이제 문자열 포매팅을 익숙하게 사용할 수 있을 것 같다. 앞으로 꾸준히 사용해보는 것이 중요할 것 같다. 특히 마지막 방법인  f 포매팅!_

   

   ---

   > 오늘 풀이한 알고리즘 문제

   ```python
   # 나무 조각 백준 2947번
   ## 코드 더 간단하게 고쳐보기
   
   order = list(map(int, input().split()))
   
   while order!= sorted(order):
       for i in range(len(order)):
           change_num = order[i]
           
       	if i!=4 and order[i] > order[i+1]:
   			order[i] = order[i+1]
         		order[i+1] = change_num
               
       	if order[i]!=change_num:
         		for j in order:
           		print(j, end=" ")
                   
        		print()
   ```

   ```python
   # 나는 요리사다 백준 2953번
   
   scores_tot = []
   
   for i in range(5):
       score = list(map(int, input().split()))
       scores_tot.append(sum(score))
       
   print(scores_tot.index(max(scores_tot))+1,max(scores_tot))
   
   ```

   ```python
   # 평균은 넘겠지 백준 4344번
   
   c = int(input())
   
   for i in range(c):
       score = list(map(int, input().split()))
       average = sum(score[1:])/score[0]
       number = 0
       for j in score[1:]:
           if j > average:
               number += 1
       print("%.3f%%" %(number/score[0]*100))
   ```

   

   

   

   

