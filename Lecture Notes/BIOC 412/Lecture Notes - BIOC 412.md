Class: #BIOC412 #Courses 
***
# Wednesday, Sep 13, 2023
Topic: **Data Sets**

## Todo/Assignments

- [x] Look at Assignment Part 2 ✅ 2023-09-19
- [x] Ask Dr. Murch about her Turkish Coffee [completion:: Oct 17, 2023 @ 02:51 PM]

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

- [x] Assignment 2 📅 2023-09-27 [completion:: Oct 17, 2023 @ 02:52 PM]

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
- [x] Actually look at the data!!! [completion:: Oct 17, 2023 @ 02:52 PM]

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

# Wednesday, Oct 04, 2023
###### Topic: **D**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

What is a signal vs noise
What is limit of detection without standard
What is real vs what is garbage
How precise do you want to be with each individual peak?

What is a PEAK?
- Checks gradient between points (derivative, basically) and starts when it goes up and stops when it goes down.
	- 3 Points
- It will ask you what you want to define as a peak.
	- The more points you use, the less sharp peaks you get.
- Does it have to go back to the baseline to be a peak?

### MZmine Continued

- [ ] Make sure to use her slide deck to walk yourself through MZmine. !!!!!!!!!!!!!!!!!

MS level 1 in +ve mode.

DIA or DDA mode:
- **DIA**: Data Independent Acquisition
	- Captures everything
- **DDA**: Data Dependent Acquisition
	- Captures the big signals and their fragments.

Always choose exact mass.

$3\times10^5$ Noise Level (30k)
Show Preview

Murch maybe would choose 55k.

Don't have more than 70000 lines.

Use Lauren's ADAP parameters.

Try Savitzky Golay resolver. And other resolvers.
`Resolving == Smoothing`

Gustavo is the Plight of the Modern Age

What does EIC mean?

Plant 4 vs 2 other plants.

Definitely try out annotations.
- Database Match to HormonomicsDB

# Wednesday, Oct 11, 2023
###### Topic: **Deconvolution and Tooling**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Metabolomics is Never Normal

Cannot do an ANOVA, have to do non-parametric analysis!

PLS-DA, Random Forests, MVA.

### msDIAL

Data Independent Algorithm

### How do I get from a peak to a molecule?
1. Determine correct adduct,
2. Determine correct molecular formula,
3. Determine list of candidate structures

Centroid data

1% of known chemicals have MS/MS spectra

- [ ] Check Adduct Spreadsheet from UCDavis

#### Alternative Solutions to Compound ID

- Reaction Chemistry Methods
	- MS-Finder
	- Mass Frontier
- Machine Learning
	- Sirius+CSI-Finger ID
	- CFM-ID
- Heuristic
	- LipidBLAST
- Quantum Chemistry
	- QCEIMS

### How Do You Trust Metabolite ID?

A. Trust the researcher?
B. It has the name?
C. It's in a journal?

- [ ] Metabolomics Workbench

### Metabolomics Standards Initiative (MSI)

Started in 2005
**Aim:** Provide a reporting standard for identification of compounds.

#### Schymanski Levels

1. Confirmed by Reference Standard
2. Probable Structure by Library Spec Match or Diagnostic Evidence
3. Tentative Candidate by Structure, Substituent, or Class
	1. Exp. Data
4. Unequivocal Molecular Formula
	1. MS Isotope/Adduct
5. Exact Mass of Interest
	1. MS

#### MSI Levels Guide

Peak quality?
Determine mass error +/- 1 mDa
m/z-RT match?
MS/MS match? Is it good or bad? Are there other possible hits with good MS/MS match? (non-unique)
Biologically plausible?
If MSI fits but does not match criteria, but you have a good match - are your criteria too strict?

### Molecular Formula Deconvolution

Accurate Mass
MS/MS Spectrum and Fragment Ion Analysis
- Neutral Loss
- m/z Difference
Accurate Isotopic Abundances
Characteristic Isotopic Patterns
- 12C, 13C, *14C*
- 3:1 - Cl [M]+:[M+2]+
- 1:1 - Br [M]+:[M+2]+

