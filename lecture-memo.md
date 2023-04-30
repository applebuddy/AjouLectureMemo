

# 빅데이터

- 목차
  - 1-2차시 빅데이터-01-Python Basics
  - 3-5차시 빅데이터-02-Python Data Structures
  - 6-8차시 빅데이터-03-Python Functions OOP Files
  - 5-6차시 3. 코딩과 재귀 관계
  - 7-8차시 4. 데이터베이스와 관계
  - 9-10차시 5. 관계의 특성과 동치관계
  - 10-11차시 빅데이터-05-Python Libraries - 작성중
  - 12차시 빅데이터-07-Python 3rd Party Libraries (수정완료)

- NDArray: numpy's Core Object, NDArray는 homogeneous 타입이다.
- C는 python보다 빠르다는 장점
- Adjacency Matrix

- 서로 인접한 꼭짓점들이 서로 연결되어있는지를 표현하는 행렬

Statistical Methods (통계적 메서드들)

SciPy (Scientific Python)

### Python Data Structures

### List Comprehension (리스트 이해)

~~~python
[word.lower() for word in sentence] # 각 원소 문자열을 소문자 문자로 구성되게 변환
[word for word in senternce if len(word) > 5] # 문자열 길이가 5보다 큰 경우만 필터링
[x ** 2 for x in seq] # [1, 4, 9]
[(x, x ** 2, x ** 3) for x in range(10)] # [(0, 0, 0), (1, 1, 1), (2, 4, 8) ... ]

[0, 1, 2, 3] # -> [1, 3, 5, 7] x * 2 + 1 형태로 맵핑
[3, 5, 9, 8] # -> [True, False, True, False] 3의 배수 여부에 따라 True, False 반환
range(!0) # -> [0, 1, 4, 9, .... 81] 9의 배수
["apple", "orange", "pear"]

~~~

### Dictionary Comprehensions

~~~python
# Dictionary Comprehensions
(key_func(vars):val_func(vars) for vars in iterable)
fav_fruit = {
  'Kim': 'Apple',
  'Lee': 'tomato',
  'park': 'banana'
}
fav_plant = { val:key for key, val in fav_fruit.items() }
~~~



### Other Comprehensions

~~~python
{ func(vars) for vars in iterable }
{ word for word in hamlet if is_palindrome(word.lewer()) } # 팰린드롬을 충족하는 원소 찾기

~~~

## 1-1) Python Basics (Python 3.8 기준)

- Google Colab을 활용해서 실습 가능

~~~python
print("Hello world!") # "Hello world!" 출력
# multiline comment 를 작성할 수도 있음
"""
Hello
World!
"""
~~~

## 배울 내용 들

- Interactive Interpreter
- Comments
- Variables and Types
  - Numbers and Booleans
  - Strings and Lists
- Control Flow
- Loops
- Functions
- I/O
  - Console IO
  - File IO



### Interactive Interpreter

- Python is an interpreted langauge, high level language
  - C언어는 파일단위로 작성을 하고 컴파일을 함 컴파일에러를 수정하고나면 컴파일된 executable file이 생성되고, 임의의 input parameter를 갖고 실행할 수 있게 됨
  - Python은 바로바로 해석되는 특징을 갖고 있는 고수준 레벨 언어이다.
- it means source code compilation is not needed
- interactive intepreters 이런 면에서 좋다.
  - 결과를 즉시 반환한다.
  - Short code-test-debug cycle, 디버깅을 빠르게 할 수 있음



### Variables and Types

~~~python
# float x = 5.0; 은 C/C++/Java type expression
#python - No type! No semicolon!
x = 5.0 #알아서 'int' class로 봄
y = "str" #알아서 'str' class로 봄
~~~

~~~python
integerDivision = 5 // 2
moduloOperation = 5 % 2
3 ** 2 = 27
x += 2 # x = x + 2
x -= 2 # x = x - 2
x = "Hello, "
x += "World!" # x = "Hello, World!"
~~~

### Booleans

~~~python
True # => True
False # => False
not TRue # => False
True and False # => False
True or False # => True (short-circuits)

1 == 1 # => True
2 * 3 == 5 # => True
1 != 1 # => False
2 * 3 != 5 # => True
1 < 10 # => True
2 >= 0 # => True
1 < 2 < 3 # => True (1 < 2 and 2 < 3)
1 < 2 >= 3 # => False (1 < 2 and 2 >= 3)
~~~

