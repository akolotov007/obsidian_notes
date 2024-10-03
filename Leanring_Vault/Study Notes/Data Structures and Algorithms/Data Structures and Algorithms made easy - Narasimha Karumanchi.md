
## 1.2 Data Types
- data types that are defined by system are called *primitive data types*
	- int, float, char, string, bool, etc.
#### User Defined Data Types
- structures in C++ and classes in Java are an example
- 
## 1.3 Data structures
1. **Linear data structure** 
	- elements are accessed in a sequential order but it isn't compulsory to store all elements sequentially
		- linked lists, stack and queues
1. **non linear data structure**  
	-  elements are stored/accessed in a non-linear order
		- trees and graphs

## 1.4 Abstract Data Types (ADTs)
- primitive data types (int, float, etc.) support basic operations (+,-, etc.)
- User-defined data types also need defined operations

- ADTs combine the data structure with their operations - consists of 2 parts
	1. Declaration of Data
	2. Declaration of Operations
- commonly used ADTs include:
	- Linked List
	- Stack
	- Queue
	- Priority Queue
	- Binary Tree
	- Dictionary
	- Disjoint Sets (Union and Find)
	- Hash Tables
	- Graphs 
	- etc.


## 1.5 What is an Algorithm?
- step-by-step unambiguous instructions to solve a given problem
	- 2 criteria's for judging an algorithm:
		- Correctness (dose the algo give solution to the problem in a finite number of steps)
		- Efficiency (how much resources does it take to execute the algo)
## 1.7 Goal of Analysis of Algorithms
- to compare algorithms mainly in terms of running time but also in terms of other factors (e.g., memory, developer effort, etc.)
## 1.8 What is Running Time Analysis? 
- determining how processing time increases as the size of the problem (input size) increases.
	- input can be of different types, common ones:
		- size of an array
		- polynomial degree
		- number of elements in a matrix
		- number of bits in a binary representation of input 
		- vertices and edges in a graph

## 1.9 How to Compare Algorithms
- Bad Measures
	- Execution times?
	- Number of statements executed?
- **Ideal Solution**?
	- expressing the running time of a given algorithm as a function of the input size *n* | ie. *f(n)*
	- and compare these different functions corresponding to running times

## 1.10 What is the Rate of Growth?
- the rate at which the running time increases as a function of input

## 1.11 Commonly Used Rates of Growth 

![[Pasted image 20240925134612.png]]



| Time Complexitity | Name               | Example                                               |
| ----------------- | ------------------ | ----------------------------------------------------- |
| 1                 | constant           | adding an element to the front of a linked list       |
| log n             | logarithmic        | finding an element in a sorted array                  |
| n                 | linear             | finding an element in a unsorted array                |
| n log n           | logarithmic linear | sorting *n* items by 'divide-and-conquer' - mergesort |
| n^2               | quadratic          | shortest path btwn 2 nodes in a graph                 |
| n^3               | cubic              | matrix manipulation                                   |
| 2^n               | exponential        | the Towers of Hanoi problem                           |
## 1.12 Types of Analysis
- to analyze, we need to know which inputs the algorithm takes less time and which inputs take more time 
- #### 3 types of analysis
	- ##### Worst Case
		- define the input for which the algorithm takes the longest time
		- input is the one for which the algorithm runs the **slowest** 
	- ##### Best Case
		- define the input for which the algorithm takes the least time
		- input is the one for which the algorithm runs the **fastest**
	- ##### Average Case
		- provides a prediction about the running time of the algorithm
		- runs the algorithm many times, using many diff inputs (pg. 26)

- `Lower bound <= Average Time <= Upper Bound`

## 1.13 Asymptotic Notation
- to represent the upper and lower bounds, need some kind of syntax...

## 1.14 Big-O Notation (Upper Bound Function) 
- gives the *tight* upper bound of a given function.
- Generally represented as: $$ f(n)=O(g(n))$$
- that means, at the larger values of *n*, the upper bound of f(n) is g(n)
- for example:
	-$$f f(n) = n^4 + 100n^2 + 10n + 50$$ 
		- n^4 =  *g(n)* 
- that means that *g(n)* gives the max rate of growth for for *f(n)* at larger values of *n*

![[Pasted image 20240925140437.png]]

-  O(g(n)) = {f(n): there exist positive constants` c` and `n0` such that 0 ≤ f(n) ≤ cg(n) for all n > n0}.
- Generally we discard the lower values of *n*. 
	- lower values of *n* are not important
- In this example, anything less than `n0` we don't consider
	- called the **threshold** for the given function
### Big-O visualization
- O(g(n)) is the set of functions with smaller or the same order of growth as g(n). 
- For example; O(n^2) includes: O(1), O(n), O(nlogn), etc.
- ![[Pasted image 20240925141026.png]]

### Big-O examples
- Example1:Find upper bound for 
	- f(n) = 3n + 8 
		- Solution: 3n + 8 ≤ 4n, for all n ≥ 8 
		- ∴ 3n + 8 = O(n) with c = 4 and n0 = 8
- 