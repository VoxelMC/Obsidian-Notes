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

Raph and Will

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

Damascone
- Tabulate the carbons from low to high chemical shifts.
- Give a first good guess about the assignments.

*Low*
A
B
...
$\omega$ 
*High*

| Shift | Assignment | Details |
| ----- | ---------- | ------- |
| 0.73  |            |         |
| 0.82  |            |         |
|       |            |         |
|       |            |         |
1H NMR (400 MHz, cdcl3) δ 7.26, 6.75, 6.61, 6.18, 6.02, 5.48, 2.77, 1.95, 1.86, 1.79, 1.76, 1.58, 1.43, 1.38, 1.34, 1.04, 0.89, 0.82, 0.73.

# Thursday, Jan 18, 2024
###### Topic: **Lecture 4 - Damascone*
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

Hard to tell from C NMR that there is or isn't benzene.

# Tuesday, Jan 23, 2024
###### Topic: **Lecture 5 - T1 Relaxation**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### The Power of Pulses

- **Hard Pulses** - Very short
	- 90 degree pulses for acquisition
	- Broadband decoupling *(lots of $\alpha$ - $\beta$ transitions)*
	- Selective decoupling
	- nOe irradiation *(fewer $\alpha$ - $\beta$ transitions)*
- *Tickly Pulses* - Very long

$B_0$ is quite homogenous, but $B_1$ is pretty crude. $B_1$ is the field generated by the transmitter.

#### Broadband Decoupling

Oscillation between alpha and beta, so that the coupling protons blur out, and average. Thus, not effecting chemical shift.

When decoupling the proton range in a C13 NMR, the carbon sees the average energy because its neighbour protons are rapidly transitioning, making it a singlet.

- This makes neighbour spins have no overpopulation, so $P_{\alpha}= P_\beta$.
- Wide chemical shift range, so fairly high power. 
	- Smaller ranges -> lower power.

#### Selective Decoupling

You can decouple just one peak using lower energy. 
At saturation, $B_0$ is zero. So irradiated peak is gone, and those that couple to it are now reduced to the correct multiplicity.

Selective Irradiation is a super useful way to get structural information if peaks overlap or you cannot make out j-values.

- Eliminates (averages) coupling to that population.
- This can be done with "presaturation"
- Can use this to suppress solvent peaks.

#### nOe Irradiation

$\alpha$ - $\beta$ transitions are relatively rare
- **for the irradiated population, $P_{\alpha}= P_\beta$.** 

The 1D NOE takes the difference of the spectra, subtract the normal from nOe (tickled) spectrum. 
- No nOe, only difference is an erased peak because both spectra are the same.
- +ve nOe, big peak - normal peak, appears as a normal peak
- irradiated peak is negative

# Thursday, Jan 25, 2024
###### Topic: **Lecture 6 - Indenone**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes
Check the excel

# Tuesday, Jan 30, 2024
###### Topic: **Relaxation +**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

**Recap:**
- Other magnets tumbling around your nucleus create an oscillating magnetic field
- If this oscillation is equal or around the Larmor frequency, it induces a spin state change from $\alpha$ to $\beta$
- Because it is at Larmor, it is a single quantum phenomenon
- If this was the only route, there would be NO nOe.

Energy just dissipates, and so doesn't go back into molecule that creates the field. Kind-of boring!

> There are two other pathways, very important!

### Coupled Double Transition

$\alpha$$\alpha$ flips to $\beta\beta$
Occurs at the SUM of the two larmor frequencies
-> Double Quantum (dq)

Small molecules is a range where this is permissible. There is population at double quantum and single quantum.
For larger molecules (macromolecules), this is not true because the population is very small at double quantum.

#### What does this mean for nOe?

**Double quantum cross-relaxation**

```
  Ha Hb
  |  |
--C--C--
  |  |
```

