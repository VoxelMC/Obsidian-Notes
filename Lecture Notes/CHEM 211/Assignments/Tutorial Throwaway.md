# Lab 3

## Materials and Methods - ChatGPT Input

### Materials
- Spectrophotometer: Thermo Scientific Spectronic 200+
- 100 mL Volumetric Flasks: Pyrex
- 1 cm Cuvettes: Cole Parmer 
- Cuvette Holders: Unknown Brand
- Analytical Balance: Johns Scientific Inc. ER-120A
- Fisherbrand Pipetboy
- San Joaquin Valley Crystal Purple Merlot
- Citric Acid Buffer


### Methods

**Determination of Wavelength Max**
1. Appropriately Label Volumetric Flask 1.
2. Weigh 0.010 g of crystal purple merlot colorant.
3. Dissolve in 100 mL volumetric flask with deionized water.
4. Fill a cuvette 3/4 full with coloured solution.
5. Zero the spectrophotometer using a cuvette filled with deionized water.
6. Measure absorbance of stock solution at 520, 535, 550, 565, and 580 nm. 
**Determination of Purple Merlot Extinction Value**
1. Appropriately label a volumetric flask 2.
2. Weigh 0.200 g of crystal purple merlot and dissolve in citric acid buffer in a 100 mL volumetric flask to prepare a stock solution.
3. Transfer 20 mL of the stock solution to a new volumetric flask labelled "0.2 dilution" 
4. Transfer 10 mL of the stock solution to a new volumetric flask labelled "0.1 dilution"
5. Fill both volumetric flasks to the stop line with CAB to make the respective dilutions.
6. Cap and invert flasks
7. Zero spectrophotometer using citric acid buffer
8. Measure absorbance at $\lambda_{max}$  
**Determination of Unknown Concentrations**
1. Prepare a dilution series starting from a 2 mg/mL stock solution. Transfer 75 mL of stock and fill to the 100 mL line to make a 3/4 dilution. Do this 5 times.
2. Zero at λ_max with deionized water.
3. Measure absorbance of each standard, starting from the lowest concentration to the highest.
4. Last, measure absorbance of unknown solutions.
5. Performed in triplicate pseudoreplicates.

### Calculations

1. **Average Absorbance (Standard Series 1 Solution):** Calculated using Excel AVERAGE function: \(0.128 \, \text{AU}\)
  
2. **Standard Deviation of Absorbance (Standard Series 1 Solution):** Calculated using Excel STDEV.S function: \(0.00057735 \, \text{AU}\)
  
3. **Standard Error (Error Bar) for Standard Series 1 Solution:** \( \%RSD = \frac{0.00057735}{\sqrt{3}} = 0.0003333 \, \text{AU}\)
  
4. **Extinction Value (EV) Calculation:** \(EV = \frac{0.2}{0.2018 \times 1.100} = 27.25470763\)
  
5. **Average Extinction Values:** Calculated using Excel AVERAGE function: \(24.4301288 \approx 24\)
  
6. **Concentration of Unknown Solution (Unknown 1):** \( \text{Concentration} = \frac{(0.183 - (-0.00842))}{1.581866} \approx 0.12101 \, \text{mg/mL}\)
  
7. **Slope and Y-intercept Standard Deviations, etc.:** Calculated using Excel LINEST function
  
8. **Squared Standard Deviation of X:** Calculated using Excel DEVSQ function: \(0.001363 \, \text{mg}^2/\text{mL}^2\)
  
9. **Number of Points Used for Calibration:** Calculated using Excel COUNT function: \(3\)
  
10. **Mean of Y Values on the Calibration Curve:** Calculated using Excel AVERAGE function: \(0.081 \, \text{AU}\)
  
11. **Number of Replicates Used for yc:** Calculated using Excel COUNT function: \(3\)
  
12. **Mean of Replicate Analyses of c:** Calculated using Excel AVERAGE function: \(0.183 \, \text{AU}\)
  
13. **Standard Deviation of Concentration of Unknown Solution (sc):** \(sc = \frac{0.000229391}{|1.581866|} \times \sqrt{\frac{1}{3} + \frac{1}{3} + \frac{(0.183 - 0.081)^2}{(1.581866^2 \times 0.001363)}} \approx 0.000279 \, \text{mg/mL}\)
  
14. **95% Confidence Interval for Concentration of Unknown Solution:** \(95\% \, \text{CI} = 12.71 \times 0.000229391 \approx 0.002916 \, \text{mg/mL}\)