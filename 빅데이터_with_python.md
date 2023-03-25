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