1. Irradiate `Ha` (tickle)
	1. Equalize the population of the alpha and beta states
	2. `Hb` no longer couples to `Ha`, and compensates the field (solving `Ha`'s problems)

It's a cycle
1. Irradiate, equalizing alpha and beta (saturating `Ha`)
2. Cross-relaxation occurs, where betas dropping to ground state induce a beta in `Hb` to drop as well 
3. But since you keep irradiating, this doesn't affect `Ha`, but it affects `Hb`
4. Stop irradiating (mixing) so things go back to normal, but `Hb` has a higher $M_{z}$

Thus, `Ha` goes to $M_{z}= 0$ and `Hb` goes to $M_{z}> M_{0}$

*By how much?*
- Not a lot! <20% single digits very normal
- Falls off dramatically \frac{w}{ through-space}distance ($\frac{1}{r^6}$)

### Coupled Transition alpha-beta -> beta-alpha

$\alpha\beta$ $\rightarrow$ $\beta\alpha$
Occurs at the difference between two Larmor frequencies. **Zero-quantum (ZQ)**

Differences of about a few hundred Hz, instead of hundreds of MHz in single- and double-quantum.

There is a very small population of small molecules, and a very large population of macromolecules.
- No nOe effect, so why do we care about it in macromolecules?
	- The zero-quantum effect is **negative** (makes the peak smaller, not bigger).

Thus, for

```
  Ha Hb
  |  |
--C--C--
  |  |
```

> `Ha` has $M_{z}=0$ and `Hb` has $M_{z} < 1$

It:
- has a small negative effect;
- is seen in very large molecules; and
- occurs at the difference in Larmor frequencies.

Do these nOes cancel out in a range?
- Yes, around 1 kDa. 
	- They show little-to-no nOe.
- ROESY uses a spin-lock instead of continuous irradiation, so you don't see zero-quantum, so you can measure nOe in those molecules.

**> Check notes for figures!**

It takes seconds to build up a good nOe difference. like t1

### Indanone

Official reference standard for the NMR

Crazy spin-coupling.

### NOESY

Why nOe over NOESY?
- 1D is faster
- NOESY suffers from COSY artifacts
- You can mathematically get distance numbers from rigid molecules, though VERY hard.
	- Not practical for elucidation, but sometimes you could do it!
	- If you have a peptide and a substrate bound to it, you don't see correlation between the two of them.
		- You do, however, get an nOe, so you can calculate the distance between the substrate and the peptide.
		- **Very cool!**
- 

### Next
- Spin-echo
- Attached proton test

# Thursday, Feb 01, 2024
###### Topic: **Carbon NMR**
Lecture Link:

## Todo/Assignments

- [ ] Next Homework: **Inverse Gated Experiment**
	- Measure the 90-degree pulse width
	- Measure t1 at the 90-degree pulse
	- Design your carbon pulse sequence with an appropriate delay, inverse-gated
	- Integrate it very carefully
	- Get J values from a gated experiment
		- 2 peaks
		- Change `dm` from `yyy` to `yyn`

## Notes

> What is going on in a carbon? Why do we make these choices?

### Standard Carbon Experiment

During 1H Decoupling, nOe develops on nearby carbons through double-quantum processes
- nOe buildup takes time on the order of seconds
- Also takes time on the order of seconds to decay (generally through T1 pathways)

Decoupling is effectively instantaneous
- Rapidly flipping

We can choose to turn on the decoupler during the initial delay and build up nOe, and turn it off and look at coupled spectrum
>NMRkup

Smaller peaks are quaternary because they are the furthest from a proton and thus build up less of a nOe.

#### No Decoupling

-> nOe is not enhanced, basically terrible.
Terrible signal to noise (2 or 3 to 1).

There is multiplicity though.
- A little bit too much? Carbon sees 1J, 2J, and 3J coupling. (2 and 3J are the same Hz)

#### Gated Experiment

Decouple during d1, but then turn it off. The decoupling goes away instantaneously, but the nOe decays over seconds.
- Same as no decoupling during acquisition, but the nOe enhances the signal to noise!

The quartet of quartets (indanone) is much prettier!

Not often done, but sometimes done.

Problems:
- Cannot tell the number of carbons from integration

#### Inverse Gated

**Short**

if d1 is short, it doesn't work. (1 second)
Running the inversion recovery, 

t1 increment * 5 (half lives)
if 4 seconds, 20 seconds. That's a lot more than 1 second.

**Long**

nOe has time to die off
If the nOe is still present, the peak is not as prominent or integrated correctly.


### 90-Degree Pulse Width Changes

Same for all of your carbons and protons

The excitation pulse needs to hit the molecule:
- **Mistuning:** One challenge is if it is directly on the frequency. If it is off, it will be weaker (need a longer pulse).
- **Impedance Matching:** If the impedances of the coil and sample are not matched, longer pulse is needed because more of the signal is reflected
	- This is also solvent-dependent
		- The differences are not huge. 

Fix this by tuning and matching.
- Do this every time we change the X-channel.

How do we make a 30 thousand dollar mistake???

Array pulse-width to find it.
- The data is VERY pretty.

### Summary of Carbon

> nOes take time, and decoupling does not.

### Shimming the Magnet

The probe has a lot of little coils! These are shimming coils.

There are a few types of shimming coils.

Z -> Spinning Shims
X & Y -> Non-spinning Shims

X & Y are averaged out when the sample spins, so they can be more coarse when you spin the sample. 
- Most people don't do anything with these, however
- if they are wrong, they can cause artifacts.
	- The most common is called "spinning sidebands".

#### Spinning Sidebands

These peaks show at +- the rate of spinning

> Fun fact: bond length between isotopes decreases with heavier atoms. This is because the zero-point vibrational frequency is lower for heavier atoms.

> Another fun fact: if you want to integrate contaminant peaks, you can use the 13C-1H side peaks because you know they are 0.5% of the primary peak.

Spinning does not help with Z problems.
- Often, there are experiments where we cannot spin the sample (nothing with a gradient).
	- X and Y need to be very good for things like 2D experiments.

Shimming might be in Jacobson.

# Tuesday, Feb 06, 2024
###### Topic: **...**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

Evolution, the APT or INEPT + the spin echo

### Chemical Shift Evolution

Refer to the drawing in Neptune book.

Take CH3Cl3

```
  CH3-Cl3
  ^
~140 Hz
```
Alpha-neighboured carbons precess more rapidly, opposite for beta.

#### Reference Frequency between Carbon Doublet Peaks

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 12.17.excalidraw]]

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 12.27.excalidraw]]

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 12.34.excalidraw]]

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 12.42.excalidraw]]

