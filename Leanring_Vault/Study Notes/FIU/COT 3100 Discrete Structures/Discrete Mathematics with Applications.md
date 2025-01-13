## Speaking Mathematically

### 1.1 Variables
- placeholder for something
- $2x+3=x^2$

#### Some important kinds of Mathematical Statements
**Universal Statement**
- says that a certain property is true for all elements in a set. 
	- All positive numbers are greater than zero.
**Conditional Statement**
- says that if one thing is true then some other thing also has to be true. 
	- If 378 is divisible by 18, then 378 is divisible by 6.
**existential statement**
- Given a property that may or may not be true, an *existential statement* says that there is at least one thing for which the property is true
	- there is a prime number that is even

**Universal Conditional Statements**
- "for every" + "if then"
- both universal and conditional
	- for every animal *a*, if *a* is a dog, then *a* is a mammal

can be rewritten in ways to make them appear purely universal or conditional:
- *conditional*
	- if *a* is a dog, then *a* is a mammal
	- if an animal is a dog, then the animal is mammal
- *universal*
	- for every dog *a*, *a* is a mammal
	- all dogs are mammals
**Universal Existential Statement**
- statement that is *universal* because its first part says that a certain property is true for all objects of a given type, and it is *existential* because its second part asserts the existence of something
	- every real number has an additive inverse

**Existential Universal Statements**
- statement that is existential because its first part asserts that a certain object exists and is universal because its second part says that the object satisfies a certain property for all things of a certain kind. 
	- there is a positive integer that is less than or equal to every positive integer

### 1.2 The language of sets 
- **axiom of extension** 
	- a set is completely determined by what its elements are - not order or repetition of elements

- What are the elements of A B C, and how are they related?
	1. $A = \{1,2,3\}$, $B = \{3,1,2\}$, $C=\{1,1,2,3,3\}$ 
	2. they contain the same elements, and are simply different ways to represent the same set

- how many elements are in the set $\{1,\{1\}\}$?
	1. the set $\{1,\{1\}\}$ has **2** elements: 1 and a set whose only element is 1.

- is $\{0\} = 0$?
	1.  No, bc $\{0\}$ is a set with one element, whereas $0$ is just symbol representing $0$

- for each non-negative integer *n*, let $U_n = \{n,-n\}$. Find $U_1,U_2,U_0$
	1. $U_1 = \{1,-1\}$ 
	2. $U_2 = \{2,-2\}$
	3. $U_0 = \{0,-0\} = 0$

#### Set Builder Notation
- Let $S$ denote a set and let $P(x)$ be a property that elements of S may or may not satisfy. We may define a new set to be the set of all elements $x$ in $S$ such that $P(x)$ is true. We denote this set as follows:
	- $\{x \in S|P(x)\}$
	- the set of all | such that

##### Subsets
- imagine $A$ and $B$ are sets
- if, and only if, every element of $A$ is also an element of $B$ 
- then $A$ is called a *subset* of $B$
	- $A \subseteq B$ means that for every element $x$, if $x \in A$ then $x \in B$  
		- $A$ is *contained* in $B$ 
		- $B$ *contains* $A$
**Proper Subset**
- Let $A$ and $B$ be sets. 
- $A$ is a **proper subset** of $B$ if, and only if, every element of $A$ is in $B$ **but** there is at least one element of $B$ that is not in $A$

**Practice**
$A = \mathbb{Z}^+$
$B = \{n\in \mathbb{Z}| 0 \leq n \leq 100\}$
$C = \{100,200,300,400,500\}$

Evaluate each condition, true or false
-  $B\subseteq A$
	- False. Zero is not a positive integer. Thus zero is not in $A$, so $B \nsubseteq A$
- $C$ is a proper subset of $A$
	- True. Each element in $C$ is positive integer and hence, is in $A$.
- $C$ and $B$ have at least one element in common
	- True, 100 is in both
- $C \subseteq B$
	- False, 200 is in $C$ but not in $B$
- $C \subseteq C$
	- True, for element in $C$ is in $C$ 
		- the definition of a subset implies that all sets are subsets of themselves

#### Distinction between *In* and *proper subset*

Which of the following are true?
1. $2 \in \{1,2,3\}$
	1. True
2. $\{2\} \in \{1,2,3\}$
	1. False. 
	2. The set $\{1,2,3\}$ would have to contain the element $\{2\}$. 
	3. $2 \neq \{2\}$
3. $2 \subseteq \{1,2,3\}$
	1. False.
	2. the number 2 would have to be a *set* and every element in the *set* 2 would have to be an element of $\{1,2,3\}$
4. $\{2\} \subseteq \{1,2,3\}$
	1. True
5. $\{2\} \subseteq \{\{1\},\{2\}\}$
	1. False
	2. Every element in the set containing only the number 2 ($\{2\}$) would have to be an element of the set whose elements are $\{1\}$ and $\{2\}$ 
	3. but 2 is not equal to either $\{1\}$ or  $\{2\}$
