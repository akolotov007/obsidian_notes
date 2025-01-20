basic math objects : 
[[Module 1 - Speaking Mathematically#Sets|Sets]]
[[Module 1 - Speaking Mathematically#Functions|Functions]] 
[[Module 1 - Speaking Mathematically#Relations|Relations]]

### Sets
- a **set** is a collection of objects 
	- A = students in this class
	- B  = {1,3,5,7}
	- $Z = \text{Integers}$

#### Elements of Sets can be written as:
- John $\in$ A  = John in set A 
- 2 $\notin$ B  = 2 not in set B 

#### Order and Repetition Doesn't Matter
{1,3,4,7} = {7,3,4,1} = {7,7,4,4,4,1,1,3,3}


#### Subsets
- every element of A is also in element B  
- $A \subseteq B$ = A is a subset of B. 
		= A is contained in B 
*example:*
		{1,3} $\subseteq$ {1,3,4,7}

##### Differences between signs
$\in$ = relation between an element and a set 
$\subseteq$ = relation between 2 sets

*example*:
- $b\in\{a,b,c\}$ is mathematically legal
- $b\subseteq \{a,b,c\}$ is ***not*** mathematically legal
	- $\{b\}\subseteq \{a,b,c\}$ is legal 



##### Proper and Improper Subsets
$A  = \{a,b,c\}$
- $\{b,c\} \subseteq A$
- $\{a,b,c\} \subseteq A$
a subset means either:
- that all of the elements that exist in the original set are in the subset
- or just some elements that exist in the original set are in the subset 

**proper subset** = contains only *some* of the elements of the original set (not all elements)
- this means that:  $\{b,c\} \subset A$

to make $\{a,b,c\}$ a *proper* subset, $A$ would have to have one more element inside of it that is not included in the subset.

**not a subset:**
	*example:*
		 {1,8} $\nsubseteq$ {1,3,4,7}

$A \subset A$


#### Set Roster Notation 
- putting elements inside of { } 

*there are times when we have enormous sets filled with elements. If there is some pattern amongst the elements, we can indicate that with "..."*

{0,2,4,6,...}
{...,-6,-4,-2,0,2,4,6,...}

#### Set Builder Notation 
- general form:  $\{x|P(x)\}$
	- x such that: x has a particular property that is true 

*examples*
- $\{x|\text{twice an integer}\}$ `all even numbers in set builder notation`
- $\{x|\sqrt(x)\in Z\}$ `numbers who's square root is an integer`

#### Special Sets and their Notations
- $\mathbb{Z} = \text{set of integers}$
	- { ...-4,-3,-2,-1,0,1,2,3,4... }
- $\mathbb{Z^+} = \text{set of non-negative integers}$
	- {0,1,2,3,4,5...}
- $\mathbb{Z^{++}} = \text{set of positive integers}$
	- {1,2,3,4,5...}

- $\mathbb{R} = \text{set of real numbers}$
- 
- $\mathbb{Q} = \text{set of rational numbers}$
	- ratio of 2 integers, 
	- ${p}/{q}$

- $\mathbb{C} = \text{set of complex numbers}$
	- $5+3i \in \mathbb{C}$

##### Defining Special Sets using Set Builder Notation
$\mathbb{Z^+} = \{n\in \mathbb{Z}| n \geq0\}$
$\mathbb{Z^{++}} = \{n\in \mathbb{Z}| n > 0\}$

$\mathbb{Q} = \{x\in \mathbb{R}| x = \frac{p}{q}, p,q\in\mathbb{Z}\}$



#### Sets without objects
Notation:
- $\{\}$
- $\emptyset$

what is $\{\emptyset\}?$
- "Set A has Set B. Set A has something. Set B has nothing."
	- like a box that has another box inside of it 


$\text{Is }\emptyset \subset\{1,2,3\}?$
- "is empty set a subset of {1,2,3}?"
	- Yes, since there is nothing to check in empty set A that would be a subset of B
		- this is called *vacuously true*


#### Cartesian Product 
 - ordered pair = $(a,b)$
	- order matters
- $(a,b) = (c,d) \text{ if } a=c \text{ and } b=d$
- $a \text{ and } b$ could come from different sets 

**Cartesian Product**
- A x B is the set of all ordered pairs $(a,b)$ where  $a\in A$ and $b\in B$ 
	- *example:* Cartesian Plane
	- coordinate pair (2,1) $\in \mathbb{R}\times\mathbb{R}$
		- the X line is all real numbers
		- the Y line is all real numbers
Set builder notation:
- $A\times B = \{(a,b) | a\in A, b \in B \}$

*Example*
- $\{a,b\} \times \{0,1\}$
	-  $A \times B$
-  $A \times B$ = $\{(a,1),(a,0),(b,1),(b,0)\}$



