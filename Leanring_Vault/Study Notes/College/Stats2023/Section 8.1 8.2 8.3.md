## Hypothesis Testing 
1. make assumption about population 
2. use sample to test assumption 
 
**hypothesis** - a premise or claim that we want to test
**null hypothesis** - $H_o$ currently accepted value for a parameter ; the default assumption 
**alternative Hypothesis** -  $H_a$ aka the research hypothesis, involves the claim to be tested.

###### Example
- it is believed that a candy machine makes chocolate bars that are 5g on average. A worker claims that the machine after maintenance no longer makes 5g bars. Write $H_o$ and $H_a$
	- $H_o$ : $\mu=5g$
	- $H_a$ : $\mu\neq5g$

**test statistic** -  calculated from sample data and used to decide the conclusion

**statistically significant** = where do we draw the line to make a decision?

**level of confidence** - C = 95%, 99%
- how confident are we in our decision 
**level of significance** - $a=1-C$
- if LoC (lvl of confid.) = .95
- $a=1-.95=0.05$

### Determining the type of test

$>$ points to the right, right tailed
$<$ points to the left, left tailed
$\neq$ used for 2 tailed test

### General steps of hypothesis testing
#### create hypothesis
- $H_O$ = Null Hypothesis
	- what we assume about the population
	- opposite of $H_a$  
- $H_a$ = Alternative Hypothesis
	- what we test about population
#### check conditions
- being a random sample
- being normally distributed 
- n > 30
- etc.
#### calculate 
- test statistic  = standardized value for $\overline{x}$ or $\hat{p}$

#### compare
- critical value = standardized value for $a$ value
- $a$ value  = probability threshold
![[Pasted image 20241121125826.png]]
#### conclude
 1. reject the null hypothesis $H_o$
 2. fail to reject $H_o$
	- if p is low, reject $H_o$

### Examples

A company has stated that their straw machine makes straws that are 4mm diameter. A worker believes the machine no longer makes straws of this size and samples 100 straws to preform a hypothesis test with 99% confidence.
- $H_o:\mu=4mm$
- $H_a:\mu\neq4mm$
- $n=100$
- $C=0.99$
- $a = 1-C = 1-.99=.01=a$

Doctors believe that the average teen sleeps on average no longer than 10 hours per day. A researcher believes that teens on average sleep longer. Find $H_o$ and $H_a$
- $H_o: \mu \leq 10$
- $H_a: \mu > 10$

The school board claims that at least 60% of students bring a phone to school. Teacher believes this number is too high and randomly samples 25 students to test at a level of significance of 0.02.
-  $H_o: p \geq 0.60$
- $H_a: P < 0.60$
- $n=25$
- $a=0.02$

- $C=1-a=1-0.02=0.98=C$


A factory has a machine that dispenses 80mL of fluid. Employee thinks its not 80mL. Using 40 samples, measures avg amount to be 78mL with SD 2.5. 
- State the null and alternative hypotheses.  
$H_o: \mu = 80$
$H_a: \mu \neq 80$
- At 95% confidence, is there enough evidence to support the idea that the machine isn't working properly?
	- *conduct a two tail test*
![[Pasted image 20241121135847.png]]

$\overline{x}=78$
$\mu_0=80$
$s=2.5$
$n=40$

$$z=\frac{\overline{x}-\mu_0}{\frac{s}{\sqrt{n}}} = \frac{78-80}{\frac{2.5}{\sqrt{40}}} = -5.06$$
- notice that -5.06 is in the far left shaded area, in the rejection region

With a 95% level of confidence we cannot accept the null hypothesis that the avg amount of fluid is 80mL. 

### Type I and Type II Errors

Type I = occurs when we **reject the null hypothesis** when it is actually true
Type II = occurs when we fail to **reject the null hypothesis** when it is actually false

## Testing a Claim about a Proportion 
- the method in this section can be used with claims about population proportions, probabilities, or the decimal equivalents of percentages.

### Normal approximation method
- conduct a formal hypothesis test of a claim about a population proportion *p*.\

**notation**
- $n =$ sample size
- $p=$ population proportion (the value used in the statement of the null hypothesis)
- $\hat{p}=\frac{x}{n}$ sample proportion
- $q=1-p$

