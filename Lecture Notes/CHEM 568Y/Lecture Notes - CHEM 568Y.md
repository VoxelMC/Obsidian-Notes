Class: #BIOC407 #Courses 
***

# Thursday, Jan 11, 2024
###### Topic: **Lecture 2**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Magnetization

- B_0
- $\alpha$ aligned
- $\beta$ anti-aligned
$$
\omega = 2 \pi \nu_{0}= \gamma B
$$
B $\rightarrow$ $B = B_{0} + B_{local}$
B_0 is BIG
B_local is TINY

### PPM

What does it mean?
1 ppm = Hz/1 million Hz (Hz/MHz)

1 ppm = 400 Hz in a 400 MHz instrument.

If the resonant freq. of a proton is 400 MHz
So, 1 ppm is a millionth of that ($\frac{1}{1000000}$), which is 400 Hz.

Why do we do this?
- Same scale for different magnets!
	- Thus, ppm $\rightarrow$ chemical shift $\delta$ is independent of field strength.
	- **Coupling constants do not change with field strength, but shifts do not.**

#### Relationship between shift and field-strength
Takeaway: **COUPLING CONSTANTS DO NOT CHANGE IN Hz, BUT SHIFTS DO NOT**

Thus, a higher field strength ==> peak resolution, but not better at reading multiplets.
==> Does not deconvolute the multiplets.

### Diamagnetic Anisotropy (DmAn)

**!!!**
It drives the chemical shift of EVERYTHING, not just pi systems.
$B_0$ causes electrons to oscillate, creating a locally induced magnetic field $B_i$.

In benzene, the middle magnetic field is weaker because the local $B_i$ the induced magnetic field is opposing $B_0$
Outside, opposite

How can we tell? Use 14-annulene
Protons on the outside are 9 ppm; protons on the inside are **-3**.

DmAn also determines alkenes.

Note, however, that ALL NUCLEI DO THIS. They have spin (?).
- More $e^-$ density, higher magnetic field. More nuclear shielding from the magnetic field.

F-C-H expected (deshielded)
I-C-H carbon is super shielded

### Shifts 

![[Lecture Notes - CHEM 568Y Th 11-Jan 2024 09.59.excalidraw]]

1 Alkyl stuff
2 Stuff near carbonyl, phenyl, or halogens
3 Stuff near N
~>3.5 Stuff near O
5 Vinyl stuff
7-8 Aromatic stuffs
9 Aldehydic proton
12-13 carboxylic acids

Carbene H also around 9
Metal hydrides ~ -10

Amides -> Lovely range that is different from NHs
- NH is less spread out than OH, but they go around
- NH is always broad because it's quadrupolar
- Amides are broadened

> Carbon shifts calculate well, because they are not very sensitive to their environment.

Carbon shifts
Superimpose and find that they are pretty similar

| Shift | What?                   |
| ----- | ----------------------- |
| 10    | Alkyl                   |
| ~40   | N,X                     |
| 70    | O                       |
| 120   | enes and start aromatic |
| 160   | end aromatic            |
| 180   | Esters and amides       |
| 220      | Aldehydes and ketones                        |

Phenol or phenyl ester -> 160
Benzene -> 122.5 ish
> 200 is the magic line! Left, `ald` and `ket`; right, `esters` and `amides`.

Silverstein -> Theory is simplified but correct
- The second half of every chapter is `So you have X, here is what you could see.`

### Spin Coupling

> It's cooler than you think!

$\alpha$ --> Increase the field --> Increase the frequency of the peak
Inverse for $\beta$.

Note, however, that this is **not** through-space. It is through a bonding matrix because electrons are magnets and have spin. This is done *via* orbitals:
- Electron density between the nuclei matters a lot; and
- Orbital alignment between the two nuclei matters a lot.

![[Lecture Notes - CHEM 568Y Th 11-Jan 2024 10.22.excalidraw]]

$^3J$ coupling (3-bond distance).
$^4J$ if things are perfect.
$^2J$ can be unmeasurably small or large (bond-angle dependent)

