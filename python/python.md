- [Python](#"Python")
- [What Is Python](#"What""Is""Python")
- [Why Use Python](#"Why""Use""Python")
- [What Is Editor](#"What""Is""Editor")
- [Basic Concepts](#"Basic""Concepts")
  - [Function](#"Function")
  - [Variable](#"Variable")
    - [Rules For Variable](#"Rules""For""Variable")
    - [To Check The Inbuilt Keywords](#"To""Check""The""Inbuilt""Keywords")
    - [Global Local Variable](#"Global""Local""Variable")
  - [Comment](#"Comment")
  - [Constant Variable](#"Constant""Variable")
- [Function](#"Function")
- [Operators](#"Operators")
- [What Are Different Statements In Python](#"What""Are""Different""Statements""In""Python")
- [Match Case Switch Case](#"Match""Case""Switch""Case")
  - [Armstrong Number](#"Armstrong""Number")
  - [Fibonacci Series](#"Fibonacci""Series")
  - [Perfect Number](#"Perfect""Number")
  - [Function Function Pdf](#"Function""Function""Pdf")
    - [Why Use Function](#"Why""Use""Function")
    - [Two Types Of Function](#"Two""Types""Of""Function")

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
### Function
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

## Function
To create a function in python we use the def keyword 
```python
name='jethalal'
def display():
    print(name)
display()
```

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

## What Are Different Statements In Python
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

### Function Function Pdf

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

