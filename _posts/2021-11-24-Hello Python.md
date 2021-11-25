---
layout: single
title: Python 기본문법 (문자열, 컬렉션, 조건문, 반복문) 
---


## 문자열(str)


> 줄바꿈(\n), Tab(\t)


```python
a = "Hello\nWorld"
print(a)
b = 'Hello\tworld'
print(b)
```

    Hello
    World
    Hello	world
    

> string formatting


```python
print('금월 점수는 {}점이며 전월은 {}점 입니다'.format(100,90))

print('금월 점수는 {tm}점이며 전월은 {pv}점 입니다'.format(pv=90,tm=100))
```

    금월 점수는 100점이며 전월은 90점 입니다
    금월 점수는 100점이며 전월은 90점 입니다
    

## 컬렉션 (list, tuple, dict, set)

> dict 함수 keys values items


```python
a = {'korea':'seoul','japan':'tokyo','france':'paris'}
print(a.keys())
print(a.values())
print(a.items())
```

    dict_keys(['korea', 'japan', 'france'])
    dict_values(['seoul', 'tokyo', 'paris'])
    dict_items([('korea', 'seoul'), ('japan', 'tokyo'), ('france', 'paris')])
    

## 조건문(if, elif, else) type = bool 

> condition, break 

## 반복문  (While)

> 1에서 100까지 합 구하기


```python
i = 1
_sum = 0 
while i <= 100:
    _sum += i
    i += 1
print(_sum)
```

    5050
    

> 구구단 출력하기


```python
x = 2
y = 1 

while (x<10):
    y = 1 # y=1을 다시 정의해주는 것
    while (y<10):
        print("{}X{}={}".format(x,y,x*y))
        y += 1
    x += 1
```

    2X1=2
    2X2=4
    2X3=6
    2X4=8
    2X5=10
    2X6=12
    2X7=14
    2X8=16
    2X9=18
    3X1=3
    3X2=6
    3X3=9
    3X4=12
    3X5=15
    3X6=18
    3X7=21
    3X8=24
    3X9=27
    4X1=4
    4X2=8
    4X3=12
    4X4=16
    4X5=20
    4X6=24
    4X7=28
    4X8=32
    4X9=36
    5X1=5
    5X2=10
    5X3=15
    5X4=20
    5X5=25
    5X6=30
    5X7=35
    5X8=40
    5X9=45
    6X1=6
    6X2=12
    6X3=18
    6X4=24
    6X5=30
    6X6=36
    6X7=42
    6X8=48
    6X9=54
    7X1=7
    7X2=14
    7X3=21
    7X4=28
    7X5=35
    7X6=42
    7X7=49
    7X8=56
    7X9=63
    8X1=8
    8X2=16
    8X3=24
    8X4=32
    8X5=40
    8X6=48
    8X7=56
    8X8=64
    8X9=72
    9X1=9
    9X2=18
    9X3=27
    9X4=36
    9X5=45
    9X6=54
    9X7=63
    9X8=72
    9X9=81
    

## 반복문 (for)

> 구구단 출력하기 


```python
# x = [2,3,4,5,6,7,8,9]
x = list(range(2,10))
# y = [1,2,3,4,5,6,7,8,9]
y = list(range(1,10))
for i in x: 
    for j in y: 
          print('{}X{}={}'.format(i,j,i*j))
```

    2X1=2
    2X2=4
    2X3=6
    2X4=8
    2X5=10
    2X6=12
    2X7=14
    2X8=16
    2X9=18
    3X1=3
    3X2=6
    3X3=9
    3X4=12
    3X5=15
    3X6=18
    3X7=21
    3X8=24
    3X9=27
    4X1=4
    4X2=8
    4X3=12
    4X4=16
    4X5=20
    4X6=24
    4X7=28
    4X8=32
    4X9=36
    5X1=5
    5X2=10
    5X3=15
    5X4=20
    5X5=25
    5X6=30
    5X7=35
    5X8=40
    5X9=45
    6X1=6
    6X2=12
    6X3=18
    6X4=24
    6X5=30
    6X6=36
    6X7=42
    6X8=48
    6X9=54
    7X1=7
    7X2=14
    7X3=21
    7X4=28
    7X5=35
    7X6=42
    7X7=49
    7X8=56
    7X9=63
    8X1=8
    8X2=16
    8X3=24
    8X4=32
    8X5=40
    8X6=48
    8X7=56
    8X8=64
    8X9=72
    9X1=9
    9X2=18
    9X3=27
    9X4=36
    9X5=45
    9X6=54
    9X7=63
    9X8=72
    9X9=81
    

> dict 함수 반복 


```python
a = {'korea':'seoul','japan':'tokyo','france':'paris'}

for i in a.keys():
    print(i)
    
for i in a.values():
    print(i)
    
for i in a.items():
    print(i)
```

    korea
    japan
    france
    seoul
    tokyo
    paris
    ('korea', 'seoul')
    ('japan', 'tokyo')
    ('france', 'paris')
    

> range 함수 이용해서 list 만들기


```python
print(list(range(10)))
print(list(range(1,10)))
print(list(range(1,10,2)))
```

    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    [1, 2, 3, 4, 5, 6, 7, 8, 9]
    [1, 3, 5, 7, 9]
    


```python
a = list(range(1,101))

for i in a: 
    if (i % 2 == 0) or (i % 11 == 0) : 
        print(i)
```

    2
    4
    6
    8
    10
    11
    12
    14
    16
    18
    20
    22
    24
    26
    28
    30
    32
    33
    34
    36
    38
    40
    42
    44
    46
    48
    50
    52
    54
    55
    56
    58
    60
    62
    64
    66
    68
    70
    72
    74
    76
    77
    78
    80
    82
    84
    86
    88
    90
    92
    94
    96
    98
    99
    100
    

> 연습문제 
>* [22, 1, 3, 4, 7, 98, 21, 55, 87, 99, 19, 20, 45] 최대값
>* [22, 1, 3, 4, 7, 98, 21, 55, 87, 99, 19, 20, 45] 최소값
>* [22, 1, 3, 4, 7, 98, 21, 55, 87, 99, 19, 20, 45] 평균


```python
a = [22, 1, 3, 4, 7, 98, 21, 55, 87, 99, 19, 20, 45]
_min = a[0]
_max = a[0]
_sum = 0 

for i in a:
    if i < _min :
        _min = i
print('min값은: ',_min)

for j in b:
    if j > _max :
        _max = j
print('max값은: ',_max)        
```

    min값은:  1
    max값은:  22
    


```python
_sum = 0 
k = 0 
while k < len(a):
    _sum = _sum + a[k]
    k += 1
print('평균값은: ',_sum/len(a))
```

    평균값은:  37.0
    


```python
_sum = 0 
for l in a:
    _sum += l
print('평균값은: ',_sum/len(a))
```

    평균값은:  37.0
    