**requirements**
- sample observations are simple random sample
- is binomial distribution
	- fixed number of trails
	- trails are indep.
	- has "success" and "failure"
	- prob of success remains the same in all trails
- the condition $np\geq5$ and $nq\geq5$ are both satisfied
	- binomial distr. can be approximated by normal distr. with $\mu=np$ and $\sigma=\sqrt{npq}$

#### Test Statistic for Testing a Claim about a Proportion
$$z = \frac{\hat{p}-p}{\sqrt{\frac{pq}{n}}}$$

**P-values and critical values** = use standard normal distr. table (Table A-2)

#### Example
- A researcher claims that based on the information obtained from the Centers for Disease Control and Prevention, 17% of young people ages 2–19 are obese. To test this claim, she randomly selected 200 people ages 2–19 and found that 42 were obese. At α = 0.05, is there enough evidence to reject the claim?
**step 1**
$H_o:p=0.17$
$H_a:p\neq0.17$
$p=0.17$
$\hat{p}=\frac{obese}{total}=\frac{42}{200}=0.21$
$n=200$
$a=0.05$

**step 2**
$$z_c = \frac{\hat{p}-p}{\sqrt{\frac{pq}{n}}} = \frac{0.21-0.17}{\sqrt{\frac{0.17\times0.83}{200}}} \approx 1.505$$
**step 3**
for a two tailed test with $a=0.05$, the critical z-values are $\pm 1.96$
- $a/2 = 0.025, 1-0.025 = .975$ (Z-score table) => 1.96

**step 4**
since our $z_c$ (test statistic) is less than the critical value 1.96 (or behind -1.96), **we fail to reject the null hypothesis.**



#### Example 2
An attorney claims that more than 25% of all lawyers advertise. A random sample of 200 lawyers in a certain city showed that 63 had used some form of advertising. At α = 0.05, is there enough evidence to support the attorney’s claim? Use the P-value method.

$H_o:p=0.25$
$H_a:p>0.25$
$\hat{p}=\frac{63}{200}=0.315$
$n=200$
$a= 0.05$ 

**step 1**
calculate the test statistic
$$z_c = \frac{\hat{p}-p}{\sqrt{\frac{pq}{n}}} \approx2.12$$
**step 2**
find the P value

Since the alternative hypothesis is $p>0.25$, this is a **one-tailed test**. 
To find the P-value, we look up the z-value of 2.12 in the standard normal distribution table (or use a calculator).
The corresponding area to the left of $z=2.12$ is approximately $0.9830$. Since we're testing for a greater proportion, the P-value is:

$P(z>2.12)=1−0.9830=0.0170$

**step 3**
$P=0.017 < a= 0.05$

Since the P-value (0.0170) is less than the significance level (0.05), we **reject the null hypothesis**. There is enough evidence to support the attorney's claim that more than 25% of lawyers advertise.


#### Example 3
A report stated that 21% of babies are delivered by Caesarean section. A researcher believes that the percentage is less than 21% in the large hospital in his hometown. He randomly selected 50 newborn infants and found that 8 were born by Caesarean section. At α = 0.01, is there enough evidence to support his claim?

$H_o:p=0.21$
$H_a:p>0.21$
$\hat{p}=\frac{8}{50}=0.16$
$n=50$
$\alpha= 0.01$

**step 1**
calculate the test statistic
$$z_c = \frac{\hat{p}-p}{\sqrt{\frac{pq}{n}}} \approx-0.868$$

**step 2**
find p-value

p<0.21, this is a **left-tailed test**.
To find the P-value, we need to look up the z-value of $−0.868$ in the standard normal distribution table or use a calculator.
corresponding area to left of $z=-0.868$ is approx $0.1924$
$P=0.1924$

The significance level $\alpha = 0.01$. If the P-value is less than $\alpha$, we reject the null hypothesis.

$P=0.1924 >\alpha=0.01$

**step 3**

Since the P-value (0.1924) is greater than the significance level (0.01), we **fail to reject the null hypothesis**. There is not enough evidence to support the claim that the percentage of babies born by Caesarean section is less than 21% in the hospital.



