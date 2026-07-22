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

