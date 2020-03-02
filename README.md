# python_cheatsheet

- 파이썬이란?

  - Guido van Rossum의 (1999) : Computer Programming for Everybody 모두의 프로그래밍
  - 한 줄에 명령어 한 줄씩 치며, ; 를 사용하지 않고, Indentation(들여쓰기, 내어쓰기)로 블럭을 구별한다.
  - 들여쓰기는 탭키를 쳐서 문장을 오른쪽으로 보내는 것이며, 윗문자에 아래 명령이 종속될 경우
  - 내어쓰기는 쉬프트-탭키를 쳐서 문장을 왼쪽으로 보내는 것이며, 윗 문장의 종속을 빠져나오는 기능을 한다.

- 코멘트(주석)
  - 한줄짜리 주석 : 프로그램에 관계 없지만 설명을 넣는 문구를 쓸때 #을 맨 앞에서 붙여서 쓴다
  ```
  # 이 문장은 실행되지 않습니다. 설명을 위해서 쓸 말을 쓰지요
  # 따라서 # 문장은 실습할 때 타이핑 하지 않는 부분입니다.
  ```
  - 여러 줄 주석 :
  ```python
  """
  여러줄의 주석을 쓰는 경우에는 "를 3개를 주석의 위 아래를 감싸주면 됩니다.
  주석을 여러줄 짜리를 쓸지 말지는 본인의 스타일에 따라서 고르면 되나 간단 경우는 한줄짜리가 편합니다.
  """
  ```

---

- python 실행
  - 컴퓨터에 설치된 python3를 실행하거나,
  - http://www.python.org에 가서, ">\_" 모양 아이콘을 누르고 기다리면 실행된다.
  - ">>>" 문자는 파이썬 해석기의 맨 처음에 나오는 것으로 "prompt"프람프트라고 있으며 타이핑하지 않는다.

---

- 사칙연산

  ```
  # 더하기
  >>> 1 + 2
  # 빼기
  >>> 1 - 2
  # 곱하기
  >>> 1 * 2
  # 나누기
  >>> 10 / 5
  # 나머지
  >>> 10 % 3
  1
  # 몫 방법1 : 몫 연산자를 이용해서 구하는 방법
  >>> 10 // 3
  3
  # 몫 방법2 : 나머지를 정수로 만들어서 방법
  >>> int(10/3)
  3
  # 제곱
  >>> 2 * 2
  ```

---

- 프로그램 기초

  - 프로그래의 문장은 A=B의 형태를 이해해야 함.
  - A는 값이 들어가는 목적지(대상)이고, B는 그 값에 집어넣고 싶은 수식.
  - A는 주로 변수가 되고, B는 주로 +-\*/ 사칙연산으로 이뤄지건, 상수가 된다.

  ```
  # 변수 선언
  >>> A = 2

  # 아래는 안됨 상수값에 변수를 집어넣기 때문에 허용안됨
  # 변수는 변하는 수이고, 상수는 변하지 않는 고정값
  >>> 2 = A

  # 변수를 다른 변수값을 수식으로 변환해서 받을 수 있음.
  >>> B = A + 2

  # 좌측값(L-value)는 미래의 값이고, 우측값(R-value)는 현재의 값이다.
  # 줄이 실행이 되면 좌측값이 변하게 되어서 현재의 값이 된다.
  # 변수를 더하기
  >>> A = 1
  >>> A = A + 2 # 현재 A 는 1
  >>> print(A)  # 현재 A 는 3

  # 변수를 뺴기
  >>> A = A - 2

  ```

---

- 변수 : 값을 저장하는 공간

  ```python
  # n에 123을 담습니다.
  >>> n = 123

  # n에 문자열 abc를 담습니다. ' 이나 " 중의 하나를 골라써야 합니다
  # 다만 ' 로 시작하면 ' 로 끝내야 합니다.
  >>> s = 'abc'
  >>> s = "abc"

  # arr에 1,2,3 3개의 숫자를 담습니다.
  >>> arr = [1,2,3]

  # arr에 a, b, c 3개의 숫자를 담습니다.
  >>> arr = ['a','b','c']
  ```

---

- 변수 타입

  - 정수 : 소수점이 없는 수
  - 부동소수 : 소수점이 floating이 물 위의 부표처럼 숫자사이로 이동 가능한

  ```
  # 타입을 알아보려면 내장함수 type으로 변수를 조사해본다.
  >>> type(1)
  >>> <class 'int'>
  >>> type("abc")
  <class 'str'>
  >>> type([1,2,3])
  <class 'list'>
  ```

