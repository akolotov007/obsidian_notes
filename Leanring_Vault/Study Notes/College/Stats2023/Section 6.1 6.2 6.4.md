Resources; https://www.youtube.com/watch?v=CjF_yQ2N638 = organic chemo tutor, Standard Normal Distribution Table 
## Section 6.1

### Uniform Distribution
- area under the graph of a continuous probability distribution =1
- a continuous random variable has **uniform distribution** if its values are equally spread over the range of possibilities


### Density Curve
- the graph of any continuous probability distribution is called a density curve
	- because the total area under any density curve is = 1, there is correspondence btwn area and probability ^1


#### Example
- During certain time periods at JFK airport in New York City, passengers arriving at the security checkpoint have waiting times that are uniformly distributed between 0 minutes and 5 minutes, as illustrated in the figure on the next page.
	- A. given the uniform distribution illustrated in the figure,the find the probability that a randomly selected passenger has a waiting time of at least 2 minutes.

![[Pasted image 20241106123118.png]]
- wait time can be any value btwn 0 and 5 
- make the height of the vertical line in a uniform distribution = $\frac{1}{\text{range}}$

**Solution** A
- the shaded area represents waiting times of at least 2 minutes. Knowing that there is correspondence btwn area and probability, easily find probability using **areas** ^1
	- P(wait time of at least 2 min) = height * width of shaded area = 1


### Standard Normal Distribution
 - a specific normal distribution having 3 properties:
	 - bell shaped 
	 - $\mu = 0$
	 - $\sigma = 1$
	 - total area under density curve = 1

![[Pasted image 20241106124308.png]]
#### Find Probabilities when given Z score
- Use technology
- Use Table
	- only used for standard normal distribution

#### Example
- A bone mineral density test can be helpful in identifying the presence or susceptibility to osteoporosis, a disease that causes bones to become more fragile and more likely to break. The result of a bone density test is commonly measured as a z score. The population of z scores is normally distributed with a mean of 0 and a standard deviation of 1, so these test results meet the requirements of a standard normal distribution.
	- A randomly selected adult undergoes a bone density test. Find the probability that this person has a bone density test score less than 1.27.

**Solution**
- in Excel:
	- `=NORM.DIST(1,27,0,1,1)`
		- find cumulative area **left** of the z-score
- = 0.8980
	- 89.90% of people have bone density levels below 1.27

- in Ti 84:
	- 2nd, distr menu
	- normal cdf
	- fill in data
	- ![[Pasted image 20241106130648.png]]

### Notations
- $P(a<z<b)$ 
- $P(z<a)$ 
- $P(z>a)$

### Critical Values
- a z-score on the borderline separating those z-scores that are **significantly low** or **significantly high**

#### Notation - $z_a$ z-score with area $a$ to its right
Example
- find value of $z_{0.025}$


## Section 6.2
$$Z = \frac{x-\mu}{\sigma}$$
- the formula allows to "standardize" any normal distribution so that *x* values can be transformed to z scores

![[Pasted image 20241106132620.png]]

### Example
- Heights of men are normally distributed with a mean of 68.6 in. and a standard deviation of 2.8 in. Find the percentage of men who are taller than a showerhead at 72 in.

**Solution**
$$ Z = \frac{72-68.6}{2.8} = 1.214$$
z score = 1.214, find cumulative probability (z-score table or Ti84)
- with T-84 plus
	- `normalcdf(lower,upper,mean,SD)`
	- `normalcdf(-1e99, 1.214 (z-score is upper bound), 0, 1)`

$\approx$ 88.76% / left of z-score, find right side:
1 - .8876 = 0.1124
$\approx$ 11.24% of men are taller than a showerhead of 72 inches


## Section 6.4
https://www.youtube.com/watch?v=4YLtvNeRIrg&list=PL0o_zxa4K1BVsziIRdfv4Hl4UIqDZhXWV&index=62 | organic chem tutor, central limit theorem 
## The Central Limit Theorem
- for all sample of the same size *n* with *n*>30, the sampling distribution of  (x means) $\overline{x}$ can be approximated by normal distribution with mean $\mu$  and a standard deviation of $\frac{\sigma}{\sqrt{n}}$
	- if the sample size is large enough, the sample distribution taken from any population distribution regardless of its shape will approximate a normal distribution

#### some equations
$$\mu_{\overline{x}} = \mu \text{ | mean of all values of }\overline{x}$$
$$ \sigma_{\overline{x}}= \frac{\sigma}{\sqrt{n}}\text{ | Standard Dev. of all values of }\overline{x}$$
$$Z = \frac{\overline{x}-\mu}{\frac{\sigma}{\sqrt{n}}}\text{ | Z score conversion of } \overline{x}$$
### Checking requirements
- when working with the mean from a sample, verify that the normal distribution can be used by confirming that the original population has a normal distribution **or** the sample size is *n*>30.


### Example
- American Airlines uses Boeing 737 jets with 126 seats in the main cabin. In an attempt to create more room, an engineer is considering a reduction of the seat width from 16.6 in. to 16.0. in. Adult males have hip widths that are normally distributed with a mean of 14.3 in. and a standard deviation of 0.9 in. (based on data from Applied Ergonomics).
- A) Find the probability that a randomly selected adult male has a hip width greater than the seat width of 16.0 in.
- B) Find the probability that 126 main cabin seats are all occupied by males with a **mean hip width** greater than the seat width of 16.0 in.

**Solution**
A) find randomly selected adult has greater width than 16in
- $X = 16,\mu=14.3,\sigma=0.9$
- $$Z = \frac{X-\mu}{\sigma} =  \frac{16-14.3}{0.9} = 1.89$$
- Z = 1.89 (Z-table or tech) $\approx0.9706$
-  $P(X>16) = 1 - P(X>16) = 1-0.9706 =0.294$
- the probability of selecting a male with a hip width greater than 16 inches is: 2.94% 





B "Find the probability that 126 main cabin seats are all occupied by males with a **mean hip width** greater than the seat width of 16.0 in."

- $n = 126, \overline{x} = 16,\mu=14.3,\sigma=0.9$ 
- $P(\overline{x}>16.0) = P(Z = \frac{\overline{x}-\mu}{\frac{\sigma}{\sqrt{n}}})$
- $$P(Z = \frac{16-14.3}{\frac{0.9}{\sqrt{126}}}) = P(Z>21.21)$$
- Z score = 21.21 (table or tech) $\approx1$
- find complement (to the right of the graph)
- 1-1= 0 
	- statistically highly unlikely

