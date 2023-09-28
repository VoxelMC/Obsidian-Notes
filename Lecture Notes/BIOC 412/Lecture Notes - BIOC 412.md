Class: #BIOC412
***
# Wednesday, Sep 13, 2023
Topic: **Data Sets**

## Todo/Assignments

- [x] Look at Assignment Part 2 ✅ 2023-09-19
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

# Monday, Sep 18, 2023
###### Topic: **Metabolomics Workflow: Data Acquisition** Guest Lecture
Lecture Link: N/A

## Todo/Assignments

- [ ] Assignment 2 📅 2023-09-27

## Notes

### TMIC - The Metabolomics Innovation Center

- [ ] Check out TMIC web page

hmdb
Many services for doing stuff below.

### NMR Metabolomics

- Non-destructive
- Robust instruments
- Minimal instrument downtime
- Simple sample prep
- No chromatography
- No chemical derivatization
- Spectra are predictable
- Allows for precise structure determination
- Inherently quantitative
- Easily automated
But...
- Poorly sensitive
- Modest metabolite coverage
- Expensive instruments
- Large instrument footprint
- Needs cryogens (He (l))
- Need to maintain
- Small spectral databases
- Few software resources

- [ ] Read: NMR Metabolomics: A look ahead in Perspectives in Magnetic Resonance. David S. Wishart.

### GCxGC-MS and GC-MS Metabolomics

GCxGC-MS
- Excellent sensitivity
- Excellent separation
- High peak capacity
- 2D separation plane
- More information per unit time
But..
- Limited availability of fast detectors
- Maximum allowable operating temp
- vast amount of data

GC-MS
- Sensitive
- Excellent separation
- Comprehensive DBs for identification
But...
- Requires derivatization to make things volatile
	- E.g. Sugars $\rightarrow$ acetylation
- Fit for non-targeted screening of volatile compounds

### LC-MS Metabolomics

Non-volatiles
- Most popular
- Lots of options for detectors, chromatography, derivatization, etc.
- Targeted or untargeted
- Less clear of pros and cons.
	- Can get expensive

### Metabolomics Toolbox

#### Experimental Design
Cassette model with complete randomized standards
Sample replicates with automated data collection and integration

#### Validated Metabolomics Methods
- Validation Standards
- Alignment Standards
- Targeted Standards

#### Statistical Models and Scripts
- Eliminate false discoveries
- Discover new metabolites

#### Logical Algorithms and Biotransformations
- Discover new pathways
- Discover metabolomic responses
- Discover metabolite families
Murch is interested in this.

[pnnl-comp-mass-spec.github.io](pnnl-comp-mass-spec.github.io) 

# Wednesday, Sep 20, 2023
###### Topic: **dd**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

Guest Lecture from Concordia on Friday. Metabolomics in the medical system. 1pm!!! Be there!!!

### Case Study: Thidiazuron (TDZ)

TDZ is a Herbicide
- Sprayed on cotton fields
- Chemically synthesized
	- Diurea derivative (thiadiazole and phenyl)
- All the leaves fall off the plants
- Plant growth regulator
- Mediator of endogenous plant growth regulators
- Sold as DROPP
	- Made cotton cheap!
	- Sprayed 5 days before harvest
	- Leaves drop in 3 days
		- Unique to Malvaceae
	- Leaves are green and turgid

Many papers published
- *In vivo* propagation
	- Cotton defoliations
	- Bud breaking of apple trees
	- Greenhouse regeneration
- *In vitro* propagation
	- Organogenesis
	- Somatic embryogenesis
		- Basically budding, African violet.
			- Murch part of breeding program.
			- Horsters greenhouse in Ontario.
			- Undifferentiation from somatic cell, rearranges its identity, and redifferentiates into an embryo.

FT-MS: Fourier Transform MS
- Quadropole
- Detector collects all signals off of very long poles
- Math uses FFT to transform signal to *m/z*s
- Developed by Comisarow M. was from UBC Vancouver - Fourier transform ion cyclotron resonance spectroscopy. He invented it..
- UVIC has a 14T
- Custom built instruments

#### Hypotheses: 

##### Thidiazuron forms oligomers in solutions and plant tissues.