6. $\{2\} \in \{\{1\},\{2\}\}$
	1. True

### Cartesian Products

$$ \{\{a\},\{a,b\}\}$$
this set has elements $\{a\}$ and $\{a,b\}$. If $a \neq b$, then the two sets are distinct and $a$ is in both sets whereas $b$ is not.
- side note, if $a=b$, then the set would simplify to $\{\{a\},\{a,a\}\} = \{\{a\}\}$

That set is simplified to:
$$(a,b)$$
two ordered pairs are equal if and only if:

$(a,b) = (c,d)| a=c \text{ and } b=d$

**Practice**
1. Is $(1,2) = (2,1)$?
	1. No, bc $1\neq2$ , and $2\neq1$
2. Is $(3,\frac{5}{10}) = (\sqrt{9},\frac{1}{2})$?
	1. Yes, bc $3=\sqrt{9}$ and $\frac{5}{10} = \frac{1}{2}$
3. What is the first element of $(1,1)$?
	1. It is 1, which is also the second element

#### Ordered n-tuples
let $n$ be a positive integer and let $(x_1,x_2,...x_n)$ be elements.
**ordered n-tuple** = $(x_1,x_2,...x_n)$

two ordered tuples are **equal** if, and only if:
$(x_1,x_2,...x_n) = (y_1,y_2,...y_n) \iff x_1=y_1,x_2=y_2,...x_n=y_n$

*back to Cartesian products*

given $A_1,A_2,...A_n$ the Cartesian product is $A_1\times A_2\times...A_n$

**Examples**
Let 
$A = \{x,y\}$
$B = \{1,2,3\}$
$C = \{a,b\}$

1. find $A\times B$
	1. $\{(x, 1), (y, 1), (x, 2), (y, 2), (x, 3), (y, 3)\}$
2. find $B \times A$
	1. $\{(1, x), (1, y), (2, x), (2, y), (3, x), (3, y)\}$
3. find $A \times A$
	1. $\{(x, x), (x, y), (y, x), (y, y)\}$
4. how many elements are in 1-3?
	1. Has 6 elements 
	2. Has 6 elements
	3. Has 4 elements
5. find $(A \times B) \times C$
	1.  = $\{u,v\}|u \in A \times B \text{ and } v \in C\}$ *definition of Cartesian Product*
	2. = $\{((x, 1), a), ((x, 2), a), ((x, 3), a), ((y, 1), a), ((y, 2), a), ((y, 3), a), ((x, 1), b), ((x, 2), b), ((x, 3), b), ((y, 1), b), ((y, 2), b), ((y, 3), b)\}$
6. find $A \times B \times C$
	1. similar to the previous, yet different
	2.  $= \{(u,v,w)|u \in A, v \in B \text{ and } w \in C\}$
	3. $= \{(x, 1, a), (x, 2, a), (x, 3, a), (y, 1, a), (y, 2, a), (y, 3, a), (x, 1, b), (x, 2, b), (x, 3, b), (y, 1, b), (y, 2, b), (y, 3, b)\}$

### 1.3 The Language of Relations and Functions
- many different ways to consider relations
	- set *A* may be subset of set *B*
	- *A* may have one element in common with *B*

- x can by related to y if:
		- x < y
		- x is a factor of y 
		- $x^2 + y^2 = 1$

Let $A = \{0,1,2\}$ and $B = \{1,2,3\}$
- lets say an element x in A is related to an element y in B, if and only if, x is less than y.
- lets use x *R* y as shorthand for sentence "x is related to y"
 Then 0 R 1 since 0 < 1, 
 0 R 2 since 0 < 2, 
 0 R 3 since 0 < 3,
  1 R 2 since 1 < 2,
   1 R 3 since 1 < 3, and 
   2 R 3 since 2 < 3

##### A relation as a subset
recall the Cartesian Product of $A \times B$
- $A \times B = \{(x,y)| x \in A, y \in B\}$

so in this case:
$\{(0, 1), (0, 2), (0, 3), (1, 1), (1, 2), (1, 3), (2, 1), (2, 2), (2, 3)\}$
The elements of some ordered pairs in $A \times B$ are related, whereas the elements of other ordered pairs are not. Consider the set of all ordered pairs in $A \times B$ whose elements are related:

$\{(0, 1), (0, 2), (0, 3), (1, 2), (1, 3), (2, 3)\}$


#### Definition of a relation
Let $A$ and $B$ be sets. A relation **R*** from ***A to B***
is a subset of $A \times B$.
given in the ordered pair $(x,y)$ in $A \times B$, x is related to y by ***R***, written x ***R*** y if and only if $(x,y)$ is in ***R***.
- the set $A$ is called the *domain* of ***R*** and the set of $B$ is called its *co-domain*:

$x \textbf{ R } y$ means that $(x,y) \in \textbf{R}$

and x *~~R~~* y means that x is not related to y by *R* 

