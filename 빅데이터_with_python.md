# 빅데이터

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