Obtained m/z to 6 decimal places, highest you can get!
- Vast majority of the time you don't have a separation system before collection.
- You can predict a formula from deconvolution. How?
	- 19774 lines of data
		- 3 modes and 3 extractions
			- +, -, neutral modes
			- EtOH, Water, Hexanes
			- 9 Treatments
		- 2 Replicates
			- 3 treatments
			- 6 samples
			- $15,000
	- **Deconvoluting m/z Signals**
		- Prediction algorithms
		- You really need at least 4 decimals to tell things apart.

TDZ Oligomers in stock solutions
- Old solution worked better than a brand new solution.
- Murch Review 1997
	- 220, 440, 660, 880, 1100, 1320 peaks
- Diels-Alder!!!
	- Diene and Dienophile
- Tetramer is very structural, maybe it is docking specifically somewhere and doing something.
	- Monomer is really not that active.

##### Thidiazuron is metabolized by plant cells to release bioavailable sulfur and nitrogen.

Looking at breakdown products, there are compounds that could give N or S.
Glutathione is higher in lower [TMZ] treatment.

##### TDZ increases uptake and catabolism of 5C and 6C sugars from the culture medium.

Holds the glucose transporter open sterically.
(Slide | Gray dots decreased, pink dots increased).
- Investigate pathway increases
- TMD changes how plants move sugars.
- Shut down chlorophyll metabolism; porphyrin.

Mummichog vs. GSEA

##### TDZ forms conjugates with molecules in plant cells.

Look at slides.

##### TDZ inhibits biosynthesis of diterpene-derived metabolites and enhances synthesis of sesquiterpenes and triterpenes.

Growth regulators
- Absiscic acid decreased completely!
	- Is responsible for leaves staying on

##### TDZ Affects the Shikimate Pathway

Kynurenine stuff
- Oxidation product of tryptophan


#### On TDZ

~4.5 million kg of TDZ used per year IN THE US
- We barely know anything about it
- It does a lot in plants
- What does it do in us?
- We spray on:
	- Apples (Bloop),
	- Canola, 
	- Cotton,
	- Pears (Bloom).

#### Purpose

We will be making something just like this. 
- [ ] Double check the case study slides

### Assignment 1, Part B

How to count features:
- Count signals in each column (treatment across replicates).

Add and subtract things that enzymes can do.
Pick a molecule, and check out how it is affected.
- Look for its modification

- [ ] Make a script to add and subtract masses to stuff

Enzymes are super simple. They do serial things - add or take *something*.
- Predictable by change in mass: ($\pm$)
	- NH2
	- Carboxy
	- Acetyl
	- Proton
	- Hydroxy
	- Glucose
	- 
- Isomerization can be looked at using same mass at different retention times.

- [ ] Look at Wikipathways or Kegg for pathways
- [ ] Actually look at the data!!!

### NMR Based

Shipley sometime soon.

# Monday, Sep 25, 2023
###### Topic: **SOmething**
Lecture Link:

## Todo/Assignments

- [ ] FINISH THE ASSIGNMENT

## Notes

### For Assignment 1 Part B

Grubbs or CI
Really go over data quality 
Allocation of features by treatment Fig 2 or 1 (1 would be experimental design).
Venn diagram
- Intersection of features per treatment

What does the data really mean?
- an individual molecule present at some point.
	- m/z
		- molecular identity
	- retention time
		- how long it took to get through the column and the ToF to the detector.

Reverse phase on ToF.

### What is m/z?

+ve Mode makes +ve things go through the MS.
real mass is -1 proton.

+ve mode add a proton
-ve mode remove a proton

### Exporting Data from Mass Spectrometers

Centroid Data vs. Continuous Data.

Centroid for Isotope comparison
Continuous for Peak comparison.

### Cannabis

White Widow is the worlds most generic cannabis.

Big Bud 1 through 5.

Individual seeds grew at different heights.

White widow is the control.

Plant 4 is weird.
- Eliminate it if you want.

BEH C18 column -> reverse phase (hydrophobic stays, philic goes)
- Eluting with Acetonitrile and acetic acid.

Data Independent Acquisition 
- EVERY FEATURE.

CSV is constant.

Pathway mapping tools.
- -> Feature to Feature

### MZmine3

Pick different confidence levels
Think about ion mode

