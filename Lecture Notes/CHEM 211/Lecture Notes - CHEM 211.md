Class Code: #CHEM211
***
# Tuesday, Sep 12, 2023
Topic: **General Statistics**
## Todo/Assignments

- [ ] Bonus Marks for Excel Funny Time 🔼 ➕ 2023-09-12
- [ ] Tutorial Pre-...lab? 📅 2023-09-18
## Notes

#### Smarties

Statistics!

- 4 Yellow
- 2 Blue
- 2 Pink
- 1 Purple
- 9 Total

## Statistics Notes
#### Normal Distribution of data in a sample
- Values will cluster around the mean in a predictable distribution
	- Only with random errors
- Gaussian

#### Standard Deviation
- $\sigma$ is the true standard deviation of an infinite dataset
- Sample SD (s) is the closeness of the cluster in a limited dataset
- Variance is $s^{2}$
- %Relative SD (%RSD = $\frac{s}{mean} * 100$)
- $s = \sqrt{\frac{\Sigma (x_{i} - \bar{x})^2}{n-1}}$
- Triplicate is the minimum
- Small tiny baby error bars are probably not all that good, usually.

#### Standard Error
$s_{\bar{x}} = \frac{s}{\sqrt{n}}$
- Experiment with Error Bars

#### % Relative Standard Deviation
$\text{\% RSD} = \frac{s}{mean}\cdot 100$
- Smartie factory doesn't try to put the same number of colours or smarties in the box.

# Thursday, Sep 14, 2023
Topic: **Statistical Significance**

## Todo/Assignments
N/A

## Notes

### How do you know if 2 things are the same or different?

#### What do we need?

- Normal Data
- Hypothesis
	- 5% chance the things are the same,
	- 95% chance the things are different
	- (Confidence Interval)
	- Null: Means of two sets are not different within a confidence interval of 5%

#### Confidence Interval

- Each side is called a Confidence Limit
- How to choose them is a value judgement
	- Inherent Bias

#### Student's t-test

- Plot two gaussian curves,
- Calculate the difference between them
- Significant difference
	- Probability that the next measurement will fall within the CI of the control OR treatment, but not both.
	- $P \lt 0.05$ or $P = 0.05$
	- $\frac{1}{20}$ chance of a Type 1 error. (False Positive)
- Push in Medical Literature to go from 95% $\rightarrow$ 99%
- Most of the time there isn't enough data
	- Calculated mean $\bar{X}$ and STD $s$ from a finite number of samples
	- Real mean and STD might be different if you had more data
	- t-factor $\rightarrow$ Extrapolation to infinite dataset
- Deals with problems in small datasets

Treatment vs Control group
- Different t value for each degrees of freedom and CI.
- If calc is less than in table, then it is statistically different
- Not calculating t by hand.

Equal variance = same test same way on all samples; vitamin C in oranges and limes with same methods
Unequal variance = male vs. female, not the same, no reason to expect that they respond in the same way

zzzzzzzzzz

t-val 1.9~~

t-stat
$P(T\le t)$ one-tailed

$P(T\le t)$ two-tailed

@TINV(Prob of Outlier, DoF)
@TINV(0.05, n)

##### One-Tailed vs. Two-Tailed

Two-tailed $\rightarrow$ Normal Data for both datasets
One-tailed $\rightarrow$ Experiment imposed a condition that forced the data in a direction.[^1]

[^1]: Miller, Miller, & Miller p. 45

Group of Results
CI = $\bar{x}\pm t \cdot s$

CI = $\bar{x}\pm t \cdot s^-_{x}$

#### F-test
Assesses random errors between two sets.
$$
F_{calculated}=\frac{s^2_{1}}{s^2_{2}}
$$

### How Many Replicates Do I Need?

Use t-value to determine n by solving for n

$$
n = \left( \frac{s}{z} \right)^{2} 
$$

$$
n = \left( \frac{s}{1.960} \right)^{2}
$$
Above for 95% confidence.

Estimate $s$ from preliminary data.

$$
n=\left( \frac{3.2}{1.960} \right)^2
$$
For prelim $s$ of 3.2.

Studies:
1. Efficacy of New Drug $\rightarrow$ MANY n
2. Environmental Assessment
3. Election Polling
4. Disease diagnosis $\rightarrow$ Likely 1 n...

#### Parametric Nonparametric Skew

Median $\rightarrow$ Middle
- Right???
- Look at it, is it in the middle?
- If it's normal, mean and median should be the same.

Bootstrapping[^2]
- Resamples the data to find the range of data that fits a normal distribution
1. Calculate mean and median
2. Calculate 95% CI around median
3. Plot histogram with % and cumulative %
4. Randomize data

[^2]: Miller, Miller & Miller pp. 193-94

### Correlation

Pearson Correlation Coefficient[^3]

You can correlate use of the internet with a LOT of things.

- [ ] Read Harris and Lucy Ch. 4
- [ ] Read Miller, Miller, & Miller Ch.3

[^3]: Miller, Miller & Miller pp. 124-28

### Accuracy vs. Precision

#### Accuracy
Likelihood that you captured the true value in your measurement.
Need to compare to a standard.

#### Precision
Data is closely clustered.
Measure by %RSD

#### Both?
Data is likely the true value, and you hit it every single time.

- [ ] Watch Video on Accuracy and Precision