### Strings

- Python doesn't have an explicit char type. (python은 명시적으로 char type이 없어요.)
- instead, chars are strings with length 1. (대신, char는 한자리 string으로 본다.)
- ' ', " " 로 string 리터럴을 표시해요.



### Slicing

- s[0:2] 로 zero based index를 지정해서 일부 영역의 문자열을 지정가능

~~~python
s = "Apple"
s[0:2] == "Ap"
s[3:5] == "le"
s[1:4] == "ppl" #마지막 인덱스의 문자는 포함하지 않음
~~~

- s[start:stop:step]

~~~python
s = "Apple"
s[1:4] == "ppl"
s[1:4:2] == "pl" # 중간의 'p'가 빠짐
s[::-1] == "elppA" # string을 뒤집을 수도 있음
~~~



### Converting Values

~~~python
str(42) # => "42", All objects have a string representation
int("42") # => 42
float("2.5") # => 2.5
float("1") # => 1.0
~~~



### Lists

~~~python
# square brackets limit the list, 여닫는 사각 괄호가 리스트를 표현합니다.
# Commas separate the elements, 콤마가 원소들을 분리합니다.
array = [1, 2, 3]

# Create a new list, 리스트 생성 예시
empty = []
letters = ["a", "b", "c", "d"]
numbers = [2, 3, 5]

# Lists can contain elements of different types, 다양한 타입의 원소를 하나의 list에 혼재하여 관리할 수 있다.
mixed = [4, 5, "seconds"]

# Append elements to the end of a list, append를 사용하면 list의 끝에 새로운 원소를 넣을 수 있다.
numbers.append(7) # numbers == [2, 3, 5, 7]
numbers.append(11) # numbers == [2, 3, 5, 7, 11]
~~~



### Inspecting List Elements

~~~python
letters = ["a", "b", "c", "d"]
numbers = [2, 3, 5, 7, 11]

# zero based indexing 방식으로 element를 찾을 수 있다.
numbers[0] # => 2
numbers[-1] # => 11 (뒤에서 1번째)

# You can also slice lists - the same rules apply
letters[:3] # => ["a", "b", "c"]
numbers[1:-1] # => [3, 5, 7]
~~~



### Nested Lists

~~~python
# Lists can contain anything - even other lists!
letters = ["a", "b", "c", "d"]
numbers = [2, 3, 5, 7, 11]
# nested list, 다양한 타입을 가진 리스트를 하나의 list에 관리할 수 있다.
combo = [letters, numbers]

combo # => [["a", "b", "c", "d"], [2, 3, 5, 7, 11]]
combo[0] # => letters
combo[0][1] # => "b"
combo[1][2:] # => [5, 7, 11]
~~~



### General Queries on Lists

~~~python
# Length query (len)
len([]) # => 0
len("python") # => 6
len([4, 5, "seconds"]) # => 3

# Membership query (in)
0 in [2, 3] # => False
"y" in "python" # => True
"minutes" in [4, 5, "seconds"] # => False
"pyt" in "python" # => True
~~~



### Control Flow: If Statements

- 파이선은 switch를 갖고 있지 않다. 대신 if/elif/else를 선호한다.

~~~python
if some_condition:
        print("Do some action")
elif other_condition:
    print("Other action")
else:
      print("Neither condition action")
~~~



### Python Example

- 팰린드롬인지 체크하는 기능을 만들어보자!

~~~python
word = input("Please enter a world: ") # 입력 받고,
reversed_word = word[::-1] # 뒤집은 문자를 reversed_word에 할당하고
# word, reversed_word를 비교하여 팰린드롬인지 체크할 수 있다.
if word == reversed_word:
      print("this is palindrome!")
else:
      print("this is not a palindrome!")
    
~~~



### Falsy Conditions

- bool()의 인자로 넣었을때 0, 0.0, [], None 등은 모두 false로 반환된다.
  - empty string, empty list 또한 falsy하다.
- 위 이외의 컨텐츠들은 대부분 truthy하다.



### Checking for Truthiness

- python에서는 truthy condition check를 할때 == True를 굳이 명시할 필요가 없다.

~~~python
data = []
if data:
      process(data)
else:
      print "There's no data!!"
~~~


## Python Programming    

#### Funtional Programming

Map and Filter, Lamdas, Iterators/Generators, Decorators!

#### Pure functions are mathematical!, 순수 함수는 매우 정확하다?!

