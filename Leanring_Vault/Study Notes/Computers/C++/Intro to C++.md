# Quick Guide

```c++
//declaring a var
int number = 1;

// declaring constant
const double pi = 3.14;

// math expression
int x = 10+3;

// writing to console 
cout << "x = " << x;

// reading from console
cin >> number;

for ()

if ()

while()



```


# The Basics


**cout** = write out characters to the *Standard Output Stream*  / console or window
**cin**  = read data from the *Standard Input Stream* / keyboard

"<<" = Stream Insertion Operator - writes data to a stream
">>" = Stream Extraction Operator - read data from a stream

STL = Standard Template Library - consists of several file each containing functions for diff purpose 
- to use, **#include** *directive*

## Naming Conventions

``` C++
// Snake case
	int file_size
// Pascal case
	int FileSize
// Camel case
	int fileSize
// Hungarian Notation = first letter is data type
	int iFileSize

```


## Variables and Constants 
### Variables
- a **variable** is just a name of a location in memory that stores some value
- specify what data type
```C++
int filesize = 100; //best practice to initalize and define, if not then its garbage
double sales = 9.99;
// can also intialize multiple on the same line, although not recommended
double sales = 9.99, counter = 1.0;
```

**Exercise**: How can you change the value of 2 variables?

```C++
int a=1;
int b=2;
int temp=a;
a=b;
b=temp;
```

## Constants
- **constant ** = cannot be changed/modified once created and initialized
```c++
const double pi = 3.14;
```

## Math Expressions

```C++
+ , -, /, % (modulus / remainder from division) , * 
```

```C++
int x = 10; y = 3;
z = x/y; // will print a whole number, since x and y are int
// convert x or y to double

int x = 10;
double y = 3;
z  = x/y; // will return double 

```

### Incrementing 

```C++
int x = 10;

int y = x++; // y = 10, x = 11

// OR


int z = ++x; // z = 11, x = 11

```


### Order of Operations
- follows PEMDAS

```C++
double x = 1 + 2 * 3; // 7 
double y =5;
double z = (x+10)/(3*y);
```


## Writing and Reading to Console

```C++
int x = 10;
int y = 20;
std::cout << "x = " << x; // x = 10
std::cout << "y = " << y; // y = 20
// together it will print: x = 10y = 20
// add std::endl at the end
std::cout << "x = " << x << std::endl;
// combine the lines
std::cout << "x = " << x std:endl 
		   << "y = " << y;
```

### using namespace std;
- allows us to not have to call `std` every time, such as:
```c++
using namespace std;

cout << "x = " << x << endl 
	 << "y=  " << y;

//notice how we didn't do std::cout
```


**Exercise**: given sales, calculate state, county and total tax to be paid

```c++
using namespace std;
int main(){
int sales = 95000;
double state_tax = .04;
double county_tax = .02;

double total_tax = (sales*state_tax)+(sales*county_tax);

cout << "total tax is: " << total_tax << endl;
}

```

### reading from console

use `cout`

```c++
using namespace std;
int main() {
cout << "enter values: "
int x;
int y;
cin >> x;
cin >> y;
cout << x+y;

// as with cout, can chain w/ cin

cin >> x >> y;

```

### working with standard library

``` c++
#include <cmath>
// various standard libraries to be used, here additional math operators

double result = floor(1.2);

double result = power (lcpp_x:2,lcpp_y:3)
cout << result;
```


## comments

```
/* 
* multiline
*/

// single line
```


# Data Types

## Fundamental Data Types
 
```c++
int a = 4;
double b = 9.99;
floatc = 3.67F; // F/f for float, at the end of number
long d = 90000L; // L/l for long 
char letter = 'a';
string name "Mosh";
bool isValid = true/false;
auto letter = 'a'; // can use `auto` to let complier infer the type of var 
auto long_time = 90000L; // don't forget L notation for Long data type

sizeof(long_time); // number of bytes taken by data type

int numbers[] = {1,2,3};
cout <<numbers[0];

```

