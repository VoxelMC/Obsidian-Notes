Class Code: #CHEM211
***
# Tuesday, Sep 12, 2023
Topic: **General Statistics**
## Todo/Assignments

- [x] Bonus Marks for Excel Funny Time 🔼 ➕ 2023-09-12 ✅ 2023-09-26
- [x] Tutorial Pre-...lab? 📅 2023-09-18 [completion:: Sep 19, 2023 @ 03:11 PM]
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

- [x] CheatGPT 📅 2023-09-15 [completion:: Sep 19, 2023 @ 03:11 PM]

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

[^1]: Miller, Miller & Miller p. 45

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

T-test
If table value is less than calculated, there is bias

# Tuesday, Sep 19, 2023
###### Topic: **...**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

Elizabeth Holmes

908 Devices Mass Spec
- Tiny paper mass spec

To determine whether or not something falls into a category, you have to capture your error first. 

### Types of Error [^4] [^5]  

#### Gross Error

So serious you abandon all hope and start again
- Instrumental failure,
- Lost sample,
- Solvent contamination.

#### Random Error

Causes replicate results to differ - *Precision*.
- Poor technique,
- Human factors.

### Systematic Error

Causes all results to be incorrect in the same way - *Accuracy*.
- Bias caused by human or instrument malfunction.

[^4]: Miller, Miller & Miller pp. 3-11
[^5]: Harris & Lucy, ch. 3, pp. 51-64

### Experiments - Human Error

All experiments have errors!

Humans are not robots
Robots are not perfect
Instruments fail
People make mistakes
Stuff happens

- [ ] Check overly honest methods on twitter.

You have to try to control error
- Spike some samples
- Double up on samples
- Send them blindly numbered
So that you can check the quality and compare the data you get out for error.

### Uncertainty

Sum of each possible errors

$$
\sqrt{ \sum (error_{1})^{2} (error_{2})^{2} + \dots + (error_{n})^2}
$$

### Error Types 1 and 2

#### Type 1

False Negative Data
Fail to detect something that is really there.

#### Type 2

False Positive Data
Detect something that is really NOT there.

### Can We Trust Scientists?

**What does it mean to publish data?**
Reviewer's word is law. Disagree? Retract and submit to another journal...