Output은 Input에만 의존한다.
내부 상태를 바꾸는 사이드 이펙트가 없다.

Concat : 두 작업은 순차적으로 연결하는 것

#### Why Funtional Programming?

- python언더는 functional programming 패러다임도 갖고 있습니다.

- Formal Provability, Line-by-line invariants, Modularity, Eash Debugging, Composability

~~~python
languages = ["python", "perl", "java", "c++"]
[len(s) for s in languages]
# -> [6, 4, 4, 3], 각 문자열의 길이로 변환
~~~

#### Map function

~~~python
map(func, iter)
[len(s) for s in languages]
map(len, languages) # map은 좌측과 같이 mapping에 사용

map(float, ["1.0", "3.3", "-4.2"]) # [1.0, 3.3, -4.2]
filter(is_prime, range(100))

# map, filter 등을 혼합해서 사용도 가능하다.
~~~

#### Filter function

~~~python
# 1) filter 사용 안할때 짝수만 필터링
[num for num in fibs if is_even(num)] 
# 2) filter 사용 할때, 위 라인과 동일 기능이지만, 더 짧고, 사이드이펙트를 줄여줄 수 있다.
filter(func, iter)

~~~

#### Lamda function, 익명함수

~~~python
(lamda x: x.  3)(4) # => True, 기존 정의된 함수가 아니라 라인안에 바로 만들고 쓸 수 있다.
~~~

#### Reduce function

~~~python
from functools import reduce

values = [1, 2, 3, 4, 5, 6, 7]
reduce(lambda x, y: 10*x+y, values) # => 1234567
~~~

#### Built-in use Iterators

~~~python
# Return a value max(iterable)
var in iterable all(iterable)
# Return an iterable
enumerate(iterable)
map(fn, iterable)
~~~

#### Generator

- Generator는 local variable의 데이터가 초기화되지 않고, 계속 유지된다.

#### 왜 Iterator, Generator를 사용할 까?

- 비용이 큰 함수 사용을 줄이기 위해
- data stream을 표현하기 위해
- memory buffering을 줄이기 위해
- 기억해두었다가 비동기적인 프로그래밍에 활용 가능
- iterables를 range, map, filter 등에서 활용합니다.

#### Import Conventions

- import 는 file 바로 윗쪽, header comment 이후에 사용 한다.
  - Dependency를 명확하게, conditional imports를 피하기 위해..
- from ... import ... 보다는 import를 권장한다.
  - 이름 충돌을 방지하기 위해
- from ... imports * 는 피하는 것이 좋다.
  - 모든것을 import하게 되면 모듈 이름의 충돌 등을 야기할 수 있음



### Python Libraries (1)

- 머신러닝과 관련된 pytorch library 등은 3rd-party library이다.

#### How to get new Tools?

- Pip is the preferred Python package manager. Use pip!
  - pip install numpy
- etc. conda, easy_install, python setup.py install and so on...

#### Python Standard Libraries

- Modules and Packages
- pdb - Python's Debugger!
- Collections - Specialized Containers for Data!
- itertools - Better iterators!
- functools - Functions on Callable Objects! (Reduce 등 사용할때...)
- re - Regular Expressions, Pattern Matching!
- pickle, json - Object Serialization!
- pathlib - Object-Oriented Filesystem!
- Threading - Thread-Based Parallelism!

#### Module, Package, Standard Library

- Module < Package < Standard Library
- Module : 재사용 가능한 가장 작은 단위, File 하나하나 로 볼 수 있다.
  - File containning Python definitions and statements
- Package : Logical collection of modules
  - E.g. Nimpy contains hundreds of different modules

~~~python
import sound
# sound package import 이후, sound package 내의 module을 사용 가능
sound.effects.echo.echofilter(input, output)

# Subpackage만 import 할 수도 있음
from soundeffects import echo
echo.echofilter(input, output, delay=0.7, atten=4)
~~~

- Standard Library : Collection of packages and modules
  - Standard Library는 기본적으로 Python과 함께 배포됩니다.


#### Package Import 규칙

~~~python
# 아래처럼 sub module, sub package를 사용할 수 있다.
from package import item

# 마지막은 package가 되어야 한다.
import item.subitem.subsubitem

import fibo, sys
dir(fibo) # 모듈 안에 어떤게 있는지 알고 싶을때, dir()을 사용 가능
~~~



#### The pdb Package