## Testing a Claim About a Mean

### Testing claims about a population mean with $\sigma$ not known

**notation**
$n$ = sample size
$\bar{x}$ = sample mean
$s$ = sample standard deviation
$\mu_{\bar{x}}$ = population mean

**requirements**
- sample is simple random 
- either or both of these conditions:
	- population normally distributed 
	- n>30

#### Equation
$$t=\frac{\bar{x}-\mu_{\bar{x}}}{\frac{s}{\sqrt{n}}}$$

#### Requirements of Normality or n>30
- if not normally distributed, n>30 for justifying
- Sample sizes of 15-30 are sufficient if the population has a distribution that is not far from normal

![[Pasted image 20241122141835.png]]


#### Examples

Find the critical t value for $\alpha$ = 0.05 with df = 16 for a **right-tailed** t test.

$t_a=1.746$


Find the critical t value for α = 0.01 with d.f. = 24 for a left-tailed t test.
$2.492$ on the table => $-2.492$

Find the critical values for α = 0.10 with d.f. = 18 for a two-tailed t test
$\pm1.734$


#### The Traditional Method
- state hypothesis, identify claim
- find critical values
- compute the test value
- make the decision to reject or not reject the null 
- summarize the results

##### Example
A medical investigation claims that the average number of infections per week at a hospital in southwestern Pennsylvania is 16.3. A random sample of 10 weeks had a mean number of 17.7 infections. The sample standard deviation is 1.8. Is there enough evidence to reject the investigator’s claim at α = 0.05? Assume the variable is normally distributed.
$$
H_0:\mu=16.3,
H_1:\mu\neq16.3;
\mu = 16.3,
n = 10,
\overline{x} = 17.7,
s  = 1.8,
\alpha = 0.05
$$

**step 1**
test statistic 

$$t=\frac{\bar{x}-\mu_{\bar{x}}}{\frac{s}{\sqrt{n}}}= \frac{17.7-16.3}{\frac{1.8}{\sqrt{10}}} \approx2.46$$

**step 2**
find critical value
**two tailed** since no specific direction of being greater or less than. is or is not
$\alpha=0.05$, $df=9$
$t=\pm2.262$

**step 3**
compare $t$ to test statistic 
calculated t-statistic = $2.52$
critical t-value = $\pm2.262$

$t>\text{test statistic}$ 

Since the calculated t-statistic (2.52) is **greater** than the critical t-value (1.761), we **reject the null hypothesis**.

At$\alpha = 0.05$, there is enough evidence to reject the investigator's claim that the average number of infections per week is 16.3. The data suggests that the average number of infections is different from 16.3 (either higher or lower).




#### The P value Method
- state the hypothesis, identify claim
- compute the test value
- find P value
- make decision
- summarize the results

##### Example
A physician claims that joggers’ maximal volume oxygen uptake is greater than the average of all adults. A *random sample of 15 joggers* has a **mean of 40.6** milliliters per kilogram (ml/kg) and a *standard deviation of 6* ml/kg. If the average of all adults is 36.7 ml/kg, is there enough evidence to support the physician’s claim at α = 0.05? Assume the variable is normally distributed.

$H_o:\mu=36.7$
$H_a:\mu>36.7$
$\overline{x}=40.6$ | sample mean
$\mu_0 = 36.7$ | population mean
$s=6$ | SD
$n=15$
$\alpha= 0.05$

**step 1**
calculate test statistic 
$$t=\frac{\bar{x}-\mu_{\bar{x}}}{\frac{s}{\sqrt{n}}} = \frac{40.6-36.7}{\frac{6}{
\sqrt{15}}}\approx2.52$$

**step 2**
find critical t-value

**right tailed test**, because physician claims that jobbers have a greater maximal oxygen uptake.
given $\alpha = 0.05$ and df = (n-1) = 14:

$t=1.761$

**step 3** 
compare $t$ to test statistic 

$t>\text{test statistic}$ 
at $\alpha = 0.05$, we reject the null hypothesis, and that there is enough evidence to support the claim that joggers' max volume oxygen uptake is greater than avg of all adults.


