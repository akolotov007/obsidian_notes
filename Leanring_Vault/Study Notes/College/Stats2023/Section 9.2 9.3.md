Inference from Two Samples 
## Two means: independent samples

Two samples are **independent** if the values from one population are not related to the sample values of the other population

Two samples are **dependent** (or consist of matched pairs) if the sample values are somehow matched, where the matching is based on some inherent relationship.

### Objectives
Hypothesis Test
- hypothesis about two indep. population means
Confidence Interval 
- confidence interval estimate of the difference between two indep. population means


### Notation
For population 1:
$\mu_1 =$ **population** mean
$\sigma_1 =$ **population** standard deviation
$n_1 =$ size
$\overline{x}_1 =$ **sample** mean
$s1 =$ **sample** deviation

### Requirements


1. The values of $\sigma_1$ and $\sigma_2$ are unknown and we do not assume that they are equal.
2. The two samples are independent.
3. Both samples are simple random samples.
4. Either or both of these conditions are satisfied: 
	-  The two sample sizes are both large (with n1 > 30 and n2 > 30) 
	- both samples come from populations having normal distributions.

### Hypothesis Test Statistic For Two Means: Indep. Samples
(with $H_0:\mu_1=\mu_2$)

$$t=\frac{(\overline{x}_1-\overline{x}_2)-(\mu_1-\mu_2)}{\sqrt{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}}$$
*where $\mu_1-\mu_2$ is often assumed to be 0*


### Confidence Interval Estimate: Indep. Samples
the confidence interval estimate of the difference $\mu_1-\mu_2$ is:
$$(\overline{x}_1 - \overline{x}_2)-E<(\overline{x}_1 - \overline{x}_2)<(\overline{x}_1 - \overline{x}_2)+E$$

where $E$:
$$E = t_{a/2}\sqrt{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}$$
and df = smaller of $n_1$-1 and $n_2$-1

### Equivalent Methods
- P-value, critical value, and confidence interval all use same distribution and standard error, so they are all equivalent in the sense that they result in the same conclusions


### Example:
A study was done to see if there is a difference between the number of sick days men take and the number of sick days women take. A random sample of 9 men found that the mean of the number of sick days taken was 5.5. The standard deviation of the sample was 1.23. A random sample of 7 women found that the mean was 4.3 days and a standard deviation of 1.19 days. At α = 0.05, can it be concluded that there is a difference in the means?

$H_0: \mu_1=\mu_2$
$H_1: \mu_1\neq\mu_2$


men:
- $n_1$: 9 
- $\overline{x}_1=$ 5.5
- $s_1$ = 1.23

women:
- $n_2$: 7
- $\overline{x}_2=$ : 4.3
- $s_2$ = 1.19

at $\alpha = 0.05$


$$t=\frac{(\overline{x}_1-\overline{x}_2)-(\mu_1-\mu_2)}{\sqrt{\frac{s^2_1}{n_1}+\frac{s^2_2}{n_2}}}=\frac{(5.5-4.3)}{\sqrt{\frac{1.23^2}{9}+\frac{1.19^2}{7}}} \approx1.97$$


## Two Dependent Samples (Matched Pairs)
pairs must be matched according to some relationship, such as before/after measurements from the same subjects, or measured and reported weights from sample of subjects

### Notation
$d$ = individual difference between the two values in a single matched pair 
$\mu_d$ = mean value of the differences *d* for the **population** of all matched pairs of data
$\overline{d}$ = mean value of the differences *d* for the paired **sample** data
$S_d$ = standard deviation of the differences *d* for the pair **sample** data
$n$ = number of **pairs** of sample data

### Requirements
- Sample data are dependent
- the matched pairs are simple random sample
- either
	- n > 30
	- the pairs of values have differences that are from a population having a distribution that is approx normal

### Test statistic for Dependent Sample
$$t = \frac{\overline{d}-\mu_d}{\frac{S_d}{\sqrt{n}}}$$
### Confidence Intervals for dependent samples

$$\overline{d}-E < \mu_d < \overline{d}+E$$
$$E = t_{a/2}\frac{s_d}{\sqrt{n}}$$

### Example
It is a common belief that if you ask someone how much they weigh, you tend to get a number that is somewhat lower than the number that you would get by using a scale to actually weigh them. Listed on the next slide are measured and reported weights (lb) of random male subjects (from Data Set 4 “Measured and Reported” in Appendix B). Use a 0.05 significance level to test the claim that for males, the measured weights tend to be higher than the reported weights.

 
| subject         | 1     | 2     | 3     | 4     | 5     | 6     | 7     | 8     |
| --------------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| measured weight | 152.6 | 149.3 | 174.8 | 119.5 | 194.9 | 180.3 | 215.4 | 329.6 |
| reported weight | 150   | 148   | 170   | 119   | 185   | 180   | 224   | 239   |

**step 1**
The claim that the measure weights tend to be higher than the reported weights can be expressed as:
$\mu_d> 0 lb$

then our other test would be:
$\mu_d<0 lb$

**step 2**
find mean of differences:

| subject         | 1     | 2     | 3     | 4     | 5     | 6     | 7     | 8     |
| --------------- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| measured weight | 152.6 | 149.3 | 174.8 | 119.5 | 194.9 | 180.3 | 215.4 | 239.6 |
| reported weight | 150   | 148   | 170   | 119   | 185   | 180   | 224   | 239   |
| Difference      | 2.6   | 1.3   | 4.8   | 0.5   | 9.9   | 0.3   | -8.6  | 0.6   |
$\overline{d}=\frac{2.6+1.3+4.8+0.5+9.9+0.3-8.6+0.6}{8} = 1.425$

**step 3**
find standard deviation of differences

$\sum(\text{individual point} -\text{mean})^2$
- (2.6−1.425)2=1.365625
- (1.3−1.425)2=0.015625
- (1.3 - 1.425)^2 = 0.015625
- (1.3−1.425)2=0.015625
- (4.8−1.425)2=11.3025
- (4.8 - 1.425)^2 = 11.3025
- (4.8−1.425)2=11.3025
- (0.5−1.425)2=0.855625
- (0.5 - 1.425)^2 = 0.855625
- (0.5−1.425)2=0.855625
- (9.9−1.425)2=71.9025
- (9.9 - 1.425)^2 = 71.9025
- (9.9−1.425)2=71.9025
- (0.3−1.425)2=1.265625
- (0.3 - 1.425)^2 = 1.265625
- (0.3−1.425)2=1.265625
- (−8.6−1.425)2=101.3025
- (-8.6 - 1.425)^2 = 101.3025
- (−8.6−1.425)2=101.3025
- (0.6−1.425)2=0.690625
- (0.6 - 1.425)^2 = 0.690625
- (0.6−1.425)2=0.690625
++ = 188.7
$s^2_d = \frac{188.7}{7} = 26.9571$
$s_d = \sqrt{26.9571} \approx 5.19$


**step 4**
found mean and SD, preform t-test statistic (value we use to compare):
$t_{a/2} = \frac{1.425}{5.19/\sqrt{8}} = \frac{1.425}{1.833}\approx0.777$

**step 5**
find critical value
for one tailed test at 0.05 significance level with $n-1 = 7$ degrees of freedom (df),

critical value ($t$)= 1.895

**step 6**
compare t-statistic vs. critical value 

$0.777 < 1.895$
therefore, we **fail to reject** the null hypothesis. there is **insufficient evidence** to support the claim that measured weights tend to be higher than the reported weights. results do not show a significant difference