- 디버깅, 디버깅 환경에서 사용되는 패키지

#### Collections Package

- collections.namedtuple
  - namedtuple creates tuple subclasses with named fields

~~~python
Point = collections.namedtuple("Point", ["X", "y"])
# 인자 레이블을 명시해서 생성할 수도 있음
p = Point(11, 22)
q = Point(x=11, y=22)
# 레이블명으로 접근도 가능
p.x, 2 * p.y
~~~

- collections.defaultdict
  - 정의되지 않은 값들에 대한 factory function을 가진 dict subclass

~~~python
input_data = [{'yellow', 1}, {'blue', 2}, {'yellow', 3}, {'blue', 4}, {'red', 1}]

# A better approach:
# Make the default value an empty list
# so that we don't need to set values undefined keys
# defaultdict는 많이 사용됩니다. ex) Hashable 객체의 빈도 카운팅을 할때
output = collections.defaultdict(list)
for k, v in input_data:
  output[k].append(v)
  
print(output)
# {"red": [1], "yellow":[1, 3], "blue": [2, 4]}
~~~

- defaultdict는 많이 사용됩니다. ex) Hashable 객체의 빈도 카운팅을 할때

~~~python
s = "mississippi"
d = dict(collections.Counter(s)) 
# counting result
# Counter({"i": 4, "p": 2, "m": 1, "s": 4})
~~~



#### The itertools Package

- 더욱 창의적인 loops를 위해 더 나은 iterators를 제공하는 package입니다.
- product()
- permutation()
  - 순서가 중요, 모든 pair를 만드는 것
- combination()
  - 조합, "CD", "DC" 같은 중복요소가 있는 경우는 하나를 제외하고 표현
- Count()
- cycle("ABCD") -> A B C D A B C D
- repeat(10, 3) -> 10, 10, 10



#### The re Package

- Regular expressions and pattern matching
  - 정규표현식은 알아두면 매우 큰 역할로 사용될 수 있습니다.
- re.match(pattern, string) : 이 pattern이 string 내에 있느냐? 아니면 none을 반환
  - pattern에 맞는 정보를 추출할 때 사용
- re.search(pattern, string) : string 내에서 pattern이 나오는 첫번째 위치 반환
  - 한글자 이상의 단어 두개 사이에 공백이 있는지 체크... 
    - m.group(0) : 전체 메칭 단어들
- re.finditer(pattern, string) : string 내에서 pattern이 나오는 모든 곳을 반환
- re.sub(pattern, sub, string) : string 내에서 pattern에 해당되는 내용을 sub로 바꿔줌

#### 정규표현식 규칙 예시

- [^A-Z] ㅣ 대문자가 아닙니다.
- [^Ss] S나 s가 아닙니다.
- [^e^] e나 ^가 아닙니다.



#### random generator

~~~python
random.random() # float x 0.0 <= x < 1.0
random.uniform(1, 10) # 1.0 ~ 10.0
random.randint(1, 6) # 1 ~ 6
~~~



#### pickle Package - Python object serialization

- 데이터를 byteString으로 flat하게 저장할때 많이 사용된다.



### Python Web Scraping and Text Processing

### HTML Corpus

##### Cleaning HTML file for text extraction

- fileIds, categories를 받아서 documents를 얻는 루프문

##### Defining paras()

- def paras 를 정의

Tokenization: Identifying individual Tokens (식별가능한 개별 토큰들로 토큰화)

- 토큰화에 대한 고려가 필요

##### Part-of-Speech Tagging

- NLP (Natural Landuage Process)
- NN: 단수 nouns /  NNS: 복수 nouns

~~~swift
// pos tag(wordpunct_tokenize(send)) 가 아랫 줄로 내려가야함... [wrong expression]
~~~

- 마지막 코드 : reading을 할때 도움이 될 수 있다. 

- summary : POS Tagging을 해서 input 값에 대한 결과를 도출, describe로 현재 상황을 확인 (monitoring system) 마지막 페이지 처럼 Corpus logging 가능

##### Vectorization 

- 문장 하나마다 vector를 만들어줌 (corpus 전체를 vectorize)

##### Starting with text tokenizing 

- text를 받아서 단어 끝의 s를 없애고, lowercased()로 변환
- word_tokenize를 통해 공백이 있으면 단어 단위로 나눔

##### One Hot Encoding

- vector에 있으면 1, 없으면 0으로 표현하는 기법

