## Section 4.1

### Basic Concepts of Probability
- probability values range from 0-1. 

- **Event**                = any collection of results or outcomes of a procedure
- **Simple Event**    = an outcome or event that cannot be further broken down into simpler components
- **Sample Space**  = consists of all possible **simple events**. 
	- that is to say, the sample space consists of all outcomes that cannot be broken down any further

### 3 Common approaches to finding the probability of an event
#### Prerequisite
![[Pasted image 20241024141708.png]]
##### notable values of probability

| 1                 | Certain    |
| ----------------- | ---------- |
| $0.5\leq{x}\leq1$ | Likely     |
| 0.5               | 50/50      |
| $0\leq{x}\leq0.5$ | unlikely   |
| 0                 | Impossible |

#### 1. Relative Frequency Approximation of Probability
- conduct a procedure and count the number of times that event *A* occurs. *P(A)* is the approximated as follows:
$$P(A) = \frac{\text{number of times A occured}}{\text{number of times the procedure was repeated}}$$

#### 2. Classical Approach to Probability 
requires equally likely outcomes 
- if procedure has *n* different simple events that are **equally likely**, and if event *A* can occur in *s* different ways, then:
$$P(A) = \frac{\text{number of times A occurs}}{\text{number of different simple events}} = \frac{s}{n}$$
**CAUTION**  when using classical approach, always confirm that outcomes are equally likely

#### 3. Subjective Probabilities
- the probability of event *A* is **estimated** by using the knowledge of the relevant circumstances

### Rounding Probabilities
 - either give **exact** fraction, or final decimal rounded to 3 significant figures
	 - better as decimal if fraction isn't simple, ie: $\frac{3}{5}$

### Example: Relative Frequency Probability
- In a recent year, there were about 39 million commercial airline flights and 16 of them crashed. We use the relative frequency approach as follows:
	- Find the probability that a commercial airliner will crash on any given flight.

occurrence of A = 16
all occurrences = 39 million

$P(A) = \frac{16}{39000000} =4.102564102564103 e-7$

#### Another Example: Relative Frequency Probability
- In a Pew Research Center survey, randomly selected adults were asked if they have seen or have been in the presence of a ghost. 366 of the respondents answered “yes,” and 1637 of the respondents answered “no”. 
	- Based on these results, find the probability that a randomly selected adult says that they have seen or been in the presence of a ghost (**yes**).

366 = yes
1637 = no
all  responses = 1637+366 = 2003 

now we can use relative freq.
$P(A) = \frac{366}{2003} =0.183$


### Complement Events
- the complement of even *A* denoted by $\overline{A}$ consists of all outcomes in which event *A* does **not** occur
### Example
- In a Pew Research Center survey of 2002 randomly selected adults, 1782 of those respondents said that they use the Internet. 
	- Find the probability that a randomly selected adult does not use the Internet.

use internet  = 1782
total  = 2002
2002 - 1782 = 220 | people who don't use the internet

$P(\overline{A}) = \frac{20}{2002} \approx 0.109$

*a quicker way:*

$P(\overline{A})=1−P(A)$

$P(\overline{A}) = 1 -\frac{1782}{2002} \approx 0.109$


### Identifying Significant Results with Probabilities
- #### significantly high number of success when odds of x succeeding less than 0.05
	- *x*  successes among *n* trials is **significantly high** number of successes if the probability of x or more successes is unlikely with a probability of 0.05 or less. That is, x is a significantly high number of successes if P(x or more) ≤ 0.05*.
	- *The value 0.05 is not absolutely rigid.
- #### significantly low number of success when odds of x succeeding less than 0.05
	- *x* successes among *n* trials is a significantly low number of successes if the probability of *x* or fewer successes is unlikely with a probability of 0.05 or less. That is, x is a significantly low number of successes if P(x or fewer) ≤ 0.05*.

### Probability Review 
![[Pasted image 20241024150947.png]]

### Odds of an event
##### odds in favor
- define the favorable outcome
	- count the number of ways favorable outcome occurs
- count the total possible outcomes 
- favorable outcomes : total outcomes
##### odds against
- inverse of odds in favor

