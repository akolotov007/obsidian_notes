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
		- count favorable outcomes : (5,6)
	- count total outcomes : 6 (1,2,3,4,5,6)
	- 2:6 = 1:3 odds in favor of rolling a dice 5 or higher

- Odds against rolling a 5 or higher?
	- 2 unfavorable outcomes (5,6). what are favorable?:
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
	 We are certain (with probability 1) that either an event A occurs or it does not occur, so it follows that P(A "or"  $\overline{A}$)=1. Because events A and $\overline{A}$ must be [[Section 4.1 4.2 4.3 4.4#Disjoint Events|disjoint]], we can use the addition rule to express this principle as follows:
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
- if not independent, then events are considered **dependent**

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
- P(negative test result) = 5/**49(-1)** = 0.1020408

- P(T first, N second) = $P(P) \times P(N|P) = 0.9\times0.1020408 = 0.0918$


### Sampling 
- **with** replacement
	- selections are **independent** events
- **without** replacement
	- selections are in **dependent** events



## Section 4.3

### Conditional Probability
- *extending the multiplication rule to include the probability that among several trials, we get **at least one** of some specified event.*
-  **conditional probability** = the probability of event occurring when we have additional info that some other event has already occurred
	- brief intro to Bayes' theorem

### Complements : The probability of "At Least One"
- when finding probability of "at least once", understand that:
	- "at least once" = "one or more"
	- finding complement of getting "at least one" event is **no** occurrence of that event 

#### The Probability of "at least one"
- A = at least one of some event
- $\overline{A}$ = getting none of the event
- subtract from 1:
	- $P(\text{at least one occurence }A) = 1-P(\text{no occurence of event }A)$

- in essence, exactly same concept of complements, adding on "at least once" as a label

#### Example
- A factory of the Global Manufacturing Company was manufacturing products with a defect rate of **15%** (based on data from the Harvard Business Review). If a customer purchases 12 of the products, what is the probability of getting at least one that is defective?

- let $A$ = at least 1 of 12 is defective
- identify the complement: 
	- not getting at least 1 of 12 defective = all 12 items are good with no defects
	- $\overline{A}$ = all 12 items are good

Step 1 
- find the probability of **a product** being non-defective:
	- $1 - .15 = .85$
- $P(\overline{A})$ = ( non-defective$)^{items}$ = $0.85^{12}\approx 0.142$  
	- about 14.2% chance that all products are non-defective

Step 2:
- find the complement of $P(\overline{A})$ :
	- $1 - P(\overline{A})  = 1 - 0.142 = 0.858$
- approx. 85.8% that **at least one** product will be defective 


### Conditional Probability 
- the probability obtained with the additional information that some other event has already occurred
- $P(B | A)$
	- the conditional probability of event B occurring, given that event A has already occurred.

#### Intuitive Approach for finding P(B|A)
- **assuming that event A** has occurred and then calculating the probability that event B will occur.
	- *said the same shit as in conditional probability*


#### Formal Approach for finding P(B|A)
$$ 
P(B|A) = \frac{P(A \text{ and }B)}{P(A)}
$$
#### Example
a. If 1 of the 555 test subjects is randomly selected, find the probability that the subject had a positive test result, given that the subject actually uses drugs. That is, find P(positive test result | subject uses drugs).

b. If 1 of the 555 test subjects is randomly selected, find the probability that the subject actually uses drugs, given that he or she had a positive test result. That is, find P(subject uses drugs | positive test result).

b is flipped version of a

|                           | Positive Test Result | Negative Test Result |
| ------------------------- | -------------------- | -------------------- |
| Subject Uses Drug         | 45 (True Positive)   | 5 (False Negative)   |
| Subject Does not Use Drug | 25 (False Positive)  | 480 (True Negative)  |
**Part A**
$$
P(\text{Positive Test Result}∣\text{Subject Uses Drugs})=\frac{\text{P(Positive Test Result and Subject Uses Drugs})}{P(\text{Subject Uses Drugs})}​
$$
- True Positive  (**uses drugs and tests positive** )= 45
- False Negatives (subjects who use drugs and test negative): 5
- $\text{total using drugs} = 50$
> *can be simplified to just 45 and 50, excluding total participants*
> 
> now find $\text{P(Positive Test Result and Subject Uses Drugs})$
	 45/555
>
>now find $P(\text{Subject Uses Drugs})$
	 50 / 555

now substitute values:
	$$\frac{\frac{45}{555}}{\frac{50}{555}} = \frac{45}{50} = 0.9$$
Therefore, the probability that a subject has a **positive test result** and they actually **use the drug** is 0.9

**Part B**

$$
P(\text{Subject Uses Drugs}|\text{Positive Test Result})=\frac{\text{P(Positive Test Result and Subject Uses Drugs})}{P(\text{Positive Test Result})}​
$$
now simplified:

- uses drugs and positive test result = 45
- all positive test results = 45+25 = 70


$\frac{45}{70} \approx 0.643$


## Section 4.4

### Counting
- 5 different methods of counting the number of possible outcomes in a variety of situations

### Multiplication Counting Rule
- for sequence of events in which the first event can occur $n_{1}$ ways, the second event can occur $n_{2}$ ways... the total number of outcomes is: $n_{1}*n_{2}*n_{3}*...n_{n}$

#### Example
- A computer hacker finds that a password is entered as •••••, so the characters are hidden, but we can see that there are five characters. We can use 92 different characters with a typical keyboard. How many different passwords are possible using five characters? If the hacker starts to generate all different possibilities, what is the probability of guessing the correct password **on the first attempt?**

There are 92 different possibilities for each character, so the total number of different possible passwords is:
n1 · n2 · n3 · n4 · n5 = 92 · 92 · 92 · 92 · 92 = 659,081,000,000

on the first attempt:
1/659,081,000,000 = $1.517*10^{-12}$



### Factorial Rule
- the number of different **arrangements** (order matters) of *n* different items when all *n* of them are selected is *n!*

- factorial symbol (**!)** = the product of decreasing positive whole number values. By special definition: 0! = 1
	- n! = n(n-1)(n-2)... 3 * 2 * 1

#### Example
- Some words consist of letters which can be rearranged to form other words. Consider the word “steam.”
	a. How many different ways can the letters of “steam” be arranged?
	b. If the letters of “steam” are arranged randomly, what is the probability that the letters will be in alphabetical order?

**Solution**
A
- for those 5 different letters, the number of different arrangements is 
- 5! = 5 * 4 * 3 * 2 * 1 = 120

B
- there is only 1 arrangement in which the letters will be in alphabetical order: "aemst"
- therefore, the probability of the letters being listed in alphabetical order is:
	- 1/120


### Permutations and Combinations

#### Permutations
- are arrangements in which different sequences of the same items are counted **separately**
	- abc, acb, bac, bca, cab, cba:  are all counted **separately** as six different permutations

#### Combinations
- are arrangements in which different sequences of the same items are counted as **being the same**
	-  abc, acb, bac, bca, cab, cba:  are all considered the **same** combination

#### Mnemonics of Permutations and Combinations
- Permutations Position
	- position makes difference
- Combinations Committee

#### Permutations Rule 
- when *n* different items are available and *r* of them are selected without replacement, the number of different permutations (order counts) is given by:
$$P(n,r) =\frac{n!}{(n-r)!} $$

##### Example
- In a horse race, a trifecta bet is won by correctly selecting the horses that finish first and second and third, and you must select them in the correct order. The 144th running of the Kentucky Derby had a field of 20 horses.
	a. How many different trifecta bets are possible?
	b. If a bettor randomly selects three of those horses for a trifecta bet, what is the probability of winning by selecting Justify to win, Good Magic to finish second, and Audible to finish third, as they did? Do all of the different possible trifecta bets have the same chance of winning? (Ignore “dead heats” in which horses tie for a win.)

**Solution**
A
	there are n=20 horses, and we must select r=3 of them without replacement:
	$$P(20,3) =\frac{20!}{(20-3)!} = \frac{20!}{17!} = 20\cdot19\cdot18 = 6840$$

B
given a specific event of 3 horses winning in order = 1 specific event / all possible events
$$\frac{1}{6840}$$


#### Combinations Rule
- almost same as permutations, where order doesn't matter
$$C(n,r) =\frac{n!}{r!(n-r)!} $$
##### Example
- In Florida’s Cash 5 lottery game, winning the jackpot requires that you select 5 different numbers from 1 to 35, and the same 5 numbers must be drawn in the lottery. The winning numbers can be drawn in any order, so order does not make a difference.
	a. How many different lottery tickets are possible?
	b. Find the probability of winning the jackpot when one ticket is purchased.

**Solution**
A
	n = 35
	r = 5
	
$$C(35,5) =\frac{35!}{5!(35-5)!} = \frac{35!}{5!(30)!}  = \frac{!35}{!5\cdot!30} = \frac {35\times34\times33\times32\times31}{!5}$$
$$\frac {35\times34\times33\times32\times31}{120} = \frac{38,955,840}{120} =324,632 $$

B
finding the probability of winning the jackpot when one ticket is purchased:
$\frac{1}{324,632} = 0.00000308 = 3.08\cdot10^{-6}$
