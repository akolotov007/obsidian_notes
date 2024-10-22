## Weighted Means
![[Pasted image 20241021190630.png]]
#### Example
In her first semester of college, a student took five courses. Her final grades, along with the number of credits for each course, were:
A (3 credits), 
A (4 credits),
B (3 credits), 
C (3 credits),  
F (1 credit). 

The grading system assigns quality points to letter grades as follows: 
A = 4; B = 3; C = 2; D = 1; F = 0. 
Compute her grade-point average.
__
so our *weights* are :3,4,3,3,1
and our quality points (x) = A A B C F = 4 4 3 2 0 

add up all **w**eights:
- 3+4+3+3+1+0 = 14
add up all **x** values:
- 4+4+3+2+0 = 13

$$ w*x/14 = 14*13/13 = 14 $$

# Section 3.2 Measures of Variation
Range, Standard deviation and variance
- when rounding off, carry one more decimal place

## Range  = biggest - smallest
- the difference btwn max data value and min data value
- not resistant ^1
- since it doesn't look at all values, doesn't reflect the variation in the data

![[Pasted image 20241021193637.png]]

75-20 = 55 is range


### Standard Deviation = how far data moves away from the mean
- a set of sample values, ***s***, measures how much data deviates from the mean 
- can **never be 0**
	- unless all data values are equal 
- larger values of ***s*** indicates greater amounts of variation
	- heavily affected by *outliers*
- same unit as data values (inches, pounds, meters)
- sample standard deviation ***s*** is *biased estimator* of the population **σ**, 
	- which means ***s*** doesn't center around the value of **σ**
	
![[Pasted image 20241021194048.png]]

#### Sample Standard Deviation
![[Pasted image 20241021194131.png]]

#### shortcut for Sample Standard Deviation (by calculators and software)
![[Pasted image 20241021194208.png]]

##### Example
![[Pasted image 20241021194849.png]]

1. find mean
	1. add all values : 430
	2. count how many values: 11
	3. 430/11 =~ 39;
2. subtract mean from each value
3. Square each deviation 
4. sum all deviations
5. divide sum by n-1
6. take square root of quotient