So, **At $τ = \frac{1}{J}$**, *should* be 
- C -> +ve
- CH -> -ve
- CH2 -> +ve
- CH3 -> -ve

This assumes that the reference frequency is at the multiplet frequency.
- We *transmit* the reference frequency and subtract everything from *that*.
- Only works for peaks *at exactly the reference frequency*.

##### Scalar Evolution

The only time this is independent of chemical shift evolution is when δ = $ν_0$

> **Time for the Spin Echo**

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 12.48.excalidraw]]

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 12.56.excalidraw]]

#### APT Pulse Sequence

What if we want to see the effects of scalar evolution but remove the effects of chemical shift evolution?
- Chemical shift evolution is always happening
- Scalar evolution can be turned off by turning on the decoupler for the coupled nucleus.

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 13.02.excalidraw]]

S/N of an APT is less than a normal 13C spectrum due to a delay of 2τ after the 90-degree pulse
If there is no spin and viscous solvent, the T2 can also be refocused. 

> That's pretty cool, but it's also kind of redneck.

![[Lecture Notes - CHEM 568Y Tu 06-Feb 2024 13.11_0.excalidraw]]

### Homework Next

- Put some analysis on the homework results.

# Thursday, Feb 08, 2024
###### Topic: **...**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### Lock Scan and Shimming

The number is meaningless; it's the changes that matter.
Try to be around 60-80.
This magic finger measures the deuterium signal.
If you have a magic finger on the acetone peak, it will keep track of the drift.

Power depends on the amount of deuterium in the sample.

#### Order of the Shim

- Sequential refinements in that direction
- Looks like p, d, and f orbitals
- X, Y, and Z affect the entire line shape
	- Higher-order shims affect the baseline more closely.
- Even-order shims widen one side not the other
- Odd-order shims do both sides

