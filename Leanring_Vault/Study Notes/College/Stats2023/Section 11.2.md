## Goodness of fit and Contingency Tables
**contingency table** - (two way freq table) table consisting of frequency counts of categorical data corresponding to two different variables. (One variable is used to categorize rows, and a second variable is used to categorize columns

**test of independence** - we test the null hypothesis that in a contingency table, the row and column variables are independent. (That is, there is no dependency between the row variable and the column variable.)

### Notation
***O*** = observed frequency in a cell inside table
***E*** = expected frequency in cell ; found by assuming that row and column vars are indep 
***r*** = number of rows
***c*** = number of columns

### Requirements
- sample data is randomly selected
- sample data represented as frequency counts in a two-way table
- for every cell, expected frequency **E*** is at least 5  
	- (There is no requirement that every observed frequency must be at least 5.)

### Null and Alternative Hypothesis
$H_0$= rows and column variables are **independent**
$H_1$ = rows and columns variables are **dependent**

## Test Statistic for Test of Indep
$$x^2 = \sum{\frac{(O-E)^2}{E}}$$
*where O is observed freq in a cell, and E is the expected freq, found by:*
$$E = \frac{(\text{row total})(\text{column total})}{\text{grand total}}$$

### P value and Critical Value
P value  = A-4 table

Critical Values = DF = $(r-1)(c-1)$

tests of independence with contingency tables are always **right tailed**

## Relationship among Key Components in a Test of Independence 
![[Pasted image 20241202141735.png]]

### Example
The contingency table contains the data relating autism and the measles vaccine. Also included are the row totals and column totals. 
- Find the expected frequency E for the cell with an observed frequency of 25.

|           | Unvaccinated | Vaccinated | *Total*    |
| --------- | ------------ | ---------- | ---------- |
| Autism    | 25 (E = ?)   | 64         | ***89***   |
| No Autism | 362          | 1427       | ***1789*** |
| *Total*   | ***387***    | ***1491*** | **1878**   |

$$E = \frac{(\text{row total})(\text{column total})}{\text{grand total}} = \frac{(89)(387)}{(1878)} = 18.340 = E$$
The **expected** frequency for the cell with an observed frequency is = 18.340