- [ ] Check out Retraction Watch Database`

**When is data bad?**
The biggest error is people.

Bad research is the *exception*. The vast majority of science is thorough and real. 
Incentives are a point of contention.

- [ ] In Defense of Plants Podcast by Melanie Jones on Mycorrhizal Fungi

# Thursday, Sep 21, 2023
###### Topic: **Chemometrics**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### How Do You Know if >2 Things are the Same or Different?

#### 1 Group

One way t-test to known value

#### 2 Groups

Two way paired t-test to compare to each other

#### >2 Groups

ANOVA

### What is Variance?

Square of the Standard Deviation.

An **ANOVA** analyses the variances of many groups of data.

#### Example:

**Water, OJ, and Coffee**
- Measure the minutes it takes someone to complete a task. (5 measurements).

Theoretically, the data looks like 3 bell curves with different means with different SD/Variances

Calculate the difference between the means, and calculate the area under the curve where the curves overlap with each other.

There is variance within the groups, and variance between the groups.

- [ ] Check lecture slides for ANOVA video.

F = variance between groups/variance within groups.

Which is F = difference between means / variance of the group.

***Complete Randomized Block***

|        | Men | Women |
| ------ | --- | ----- |
| Water  | 5   | 5     |
| Juice  | 5   | 5     |
| Coffee | 5   | 5     |

Ideal Minimum of Replicates for ANOVA is 5

One factor: Water, Juice, Coffee (One Variable)
Two factor: Water, Juice, Coffee and Men, Women (Two Variables)

- [ ] Miller, Miller & Miller Sec 3.8 to 3.10 and Ch 4.

### Chemometrics

**How to apply statistics in chemistry.**

To begin, you need a hypothesis: Testable by Statistics, Based on Previous Knowledge

Then, find a method, determine its limits, 

#### Replicate Types
Analytical - Different smarties all of the same colour
Biological - DIfferent smarties all of different colour
Pseudo - Analysis of several where each is different colour but colour doesnt matter
Bulk - A bunch of smarties mushed into one big sample
Sub - 

- [ ] HPLC Schematic will be on midterm

# Tuesday, Sep 26, 2023
###### Topic: **AI Tools and Chromatography**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Chromatography Columns
**Input $\rightarrow$ Frit $\rightarrow$ Stationary Phase $\rightarrow$ Frit $\rightarrow$ Output**

Stationary Phase is really really packed. Can handle really high pressure.

Small particles comprising the column packing increase speed of elution. Too small is bad though, leads to making concrete :)
$\rightarrow$ Literally bricked.

HPLC vs UPLC are different trade names. Different parameters.[^6]

[^6]: Table 25-2 in textbook.

- [ ] Watch old style HPLC video on Canvas.

### HPLC Pump

Sapphire tipped piston, ruby ball for one way valve.
### Normal Phase Chromatography

Silica Matrix
Elutes based on particle size.
*Larger first $\rightarrow$ Smaller last.*
-ve is repelled from beads, so elute first. +ve adsorbs, need acid or salt to release them.

Incredibly high surface area in a column.
Cannot be used above 8 pH

Somewhat less polar mobile phase
More polar $\rightarrow$ better eluent strength
Pentane = 0

Not that good

10% of the time
### Reverse Phase Chromatography

Non-polar stationary phase.
C18 column has SDS on beads of silica.

Used 80% of the time.

Detergent column. So, it holds onto stuff.

Many other matrix types:
Refer to [^7]

[^7]: Table 25-3

Establish an eluent gradient
A $\rightarrow$ Formic acid
B $\rightarrow$ Non-polar solvent
Go from A $\rightarrow$ B 
Over time, mix them together at different ratios, and all the molecules will come off of the column!

- [ ] HPLC Solvent Gradient Curve Programs??

Also, may eluents[^8]

[^8]: Table 25-4 in textbook

#### Isocratic -> Only One Solvent 

### Hydrophilic Interaction Chromatography (HILIC)

Stationary is strongly polar
Mobile phase is 60-97% acetonitrile mixed with aqueous buffer (mostly organic).

Put a coating around the beads of acetonitrile.
Layer of aq around that
Phase partitioning and diffusion

Low aq $\rightarrow$ High aq

Solves problems for sugars, because they are really polar and closely related. 

# Thursday, Sep 28, 2023
###### Topic: **Chromatography 2**
Lecture Link: 

## Todo/Assignments

- [ ]

## Notes

### Ion Exchange

All about charge!!
They tend to fall apart... e.g. stuff falls off of the beads.

#### Anion Exchange 

(+)ve Stationary Phase
So it exchanges anions.
Positive stuff goes right through.
- Organic Acids

#### Cation Exchange 

(-)ve Stationary Phase
So it exchanges cations.
Negative stuff goes right through.

### Molecular Exclusion

Big molecules first, smaller after. More ways for the smaller ones, less ways for the bigger ones.
Completely inert glass beads.

No chemistry! Just a big filter. 

### Affinity

Antibodies!!! Did or didn't. 

### Capillary Electrophoresis

### Gel Electrophoresis

### 

Remember what comes out first or last
What is the stationary phase do and how does it transfer stuff to the mobile phase.

# Tuesday, Oct 03, 2023
###### Topic: **...**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Baby Foot Blood

Half a microlitre $\times$ 3 replicates. You have to get the right answer.

#### Workflow

Card $\rightarrow$ Punch a piece $\rightarrow$ Extract (Dissolve paper, solubilize amino acids, precipitate proteins) $\rightarrow$ Grind $\rightarrow$ Filter solids $\rightarrow$ Derivatization

### Derivatization 

A kit you can buy!
7 Calibrants
Internal Standard
QC Standards
Reagents
Diluent
Buffer
Plates!
Formic acid
**Little bits and bobs!**

Highly optimized organic synthesis
- Rigorously reproduced.
- Adds a "tag."

**Protects the amine from an amino acid.**
Now everything is negative, because they all have an available carboxylic acid group.

**Makes them heavier.**
Much easier to detect from little 80-ish amu molecules.

They have chromophores now. Absorbs UV and fluoresces.

Enables separation by reverse phase chromatography

UV 280 
Fluo 395 
Blow off tag 171 amu peak

Derivatization is what Analytical Chemists call Synthesis reactions.

**Must be HIGHLY REPRODUCIBLE and HIGHLY REPEATABLE**
- Validation
- Standardized
- Optimized
- Controlled
- Robust Statistics

Everyone must have the same answer.

#### Validation

Set up your instrument to a prescribed way. Every doctor's office, every hospital. 
**Only one company has the approved license for this test.**

### Amino Acid Separation

BEH C18 Column

Reverse Phase
Polar to Non-polar

Asparagine
Glutamine
Serine
$\beta$-Alanine
Sacrosine
Alanine
Proline
Lysine
Tyrosine
Valine
Isoleucine
Leucine
Phenylalanine
Tryptophan

Solvent A - Water with 0.1% formate
Solvent B - AcCN with 0.1% Formate

Needle Wash - B
Purge - A
Column Temp 55$\degree$

Curve 6

**Babies need proline!!!**

208 Peak is a side product - Piece of the tag that falls off.

### Method Validation

**Validation:** A Set of Experiments that you MUST do to ensure that any analytical procedure is BOTH ACCURATE and PRECISE.
Controls for all of the things that **Humans** do.

Robots make mistakes, too.

**QC Sample** - Something you can use to calculate variation over time.
*How much do certain factors change how things happen?*
Test the top and bottom ranges of the method. 

You cannot show that something is "0".

Standard is 2.5 $\mu$mol/mL, 1 mL
Limit of Detection: 3 pg/10$\mu$L = 300 pg/mL
Average AA: 121 g/mol = 121 $\mu$g/$\mu$mol

#### Dilution

Bottle 1 -> 300 $\mu$g/mL 
Bottle 2 -> 30 $\mu$g/mL 
Bottle 3 -> 3 $\mu$g/mL
Bottle 4 -> 300 ng/mL
Bottle 5 -> 30 ng/mL
Bottle 6 -> 3 ng/mL
Bottle 7 -> 300pg/mL

Calibration curve of peak AUC.
Should be straight line w negative curve! (bottles on x axis)

What is a calibration curve, really? *NOT A STRAIGHT LINE.*

Somewhere between not having enough to detect and having so much that the detector is saturated.
**Lower Limit and Upper Limit of Quantification**
*LLOQ and ULOQ*

Limit of Detection (LOD) is past the LLOQ.

Between LLOQ and ULOQ is the linear range.

Cannot include **plateaued** points in the curve!
						 ^ Strange Word

You are more likely to underestimate a concentration than overestimate.

# Thursday, Oct 05, 2023
###### Topic: **Statistical Validation**
Lecture Link:

## Todo/Assignments
N/A

## Notes
### Fit for Purpose

`We call this fit-for-purpose; because you can't call it the rat in the potato chips method.`