**example**
let $A = \{1,2\}$ and $B = \{1,2,3\}$ and define the relation **R*** from $A \text{ to }B$ as follows: 
- given any $(x,y) \in A \times B$:
	- $(x,y) \in R$ means that $\frac{x-y}{2}$ is an integer 

1. state explicitly which ordered pairs are in $A \times B$ and which are in *R*
	$A \times B = \{(1, 1), (1, 2), (1, 3), (2, 1), (2, 2), (2, 3)\}$
	- going through each pair and seeing if it satisfies *R*
		- $R = \{(1,1),(1,3),(2,2)\}$
1. Is 1 *R* 3? 2 *R* 3? 2 *R* 2?
	1. Yes, 1 *R* 3 bc $(1,3) \in R$
	1. No , 2 ~~*R*~~ 3 bc $(1,3) \notin R$
	1. Yes, 2 *R* 2 bc $(2,2) \in R$
1. what are the domain and co-domain of *R*?
	1. domain of *R* is $\{1,2\}$ and co-domain is $\{1,2,3\}$
		1. *refer back to definition of Relation*


**The circle Relation**
define a relation $C$ from ***R*** to ***R*** as follows: for any $(x,y) \in \textbf{R}\times\textbf{R}$,
- $(x,y) \in C \text{ means that } x^2 + y^2 = 1$

1. is $(1,0) \in C$?
	1. yes, bc $1^2 + 0^2 = 1$
2. is $(0,0) \in C$?
	1. no, bc yes, bc $0^2 + 0^2 \neq 1$
3. is $(-\frac{1}{2},\frac{\sqrt{3}}{2}) \in C$?
	1. yes, bc =1
4. is $-2  C 0$? 
	1. No, $-2$ ~~C~~ 0 bc, $(-2)^2 + 0^2 = 4 \neq 1$
5. is $0 C (-1)$
	1. Yes, bc $0^2 + (-1)^2 = 1$ 
6. is $1C1$
	1. No, bc $1^2 + 1^2 = 2 \neq 1$

8. what are the domain and co-domain of $C$?
	- the domain and co-domain of $C$ are both ***R***, the set of all real numbers

### Functions 
A function ***F*** from a set $A$ to a set $B$ is a relation with domain $A$ and co-domain $B$ that satisfies two properties:

1. for every element $x$ in $A$, there is an element $y$ in $B$ such that $(x,y) \in F$
	- *every element of $A$ is the first element of an ordered pair of F*
1. for all elements $x$ in $A$ and $y$ and $z$ in $B$,
	1. if $(x,y)\in F$ and $(x,z)\in F$, then $y=z$
	- *no two distinct ordered pairs in F have the same first element*

**Function Notation**
 If $A$ and $B$ are sets and $F$ is a function from $A$ to $B$, then given any element $x$ in $A$, the unique element in $B$ that is related to $x$ by $F$ is denoted $F(x)$, which is read "F of x.”

##### Functions and relations on Finite Sets
- Let $A = \{2,4,6\}$ and $B = \{1,3,5\}$. Which of the relations $R,S,T$ defined below are functions from $A$ to $B$?
	1. $R = \{(2,5),(4,1),(4,3),(6,5)\}$
		1. $R$ is not a function because of the second property. $(4,1) \text{ and } (4,3)$ have the same first element but different second elements.
	2. $S$ = for every $(x,y) \in A \times B, (x,y) \in S$ means that $y=x+1$ 
		1. $S$ is not a function bc it doesn't satisfy the first property. It It is not true that every element of $A$ is the first element of an ordered pair in $S$. For example, $6  \in A$ but there is no $y$ in $B$ such that $y = 6+1=7$. You can also see this graphically by drawing the arrow diagram for S.
		2. ![[Pasted image 20250112114720.png]]
	
	3. $T$ is defined by the arrow diagram 
		![[Pasted image 20250112114247.png]]
		- $T$ is a function: Each element  in $\{2,4,6\}$ is related to some element in $\{1,3,5\}$ and no elements in $\{2,4,6\}$ is related to more than one element in $\{1,3,5\}$ 
		- $T(2)=5,T(4)=1, T(6)=1$ 

##### Functions Defined by Formulas
(page 21)

- a function is an entity in its own right. It can be thought of as certain relationship btwn sets.
- A relation is a subset of a Cartesian Product and a function is a special kind of relation.
	- Specifically, if $f \text{ and } g$ are functions from set $A$ to set $B$ then:
		- $f = \{(x,y)\in A\times B | y =  f(x)\}$ and 
		- $g = \{(x,y)\in A\times B | y =  g(x)\}$ 
	- it follows that: 
		- $f = g$ if and only if, $f(x)=g(x)$ for all $x$ in $A$

**Equality of Functions**
- $f(x) = |x|$ for every $x\in \textbf{R}$
-  $g(x) = \sqrt{x^2}$ for every $x\in \textbf{R}$
	- does $f=g$?
	- Yes, bc $|x| = \sqrt{x^2}$


### 1.4 The Language of Graphs
