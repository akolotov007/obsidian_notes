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
- 