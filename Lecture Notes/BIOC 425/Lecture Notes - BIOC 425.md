Class: #BIOC425
***
# Wednesday, Sep 13, 2023
Topic: **Finishing Stereoselectivity**

## Todo/Assignments

- [x] Remember My Blood Group [completion:: Sep 19, 2023 @ 03:12 PM]

## Notes
### Definition
Stereospecificity $\rightarrow$ only MAKES ONE stereoisomer
Stereoselectivity  $\rightarrow$ only ACTS on ONE stereoisomer.

### Kinetics
#### Kinetic Equations
E $\rightarrow$ Enzyme
S $\rightarrow$ Substrate

$$
E + S \overset{k_{1}}\leftrightharpoons ES \overset{k_{3}}\rightarrow E + P
$$
$$
V_{1}=\frac{d[P]}{dt}=\frac{k_{3}[E_{t}][S]}{[S]+\left(\frac{k_{2}+k_{3}}{k_{1}} \right)}
$$
$$
= \frac{k_{cat}[E_{T}][S]}{[S]+K_{m}} = \frac{V_{max}[S]}{[S]+K_{M}}
$$
$k_{cat}=$ unit of $s^1$ $\rightarrow$ turnover number

##### Catalytic Efficiency
$$
\frac{k_{cat}}{K_{M}} [M^{-1}\cdot s^-1]
$$

Catalytically perfect enzymes have a $k_1$ approaching the rate of diffusion

#### Equilibrium Controlled Process
**Example:** Glucose isomerase
**Reaction:** $\text{Glucose}\overset{GI}\leftrightharpoons\text{Fructose}$
Product reaches max concentration once equilibrium is reached.

#### Kinetically Controlled Process
Product reaches maximum concentration at a given time point and then decreases.

**Example:** Amoxicillin production
![[Drawing 2023-09-13 16.19.00.excalidraw]]

**Serine Protease Bullshit Magic**
![[Drawing 2023-09-13 16.24.10.excalidraw]]
It can go backwards if you switch the order of $NH_2$ and $H_2O$.

### Determining Stereoselectivity
Enzymes have varying levels of stereoselectivity.
Stereospecificity is defined by the preference for (R) or (S) enantiomers.

![[Drawing 2023-09-13 16.38.05.excalidraw]]

#### Kinetic Resolution
$\rightarrow$ resolve and purify a single enantiomer using enzyme.
- $E_{eq}$ $\rightarrow \frac{\left( \frac{k_{cat}}{K_{M}} \right)_{S}}{\left( \frac{k_{cat}}{K_{M}} \right)_{R}}$ where top is of (S) and bottom is of (R).
- Compare initial velocities of enzyme with (R) and (S) (Product vs. Time).

#### Chymotrypsin
(I am not drawing this; in lecture slides)

- [x] Finish This Table ✅ 2023-09-14

| Enantiomer | $K_M$ (mM) | ${k_{cat}}$ ($s^{-1}$) | CE ($M^{-1}s^{-1}$) | $E_{eq}$ |
| ---------- | ---------- | ---------------------- | ------------------- | -------- |
| S          | 50         | 0.46                   | 9.2                 | 18.4     |
| R          | 150        | 0.08                   | 0.5                 | ^        |
| S Amine    | 4          | 0.8                    | 200                 | 281.7    |
| R Amine    | 7          | 0.005                  | 0.71                | ^        |

```
Questions for Next Lecture
1. Why would reactive oxygen species affect the KrmI gene negatively?
2. Why might KrmI not be able to add iodine to the 5-HT?
3. The paper doesn't mention how Flavin is used in this reaction. What does it do? I know that flavin is usually involved in redox reactions.
```

