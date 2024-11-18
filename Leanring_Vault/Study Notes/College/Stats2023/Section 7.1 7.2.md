## Estimating Parameters and Determining Sample Sizes
### Estimating a Population Portion 
- Point Estimate
	- the sample proportion is the best **point estimate** of the population proportion *p*
		- single value used to estimate population parameters. 
- Confidence Interval
	- we can use a sample proportion to construct a **confidence interval** estimate of the true value of a population proportion 
- Sample Size necessary
	- we should know how to find the sample size necessary to estimate population proportion 


### Point Estimate 
- unbiased estimator 
	- is a "best guess" or "single best value" for the true parameter, based on the sample data.
		- when you collect a sample from a population, you use sample data to estimate population parameters such as: 
		- population mean $\mu$, 
		- population proportion $p$, 
		- population variance $\sigma^2$.
- statistic targets the population proportion *P*

#### Example
- The chapter problem included reference to a Sallie Mae survey of 950 undergrad college students, and 53% of them said that they take of online courses. Based on the result, find the best point estimate of the **proportion** of *all* undergraduate college students who take online classes.

$$
p = \frac{\text{number of students taking online classes}}{\text{total number of students surveyed}} = 0.53
$$
- given 53%, we can just pull the percent and convert it 


### Confidence Interval
- aka interval estimate 
- is a range (or an interval) of values used to estimate the true value of population parameter. 
- abbreviated as CI

### Confidence Level 
- is probability 1-*a*  that the confidence interval actually does contain a population parameter, assuming that the estimation process is repeated a large number of times. 
- aka (degree of confidence)


### Relationship between confidence Level and *a*

| Most Common Confidence Levels | Corresponding Values of *a* |
| ----------------------------- | --------------------------- |
| 90%                           | a = .10                     |
| 95%                           | a = 0.05                    |
| 99%                           | a = 0.01                    |

### Critical Values 
- in standard normal dist, a **critical value** is z score on the borderline separating those z-scores that are significantly low or high from those that are not significant.
- ![[Pasted image 20241114193323.png]]

#### Finding Critical Values
- find critical value corresponding to a 95% confidence level
	- when finding critical z-score for 95%, we use a cumulative left area of 0.975 (not 0.95)
	- ![[Pasted image 20241114193559.png]]

### Common Critical Values 
$$Z_{\frac{a}{2}} = $$

| Confidence Level | *a*  | Critical Value |
| ---------------- | ---- | -------------- |
| 90%              | 0.1  | 1.645          |
| 95%              | 0.05 | 1.96           |
| 99%              | 0.01 | 2.575          |

### Margin of Error 
*inverse relation with sample size*
- denoted by *E*
- **maximum likely amount of error** 
	- (the amount by which the sample statistic misses the population parameter)
- also known as **max error of estimate**
	- can be found by multiplying the critical value and estimated standard deviation of sample proportions 
$$Z_{a/2}\times\frac{\sigma}{\sqrt{n}}$$

#### Margin of Error *E* for Proportions 
##### Wald Confidence Interval
$$ E = z_{\frac{a}{2}}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}} $$
- where  $Z_{\frac{a}{2}}$= critical value
- and $\sqrt{\hat{p}{\hat{q}}/n}$ is the estimated standard deviation if sample proportions 

###  Confidence Interval for Estimating a population Proportion *P*
- Notation 
	- $P$ = population proportion 
	- $\hat{p}$ = sample proportion 
	-  n = number of sample values
	-  *E* =  margin of error 
	-  $Z_{\frac{a}{2}}$= critical value corresponding to the desired confidence intervals
- Requirements
	- sample is simple random sample
	- conditions for binomial distribution is satisfied 
		- fixed number of trails
		- trails are independent 
		- two categories of outcomes
		- and probabilities remain constant for each trial 
	- there are 5 successes and failures 

- rounded to 3 decimal places
$$ \hat{p}-E < P < \hat{p}+E$$
Confidence interval often expressed as:
$\hat{p}\pm E$ or $(\hat{p}-E,\hat{p}+E)$

### Interpreting confidence Interval 
- 0.405 < p < 0.455

- **correct** interpretation:
- "we are 95% **confident** that the interval from 0.405 to 0.455 actually does contain the true value of the population"

- **wrong ways** to interpret:
	- "there is a 95% chance that the true value of *p* will fall between 0.405 and 0.455"
	- "95% of sample proportions will fall between 0.405 and 0.455"

### Procedure for Constructing a Confidence Interval for *p*
- use tech or z-scrore table to find the critical value that corresponds to the desired confidence level 
- evaluate the margin of error
- using the value of the calculated margin of error $E$ and the value of the sample proportion, find the values of the **confidence interval limits**. 
- round final results to 3 places


#### Example
- we noted that in a Sallie Mae survey of 950 undergraduate students, 53% take online courses. The sample results are 
- $n = 950$ 
- $\hat{p} = 0.53$

