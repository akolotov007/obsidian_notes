## Chapter 1: Speaking Mathematically

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
**Existential statement**
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
- we can use graphs to visualize relations 
![[Pasted image 20250113185048.png]]

- a dot is called a *vertex* - plural is vertices
- a line is called an *edge* 
![[Pasted image 20250113185302.png]]
two vertices that are connected by an edge are called *adjacent*

- an edge that connects a vertex is called a *loop*
	- a vertex is said to be *adjacent to itself*
- when two edges connect the same pair of vertices, they are *parallel*
- when a vertex is unconnected to anything, it is *isolated*

you can represent the relation between edges and endpoints in a table:
*for example*:
![[Pasted image 20250113190639.png]]

##### How different graphs can represent the same thing
![[Pasted image 20250113192027.png]]
![[Pasted image 20250113192038.png]]


#### Using a Graph to Represent a Network
- a typical network is called a *hub and spoke model*
![[Pasted image 20250113193023.png]]

A **directed graph** is (digraph) consists of two finite sets $V(G)$ of vertices and a set $D(G)$ of directed edges, where each is associated with an ordered pair of vertices called its **endpoints**. If edge $e$ is associated with the pair $(v,w)$ of vertices, then $e$ is said to be the **(directed) edge** from $v \text{ to }w$

#### Using Graphs to Represent Knowledge
![[Pasted image 20250114081226.png]]

for example:
- from the knowledge that the *Los Angeles Times* is a big-city daily and that big-city daily contains national news, AI could infer that *LA times* contains national news.

Definition:
Let $G$ be a graph and $v$ a vertex of $G$. The **degree of $V$** denoted $deg(v)$, equals of edges that are incident on $v$, with an edge that is a loop counted twice.

Example:
Find the degree of each vertex of the graph $G$:
![[Pasted image 20250114081953.png]]

- solution:
	- $deg(v1) = 0$, since no edge is incident on $v_1$
	- $deg(v2) = 2$ 
	- $deg(v3) = 4$
		- since $e_1$ and $e_2$ are incident on $v_3$ and the loop $e_3$ is also incident on $v_3$ (and contributes 2 degrees of $v_3$)


## Chapter 2: The Logic of Compound Statements

### 2.1 Logical Form and Logical Equivalence
- An argument is a sequence of statements aimed at demonstrating the truth of an assertion. 
	- the assertion at the end of the sequence =  **conclusion**
	- the preceding statements  = **premises**

- A **proposition** is a logical statement and an expression that is either true or false, but not both 

In logic, the *form* of the argument is distinguished from it *content*.
- logical analysis helps analyze the arguments form to figure out whether the truth of the conclusion follows **necessarily** from the truth of the premises.

Example:
$p$ = the bell rings
$q$ = the flag drops
$r$ = the race is over

If the bell rings or the flag drops, then the race is over.
$\therefore$  (therefore) If the race is not over, then the bell hasn't rung and the flag hasn't dropped.

The common form of the argument is:
- If $p$ or $q$, then $r$.
- $\therefore$ If not $r$, then not $p$ and not $q$

#### Statements
- a (proposition) is a sentence that is true or false but not both

#### Compound Statement 
- *~* | $\neg$ = not
- $\land$ = and 
- $\lor$ = or

$p \land q$ = P and Q
$p \lor q$ = P or Q
$\neg p$ = not P

#### Logical Operators

| Name                  | Logical Operation | Symbolic                     | Representation                      | Comments                   |
| --------------------- | ----------------- | ---------------------------- | ----------------------------------- | -------------------------- |
| Negation              | NOT               | $\neg$, ~                    | ~$p$, $\neg p$                      | not P                      |
| Conjunction           | AND               | $\land$                      | $p \land q$                         | P and Q                    |
| Disjunction           | OR                | $\lor$                       | $p \lor q$                          | P or Q                     |
| Exclusive Disjunction | XOR               | $\oplus$                     | $p \oplus q$                        | P xor Q                    |
| Conditional           | IF THEN           | $\rightarrow$ , $\leftarrow$ | $p \rightarrow q$, $p \leftarrow q$ | if P then Q \| If Q then P |
##### Logical Operators in Programming

| ~       | !     |
| ------- | ----- |
| $\land$ | $$    |
| $\lor$  | \| \| |

##### Order of Operations
- $\neg$ comes first
	- $\neg p \land q = (\neg p) \land q$
	- $\neg (p \land q)$ = negation of the conjunction of $p$ and $q$ 
- $\land,\lor,\oplus$ second
- $\rightarrow,\leftarrow, \iff$, last


A variety of English words translate into logical symbols.
- *but* = *and*
	- generally, the word *but* is used in place of *and* when a part of the sentence that follows is unexpected.
	- "Jim is tall but he not heavy"
	- $p$ but $q$ = $p$ and $q$ 
- *Neither-nor* = *not*
	- neither $p$ nor $q$ =  $\neg p \text{ and } \neg q$

#### and, or, and inequalities
1. $x \leq 3$
	1. $q \lor r$
2. $0<x<3$
	1. $p \land q$
3. $0<x\leq 3$
	1. $p \land (q \lor r)$

#### Truth Values
- we built compound sentences of components statements and the terms **not, and, or**. 
	- have to have defined truth value - either true or false.

| $p$ | $\neg{p}$ |
| --- | --------- |
| T   | F         |
| F   | T         |
*we use truth tables to organize and show all possible combinations of different truth values*

Example:
P and Q = ***conjunction***

| $P$ | $Q$ | $P \land Q$ |
| --- | --- | ----------- |
| T   | T   | T           |
| T   | F   | F           |
| F   | T   | F           |
| F   | F   | F           |

Example:
P or Q = ***disjunction***

| $P$ | $Q$ | $P \lor Q$ |
| --- | --- | ---------- |
| T   | T   | T          |
| T   | F   | T          |
| F   | T   | T          |
| F   | F   | F          |
#### Evaluating the Truth of More General Compound Statements
A **statement form** (or propositional form) is an expression made of statement variables ($p,q,r$) and logical connectives ($\neg,\land,\lor$) that becomes a statement when actual statements are substituted for the component statement variables. 


Two *statement forms* are **logically equivalent** if and only if, they have identical truth values for each possible substitution of statements for their statement variables. 
- The logical equivalence of the statement forms *P* and *Q* is denoted as:
	- $P \equiv Q$

**Double Negative Property:** $\neg (\neg p) \equiv p$  
construct a truth table: 

| $p$ | $\neg p$ | $\neg(\neg p)$ |
| --- | -------- | -------------- |
| T   | F        | T              |
| F   | T        | F              |
- notice how $p$ and $\neg(\neg p)$ always have the same truth values, so they are logically equivalent

**Showing Nonequivalence**

| $p$ | $q$ | $\neg p$ | $\neg q$ | $p \land q$ | $\neg (P \land Q)$ |         | $\neg p \land \neg q$ |
| --- | --- | -------- | -------- | ----------- | ------------------ | ------- | --------------------- |
| T   | T   | F        | F        | T           | F                  |         | F                     |
| T   | F   | F        | T        | F           | T                  | $\not=$ | F                     |
| F   | T   | T        | F        | F           | T                  | $\not=$ | F                     |
| F   | F   | T        | T        | F           | T                  |         | T                     |
#### De Morgan's Law
- the negation of an *and* statement is logically equivalent to the *or* statement in which each component is negated.
	- $\neg (p\land q) \equiv \neg p \lor \neg q$
- the negation of an *or* statement is logically equivalent to the *and* statement in which each component is negated.
	- $\neg (p\lor q) \equiv \neg p \land \neg q$

#### Tautologies and Contradictions

**Tautology**
- a statement form that is always **true** regardless of the truth values of the individual statements substituted for its statement variables.

| $p$ | $q$ | $p \lor \neg p$ |
| --- | --- | --------------- |
| T   | F   | T               |
| F   | T   | T               |

- $p \lor \neg p$  contains all true, therefore tautological  

**Contradiction**
- a statement form that is always **false** regardless of the truth values of the individual statements substituted for its statement variables.


| $p$ | $q$ | $p \land \neg p$ |
| --- | --- | ---------------- |
| T   | F   | F                |
| F   | T   | F                |
- $p \land \neg p$ contains all false, therefore contradictory 

#### Logical Equivalence Involving Tautologies and Contradictions
- if **t** is a tautology and **c** is a contradiction, show that $p \land \textbf{t} \equiv p$ and $p \land \textbf{c}\equiv \textbf(c)$


| $p$ | $t$ | $p \land \textbf{t}$ | $p$ | $c$ | $p \land \textbf{c}$ |
| --- | --- | -------------------- | --- | --- | -------------------- |
| T   | T   | T                    | T   | F   | F                    |
| F   | T   | F                    | F   | F   | F                    |

#### Logical Equivalences
![[Pasted image 20250120135924.png]]

- It can be shown that the first 5 proofs form the core from which the other laws can be derived.
	- the first 5 laws are axioms for a Boolean Algebra



### 2.2 Conditional Statements
- When you make a logical inference or deduction, you reason from a hypothesis to a conclusion. 
	- “If such and such is known, then something or other must be the case"

