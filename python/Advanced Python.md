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
  - [Basic Generator With Yield](#"Basic""Generator""With""Yield")
  - [Generator With While Loop](#"Generator""With""While""Loop")
  - [Using Next On Generator](#"Using""Next""On""Generator")
  - [Using Iter And Next On List](#"Using""Iter""And""Next""On""List")
  - [Generator Expression](#"Generator""Expression")
  - [List Comprehension Vs Generator For Even Numbers](#"List""Comprehension""Vs""Generator""For""Even""Numbers")

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

#### Basic Generator With Yield
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
