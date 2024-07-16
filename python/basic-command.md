# python

> ## python 기초정보
if와 else와 elif 차이
- if  : 조건 1이 참일 때 실행하는 코드
- elif : 조건 1이 거짓이고, 조건 2가 참일 때 실행되는 코드
- else: 모든 조건에 부합하지 않는 경우

whil문과 for 문의 차이
- whil문은 조건이 참(True)인 동안 반복하여 코드 블록을 실행.
- for문은 시퀀스(리스트, 튜플, 등)의 각 요소에 대해 순차적으로 반복.

dictionary 반복문
```python
for key in dict: -> 키(변수이름)이름이 나옴
for key in dict.keys(): -> 키(변수이름)이름이 나옴. 위와 같음
for key in dict.values(): -> 값(변수 값)이 나옴.
for key, value in dict.items(): 키, 값이 나옴.
```

break
- 반복문을 종료시킴
- else 문은 끝까지 반복된 후 실행. 즉, break를 만나지 않았을떄 실행됨.

continue
- 이후 코드를 실행하지 않고 반복진행 

> ## method
- append(): 리스트 뒤에 데이터 추가
```python
numbers = [1 ,4, 3, 6, 8, 9, 3]
numbers.append(10)
print(numbers) -> [1, 4, 3, 6, 8, 9, 3, 10]
```

- extend(): 숫자형 리스트를 합침
```python
numbers = [1 ,4, 3, 6, 8, 9, 3]
a = [99, 100]
numbers.extend(a)
print(numbers) -> [1, 4, 3, 6, 8, 9, 3, 99, 100]
```

- insert(): 원하는 위치에 데이터 추가
```python
numbers = [1 ,4, 3, 6, 8, 9, 3]
numbers.insert(0, -10)
print(numbers) -> [-10, 1, 4, 3, 6, 8, 9, 3]
```

- remove(): 데이터 찾아 제거
```python
numbers = [-10, 1 ,4, 3, 6, 8, 9, 3, -10]
numbers.remove(-10)
print(numbers) -> [1, 4, 3, 6, 8, 9, 3, -10]
```

- pop(): 기본으로 맨뒤 데이터 제거, () 안에 위치 값 제거.
```python
numbers = [-10, 1 ,4, 3, 6, 8, 9, 3, -10]
numbers.pop()
print(numbers) -> [-10, 1, 4, 3, 6, 8, 9, 3]
```

> ## 집합 method(중복이 허용되지 않는 세트.)
- add(): 단일 데이터 추가
```python
fruits = {'apple', 'banana', 'melon'}
fruits.add('watermelon')
print(fruits) -> {'melon', 'apple', 'banana', 'watermelon'}
```

- update(): 여러 데이터 추가

- remove(): 제거


- map: 반복작업활용
```python
numbers = [1, 2, 3, 4, 5]
result = map(str, numbers)
print(list(result)) -> ['1', '2', '3', '4', '5']
```
> map은 함수의 기능이 돌아가면 됨

filter: 특정 조건을 만족하는 요소들만 선택하는 데 사용되는 내장 함수
```python
def is_odd(x):
    return x % 2
numbers = [1, 2, 3, 4, 5]
result = filter(is_odd, numbers)
print(list(result)) -> [1, 3, 5]
```
> filter는 True, False가 들어가야함