mzmine.github.io

Can handle proprietary software.

Not very good stats, do it in other stuff.

Export to CSV. :)

Import Raw Data.
**mzML in centroid**
**raw files in thermo**

extract to csv

Mass Detection
Merge raw data from all files into one
- Suggest merging

Feature Detection
- **look at all the stuff.**.

End all is excel

Play with settings for a while

Make it into a job.

Visualization -> Histogram
- Feature intensity plot
- Spectra tree
- Isotope pattern preview

***There's a wizard***

Sample metadata
-> Information about how the experiment is run.

*I want to see the differences between all the plants and plant 4*

- [ ] Add metadata to mzmine stuff.

Zoom in on baseline
How do i want it to look like
Pick a number for where to set the baseline
Everything below it no longer exists.

Check in more than one sample $\uparrow$

Create a mass list (highlight all, go to mass detection)
Polarity +ve mode
Set filters and scan types, exact mass.
- DIA data -> pick all scan types.
- Orbi -> Exact Mass
- Centroid -> Centroid
Look through scans to see if noise is reasonable.
Wait

LC-MS -> ADAP chromatogram builder
- Min # of consecutive scans that must have an m/z present
- Dependent on scan speed and chromatography settings
- Min 4-5
- Examine raw chromatograms to see min number of data points in smallest width peak
- Look at replicates that are comparable.
- Scan to scan
	- Orbi -> 0.002-0.005 m/z
		- 5-10ppm
	- TOF -> 0.005 m/z
		- d
- Suffix => date_ID
- Artificial groups happen if m/z and time are too close.
	- Tends to lose isomers, other things that are too close together.
	- Uses S/N
		- S/N does not matter that much, but important to discuss it in a paper.

Alignments
Baseline Corrections

Play around!!!

**We will also do MSDial, and maybe MSFinder**.

# Wednesday, Sep 27, 2023
###### Topic: **NMR Metabolomics**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### NMR Based Metabolomics - The Data

Phenolics $\rightarrow$ Sugars $\rightarrow$ Organic Acids $\rightarrow$ 0 ppm

Fingerprint with Cool Advantages

Chemical Shift vs Intensity is a 2D Dataset
Shift is the header

|        | ppm 1 | ppm 2 | ... |
| ------ | ----- | ----- | --- |
| Sample |       |       |     |

What makes them different?
How important is each ppm?

Concentrations of 1 environment should be the same for another

Multi variant analysis
What compounds drive that variance
What is their presence?

#### qNMR vs Validated HPLC

Concentration can be Quantified by NMR

Consistent across both methods

#### Databases - NMR Gets Better

How is it done? By molecule ID.

#### TMIC

Inifnite rat in a cage that you nver need to feed.

### Questions to Shipley

**Why is NMR so much less sensitive?**
Tiny magnetic moment, 300000:300001 spin up:down.

**Typical NMR Experiment for Metabolomics**
How many samples?
The more samples, the more statistical power.

KAVA

**NMR Database**
HMDB has a lot of stuff.

**Combine Quantification Methods in a Single Model**
Not a good idea, statistically, to combine them.

NMR $\rightarrow$ 64000 Data Points w/ low variance
HPLC $\rightarrow$ 70000 Features w/ High variability

Orthogonally?
Can use them to confirm each other.

**Flavonoids make Complexes with a Metal Ion**
NMR $\rightarrow$ If there is a paramagnetic metal in there, signals are squished and theres no spectrum

**Where Should I Start?**
What is the question?
What am I asking of my data?

NMR Technician???

**Solid State NMR**
Low resolution

You would hate to be spun at tens of thousands of hertz

**Derivatization**
Enantiomers??
Give identical spectra in NMR. Add Enantiomers 

- [ ] NMR almost died so new interview Shipley, check it out!!!

**Binning Data**
Do we bin data, or do we not bin data?
1 singlet $\rightarrow$ 6 points. Do we consider them the same via running average? 

Pick things that are close together, or pick things that vary together?
Pick by slope?

**When to Choose NMR or MS?**
NMR $\rightarrow$ 

MS $\rightarrow$ better at quantification (easier)

Has anyone combined NMR with chromatography? Not FT-MS

- [ ] NMR Paper


