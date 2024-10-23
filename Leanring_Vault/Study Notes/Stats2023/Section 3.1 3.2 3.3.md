## 3.1 - Describing, Exploring, and Comparing Data

- Measures of center = value at the middle of a data set
	- different ways to find the middle = measure***s***
- resistant statistic = statistic that isn't drastically affected by extreme values (outlier) ^1
### finding the center of data

####  **mean**  = add all numbers, divide by how many numbers you have
- don't call it the "average" 
- can be affected by an outlier in data (extreme values)
	- in turn changing value of mean 

![[Pasted image 20241021143038.png]]
![[Pasted image 20241021143150.png]]

![[Pasted image 20241021143310.png]]
![[Pasted image 20241021143330.png]]

##### Example
given a sample of population: 
- 50  25  75  35  50  25  30  50  45  25  20
find mean:
- count how many numbers we have: 11
- add up all numbers: 430
- divide 430/11
$$430/11 = 39.1$$



#### **median** = when numbers are sorted in order, middle number from that order
- resistant to extreme values^1

##### If number of data values is ODD
![[Pasted image 20241021144248.png]]

##### ##### If number of data values is EVEN
![[Pasted image 20241021144420.png]]
- get the 2 values in the middle
	- add them and divide by 2 
$$35+45/2 = 40$$

#### **Mode** = the number that occurs with greatest frequency
- can be found with qualitative data
- data set can have no mode, 1 mode, or multiple modes
	- **bi-modal** = 2 data values share same greatest frequency
	- multimodal = 2 or more data values share same greatest frequency

##### Example:
![[Pasted image 20241021144829.png]]
- sort to make it easier 
- 20,30,30,**35,35,35**,45,50,50,75,95
	- mode is: 35


#### Midrange = data value midway between the max and min values of data set
- easily affected by extreme values (outliers) 
	- not resistant ^1

- rarely used but has use case:
	- *skipped 2 cases, theory based*
	- can be mistaken for median, helpful to distinguish the two

![[Pasted image 20241021145035.png]]

#### Example
![[Pasted image 20241021145303.png]]

$$(75+20)/2 = 47.5$$

### Round off rules for Measures Of Center
- for **mean**, **median** and **midrange** - carry one more decimal place than is present 
- mode = leave as is

### Calculating the mean from a frequency distribution 

#### Step 1: Understand the Frequency Distribution

A frequency distribution summarizes how often each value or range of values occurs in a dataset. It often looks like this:

| Class Interval | Frequency |
|----------------|-----------|
| 10 - 19        | 5         |
| 20 - 29        | 8         |
| 30 - 39        | 12        |
| 40 - 49        | 6         |

#### Step 2: Calculate the Midpoints

For each class interval, calculate the midpoint (also called the class mark):

$$
\text{Midpoint} = \frac{\text{Lower Limit} + \text{Upper Limit}}{2}
$$

For the example above:

- For **10 - 19**: $$(10 + 19) / 2 = 14.5$$
- For **20 - 29**: $$(20 + 29) / 2 = 24.5$$
- For **30 - 39**: $$(30 + 39) / 2 = 34.5$$
- For **40 - 49**: $$(40 + 49) / 2 = 44.5$$

Now your table looks like this:

| Class Interval | Frequency | Midpoint |
|----------------|-----------|----------|
| 10 - 19        | 5         | 14.5     |
| 20 - 29        | 8         | 24.5     |
| 30 - 39        | 12        | 34.5     |
| 40 - 49        | 6         | 44.5     |

#### Step 3: Multiply Frequencies by Midpoints

Next, multiply each frequency by its corresponding midpoint:

| Class Interval | Frequency | Midpoint | Frequency × Midpoint |
|----------------|-----------|----------|-----------------------|
| 10 - 19        | 5         | 14.5     | $$5 \times 14.5 = 72.5$$ |
| 20 - 29        | 8         | 24.5     | $$8 \times 24.5 = 196$$  |
| 30 - 39        | 12        | 34.5     | $$12 \times 34.5 = 414$$ |
| 40 - 49        | 6         | 44.5     | $$6 \times 44.5 = 267$$  |

#### Step 4: Sum the Frequencies and the Products

Now, sum the frequencies and the products:

- **Total Frequency** = $$5 + 8 + 12 + 6 = 31$$
- **Total of Frequency × Midpoint** = $$72.5 + 196 + 414 + 267 = 949.5$$
#### Step 5: Calculate the Mean

Finally, the mean is calculated using the formula:

$$
\text{Mean} = \frac{\text{Total of Frequency × Midpoint}}{\text{Total Frequency}}
$$

Substituting in the values:

$$
\text{Mean} = \frac{949.5}{31} \approx 30.6
$$


### Calculating a weighted Mean

### Weighted Means
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

## Section 3.2 Measures of Variation
Range, Standard deviation and variance
- when rounding off, carry one more decimal place

### Range  = biggest - smallest
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
	- heavily affected by ***outliers***
- same unit as data values (inches, pounds, meters)
- sample standard deviation ***s*** is ***biased** estimator* of the population **σ**, 
	- which means ***s*** doesn't center around the value of **σ**
	
![[Pasted image 20241021194048.png]]

#### Sample Standard Deviation
![[Pasted image 20241021194131.png]]

##### shortcut for Sample Standard Deviation 
![[Pasted image 20241021194208.png]]

#### Example
![[Pasted image 20241021194849.png]]

1. find mean
	1. add all values : 430
	2. count how many values: 11
	3. 430/11 =~ 39

| 2. Subtract Mean | 3. Square each Deviation | Sum all Deviations |
| ---------------- | ------------------------ | ------------------ |
| 10.91            | 119                      |                    |
| -14.09           | 198.6                    |                    |
| 35.91            | 1289.5                   |                    |
| -4.09            | 16.7                     |                    |
| 10.91            | 119                      |                    |
| -14.09           | 198.6                    |                    |
| -9.09            | 82.6                     |                    |
| 10.91            | 119.0                    |                    |
| 5.91             | 34.9                     |                    |
| -14.09           | 198.5                    | *total*            |
| -19.09           | 364.5                    | 2740.9             |
- count how many values (n):  11 -1 : 10 
1. divide sum by n-1
$$ 2740.9 / 10 = 274.09$$
2. take square root of quotient

$$ \sqrt{274.09} = 16.56$$

##### Range Rule of Thumb for understanding SD
- range rule of thumb = understand and interpret SD. 
	- the vast majority (95%) of sample values lie within 2 SD of the mean
- ##### Identifying Significant Values
- ![[Pasted image 20241022211114.png]]

##### Range rule of thumb for estimating value of SD *s*
- to roughly estimate the SD from a collection of data, use (range/4)

#### Standard Deviation of a Population
![[Pasted image 20241022212233.png]]
- only difference is division by population size: `N`

### Variance of a Sample and a Population 
- Variance  = a measure of variation equal to the square of the SD
	- Sample Variance = $S^2$
	- Population Variance = $\sigma^2$
- not resistant ^1
- never negative
- sample variance $s^2$ is **unbiased estimator** of population variance $\sigma^2$
	- tends to center around the value of of $\sigma^2$
### Notation Summary 
![[Pasted image 20241022212705.png]]


## 3.3 Measures of Relative Standing and Boxplots 

### Z Score 
- the number of standard deviations that a given value x is above or below a mean
- round off 2 deci places (2.13)
- expressed as number, no unit
 
![[Pasted image 20241022213517.png]]
 
- **Sample**: Z = data point - sample mean / sample SD
- **Population** = data point - population mean / population SD

- Significantly Low
	- if Z-score $\leq -2$
- Significantly High 
	-  if Z-score $\geq +2$

#### Example:
Which of the following two data values is more extreme relative to the data set from which it came?
1.  The 99°F temperature of an adult 
	- sample mean  = 98.20°F 
	- sample SD =  ***s*** = 0.62°F
2. The 5.7790 g weight of a quarter 
	-  sample mean  = 5.63930 g 
	-  sample standard deviation s = 0.06194 g 

1. 99 F temperature $$Z = \frac{99-98.20}{0.62} = 1.29$$
2. Weight of quarter $$ Z = \frac{5.7790-5.63930}{0.06194} =2.26 $$
### Percentiles 
- are measure of location which divides a set of data into 100 groups, with 1% of values in each group  
	- denoted by $P_{1}$ 
![[Pasted image 20241022215914.png]]
- round to whole number

#### Example
![[Pasted image 20241022215947.png]]
- find percentile of 45 (x)

- **count** how many numbers less than 45: 36
- **count** how many total numbers: 50
$$ x = \frac{36}{50} *100 = 72 $$
#### Notation 
![[Pasted image 20241022220740.png]]

#### Converting a Percentile to a Data Value
![[Pasted image 20241022220902.png]]

##### Example

![[Pasted image 20241022221054.png]]