#### Example
- suppose we roll a fair die, what are the odds in favor of rolling a 5 or higher?
	- favorable outcome = 5 or greater 
		- count 2 : (5,6)
	- count total outcomes : 6 (1,2,3,4,5,6)
	- 2:6 = 1:3 odds in favor of rolling a dice 5 or higher

- Odds against rolling a 5 or higher?
	- 2 unfavorable outcomes (5,6). what are favorable:
		- 1,2,3,4
	- 4 favorable outcomes : 6 total outcomes
		- 4:6 = 2:3 odds against rolling a number 5 or greater

#### Another Example
 - The odds in favor of raining is 3 to 7. What is the probability of raining?
	 - 3:7 = 3/7 = .3 = 30% chance of raining


## Section 4.2
### Addition and Multiplication of probabilities
- or = "addition"
- and  = "multiplication"

- **compound event** = any event combining 2 or more **simple events** 
### Disjoint Events 
- (mutually exclusive)
	- A and B are **disjoint**, if they cannot occur at the same time 
		- A and B don't overlap
	- Example:
		- event A - randomly selecting a male in clinical trial
		- event B - randomly selecting a female in clinical trial
			- can't be both at the same time

### Addition Rule
$P(A \text{ or } B)$ = *P*(in single trail, event A occurs ***or*** event *B* occurs, ***or*** both occur)

#### Intuitive Addition Rule 
- to find P(A or B), add number of ways A can occur to B. Add in such a way that every outcome is counted only once.
	-  P(A or B) is equal to that sum, divided by the total number of outcomes in the sample space

#### Formal Addition Rule
- P(A or B) = P(A) + P(B) − P(A and B)
	- P(A and B) = both A and B occur at the same time as an outcome 

#### Complementary Events and Addition Rule
We use $\overline{A}$ to indicate that event $A$ does not occur. 
>     Common sense dictates this principle: 
	 We are certain (with probability 1) that either an event A occurs or it does not occur, so it follows that P(A "or"  $\overline{A}$)=1. Because events A and $\overline{A}$ must be disjoint, we can use the addition rule to express this principle as follows:
	 $P(A\text{ or }\overline{A}) = P(A)+P(\overline{A}) = 1$


#### Rules of Complementary Events
$P(A)+P(\overline{A}) = 1$
$P(A)= 1 - (\overline{A})$
$P(\overline{A})= 1 - P(A)$


#### Example
- Based on survey results from the Consumer Technology Association, the probability of randomly selecting a household in the United States and getting one with a smartphone is 0.87 so P(smartphone) = 0.87. 
	- If a household is randomly selected, find the probability of getting one that does not have a smartphone.

$P(\overline{A})= 1 - P(A) =$
	$1-P(\text{smartphone}) =$
	$1-0.87 = 0.13$
$P(\overline{A}) = 0.13$


### Multiplication Rule
$P(A \text{ and }B)$ = P(A occurs in a first trail and B occurs in a second trail)

$P(B|A)$ = probability event B occurring after it is assumed that event A has already occurred

#### Intuitive Multiplication Rule
- multiply probability A and probability B, be sure that the probability of event B is found by assuming that event A has already occurred 

#### Formal Multiplication Rule
$P(A \text{ and }B) = P(A) \times P(B|A)$

#### Independence 
- two events *A* and *B* are **independent** if occurrence of one doesn't affect the probability of the other.
- if not independent, the events are considered **dependent**

#### Example:
![[Pasted image 20241024163706.png]]
![[Pasted image 20241024163715.png]]
part A. 
	P(positive test result) = 45/50 = 0.9
		P(T)
	P(negative test result) = 5/50 = 0.1
		P(N)
	P( T first, N second) =$P(T) \times P(N) =0.9\times0.1=0.9$

part B.
	when selecting **without replacement**, the total number of subjects change after the first selection. (after pulling a person from sample, now sample size -1)
- P(positive test result) = 45/50 = 0.9
- P(negative test result) = 5/**49** = 0.1020408

- P(T first, N second) = $P(P) \times P(N|P) = 0.9\times0.1020408 = 0.0918$


### Sampling 
- **with** replacement
	- selections are **independent** events
- **without** replacement
	- selections are in **dependent** events