A sentence of the form "'If $p$ then $q$"
- $p \rightarrow q \equiv \neg p \lor q$ 
- $p$ hypothesis 
- $q$ conclusion
- conditional bc truth of the statement $q$ is conditioned on the truth statement $p$.

- $p$ is a **sufficient** condition of $q$
- $q$ is a **necessary** condition of $p$

| $p$ | $q$ | $p \rightarrow q$ |
| --- | --- | ----------------- |
| T   | T   | T                 |
| T   | F   | F                 |
| F   | T   | T                 |
| F   | F   | T                 |
- $p$ necessarily implies $q$ , meaning that if $q$ is false then $p$ cannot hold true


**Converse of** $p \rightarrow q$
- $q \rightarrow p$

**Inverse of** $p \rightarrow q$
- $\neg p \rightarrow \neg q$

**Contrapositive of** $p \rightarrow q$
- $\neg q \rightarrow \neg p$
	- The conditional statement is logically equivalent to the contrapositive statement


#### Facts about conditional Statements

**Fact 1**: Contrapositives is a reciprocal relation  
- $p \rightarrow q$  contrapositive to $\neg q \rightarrow \neg p$

**Fact 2**: The contrapositive of a *converse* is *inverse*
$q \rightarrow p$ contrapositive to $\neg p \rightarrow \neg q$
converse $\equiv$ inverse

**Fact 3**: $p \rightarrow q \equiv \neg q \rightarrow \neg p$
- proof 1:

| $p$ | $q$ | $\neg p$ | $\neg q$ | $\neg p \lor q$ | $q \lor \neg p$ |
| --- | --- | -------- | -------- | --------------- | --------------- |
| T   | T   | F        | F        | T               | T               |
| T   | F   | F        | T        | F               | F               |
| F   | T   | T        | F        | T               | T               |
| F   | F   | T        | T        | T               | T               |
- proof 2:
	- If today is Easter, then tomorrow is Monday $\equiv$ If tomorrow is not Monday, then today is not Easter


##### Only If and Biconditional 
$p$ if $q$ $\equiv$ if $q$ then $p$ $\equiv$ $q \rightarrow p$

$p$ only if $q$ $\equiv$ $p$ can take place only if $q$ takes places
- meaning that - q doesn't take place, then $p$ cannot take place
- $\equiv \neg q \rightarrow \neg p$
- $\equiv p \rightarrow q$

$p$ if and only if $q$ $\equiv$ $(p \rightarrow q) \land (q \rightarrow p) \equiv p \iff q$
- $p$ is a sufficient condition for $q$ means " if $p$ then $q$"   $p \rightarrow q$
- $p$ is a necessary condition for $q$ means "if  $\neg p$ then $\neg q$"   $\neg p \rightarrow \neg q$
**Clarification**:
- if 2=3, then FIU is a private University | **T**
	- *in logic we focus on the form of the argument as compared to our daily life and how we make connections*


### 2.3 Valid and Invalid Arguments
In this section we show how to determine whether an argument is valid—that is, whether the conclusion follows necessarily from the preceding statements. We will show that this determination depends only on the **form** of an argument, ***not*** on its **content**.

An **argument** is a sequence of statements and a **argument form** is a sequence of statement forms. 
premises (assumptions / hypothesis) 
conclusion
**argument form** is *valid* means that no matter what  statements are substituted for the statement variables in its premises, if the resulting premises are all true, then the conclusion is also true.
**argument** is valid if its **form** is valid 


Example of a Valid Argument:

> If Socrates is a man, then Socrates is mortal
> Socrates is a man
> $\therefore$ Socrates is mortal

> If $p$ then $q$
> $p$
> $\therefore q$


#### Modus Ponens and Modus Tollens

**Syllogism** - and argument form containing 2 premises and a conclusion
- major and minor premise

##### Modus Ponens
- method of affirming 


> If $p$ then $q$
> $p$
> $\therefore q$


|     |     | premises          | premises |     |                |
| --- | --- | ----------------- | -------- | --- | -------------- |
| $p$ | $q$ | $p \rightarrow q$ | $p$      | $q$ |                |
| T   | T   | T                 | T        | T   | *critical row* |
| T   | F   | F                 | T        |     |                |
| F   | T   | T                 | F        |     |                |
| F   | F   | T                 | F        |     |                |
- The first row is the only which **both** premises are true, and the conclusion in that row is also true.
	- hence the argument form is valid

##### Modus Tollens
- method of denying 

> if $p$ then $q$
> $\neg q$
> $\therefore \neg p$

Example:
> if Zeus is human, then Zeus is mortal
> Zeus is not mortal
> $\therefore$ Zeus is not human

The validity of *modus tollens* can be shown to follow from *modus ponens* together with the fact that a conditional statement is **logically equivalent to its contrapositive**. Or it can be established formally by using a truth table.


##### Additional Valid Argument Forms: Rule of Inference
- **rules of inference** is a form of argument that is valid 
- Thus **modus ponens** and **modus tollens** are both rules of inference.

###### Generalization

> $p$
> $\therefore p \lor q$

> $q$
> $\therefore p \lor q$
- If $p$ is true, then more generally $p \lor q$ is true for ***any*** other statement $q$.

> Anton is a junior
> $\therefore$ (more generally) Anton is a junior or Anton is a senior 


###### Specialization

> $p \land q$
> $\therefore p$

> $p \land q$
> $\therefore q$

- brings

###### Elimination

> $p \lor q$
> $\neg q$
> $\therefore p$

> $p \lor q$
> $\neg p$
> $\therefore q$

###### Transitivity

> $p \rightarrow q$
> $q \rightarrow r$
> $\therefore p \rightarrow r$

###### Proof by Division into Cases
> $p \lor q$
> $p \rightarrow r$
> $q\rightarrow r$
> $\therefore r$

It often happens that you know one thing or another is true. If you can show that in either case a certain conclusion follows, then this conclusion must also be true.


##### Fallacies
- **Fallacy** - an error in reasoning that results in an invalid argument.
	- **ambiguous premises** - and treating them as if the were unambiguous 
	- **circular reasoning** - (assuming what is to be proved without having derived it from the premises) 
	- **jumping to a conclusion** - (without adequate grounds)

- **converse error** and **inverse** **error**, which give rise to arguments that superficially resembles modus ponens and modus tollens

##### Converse Error
> $p \rightarrow q$
> $q$
> $\therefore p$

> If Zeke is a cheater, then Zeke sits in the back row
> Zeke sits in the back row
> $\therefore$ Zeke is a cheater

- AKA *fallacy of affirming the consequent*

##### Inverse Error
> $p \rightarrow q$
> $\neg p$
> $\therefore \neg q$

> If these two vertices are adjacent, then they do not have the same color
> These two vertices are not adjacent
> $\therefore$ These two vertices have the same color


##### A valid Argument with a False Premise and False Conclusion 
- the argument below is valid by modus ponens, but its major premise is false, and so is its conclusion

> If Canada is north of the United States, then temperatures in Canada never rise above freezing
> Canada is north of the United States
> $\therefore$ Temperatures in Canada never rise above freezing
##### An Invalid Argument with a True Premise and True Conclusion
- The argument below is invalid by the converse error, but it has a true conclusion

> If New York is a big city, then New York has tall buildings
> New York has tall buildings
> $\therefore$ New York is a big city

An argument is called ***sound*** if, and only if, it is **valid** *and* all its **premises** are true.
- An argument that is not sound is called ***unsound***.


#### Contradictions and Valid Arguments

##### Contradiction Rule

> $\neg p \rightarrow c$, where $c$ is a contradiction 
> $\therefore p$


| p   | $\neg p$ | $c$ | $\neg p \rightarrow c$ | $p$          |
| --- | -------- | --- | ---------------------- | ------------ |
| T   | F        | F   | T                      | T            |
| F   | T        | F   | F                      |              |
|     |          |     | *premises*             | *conclusion* |
The contradiction rule is the logical heart of the method of proof by contradiction. A slight variation also provides the basis for solving many logical puzzles by eliminating contradictory answers: *If an assumption leads to a contradiction, then that assumption must be false.*

##### Knights and Knaves
- The logician Raymond Smullyan describes an island containing two types of people: knights who always tell the truth and knaves who always lie. You visit the island and are approached by two natives who speak to you as follows:
	-  *A* says : *B* is a knight
	- *B* says : *A* and I are of opposite type
what are A and B?

**Solution**
Suppose A is a knight
$\therefore$ What A says is true  - *definition of a knight*
$\therefore$ B is a also a knight - *what A said*
$\therefore$  What B says is true - *definition of a knight*
$\therefore$ A and B are of opposite types - *What B said*
$\therefore$ We have arrived at contradiction: A and B are both knights and A and B are of opposite type
$\therefore$ The Supposition is false - *by the contradiction rule*
$\therefore$ A is not a knight - *negation of supposition*
$\therefore$ A is a knave - *by elimination: It is given that all inhabitants are knights or knaves. Since A is not a knight, A is a knave*
$\therefore$ What A says is false
$\therefore$ B is not a knight
$\therefore$ B is also a knave - *by elimination*