a. find the margin of error *E* that corresponds to a 95% confidence interval   
$$E = z_{\frac{a}{2}}\sqrt{\frac{\hat{p}(1-\hat{p})}{n}} = 1.96 \times \sqrt{\frac{0.53(1-0.53)}{950}}\approx 0.0317$$
- the margin of error is 0.0317

b. Find the 95% confidence interval estimate of the population proportion p.
- the 95% confidence interval for the population proportion is given by:
	- $\hat{p}\pm E => 0.53 \pm 0.0317$
	- $[0.4983, 0.5617]$

c. Based on the results, can we safely conclude that more than 50% of undergraduates take online courses?
-  Based on the confidence interval obtained in part (b), we **cannot** safely conclude that more than 50% of undergraduates take online courses. 
- Because the confidence interval ranges from $0.498 \text{ to } 0.562$, it is possible that the population percentage is below 50%.

d. Assuming that you are an online reporter, write a brief statement that accurately describes the results, and include all of the relevant information.
- 53% of undergraduates take online courses. That percentage is based on a Sallie Mae survey of 950 randomly selected undergraduates. In theory, in 95% of such polls, the percentage should differ by no more than 3.2 percentage points in either direction from the percentage that would be found by interviewing all undergraduates.



### Finding the Point estimate and *E* from a confidence interval 

$$\hat{p}=\frac{\text{upper confidence limit + lower confidence limit}}{2}$$
$$E=\frac{\text{upper confidence limit - lower confidence limit }}{2}$$

#### example
- The article “High−Dose Nicotine Patch Therapy,” by Dale, Hurt, et al. (Journal of the American Medical Association, Vol. 274, No. 17) includes this statement: “Of the 71 subjects, 70% were abstinent from smoking at 8 weeks (95% confidence interval {CI}, 58% to 81%).” Use that statement to find the point estimate and the margin of error E.

$$\hat{p} = \frac{0.81+0.58}{2} = 0.695$$
$$E = \frac{0.81-0.58}{2} =0.115$$


### Finding the Sample size Required to estimate a Population Proportion
- when planning to collect data in order to estimate about a population, we have to determine the *sample size*
- when rounding, round to **nearest whole number up**

When estimate of $\hat{p}$ is known:
$$n = \frac{Z^2\hat{p}\hat{q}}{E^2}$$
When estimate of $\hat{p}$ is **un**known:
$$n = \frac{[Z_{a/2}]^20.25}{E^2}$$

#### Example
-  2016 Pew Research Center survey of 4787 randomly selected U.S. adults showed that 79% of the respondents shop online. If we want to conduct a new survey to determine whether that percentage has changed, how many adults must be surveyed in order to be 95% confident that the sample percentage is in error by no more than (3%) three percentage points?

$Z = 0.95 (zscore)=> 1.96$
$\hat{p} = 0.79$
$\hat{q} = 1-0.79 = 0.21$
$E = 0.03$

a. Assume that 79% of adults make online purchases.
$$n = \frac{Z^2\hat{p}\hat{q}}{E^2} = \frac{1.96^2(0.79)(0.21)}{0.03^2} = 708.135 = 709$$
- we need to obtain a simple random sample that includes **at least** 709 adults


b. Assume that we have no prior information suggesting a possible value of the population proportion.

$$n = \frac{[Z]^2\times0.25}{E^2} = \frac{1.96^2\times 0.25} {0.03^2} = 1067.11 = 1068 $$
- we need to obtain a simple random sample that includes **at least** 1068 adults (not knowing that population proportion)

### Coverage Probability 
- refers to the probability that a given statistical procedure will yield an estimate that contains the **true** parameter value (e.g., a population mean or proportion) within a certain range or interval.  
#### Example:

1. Suppose you have a population, and you want to estimate its mean. You take a sample and construct a confidence interval for the mean.
2. If you repeat this process 100 times, you would expect that about 95 of those 100 confidence intervals should contain the true population mean (if the confidence level is 95%).
3. If you construct a confidence interval and it **does not contain** the true mean, the coverage probability reflects the frequency with which such errors occur.


### Better performing confidence intervals

#### Plus 4 method
- better than Wald confidence
- coverage probability is closer to the confidence level being used 
- **Steps**
	- add 2 to number of successes *x*
	- add 2 to number of failures
	- then find Wald confidence Interval 

#### Wilson Score
- better than Wald, coverage probability is closer to confidence interval 
$$
CI_{\text{lower}} = \frac{\hat{p} + \frac{z_{\alpha/2}^2}{2n} - z_{\alpha/2} \sqrt{\hat{p}(1-\hat{p}) + \frac{z_{\alpha/2}^2}{4n}}}{1 + \frac{z_{\alpha/2}^2}{n}}
$$

$$
CI_{\text{upper}} = \frac{\hat{p} + \frac{z_{\alpha/2}^2}{2n} + z_{\alpha/2} \sqrt{\hat{p}(1-\hat{p}) + \frac{z_{\alpha/2}^2}{4n}}}{1 + \frac{z_{\alpha/2}^2}{n}}
$$