We achieve Fit for Purpose by rigorous validation. This is a law thing.

### Validation Terms

- [ ] Check AOAC Documents (two) on Canvas

Does the method work?
Is the method Fit for Purpose?
How confident are you in the results?
How accurate and precise is your data?

#### Selectivity

How far away is stuff from your stuff.

#### Performance Characteristics

Functional qualities.
Statistical measures.

What must a sample/product achieve? How far is the defined value from the true value?

#### SLV - Single Lab Method Validation

1. Identity - What are you measuring? Isomers, adducts, misidentification
2. Method/Optimization
3. Reference Standard/Material
4. Ruggedness Trial
	- The idea of: If I make a change, how big is the impact? How important is the impact?
5. Specific Variables
	- Analyte Addition
	- Re-extraction
	- Solvent comparisons
	- Orthogonal methods
6. Selectivity
7. Repeatability
8. Reproducibility
9. Stability

#### Standard Curve

Minimum of 5 measurements. More is better.

#### Linearity

R$^2$ of the Linear Region of the Standard Curve should be 0.99XX
Take regression over 3 days, if %RSD <20%, its okay.

Use the highly sophisticated method of **EYEBALLOMICS**.

#### LOQ 

Amount of substance that can reliably be assigned a quantitative value.
US Pharmacopeia - 10% RSD
IUPAC 10x Noise

#### LOD

Least amount of substance that can reliably be assigned a quantitative value.
IUPAC: 3x Noise

# Tuesday, Oct 10, 2023
###### Topic: **Standards**
Lecture Link:

## Todo/Assignments
- [ ]

## Notes

### What is a Standard?

A material that is sufficiently homogenous and stable with respect to one or more specified properties.

#### Peanut Butter?? How Do We Know It's Peanut Butter?

Well, probably a standard.

#### NIST - National Institute for Standards and Technologies

#### NRC - Canadian Certified Reference Materials Project

Holds the world's standard for Nicotine in Tobacco.
- Also THC
	- 20k kg of cannabis to get this.
