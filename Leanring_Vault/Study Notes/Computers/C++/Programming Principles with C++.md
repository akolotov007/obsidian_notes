
## 1.4 Linking
![[Pasted image 20240921123708.png]]


## 2.1 Input
![[Pasted image 20240921123925.png]]

```c++
#include "PPP.h"

int main(){
	cout << "Please enter your first name: \n";
	string first_name;
	cin >> first_name;
	cout << "Hello," << first_name << "!\n";
}
```


## 2.2 Variables
```c++
int		39
double	2.3	
char	'a'
string	"annemarie"
bool	true

```

## 2.4 Operations and operators
![[Pasted image 20240921124418.png]]

![[Pasted image 20240921124433.png]]

## 2.5 Assignment and initialization

![[Pasted image 20240921124535.png]]

*another example*

![[Pasted image 20240921124557.png]]

## 2.10 Type deduction: auto
```c++
// lets create 2 var
int x = 7;
double d = 7.7;
// we can let the compiler deduce the type from the initializer (after =)
auto x = 7;
auto d = 7.7;
```


## 3.3 Expressions
- computes a value from a number of operands
- names of variables are also expressions
	- `int length, width; length = 20; width = 40; int area = length*width; `

### 3.3.1 Constant Expressions
```c++
constexpr double pi = 3.14159
pi = 7 // error: constant
double c = 2*pi*r // works, since its being read
```


 a `constexpr` symbolic constant must be **given a value** that is known at compile time 
```c++
constexpr int max = 100;
int n; 
cin >> n;
constexpr int c1 = max+7; // 107
constexpr int c2 = n+7 // error: we don't know the value of n

```

if you want to initialize with the value unknown at compile time, but never changes, there is `const`

```c++
int n;
cin >> n;

const int c3 = n; // OK
c3 = 7            // error: c3 is a const
```

### 3.3.2 Operators
![[Pasted image 20240921130447.png]]
![[Pasted image 20240921130455.png]]

## 3.4.1.1 if-statements

```c++
if (expression)
	statement
else if (expression)
	statement
else
	statement
```

```c++
int a = 0;
int b = 0;
cout << "please enter 2 ints:\n";
cin >>a>>b;

if (a<b) // condition
	cout << a << "is smaller than" << b << '\n';
else
	cout << a << "is larger than or equal to" << b << '\n';
```


### 3.4.1.2 Switch Statements
```c++
switch (unit) {
case 'i':
	cout << length << "in == " << length∗cm_per_inch << "cm\n";
	break;
case 'c':
	cout << length << "cm == " << length/cm_per_inch << "in\n";
	break;
default:
	cout << "Sorry, I don't know a unit called '" << unit << "'\n";
	break;
}
```

### 3.4.1.3 switch technicalities
- the value on which we switch must be of `int`, `char`, or enumeration type.
	- can't switch on a `string` or `floating-point`
- value in *case* labels must be constant expression. 
	- you can't use a variable in a case label
- can't use the same value for two case labels
*page 63*

- forgetting to break from the switch statements, the case 'i' will "fall through" into case 'c'
```c++
switch (unit) {
	case 'i':
		cout << length << "in == " << length∗cm_per_inch << "cm\n";
	case 'c':
		cout << length << "cm == " << length/cm_per_inch << "in\n";
}
// 2in == 5.08cm 
// 2cm == 0.787402in
```

if rarely needed, you can explicitly say to **fall through**
```c++ 
switch (check) {
	case checked:
		if (val<0)
			val = 0;
		[[fallthrough]];
	case unchecked:
		// ...use val ...
		break;
}
```
## 3.6 Vectors
- a sequence of elements that you can access by an index. 
- stores elements && stores its size (bytes)
![[Pasted image 20240907231431.png]]

```c++
vector<int> v = {5,7,9,3,4}; // vector of 6 ints
// element type comes after the vector in <>

// will only accept elements of declared type
vector<string>philosopher = {"Kant", "Plato","Hume", "Kierkegaard"};
philosopher[2] = 99; // error : trying to assign an int to a string 

// can define/[declare?] size wo/ specifing element values
vector vi(6); // vector of 6 ints initialized to 0
vector vs(4); // vector of 4 strings initialized to ""


vector v = {5, 7, 9, 4, 6, 8}; 
for (int x : v) // for each x in v 
	cout << x << '\n';
```

### 3.6.2 Growing a Vector
- `push_back()` = adds new element to the *end* of the vector
![[Pasted image 20240907232140.png]]

### 3.6.4 A text Example

```c++
int main()
// simple dictionary: list of sorted words
{
	vector<string> words;
	for (string temp; cin >> temp; ) // read whitespace-separated words
		words.push_back(temp); // put into vector
	cout << "Number of words: " << words.size() << '\n';
	ranges::sort(words); // sort the words
	for (int i = 0; i < words.size(); ++i)
		if (i == 0 || words[i−1] != words[i]) // is this a new word? //
			cout << words[i] << "\n";
}
// input: a man a plan a canal panama
// output:
/* 
*a 
*canal 
*man
*panama
*plan
*/
```


# 4. Errors!
- *compile time errors*
	- syntax errors; Type errors
- *link time errors*
	- errors found by the linker when its trying to combine object files into an executable program
- *runtime errors* 
	- Errors found by checks in a running program. We can further classify runtime errors as:
		- Errors detected by the computer (hardware and/or operating system) 
		- Errors detected by a library (e.g., the standard library) 
		- Errors detected by user code 
	- Such errors are also called *Logic errors*.
- *Exceptions* 
	- Bad arguments; Range errors; Bad input 
- *Avoiding and finding errors* 
	- Estimation; Debugging; Assertions; Testing; Random numbers

