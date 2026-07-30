- [List Comprehension](#"List""Comprehension")
  - [Basic List Comprehension](#"Basic""List""Comprehension")
  - [List Comprehension With Condition](#"List""Comprehension""With""Condition")
  - [String Operation In List Comprehension](#"String""Operation""In""List""Comprehension")

- [Dictionary Comprehension](#"Dictionary""Comprehension")
  - [Basic Dictionary Comprehension](#"Basic""Dictionary""Comprehension")
  - [Dictionary Comprehension With User Input Students](#"Dictionary""Comprehension""With""User""Input""Students")
  - [Dictionary Comprehension With User Input Products](#"Dictionary""Comprehension""With""User""Input""Products")

- [Generator](#"Generator")
  - [Generator Concept](#"Generator""Concept")
  - [Benefits Of Generators](#"Benefits""Of""Generators")
  - [Basic Generator With Yield](#"Basic""Generator""With""Yield")
  - [Generator With While Loop](#"Generator""With""While""Loop")
  - [Using Next On Generator](#"Using""Next""On""Generator")
  - [Using Iter And Next On List](#"Using""Iter""And""Next""On""List")
  - [Generator Expression](#"Generator""Expression")
  - [List Comprehension Vs Generator For Even Numbers](#"List""Comprehension""Vs""Generator""For""Even""Numbers")

- [Class And Oops Revise](#"Class""And""Oops""Revise")
  - [Class Method Vs Instance Method](#"Class""Method""Vs""Instance""Method")
  - [Class Variable](#"Class""Variable")
  - [Instance Variable With Constructor](#"Instance""Variable""With""Constructor")
  - [Instance Method](#"Instance""Method")
  - [Class Method](#"Class""Method")
  - [Static Method](#"Static""Method")
  - [Method Overriding](#"Method""Overriding")

- [Magic Method](#"Magic""Method")
  - [Str Method](#"Str""Method")
  - [Len Method](#"Len""Method")
  - [Add Method](#"Add""Method")

- [Decorator](#"Decorator")
  - [Function As Parameter](#"Function""As""Parameter")
  - [Basic Decorator With Before And After](#"Basic""Decorator""With""Before""And""After")
  - [Syntax Decorator With Arguments](#"Syntax""Decorator""With""Arguments")
  - [Decorator With Arguments](#"Decorator""With""Arguments")
  
- [Builtin Modules](#"Builtin""Modules")
  - [Import Vs From](#"Import""Vs""From")
  - [Math Module](#"Math""Module")
  - [Datetime Module](#"Datetime""Module")
  - [Random Module](#"Random""Module")
  - [Custom Modules](#"Custom""Modules")
  - [Importing Classes From Modules](#"Importing""Classes""From""Modules")
  - [Dir Function](#"Dir""Function")
  - [Os Module](#"Os""Module")
  - [Sys Module](#"Sys""Module")

---
## List Comprehension

##### Basic List Comprehension
Squaring each element in a list using comprehension instead of a for loop.
```python
list1=[2,3,4,5]
list2=[i**2 for i in list1]
print(list2)
'''
Output:
[4, 9, 16, 25]
'''
```

##### List Comprehension With Condition
Filtering even numbers from a range using a condition inside comprehension.
```python
list3=[i for i in range(11) if i%2==0]
print(list3)
'''
Output:
[0, 2, 4, 6, 8, 10]
'''
```

##### String Operation In List Comprehension
Converting all strings to uppercase using comprehension.
```python
list4=["suraj","sachin","rahul"]
list5=[i.upper() for i in list4]
print(list5)
'''
Output:
['SURAJ', 'SACHIN', 'RAHUL']
'''
```

---
## Dictionary Comprehension

##### Basic Dictionary Comprehension
Creating a dictionary with numbers as keys and their squares as values.
```python
list1=[1,2,3,4,5]
dict1={i:i**2 for i in list1}
print(dict1)
'''
Output:
{1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
'''
```

##### Dictionary Comprehension With User Input Students
Taking student name and age as input and storing in a dictionary.
```python
count=input("Enter Student Details count:")
result={input("Enter Student Name:"):int(input("Enter Student age:")) for i in range(int(count))}
print(result)
'''
Output:
{'suraj': 20, 'aarish': 24}
'''
```

##### Dictionary Comprehension With User Input Products
Taking product name and price as input and storing in a dictionary.
```python
p_count=int(input("Enter product details count: "))
result={input("Enter the product name: "):int(input("Enter the product price: ")) for i in range(p_count)}
print(result)
'''
Output:
{'chai': 15, 'biscuit': 10, 'coffee': 10}
'''
```

---
## Generator

##### Generator Concept
- pre defined function (method)
- A special type of function where values are iterated one at a time.
- The entire sequence is not stored in memory. Uses `yield` keyword instead of `return`.
- Reserves state between iterations unlike normal functions.
- Multiple values can be returned using yield.

### Benefits Of Generators

1. **Memory efficient** – Generators produce one value at a time instead of storing all values in memory.
2. **Lazy evaluation** – Values are generated only when needed, making them efficient for large datasets.
3. **Executes line by line** – The function pauses at each `yield` statement and resumes from there when the next value is requested.
4. **Faster for large data** – Since values are generated on demand, they can process large amounts of data more efficiently.
5. **Easy to work with streams** – Useful for reading large files, processing data streams, or handling infinite sequences.

### Basic Generator With Yield
Generator function pauses and resumes execution using `yield`. Each `yield` returns a value.

```python
def my_gen():
    yield 1
    yield 2
    yield 3
    yield 4

for i in my_gen():
    print(i)
'''
Output:
1
2
3
4
'''
```

#### Generator With While Loop
Generator can use a loop to yield values dynamically until a condition is met.

```python
def gen2(n):
    count=1
    while count<=n:
        yield count
        count+=1

for i in gen2(10):
    print(i)
'''
Output:
1
2
3
4
5
6
7
8
9
10
'''
```

#### Using Next On Generator
`next()` fetches the next yielded value from the generator one at a time.

```python
def gen3():
    yield 1
    yield 2
    yield 3
    yield 4

var=gen3()
print(next(var))
print(next(var))
print(next(var))
print(next(var))
'''
Output:
1
2
3
4
'''
```

#### Using Iter And Next On List
`iter()` converts a list into an iterator. `next()` fetches elements one by one.

```python
list1=[1,2,3,4,5]
iter1=iter(list1)
print(next(iter1))
print(next(iter1))
print(next(iter1))
print(next(iter1))
print(next(iter1))
'''
Output:
1
2
3
4
5
'''
```

#### Generator Expression
Using parentheses `()` creates a generator expression. Values are generated lazily, not stored in memory.

```python
squ=(i**2 for i in range(5))
print(squ)
for j in squ:
    print(j)
'''
Output:
<generator object <genexpr> at 0x0000013F68B836B0>
0
1
4
9
16
'''
```

#### List Comprehension Vs Generator For Even Numbers
List comprehension stores all values in memory. Generator yields values one at a time, saving memory.

```python
eve = [i for i in range(10) if i%2==0]
for j in eve:
    print(j)
print()

def pr_eve(n):
    for i in range(n):
        if i%2==0:
            yield i

for j in pr_eve(10):
    print(j)
'''
Output:
0
2
4
6
8

0
2
4
6
8
'''
```

---
## Class And Oops Revise 
class variable is decalred inside the class , class variable is shared by all the objects in the class , 

![[Pasted image 20260722170831.png]]


### Class Method Vs Instance Method

| ** Class Method**                           | ** Instance Method **                            |
| ------------------------------------------- | ------------------------------------------------ |
| Defined using `@classmethod` decorator.     | Defined normally without any decorator.          |
| Takes `cls` as the first parameter.         | Takes `self` as the first parameter.             |
| Works with **class variables**.             | Works with **instance variables**.               |
| Can be called using the class or an object. | Usually called using an object (instance).       |
| Used to modify or access class-level data.  | Used to perform operations on a specific object. |

class variable 
all object copy the same variable 
object name is use to access the class 

instance variable is used to make each object , so that it doesnt effect each other 
instance method use self key to acces the varialbe

class method to access the class u use @classmethod

we use @staticmethod there is no **cls** and **self**  method  

##### Class Variable
Class variable is shared by all objects. Every object accesses the same variable value.
```python
class student:
    name="suraj" #class variable
    age=20
obj1=student()
obj2=student()
print(obj1.name)
print(obj2.age)
'''
Output:
suraj
20
'''
```

##### Instance Variable With Constructor
Instance variable is unique to each object. `__init__` constructor assigns values using `self`.
```python
class Student:
    def __init__(self,name,age): #constructor
        self.name=name
        self.age=age

obj1=Student("suraj",20)
obj2=Student("sachin",21)
print(obj1.name, obj1.age)
'''
Output:
suraj 20
'''
```

##### Instance Method
Instance method uses `self` to access and display instance variables for each object.
```python
class Student:
    def __init__(self,name,age): #constructor
        self.name=name
        self.age=age
    def display(self):
        print("Name:",self.name)
        print("Age:",self.age,'\n')
obj1=Student("suraj",20)
obj2=Student("sachin",21)
obj1.display()
obj2.display()
'''
Output:
Name: suraj
Age: 20 

Name: sachin
Age: 21 

'''
```

##### Class Method
Class method uses `@classmethod` decorator and `cls` parameter to access class variables directly.
```python
class student:
    name="suraj"
    @classmethod
    def display(cls):
        print("Name:",cls.name)
obj1=student()
obj1.display()
'''
Output:
Name: suraj
'''
```

##### Static Method
Static method uses `@staticmethod` decorator. No `self` or `cls` needed. Can be called using class name directly.
```python
class student:
    name="suraj"
    @staticmethod
    def display():
        print("Name:",student.name)
obj1=student()
obj1.display()
'''
Output:
Name: suraj
'''
```

##### Method Overloading
Python does not support true method overloading. Use default parameters to handle variable arguments.
```python
class Student:
    def add(self,a,b,c=0):
        return a+b+c

obj1=Student()
print(obj1.add(10,20))
print(obj1.add(10,20,30))
'''
Output:
30
60
'''
```

##### Method Overriding
Child class provides its own implementation of a method that exists in the parent class.
```python
class Animal:
    def sound(self):
        print("Animal makes a sound")

class Dog(Animal):
    def sound(self):      # Overriding parent method
        print("Dog barks")

d = Dog()
d.sound()
'''
Output:
Dog barks
'''
```

---
## Magic Method
Magic method are special method called automatically .
we use __ __ (double underscore between the majic method )
ex: __ init __ (no spaces)

![[WhatsApp Image 2026-07-23 at 4.39.38 PM.jpeg]]

##### Str Method
`__str__` defines what `print()` outputs for an object. Returns a human-readable string.

```python
class Student:
    def __init__(self,name):
        self.name=name
    def __str__(self):
        return f"student ID {self.name}"

std=Student("suraj")
print(std)
'''
Output:
student ID suraj
'''
```

##### Len Method
`__len__` defines what `len()` returns for an object. Returns the length of the object.

```python
class Student:
    def __init__(self,names):
        self.names=names
    def __len__(self):
        return len(self.names)

list1=Student(["suraj","lucky","ram"])
print(len(list1))
'''
Output:
3
'''
```

##### Add Method
`__add__` defines the `+` operator for objects. Allows adding two objects together.

```python
class Student:
    def __init__(self,num):
        self.num=num
    def __add__(self,var):
        return Student(self.num+var.num)
    def __str__(self):
        return f" {self.num}"

std=Student(10)
obj=Student(20)
print(std+obj)
'''
Output:
 30
'''
```

--- 
## Decorator

A decorator is a function that takes another function, adds behavior, and returns it—without changing the original code.

##### Function As Variable
A function can be stored in a variable and called through it.

```python
def hello():
    print("hello")

var = hello  # function stored in variable
var()        # calls hello()
'''
Output:
hello
'''
```

##### Function As Parameter
Passing a function as an argument to another function.

```python
def hello():
    print("hello")

def display(func):
    func()

display(hello)
'''
Output:
hello
'''
```

##### Basic Decorator Pattern
Decorator wraps a function and adds extra behavior before and after.

```python
def decorator(func):
    def inner():
        print("Before")
        func()
        print("After")
    return inner

@decorator
def welcome():
    print("welcome")

welcome()
'''
Output:
Before
welcome
After
'''
```

`@decorator` is shorthand for `welcome = decorator(welcome)`

##### Decorator With Arguments
Decorator handles `*args` and `**kwargs` to support any function signature.

```python
def decorator(func):
    def wrapper(s, *args, **kwargs):
        print("Before")
        func(s, *args, **kwargs)
        print("After")
    return wrapper

@decorator
def add(s, a, b):
    print(s, a + b)

add("Result:", 2, 4)
'''
Output:
Before
Result: 6
After
'''
```

- `*args` → handles positional arguments
- `**kwargs` → handles keyword arguments

##### Remember

> Decorators wrap a function to add behavior before and after, without changing the original code.

---

## Builtin Modules

##### Import Vs From
- **`import module`** → use `module.function()`
- **`from module import function`** → use `function()` directly

```python
# import
import math
math.sqrt(16)  # need module name

# from
from math import sqrt
sqrt(16)  # no module name needed
```

##### Math Module
`math.sqrt()` → square root of a number.

```python
import math
math.sqrt(16)  # 4.0
```

##### Datetime Module
`datetime.datetime.now()` → current date and time.

```python
import datetime as dt
dt.datetime.now()  # 2026-07-30 16:31:50.023204
```

##### Random Module
`randint(a, b)` → random integer between a and b.

```python
from random import randint
randint(1, 10)  # e.g. 7
```

##### Custom Modules
**mymodule.py**
```python
def addition(a, b):
    return a + b

def subtraction(a, b):
    return a - b
```

**main.py**
```python
import mymodule as mm

mm.addition(5, 10)  # 15
mm.subtraction(10, 5)  # 5
```

##### Importing Classes From Modules
Use `from module import ClassName` to import a specific class.

**display.py**
```python
class Myclass:
    def display(self, name):
        return f"Hello {name}!"
```

**main.py**
```python
from display import Myclass

obj = Myclass()
obj.display("Anudip")  # Hello Anudip!
```

##### Dir Function
`dir(module)` → lists all attributes and methods of a module.

```python
import os
dir(os)  # ['F_OK', 'mkdir', 'chdir', ...]
```

##### Os Module
`os.mkdir()` → creates a directory.
`os.chdir()` → changes current directory.
`os.path.abspath()` → gets full path.

```python
import os
os.mkdir("sample")
os.chdir("sample")

with open("sample.txt", "w") as f:
    f.write("Hello!")

os.path.abspath("sample.txt")  # full path
```

##### Sys Module
- `sys.path` → Python search paths
- `sys.platform` → OS name
- `sys.version` → Python version

```python
import sys
sys.path  # list of paths
sys.platform  # 'win32'
sys.version  # '3.12.10'
```

> **Remember:** Use `import` when you need the full module, use `from...import` when you need specific functions or classes.
