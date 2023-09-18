Class: #BIOC425
***
# Wednesday, Sep 13, 2023
Topic: **Finishing Stereoselectivity**

## Todo/Assignments

- [ ] Remember My Blood Group

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

Next lecture... [[#Wednesday, Sep 13, 2023]] (change)