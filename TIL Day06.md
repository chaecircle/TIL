# TIL 정리하기

> 오늘은 알고리즘 문제 풀이만



```python
# dictionary practice -1

animations = {
    'Pokemon': 'Pikachu',
    'Digimon': 'Agumon',
    'Yugioh': 'Black Magician'
}

word = input()
print(animations.get(word,"I don't know"))
```

```python
# dictionary practice -2

num = int(input())
nat_cap = {}

for i in range(num):
    word = input().split()
    nat_cap[word[0]]= word[1]

word = input()
print(nat_cap.get(word,'Unknown Country'))

## for문 안에 살짝 다른 방법

for i in range(num):
    country, city = input.split()
    nat_cap[country] = city
```

```python
# dictionary practice -3

foul = input().split()
foul_record = {}


for i in foul: 
    if i not in foul_record.keys():
        foul_record[i] = 1
    else:
        foul_record[i] += 1

min_foul = min(foul_record.values())

for i in foul_record.keys():
    if foul_record[i] == min_foul :
        print(i)

print(min_foul)
```

```python
# 유학 금지 백준 2789번

word = input()
del_word = list('CAMBRIDGE')
new_word = ''

for i in range(len(word)):
    if word[i] not in del_word:
        new_word += word[i]

print(new_word)

## 문자열 메서드 replace 이용한 방법2

word = input()

for i in 'CAMBRIDGE':
    word = word.replace(i,'')

print(word)
```

```python
# 태보태보 총난타 백준 17249번

taebo = input()
left, right = taebo.split('(')

l_num = left.count('@')
r_num = right.count('@')

print(l_num, r_num)
```



_오늘 풀이한 알고리즘 문제들. 뭔가 안 풀리다가 풀리는 게 참 재밌다_