### Structure Deconvolution

Get a high resolution MS

MS/MS Spectrum
1. Precursor Match
2. Product Ion Search
3. DB
Returns Results with Annotation.

#### Databases:
\$\$\$: NIST & METLIN
Free: MoNA & In-House

Use MS/MS, but not limited to MS1 or MS<sup>n</sup>

NIST MS Search
<600 is bad.

#### MS-DIAL Entropy Score

Score from 1-4, meaning how much a molecule makes noise in the instrument. 
Increases with more fragmentation or noise.

0. Guanosine - No fragments
1. Lactitol - 3 fragments
2. L-Valine - Like 10 fragments
3. Juarezic Acid - So many fragments.

#### Quantum Chemistry

Rebuilds molecule from the entropy - Considers bond strength of individual bonds.

#### MS-FINDER

- [ ] Mess around with MS-FINDER
- [x] Check out Lotus Database [Link](https://lotus.naturalproducts.net/) [completion:: Oct 17, 2023 @ 02:52 PM]

#### MetaboAnalyst 5.0

It's Canadian
Does Stats

Has NMR Peak Lists
NMR Bayes is there under other, check out what that does!

# Wednesday, Oct 18, 2023
###### Topic: **Software**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

AD AD processing
MS scan 1
make sure not MS2
Polarity +

Data from an MS to excel is hard...

MZmine is an irrational program

### Software 1 - MetaboAnalyst

How to meaningfully use MetaboAnalyst
- Think about your data, and what you are actually putting into the program.

- [ ] Read Tutorials at [MetaboAnalyst](https://www.metaboanalyst.ca/docs/Tutorials.xhtml)
- [ ] Check https://omicsforum.ca

Seq2Fun - RNASeq with Metabolomics Data

- [ ] Check [MetaboAnalystR](https://www.metaboanalyst.ca/docs/RTutorial.xhtml)
Automated p-values are weighted for the human genome, so might have to change that. Use something-Wallis p-value

**Things to Try:**
1. Load mzML into LC-MS spectra processing,

Start at the bottom, and work up.

Check the data file to make sure it looks like your input, might be why it doesn't work.

#### Transformation and Normalization

Bring small things up and change big things by not that much.
Play around with this, make all the things go to the middle.
**For Portfolio** Step 1. Normalize Data

#### Processing

SAM data is RNA processing from a microarray but with your MS data

Map Pathway from most significant feature
PLS-DA most VIP score

### Software 2 - Murch's Stuff



### MSDial


# Monday, Oct 23, 2023
###### Topic: **More MetaboAnalyst**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

## Cranberry Data

Stevens Cranberry is our one

**MetaboAnalyst**

What is the best statistic in terms of filtering
SD, RSD?

We use whatever is default for filtering

*Data Normalization*
Once it's normalized, the file is mutated. Don't do it again.

-> Log Transform
-> Auto Scaling

Now that there are 5 treatments

Network Plots
Edges length $\rightarrow$ How far apart are the values

### PCAs

Often overinterpreted

---

Heatmap shows outlier Stevens B

Same with K-means

- [ ] Chec out excel Data > Text to Columns

Get a hit list from SAM or something
Put it into mummichog (Pathway Analysis)

Set up data in CSV to do some metabolite mapping

Biomarker Analysis
Compare stevens to ONE thing for the ROC analysis (receiver operator characteristic)
- Calculates AUC and ranks by ROC curve. Determines most significant in data if data is not normal
- For each metabolite what is the most significant difference.
- Plots true positive rate against false positive rate.

Then load this to pathway thing


Meta Analysis thing
Upload data
get a kegg map

## Metabolomics Workbench

Just wanna do science and publish a paper w/o being in a lab?
Design an experiment, download data from here, and write a paper.

Ask any question you want

# Wednesday, Oct 25, 2023
###### Topic: **Metabolomics Workbench and Public Databases**

## Todo/Assignments

## Notes

Piktochart [link](https://create.piktochart.com/teams/29861254/dashboard) for Portfolio

### Public Databases

You can put data on a hard drive for never or you can put it into a public repository!

#### Benefits

Transparency = reader confidence
If YOU are confident, make it public

Allows for other researchers to reproduce results = reader confidence

Publications in better journals

#### Retip

Open-access.
Machine-learning tool
- All of the chromatography data,
- learned from retention time, molecule, and column

#### Reporting Guidlines

FAIR: Findable, Accessible, Interoperable, Reproducible

FAIR Data policies are in place across many fields of scientific research including microarray data, genomics, proteomics.

Est. that 2/3 of researchers have concerns about data reproducibility.

##### **F**indable
Data and supplementary materials have sufficiently rich metadata and a unique and persistent identifier

##### **A**ccessible
Metadata and Data are understandable to HUMANS and MACHINES. Data is deposited in a trusted repository

##### **I**nteroperable
Metadata use a formal, accessible, shared, and broadly applicable language for knowledge representation

##### **R**eusable
Data and collections have a clear usage license and provide accurate information on provenance
- License number,
- Ethics,
- Biosafety

##### Reporting

Plant people are better at being compliant.

Metabolomics Workbench is the most compliant for plants.

### Repositories

Metabolomics Workbench
MetaboLights
Metabolic Phenotype Database (MetaPhen) GC-MS Focused
Metabolomics Repository Bordeaux (MeRy-B) NMR Focused
MetabolomeXChange
GNPS** No minimum data reporting requirements

ProteomeXChange

### Workbench

Do:
Volcano Plot
Network Analysis

### Publication

Something called Dryad
If you need to make data public, use Metabolomics Workbench

### Data Workflow

Acquire
Data quality
Visualize
Normalize and scale
Visualize
Apply analysis

1. Minimize Data, filter some out
	- PCA?
	- Need Blanks
		- Solvent Blanks
			- One for each solvent
		- Blank Matrix (Subtractive Metabolomics)
			- Sugar Matrix, so you can remove the sugars
			- Wild Type, so you can remove consistent data

	Independent Variables
	- Experimental condition or treatment
	- Chosen in design
		- Nominal (>2 unordered groups)
		- Ordinal (>2 ordered groups)
		- Binary (2 groups)
	
	Dependent Variables
	- Measurement
		- Time, m/z, spectra, etc.
	- Data collected
		- Continuous (conc, peak intensity)
		- Discrete (read counts)

### Univariate vs. Multivariate Analysis
1 variable or many variables.

SAM is **Uni**
ANOVA is **Multi**

**Uni**
Is the metabolite changing between treatments?

**Multi**
Is the metabolite changing between treatment groups?
Which metabolites are different between groups?
What metabolites are most responsible for the differences between groups?

**Bayesian** - *What will come next?*
What metabolites are most important?
- "These previous samples had lots of sugar, weight the algorithm to look for more sugar."

# Monday, Oct 30, 2023
###### Topic: **MetaboAnalyst - What Tests Mean**
Lecture Link:

## Todo/Assignments

- [ ] Portfolio assignment opens on November 1, will be due in December.

## Notes

### Continuing Last Lecture

- [ ] What is Pareto? What is frontloading the data?
#### Descriptive Statistics in Metabolomics

Name the numbers of the normal curve
68.2 95.5 99.7
1 sd 2 sd 3 sd

%RSD = Coefficient of Variation
- Useful for data with very different means

Pseudoreplication is VERY PRECISE
Real biological replication is not. This is more accurate.

**Precision in metabolomics is**
- Quality control standards
- Alignment standards
- Instrument calibration standards
- Comparison between experiments, labs, datasets.

#### Multivariate Statistics in Metabolomics

Dependent variables in multivariate are interlinked. They depend on each other.

Particularly important in metabolomics since metabolites do not function in isolation.

Classification of metabolites into Unsupervised and Supervised groups.
- **Unsupervised**: Exploratory; trends not 
	- PCA
- **Supervised**: Confirmatory; You tell which things belong where
	- PLS-DA

##### Principal Component Analysis - What is It

Circles are 95% confidence in the *model*. 95% sure you used the right model.

Add the variance from each axis to get how much of the sample variance is described by these two components.

Variance: Square of SD of how different the things are from each other.

Bottom axis: Thing that varies the most
Side axis: Second or third thing that varies the most.

This is a matrix projection method.
- Windows in multi dimensional spaces
	- Tables with many correlated variables
- Generates new independent latent variables consisting of scores ($t_i$) and loadings ($p_i$)
- Interpretation of scores: info about relationships between objects
- Interpretation of loadings: info about how far from an axis

**What is it doing?**
Calculating the difference between data points
Plotting difference data along a vector
Ranking data by distance to the vector
Centering to the most dense data
Determining points furthest from the most data (most different)
Clustering samples based on distance from centered data.

### PCA and Eigenvalues/Eigenvectors

Assume data is linear
Transform data
Sort by scores
Compare by loadings

- [ ] Do eigen stuff at the eigen institute for a weekend. ::BUCKETLIST

#### Data to Variable Space

1. Plot in 3d
2. Move origin of axes to the middle of the cluster
3. First principal component (PC1)
	1. Biggest data difference
	2. Set to describe the largest variation in the data, which is the same as the direction in which the points spread most in the variable space.
	3. Score ($t_{i1}$) is distance from projection of the point on the 1st component to the origin

![[Lecture Notes - BIOC 412 Mo 30-Oct 2023 17.38.excalidraw]]

Honestly, just look at the slides. AND DOWNLAOD THEM

- [ ] Download all of the slides!!!!!!

Loading is the distance that the features have moved from theoretical 0, intersection of the two scores. Basically a 3d coordinate.

Biplot
- Arrows represent the eigenvectors

Scree plot
- Total variance explained by each principal component.

Variation compressed from K dimensions to 2 dimensions

Hotelling's T^2 test
- Generalized Student's t-test of a PCA
- Tells what the outliers are. 

### Uses of PCA

It definitely tells the stunningly obvious
- Data exploration and visualization
- Outlier Detection
- Variable reduction
- Data preprocessing evaulation (are there obvious groups?)
- Validation

### PLS-DA

Cross-validation

IF you get a WILDLY different answer from PLS-DA from PCA, something is wrong.
They *should* be the same.

If the result is non-specific, you can use non-linear supervised analyses such as random forests.

Using too many components overfits the model. 

**VIP Scores (Variable Importance on Projection)**

1 score per variable per component.
Tells you which components have high and low variability based on treatment.
What is different between the thing and the major component in the thing.

\>1 is significant, depending on number may set a higher cut-off
<1 is less important, can also excluding from the model

Analogous to univariate p-values.
Tells which features to investigate.
Probably the most useful.

### False Discoveries and True Values

How do I know?

#### Significant Analysis of Microarrays (SAM)

For each variable, finds highest and lowest values and calculates a t-test for them.

![[Lecture Notes - BIOC 412 Mo 30-Oct 2023 18.07.excalidraw]]

Does not assume normality. 

Things above the line are not different, things below are. In metabolomics, we want our chosen components to NOT be below the line.

### Bayesian Statistics

Mapping and clustering

- [ ] Website called linked papers to make a map of papers which cited a paper.

Pick a molecule, and look at all of the things that are linked to that molecule. 

Predictive, hypothesis generating, clustering, mapping, networking, machine learning.
Each parameter can have a probability distribution given some extra context (prior knowledge)

Allows you to ask "which result is more important"?

Compares distributions of observations.

Edges - distance between individual things in a cluster.

**Cytoscape** and **GNPS** are good tools for this.

### Clustering Methods

https://fronteirsin.org/articles/10.3389/fbioe.2018.00031/full 

Hierarchal Clustering

Outputs as dendrograms and heat maps.
- Lines on the side, series of clusters.
	- Find 2 most similar metabolite expression levels or curves
	- find net closes pair of levels
	- iterate

K-means clustering, calculate averages between different nodes of the cluster.
- Randomly chooses k observations from the datasets and uses these as initial means
- Calculates the similarity of the next object to this centroid
- If similarity is greater than threshold, object added to the cluster and centroid is recomputed, if not the object starts a new cluster
- Repeat until done

#### Biological Context

If it doesn't look right go back and look at it again.

Many approaches are prone to overfitting
Other times no obvious separation by PCA/PLS-DA but a strong biological phenomenon should be present
Consider groups of metabolites that are known to be involved in the process
Targeted/untargeted analysis

# Wednesday, Nov 01, 2023
###### Topic: **GNPS**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Assignment (Portfolio)

Make a good biorender!
Make the whole thing pretty

Analysis report is an appendix for the final report.

### GNPS

In silico enzyme prediction
Precursor; Predict that the enzyme exists; do the math to figure out what the product should be; figure out that its there.

#### Synthetic Biotransformations

AKA In silico enzymology, logical algorithms.

#### GNPS Continued

https://gnps.ucsd.edu/

"Social Molecular Networking"
-> Structural Dereplication 
- Find unknown knowns.

https://ccms-ucsd.github.io/GNPSDocumentation/quickstart

Can use mzXML, mzML, or Thermo raw.
Less than 3 treatments.
Analysis maxiumum of 50 spectrum files.
Each file less than 200 MB.

MASST
- Library of spectra
	- "MS equivalent of NCBI BLAST"

linked paper website!!!!

Assumes data independent

Takes ALL The peaks, no baseline editing.

# Monday, Nov 06, 2023
###### Topic: **HormonomicsDB**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### The HormonomicsDB Story

**Plants are way cooler than animals.**

ALL plant cells are totipotent - Any cell can become another cell. Even embryos.

There is one pomelo that is natrually occurring.

Citrus made from protoplasts, fusing them together, and growin'em and seeing what we got.

Hormones supposed to be at small quantities, so why:
- Cytokinins from adenine
- Auxins from tryptophans
- (Skoog and Miller Hypothesis) All cytokinin and auxin knockouts are lethal.

High aux low cyt $\rightarrow$ Roots
Opposite $\rightarrow$ Shoots
High both $\rightarrow$ Callus

How do we measure hormones? So little!!!
\+ site of synthesis changes

Cell walls are made into desks and chairs.

Apoplastic space is 5.7 pH. Media is too because you want to mimic it.
Lower auxin at a specific location makes pH to 5.2 which activates cellulase and hemicellulases specifically at one place in the cell wall, which cuts it, and then causes plant bending!

Ethylene is a plant scream.

There are lots of plant hormone classes.
- Auxin
- Cytokinins
- Salicylates
- Strigolactones
- Brassinosteroids
- Ethylene
- Karrikins
- Gibberellins
- Abscisic Acids
- Jasmonates

Karrikins are released by wildfires, and old (30 yo) seeds can germinate because of karrikin presence.
Natural repair of forests and stuff.

#### Melatonin and Serotonin - Plant Growth Regulators???

Murch's PhD thesis, discovering melatonin in plants! 1997.

In 2000 she found the pathway using 14C doping. 12-13 years to get in textbooks.

Murch used crazy drugs on plants in subsequent papers (2001, 2002).

Measurement at a moment in time may or may not contribute to what is actually happening in the plant. Its all cross talking and in flux, so what's the point?

Quantum dots can be used for single molecule detection.

- [ ] Quantum dot things

"not looking at any trevors in the room"

HormonomicsDB is for NUANCE. Not many compounds, but so much information about their relationships.

Was smell of cannabis correlated with terpene profile?

High THC are lower because carbon flux goes towards giberrelic acid.
- High THC varieties smell different. Woodier and skunkier
- Low THC High CBD is citrusy and sweet and tropical.