---

- 변수 타입 변환

  ```
  # 정수로 바꾸기
  >>> int(1.23)
  1
  # 문자열로 바꾸기
  >>> str(1.23)
  '1.23'
  # 부동소수로 바꾸기
  >>> flot(3)
  3.0
  # 리스트로 바꾸기
  >>> list('123')
  ['1', '2', '3']
  ```

---

- 표준 출력

  - 콘솔(터미널)방식의 예전 컴퓨터부터 있던 출력 방식으로 간단하게 데이터를 처리할 수 있어서 GUI방식보다 어렵지만, 개발에 많이 사용됨.
  - print 함수를 이용해서 다양한 출력

    ```
    # 한번 호출 할 경우 줄 바뀜이 일어나서 다음 줄에 출력이 됨
    >>> print("Hello")
    Hello
    >>> print("World")
    World

    # 줄바뀜을 안하고 싶다면 end(끝문자)를 지정해주면 됩니다.
    print("1", end="")
    print("2")
    # 끝문자가 공백인 경우
    print("Hello", end=" ")
    print("World")
    ```

---

- 표준 입력

  - 기본 입력 받기

    ```python
    l = input()
    ```

  - 입력 받아서 정수로 바꾸기

    ```python
    l = int(input())
    ```

  - 입력 받아서 쪼개기

    ```python
    l = input().split()
    ```

  - 입력 받아서 int 로 2개 받기

    ```python
    l = input().split()
    a = int(l[0])
    b = int(l[1])
    print(a+b)
    ```

  - 입력 받아서 쪼갠후 정수로 바꾸기

  ```python
  l = list(map(int, input().split()))
  # 리스트 컴프리헨션을 이용해도 똑같이 된다.
  l =  [int(x) for x in input().split()]
  ```

- 분기(브랜치, branch)

  ```python
  if a == 'seoul' :
   print('korea')
  elif a == 'seattle' :
   print('usa')
  else
   print('unknown')

  if a >= 90 :
   print('A')
  else a < 90 and a >= 80 :
   print('B')
  else a < 80 and a >= 70 :
   print('C')
  else
   print('D')
  ```

---

- 흔히 사용되는 if문

  ```python
  # 짝수 인지 구별
  if i % 2 == 0 :
    print("짝수")
  if i % 2 == 1:
    print("홀수")

  if i % 3 == 0 :
    print("3의 배수")
  ```

---

- 루프(loop)
  - 여러차레 같은 명령어 블럭을 반복해서 처리하게 하는 것
  - 음악의 도돌이표와 비슷함.
  - 반복이 되는 구역은 들여쓰기가 되는 부분임
  - for 문보다 오른쪽으로 들어간 부분은 모두 for문의 영향으로 같은 횟수만큼 반복된다.
  - 루프를 벗아날때는 break(브레이크)명령어로 루프를 깨고 나온다.
  - for를 이용한 루프와 while을 이용한 루프
  - for를 이용한 루프는 시작값과 끝값을 지정하는 형식
  - while문은 루프가 유지되는 조건을 지정해서 그 조건이 맞는동안 계속 반복하는 형식
  - for/while은 근본적으로 서로 같게 표현할 수 있으나, 상황에 맞게 선택
  - 대부분 for문으로 처리가 가능하고, 특별한 경우에 while문이 훨씬 간결하고 쓸수 있다.
    - 코드를 간결하게 쓴다는 것은 에러가 적고 논리적으로 헛점을 쉽게 발견할 수 있게 짜기위함이다.
    - 따라서, 그 이상은 넘어서 이해가 어려울 정도로 짧게 짜는 경우는 특정한 조건(퀴즈,시합)에서는 쓴다.

---

- 자주 쓰는 루프문

  - 0에서 10까지 출력 (for)

    ```python
    for i in range(0, 11) :
      print(i)

    # 앞의 0은 생략 가능
    for i in range(11) :
      print(i)

    # 두칸씩 건너 뛸 때
    for i in range(0, 11, 2) :
      print(i)

    # -1씩 뒤로 줄어들 때
    for i in range(0, 11, -1) :
      print(i)
    ```

  - 약수의 갯수 세기 (for)

    ```python
    n = int(input())
    count = 0
    for i in range(1, n+1) :
    if n % i == 0 :
      count += 1
    print(count)
    ```

  - 0에서 10까지 출력 (while문을 이용한 경우)

    ```python
    i = 0
    while i > 10 :
      print(i)
      i += 1
    ```

---

# 문자열