##### Term Frequency-Inverse Document Frequency (TF-IDF)

1. 단어 빈도를 계산, corpus를 불러서 vectorizing을 한다. 
2. corpus의 doc을 tokenizing한다. 
3. corpus로부터 corpis에 해당하는 전체 texts를 구한다.
4. text로부터 tf_idf값을 구할 수 있음

### Data Preparation

##### Motivation: Data Types and Variations of Problems

- Classification

##### Feature Extraction

- Sensor : 저레벨 신호를 vector값 등으로 변환 가능
- Image : Pixels를 시각적 단어, histogram(도수분포표) 등으로 표현 가능

##### Data Type Portability

- Data를 구성하다보면 자주 복잡성이 증가합니다. (Heterogeneous)
- Ways of Transforming Data
  - Numeric -> Categorical (수치르 그래프 등으로 이산화되어있는 데이터로 바꾸는 것)
  - Text -> Numeric : 바이너리화

# 컴퓨팅 사고와 이산수학

- 목차
  - 0. 과목소개
  - 1. 빅데이터와 집합
  - 3-4차시 2. 인공지능과 알고리즘
  - 5-6차시 3. 코딩과 재귀 관계
  - 7-8차시 4. 데이터베이스와 관계
  - 9-10차시 5. 관계의 특성과 동치관계
  - 11-12차시 6. 분할과 관계의 폐쇄
  - 13-14차시 7. 접근제어와 격자

- 예홍진 교수

Computational Thinking and Discrete Mathematics


### Computational Thinking

- 컴퓨팅의 기본적인 개념과 원리를 기반으로 문제를 효율적으로 해결할 수 있는 사고 능력



### 이산수학과 관련하여 다룰 수 있는 주제들 

- 집합, 관계, 그래프, 트리, 확률, 오토마타, 부울대수, 알고리즘, 정수론 ...



## 빅데이터와 집합

### 1-1) 데이터의 집합, 데이터베이스(DateBase)

- DB는 통합하여 관리되는 데이터의 집.합.체를 의미한다.
- 중복된 데이터를 없애고, 자료를 구조화하여, 효율적인 처리를 할 수 있도록 한다.
- 사용자의 질의에 대하여 즉각적인 처리와 응답이 이루어진다.
- 생성/수정/삭제를 통해서 항상 최신의 데이터를 유지
- 사용자들이 원하는 데이터를 동시에 공유 가능
- 사용자가 원하는 데이터를 주소가 아닌 내용에 따라 참고 가능
- 응용프로그램과 데이터베이스는 독립되어있으며, 별개로 동작



### Relational database (관계형 데이터베이스)란?

- 관계형 데이터베이스는 현재 가장 많이 사용되고 있는 데이터베이스의 한 종류입니다.
- 관계형 데이터베이스는 테이블(table)로 이루어져 있으며, 이 테이블은 Key, Value의 관계를 나타냅니다.
  - 테이블에 몇개의 항, Record가 있느냐?
  - column, field, attribute, record등으로 구성 됨

- 데이터의 종속성을 관계(relationship)로 표현하는 것이 관계형 데이터베이스의 특징



#### 데이터베이스 값

- 테이블은 각각의 행과 열에 대응하는 값을 가지고 있음
- 이러한 값은 열의 타입에 맞는 값이어야 함

#### 키

- 테이블에서 행의 식별자로 이용되는 열을 키(key) 혹은 기본 키(primary key)라고 할 수 있음
  - 즉, 테이블에 저장된 레코드를 고유하게 식별하는 후보 키(candidate key) 중에서 데이터 데이터베이스 설계자가 지정한 속성을 의미



### 빅데이터란 무엇인가?

- 기존 데이터에 비해 규모, 속도, 다양성, 복잡성 측면에서 구별된 특성을 지닌 데이터
- 굉장히 다양한 데이터 타입을 다룸



#### Variable (변수)

- 변수란, 데이터를 저장하기 위해 프로그램에 의해 이름을 할당받은 메모리 공간
- 즉, 변수란 데이터를 저장할 수 있는 메모리 공간이며, 저장된 값은 변경될 수 있다.



## 1-2) 집합

- 학습 목차
  - 집합
  - 부분집합
  - 멱집합
  - 데카르트 곱
  - 집합의 연산
  - 집합의 항등
  - 컴퓨터에서 집합의 표현

### 집합

