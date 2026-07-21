- [Python](#"Python")
- [What Is Python](#"What""Is""Python")
- [Why Use Python](#"Why""Use""Python")
- [What Is Editor](#"What""Is""Editor")
- [Basic Concepts](#"Basic""Concepts")
  - [Functionn](#"Functionn")
  - [Variable](#"Variable")
    - [Rules For Variable](#"Rules""For""Variable")
    - [To Check The Inbuilt Keywords](#"To""Check""The""Inbuilt""Keywords")
    - [Global Local Variable](#"Global""Local""Variable")
  - [Comment](#"Comment")
  - [Constant Variable](#"Constant""Variable")
- [Operators](#"Operators")
- [Statements](#"Statements")
- [Match Case Switch Case](#"Match""Case""Switch""Case")
- [Armstrong Number](#"Armstrong""Number")
- [Fibonacci Series](#"Fibonacci""Series")
- [Perfect Number](#"Perfect""Number")
- [Function](#"Function")
	- [Why Use Function](#"Why""Use""Function")
    - [Two Types Of Function](#"Two""Types""Of""Function")
- [String](#"String")
  - [String Operations](#"String""Operations")
    - [Upper And Lower](#"Upper""And""Lower")
    - [Replace](#"Replace")
    - [Split And Join](#"Split""And""Join")
    - [Find Len Count](#"Find""Len""Count")
    - [Startswith And Endswith](#"Startswith""And""Endswith")
    - [Strip,Lstrip,Rstrip](#"Strip,Lstrip,Rstrip")
    - [Isalpha,Isdigit,Isalnum](#"Isalpha,Isdigit,Isalnum")
    - [Indexing And Slicing](#"Indexing""And""Slicing")
- [List](#"List")
  - [Update List Element](#"Update""List""Element")
  - [Functions In List](#"Functions""In""List")
    - [Append And Length](#"Append""And""Length")
    - [Insert](#"Insert")
    - [Remove](#"Remove")
    - [Pop](#"Pop")
    - [Index](#"Index")
    - [Count](#"Count")
    - [Sort And Reverse](#"Sort""And""Reverse")
    - [Copy](#"Copy")
    - [Descending Sort](#"Descending""Sort")
    - [Looping In List](#"Looping""In""List")
  - [Assignments In List](#"Assignments""In""List")
- [Dictionary](#"Dictionary")
  - [Dictionary Functions](#"Dictionary""Functions")
    - [Create And Copy Dictionary](#"Create""And""Copy""Dictionary")
    - [Clear Dictionary](#"Clear""Dictionary")
    - [Items, Get, Keys, Values](#"Items,""Get,""Keys,""Values")
    - [Pop](#"Pop")
    - [Popitem](#"Popitem")
  - [Looping Through Dictionary](#"Looping""Through""Dictionary")
    - [Looping Through Dictionary Keys](#"Looping""Through""Dictionary""Keys")
    - [Looping Through Dictionary Values](#"Looping""Through""Dictionary""Values")
    - [Looping Through Key–Value Pairs](#"Looping""Through""Key–Value""Pairs")
   - [Update Dictionary Value](#"Update""Dictionary""Value")
   - [Duplicate Keys Overwrite](#"Duplicate""Keys""Overwrite")
   - [Multiple Keys In Dictionary](#"Multiple""Keys""In""Dictionary")
   - [Nested Dictionary](#"Nested""Dictionary")
   - [Check If Key Exists](#"Check""If""Key""Exists")
- [File Handling](#"File""Handling")
- [OOP Class And Object Code](#"OOP""Class""And""Object""Code")
  - [Basic Dog Class With Description](#"Basic""Dog""Class""With""Description")
  - [Dog Class With Bark Method](#"Dog""Class""With""Bark""Method")
- [Inheritance Code](#"Inheritance""Code")
  - [Multilevel Inheritance](#"Multilevel""Inheritance")
  - [Hierarchical Inheritance](#"Hierarchical""Inheritance")
  - [Single Inheritance With Super](#"Single""Inheritance""With""Super")
  - [Method Overriding](#"Method""Overriding")
  - [Multiple Inheritance](#"Multiple""Inheritance")
- [Encapsulation Code](#"Encapsulation""Code")
  - [Private Variable With Double Underscore](#"Private""Variable""With""Double""Underscore")
- [Exception Handling Code](#"Exception""Handling""Code")
  - [Try Except Finally](#"Try""Except""Finally")
  - [Custom Exception With Raise](#"Custom""Exception""With""Raise")
- [Tuple](#"Tuple")
  - [Tuple Functions](#"Tuple""Functions")
    - [Create Tuple And Access Elements](#"Create""Tuple""And""Access""Elements")
    - [Tuple Concatenation](#"Tuple""Concatenation")
    - [Tuple Membership](#"Tuple""Membership")
    - [Tuple Repetition, Length, Count](#"Tuple""Repetition,""Length,""Count")
    - [Min And Max In Tuple](#"Min""And""Max""In""Tuple")
    - [Sort Tuple](#"Sort""Tuple")
    - [Tuple Unpacking](#"Tuple""Unpacking")
    - [Sum Of Tuple Elements](#"Sum""Of""Tuple""Elements")
    - [Looping Tuple](#"Looping""Tuple")
- [Set](#"Set")
  - [Set Functions](#"Set""Functions")
    - [Creating Set And Empty Set](#"Creating""And""Empty""Set")
    - [Add, Remove, Discard, Clear](#"Add,""Remove,""Discard,""Clear")
    - [Union](#"Union")
    - [Intersection](#"Intersection")
    - [Difference](#"Difference")
    - [Symmetric Difference](#"Symmetric""Difference")
    - [Issubset](#"Issubset")
- [Object Oriented Programming Oops](#"Object""Oriented""Programming""Oops")
  - [Inheritance](#"Inheritance")
  - [Encapsulation](#"Encapsulation")
- [Exception Handling](#"Exception""Handling")
  - [Exception Interview Asked](#"Exception""Interview""Asked")

https://share.google/0chz6vfQdUuM0Q1ob

# Python
## What Is Python
- python is a high level programming language 
- easier to read and easier to understand
- automatic memory management 
- it provides a large built in libraries 
- created in 1991 
- creator Guido van Rossum
---
## Why Use Python
- easy to learn , easy to understand
- interpreted language (works line by line )
- Its a oops language
- cross-platform (python can run on any platform )
- large amount of libraries 
- open source 
---
## What Is Editor
to execute the code 
types of editor 
- vs code,  idle , jupyter , pycharm , spyder
---
## Basic Concepts
### Functionn
function is a block of statement where u can perform a particular task 
function=method 

### Variable
variable is a simple container where u can store and manage the data 
variable is mutable (changeable)

#### Rules For Variable
	variable cannot start with a number 
	variable can contain alpha numerical characters (0-9,@#$%)
	variable name are case sensitive
	don't use the keyword name as variables 

![[Pasted image 20260617163431.png]]
#### To Check The Inbuilt Keywords
```python
import keyword

liss=keyword.kwlist

print(liss)
```

#### Global Local Variable
if the variable declared inside the block is called **local** variable
	can only be used in the block 
the variable declared outside the block is called **global*** variable
	can be used anywhere inside or outside the block 

### Comment
used for adding comments and is not compiled in the code 
single line (#)
multiline (''' ''')

### Constant Variable
to make a constant variable u have to use capital letters 
ex :
```python
PI=3.14
```


---

## Operators
![[Pasted image 20260617170707.png]]
operands means the variables which are used 
![[Pasted image 20260617170811.png]]
![[Pasted image 20260617170851.png]]
![[Pasted image 20260617171131.png]]
Bitwise operator 
is used for binary manipulation directly  
![[Pasted image 20260617171212.png]]
![[Pasted image 20260617171608.png]]
![[Pasted image 20260617171744.png]]
![[Pasted image 20260617171756.png]]
![[Pasted image 20260617172201.png]]

## statements
What Are Different Statements In Python
![[Pasted image 20260624165254.png]]
1. assignment statement 
ex 
a=10 

2. expression statement 
this is theoratical  

3. print statement used to print the statement on the console 

4. input used to take input from the user to assign the particular value to the variable 

5. conditional statement 
```
bore hogaya 🥀
```
  break and continue statement 

6. looping statement 
	python does not support ```do while loop ```
![[Pasted image 20260624165844.png]]
```python

n=10
for i in range(1, n + 1):
    print(i)
```

7. return statement 
![[Pasted image 20260624170048.png]]



## Match Case Switch Case

```python
#write a program for match case (switch)
#1-Monday 2-Tuesday 3-Wednesday 4-Thursday 5-Friday 6-Saturday 7-Sunday
day=int(input("Enter a number between 1 to 7: "))
match day:
    case 1:
        print("Monday")
    case 2:
        print("Tuesday")
    case 3:
        print("Wednesday")
    case 4:
        print("Thursday")
    case 5:
        print("Friday")
    case 6:
        print("Saturday")
    case 7:
        print("Sunday")
    case _:
        print("Invalid input")
   #Enter a number between 1 to 7: 1
```



### Armstrong Number
when a numbers digit s are cubed and added together the result is equal to the original number
then its called armstrong number ex. 153 => 1^3 + 5^3 + 3^3 = 153

```python
n=int(input("Enter your number "))
sum=0
temp=n
while temp>0:
    digit=temp%10
    sum+=digit**3
    temp//=10

if n == sum:
    print(n, "is an Armstrong number")
else:
    print(n, "is not an Armstrong number")
   
'''
output of 153
153, is an Armstrong number
 '''
```

### Fibonacci Series
Fibonacci series is a series of numbers where each number is the sum of the two preceding ones, usually starting with 0 and 1.

```python
n=int(input("Enter number for fibonacci"))
a=1
b=1
for i in range (1,n+1):
    print(a)
    c=a+b
    a=b
    b=c
'''output of 8
1 1 2 3 5 8'''
```

### Perfect Number
  A number is perfect when the sum of its proper divisors is equal to the number itself. For example, 6 is a perfect number because its divisors are 1, 2, and 3, and their sum is 6.
```python
  n = int(input("Enter a number: "))
sum = 0
for i in range(1, n):
    if n % i == 0:
        sum += i
        
if sum == n:
    print("The number is a perfect number.")
else:
    print("The number is not a perfect number.")
'''
output of 6
The number is a perfect number.
 ''' 
    
```

### Function
<a href="obsidian://open?vault=Anudip-obsidian-vault&file=python%2Fpython%20pdf%2FFunctions.pdf">Function Pdf</a> <a href="obsidian://open?vault=Anudip-obsidian-vault&file=python%2Fpython%20ipynb%2Fday6.ipynb">Function code </a>

- it is a collection of statement used for performing a particular task
- is a reusable block (can be used n number of times)

birthday party rajnish ka
birthday party is a function 
```birthday
function birthday(gift){
gift is parameter
rajnish=gift 
returngift=chana 
return returngift
}
```
#### Why Use Function
- To *reduce* code by using reusable code block 
- testing becomes easier by using functions
- Debugging and checking the flow of the task becomes easy (by making different modules of the task )
- 
![[Pasted image 20260629164127.png]]


#### Two Types Of Function
built in function, user defined function

1. User defined : declared by the user 
```python 
def function_name(parameters): 
""" Docstring (optional): Description of the function. """ 
# Function body: Statements to perform the task 
result = ...
return result # Return statement (optional)
```

2. Built in :declared within the system (int)
![[Pasted image 20260629164446.png]]
![[Pasted image 20260629165327.png]]
![[Pasted image 20260629165410.png]]

## String
<a href="obsidian://open?vault=Anudip-obsidian-vault&file=python%2Fpython%20ipynb%2Fday7.ipynb">String Code </a>

What is a String
- string is a sequence of character enclosed in a single or double quote 
declared in 2 ways ⇒ '' , ""
- string is immutable 
- string starts from the index 0


### String Operations

##### Upper And Lower
Used to convert a string into uppercase or lowercase.

```python
str_val = "Suraj"
print("Upper case:", str_val.upper())
print("Lower case:", str_val.lower())

'''
Output:
 Upper case: SURAJ
 Lower case: suraj
'''
```

##### Replace
Used to replace one part of a string with another value.

```python
str1 = "I am learning python programming"
rep = str1.replace("python", "java")
print("Replaced string:", rep)

'''
Output:
 Replaced string: I am learning java programming
'''
```


##### Split And Join
`split()` breaks string into a list, and `join()` combines list items into one string.

```python
str2 = "I am learning python programming"
print("Split string:", str2.split(" "))

str3 = ["i", "am", "learning", "python", "programming"]
print("Joined string:", "".join(str3))

'''
Output:
 Split string: ['I', 'am', 'learning', 'python', 'programming']
 Joined string: iamlearningpythonprogramming
'''
```

##### Find Len Count
Used to find index, total length, and number of occurrences.

```python
str4 = "I am learning python programming"
print("Index of 'python':", str4.find("python"))
print("Length of the string:", len(str4))
print("Count of 'python':", str4.count("python"))

'''
Output:
 Index of 'python': 14
 Length of the string: 32
 Count of 'python': 1
'''
```

##### Startswith And Endswith
Checks if a string starts or ends with a specific pattern.

```python
str5 = "python"
print("Starts with 'py':", str5.startswith("py"))
print("Ends with 'on':", str5.endswith("on"))

'''
Output:
 Starts with 'py': True
 Ends with 'on': True
'''
```

##### Strip, Lstrip,Rstrip
Used to remove whitespace from both sides, left side, or right side.

```python
str6 = "        I am learning python programming     "
print("String after stripping whitespace:", str6.strip())
print("String after left stripping:", str6.lstrip())
print("String after right stripping:", str6.rstrip())

'''
Output:
 String after stripping whitespace: I am learning python programming
 String after left stripping: I am learning python programming     
 String after right stripping:         I am learning python programming
'''
```

##### Isalpha,Isdigit,Isalnum
Used to check character types inside the string.

```python
str7 = "python class"
print("String contains only alphabetic characters:", str7.isalpha())

str8 = "1234"
print("String contains only digits:", str8.isdigit())

str9 = "python class1234"
print("String contains only alphanumeric characters:", str9.isalnum())
print("String after removing whitespace:", str9.replace(" ", "").isalnum())

'''
Output:
 String contains only alphabetic characters: False
 String contains only digits: True
 String contains only alphanumeric characters: False
 String after removing whitespace: True
'''
```

##### Indexing And Slicing
Used to access characters using index positions.

```python
str10 = "python"
print("Second last character:", str10[-2])
print("First two characters:", str10[:2])
print("Characters from index 0 to 2:", str10[0:2])
print("Characters from index 2 to end:", str10[2:])
print("Characters from index 2 to 6:", str10[2:6])

'''
Output:
 Second last character: o
 First two characters: py
 Characters from index 0 to 2: py
 Characters from index 2 to end: thon
 Characters from index 2 to 6: thon
'''
```

## List
is a one data structure where we can store various datatypes values 

- list is mutable (changeable),and stores heterogenous values
- not fixed size ,dynamic size, (shrink and grow ),
- heterogenous data =different types of data ,
- we can maintain the order , elements are stored and in the same sequence 

```python
#creating the list 
list1=["apple", 2,4.4,True]
print(list1) #accessing the list
print("Float value:",list1[2]) #accessing the float value
print("Boolean element:",list1[3]) #accessing the boolean element
print("Slice of list:",list1[1:3]) #accessing the slice of list

'''
Output:
 ['apple', 2, 4.4, True]
 Float value: 4.4
 Boolean element: True
 Slice of list: [2, 4.4]
'''
```

##### Update list element
Used to update value at a specific index.

```python
list1=["apple", 2,4.4,True]
list1[2]=10 
print("Updated list:",list1)

'''
Output:
 Updated list: ['apple', 2, 10, True]
'''
```

### Functions in list 
##### Append and length
`append()` adds element at the end and `len()` returns list size.

```python
list2=["banana",1,3.5]
list2.append("mango")
print("List with new element:",list2)
print("Length of the list:",len(list2))

'''
Output:
 List with new element: ['banana', 1, 3.5, 'mango']
 Length of the list: 4
'''
```

##### Insert
`insert()` adds an element at a specific index.

```python
list3=["grapes",5,2.5]
list3.insert(1,"kiwi")
print("List with inserted element:",list3)

'''
Output:
 List with inserted element: ['grapes', 'kiwi', 5, 2.5]
'''
```

##### Remove
`remove()` deletes the first occurrence of a value.

```python
list4=["orange",3,1.5]
list4.remove(3)
print("List after removing 3 element:",list4)

'''
Output:
 List after removing 3 element: ['orange', 1.5]
'''
```

##### Pop
`pop()` removes and returns element from given index.

```python
list5=["watermelon",4,2.0]
popped_element=list5.pop(1)
print("Popped element:",popped_element)
print("List after popping an element:",list5)

'''
Output:
 Popped element: 4
 List after popping an element: ['watermelon', 2.0]
'''
```

##### Index
`index()` returns the index of first occurrence.

```python
list6=["peach",6,3.0]
index_of_peach=list6.index("peach")
print("Index of 'peach':",index_of_peach)

'''
Output:
 Index of 'peach': 0
'''
```

##### Count
`count()` returns how many times a value appears.

```python
list7=["pear",7,3.5,"pear"]
count_of_pear=list7.count("pear")
print("Count of 'pear':",count_of_pear)

'''
Output:
 Count of 'pear': 2
'''
```

##### Sort and reverse
`sort()` arranges ascending and `reverse()` reverses the list.

```python
list8=[5,2,9,1,5,6]
list8.sort()
print("Sorted list:",list8)

list8.reverse()
print("Reversed list:",list8)

'''
Output:
 Sorted list: [1, 2, 5, 5, 6, 9]
 Reversed list: [9, 6, 5, 5, 2, 1]
'''
```

##### Copy
`copy()` creates a shallow copy of list.

```python
list9=["cherry",8,4.0]
list10=list9.copy()
print("Copied list:",list10)

'''
Output:
 Copied list: ['cherry', 8, 4.0]
'''
```

##### Descending sort 
using slicing and sorted
Two ways to get descending order list.

```python
list11=[1,2,34,53,6,7,8,9]
list11.sort()
print("Reversed sorted list:",list11[::-1])

list12=[1,2,32,44,5]
desc=sorted(list12,reverse=True)
print("Sorted list in descending order:",desc)

'''
Output:
 Reversed sorted list: [53, 34, 9, 8, 7, 6, 2, 1]
 Sorted list in descending order: [44, 32, 5, 2, 1]
'''
```

##### Looping in list 
(for, while, enumerate)
Used to iterate list elements in different ways.

```python
list13=[1,2,3,4,5,8]
print("for loop")
for i in list13:
    print("Element:",i)
print()

print("while loop")
i=0
while i<len(list13):
    print("Element:",list13[i])
    i+=1
print()

print("enumerate function")
list14=[1,22,26,41,5]
for index,value in enumerate(list14):
    print("Index:",index,"Value:",value)

'''
Output:
 for loop
 Element: 1
 Element: 2
 Element: 3
 Element: 4
 Element: 5
 Element: 8
 
 while loop
 Element: 1
 Element: 2
 Element: 3
 Element: 4
 Element: 5
 Element: 8
 
 enumerate function
 Index: 0 Value: 1
 Index: 1 Value: 22
 Index: 2 Value: 26
 Index: 3 Value: 41
 Index: 4 Value: 5
'''
```

### assignments in list 
1.  Even and odd numbers from list
Separates list values into even and odd lists.

```python
list15=[1,2,3,4,5,6,7,8,9,10]
even_numbers=[]
odd_numbers=[]
for i in list15:
    if i%2==0:
        even_numbers.append(i)
    else:
        odd_numbers.append(i)
print("Even numbers:",even_numbers)
print("Odd numbers:",odd_numbers)

'''
Output:
 Even numbers: [2, 4, 6, 8, 10]
 Odd numbers: [1, 3, 5, 7, 9]
'''
```

2. Maximum number in list
`max()` gives the largest value in the list.

```python
list16=[1,2,3,4,5,6,7,8,9,10]
max_number=max(list16)
print("Maximum number:",max_number)

'''
Output:
 Maximum number: 10
'''
```

3. Second largest number in list
Sort in reverse and pick index `1`.

```python
list17=[20,25,45,22,68]
list17.sort(reverse=True)
print("Second largest number:",list17[1])

'''
Output:
 Second largest number: 45
'''
```


## Dictionary
A **dictionary in Python** is a built‑in data structure that stores **key–value pairs**
where each key is **unique and immutable**, 
and values can be of any type.
Dictionaries are **mutable** and allow **fast access** to values using their keys.

- mutable 
- access the value with the help of the ==key== 
- duplicate key are not allowed 
- duplicate key added overwrites the previous key 
- value can be duplicates 

	dictionary is used with =>{key: value }

### Dictionary Functions

##### Create and copy dictionary
Create an empty or populated dictionary, and copy it using `copy()`.

```python
dict1={'Name':'Zara','course':'Python','id':123}
print(dict1)
print(dict1['Name'])

copy_student=dict1.copy()
print('copy function:',copy_student)

'''
Output:
 {'Name': 'Zara', 'course': 'Python', 'id': 123}
 Zara
 copy function: {'Name': 'Zara', 'course': 'Python', 'id': 123}
'''
```

##### Clear dictionary
`clear()` removes all key–value pairs from the dictionary.

```python
copy_student={'Name':'Zara','course':'Python','id':123}
copy_student.clear()
print('clear function:',copy_student)

'''
Output:
 clear function: {}
'''
```

##### Items, get, keys, values
Returns tuple list, value by key, all keys, and all values respectively.

```python
student1={'Name':'Zara','course':'Python','id':123}
student_items=student1.items()
print('.items() =>',student_items)
print('.get() =>',student1.get('Name'))
print('.keys() =>',student1.keys())
print('.values() =>',student1.values())

'''
Output:
 .items() => dict_items([('Name', 'Zara'), ('course', 'Python'), ('id', 123)])
 .get() => Zara
 .keys() => dict_keys(['Name', 'course', 'id'])
 .values() => dict_values(['Zara', 'Python', 123])
'''
```

##### Pop
`pop()` removes a key–value pair by key and returns the value.

```python
student1={'Name':'Zara','course':'Python','id':123}
value=student1.pop('course')
print('.pop() =>',value)
print(student1)

'''
Output:
 .pop() => Python
 {'Name': 'Zara', 'id': 123}
'''
```

##### Popitem
`popitem()` removes and returns the last inserted key–value pair as a tuple.

```python
dict1={"emp_id":101,"salary":10000,"dept":"IT"}
item=dict1.popitem()
print('.popitem() =>',item)

'''
Output:
 .popitem() => ('dept', 'IT')
'''
```

### Looping through dictionary 

1. Looping dictionary keys
Iterate over dictionary keys using a for loop.

```python
dict2={'Name':'Zara','course':'Python','id':123}
print('keys of the dictionary:')
for key in dict2:
    print(key)

'''
Output:
 keys of the dictionary:
 Name
 course
 id
'''
```

2. Looping dictionary values
Iterate over dictionary values using `dict.values()`.

```python
dict2={'Name':'Zara','course':'Python','id':123}
print("values for dictionary:")
for values in dict2.values():
    print(values)

'''
Output:
 values for dictionary:
 Zara
 Python
 123
'''
```

3. Looping through key–value pairs
Iterate over key–value pairs using `dict.items()`.

```python
dict2={'Name':'Zara','course':'Python','id':123}
print("key and values for dictionary:")
for key,values in dict2.items():
    print(key,values)

'''
Output:
 key and values for dictionary:
 Name Zara
 course Python
 id 123
'''
```

##### Update dictionary value
Access and update value by key name.

```python
dict3={"Name":"suraj"}
dict3["Name"]="suraj dobar"
print("updated dictionary:",dict3)

'''
Output:
 updated dictionary: {'Name': 'suraj dobar'}
'''
```

##### Duplicate keys overwrite
If same key added twice, last value overwrites the first.

```python
dict4={"Name":"suraj","course":"Python","Name":"suraj dobar"}
print("updated dictionary with duplicate key:",dict4)

'''
Output:
 updated dictionary with duplicate key: {'Name': 'suraj dobar', 'course': 'Python'}
'''
```

##### Multiple keys in dictionary
Store multiple key–value pairs with any data type.

```python
dict5={"suraj":99,"vikas":-99,"sachin":100}
print("dictionary with multiple keys:",dict5)

'''
Output:
 dictionary with multiple keys: {'suraj': 99, 'vikas': -99, 'sachin': 100}
'''
```

##### Nested dictionary
Dictionary inside a dictionary for hierarchical data.

```python
students={
    "101":{"Name":"suraj","course":"Python"},
    "102":{"Name":"vikas","course":"Java"},
}
print(students["101"]["Name"])

'''
Output:
 suraj
'''
```

##### Check if key exists
Use `in` operator to check key presence.

```python
dict6={"suraj":99,"vikas":-99,"sachin":100}
if "Aarish" in dict6:
    print("Aarish is present in the dictionary")
else :
    print("key not exist")

'''
Output:
 key not exist
'''
```

## Tuple
what is tuple :
A tuple is a collection which is ordered and **unchangeable**.
- tuple is immutable
- tuple maintains order 
- any type of data can be added 
- use the index to get the element 
- created using ()

### Tuple Functions
##### Create Tuple And Access Elements
Create empty, singleton, and multiple-element tuples, then access elements using index and slice.

```python
tuple1=()#empty tuple
tuple1=(10,)#singleton tuple
tuple2=(1,2,3,4,5)#multiple element tuple
print(tuple2)

tuple3=(1,2,3,4,5,6,7,8,9,10)
print("tuple3[1]:",tuple3[1])
print("tuple3[2:4]:",tuple3[2:4])
print("tuple3[-1]:",tuple3[-1])

'''
Output:
 (1, 2, 3, 4, 5)
 tuple3[1]: 2
 tuple3[2:4]: (3, 4)
 tuple3[-1]: 10
'''
```

##### Tuple Concatenation
Use `+` operator to combine two tuples.

```python
tuple4=(3,4,5,6,7)
tuple5=(1,2,3)
concat=tuple4+tuple5
print("tuple4+tuple5:",concat)

'''
Output:
 tuple4+tuple5: (3, 4, 5, 6, 7, 1, 2, 3)
'''
```

##### Tuple Membership
Use `in` and `not in` to check value presence.

```python
tuple6=(1,2,3,4,5)
print("5 in tuple6:",5 in tuple6)
print("5 Not in tuple6:",5 not in tuple6)

'''
Output:
 5 in tuple6: True
 5 Not in tuple6: False
'''
```

##### Tuple Repetition, Length, Count
Repeat tuples, get size, and count occurrences.

```python
tuple7=(1,2,3)
print("tuple7*3:",tuple7*3)
size=len(tuple7)
print("Size of tuple7:",size)
print("Count of 3 in tuple7:",tuple7.count(3))

'''
Output:
 tuple7*3: (1, 2, 3, 1, 2, 3, 1, 2, 3)
 Size of tuple7: 3
 Count of 3 in tuple7: 1
'''
```

##### Min And Max In Tuple
Use `min()` and `max()` to get smallest and largest values.

```python
tuple8=(3,0,2,7)
print("min(tuple8):",min(tuple8))
print("max(tuple8):",max(tuple8))

'''
Output:
 min(tuple8): 0
 max(tuple8): 7
'''
```

##### Sort Tuple
`sorted()` returns sorted values as a list.

```python
tuple9=(20,45,3,6)
result=sorted(tuple9)
print("sorted(tuple9):",result)

'''
Output:
 sorted(tuple9): [3, 6, 20, 45]
'''
```

##### Tuple Unpacking
Assign tuple values to multiple variables directly.

```python
tuple9=(20,45,3,6)
p,q,r,s=tuple9
print("unpacking of tuple9:",p,q,r,s)
print("p=",p)
print("q=",q)
print("r=",r)
print("s=",s)

'''
Output:
 unpacking of tuple9: 20 45 3 6
 p= 20
 q= 45
 r= 3
 s= 6
'''
```

##### Sum Of Tuple Elements
Use `sum()` to get total of numeric tuple values.

```python
tuple10=(5,34,21,6)
total=sum(tuple10)
print("sum(tuple10):",total)

'''
Output:
 sum(tuple10): 66
'''
```

##### Looping Tuple
Iterate tuple elements using a `for` loop.

```python
tuple10=(5,34,21,6)
print("for loop tuple10:")
for i in tuple10:
    print(i)

'''
Output:
 for loop tuple10:
 5
 34
 21
 6
'''
```


## Set

- set is a unique item made by using {}
- can be made by two ways => set constructor or {}
- set is mutable in nature
- no duplicate value allowed
- contain unordered values (output order may vary)

##### Creating and empty set
Create sets using `{}` and `set()`, and create empty set using `set()`.

```python
#creating set using curly braces 
newset={20,30,40,50,60}
print(newset)

#creating set using set() constructor
newset=set([20,30,40,50,60])
print(newset)

#for creating empty set we have to use set() constructor only 
emptyset=set()
print(emptyset)

'''
Output:
 {50, 20, 40, 60, 30}
 {40, 50, 20, 60, 30}
 set()
'''
```

### Set Functions
##### Add, remove, discard, clear
Basic modification methods for adding/removing values in sets.

```python
newset={10,20,30,40,50,60}
newset.add(70)
print(".add(70):",newset)

newset.remove(20)
print(".remove(20):",newset)

newset.discard(20)
print(".discard(20):",newset)

newset.clear()
print(".clear():",newset)

'''
Output:
 .add(70): {50, 20, 70, 40, 10, 60, 30}
 .remove(20): {50, 70, 40, 10, 60, 30}
 .discard(20): {50, 70, 40, 10, 60, 30}
 .clear(): set()
'''
```

#### Union
`union()` returns all unique elements from both sets.

```python
newset1={10,20,30,40,50,60}
newset2={40,50,60,70,80,90}
result=newset1.union(newset2)
print("newset1.union(newset2):",result)

'''
Output:
 newset1.union(newset2): {70, 40, 10, 80, 50, 20, 90, 60, 30}
'''
```

##### Intersection
`intersection()` returns common elements from both sets.

```python
newset3={10,20,30,40,50,60}
newset4={40,50,60,70,80,90}
result=newset3.intersection(newset4)
print("newset3.intersection(newset4):",result)

'''
Output:
 newset3.intersection(newset4): {40, 50, 60}
'''
```

##### Difference
`difference()` returns elements in first set but not in second set.

```python
newset5={10,20,30,40,50,60}
newset6={40,50,60,70,80,90}
result=newset5.difference(newset6)
print("newset5.difference(newset6):",result)

'''
Output:
 newset5.difference(newset6): {10, 20, 30}
'''
```

##### Symmetric difference
`symmetric_difference()` returns elements not common in both sets.

```python
newset7={10,20,30,40,50,60}
newset8={40,50,60,70,80,90}
result=newset7.symmetric_difference(newset8)
print("newset7.symmetric_difference(newset8):",result)

'''
Output:
 newset7.symmetric_difference(newset8): {70, 10, 80, 20, 90, 30}
'''
```

##### Issubset
`issubset()` checks whether all elements of one set are present in another.

```python
newset9={10,20,30}
newset10={10,20,30,40,50,60} 
result=newset9.issubset(newset10)
print("newset9.issubset(newset10):",result)

'''
Output:
 newset9.issubset(newset10): True
'''
```


## Object Oriented Programming OOPS 
[Classes and objects pdf](obsidian://open?vault=Anudip-obsidian-vault&file=python%2Fpython%20pdf%2FClasses%20and%20Objects.pdf)

- object is a instance of a class . variable of the class , real world entity 
- class is a blueprint where we create multiple objects , we define various data member and member functions 
- constructor is a special method used to initialize the object 

# kuch bhi nahi samja 🥀

class Student{
int a;
string name;
}


student() //constructor
{}
student(int a , string str) {} //parameterized constructor 

student()
{
a=20
name='aarish'
}
// default constructor 

//member function 

```python 
class Dog:
    #construcotr method
    def __init__(self, name, age):  
        self.name = name #attributes
        self.age = age
#method
    def bark(self):
        print(f"{self.name} barks!")
#creating objects (instances) of the Dog class
dog1 = Dog("Buddy", 3)
dog2 = Dog("Max", 5)
  
#Accessing attributes and calling methods

print(f"{dog1.name} is {dog1.age} years old.") #Output:Buddyis3yearsold
dog1.bark()
dog2.bark()
```

#### encapsulation :
capsule 
abe kya hai bhai kuch bhi nahi samaj ra 

binding your data and data function 
	
 <center><h1>pdf se padlo bc 🥀🥀 </h1></center>
 
 
 

## Inheritance 
<a href ="obsidian://open?vault=Anudip-obsidian-vault&file=python%2Fpython%20pdf%2FInheritance%20MethodOverriding.pdf"> inheritance pdf </a>

- to inherit the properties of another class 

## Encapsulation 
- binding the data and function together that operates as a single unit called class 
- to achieve the encapsultaion we use the access modifier called : public,  private, protected

example : capsule 

1. public 
	accessible anywhere 
2. private 
	accessible in the only class and is indicated by double underscore __
3. protected 
	protected data member access by subclass indicated by single underscore _

```python 
class Student:
    def __init__(self,name):
        self.__name=name
    def display(self):
        print(self.__name)

obj=Student("John")
obj.display()
```

## exception handling 
exception is the error that occur during the exectuion of the program and which stop your execution of the program and display the error message.

example

- zero division error (when we divide a number by zero)

- index error (when index out of range )

- type error (when we perform operation on different data type)

- value error (when we perform operation on invalid value)

- file not found error (when we try to open a file which is not present in the directory)

```python 
try :
    answer=10/0
except ZeroDivisionError:
    print("you cannot divide a number by zero")
```


try: the code which is going to throw erorr 
except : what error output should be 
finally always run no matter exception raise or not

when making custom exception 
we use raise 
``` python 
	age=int(input("enter your age"))
if age<18:
    raise ValueError("age should be greater than 18")
print("your age is",age)
```


### exception interview asked 

try : contain the code that raise the exception 
else : block executes only if no exception occurs 
finally : block executes always whether exception occurs or not 
except: that contain code that handle the exception 
raise : u can make custom exception using raise keyword 

	if try block raise the exception then except and finally block execute 

	if try block not raise exception then else and finally block will execute 



## file handling
file is used to store the data


## OOP - Class and Object Code

##### Basic Dog class with description
Creating a class with `__init__` constructor and a method that returns a formatted string.

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def description(self):
        return f"{self.name} is {self.age} years old."

my_dog = Dog("Buddy", 5)
print(my_dog.name)
print(my_dog.age)
print(my_dog.description())
'''
Output:
Buddy
5
Buddy is 5 years old.
'''
```

##### Dog class with bark method
Creating two objects of the same class and calling methods on each.

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"{self.name} barks!")

dog1 = Dog("Buddy", 3)
dog2 = Dog("Max", 5)

print(f"{dog1.name} is {dog1.age} years old.")
dog1.bark()
dog2.bark()
'''
Output:
Buddy is 3 years old.
Buddy barks!
Max barks!
'''
```

## Inheritance Code

##### Multilevel inheritance
Chain of inheritance: grandparent -> parent -> child. Each level adds its own method.

```python
class Anudip:
    def display(self):
        print("Anudip Foundation Thane")

class Rajshree(Anudip):
    def academy(self):
        print("Technical Professor: Rajshree maam")

class Student(Rajshree):
    def lerning(self):
        print("Stduent of anudip foundation")

std=Student()
std.display()
std.academy()
std.lerning()
'''
Output:
Anudip Foundation Thane
Technical Professor: Rajshree maam
Stduent of anudip foundation
'''
```

##### Hierarchical inheritance
One parent class with multiple child classes, each child inherits parent's methods.

```python
class Parent:
    def display(self):
        print("This is parent Class")

class Child1(Parent):
    def child_display(self):
        print("This is fist child Class")

class Child2(Parent):
    def child2(self):
        print("This is second child class method")

obj1=Child1()
obj2=Child2()

print("parent and Child 1 Class methods msg")
obj1.child_display()
obj1.display()

print("parent and Child 2 Class methods msg")
obj2.child2()
obj2.display()
'''
Output:
parent and Child 1 Class methods msg
This is fist child Class
This is parent Class
parent and Child 2 Class methods msg
This is second child class method
This is parent Class
'''
```

##### Single inheritance with super()
One parent, one child. `super()` is used to call parent constructor and methods.

```python
class Parent1:
    def __init__(self,name):
        self.name=name

    def parent_method(self):
        print("This is a parent class method")
        print(self.name)

class Child1(Parent1):
    def __init__(self,name,age):
        super().__init__(name)
        self.age=age

    def child_method(self):
        print("This is a child 1 class method")
        print(self.age)

obj=Child1("Shyam",20)
obj.parent_method()
obj.child_method()
'''
Output:
This is a parent class method
Shyam
This is a child 1 class method
20
'''
```

##### Method overriding
Child class provides its own implementation of a method already defined in parent class. Same name, same parameters.

```python
class Parent:
    def __init__(self):
        print("Parent Class Constructor")

    def display(self):
        print("parent method")

class Child(Parent):
    def __init__(self):
        print("Child Class Constructor")

    def display(self):
        super().__init__()
        print("Child Method")
        super().display()

obj=Child()
obj.display()
'''
Output:
Child Class Constructor
Parent Class Constructor
Child Method
parent method
'''
```

##### Multiple inheritance
One child inherits from more than one parent class.

```python
class Dog:
    def display(self):
        print("Dog Class")

class Cat:
    def cat_print(self):
        print("Cat Class")

class Animal(Dog,Cat):
    def animal_display(self):
        print("Child Class of both classes")

obj=Animal()
obj.display()
obj.cat_print()
obj.animal_display()
'''
Output:
Dog Class
Cat Class
Child Class of both classes
'''
```

## Encapsulation Code

##### Private variable with double underscore
Using `__` prefix to make a variable private. Accessible only within the class.

```python
class Student:
    def __init__(self,name):
        self.__name=name
    def display(self):
        print(self.__name)

obj=Student("John")
obj.display()
'''
Output:
John
'''
```

## Exception Handling Code

##### Try except finally
Handling errors using try, except, and finally blocks. `finally` always runs regardless of exception.

```python
try :
    answer=10/0
except ZeroDivisionError:
    print("you cannot divide a number by zero")

try :
    int(input("enter a number"))
except :
    print("invalid input")
finally:
    print("will run no matter exception occurs or not")
'''
Output:
you cannot divide a number by zero
invalid input
will run no matter exception occurs or not
'''
```

##### Custom exception with raise
Using `raise` to create a custom exception when a condition is not met.

```python
age=int(input("enter your age"))
if age<18:
    raise ValueError("age should be greater than 18")
print("your age is",age)
'''
Output:
ValueError: age should be greater than 18
'''
```

