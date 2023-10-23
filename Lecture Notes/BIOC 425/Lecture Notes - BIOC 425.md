Class: #BIOC425 #Courses 
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

- [x] Problem Set 📅 2023-09-26 [completion:: Oct 17, 2023 @ 02:52 PM]

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

# Wednesday, Sep 27, 2023
###### Topic: **Case Study: p-nitrobenzyl Esterase**
Lecture Link: [[Moore_Arnold_1996.pdf]]

## Todo/Assignments

## Notes

cbauy gruling jeponese cv resume ✅

epPCR $\rightarrow$ Shuffling Approach

# Friday, Sep 29, 2023
###### Topic: **Saturation Mutagenesis**
Lecture Link: [[Iterative Saturation]]

## Todo/Assignments

- [ ]

## Notes

### Saturation Mutagenesis

![[Codon Wheel.png]]

DpnI Digests of the plasmid with the gene, after methylation of gene then cloning, will destroy the plasmid entirely.

Make a primer with some Ns in it. 
Targets residues near the active site, or residues in flexible loop regions
Screen 3x n of possibilities colonies

#### Typically Used Codons

**NNK codon**
$\rightarrow$ 32 $\rightarrow$ 1024 $\rightarrow$ 32768 possible codons.

**NDT codon**
$\rightarrow$ 12 $\rightarrow$ 144 $\rightarrow$ 1728 possible codons.

### Warren L. DeLano

Created PyMOL
- [x] Try to use PyMOL. [completion:: Oct 17, 2023 @ 02:52 PM]
- [x] PDB [completion:: Oct 17, 2023 @ 02:52 PM]

# Wednesday, Oct 04, 2023
###### Topic: **3D Structures**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### B-Factor

### Iterative Saturation Mutagenesis

Design Oligonucleotides to completely change a specific amino acid. Specifically at parts of the active site.
**NNK**.

#### 22c Trick

If you change 3, you go from ~100000 to ~32000 colonies to screen, then with 22c-Tang it goes to ~22000.
12:9:1 of NDT:VHG:TGG
12:6:1:1 of NDT:VMA:ATG:TGG

### Computational Protein Engineering

$\beta$-Amino Acid Synthesis are of interest in the pharmaceutical world.

#### Rosetta Commons

**David Baker**
- [ ] David Baker, Rosetta - Summer Internships - Worth a look :)

- [ ] Read Roethlisberger Paper - Nature 2008

[Biocatalysis | Max-Planck-Institut für Kohlenforschung (mpg.de)](https://www.kofo.mpg.de/en/research/biocatalysis)

# Friday, Oct 06, 2023
###### Topic: **Computational Design**
Lecture Link:

## Todo/Assignments
N/A

## Notes

- [ ] Rosetta - Double Check This

# Wednesday, Oct 11, 2023
###### Topic: **Non-canonical Amino Acids**
Lecture Link:

## Todo/Assignments
N/A

## Notes

### Non-canonical Amino Acids

Any amino acid that is not incorporated into proteins.

### Unnatural Amino Acids

Non-canonical Amino Acids that are not present or found in nature.

### P.G. Schultz - Genetic Code Expansion

**Genetic code expansion** 

#### tRNA Synthetases

There is lots of variability between typical tRNA Synthetases.

tRNAs have Identity Elements and Anti-Identity Elements
Identity $\rightarrow$ I want THIS tRNA SYNTHETASE to modify me.
Anti-Identity $\rightarrow$ I don't want ANYTHING ELSE to modify me.
- Methylation of G73 of *S. cerevisiae* tRNA$_{\text{Asp}}$ prevents mis-aminoacylation by ArgRS synthetase.

Changing 3 bases can change tRNA Synthetase Specificity.

# Friday, Oct 13, 2023
###### Topic: **Metabolic Engineering**
Lecture Link:

## Todo/Assignments

## Notes

Common issues of redirecting flux in microbial factories.
- Poor expression of genes
- Toxicity of intermediate
- Cost of C sources
- Expression levels of enzymes are frequently dramatically higher than would be naturally found
- High expression robs flux of nts and AAs that could have been used for biomass production or desired product, decreasing titers and inducing stress responses (in the cells AND the researcher)
- You are fighting homeostasis

- [ ] 2 plasmids in the same host cannot have the same ORI...?

# Wednesday, Oct 18, 2023
###### Topic: **Artemisinic Acid: Case Study**
Lecture Link:

## Todo/Assignments

- [ ] Look at practice Midterm

## Notes

Artemisinin found after metabolic engineering, after a lot of looking for ADH and stuff.

- [ ] Nature Paper: Microbial supply chain for production of the anti-cancer drug vinblastine

2000 kg of leaves to get 1 g of product.

### Immobilized Enzymes

Glucose isomerase $\rightarrow$ Fructose
Sucrose mutase $\rightarrow$ **...**
Penicillin acylase $\rightarrow$ 6-APA
Thermolysin $\rightarrow$ Aspartame
Nitrilase $\rightarrow$ Acrylamide

#### Supports

Water-insoluble $\rightarrow$ polysaccharides or gelatin/albumin
Inorganic supports $\rightarrow$ silica

![[Pasted image 20231018162134.png]]

#### Entrapment

Inclusion in a polymer network (agarose, silica sol-gel)
Covalent attachment is required
Entrapment generally requires the synthesis of the polymeric matrix in the presence of the enzyme.

##### Silica Sol-gels
Hydrolytic polymerization of tetraethoxysilane
Drying of the gel leads to formation of cages
Can remove methanol from waste water
Used with whole cell catalysts rather than enzymes

**Hydrogels**
Immobilized using natural or synthetic polymers
![[Pasted image 20231018162338.png|50%]]

#### Crosslinking

CLEC or CLEA
crosslinked enzyme crystals/aggregates

Highly concentrated enzyme activity in the catalyst
Lower production cost due to lack of carrier

(NH3)2SO4 to precipitate, then add glutaraldehyde to crosslink them. Because it can crystallize because it is highly concentrated.

Amines react w/ aldehydes

![[Pasted image 20231018163114.png]]

#### Measuring Success of Immobilization

% Yield = $100 \times \frac{\text{Immobilized activity}}{\text{Starting activity}}$

Immobilization efficiency = $\frac{\text{Observed activity}}{\text{Immobilized Activity}}$

Activity recovery = $\frac{\text{Observed activity}}{\text{Starting Activity}}$

Example:
$$\% Yield = 100 \times \frac{80U}{100U} = 80\%$$

$$
\% Efficiency = 100 \times \frac{40U}{80U} = 50\%
$$

$$
\% Activity_{Recovery} = 100 \times \frac{40U}{100U} = 40\%
$$

**Do we need to do a specific change in amino acid, or just random degenerate for all amino acids**

**Does the primers work like this or like this**
![[Lecture Notes - BIOC 425 We 18-Oct 2023 16.44.excalidraw]]

# Friday, Oct 20, 2023
###### Topic: **Industry Enzymes**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

Emperical Rule: **Kazlauka's Rule**
Predicts how a lipase will react in terms of stereoselectivity in a lipase catalyzed reaction.

Lipases need no cofactors or coenzymes.
Used in everything, a very big industry.

Trans-esterification! Chocolate!

### Production of Naproxen

Dynamic Kinetic Resolution $\rightarrow$ Kinetic Resolution coupled to racemization of unwanted enantiomer. 
- Desired product must no racemize
- Enzymatic reaction needs high stereoselectivity
- Substrate must racemize faster than enzymatic reaction 