`Aldehyde` proton 3 bonds away from an alkyl chain. What happens?
- $^3J$ is about 1-2 Hz
	- Why? Poor electron density of the carbonyl carbon.
> Electron density of a carbonyl carbon is **0.4 of a charge** (acetone)

`Styrene`
- Z bond is 14 Hz
- E bond is 20 Hz
- $^2J$ of terminal bonds is ~1-2 Hz (mark of a terminal alkene)

Karplus relationships help predict changes in $^{2}J + ^3{J}$ with dihedral/bond angles.

### Main Chunks

- Coupling

- Integration
- NOE

### Next

Relaxation on Thursday
Karplus plots next week

RAvi and Will

# Tuesday, Jan 16, 2024
###### Topic: **Lecture 3**
Lecture Link:

## Todo/Assignments

- [ ]
## Notes

### 90 Degree Pulse

bulk B0 in +z direction

magic hand is RF transmitter, rotate the cone by 90 degrees, so it goes in a way
letys say all pointing to -x.
Let go, and everything above X-Y plane goes to $\alpha$ and everything below now goes to $\beta$ 
now we have new populations, each split populations
So then, you get $P_{\alpha}= P_{\beta}$
But it leans to one side
so then bulk magnetization points to -x instead of +z

This is now our bar magnet which we can actually measure.
The bulk magnetization now precesses (or rotates, in this case) at the Larmor frequency.
As the magnetization rotates around the Z axis, and the coil is around the sample, you can detect the current in the coil 
If the magnetization did not return to +z, the FID would be a sine wave (as the magnet is rotating)
But since it does, it looks as though it is (and it is) a decay.

2 differences from the ground state:
- $P_{\alpha}= P_{\beta}$ 
- Coherence (bulk magnetization put into the X-Y plane).

### Relaxation Pathways

Both are able to occur independently of one another. 
Both have multiple ways of occurring, but also have a primary way of it happening.
This is the means by which the bulk magnetization returns to the +x direction.
Both are exponentials and have half-lives ($t_{\frac{1}{2}}$)
**T2 is always faster than T1**

#### T2 - Loss of Coherence

> *Faster than T1. Thus, we are never limited by T2.*

Look at the diagram in the notes with 4 cones, and insert here.

Rotating frame -> observing from the center of the axis

##### Field Homogeneity

T2 occurs primarily through field heterogeneity, causing some systems to precess faster or slower due to stronger or weaker magnetic fields in the tube. Can be reduced by stellar shimming...?

##### Tumbling

It doesn't take anything to rotate a molecule
kHz MHz GHz. Thus, molecular tumbling can be a problem.

Benzene tumbles!
It is also a magnetic field.
Thus, it is an OSCILLATING MAGNET.
> Chemical Shift Anisotropy!
- If the tumbling freq. is fast, it doesn't do much for T2.
	- Averages out in the time-scale of an NMR experiment.
- If slow, it's reasonable that it probably doesn't average out (in that time frame).
	- Thus, it is intrinsic to molecular size and temperature.
		- Bigger and colder -> slower tumbling.
- For a given solvent viscosity, the bigger the molecule is, the faster T2 will be by this method.

###### Tumbling Rates

Look at chart

The bigger the molecule, the slower its average tumbling rate will be.
Thus, as molecular weight increases, the T2 relaxation rate gets shorter and shorter (another chart).

### T1 Relaxation

Often called spin-lattice relaxation
Same physical phenomenon is the nOe.

##### Spin-Lattice Relaxation
Depends on the tumbling rate as well.
Nuclei do not experience the outside world. We only experience their magnetic fields.
- They stay aligned with or against the applied magnetic field.
If the nuclei rotate at Larmor frequency around a C13 atom, in this case, it will induce beta to alpha (or vice versa) transitions, just like a pulse would! Thus, you can return to the ground state faster, which is bad.

Looking at the tumbling graph above, very large molecules will have few rotations near the Larmor frequency. However, this is also true of really small molecules.
The sizes between these are near the peak efficiency for T1.

### Next Thursday

Damaskanone
- Tabulate the carbons from low to high chemical shifts.
- Give a first good guess about the assignments.

*Low*
A
B
...
$\omega$ 
*High*