#### Clopper-Pearson 
- "exact method"
- based on exact binomial distribution instead of an approx of the distribution 
- considered **too conservative**

In the end, consider using the **plus 4 method** since it's just as easy as the Wald, and more accurate




## Estimating a Population Mean
- Requirements
	- sample is a simple random sample
	- either:
		- population is normally distributed 
		- or n > 30
- Round off rule
	- **original data set**
		- round one more decimal place than original data set
	- **Summary Stats**
		- round confidence interval limits to same number of deci places used for sample mean
### t distribution
$$t =\frac{\bar{x}-\mu}{\frac{s}{\sqrt{n}}}$$

#### key points about t distribution 
 - Finding the critical values requires a value of **Degrees of freedom** 
	 - n-1 = DF  
 - t distribution varies based on sample size

### Procedure for constructing a Confidence interval for $\mu$
- sample is simple random sample
- normally distributed population 
- n > 30

### Confidence Interval for population mean 

the general formula for constructing a confidence interval for the population mean $\mu$:
$$ \text{confidence interval}= \bar{x}\pm t_{a/2}\times\frac{s}{\sqrt{n}} $$
- $\bar{x}$ = sample mean
- $s$ = sample standard dev
- $n$ = sample size
- $t_{a/2}$ = desired confidence interval 


#### Sample Standard Deviation
	$$S = \sqrt{\frac{\sum(x_i-\bar{x})^2}{n-1}}$$


#### Example
- Listed below are weights (grams) of randomly selected Reese’s Peanut Butter Cups Miniatures. They are from a package of 38 cups, and the package label states that the total weight is 12 oz, or 340.2 g. If the 38 cups have a total weight of 340.2 g, then the cups should have a mean weight  ($\bar{x}$) 340.2 g/38 = 8.953 g.

- 8.639.  8.689   8.548   8.980   8.936   9.042

**solution** 

find the sample mean $\bar{x}$ = 
$\bar{x} = 8.839 + 8.689+8.548+8.980+8.936+9.042 = 52.834/2 \approx 8.806g$

calculate the sample standard deviation $s$:
$$S = \sqrt{\frac{\sum(x_i-\bar{x})^2}{n-1}} $$

| $X_i$ - | $\bar{X}$ | =      | $x^2$  | $\sum$     |
| ------- | --------- | ------ | ------ | ---------- |
| 8.839   | 8.806     | -0.167 | 0.0279 |            |
| 8.689   |           | -0.117 | 0.0137 |            |
| 8.980   |           | -0.258 | 0.0665 |            |
| ...     |           | ...    | ...    | ...        |
|         |           |        |        | **0.2109** |
$$S = \sqrt{\frac{0.2109}{6-1}} = 0.205g$$

find the critical value for $t_{a/2}$:
- assuming 95% confidence, look up values of $t_{a/2}$ for $a$ = 0.05
- $df$ = 6-1 = 5 
-  use t-distribution table or calculator to find critical value = **2.571**
- $t_{a/2} = 2.571$
Next find the margin of error:
$$E = t_{a/2}\times\frac{s}{\sqrt{n}} = 2.571 \times\frac{0.205}{\sqrt6} \approx 0.215g$$
Therefore:
- we are 95% confident that the true mean of the cups is within $\pm0.215g$ of the sample mean ($8.806g$).
-  confidence interval is $(0.851,9.021)$




### Estimating the Population mean when $\sigma$ is known
- if we somehow know the value of $\sigma$, the confidence interval is constructed using **standard normal distribution** instead of t-distribution. so the same procedure can used for the margin of error
$$E = z_{a/2}\times\frac{\sigma}{\sqrt{n}}$$

#### Choosing the correct Distribution
![[Pasted image 20241118131749.png]]


### Finding the Sample size required to estimate a Population Mean
- find $n$ to estimate the value of a population mean $\mu$
- round to the next higher whole number
**Notation**
$\mu$ = population mean
$\sigma$ = population standard deviation
 $\bar{x}$= sample mean
 $E$= desired margin of error
$Z_{a/2}$ = z-score separating the right tail of the standard normal distribution

$$n = (\frac{Z_{a/2}\times\sigma}{E})^2$$


### Dealing with Unknown $\sigma$ When Finding Sample Size
##### Range Rule of Thumb 
- $\sigma\approx\text{range}/4$ | where range is determined from sample data 

##### Start and improve
- start sample collection process without knowing $\sigma$, using the first several values to calculate sample standard deviation $S$  

#### Example
Assume that we want to estimate the mean IQ score for the population of statistics students. How many statistics students must be randomly selected for IQ tests if we want 95% confidence that the sample mean is within 3 IQ points of the population mean?

confidence interval = 0.95
margin of error = 3
and a assumed standard deviation of 15 (for IQ points)

$$n = (\frac{Z_{a/2}\times\sigma}{E})^2 = n = (\frac{1.96\times15}{3})^2 = 9.8^2 \approx 97 $$
- To estimate the mean IQ score of statistics students with 95% confidence and a margin of error of 3 IQ points, you would need to survey **at least 97 students**.
