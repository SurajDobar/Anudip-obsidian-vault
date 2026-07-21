## List comprehension

##### Basic list comprehension
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

##### List comprehension with condition
Filtering even numbers from a range using a condition inside comprehension.
```python
list3=[i for i in range(11) if i%2==0]
print(list3)
'''
Output:
[0, 2, 4, 6, 8, 10]
'''
```

##### String operation in list comprehension
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

## Dictionary comprehension

##### Basic dictionary comprehension
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

##### Dictionary comprehension with user input (students)
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

##### Dictionary comprehension with user input (products)
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

##### Generator concept
A special type of function where values are iterated one at a time. The entire sequence is not stored in memory. Uses `yield` keyword instead of `return`. Reserves state between iterations unlike normal functions. Multiple values can be returned using yield.