National mandate to provide measurement science, advice, and technical services to government and industrial clients
- Ensures basis of fair trade and commerce
- Enhances societal well-being
- Enables innovation through evolving and emerging technologies that rely on *precision measurement*.


### Anecdotes

#### pH - Only Ever 2 Decimals
#### Biotoxins

Rare and difficult to get and weigh. Very expensive if available!!! 40,000mg.
Careful matters. Tidy matters.

#### In-House RM

Don't bet it's there but consider that it should be.
Not true enough to call Justin Trudeau

### Uses of RMs and CRMs

**How Do You Measure Accuracy???**: YOU USE A CERTIFIED REFERENCE MATERIAL.
- Calibration of instrumentation and assays
- Evaluation of trueness
- Estimation of uncertainty
- Method development
- Method validation
- Quality assurance and quality control

```
I am a matrix effect
```

### Stuff You Should Know for the Midterm

Chromatography
Qualitative and Quantitative data
- Can meausre it
Fit for Purpose
- Instrument that just works for what you need it for, so its the same for everyone and you get the same answer.
- If you have a nail use a hammer not a shoe. You don't need an MS.
Validation
- Prescribed set of specific experiments which test how good your method is.
**AOAC**
- **Association of Official Analytical Chemists**
Single Lab Validation
Performance Characteristics
- Set of measures
Sample Matrix
Dilution series
Standard curve
- Not a line its a CURVE!!! You just don't see the whole thing.
Linearity
LOD
- Lowest you can see  a thing but its not a real thing
LOQ
- Lowest or highest you can say its there
CRM/RM
- (Certified) Reference Materials
- Very few agencies
	- NIST
	- NRC
	- Tested in a bunch of different ways, super expensive.
- 

# Thursday, Oct 12, 2023
###### Topic: **Standards**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Make a Peanut Butter Reference Solution!
1. Find out what it dissolves in,
2. Separate polar and non polar phases
	1. Normal Phase for Polar
	2. Reverse Phase for Non Polar
3. We wanna check Afflatoxin?
	1. Get a CRM of Afflatoxin.
	2. Quantification standard for the standard curve.

Fit for Purpose could mean Looking at the cookies and Seeing if there is Wood

Health Canada found a sus product that send 25 people to the emergency room! Here is what we know, tell me what you would do.
- [ ] Do this practice question.

### AOAC Official Methods of Analysis

3000 Methods recognized worldwide. They are the authority.

### Single Lab Validation

1. Identity - What ar you measuring?
2. Method / Optimization
3. Reference Standard
	1. CRMs are external standards
4. Ruggedness
5. Specific Variables
	1. Analyte addition
	2. Re-extraction
	3. Solvent comparisons
	4. Orthogonal Methods
6. Selectivity
7. Repeatability
8. Reproducibility
9. Stability

#### More on CRMs

Don't take into account the sample matrix.

##### Standard Addition Experiment

5 flask dilution series
5 mL of unknown in each flask
Add 0, 5, 10, 15 and 20 mL of standard to them too
Dilute to 50mL

Extrapolate down to 0 = y to find volume of added standard to equal that concentration (-6mL or something). 

Back to PB.

Add aflatoxin, extrapolate back
If there wasn't, it will extrapolate back to 0.

**Not the most accurate**

**Takes into account the matrix effect**
Because sample and standard are in all samples, pretty much.

Best way to do this, is to use an internal standard.

$$
\text{Ratio} = \frac{\text{Area Under Peak}}{\text{[Internal Standard]}}
$$

$\text{\% Recovery}$

You know how much X you put in, so you can see how much you get out.
$$
Spike = \frac{\text{Area}}{\text{[Added]}}
\text{ and }
Peak = \frac{\text{Area}}{\text{[Sample]}}
$$

$$
\text{\% Recovery} = \frac{\text{(Area of Analyte + Spike) - Area of Analyte}}{\text{Area of Analyte in Spike}}
$$

Do the math
Do the experiment
See how much you should have gotten
Weep

#### Ruggedness

**% Relative Standard Deviation**

Degree of reproducibility of the results obtained under a variety of conditions
These conditions include different labs, analysts, instruments, reagents, days, etc.
Measured by reproducing the same analysis in multiple labs

Which things matter and which things don't?

##### Youden Trial

Choose 7 Factors
Choose a high and low for each
Run a series of experiments that mix the highs and lows so all are covered
Stats calculate the effect of each factor
Plot on a line according to relative weight of each factor

**Identifies factors that matter in the analysis.**

### Multiple Lab Validation

InterLab?