- C means coarse. They are different shim coils, though. So you have to adjust them both!!

If short and broad
- Its a low order because it affects top to bottom
- Its an odd order because it affects both sides.

Z2 + affects the left of the peak, - affects the right of the peak.\\

If you change higher order, like Z3, gotta change Z1 again. But not Z2 because its symmetrical and Z2 is not.

> Amazing integration requires great higher-order shimming.

The goal when shimming is to bring the lock signal up.

Do X and Y, then gradient shim for Zs.

The gradient is flat because there is a linear field distribution in the sample, broadening the peak A LOT.

Long decay, thin peaks
Short decay, wide peaks

How much paramagnetic metal gives rise to a bad peak?

Particulates = T2 relax bad

if not many peaks, should be no beat freqs. 

`df` shows the FID
`ds` shows spectrum

### NMR Architecture

![[Lecture Notes - CHEM 568Y Th 08-Feb 2024 10.39.excalidraw]]

If it's getting too hot, find the VT box with red (or green) lights and flick the black switch!!!

# Tuesday, Feb 13, 2024
###### Topic: **...**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### What Have We Seen

Scalar and Chemical Shift evolution complete.

### Doing More Math

Coherence Transfer is Magic Math

You cannot describe 2D NMR with just a vector model.

> We have already talked about one type of polarization transfer
- **the nOe** - a T1-like process

We will now work towards **coherence transfer.**

- nOe
	- Through space
- Coherence transfer
	- Through scalar coupling
	- Through bond

### The INEPT

HOHAHASECSYTOCSY?

**Insensitive Nucleus Enhancement by Polarization Transfer**

![[Lecture Notes - CHEM 568Y Tu 13-Feb 2024 12.07.excalidraw]]

INEPT gives a 4-fold increase in carbon signal
That's why DEPT gives very good S to N on protonated carbons

### Product Operator Formalisms

**Notebook**

In an isolated C-H system

```
C -- H
^ 
S
```

IDEA FOR NMRkup: make interactive sequences where you can hover and describe what each pulse/delay does and why

#### Chemical Shift Evolution

Notebook

#### Scalar Evolution

Notebook

#### Pulses & Effect on Product Operators

Notebook

# Tuesday, Feb 27, 2024
###### Topic: **More Sequences**
Lecture Link:

## Todo/Assignments

- [ ]

## Notes

### INEPT

$Iz \rightarrow Iy \rightarrow 2I_xS_z \rightarrow -2I_zS_x$
- We always write the observable first. **BUT**, remember we started with `1H` coherence, from `1H` overpopulation, which is 4x greater than the 13C overpopulation
 - Thus, $-2I_zS_x$ is really $4(-2S_xI_z)$
 - With the BUTs, this only works for a peak @ reference frequency. Other peaks also have phase issues to solve due to chemical shift evolution. Thus, use Spin Echo!
	 - This is the refocused INEPT.

In INEPT, antiphase peaks cancel each other out.

This works perfectly, unless the peak is a triplet or quartet. This is because of the dependence on 1/4J, so you cannot see a C, CH2, or CH3!
- Works the same as a DEPT90. (unless its a terminal alkyne?)

For a doublet in the second spin echo, 
- $2S_xI_z \rightarrow 2S_xI_z \cdot cos(\pi J \Delta) + S_y \cdot sin(\pi J \Delta)$ where Δ is the full second evolution time.
	- if Δ = $\frac{1}{2J}$, $\frac{\pi J}{2J}$, $cos(2\pi) = 0$, $sin(2\pi) = 1$
- The rest is on paper, add here later.

# Tuesday, Mar 05, 2024
###### Topic: **Gradient**

## Todo/Assignments

- [ ]

## Notes

### The Gradient

In a tube, you want the magnetic field to be constant in all directions (throughout the measurement window).
-> However, sometimes it is cool to make it *very predictably* not constant. This is where the **gradient** comes in.
- The gradient is linear up and down the sample. 
	- Weaker at the top and stronger at the bottom.
	- Faster precession at the bottom then, and vice versa.