- 문자열 s안 에 안에 있는 p 글자 개수 세기

  ```python
  s = 'codingpen codingpen'
  count = 0
  for c in s :
    if c == 'p' :
      count += 1
  ```

* 문자열중 인덱스로 글자만 뽑기

  ```python
  >>> s = 'abc'
  >>> s[0]
  'a'
  >>> s[1]
  'b'
  >>> s[2]
  'c'
  ```

* 부분 문자열(Substring)

  ```python
  >>> s = 'AM 12:34'
  >>> s[0:2]
  'AM'
  >>> s[3:]
  '12:34'
  >>> s[:2]
  'AM'

  # 'cba'가 출력됩니다.
  print(sr)
  ```

* 문자열 합치기( +로 합치며 + 좌우에 문자열이나, 식 과 변수가 온다)

  ```python
  >>> s = '3*3 = ' +  3*3
  >>> print(s)
  3*3 = 9
  ```

* 문자열 뒤집기

  ```python
  s = 'abc'
  sr = s[::-1]
  # 'cba'가 출력됩니다.
  print(sr)
  ```

* 문자열 치환

  ```python
  >>> s = "Hello".replace("H", "W")
  >>> s
  'Wello'
  ```

- 문자열 끊어 붙이기

  ```python
  >>> s = "01245"
  >>> s = s[0:3] + '3' + s[3:]
  >>> s
  '012345'
  ```

- 문자열을 리스트로 변환

  ```python
  # 리스트를 이용해서 문자열을 한 글자씩 나누기
  >>> s = "012345"
  >>> s = list(s)
  >>> s
  ['0', '1', '2', '3', '4', '5']

  # map함수를 이용해서 정수로 변환후 리스트로 바꾸기
  >>> s = list(map(int, s))
  >>> s
  [0, 1, 2, 3, 4, 5]
  ```

* 문자열로 된 리스트를 다시 문자열로 바꾸기

  ```python
  >>> s = "012345"
  >>> s = list(s)
  >>> ''.join(s)
  >>> '012345'
  ```

* 문자열을 아스키코드(10진수)로

  ```python
  >>> s="aA"
  >>> ord(s[0])
  97
  >>> ord(s[1])
  65
  ```

* 문자열 전체를 소문자/대문자로
  ```python
  >>> 'abc'.upper()
  'ABC'
  >>> 'Abc'.lower()
  'abc'
  ```

* 문자열 앞 뒤의 공백 없애기
  ```python
  >>> ' abc '.strip()
  'abc'
  ```

* 아스키코드(10진수)를 문자열로

  ```python
  >>> chr(97) + chr(65)
  'aA'
  ```

* 대소문자 변환

  ```python
  >>> s = "a"
  # 소문자 a와 대문자 A사이의 아스키코드 차이값을 구한다.
  # 대문자 a가 소문자 a보다 앞에 있다.
  >>> diff = ord('a') - ord('A')
  >>> diff
  32
  # 소문자를 대문자로 바꿀 경우
  >>> s = chr(ord(s[0]) - diff)
  >>> s
  'A'
  # 대문자를 대문자로 바꿀 경우
  >>> chr(ord(s[0]) + diff)
  >>> s
  'a'
  ```

* 문자열 포맷팅(Formatting)
  - python 3.6 부터 도입된 f string을 쓰는게 가장편함
  ```python
  >>> n = 15
  >>> print(f"result is {n}")
  result is 15
  >>> print(f"n:{n} 2*n:{2*n} n*n:{n*n} hex:{n:x} HEX:{n:X} octal:{n:o} binary:{n:b}")
  n:15 2*n:30 n*n:225 hex:f HEX:F octal:17 binary:1111
  # hex : hexadecimal 16진수
  # octal : 8진수
  # binary : 16진수
  >>> s = "hello"
  # 왼쪽 정렬 : <
  # 오른쪽 정렬 : >
  # 가운데 정렬 : ^
  >>> print(f"{s:<10}{s:>10}{s:^10}\n" + "0123456789"*3)
  hello          hello  hello
  012345678901234567890123456789
  >> n= 6
  >>> print(f"{s:<{n}}{s:>{n}}{s:^{n}}\n" + "01234567"*3)
  hello      hello hello
  012345670123456701234567
  # 변수로 너비 지정하기
  >>> n = 7
  >>> w = 8
  >>> print(f"_{n:>{w}b}_{n:<{w}b}_")
  _ 111_111 _
  # 소숫점 자르기
  >>> p = 3.14159
  >>> print(f"{p:.2f}")
  3.14
  ```

````

---

# 리스트