- 집합이란 순서를 고려하지 않은 개체(object)의 모임이다. 집합에 속한 개체는 원소(element) 또는 구성원(member)라고 하고, 집합은 그 원소를 포함한다.

### 부분집합(subset)

- 두 집합이 같은 원소를 갖고 있다면, 그 두 집합은 같다. 
- 집합 A의 모든 원소가 또한 집합 B의 원소이면 A는 B의 부분집합이라고 불릴 수 있으며, 기호는 A ⊆ B로 표현 가능
- 진부분집합(proper subset)은 부분집합이나, 두 집합이 같은 경우가 없는 경우를 말한다. 기호로는 A ⊂ B로 표현 가능
- 집합의 크기 : 기호로는 |S|로 S집합의 원소 갯수를 표현 가능

### 멱집합

- 임의의 집합 S가 주어졌을 때, 집합 S의 멱집합(power set)은 집합 S의 모든 부분집합의 집합이다. S의 멱집합은 P(S)로 표현
  - 모든 집합의 부분집합은 공집합과 자기자신을 부분집합으로 반드시 포함한다.
- 집합 {0, 1, 2}의 멱집합은 P({0, 1, 2})로 표현 가능하며, {༳, {0}, {1}, {2}, {0, 1}, {0, 2}, {1, 2}, {0, 1, 2}}

- 만약 집합이 N개의 원소를 가지면, 그 멱집합은 2^N개의 원소를 갖는다.



### 데카르트 곱

- A, B가 집합이라 하면, A와 B의 데카르트 곱 A x B는 a ∈ A, b ∈ B인 모든 순서쌍의 집합
- 데카르트 곱 A x B의 부분집합 R을 집합 A로부터 집합 B로의 관계(relation)라고 한다.



### 집합의 연산

- A U B : A와 B의 합집합(union), A U B = {x | x ∈ A v(or) x ∈ B}
- A ∩ B : A와 B의 교집합(intersection), A ∩ B = {x | x ∈ A ^(and) x ∈ B}



### 컴퓨터에서 집합의 표현

- U의 부분집합 A를 길이 n의 비트열(bit string)으로 표현 가능

- U = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10}, |U| = 10개

- {1, 3, 5, 7, 9}, {2, 4, 6, 8, 10}, {1, 2, 3, 4, 5}

  - 1010101010처럼 비트열로 원소 유무를 판단가능

### 관계의 폐쇄

- 반사 폐쇄, 대칭 폐쇄, 전이 폐쇄를 다 합쳐주어야 동치 관계로서 확장이 됩니다.
- 반사 폐쇄
  - R = {(a, a), (a, b), (b, c), (c, d), (d, c), (c, b)} => (b, b), (c, c)가 있으면 R의 반사 폐쇄 행렬 성립
  - 그래프로 본다면, 자기자신에 대한 루프를 추가해주면 반사 폐쇄 그래프를 그릴 수 있다.
- 대칭 폐쇄
  - R = {(a, a), (a, b), (b, c), (c, d), (d, c), (c, b)} => {(a, a), (b, a), (c, b), (d, c), (b, c), (c, b)} 가 있나? 없으면 합쳐.
  - 원소 각각의 역관계가 함계 포함하도록 한다.
- 전이 폐쇄
  - 수형도 : 모든 경우의 수를 그린 것
  - R^(2~N)에 대한 그림을 그리고, 이 중 없는 케이스의 원소를 추가한다.

### 13 ~ 14) 접근제어와 격자

#### 접근제어, Access Control