a better way to initialize a variable is with {}
- forces red underline in IDE, compiler won't execute code
	- double checks for us to make sure that given value is correct for a variable

```c++
int number = 1.2;
cout << number;
// returns 1

int number {1.2};
cout << number;
// returns error

int number {1};
// correct

int number {};
// will set number = 0, instead of garbage

```

**Number systems**

| System                | Digits   | Example |
| --------------------- | -------- | ------- |
| Decimal (base 10)     | 0-9      | 255     |
| Binary (base 2)       | 0,1      | 111101  |
| Hexadecimal (base 16) | 0-9, A-F | FCFCFC4 |

```C++
int number = 0b11111111; // 255 in binary
int number = 0xff; // 255 in hexadecimal
int number = 255 // 255 in decimal
```


## Casting  

```C++
// C style casting 
double a = 2.0;
int b = (int) a;

//C++ style casting
int c  = static_cast<int>(a);


```


## Conversions

### widening
- conversions that preserve information   `char`  to `int`
### narrowing
- conversions that may lose information, such as `int` to  `char` 
when you initialize a variable of a smaller type using a larger type
aka long long => int

```c++
int number = 100'000'0000;
short another = number; // 16960 
						// narrowing occured
short another {number}; // throw error

// the inverse can also be done 
short number = 100;
int another = number;
```

## checking narrowing
- we can check whether a variable can be narrowed, by the 4 different notations that C++ provides
```c++
int x0 = 7.8; // narrows, some compilers warn 
int x1 {7.8}; // error : {} doesn’t narrow 
int x2 = {7.8}; // error : ={} doesn’t narrow (the redundant = is allowed) 
int x3 (7.8); // narrows, some compilers warn
```
- = & ={} come from C
## generating a "random" number

```C++
#include <cstdlib>
using namespace std;
include main(){
	int random = rand(); // will always give the same random number when re-run. 16807
	cout << random;
	return 0 
}
// can also seed the rand() w/ srand()
	srand(5)
	int random = rand();
	cout << random;
	return 0
```

so how can we truly get a completely random number? 
- by taking the time (in seconds) since Jan 1970 and putting that as the seed for the srand()

```c++
#include <cstdlib>
#include <ctime>

int main(){
	long elapsedSeconds = time(0); // Jan 1 1970
	srand(elapsedSeconds);
	int number = rand() % 10; // to make the number smaller 
	cout<<elapsedSeconds;
	return 0;
}
// simply 
srand(time(0))
rand()

```


# Decision Making

## Boolean

```c++
// Comparison Operators
bool a = 10 > 5; // true
bool b = 10 == 10; // true
bool c = 10 != 5; // true

// Logical Operators
bool d = a && b // AND
bool e = a || b // OR
bool f = !a;    // NOT


```
## If, else if, else

```c++
if (temp < 60) {
	//
} else if (temp < 90) {
	//
} else {
	//
}
```

## Conditional Operator

```C++
double commision  = (sales < 10'000) ? .05 : .1;
```

## Switch / Case

```c++
switch (menu){
	case 1:
	//
		break;
	case 2:
	//
		break;
	default:
	//
}```

# Loops
- *for loops* = know how many times to repeat something
	- *ranged based* = iterating over list of items
- *while*  = don't know how many times to repeat something, 10 or 100,000 items?
	- *do-while* 
*break*  = break out of loop
*continue* = skip an iteration


```c++
// For loops
for (int i=0;i<5;i++)
	cout << i << endl;

// Ranged Based for loop
int numbers [] = {1,2,3,4};
for (int number: numbers)
	cout << number << endl;

// While loop
int i = 0;
while (i<5){
	cout << i << endl;
	i++;
}

// Do-While
int i = 0;
do{
	cout << i << endl;
	i++;
} while (i<5);
```