$G_z$ (gradient field) is VERY weak  in comparison to (0.1% of $B_0$)
- Field is now $B_g(z) = B_0 + G_z(z)$
- Not originally developed for NMR. 
	- It is originally for MRI.
		- MRI measures the water peak in a gradient (closer is stronger, etc.)
		- (MRI also uses relaxation time now, just so you know :))

**Thought Experiment**
![[Lecture Notes - CHEM 568Y Tu 05-Mar 2024 12.07.excalidraw]]

In A, time 1 has a spectrum (duh) but time 2 has no more spectrum.
In B, time 1 and 2 are the same, but in time 3 after the -G pulse, there is coherence again!
- However, during that time in time 2, chemical shift evolution was occurring.
- To eliminate CSE, we do a Spin Echo! Obviously.

*What happens to our gradient during a 180˚ pulse?*
It flips the handedness. CCW to CW, vice versa.

You can make a PFGSE to reverse CSE.

![[Lecture Notes - CHEM 568Y Tu 05-Mar 2024 12.17.excalidraw]]

What if I do this to sucrose sample?

![[Lecture Notes - CHEM 568Y Tu 05-Mar 2024 12.29.excalidraw]]
1. What is the fate of the water peak?
	1. It remains the same as before with no CSE.
	2. Signal because it is coherent.
2. What is the fate of the other peaks?
	1. Affected by the gradient, but since did not receive the 180$\degree$ pulse, the second G pulse makes for $2G_z$
	2. No signal because it is not coherent.

We can use this to make the INEPT better.
- A main problem with the INEPT is:
	- What happens to all of the carbons that don't receive the polarization transfer?

### Improving the INEPT again

![[Lecture Notes - CHEM 568Y Tu 05-Mar 2024 12.33.excalidraw]]

After this sequence, there is still CSE. Let's get rid of it now.

![[Lecture Notes - CHEM 568Y Tu 05-Mar 2024 12.44.excalidraw]]
**AKA: gradient-selected refocused INEPT**

This pulse (Double PFGSE) uses the full INEPT sequence, with two gradient pulses.
- The second negative pulse is 4 times as strong because the C13 magnetic moment is weaker than the proton magnetic moment.
	- Remember that before the second 90 degree pulse, the coherence is in the protons, and after, the coherence is in the carbons. This is why the untwist is -4 times as strong.

> The ability to be twisted or untwisted depends on the strength of the nuclear magnet!

This sequence eliminates anything that was not 1H single-quantum coherent @ first gradient, and 13C single-quantum coherent @ second gradient.

#### Selection of a coherence pathway

Formalization:
Any pathway whose sum is 0 survives.

So, if 1H SQC's p = 4 and 13C SQC's p = 1, and G1 = 1 and G2 = -4, you can sum their products to get 0
$\sum p_iG_i = 4 \cdot 1 + 1 \cdot (-4) = 4 - 4 = 0$

| Pair      | Quantum | p =       |
| --------- | ------- | --------- |
| SI        | ZQ      | 3 (4-1)   |
| I(a)-I(b) | ZQ      | 0 (4-4)   |
| SI        | DQ      | 5 (4 + 1) |
Things that are 0 are detectable, things that are not zero are not detectable.

**How does this filter for failed coherence transfer???**
- This is normal. Any part of the system that is not antiphase does not transfer.
- Since there is a range of error, not all of it antiphases.

After evolution we should see some 2IySz + Sz
**If the experiment is:**
2IySz + Sz -- P -> 2IzSx + Sx
- (2IzSx is desired)
P = simultaneous 90(x) pulses on 1H and 13C.
First gradient: p(Gz) = 0(1) -> no effect in 13C z direction
Second gradient: p(Gz) = +1(-4) <- filtered out, 13C SQC.

##### Some practical bits
- We assumed that no molecules moved in the gradient on the z axis between gradients.
	- Spinners destroy all of the effect of the gradient. Give everything time to calm down before using the gradient.
- Gradients are not nucleus specific. This screws up our lock on deuterium temporarily.
	- Need a great lock for 2D experiments.

### Check this out: DPFGSE nOe!

![[Lecture Notes - CHEM 568Y Tu 05-Mar 2024 13.20.excalidraw]]


