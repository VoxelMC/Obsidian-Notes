Class: #BIOC412
***
# Wednesday, Sep 13, 2023
Topic: **Data Sets**

## Todo/Assignments

- [ ] Look at Assignment Part 2
- [ ] Ask Dr. Murch about her Turkish Coffee

## Notes

### Datasets
#### Wine
Top Middle and Bottom Replicates $\rightarrow$ Pseudoreplicate
**Hypothesis:**
What can we use this data to ask?
*Compare years 2005 vs. 2006?*
*Compare Wineries*
*Top vs. Middle. vs. Bottom OF EACH DIFFERENT WINERY*
*Alcohol level vs. Chemical Diversity*

#### Coffee
Big dataset!
Different brands.
*Is prep (extraction temps) contributing to diversity.*

#### Cannabis
White Widow and Big Bud with different plant replicates.


### Assignment
What do I want to compare?
Data quality characteristics!
- High-risk vs. low-risk
	- 3 Replicate $\rightarrow$ features detected, how many replicates does it need to be present in to be **my data?**
		- All 3 can throw out good data (Type 2 - False Negative);
		- Only in 1 increases risk of artifacts (Type 1 - False Positive).
		- **No Real Wrong Decision**
Find out the quality of the data - do some testing of the water.

- [ ] What constitutes a feature in the data?

### Types of Experimental Design for Metabolomics Data Analysis


#### Complete Randomized Block
Simplest design

|             | Group 1 | Group 2 |
| ----------- | ------- | ------- |
| Treatment 1 | X       | X       |
| Treatment 2 | X       | X       |
| Treatment 3 | X       | X       |
**Stats to Compare**
Compare treatments
Compare groups
Compare treatment x group interactions

Use ANOVA

#### Nested Design

Two conditions
(Pretend there are two)

| Treatment | Group 1 | Group 2 |
| --------- | ------- | ------- |
| 1         | X       | X       |
| 2         | X       | X       |
| 3         | X       | X       |

Use MANOVA

#### Time Study
| Treatment | Start | Time Interval 1 | 2   | 3   | n   |
| --------- | ----- | --------------- | --- | --- | --- |
| 1         | init  | Replicates      | ... | ... | ... |
| 2         | init  | Replicates      | ... | ... | ... |
| 3         | init  | Replicates      | ... | ... | ... |

**Stats to Compare**
Compare Treatments
Compare Time Points
Compare Treatment x Time
Regression analysis
Multivariate analysis

#### Replicating Blocks

| Experiment | Dependent   | Independent     |
| ---------- | ----------- | --------------- |
| 1          | Treatment 1 | Replicate Tests |
| 1          | Treatment 1 | Replicate Tests |
| 1          | Treatment 1 | Replicate Tests |
| 2          | Treatment 1 | Replicate Tests |
| 2          | Treatment 1 | Replicate Tests |
| 2          | Treatment 1 | Replicate Tests |

ANOVAs within each block
- Hope you get the same answer
- If not, try again
- Not a MANOVA


### Data Minimization
Pick treatments and use ML to predict the space between treatments.

#### DOE - Design of Experiments
- Originally developed to optimize manufacture of ball bearings!
- System of selected treatments and comparisons to extrapolate relationships.
- Method of simplifying and reducing sample numbers.
- Determines relationships BETWEEN treatments and responses as a geometric pattern.
- Makes predictions for responses.

1. One factor x
2. Two factor xy
3. Three factor xyz
4. Four factor - orthogonal projection
5. Nine factor cube projection
6. Ten dimensional cube projection

DesignExpert
jmp Statistical Discovery
R...?
- [ ] DO R IN CHATGPT. JUST TRY IT.

Ellistat is FRUSTRATING AND HARD TO USE

Give ranges, program makes a small set of tests

Do it at the start, do the minimum amount of work and get the maximum amount out of it.

#### Youden Experiment - Type of DOE
Older, no cool fancy tools in R.

Investigate 7 factors in one experiment requiring only 8 determinations.

1. Choose 7 factors
2. Choose a high and low value for each
3. run experiments so that all are covered
4. stats calc the effect of each factor
5. plot factors along a line according to relative weight
6. identify factors that matter.

$\frac{X_1+X_2+X_3+X_4}{4} - \frac{X_5+X_6+X_7+X_8}{4}=J$

### Mass Spec
**m/z can be used for:**
Compound ID
Checking Isotopes

#### Let's Build a Mass Spec
1. Sample injection
	1. Chromatography (HP-LC)
	2. Heat (GC-MS)
	3. Paper (Airport)
	4. Laser Ablation
	5. MALDI
	6. ...
2. Ionizer
	1. ESI (Electrospray Ionization)
		1. COULOMBIC EXPLOSION
3. Focuser
	1. Lens, Z-Stack, Filter, basically a copper coil
	2. Lower charges are slower
	3. Smaller molecules are faster
4. Quadrupole
	1. Alternating charges metal rods
	2. Spins 'em around
5. Archetype
	1. **Single quadrupole**
	2. **Time of Flight**
		1. Out of Q1 into literally a box
		2. Pushers and Pullers - Back and Forth
		3. V and M modes
		4. Smallest and Most Charged Leave First
		5. m/z directly proportional to time spent in the trap.
	3. **Triple Quadrupole - MS-MS (Tandem)**
		1. Q1 - First Quadrupole
		2. Q2 - Collision Cell
			1. Has Poles
			2. In a box
			3. Put in some Argon gas 'cuz it's inert
			4. High voltage to fragment
		3. Q3 - Put fragments in a nice straight line
		4. Single Reaction Monitoring - Not everything will fragment in Q2
			1. MRM, SRM, SRI
		5. Only measure the fragments you optimize for
	4. **Orbitrap**
		1. Modified version of a ToF MS.
		2. Stuff never has to leave
			1. You can pick when to let stuff leave
		3. You can also fragment everything
		4. Data-Dependent Analysis
			1. Pick one m/z to fragment and detect
		5. Data-Independent Analysis
			1. Fragment EVERYTHING
			2. MSDIAL puts everything back together from fragments.