# Friday, Sep 15, 2023
###### Topic: **Enzyme Discovery**
Lecture Link: [Enzyme Discovery](https://canvas.ubc.ca/courses/126518/files/28538712?module_item_id=6151064)

## Todo/Assignments

- [ ]

## Notes

### Where Do We Get Enzymes?

Chemical Vendors!

Gene Synthesis!
- Recombinant Expression
- Cell Free Protein Synthesis

"I used all the malic enzyme"
"what."

Affinity to enzyme substrate can be used to make a specific chromatography matrix that selects by that affinity (ADP)

### Expression Vectors

- Plasmid $\rightarrow$ 1-10kb insert
- Cosmid $\rightarrow$ 25-35kb inserts
	- Contains $\lambda$ cos DNA sequence
	- $\lambda$ virus packages any DNA with the cos sequence
	- [ ] How are cosmids assembled?🔼
- Fosmid $\rightarrow$ 25-45kb inserts
	- Uses F-factor and F-pilus
	- Better than cosmid.
- Bacterial Artificial Chromosome (100-200kb)

### Metagenomics

#### Sequence-Based Approach

BLAST and Align into a Web Logo, find consensus sequences. (40% homology is a good number)
Design primers based on the consensus sequences. :: Degenerate oligonucleotides

#### Function-Based Approach

Next lecture... [[#Monday, Sep 18, 2023]] (change)

# Monday, Sep 18, 2023
###### Topic: **Continuing Enzyme Discovery**
Lecture Link:

## Todo/Assignments
N/A

## Notes

#### Function-Based Approach cont.

**Why is hit rate so low?**
Start of translation is AUG in E. coli, but some bacteria can have different translation starts like GUG or something.

There may also be secondary structures in mRNA at start site that the E. coli might not recognize, or otherwise.

Diversity of library can skew or miss results. Typically a very low number of putative enzymes can actually be used as biocatalysts.

*More:*
- Gene orientation might be wrong!
- Assay may have low throughput/signal noise ratio
- Gene expression efficiency
- Gene cluster may remain absent in absence of stimulus
- Post-translational needs

# Wednesday, Sep 20, 2023
###### Topic: **More On Metagenomics + Enzyme Engineering**
Lecture Link:

## Todo/Assignments
N/A

## Notes

### Sequence-Based Approach

#### Halogenation

Important for improving bioavailability and bioactivity of molecules.

In chemistry, inserting a halogen at a specific, regioselective site is difficult and often uses noxious reagents, etc.

Marine organisms like to halogenate things, I guess.

*Keramamides*
- Halohydroxytryptophan motifs

- NRPS make cyclic polypeptides, and they are typically similar
	- Should be in gene clusters, so new halogenases should be in gene clusters too.
	- Amplify based off of NRPS degenerate primers, and look in the middle.

### When To Use Either Approach

**Function-Based**
- Needs a high throughput way to screen the enzymatic functions.

**Sequence-Based**
- Need to be able to create the degenerate primers based off of known data.

### Protein Engineering!

**Why do it?**
- Stabilize
	- Temp, pH, solvents
- Improved substrate reactivity
- Expand substrate scope, impart catalytic promiscuity
- Improve or invert stereoselectivity 
- More...

**How do it?**
- Rational Design
- Directed Evolution

# Friday, Sep 22, 2023
###### Topic: **Error Prone PCR**
Lecture Link:

## Todo/Assignments

- [ ] Problem Set 📅 2023-09-26 

## Notes

### Producing Errors in PCR
- Create sequence diversity by random point mutagenesis
- Mutation rate adjusted to one to two amino acid substitutions per gene
	- Skew concentration of dNTPs
	- Introduce $\text{Mn}^{2+}$ instead of $\text{Mg}^{2+}$

| Substitutions | Number of Variants |
| ------------- | ------------------ |
| 1             | 3800               |
| 2             | 7 million          |
| 3             | 9 billion          |
| 4             | 8 trillion    ff   |
| 5             | 6 quadrillion      |

Spontaneous mutations occur with frequency of 10^-10 to 10^-9 of wrongly incorporated nt/bp per cell division.

Goal: 1-10 nt mutations per 1000 bp.

Minimize bias by making multiple libraries using different polymerases.

Incremental changes in protein activity.

#### Example: Single Point Mutations
Changing one base, what could these amino acids become?

##### Serine (UCN)
|         | **1st Base**  | **2nd Base**                  | **3rd Base** |
| ------- | ------------- | ----------------------------- | ------------ |
| *Codon* | ACN, GCN, CCN | UGN, UUN, UAN                 | UCN          |
| *AAs*   | Thr, Ala, Pro | Cys, Trp, Phe, Leu, Tyr, Stop | Ser          |
| *#*     | 3             | 5 + Stop                      | 1            |
Leaves out the charged amino acids. Doesn't dramatically change the functionality.

##### Valine (GUN)
|       | **1st Base**           | **2nd Base**           | **3rd Base** |
| ----- | ------------------ | ------------------ | -------- |
| *Codon* | CUN, AUN, UUN      | GAN, GCN, GGN      | GUN      |
| *AAs*   | Leu, Ile, Met, Phe | Asp, Glu, Ala, Gly | Val      |
| *#*     | 4                  | 4                  | 1        |

Degeneracy means that 6 of possible 19 amino acid substitutions are possible (one nucleotide change).

To access codons for other amino acids either two or three point mutations are required.

- [ ] Life or death: could you destroy function on purpose, then work from there?


# Monday, Sep 25, 2023
###### Topic: **DNA Shuffling Mutagenesis**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Frances Arnold - DNA Shuffling

***Engineer***
**Nobel Prize for Chemistry in 2018**

Randomization by recombinance.
Put homologous genes together, recombine, screen, recombine, screen...
Larger access to sequence space than epPCR.

### How to Shuffle Genes

Low concentration of gene (1-0.1ng per 50$\mu$L)
Primers are more (100ng per $\mu$L)
**This is just PCR**.

You use DNAse 1 to fragment the DNA.
Then, PCR without oligos to do some PCR recombination.
Average of 1-4 crossovers.
THEN you add fwd and rev primers so you only get full length transcripts.

Requires high level of sequence identity!

Its like PCR it has to anneal enough to be extended.

### StEP

Crazy, wacky, hate it.
PCR with super short annealing and extension.
