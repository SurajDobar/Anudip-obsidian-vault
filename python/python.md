https://share.google/0chz6vfQdUuM0Q1ob

#  python 
## What is python ?
- python is a high level programming language 
- easier to read and easier to understand
- automatic memory management 
- it provides a large built in libraries 
- created in 1991 
- creator Guido van Rossum
---
## why use python ? 
- easy to learn , easy to understand
- interpreted language (works line by line )
- Its a oops language
- cross-platform (python can run on any platform )
- large amount of libraries 
- open source 
---
## what is editor 
to execute the code 
types of editor 
- vs code,  idle , jupyter , pycharm , spyder
---
## basic concepts 
### *function*
function is a block of statement where u can perform a particular task 
function=method 

### *variable*
variable is a simple container where u can store and manage the data 
variable is mutable (changeable)

#### Rules for variable 
	variable cannot start with a number 
	variable can contain alpha numerical characters (0-9,@#$%)
	variable name are case sensitive
	don't use the keyword name as variables 

![[Pasted image 20260617163431.png]]
#### to check the inbuilt keywords 
```python 
import keyword

liss=keyword.kwlist

print(liss)
```

#### Global , local variable 
if the variable declared inside the block is called **local** variable
	can only be used in the block 
the variable declared outside the block is called **global*** variable
	can be used anywhere inside or outside the block 

### *comment # ,''' '''*
used for adding comments and is not compiled in the code 
single line (#)
multiline (''' ''')

### *constant variable* 
to make a constant variable u have to use capital letters 
ex :
```python
PI=3.14
```


---

## function 
To create a function in python we use the def keyword 
```python
name='jethalal'
def display():
    print(name)
display()
```

## operators 
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

## what are different statements in python 
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
#write a program to print number from 1 to n take the value of n from the user , using for loop
n = int(input("Enter a number: "))
for i in range(1, n + 1):
    print(i)
```

7. return statement 
![[Pasted image 20260624170048.png]]



## Match case (switch case)

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



### Armstrong number 
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

### Fibonacci series 
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

### Perfect number 
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