- We ‘‘forgot’’ to mention two of the nastiest kind of errors: 
	- Undetected logic errors leading to crashes or wrong results. 
	- Mismatches between what the user needs and what the code delivers

### 4.2 Source of Errors
- Poor specification
- Incomplete programs
- Unexpected arguments
- Unexpected input
  Unexpected state
	  Most programs keep a lot of data (‘‘state’’) around for use by different parts of the system. Examples are address lists, phone directories, and vectors of temperature readings. What if such data is incomplete or wrong? The various parts of the program must still manage.
  Logical errors
	  code that simply doesn’t do what it was supposed to do

___
*from 4.6.3 Bad Input*

The standard library defines a few types of exceptions, such as the out_of_rang e thrown by vector. It also supplies runtime_error which is pretty ideal for our needs because it holds a string that can be used by an error handler. So, we can write our simple error() like this:

```c++
void error(string s)
{
throw runtime_error{s};
}
```

When we want to deal with runtime_error we simply catch it. For simple programs, catching runtime_error in `main()` is ideal:

```c++
int main()
try {
// .. our program
return 0; // 0 indicates success
}
catch (runtime_error& e){
	cerr << "runtime error: " << e.what() << '\n';
	return 1; // 1 indicates failure
}
catch (...){
	cerr << "Oops: unknown exception!\n"; 
	return 2; // 2 indicates failure
//We added catch(...) to handle exceptions of any type whatsoever.
}

```

The call `e.what()` extracts the error message from the runtime_error. The `&` in `catch(runtime_error& e) ` is an indicator that we want to ‘‘pass the exception by reference.’’ For now, please treat this as simply an irrelevant technicality.
____
>The third reason is the serious one. It is easy (once you are an experienced programmer) to find examples where checking a precondition would take significantly more work than executing the function. An example is a lookup in a dictionary: a precondition is that the dictionary entries are sorted – and verifying that a dictionary is sorted can be far more expensive than a lookup. Sometimes, it can also be difficult to express a precondition in code and to be sure that you expressed it correctly. "

- **write a quick check of the preconditions** for the code that you are writing 

ex:
```c++
int my_complicated_function (int a, int b,int c)
// the arguments are positive and a < b < c
{
expect( [&]{return 0<a && a<b && b<c;}, "bad arguments for mcf")'
	//... | ^ lambda expression
}
```

and write a **postcondition check** as well
### 4.7.3.3 Postconditions

Precondition only, assuming that computation is correct: 
```C++
int area(int length, int width) 
// calculate area of a rectangle 
// the arguments are positive 
{ 
expect([&]{ return 0 < length && 0 < width;}, "bad arguements to area()");
}
```

Postcondition as well, checking if result is positive:
```c++
int area(int length, int width) 
// the arguments are positive 
{ 
	expect([&]{ return 0 < length && 0 < width;}, "bad arguements to area()")
	int a = length*width;	  

	expect([&]{return 0<a;}, "bad area() result")
	return a;
}
```

### 4.7.4 Testing 
- executing a program w/ large selected set of inputs and comparing results to what was expected/
	- *test case* = a run with a given set of inputs
- *testing framework* - allow to write a set of code examples and for each to say what is the expected result
	-  `Boost.Test, Catch2, CTest, Google Test, Microsoft Unit Testing Framework for C++, and UnitTest++.`

### 4.7.5 Random Numbers
- we can use randomness to be used when testing our code

generating random ints
```c++
int random_int(int min,int max); // get an int from the range [min:max]
int random_int(int max); // get an int from the range [0:max]

// we can now say
for (int i=0; i<10; ++i) cout << random_int(1,6) << ' '; 
// get a value from the distribution using the engine
```

generating random strings, all lowercase
```C++
string random_letters(int n, int m) // generate a string with between 4 and 24 random lower-case characters 
{ 
string s(random_int(n, m),'x'); // a string with a size in the [n:m] range
for (char& ch : s) 
	ch = narrow(random_int('a','z')); // a lower-case letter 
	return s; 

}
```

pg. 123 has a really good exercise to work with and get used to reading errors and fixing bugs



### 5.2.1 stages of development
- **Analysis**
	- figure out what should be done and write a description of your (current) understanding of that.
- **Design**
	- create an overall structure for the system
	- consider which tools - such as libraries - can help you structures the program
- **implementation**
	- write the code, debug it, and test that is does what its supposed to do

### 5.2.2 Strategy 
1. What is the problem to be solved?
2. Try breaking the program into manageable parts? 
3. build a small, limited version of the program that solves a key part of the problem
4. build a full-scale solution, ideally by using parts of the initial version.
	- the ideal is to grow a program from working parts rather than writing all the code at once

## 5.3.2 Tokens
- **token** - a sequence of characters that represents something we consider a unit, such as a number or an operator.
	- *pg 122*
 
- given: 1 + 2 x 3 | what result should it be?
	- mathematically, it is 7, but written in code it reads as: (1+2) x 3
		- somehow we have to "look ahead" to see if there is a `*` or `/` and change the evaluation order?
- Problems:
1. we don't actually need for an expression to be on one line, for example:
	`1`
	`+`
	`2`
2. How do we remember where a `*` was? 
3. How do we search for `*` or `/` among all other symbols and on several input lines?
4. How do we handle evaluation that's not strictly left-to-right?

we can 'tokenize'
- the input characters are read and assembled into tokens, so if you type in:
	-  45+11.5/7 
		- the program should produce a list of tokens representing 
		- 45 
		+ + 
		+ 11.5
		+ /
		+ 7

### 5.3.3 Implementing Token 

```C++
	class Token  // simple user defined type
	{ 
	public:
		char kind;
		double value;
	
	}
```

-  `token` is a type like `int` or `char` so it can be defined variables and hold values
- 
- 