#### Summary of Rules of Inference
![[Pasted image 20250123143851.png]]

*make into table*

### 2.4 Digital Logic Circuits
![[Pasted image 20250123144419.png]]

![[Pasted image 20250123144428.png]]

![[Pasted image 20250123162140.png]]

#### Black Boxes and Gates
- the inside of a black box contains the detailed implementation of the circuit and is often ***ignored*** while attention is focused on the relation between the **input** and the **output** signals.
![[Pasted image 20250123172518.png]]


![[Pasted image 20250123172625.png]]

![[Pasted image 20250123172711.png]]

#### Finding a Boolean Expression for a Circuit
![[Pasted image 20250129104350.png]]


**Recognizer** - a circuit that outputs 1 for exactly one particular combination of input signals and output 0 for all other combinations

![[Pasted image 20250129104507.png]]


#### Designing a Circuit for a given input/output table
![[Pasted image 20250129104545.png]]

 For each row that has a result of 1, construct an and expression that produces a 1 (or true) for the exact combination of input values for that row and a 0 (or false) for all other combinations of input values.
 - row 1: $P \land Q \land R$
 - row 3: $P \land \neg Q \land R$ 
 - row 4: $P \land \neg Q \land \neg R$ 

If follows that the Boolean expression for the given truth table is: 
- $(P \land Q \land R) \lor (P \land \neg Q \land R) \lor (P \land \neg Q \land \neg R)$

![[Pasted image 20250129105204.png]]


#### Showing that two circuits are logically equivalent 
![[Pasted image 20250129105517.png]]

Both circuits have the same truth table,
- so the two circuits are **logically equivalent** iff their input/output tables are identical

#### NAND and NOR gates
- NAND - negation of AND
	- AND followed by a NOT
- NOR - negation or OR
	- OR followed by a NOT

##### NAND
- |  = logical symbol for NAND
- $P | Q = \neg(P\land Q)$ 

##### NOR
- $\downarrow$ = logical symbol for NOR
-  $P \downarrow Q = \neg(P \lor Q)$


Notice the dot at the end of AND NOR
![[Pasted image 20250129110043.png]]



## Chapter 3: The Logic of Quantified Statements

### 3.1 Predicates and Quantified Statements
- **Predicate** -  is a sentence that contains a finite number of variables and becomes a statement when specific values are substituted for the variables
	- The **domain** of a predicate variable is the set of all values that may be substituted in place of the variable.

If $P(x)$ is a predicate and $x$ has a domain $D$ the **truth set** of $P(x)$ is the set of all elements in $D$ that make $P(x)$ true when they are substituted for $x$. The truth set of $P(x)$ is:
- $\{x\in D | P(x)\}$

#### The Universal Quantifier 

One sure way to change predicates into statements is to assign specific values to all their variables.
Another way to change predicates into statements is to add **quantifiers**.
 - quantifiers - words such as "some" or "all"

- $\forall$ - the universal quantifier
	- read as :“for every”   “for each”   “for any”   “given any”  or  “for all"

Example
- “Every human being is mortal” or “All human beings are mortal"
	- $\forall$ beings x, x is mortal
		- read as: for every human being x, x is mortal.

Let $H$ be the set of all human beings, then you can more formally write it as:
$\forall x \in H, x$ is mortal


Let $Q(x)$ be a predicate and $D$ the domain of $x$. A **universal statement** is a statement of the form $\forall x \in D, Q(x)$
- It is defined to be **true** if, and only if, $Q(x)$ is *true* for each individual $x$ in $D$. 
- It is defined to be **false** if, and only if, $Q(x)$ is *false* for at least one $x$ in $D$. 
	- A value for $x$ for which $Q(x)$ is false is called a ***counterexample*** to the universal statement.


#### Truthy and Falsity of Universal Statements
1. Let $D = \{1,2,3,4,5\}$, and consider the statement:
	- $\forall x \in D, x^2 \geq x$
		- $1^2 \geq 1, 2^2 \geq 2,3^2 \geq 3, 4^2 \geq 4, 5^2 \geq 5$

2. Consider the statement: 
	- $\forall x \in R, x^2 \geq x$
		- *counterexample:* if x = $\frac{1}{2}$, then:
		- $\frac{1}{2}^2 = \frac{1}{4} \not\geq \frac{1}{2}$
	- Hence this statement is false

This technique used to show the truth of the universal statement is called the **method of exhaustion**


#### The Existential Quantifier
- $\exists$ = "there exists"  = Existential Quantifier

Example: 
- "There is a student in Math 140" can be written as: 
	- $\exists$  a person $p$ such that $p$ is a student in Math 140
- or more formally:
	- $\exists p \in P$ such that $p$  is a student in Math 140

#### Truth and Falsity of Existential Statements
1.  Consider the statement
	- $\exists m \in Z^+$ such that $m^2 = m$
	- There is at least 1 positive int, which is 1 = 1$^2$
	- therefore, true
1. Let $E = \{5,6,7,8\}$ and consider the statement:
	-  $\exists m \in Z^+$ such that $m^2 = m$
	- false

#### Translating from Formal to Informal Language

1. $\forall x \in R, x^2 \geq 0$
	- every real number has a nonnegative square
	- *or* all real numbers have nonnegative squares.
	- *or* Any real number has a nonnegative square
	- *or*: The square of each real number is nonnegative.

2. $\forall x \in R, x^2 \not= -1$
	- no real numbers have squares that do not equal -1
1. $\exists m \in Z^+$ such that $m^2 =m$
	- There is a positive integer whose square is equal to itself.
	- *or* We can find at least one positive integer equal to its own square.
	- *or* Some positive integer equals its own square


#### Universal Conditional Statements
$\forall x, \text{ if } P(x) \text{ then } Q(x)$

examples:
1. If a real number is an integer, then it is a rational number. 
	- $\forall$ real numbers *x*, if *x* is an int, then *x* is a rational number
	- $\forall x \in R, \text{ if } x\in Z, \text{ then } x\in Q$
1. All bytes have eight bits.
	- $\forall x$, if *x* is a byte, then *x* has 8 digits
2. No fire trucks are green.
	- $\forall x$, if *x* is firetruck, then *x* is not green

#### Equivalent Forms of Universal and Existential Statements

$\forall x \in U, \text{ if } P(x) \text{ then } Q(x)$
can be rewritten in the form:
	$\forall x \in D, Q(x)$

#### Bounds and Scope
- *same as in programming*

$x$ is **bound** by the quantifier that controls it and the its **scope** begins when the quantifier introduces it and ends at the end of the quantified statement


#### Implicit Quantification
- Consider the statement: If a number is an integer, then it is a rational number.
![[Pasted image 20250129131428.png]]
![[Pasted image 20250129131525.png]]

### 3.2 Predicates and Quantified Statements II
#### Negations of Quantified Statements
- Consider the statement
	- “All mathematicians wear glasses.” 
- Many people would say that its negation is:
	- “No mathematicians wear glasses,” 
	- incorrect, bc if there is at least one that wears glasses, *all* would be false
- So a correct negation is 
	- “There is at least one mathematician who does not wear glasses.”

#### Negation of a Universal Statement
![[Pasted image 20250129131921.png]]

**The negation of a universal statement (“all are”) is logically equivalent to an existential statement (“some are not” or “there is at least one that is not”)**

#### Negation of a Existential Statement
![[Pasted image 20250129132023.png]]
 **The negation of an existential statement (“some are”) is logically equivalent to a universal statement (“none are” or “all are not”)**

#### Practice:

Negating Quantified Statements:
- $\forall$ primes *p*, *p* is odd
	- applying rule of negation of a $\forall$:
	- $\exists$ a prime number *p* such that *p* is not odd
- $\exists$ a triangle *T* such that the sum of the angles of *T* equals 200 degrees.
	- applying rule of negation of a $\exists$:
	- $\forall$ triangles *T*, the sum of angles of *T* does not equal 200 degrees

rewrite the statements formally, then write the formal and informal negations 
1. No politicians are honest
	- *formal version*: $\forall$ politicians *p*, *p* is not honest
	- *formal negation*: $\exists$ a politician *p*, such that *p* is honest
	- *informal negation*: some politicians are honest

#### Negations of Universal Conditional Statements

$\neg(\forall x,P(x) \rightarrow Q(x)) \equiv \exists x \text{ such that } \neg(P(x) \rightarrow Q(x))$
- the negation of an if-then statement is logically equivalent to an *and* statement.
	- $\neg(P(x) \rightarrow Q(x)) \equiv P(x) \land \neg Q(x)$
		- substituting that into the equation, and written less formally gives us:
