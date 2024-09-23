Resources:
[W3 Schools](https://www.w3schools.com/)
____
### Print 

``` python 
# Print in terminal
print() 
# formatting print
print(f"formatting results: {x}")
print("{H} {W} ".format(H="Hello",W="World"))
```
### Basic Data Types

```python
# list
list =  [1,2,3,4,5]
	print(list[0:3])
	# indexing--^ 
	list[0] = "yes"
	# changing thing in that index
	
	list.append ("append")
	list.pop ()
	# add or remove from list

# Dictionary =  key / value pairs
dict = {"key1": 1, "key2": "banana"}

# tuple = fixed size, immutable (cannot be modified after creation)
tuple = (1,2,3,4,4,5)

# sets = unordered collection of unique elements / no duplicates shown
mysets = set("a","a",3,4.5)
some_set = {"apple","banana","cherry"}

```

[[Data Types Examples]]
###  Boolean and Logical Operators

```python
== equal 
!= not equal
<,> less/greater
<=,>= less or equal to / greater or equal to

#Logicial Operators
And = "this *and* that" # both have to occur 
or  = "this *or* that" # one has to occur
not = "opposite result" # 1==1? True, not 1==1? False
# ex:
print (1<2 and 2>3) #false
```
### If ,Else, Else if 

```python
x = 3
y = 2
if x>y:
	print("x is greater than")
elif x<y:
	print("y is greater than")
else:
	print("Invalid")
# 
```
### Loops

```python
# for loop
D = {"k1": 1, 'k2': 2, 'k3': 3}
for key, value in D.keys ():
    print (value)
    
# while loop
x = 0
while x <= 5:
    print (f"The current value of X is {x}")
    x += 1
else:
    print ("X has become 5")
```
### Break, Continue and Pass

```python 
x = "sammyY"
for letter in x:
    if letter == "a":
        continue
        # "Goes to the top of the closest enclosing loop" so continues.
        pass
    if letter == "Y":
        break
        # here it stops the loop when it reaches "Y", so it doesnt include it
        pass
    print (letter)
```
### Various Useful Operators

```python
# range 
for num in range(0,10,2)
print(num)

# enumarate
word = "abcde"
for index, letter in enumerate (word):
    print (index, letter, "\n")
	# output:  0 a, 1 b, 2 c, etc

# zip
mylist1 = [1, 2, 3, 4, 5, 6]
mylist2 = ["a", "b", "c"]
mylist3 = [100, 200, 300]
for a, b, c in zip (mylist1, mylist2, mylist3):
    print (a, b, c)
	# output:  1 a 100, 2 b 200, 3 c 300 / zips by shortest list 

# in 
print(x in [x,y,z])

# min/max
mylist = [1, 2, 30, 50, 174]
print (min (mylist))
print (max (mylist))

# user input 
x = input("Type something: ")
print(x)
```
### List Comprehension

```python
# create a new list from existing list with shorter syntax
# Original Code: 
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []
for x in fruits:
  if "a" in x:
    newlist.append(x)
print(newlist)

# List Comprehension
fruits = ["apple", "banana", "cherry", "kiwi", "mango"] 
newlist = [x for x in fruits if "a" in x]  
print(newlist)
```

[[Data Types Examples# List Manipulation]]
### Functions

```python
def my_function():
	print("Hello from Function")

my_function()

	# Parameter = what the function requires
	# arguments = what the function is given 
	
def name_call(fname,lname) # parameters
	print (fname+" "+lname)
name_call("Taro","Ingao") # arguements

```
### Lambda 

```python
# lambda = small anonymous function |  arguments:expression
x = lambda a,b,c: a+b+c
print(x(4,3,2)) # output: 9

```
### Classes and Objects 

```python 
# the essence of OOP 
# class = a blueprint for creating objects

class Person:
	def __init__(self, name, age)
	self.name = name
	self.age  = age
	
	# __str__ =  what should be returned when represented as string
	def __str__(self):
	return f"{self.name}({self.age})"
	
	# Object Methods
	def myfunc(self):
		print("Hello my name is: " +self.name)

# Using the Class
P1 = Person("John",36)
print(P1.name) # "John"
print(P1.age) # 36
 
# Example
class something:
 # "lol" =  doesn't have to be "self" but has to be first parameter of function
	def __init__(lol,date,time):
		lol.date = date
		lol.time = time

# Child Class - Inheritance
class Student(Person):
	def __init__ (self, fname, lname)
	 pass # use when not adding additional other properties or methods
	self.graduationyear = year 
		# adding a method to the class


```
### Python Scope

```python
name = "This is a global function"

def greet():
    #         v-- Enclosed function / local
    #         v-- If we were to comment this out, then python will go the the global scope, finding out what name=
    name = "Sammy"

    def Hello():
        # Local
        name = "Im a local"
        print ("Hello," + name)

    Hello ()


print (greet ()) # output: Hello, I am local 
```

### Python Modules

```python
# modules are like code libraries. 

# mymodule.py / saved file
	def greeting(name):
		print("Hello"+ name)

# Other file / 
	import mymodule
	# syntax = module_name.function_name
	mymodule.greeting("Alice")

# there are many popular/useful modules out there
```
### File Handling

``` 
demofile.txt

Hello! Welcome to demofile.txt  
This file is for testing purposes.  
Good Luck!
``` 

```python
"r" # - Read - Default value. Opens a file for reading, error if the file does not exist

"a" # - Append - Opens a file for appending, creates the file if it does not exist

"w" # - Write - Opens a file for writing, creates the file if it does not exist

"x" # - Create - Creates the specified file, returns an error if the file exists

#In addition you can specify if the file should be handled as binary or text mode

"t" # - Text - Default value. Text mode

"b" # - Binary - Binary mode (e.g. images)
```
#### Opening a file

```python
f = open("demofile.txt", "a")
# or
f = open("C:\\myfiles\welcome.txt", "a")
	# a = appends, w = overwrites

f.write("Now there is more content!")
```
#### Creating/Deleting a file

```python
f = open("myfile.txt","x")

# Deleting / need to import OS
import os 
if os.path.exists("myfile.txt"):
	os.remove("myfile.txt")
else:
	print("File does not exist")
```