- 인덱스와 값으로 이뤄져 있습니다. 인덱스는 0부터 시작해서 1씩 증가하는 숫자입니다.
- 0번 인덱스의 값은 첫번째 값이 됩니다.
- n개의 원소를 값는 리스트의 마지막 원소의 인덱스는 n-1이 됩니다.

- 길이
```python
arr = [1,2,3]
len(arr)
3
# 한줄에서 입력을 받아서 공백(스페이스)으로 분리해서 어레이로 만들기
arr = input().split()
print(arr)
````

- 맨 뒤에 추가

  ```python
  arr = []
  arr.append(1)
  arr.append(2)
  # a= [1, 2] 로 추가됨
  ```

- 같은 값의 원소 여러 개 추가하기

  ```python
  # 0 원소가 10개인 어레이
  arr = [0] * 10
  ```

- 특정 인덱스에 원소 추가

  ```python
  >>> a = [1, 2, 3]
  >>> a.insert(1, 7)
  >>> print(arr)
  [1,7,2,3]
  ```

- 인덱스를 쓰지 않고 원소를 직접 사용

  ```python
  arr = [1, 2, 3]
  for n in arr :
    print(n, end=",")
  # 출력 결과
  1,2,3,

  # 글자를 구분자로 출력
  arr = ['2019', '12', '25']
  for n in arr :
    print(n, end=":")

  # 결과
  2019:12:25
  ```

- 리스트 안에 원소가 있는 지 검사

  ```python
  >>> arr = [1, 2, 3]
  >>> print(1 in arr)
  True
  >>> print(10 in arr)
  False
  >>> if 1 in arr:
  ...    print('1')
  ...
  1
  ```

- Sort(소트) 정렬하기(크기대로 순서를 바꾸는 것)

  ```python
  arr = [1, 5, 3, 2, 7]
  arr.sort()
  print(arr)
  # 출력 결과
  [1, 2, 3, 4]
  ```

- 리버스(순서를 반대로 뒤집는 것)

  ```python
  arr = [1, 2, 3]
  arr.reverse()
  print(arr)
  # 출력 결과
  [3, 2, 1]
  ```

- 인덱스의 원소 합계 구하기
  ```
  arr = [1, 2, 3]
  sum(arr)
  ```
- 인덱스의 원소 갯수 구하기

  ```
  >>> arr = [1, 1, 2]
  >>> arr.count(1)
  2
  ```

- 인덱스의 원소 지우기

  ```python
  arr = [1, 2, 3]
  arr.pop(0)   # 맨 처음 원소 지우기
  arr.pop(len(arr)-1) # 맨 뒤 원소 지우기
  ```

- 원소의 값을 찾아서 지우기

  ```python
  arr = [10, 11, 12]
  arr.remove(11)
  print(arr)
  [10, 12]

  arr = ['a', 'b', 'c']
  arr.remove('b')
  print(arr)
  ['a', 'c']
  ```

- 전체 지우기

  ```python
  arr = [1, 2, 3]
  arr.clear()
  ```

- 리스트를 문자열로 합치기

  ```python
  arr=['2019', '12', '25']
  ':'.join(arr)
  print(arr)
  '209:12:25'
  ```

- 위 방법은 원소가 문자열일 때만 가능한데 정수 리스트를 문자열로 합치기

  ```python
  arr=['2019', '12', '25']
  ':'.join(str(x) for x in arr)
  print(arr)
  '209:12:25'
  ```

- 문자열을 리스트로 분리하기

  ```python
  # 아무것도 인자로 주지 않으면 공백을 이용해서 문자열 분리
  str = 'I like python'
  arr = str.split()
  print(arr)
  # 인자를 주면 그 문자열을 구분자로 사용해서 분리
  arr= '2019:12:25'
  arr.split(':')
  print(arr)
  ['2019', '12', '25]
  ```

- range로 list 만들기
  - python2에서는 range가 list를 돌려주나, python3부터는 range타입이 돌려주므로 list함수로 한번 더 감싸야 한다.
  ```python
  arr = list(range(0, 3))
  print(arr)
  [0, 1, 2]
  ```
- 리스트 컴프리헨션(List comprehension)

  - 리스트를 for문을 안쓰고 짧게 한줄에 만드는 법

  ```python
  # 0에서 10까지 리스트
  >>> [x for x in range(1, 11)]
  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

  # 짝수 리스트
  >>> [x*2 for x in range(1, 11)]
  [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]

  # 홀수 리스트
  >>> [x*2+1 for x in range(1, 11)]
  [3, 5, 7, 9, 11, 13, 15, 17, 19, 21]

  # 중첩 리스트
  >>> [ [x*2, y*2+1] for x in range(1, 3) for y in range(1, 3)]
  [[2, 3], [2, 5], [4, 3], [4, 5]]

  # x를 중복 사용이 가능
  >>> [[x, x*x] for x in range(1, 3)]
  [[1, 1], [2, 4]]

  # 중첩 리스트 (조건식으로 필터된)
  >>> [ [x*2, y*2+1] for x in range(1, 3) for y in range(1, 3) if x + y > 2]
  [[2, 5], [4, 3], [4, 5]]
  ```

- list 와 set의 차이

  - list 는 appned 함수로 추가, set는 add로 추가, 삭제는 둘 다 remove로 같다
  - list 는 같은 값의 원소 중복 허용, set은 같은 값인 경우 중복이 되지 않고, 기존 값이 대치됨
  - set은 인덱스가 없으므로 원소 접근시 list()함수로 변환해서 써야함.

    ```python
    >> s = {1,,2,3,3,3}
    >> s
    {1,2,3}
    ```

    - 위 예를 보면 중복되는 3은 하나로 나옴

    ```python
    # 교집합
    >> {1, 2, 3} & { 2, 3, 4}
    {2, 3}

    # 합집합
    >> {1, 2, 3} | { 2, 3, 4}

    # 차집합
    >> {1, 2, 3} - { 2, 3, 4}
    {1}
    ```

---

# 사전(Dictionary)

- 키와 밸류(값)으로 이뤄져있습니다. 리스트와 달리 순서가 없고, 인덱스는 0부터 시작하는 정수지만, 키는 아무글자나 숫자가 와도 됩니다. 말그대로 사전에서 키(단어)를 찾으면 밸류(뜻)이 나오는 것과 같습니다.
- 선언

```python
# 이름이 sword(칼)이고, damage(데미지)가 200인 아이템을 다음과 같이 선언
d = { 'name' : 'sword', 'damage' : 200 }
```

- 값 가져오기

```python
print(d['name'])
print(d['age'])
```

- 한바퀴 돌기(방문하기)

```python
for k in d :
  print(k, d[k])
```

- 키가 있는지 확인하기

````python
if 'name' in d :
  print('name이란 키가 있습니다.')
else :
  print('name이란 키가 없습니다.')
```python

````

- 키 제거하기

```python
>>> dic = {"name" : "jin"}
>>> del dic["name"]
>>> dic
{}
```

---

# Random

- random 모듈을 임포트해야함.

```python
# 랜덤함수를 쓰기 위해서 임포트를 해서 라이브러리르 가져와야 한다.
>>> import random

# 0.0에서 1.0까지의 랜덤 부동소수(1은 포함하지 않음)
>>> random.random()
0.08308504017354557

# 인수 a와 b사의 랜덤 부동소수, b(아래에서는 10)을 포함하지 않음
>>> random.uniform(1, 10)
7.519823577296704

>>> random.randint(1, 6)  # a, b 사의 랜덤, a, b를 포함
3

>>> random.choice('abcde') # 주어진 문자열중에서 랜덤 글자를 리턴
b

>>> random.choice([1, 2, 3]) # 주어진 리스트(어레이)에서 한 원소를 리턴
2

>>> random.sample([1, 2, 3], 2) # 주어진 리스트(어레이)에서 주어진 갯수(아래에서는 3개중에서 2개) 의 원소를 리턴
2,3

>>> arr = [1,2,3]
>>> random.shuffle(arr) # 주어진 리스트(어레이)를 랜덤하게 뒤섞음
>>> arr
[1, 3, 2]

```

---

# 수학관련

```python
# 3의 2제곱
3 ** 2
9
# 10의 3제곱
>>> 10 ** 3
1000
# 반올림, 부동소수를 정수로 바꿔주는데 반올림을 하는 점이 int()와 다름
>>> round(1.5)
2
# 소수점 2자리까지 유효하게 반올림
>>> round(3.1415, 2)
3.14
# 소수점 3자리까지 유효하게 반올림
>>> round(3.1415, 3)
3.141
# 소수점 자리 지정, 반올림을 하지 않고 그냥 버리는 점이 round()와 다르다.
>>> format(3.1, ".5f")
3.10000
```

- 삼각함수 (sin, cos)

  ```python
  import math

  print(math.sin(math.pi/4)
  print(math.cos(math.pi/2)
  ```

# 더 자세한 Python 내장함수

https://docs.python.org/ko/3/library/functions.html?highlight=round#format