- 누군가가 무언가를 사용하는 것을 허가하거나 거부하는 기능을 말한다.
- Access control models
  - 다양한 Access control 관련 model이 있지만, 아래 두가지만 알면 커버 가능
    - Lattice Based Access Control (LBAC, '1993. 기사 출처)
      - label or rule 기반 access control model로도 불려짐
    - Role-Based Access Control 역할기반 접근제어 모델 (국제표준)
      - RBAC를 정의할때, 아래 컨벤션이 유용하다.
        - Subject, Role, Permissions, Session, Subject Assignment, Permission Assignment
        - Partially ordered Role Hierarchy, RH는 >=로 쓰일 수도 있다.
      - 각 컨벤션들이 관계를 이룬다.
- subject(누가), object(무엇을)

### 접근제어 관련 개념 들

- 부분순서(partial order)
  - 반사적이고, 반대칭적(비대칭적)이고 전이적이면 부분순서(partial ordering)이라고 부른다.
  - 행렬의 대각선이 모두 1이면 반사적임
  - 대각선을 뺀 나머지 양쪽 부분을 비교, 서로 대칭이 아니면 비대칭적임
  - 모든 사람들의 순서를 일렬로 정하면 전체순서, 모든 순서를 정의하는게 애매하다 하면 부분순서
  - 생각해보기
    - "보다 크거나 같다" 관계(>=)는 정수의 집합에 대해 부분순서임을 보여라
      - 반사적, 반대칭적, 전이적을 보이면 됨
      - 반사적 : 3 >= 3(3은 3보다 크거나 같다.) 그래서 보는 n이라는 정수 집합에 대해서  n은 n보다 크거나 같다.
      - 반대칭적 :... 빅데이터 앞장 참고
- 전체순서(total order)
  - S의 모든 두 원소가 비교가능하면, S를 전체순서집합, 선형순서집합(Linear order), 사슬이라 부른다.
- 사전식순서(lexicographic order)
  - ex) 문자열의 사전식 순서  
- 하세도표(Hasse diagram)
  - 관계 R이 반사적이고, 반대칭적이고 전이적이면 부분순서집합(partial order)
  - 순서개념으로서 화살표를 그리는 것
  - 그림을 단순하게, 의미는 명확해질 수 있음.
  - 루프(행렬의 대각선 1)를 없애고, 전이적인 요소를 없애고, 
  - 하세도표에서는 경로가 없으면 비교 불가능
- 극대, 극소, 최대, 최소 (화살표가 위를 방향으로 간다고 가정할때, 아래로 가면 경로가 될 수 없다.)
  - 어떤 원소보다도 작지 않으면 극대, 그 반대는 극소
    - 아래 2, 5는 극소 / 위의 12, 20, 25는 극대
  - 극대/극소가 모든 원소와 비교가 될 수 있으면 최대/최소가 됨 (극대, 극소가 있지만, 최대가 최소가 없을 수 있음)
    - 혹은 위아래 최양단 끝이 단 하나씩만 있으면 최대나 최소가 있을 수 있음
- 상한계, 하한계, 최소상한계, 최대하한계
  - d보다 크거나 같은거는 상한계, 작거나 같은거는 하한계
  - **예제 (시험문제 꼭 나옵니다.)**
    - 부분집합A : {a, b, c} / {j, h} / {a, c, d, f}
    - 상한계 : {e, f, h, j} / 공집합 / {f, h, j}
    - 최소상한계 : e(상한계 중 최소)  / 없음 / {f} (상한계 중 최소)
    - 하한계 : {a} / {a, b, c, d, e, f} / {a}
    - 최대하한계 : {a} / {f} (하한계 중 최대) / {a}
- **격자(lattice)**
- 위상정렬(topological sorting)




## IoT 플랫폼

- 김재훈 교수

- 목차
  - 0차시 IoT 플랫폼 과목소개
  - 1차시 IoT 플랫폼 소개
  - 2차시 IoT 플랫폼 구조
  - 3차시 IoT 플랫폼 개요(1)
  - 4차시 IoT 플랫폼 개요(2)
  - 5차시 센서 디바이스
  - 6차시 IoT 플랫폼(아두이노)
  - 7차시 IoT 플랫폼 - 운영체제 (1)
  - 8차시 IoT 플랫폼 - 운영체제 (2)
  - 9차시 분산미들웨어 플랫폼(1)
  - 10차시 분산미들웨어 플랫폼(2)
  - 11차시 분산미들웨어 플랫폼(3)
  - 12차시 미들웨어-AllJoyn
  - 13차시 미들웨어-OCF 개요 (2)

## IoT 플랫폼 OT

### IoT 

- 사물의 상태를 파악하고 모니터링하고, 효율적으로 움직이도록 제어하는 것
- IoT가 새로운 Business Model들을 만들고 있음

### More on 4 Layers Model (IoT 4 Layer)

- **Integrated Application**
  - 응용, 비즈니스 플랫폼
- **Information Processing**
  - IoT 블록체인
  - 클라우드, 빅데이터
  - 상황인지
- **Network Construction**
  - 미들웨어 플랫폼
  - 자원관리, 데이터처리
- **Sensing and Identification (low level device)**
  - 자원관리, 데이터처리
  - 디바이스, 센서



## 1-1) IoT 플랫폼 소개