- $\neg(\forall x, \text{ if }P(x) \text{ then } Q(x)) \equiv \exists x \text{ such that } (P(x) \text{ and } \neg Q(x)$


#### The Relation among for all, exists, and & or
- Just as $\land$ and $\lor$ are negations of each other, so are $\forall$ and $\exists$
	- In a sense, universal statements are generalizations of ***and*** statements
	- and existential statements are generalizations of ***or*** statements

#### Vacuous Truth of Universal Statements
- **P**: All humans living on Mars do not know how to count
	- is P true or false?
*in order to find out if that statement is true or false, we look at its negation*
- $\neg P$ : $\exists$ a human living on Mars who knows to count
	- False

therefore, P is *Vacuous True* 


#### Variants of Universal Conditional Statements 
![[Pasted image 20250129141231.png]]
![[Pasted image 20250129141356.png]]

#### Necessary and Sufficient Conditions, Only If
![[Pasted image 20250129141604.png]]

**Example**
Rewrite each of the following as a universal conditional statement, quantified either explicitly or implicitly. Do not use the word necessary or sufficient

- Squareness is a sufficient condition for rectangularity.
	- *formal version*: $\forall x,$ if *x* is a square, then *x* is a rectangle
	- *w/ implicit universal quantification*: if a figure is a square, then it is a rectangle

- Being at least 35 years old is a necessary condition for being president of the United States.
	- *formal* : $\forall$ person *x*, if *x* is younger than 35, then *x* cannot be president of the US
	- *equal in statement but contrapositive* : $\forall$ person *x*, if *x* is president of the United States, then *x* is at least 35 years old.

### 3.3 Statements with Multiple Quantifiers

"There is a person supervising every detail of the production process.”
- contains *there is* (existential) & *every* (universal quantifier)

***When a statement contains more than one kind of quantifier, we imagine the actions suggested by the quantifiers as being performed in the order in which the quantifiers occur***

$\forall x \in D, \exists y, \in E$ such that *x* and *y* satisfy property $P(x,y)$

Example:
- "Every integer has a larger integer"
- $\forall \in Z, P(x)$ 
- expanded: $\forall \in Z, \exists y \in Z, y>x$
- True: choose y = x+1 $\in Z$

- find negation:
	- $\exists x \in Z, \forall y \in Z, y \leq x$
- and this statement doesn't make sense, therefore **False.**

Since the negation is false, the original statement is true

#### Order of Quantifiers 
 In a statement containing both $\forall$ and $\exists$ changing the order of the quantifiers significantly change the meaning of the statement. Therefore, their order matters

 If a statement has the same quantifiers, then the order doesn't matter
$\forall$ real number *x* and $\forall$ real number y, $x+y = y+x$
*is the same as*
$\forall$ real number **y** and $\forall$ real number **x**, $x+y = y+x$
*and can be a little less formal as:*
$\forall$ real numbers *x* and y, $x+y = y+x$

#### Formal Logic Notation 

$\forall x \text{ in } D, P(x)$ can be written as $\forall x (x \text{ in }D \rightarrow P(x))$
$\exists x \text{ in  D such that } P(x)$ can be written as $\exists x (x \text{ in }D \land P(x))$


### 3.4 Arguments with Quantified Statements
**Universal Instantiation** - If a property is true of *everything* in a set, then it is true of *any particular* thing in the set.
- A given theorem says that such and such is true for all things of a certain type. 
- If, in a given situation, you have a particular object of that type, then by universal instantiation, you conclude that such and such is true for that particular object.
#### Universal Modus Ponens
*formally*: 
- $\forall x, \text{ if }P(x) \text{ then } Q(x)$
- $P(a)$ for a particular $a$
- $\therefore Q(a)$

*Informally*:
- If *x* makes P(x) true, then *x* makes Q(x) true
- *a* makes P(x) true
- $\therefore$ *a* makes Q(x) true

#### Universal Modus Tollens

*formally*
- $\forall x \text{ if } P(x) \text{ then } Q(x)$
- $\neg Q(a),$ for a particular *a*
- $\therefore \neg P(a)$

*Informally*
- If *x* makes P(x) true, then *x* makes Q(x) true
- *a* does not make Q(x) true
- $\therefore$ *a* does not make P(x) true
#### Converse Error (Quantified Form)
*formally*
- $\forall x, \text{ if } P(x) \text{ then } Q(x)$
- $Q(a)$ for a particular $a$
- $\therefore P(a)$ | ***invalid conclusion*** 

*Informal Version*
- If *x* makes P(x) true, then *x* makes Q(x) true
- *a* makes Q(x)
- $\therefore$ a makes P(x) true | ***invalid conclusion***


#### Inverse Error (Quantified Form)

*formally*
- $\forall x, \text{ if } P(x) \text{ then } Q(x)$
- $\neg P(a)$ for a particular $a$
- $\neg Q(a)$ | ***invalid conclusion*** 

- If *x* makes P(x) true, then *x* makes Q(x) true
- *a* does not make P(x)
- $\therefore$ a does not make Q(x) true | ***invalid conclusion***

#### Proving Validity of Arguments with Quantified Statements
- To say that an argument form is **valid** means the following: 
- No matter what particular predicates are substituted for the predicate symbols in its premises, if the resulting premise statements are all true, then the conclusion is also true. 
- An *argument* is called **valid** *if, and only if,* its form is valid. 
- It is called **sound** if, and only if, its form is **valid** and its premises are **true**.

#### Universal Transitivity

Looking back at transitivity:
$p \rightarrow q$
$q \rightarrow r$
$\therefore p \rightarrow r$

![[Pasted image 20250129170109.png]]


## Chapter 4: Elementary Number Theory and Methods of Proofs
dhttps://www.youtube.com/watch?v=HIkIqt_ytdc

### 4.1 Direct Proof and Counterexample I : Introduction

**Assumptions**
- assuming familiarity with the laws of basic algebra.
- A,B,C | A=A, if A=B then B=A, if A=B B=C A=C
- law of substitution, if A=B then substitute B for any A
- assume there is not integer between 0 and 1 and that the set of all ints is closed under: addition, subtraction, and multiplication. (no division)

#### Even, Odd, Prime and Composite Integers

Definition: 
- An integer *n* is **even** iff, *n* equals twice some integer. 
	- $n$ is even $\iff$ $n=2k$ for some integer $k$
- *n* is **odd** iff *n* equals twice some integer plus 1
	- $n$ is odd $\iff$ $n=2k+1$ for some integer *k*

#### Even and Odd integers
Example:
- is 0 even?
	- yes, 0 x 2 = 0
- is -301 odd?
	- Yes, -301 = 2(-151)+1 and -151 is an int
- if *a* and *b* are integers, is 6a$^2$b even?
	- yes, =2(3a$^2$b) and 3a$^2$b is an integer since it is a product of ints 
- if *a* and *b* are integers, is 10*a* + 8*b* + 1 odd?
	- Yes, bc = 2(5*a*+4*b*)+1 and 5*a*+4*b* is an integer since it's sum of products of ints 
- Is every integer either even or odd?
		-  Yes, every integer is either even or odd. However, the reason for this fact is not immediately apparent. It can be deduced using the method of proof by contradiction, which is introduced in Section 4.7

**Prime**
- A int *n* is **prime** iff, n>1 and for all positive ints *r* and *s*, if $n=rs$ then either *r* or *s* equals *n*.
	- $n$ is prime $\iff$ $\forall$ positive ints $r$ and $s$, if $n=rs$ then either $r=1$, and $s=n$ or $r=n$ and $s=1$

**Composite**
- A int *n* is **composite** iff, n>1 and for some ints *r* and *s* with $1<r<n$ and $1<s<n$
	-  $n$ is composite $\iff$ $\exists$ positive ints $r$ and $s $ such that $n=rs$, and $1<r<n$ and $1<s<n$ 

Examples:
- is 1 prime?
	- No, a prime is greater than 1 
- is every integer greater than 1 prime or composite?
	- Yes. Let $n$ be any integer that is greater than 1. Consider all pairs of positive integers $r$ and $s$ such that $n = rs$. There exist at least two such pairs, namely, $r=n$and $s=1$ and $r=1$ and $s=n$. 
	- Moreover, since $n = rs$, all such pairs satisfy the inequalities $1\leq r \leq n$ and $1\leq s \leq n$.
	- If n is prime, then these two pairs are the only ways to write $n$ as $rs$. 
	- Otherwise, there exists a pair of positive integers $r$ and $s$ such that $n = rs$ and neither $r$ nor $s$ equals either$ 1$ or $n$. 
	- Therefore, in this case $1<r<n$ and $1<s<n$ and hence n is composite.
- write the first six prime numbers
	- 2,3,5,7,11,13
- write the first six composite numbers
	- 4,6,8,9,10,12

#### Proving Existential Statements
*From Section 3.1*
$\exists x \in D$ such that $Q(x)$ is true $\iff$ $Q(x)$ is true for at least one $x$ in $D$

##### Constructive Proofs of Existence
- One way to prove this is to find an $x$ in $D$ that makes $Q(x)$.
	- Another way is to give a set of directions for finding such an $x$.
- the logical principle behind proof: **existential generalization**
	- if you know  certain property is true for particular object, conclude that “there exists an object for which the property is true.”

**Example**
- Prove $\exists$ an even integer $n$ that can be written in two ways as a sum of two prime numbers.
	- Let n=10.
	- Then 10 = 5+5 = 3+7 and 3,5,7 are all prime. 
	- Thus $\exists$ an even integer - 10 - than can be written in two ways as a sum of 2 prime numbers.

- Suppose that $r$ and $s$ are integers. Prove: $\exists$ an integer $k$ such that $22r + 18s=2k$
	- Let $k$  = $11r+9s$.
	- Then $k$ is an integer bc its a sum of products and by substitution, and the distributive law of algebra:
	- $2k = (11r+9s) = 22r+18s$

##### Non-Constructive Proofs of Existence
- Involves showing either:
	- **A**. that an existence of a value of $x$ that makes $Q(x$) true is guaranteed by an axiom or a previously proved theorem or
	- **B**. that the assumption that there is no such $x$ leads to a contradiction.

#### Disproving Universal Statements by Counterexample
- Given a statement, find out if its negation (its opposite) is true.

 $\forall x$ in $D$ if $P(x)$ then $Q(x)$
- showing that this statement is false by finding out if negation is true:
$\exists x$ in $D$ such that $P(x)$ and not $Q(x)$
- *counterexample*

##### Disproof by Counterexample
Disprove the following statement by finding a counterexample:
- $\forall$ real numbers $a$ and $b$, if $a^2=b^2$ then $a=b$

To disprove this statement, find real numbers $a$ and $b$ such that hypothesis $a^2=b^2$ is true *and* the conclusion $a=b$ is false
The fact that positive and negative integers have positive squares...

**Counterexample**: 
- let $a=1$ and $b=-1$
- $a^2=1=1^2=1$ and $b^2 = (-1)^2=1$
- so $a^2=b^2$ but $a\not=b$ since $1\not=-1$


#### Proving Universal Statements
The vast majority of mathematical statements to be proved are universal. 
 $\forall x \in D$,if $P(x)$ then $Q(x)$

>The most powerful technique for proving a universal statement is one that works regardless of the size of the domain over which the statement is quantified. 
>It is based on a logical principle sometimes called *universal generalization*. aka *generalizing from the generic particular.*

##### Generalizing from the Generic Particular
- To show that *every* element of a set satisfies a certain property, suppose $x$ is a *particular* but *arbitrarily chosen* element of the set, and show that *x* satisfies the property

Example (Math trick):
- Ask person to pick any number
- Add 5
- multiply by 4
- subtract 6
- divide by 2
- subtract twice the original number
- = 7

- [ ] = contains whatever number the person picked. The table shows by the end of the calculations, the box was substracted out of the answer 
![[Pasted image 20250206122516.png]]

$x$ in this case is *particular* (because it is a single object) but also *arbitrarily chosen/generic* (because any number can be put in its place)

![[Pasted image 20250206124557.png]]

##### A direct proof a Theorem
Prove that the sum of any two *even* integers is even
 
 To prove the statement in general, show that no matter what even integers are given, their sum is even. 
 But given two *even* ints, can be written as:
- $2r$ and $2s$ for some integers $r$ and $s$
- By distributive law of Algebra:
	- $2r+2s=2(r+s)$
Formal Statement:
- $\forall$ integers $m$ and $n$, if $m$ and $n$ are even, then $m+n$ is even 

*what am I supposing?, How should I start my proof?*
**Starting Point of proof:**
- Suppose *m* and *n* are any particular but arbitrarily chosen integers that are even.
	- abbreviated: Suppose $m$ and $n$ are any even integers.

*what conclusion do I need to show in order to complete the proof?*
**To Show: *m* + *n* is even** 

At this point you need to ask yourself, “How do I get from the starting point to the conclusion?” Since both involve the term even integer, you must use the definition of this term—and thus you must know what it means for an integer to be even. It follows from the definition that since m and n are even, each equals twice some integer. 
One of the basic laws of logic, called ***existential instantiation***: 

**Existential Instantiation
- If the existence of a certain kind of object is assumed or has been deduced, then it can be given a name, as long as that name is not currently being used to refer to something else in the same discussion.

(skipping over the jumbo):

![[Pasted image 20250206125821.png]]


#### Getting Proofs Started
Once you understand the idea of generalizing from the generic particular and the method of direct proof, you can write the beginnings of proofs even for theorems you do not understand.

**Identifying the “Starting Point” and the “Conclusion to Be Shown"**
Example:
- Every complete bipartite graph is connected
formal restatement:
- For every graph G, if G is a complete bipartite, then G is connected
-               (domain)       (hypothesis)                        (conclusion)


### 4.2 Direct Proof and Counterexample II: Writing Advice

#### Directions for Writing Proofs of Universal Statements
###### 1. Copy the statement of the theorem to be proved on your paper
- This makes the theorem statement available for reference to anyone reading the proof.
###### 2. Clearly mark the beginning of your proof with the word Proof
- This word separates general discussion about the theorem from its actual proof.
###### 3. Make your proof self-contained
- Introduce and explain the meaning of each variable used in your proof, in the body of the proof.
	- "Suppose *m* and *n* are any even integers" or "Let *x* be a real number such that *x* is greater than 2"
###### 4. Write your proof in complete, grammatically correct sentences
- This does not mean that you should avoid using symbols and shorthand abbreviations, just that you should incorporate them into sentences.
	- then $m+n = 2r+2s$ | by substitution
	-                    = $2(r+s)$ | by factoring out 2
- To read such text as a sentence, read the first equals sign as “equals” and each subsequent equals sign as “which equals.”
###### 5.Keep your reader informed about the status of each statement in your proof
- Keep your reader informed about the status of each statement in your proof. Your reader should never be in doubt about whether something in your proof has been assumed or established or is still to be deduced. If something is assumed, preface it with a word like Suppose or Assume.
###### 6. Give a reason for each assertion in your proof
- Each assertion in a proof should come directly from the hypothesis of the theorem, 
- or follow from the definition of one of the terms in the theorem, 
- or be a result obtained earlier in the proof, 
- or be a mathematical result that has previously been established or is agreed to be assumed. 
- Indicate the reason for each step of your proof using phrases such as by hypothesis, by definition of Á by theorem Á and so forth. 
- It is best to refer to definitions and theorems by name or number
###### 7.Include the “little words and phrases” that make the logic of your arguments clear
- When writing a mathematical argument, especially a proof, indicate how each sentence is related to the previous one. 
- Does it follow from the previous sentence or from a combination of the previous sentence and earlier ones? 
	- If so, start the sentence with the word Because or Since and state the reason why it follows, or write *Then*, or *Thus*, or *So*, or *Hence*, or *Therefore*, or *Consequently*, or *It follows that*, and include the reason at the end of the sentence.
###### 8. Display equations and inequalities
- The convention is to display equations and inequalities on separate lines to increase readability, both for other people and for ourselves so that we can more easily check our work for accuracy. 


#### Variations among Proofs
- It is rare that two proofs of a given statement, written by 2 diff people are identical. 
	- Different notation or giving different amounts of explanation for their steps, etc.

#### Common Mistakes When Writing Proofs
###### 1. Arguing from examples

###### 2.Using the same letter to mean two different things.
- Some beginning theorem provers give a new variable quantity the same letter name as a previously introduced variable. Consider the following “proof” fragment:
	- Suppose $m$ and $n$ are any odd integers. Then by definition of odd, $m=2k+1$ and $n=2k+1$ where $k$ is an integer.
###### 3. Jumping to a conclusion 
- To jump to a conclusion means to allege the truth of something without giving an adequate reason. Consider the following “proof” that the sum of any two even integers is even.
###### 4. Assuming what is to be proved
To assume what is to be proved is a variation of jumping to a conclusion. As an example, consider the following “proof” of the fact that the product of any two odd integers is odd:

###### 5. Confusion between what is known and what is still to be shown.
- A more subtle way to jump to a conclusion occurs when the conclusion is restated using a variable.

###### 6. Use of *any* when the correct word is *some*.

###### 7. Misuse of the word *if*
- another common error is not serious in itself, but it reflects imprecise thinking that sometimes leads to problems later in a proof. This error involves using the word if when the word because is really meant. Consider the following proof fragment:
	- Suppose *p* is a prime number. 
	- If *p* is prime, then *p* cannot be written as a product of two smaller positive integers.
		- The use of the word *if* in the second sentence is inappropriate. It suggests that the primeness of p is in doubt. But p is known to be prime by the first sentence. It can't be written as a product of two smaller positive integers because it is prime. Here is a correct version of the fragment:
	- *Because* p is prime, p cannot be written as a product of two smaller positive integers.



![[Pasted image 20250208125130.png]]

![[Pasted image 20250208125250.png]]



#### Showing That an Existential Statement is False
- Recall that the negation of an existential statement is universal. It follows that to prove an existential statement is false, you must prove a universal statement (its negation) is true.
![[Pasted image 20250208125745.png]]



### 4.3 Direct Proof and Counterexample III: Rational Numbers
- A real number $r$ is **rational** if, and only if, it can be expressed as a quotient of two integers with a nonzero denominator. 
	- A real number that is not rational is **irrational**. 
	- More formally, if $r$ is a real number, then:
		- $r$ is rational $\iff \exists$ integers $a$ and $b$ such that $r=\frac{a}{b}$ and $b\not=0$

**Zero Product Property**
- if neither of two real numbers is zero, then their product is also not zero

every integer is a rational number

#### Proving Properties of Rational Numbers

![[Pasted image 20250208130507.png]]


#### Deriving New Mathematics from Old
##### Deriving Additional Results about Even and Odd Integers
Suppose that you have already proved the following properties of even and odd integers: 
1. The sum, product, and difference of any two even integers are even. 
2. The sum and difference of any two odd integers are even. 
3. The product of any two odd integers is odd. 
4. The product of any even integer and any odd integer is even. 
5. The sum of any odd integer and any even integer is odd.
6. The difference of any odd integer minus any even integer is odd. 
7. The difference of any even integer minus any odd integer is odd.
Use the properties listed above to prove that *a* is any even integer and *b* is any odd integer, then
$$\frac{a^2 +b^2 +1}{2} \text{ : is an integer}$$
Solution:
-  Suppose $a$ is any even integer and $b$ is any odd integer.
- By property 3, $b^2$ is odd
- By property 1, $a^2$ is even
- Then property 5 $a^2 + b^2$ is odd, and also bc 1 is odd...
- the sum $(a^2+b^2) + 1 = a^2+b^2 + 1$ is even, property 2
- Hence, by definition of even, there exists an integer $k$ such that $a^2+b^2 + 1 =2k$
- Divide both sides by 2 gives $\frac{a^2 +b^2 +1}{2} = k$ which is an integer
- thus $\frac{a^2 +b^2 +1}{2}$ is an integer

**Corollary** =  a statement whose truth can be immediately deduced from a theorem that has already been proved.

The double of a rational number is rational 
- The double of a number is just its sum with itself. 
- But since the sum of any two rational numbers is rational (Theorem 4.3.2), the sum of a rational number with itself is rational. 
- Hence the double of a rational number is rational. 
- Here is a formal version of this argument:
	- Suppose $r$ is any rational number. Then  $2r=r+r$ is a sum of two rational numbers. So, by Theorem 4.3.2, $2r$ is rational. 

### 4.4 Direct Proof and Counterexample IV: Divisibility

![[Pasted image 20250208131706.png]]


![[Pasted image 20250208131757.png]]


![[Pasted image 20250208134324.png]]


![[Pasted image 20250208134409.png]]


![[Pasted image 20250208135814.png]]

#### Greatest Common Divisor and Least Common Multiple

##### GCD (Greatest Common Divisor)
$x = \frac{12}{36} = \frac{p}{q}, p=12, q=36$
What integers divide 12 & 36 without remainders?
$2|12, 3|12, 6|12, 12|12$ |  read as : $n$ divides 12
$2|36, 3|36, 6|36, 12|36$ |   read as : $n$ divides 36

the largest integer (from the list) that divides both 12 and 36 is : 12
$\therefore$ GCD is 12
can be written as $GCD(12,36) = 12$

**Relative Prime**
$GCD(2,3) = 1$
- there are no integers that can divide both 2 and 3 except 1. 
- $p$ and $q$ are *relative prime*

$d = gcd(a,q) = 1$ unless $a$ is a multiple of *p*

##### Least Common Multiple (LCM) 
$LCM(a,b)$ is the smallest integer that is divisible by both $a$ and $b$

$LCM(5,10) = 10$
$LCM(2,3) = 6$
$LCM(24,36) = 72$


#### The Euclidean Algorithm
- https://www.youtube.com/watch?v=JUzYl1TYMcU
- used to find the GCD of two numbers 

$gcd(a,b) = gcd(a, a\mod b)$
- this process is repeated until $b=0$ and at that point the GCD is $a$
Step by step:
$a = bq_1 + r_1$
$b = r_1q_2 + r_2$
$r_1 = r_2q_3 + r_3$
$\cdots$ 
until $r_n = 0$

or in code:
```python
x = a \\ assuming a >= b
y = b
while (y> 0)
	r = x mod y
	x = y
	y = r
return x
```


#### The Unique Factorization of Integers Theorem 
*aka fundamental theorem of arithmetic*
- says that any integer greater than 1 either is prime or can be written as a product of prime numbers in a way that is unique except for the order in which the primes are written. For example:
	- $72 = 2\times2\times2\times3\times3 = 2\times3\times3\times2\times2 = 3\times2\times2\times3\times2$

![[Pasted image 20250208141702.png]]

Because of the unique factorization theorem, any integer $n>1$ can be put into a *standard factored form* in which the prime factors are written in ascending order from left to right:

![[Pasted image 20250208141722.png]]

##### Writing Integers in Standard Factored Form
- write 3,300 in standard factored form 
	- find all factors of 3,300 an write them in ascending order:
	- = 10 * 33 = 4 * 25 * 3 * 11
	- = 2 * 2 * 5 * 5 * 3 * 11 = $2^2 \times 3^1 \times 5^2 \times 11^1$ 

### 4.5 Direct Proof and Counterexample V: Division into Cases and the Quotient-Remainder Theorem

The quotient-remainder theorem says that when any integer $n$ is divided by any positive integer $d$, the result is a quotient $q$ and a nonnegative integer remainder $r$ that is smaller than $d$.

![[Pasted image 20250208142325.png]]


![[Pasted image 20250208143035.png]]
- *number (n)* / *divisor (d)*  = *quotient (q)* + *remainder (r)*

$q=a \text{ div } d$
$r=a \text{ mod } d$


#### Div and Mod
![[Pasted image 20250208143856.png]]


a $\equiv$ b (mod 7)
a and b have the same remainder when you divide them by 7 
#### Key Explanation 
- compute 32 *div* 9 
- compute 32 *mod* 9 
![[Pasted image 20250208144005.png]]

Written as:
- 32 mod 9 = 5
	- can be re-written as 32 $\equiv$ 5 (mod 9)
- meaning that when 32 is divided by 9 the remainder is 5. 

32 $/$ 9 = 3.555 | the quotient (as an integer, no rounding) is 3 (bc 9 x 3 = 27, and 32 is just a little bit more than 27)
now subtract 27 from 32:
32-27 = 5
this means that divide 32 by 9, you get a quotient of 3 and a remainder of 5. Therefore, 32 mod 9 = 5

https://www.youtube.com/watch?v=5_tvw_3l-RI
![[Pasted image 20250305135254.png]]
#### Examples
![[Pasted image 20250208144827.png]]




### 4.6 Direct Proof and Counterexample VI: Floor and Ceiling

*IMPORTANT* : Note the subtle differences of the box around $X$
- Bottom of box is drawn, *floor*
	- $\lfloor x \rfloor$ 
- Top of box it drawn, *ceiling*
	- $\lceil x \rceil$

#### Simple Explanation
- If x = 1, then floor and ceiling are the same, (=1)
- if x = 0.5, floor is 0, ceiling is 1
- if x = -1.5, floor is -2, ceiling is -1

- floor = round down
- ceiling = round up


##### Floor of X
![[Pasted image 20250208153440.png]]

##### Ceiling of X

![[Pasted image 20250208153523.png]]

##### Computing Floors and Ceilings
![[Pasted image 20250208153958.png]]


![[Pasted image 20250208154156.png]]



### 4.7 Indirect argument: Contradiction and Contraposition
![[Pasted image 20250208154956.png]]

##### Examples
![[Pasted image 20250208155051.png]]


#### Argument by Contraposition

![[Pasted image 20250208155311.png]]

![[Pasted image 20250208155433.png]]



### 4.8 Indirect Argument: Two Famous Theorems

##### The Irrationality of $\sqrt{2}$
![[Pasted image 20250208155847.png]]

### 4.9 Application: The Handshake Theorem
- The total degree of a graph is the sum of the degrees of all the vertices of the graph
![[Pasted image 20250208160358.png]]

#### The Handshake Theorem 
- the sum of all degrees of all vertices = twice the number of edges

![[Pasted image 20250208160528.png]]



### 4.10  Application: Algorithms
**Algorithm** - step by step method for preforming some action
- for, for each, while, if-elif-else
#### A Division algorithm
![[Pasted image 20250209222900.png]]


## Chapter 5: Sequences, Mathematical Induction and Recursion

### 5.1 Sequences 

**Sequence** - a function who's domain is either all the integers between two given integers or all the integers greater than or equal to a given integer.

We typically represent a sequence as a set of elements written in a row. In the sequence denoted:
$$a_m,a_{m+1},a_{m+2}\cdots a_{n}$$
- each individual element is a **term** ($a_k$)
- : denotes an *infinite sequence*

An **explicit formula** or **general formula** for a sequence is a rule that shows how the values of $a_k$ depend on $k$.




#### Summation Notation 
If $m$ and $n$ are integers and $m \leq n$, the symbol $\displaystyle\sum_{k=m}^{n} a_k$  , read the **summation from** k = *m* to *n* of $a_k$, is the sum of all terms $a_m, + a_{m+1}, a_{m+2}\cdots , a_n$. This is called the expanded form.
- $k$ is the index of summation
- $m$ is the **lower** limit
- $n$ is the **upper** limit

##### Practice
![[Pasted image 20250209211927.png]]
##### When the terms of a Summation are Given by a Formula
![[Pasted image 20250209212712.png]]

##### Changing from Summation Notation to Expanded Form
![[Pasted image 20250209212747.png]]

##### Small Values of *n*
![[Pasted image 20250209212349.png]]

##### Double Summation Notation
If you want to find the summation of a 2D array, you would do it with a *double summation*:
- Given function $F(i,j)$ sum all possible values with $n=4$
$$\displaystyle\sum^n _{j=1}\sum^n _{i=1} f(i,j)$$
$(\text{S)olution} = f(1,1)+f(1,2)+f(1,3)+f(1,4)+f(2,1)+f(2,2)+f(2,3)+f(2,4)+f(3,1)+f(3,2)+f(3,3)+f(3,4)+f(4,1)+f(4,2)+f(4,3)+f(4,4)$


### Product Notation
$$\displaystyle\prod^5_{k=1}a_k = a_1 a_2 a_3 a_4 a_5$$

If *m* and *n* are integers and *m* $\leq$ n, the symbol reads: the product from *k* = *m* to *n* of $a_k$ is the product of all the terms $a_m \times a_{m+1} \times a_{m_2}\cdots a_n$


#### Properties of Summations and Products
![[Pasted image 20250209214230.png]]

##### Using Properties of Summations and Products
![[Pasted image 20250209214517.png]]

#### Factorial Notation and "n choose r" Notation
##### Factorial Notation
for each positive integer *n*, the quantity *n* **factorial** denoted: $n!$ is defined to be the product of all the integers from $1$ to $n$:
$n! = n \cdot (n - 1)  \cdots 3,2,1$

**Zero Factorial** is defined to be 1:
$0! = 1$


An important use for the factorial notation is in calculating values of quantities, called *n choose r*, that occur in many branches of mathematics, especially those connected with the study of counting techniques and probability.

##### N choose R
Let $n$ and $r$ be integers with $0\leq r \leq n$ then symbol:
$$\binom{n}{r} = \frac{n!}{r!(n-r)!}$$
represents the number of subsets of size $r$ that can be chosen from a set with $n$ elements.

![[Pasted image 20250209220526.png]]
###### r-combinations vs r-permutations

![[Pasted image 20250323125050.png]]

### 5.2 Mathematical Induction I : Proving Formulas
https://www.youtube.com/watch?v=GdM_iA1Zek4 | Intro To Mathematical Induction
https://www.youtube.com/watch?v=5Hn8vUE3cBQ | A visual Explanation of Mathematical Induction

![[Pasted image 20250209221049.png]]

![[Pasted image 20250209221550.png]]
>To see the connection between this image and the principle of mathematical induction, let $P(n)$ be the sentence “The $n$th domino falls backward.” It is given that for each $k \geq 1$, if $P(k)$ is true (the $k$th domino falls backward), then $P(k+1)$ is also true (the $(k + 1)$st domino falls backward). 
>It is also given that $P(1)$ is true (the first domino falls backward). Thus by the principle of mathematical induction, $P(n)$ (the nth domino falls backward) is true for every integer $n \geq 1$


#### Method of Proof by Mathematical Induction

![[Pasted image 20250209223703.png]]

![[Pasted image 20250210130954.png]]

**Example**
##### Sum of a Geometric Sequence
![[Pasted image 20250210132117.png]]
![[Pasted image 20250210132130.png]]


### 5.3 Mathematical Induction II: Applications
In *Section 5.2* we showed how to use mathematical induction to prove formulas. In this section we will show how to apply it in a broader variety of situations.

![[Pasted image 20250210134238.png]]



### 5.4 Strong Mathematical Induction and the Well-Ordering principle for the Integers

https://www.youtube.com/watch?v=rfA0h9udl7E  | video on strong math induction
- Strong mathematical induction is similar to ordinary mathematical induction in that it is a technique for establishing the truth of a sequence of statements about integers. 
	- Also, a proof by strong mathematical induction consists of a basis step and an inductive step. 
	- However, the basis step may contain proofs for **several initial values**, and in the inductive step the truth of the predicate $P(n)$ is assumed not just for one value of $n$ but for *all values through* $k$, and then the truth of $P(k + 1)$ is proved.
- Any statement that can be proved with ordinary mathematical induction can be proved with strong mathematical induction

![[Pasted image 20250211172924.png]]




## Chapter 9: Counting and Probability
### 9.1: Introduction to Probability 
**Sample Space** = the set of all possible outcomes of a random process or experiment. 
**Event** =  is a *subset* of a **sample space.**


![[Pasted image 20250206142419.png]]

- for any finite set *A*, *N(A)* denote the number of elements in *A*
	- with this notation, the formula ^ becomes:
![[Pasted image 20250206142527.png]]

Example:

![[Pasted image 20250206144240.png]]

You can count virtually anything, along with occurrences of a given thing happening 
- heads or tails on a coin flip
- rolling dice and counting how many times a given number shows up
- finding the probability of getting a set of specific cards from a card deck


### 9.2 Possibility Trees and the Multiplication Rule
A **tree structure** is a useful tool for keeping systematic track of all possibilities in situations in which events happen in order. 

Example:
![[Pasted image 20250206144525.png]]

#### The Multiplication Rule
Consider the following example. Suppose a computer installation has four input/output units *(A, B, C, and D)* and three central processing units **(X, Y, and Z)**. 
	Any input/output unit can be paired with any central processing unit. How many ways are there to pair an input/output unit with a central processing unit?

![[Pasted image 20250206144656.png]]- 
- the total number of way to pair two types of units is the same as the number of branches of the tree which is:
	- $4\times3 = 12$
	- 
![[Pasted image 20250206144800.png]]

Example:
Counting PINS
- A certain personal identification number (PIN) is required to be a sequence of any four symbols chosen from the 26 uppercase letters in the Roman alphabet and the ten digits.
	- How many different PINs are possible if repetition of symbols is allowed?
		- 36 total possibilities (26 letters + 10 digits {0-9}) | for each PIN position (4 total positions)
		- _ _ _ _ 
		- $36\times 36\times 36 \times 36 = 36^4 = 1,679,616$
	- How many different PINs are possible if repetition of symbols is ***not*** allowed? 
		- 36 possibilities in the first position, 35 in the second, 34, 33.
		- $36\times 35\times 34 \times 33 = 1,413,720$
	- What is the probability that a PIN does not have a repeated symbol assuming that all PINs are equally likely?
		- By Part B, there are 1,413,720 with no repeated symbols and from part A a total of 1,679,616.
		- $\frac{1,413,720}{1,679,616} \approx 0.8417 = 84\%$
- 


![[Pasted image 20250206170222.png]]


#### Permutations
- a set of objects is an ordering of objects in a row.
	- example:
	- *a,b,c* has six permutations
		- *abc acb cba bac bca cab*
- In general, given a set of *n* objects, how many permutations does the set have? Imagine forming a permutation as an *n*-step operation:
	- Step 1: choose an element to write first
	- Step 2: choose an element to write second
	- Step *n*: choose an element to write *n*th

$n(n-1)(n-2)\dots 2\times 1 = n!$

![[Pasted image 20250206172057.png]]


#### Permutations of Selected Elements
- given a set $\{a,b,c\}$, there are six ways to select two letters from the set and write them in order:
	- *ab ac ba bc ca cb*
- each such ordered is called a: 2-*permutation* of $\{a,b,c\}$

##### Permutations of the Letters in a word
- How many ways can the letters in the word COMPUTER be arranged if the letters CO must remain next to each other (in order) as a unit?
	- If the letter group CO is treated as a unit, then there are effectively only seven objects that are to be arranged in a row.
		- CO M P U T E R 
	- 7! = 5040 ways



**$r$-permutation
- a set of $n$ elements is an ordered selection of $r$ elements taken from the set of $n$ elements. 
- The number of $r$-permutations of a set of $n$ elements is denoted $P(n, r)$

![[Pasted image 20250206172514.png]]

![[Pasted image 20250206172637.png]]

![[Pasted image 20250206172651.png]]


#### Counting Elements of Disjoint Sets: The Addition Rule
![[Pasted image 20250206172804.png]]

![[Pasted image 20250206180407.png]]Now there are as many three-digit integers that end in 0 as there are possible choices for the left-most and middle digits (because the right-most digit must be a 0). As illustrated below, there are nine choices for the left-most digit (the digits 1 through 9) and ten choices for the middle digit (the digits 0 through 9)![[Pasted image 20250206180854.png]]

![[Pasted image 20250206181416.png]]


#### The Difference Rule
![[Pasted image 20250206180933.png]]
![[Pasted image 20250206180951.png]]

![[Pasted image 20250206181053.png]]


#### The Inclusion/Exclusion Rule
![[Pasted image 20250206181448.png]]

![[Pasted image 20250206181507.png]]

Example: Counting elements of General Union
2. How many integers from 1 through 1,000 are multiples of 3 or multiples of 5?
	- Let $A$  =  the set of all integers from 1 through 1,000 that are multiples of 3
	- Let $B$ = the set of all integers from 1 through 1,000 that are multiples of 5.
- Then $A \cup B =$ the set of all integers (^) that are multiples of 3 ***or*** 5
- and $A \cap B$  = the set of all integers (^) that are multiples of 3 ***and*** 5 
	- = the set of all integers (^) that are multiples of 15

![[Pasted image 20250206181839.png]]

3. How many integers from 1 through 1,000 are neither multiples of 3 nor multiples of 5?
	- here are 1,000 integers from 1 through 1,000, and by part (a), 467 of these are multiples of 3 or multiples of 5. Thus, by the set difference rule, there are 1,000 - 467 = 533 that are neither multiples of 3 nor multiples of 5

##### Triple Intersection Counting:
![[Pasted image 20250206182217.png]]

4. How many students did not take any of the three courses?
	1. By the difference rule, the number of students who did not take any of the three courses = the number in the class minus the number who took at least one course. 
	2. Thus the number of students who did not take any of the three courses is $50-47=3$
5. How many students took all three courses?
	- ![[Pasted image 20250206182531.png]]
6. How many students took precalculus and calculus but not Python? How many students took precalculus but neither calculus nor Python?
- ![[Pasted image 20250206182612.png]]
- For example, since nine students took both precalculus and calculus and six took all three courses, 9 2 6 5 3 students took precalculus and calculus but not Python. Similarly, since 16 students took precalculus and Python and six took all three courses, 16 2 6 5 10 students took precalculus and Python but not calculus. 

### 9.4 The Pigeon Hole Principle
- A function from one finite set to a smaller finite set cannot be one-to-one: There must be at least two elements in the domain that have the same image in the co-domain.

![[Pasted image 20250206182743.png]]
 if $n$ pigeons fly into $m$ pigeonholes and $n > m$, then at least one hole must contain two or more pigeons.

**Examples**
1. In a group of six people, must there be at least two who were born in the same month? 
	- A group of six people need not contain two who were born in the same month. For in- stance, the six people could have birthdays in each of the six months January through June.
2. In a group of thirteen people, must there be at least two who were born in the same month? Why?
- A group of 13 people, however, must contain at least two who were born in the same month, for there are only 12 months in a year and 13 >12. To get at the essence of this reasoning, think of the thirteen people as the pigeons and the twelve months of the year as the pigeonholes. 


1. A drawer contains ten black and ten white socks. You reach in and pull some out without looking at them. What is the least number of socks you must pull out to be sure to get a matched pair? 
	- If you pick just two socks, they may have different colors. But when you pick a third sock, it must be the same color as one of the socks already chosen. Hence the answer is *three*. 
		- This answer could be phrased more formally as follows: Let the socks pulled out be denoted $S_1, S_2,S_3 \cdots S_n$ and consider the function *C*  that sends each sock to its color, as shown on the next apge
	- ![[Pasted image 20250323140238.png]]

#### Generalized Pigeonhole Principle
For any function f from a finite set *X* with *n* elements to a finite set *Y* with *m* elements and for any positive integer *k*, if for each $y \in Y, f^{-1}(y)$ has at most *k* elements, then *X* has at most *km* elements; in other words, $n \leq km$

![[Pasted image 20250329125013.png]]
![[Pasted image 20250329125055.png]]


#### Theory of the Pigeon Hole Principle

![[Pasted image 20250323143242.png]]


### 9.5 Counting Subsets of a Set : Combinations
![[Pasted image 20250326001418.png]]

**Example**
- Consider a set of 4 ppl: Ann, Bob, Cyd, and Dan. 
- a. Given the set *{Ann, Bob, Cyd, and Dan}*, each subset of size 3 is a 3-combination of its elements. List all the 3-combinations of the set. 
	- {Bob, Cyd, Dan} leave out Ann 
	- {Ann, Cyd, Dan} leave out Bob 
	- {Ann, Bob, Dan} leave out Cyd 
	- {Ann, Bob, Cyd} leave out Dan
- b. Use the result of part (a) to find $\binom43$
	- here are 4 items in the list of 3-combinations in part (a). So $\binom43 =4$ 
- c. In how many ways can the people in the set form a committee of size 3
	- The number of ways for the people in the set to form a committee of size 3 is the number of distinct such committees, which is the same as the number of subsets of size 3 and equals the number of 3-combinations of elements in the set. Thus there are 4 ways the people in the set can form a committee of size 3.

2 distinct methods that can be used to select *r* objects from a set of *n* elements
**Ordered Selection** - elements are chosen but also the order in which they are chosen that matter
**Unordered Selection** -  it is only the identity of the chosen elements that matters


**Example** Unordered Selections

 How many unordered selections of two elements can be made from the set {0, 1, 2, 3}? 
 Solution:
- An unordered selection of two elements from {0, 1, 2, 3} is the same as a 2-combination, or subset of size 2, taken from the set. These can be listed systematically: 
- {0, 1}, {0, 2}, {0, 3} subsets containing 0 
- {1, 2}, {1, 3} subsets containing 1 but not already listed 
- {2, 3} subsets containing 2 but not already listed.
Since the listing exhausts all possibilities there are six subsets in all. thus $\binom42 = 6$, which is the number of unordered selections of two elements from a set of four.

**Example** Relation between Permutations and Combinations
![[Pasted image 20250329125403.png]]
![[Pasted image 20250329125424.png]]
![[Pasted image 20250329125435.png]]


![[Pasted image 20250326095927.png]]

**Example** Calculating the Number of teams
- Choosing five members (5) from a group of twelve (12) to work as a team on a special project. How many distinct five-person teams can be chosen?
$\binom{12}{5} = \frac{12!}{(12!-5!)5!} = \frac{12 \cdot 11 \cdot 10 \cdot 9 \cdot 8 \cdot 7!}{(5\cdot4\cdot3\cdot3\cdot2\cdot1)\cdot7!} = 11\cdot9\cdot8 =792$ 
- Thus, there are 792 distinct 5 person teams


The phrase **at least n** means "n or more"
The phrase **at most n** means "n or fewer"

**Example** Teams with Members of Two Types 
- Suppose the group of twelve consists of (5) five men and  (7) seven women. 
- a. How many five-person teams can be chosen that consist of three men and two women? 
	- $\binom{5}{2} \cdot \binom{7}{2} = \frac{5!}{3!2!} \cdot \frac{7!}{2!5!} = \frac{5!\cdot7\cdot6\cdot5\cdot4\cdot3!}{3!\cdot2\cdot1\cdot2\cdot1\cdot5!} = 210$
- b. How many five-person teams contain at least one man? 
	![[Pasted image 20250329132907.png]]
	![[Pasted image 20250329132959.png]]
c. How many five-person teams contain at most one man?
- ![[Pasted image 20250329133016.png]]

**Example** Permutations of a Set with repeated elements
Consider various ways of ordering the letters in the word MISSISSIPPI: IIMSSPISSIP, ISSSPMIIPIS, PIMISSSSIIP, and so on
![[Pasted image 20250329142101.png]]

![[Pasted image 20250329142152.png]]

### 9.6 r-Combinations with repetition Allowed
![[Pasted image 20250329142251.png]]

**example**
![[Pasted image 20250329142332.png]]

[Stars and Bars Tutorial](https://www.youtube.com/watch?v=40HxI6Uc00Q)


![[Pasted image 20250329142448.png]]

**The Number of Integral Solutions of an Equation**
![[Pasted image 20250329143247.png]]
![[Pasted image 20250329143311.png]]


#### Deciding which formula to Use
![[Pasted image 20250328124203.png]]


## The Binomial Theorem and Pascal's Formula
- In this section we derive several formulas for values of $\binom43$. The most important is *Pascal’s formula*, which is the basis for Pascal’s triangle and is a crucial component of one of the proofs of the binomial theorem. 
- We offer two distinct proofs for both Pascal’s formula and the binomial theorem. 
	- “algebraic” because it relies to a great extent on algebraic manipulation
	- “combinatorial” because it is based on the kind of counting arguments

**example** Values of $\binom nn , \binom{n}{n-1} , \binom{n}{n-2}$
- Regardless of what nonnegative integers are placed in the boxes, if the integer in the lower box is no greater than the integer in the top box, then
- ![[Pasted image 20250329143829.png]]
![[Pasted image 20250329143855.png]]


### Pascal's Triangle 
![[Pasted image 20250329145050.png]]

![[Pasted image 20250329145025.png]]

**Example** Deriving New Formula's from Pascal's Formula
![[Pasted image 20250329145130.png]]


### The Binomial Theorem 
- In algebra a sum of two terms, such as $a+b$, is called a **binomial**. 
- The binomial theorem gives an expression for the powers of a binomial $(a+b)^n$, for each nonnegative integer *n* and all real numbers *a* and *b*
![[Pasted image 20250328124437.png]]It is instructive to see two proofs of the binomial theorem: an algebraic proof and a combinatorial proof. Both require a precise definition of integer power.
![[Pasted image 20250328124533.png]]

**Example**
![[Pasted image 20250329145243.png]]


## Chapter 10 Theory of Graphs and Trees

### 10.1 Trails, Paths and Circuits
