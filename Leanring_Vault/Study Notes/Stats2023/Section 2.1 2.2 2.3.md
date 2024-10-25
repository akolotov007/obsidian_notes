## 2.1 - Frequency Distribution 

## frequency distribution 
(frequency table) 
- helps understand the **distribution** of a data set
	- data partitioned among several classes (categories)

###### Lower Class limits
- **smallest** number that can belong to each of the different classes 
###### Upper Class limits 
- **largest** number that can belong to each of the different classes 
###### Class boundaries 
- numbers used to separate the classes but without gaps created by class limits
	- 10-19
- 20-29
- 30-39
###### Class midpoints 
- values in the middle of the classes
	- (lower limit + upper limit) / 2 

###### Class width 
- the difference btwn 2 consecutive lower class limits in a frequency distribution
- ![[Pasted image 20241016132605.png]]

	- class width in frequency distribution 
		- the difference between 2 lower bounds 

class boundaries
- split the difference between the **end** of one class and the **beginning** of the next class
	{(class A upper bound) + (Class B lower bound) }/ 2

### Procedure for Constructing a Frequency Distribution 
1. select the number of classes, btwn 5 and 20
2. calculate the class width
	- ![[Pasted image 20241016132608.png]]
3. choose value for the first lower class limit
4. using lower class limit and class width, create the other lower-class limits
	1. list lower class limit in vertical column and then determine and enter the upper-class limit
5. take each individual data value and put tally mark in appropriate class
	1. add tally marks to get the frequency

Example:
![[Pasted image 20241016132927.png]]

- creating 7 classes
	- calculate class width : $$(90-5)/7 =12.14 ≈ 15 $$ rounded to 15 for convenience

- first lower class limit 0  / since the lowest number is 5
 - add class width of 15 to starting value of 0, these are our **upper class limits**

| step 1. | 0-  | step.2 then we add the other half | 0-14   |
| ------- | --- | --------------------------------- | ------ |
|         | 15- |                                   | 15-29  |
|         | 30- |                                   | 30-44  |
|         | 45- |                                   | 45-59  |
|         | 60- |                                   | 60-74  |
|         | 75- |                                   | 75-89  |
|         | 90- |                                   | 90-104 |

now we add the frequencies: 
- what numbers fall into the classes that we created

| Daily Commute in Minutes | Frequency |
| ------------------------ | --------- |
| 0-14                     | 6         |
| 15-29                    | 18        |
| 30-44                    | 14        |
| 45-59                    | 5         |
| 60-74                    | 5         |
| 75-89                    | 1         |
| 90-104                   | 1         |
| *total*                  | *50*      |


### Relative Frequency Distribution 
- class frequency is replaced by a relative frequency (or a percentage)
	- sum of percentages must be very close to 100% (small margin of error)

![[Pasted image 20241021135316.png]]

*same equation, only changing decimal to percent*

![[Pasted image 20241021135326.png]]

| Daily Commute in Minutes | Frequency | Relative Frequency | Cumulative  Frequency |
| ------------------------ | --------- | ------------------ | --------------------- |
| 0-14                     | 6         | 6/50 x 100% = 12%  | 12%                   |
| 15-29                    | 18        | 18/50 x 100% = 36% | 48% \| 12+36          |
| 30-44                    | 14        | 14/50 x 100% = 28% | 76% \| 12+36+28       |
| 45-59                    | 5         | 5/50 x 100% = 10%  | 86% \| 12+36+28 + 10  |
| 60-74                    | 5         | 5/50 x 100% = 10%  | 96% \| 12+36+28 + 10  |
| 75-89                    | 1         | 1/50 x 100% = 2%   | 98%                   |
| 90-104                   | 1         | 1/50 x 100% = 2%   | 100%                  |
| *total*                  | *50*      | *100%*             |                       |
Additionally shown, cumulative frequency 


## 2.2 Histograms
- visualizes data as a bar graph
	- bars of equal width, no gap between
	- **horizontal** scale : quantitative 
	- **vertical** scale : frequencies![[512px-Symmetric-histogram.webp]]
	- shows center of data
		- shows spread
		- identifies outliers

### Building a Histogram
- given frequency distribution, make a histogram
![[Pasted image 20241021133910.png]]
![[Pasted image 20241021133925.png]]

### Relative Frequency Histogram 
-  Has the same shape and horizontal scale as a *histogram*, but vertical scale is relative frequencies 
![[Pasted image 20241021140018.png]]
- *on right, relative frequency histogram*

### Common Distribution Shapes
![[Pasted image 20241021140049.png]]

### Normal Distribution
- if the histogram is roughly bell shaped, we say that the data has a **normal distribution**
![[Pasted image 20241021140157.png]]


### Skewness
  - when the data leans to one side of the histogram 
	  - aka. data is not symmetric and extends more to one side than to the other

#### Skewed to the right 
![[Pasted image 20241021140320.png]]
- longer right "tail"

#### Skewed to the left 
![[Pasted image 20241021140352.png]]
- longer left "tail"

## 2.3 - Exploring Data with Tables and Graphs

### Stem plots (stem and leaf plots)
 - shows **quantitative** data by separating each value into 2 parts: 
	 - stem - leftmost digit
	 - leaf - rightmost digit
![[Pasted image 20241021141007.png]]
*in this case it separates the tens place and ones place*

#### Constructing a Stem-Leaf Plot
given data:
- 12, 15, 14, 22, 23, 21, 33, 31, 35
make stem plot:
- group by same first digit
	12,15,14
	22,23,21
	33,31,35
- put in order
	12,14,15
	21,22,23
	31,33,35
- create table

| Stem | Leaf    |
|------|---------|
| 1    | 2 4 5   |
| 2    | 1 2 3   |
| 3    | 1 3 5   |

### Bar Graph
- graph of bars of equal width to show frequencies of categories of qualitative data
	- may / may not have gaps
- shows relative distribution of data that's easier to compare to different categories 
![[Pasted image 20241021141716.png]]

### Pareto Chart
- a bar graph for categorical data, bars are arranged in **descending order**

![[Pasted image 20241021141938.png]]


### Graphs that Deceive
#### non-zero vertical axis
- a common deceptive graph is when the vertical axis **doesn't** start from 0
![[Pasted image 20241021142042.png]]
*on left, vertical axis starts at 10%, making it seem that Placebo is much lower than OxyContin*

#### Pictographs
- drawings of objects
	- data that should be just numbers is now shown as an object 
	- 
![[Pasted image 20241021142237.png]]
