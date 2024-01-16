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