# Functions
- **signature** of a function = includes name, and the name, order and type of parameters 
- **overloading** = creating another variation of the function with a different *signature*. 
	- can call function in diff ways

- args of a function can be passed by *value* or *reference*
	- args by value = they get copied to the parameters of the function 
	- args by reference = add & after the parameter type

- **function declaration** (prototype) =  tells compiler about the existence of a function ^1
- **function definition** (implementation) = provides the body (code) for the function^2
```c++
int square(int); // declaration of square double 
sqrt(double); // declaration of sqrt Note the terminating semicolons. 

/// A semicolon is used in a function declaration instead of the body used in the corresponding function definition: 

int square(int x){ // definition of square  
	return x∗x; 
}
```

*header file* = *.h* or *.hpp*, consists of function declarations and constants. imported using *'#include' directive*
-  tells compiler about the existence of a function ^1
*implementation file* = *.cpp*, consists of function definitions
- ^2 provides the body (code) for the function^2

- used in tandem to define and create functions 
#### void
- take no arguments, return no value

```c++

// Defining functions
void greet (string name){
	cout << "Hello "<< name;
}

string fullName(string firstName, string lastName){
	return firstName + ' ' + lastName;
}

// Parameters with default value
double calculateTax(double income, double taxRate = .3){
	return income * calculateTax; 
}

// Overloading functions
void greet (string name){
}

void greet (string title, string name){
}

// Reference parameters
void increase(double& number){
	number++;
}

// Function Declaration
void greet(string name);

// Defining a namespace
namespace messaging {
	void greet(string name) {}
}

// using a namespace
using namespace messaging;
// or
using messaging::greet;

```


# OOP in C++
## Classes and objects
**Access Modifiers**
	- Private      = only accessible inside the class
	- Public       = accessible outside of the class
	- Protected = in btwn private && public

```c++
using namespace std;

class Employee{
public: // access modifier
	string Name;
	string Company;
	int Age;

	void Introduction(){
	cout << "Name: "<<Name<<endl;
	cout << "Company: "<<Company<<endl;
	cout << "Age: "<<Age<<endl;

	}
}

int main ()
{
	Employee employee1;
	employee1.Name = 'Andre';
	employee1.Company = 'Youtube';
	employee1.Age =  '23';
	employee1.Introduction();
}
// what if we want to create multiple users? we can use constructors:
```

## Constructors
```c++
class Employee{
public: // access modifier
	string Name;
	string Company;
	int Age;

	void Introduction(){
	cout << "Name: "<<Name<<endl;
	cout << "Company: "<<Company<<endl;
	cout << "Age: "<<Age<<endl;

	}	
Employee(string name, string company, int age) //  Constructor | usually has same name as the class
	Name = name;
	Company = company;
	Age = age;
}
//
int main()
{
// class var = Constructor(parameters)
Employee employee1 = Employee ("Andre", "Youtube", 22);
employee1.Introduction

}
```


## Encapsulation
- keeping certain properties private within a class, and only allowing functions inside that class to interact with them

```c++
class Employee{
private:  // Private Properties
	string Name;
	string Company;
	int Age;

public:
// Functions that access properties
	void setName(string name) { // Setter
	Name = name;
	}
	string getName(){ // Getter
		return Name;
	}
	
	void setCompany(string Company) { // Setter
	Company = company;
	}
	string getCompany(){ // Getter
		return Company;
	}
	
		void setAge(int age) { // Setter
	Age = age;
	}
	int getAge(){ // Getter
		return Age;
	}
	
	void Introduction(){
	cout << "Name: "<<Name<<endl;
	cout << "Company: "<<Company<<endl;
	cout << "Age: "<<Age<<endl;
	}	

Employee(string name, string company, int age) 
	Name = name;
	Company = company;
	Age = age;
}
```

## Abstraction
- hiding the complex things to make it simple 
```c++


```