IoT산업은 연 평균 10~20%의 성장을 거듭하고 있었다. (2020년 기준)

### IoT를 가능하게 하는 기술들

- Device Technologies : 기기 제조 기술
- Connectivity Technologies : 연결 기술
- Service Technologies

### 사물인터넷의 범위 및 요소 기술

- 데이터 수집 > 데이터 전송 > 통신 > 데이터 분석 > 활용

### IoT 이외 유사개념과의 비교 (CPS, M2M ... )

- IoT : 사물 인터넷, 개방형 시스템, 서비스 지향형
- CPS : 사이버물리시스템, 폐쇄형 시스템, 자원 중심적
- M2M : Machine to Machine
- Internet of Everything : 모든것이 인터넷으로 연결이 된다.
- Fog Computing : 안개 처럼 우리 주변에 게이트웨이나 지역을 담당하는 분산된 클라우드가 존재



### IoT 전망

- 사물인터넷의 시장규모는 2022년까지 연 평균 10% 이상 꾸준히 성장하고 있습니다.



### IoT 플랫폼 동향

- 디바이스/데이터/서비스/... 중심 플랫폼,



### Simplified IoT Architecture

- Application
- Decision Support Tools
- Big Data Stores
- Network and Telecommunications Equipment
  - LTE, WiFi, Bluetooth...

### IoT 플랫폼 구조의 구성 요소

- 응용, 정보처리, 네트워크, 센서/디바이스



## 1-2) IoT 플랫폼 구조

### 학습 목표

- IoT 프랫폼 구조와 구성 요소를 이해한다. 
- IoT 플랫폼 구성요소의 주요 이슈를 알아본다.



### 사물인터넷 등장배경

- 소형화
- 저전력화
- 저가격화 : 센서 사용을 위한 비용이 급격히 줄어듦
- 표준화
  - 스마트홈, 헬스케어, 건설, 제조, 농업(온도제어), 에너지, 환경, 국방 등 다양한 도메인 분야에서 사용이 되고 있음



### 센서와 엑츄에이터(actuator)

- 센서 : 물리량을 측정하는 기기
  - 카메라, 가속도계, 레이더, 스위치 ...
- 엑츄에이터 : 물리량을 변화시키는 기기
  - Motor controllers, LEDs, lasers, Loudspeakers

#### Mobius Platform

사물 간에 인터넷을 할 수 있는 물적 기반인 통신 네트워크가 원활하게 작동하도록 하는 운영체제



### Distributed Computing in IoT (IoT 분산 네트워크 플랫폼)

- 서버쪽에서 모든 일을 처리하는 것이 아니라, 지역적인 서비스를 분산된 게이트웨이가 맡게되면 더욱 효율적으로, 빠르게 처리할 수 있음



### IoT 미들웨어 플랫폼

- 미들웨어란, 말 그대로 중간에 있다는 것, 사물(Thing, 하드웨어)들이 있고, OS가 올라가고, 그 다음 올라갈 수 있는 것이 middleware 이다.
- 블록체인도 하나의 미들웨어
  - 폐쇄적이고 집중화된 IoT Network ---클라우드---> 개발형의 집중화된 클라우드 IoT Network ---블록체인---> 개방형의 분산화된 클라우드 IoT Network



## 2-1) 사물인터넷 표준화

- IoT와 관련된 다양한 표준화 기구가 있습니다. (ITU, ISO, IEEE, oneM2M ...)
- oneM2M
  - 플랫폼 환경을 통합, 공유하고, 사물인터넷 공동서비스 플랫폼 개발을 위해 발족 된 사실상 표준화 단체
  - 표준화 관련 Release를 지속 업데이트 하고 있음 (1, 2, 3, ...)
- OCF(Open Connectivity Foundation)
  - 사물인터넷 구현 시 REST 구조 기반, 경량형 CoAP 프로토콜을 사용하여 **사물인터넷 장치들을 연결하고, 장치에 존재하는 자원들을 상호제어**할 수 있게 하는 표준 플랫폼 기술
- IETF(Internet Engineering Task Force, 국제 인터넷 표준화 기구)

#### MEMS

- 미세 전자 기계 시스템(Micro-Electro-Mechanical systems)의 약자

#### 시멘틱 웹

- 컴퓨터가 정보자원의 뜻을 이해하고, 논리적 추론까지 할 수 있는 차세대 지능형 웹
