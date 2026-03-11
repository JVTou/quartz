---
date created: Thursday, June 5th 2025, 10:37:03 am
date modified: Wednesday, June 11th 2025, 9:50:00 am
---
# Abstract

This experiment investigates electromagnetic induction by observing and measuring the electromotive force (EMF) generated in a coil as a permanent magnet moves through it. Key methods involve dropping a magnet through a coil from various heights and capturing the induced EMF waveform using a digital oscilloscope. Qualitative observations will relate the EMF characteristics to the magnet's speed and the magnetic field's shape. Quantitative measurements will focus on the relationship between peak EMF and magnet speed, and the calculation of magnetic flux change by numerically integrating the EMF waveform. The principal conclusions are expected to verify Faraday's Law of Induction.

# Introduction

This experiment explores Faraday's Law of Induction, which states that a time-varying magnetic flux ($\Phi_{B}$​) through a circuit induces an electromotive force (EMF, $\epsilon$) in it. The induced EMF is given by:

$$
\epsilon(t)=-\frac{d\Phi_{B}(t)}{dt}
$$

For a coil with $N$ turns, this becomes:

$$
E(t)=-N\frac{d\Phi_{B}(t)}{dt} 
$$

The negative sign in the equation is a consequence of Lenz's Law, which indicates that the induced current will flow in a direction that opposes the change in magnetic flux that produced it. In this experiment, a moving permanent magnet creates a time-varying magnetic field, and therefore a changing magnetic flux, through a stationary copper wire coil. This change in flux induces an EMF in the coil.

The objectives of this lab are to:

- Investigate the characteristics of the induced EMF, such as its dependence on the speed and orientation of the magnet, using a digital oscilloscope.

- Verify Faraday's Law of Induction by observing the induced EMF and its relation to the rate of change of magnetic flux.

- Numerically calculate the magnetic flux through the coil.

The induced EMF is directly measured as a voltage waveform using a digital oscilloscope. The change in magnetic flux ($\Delta\Phi_{B}$​) can then be determined by integrating the measured EMF ($\epsilon(t)$) over time, based on the rearranged form of Faraday's Law:

$$
\Delta\Phi_{B}=-\frac{1}{N}\int_{t_{1}}^{t_{2}} \epsilon(t) \, dt 
$$

This integral represents the area under the EMF vs. time curve. When a magnet passes completely through the coil, the total change in magnetic flux is ideally zero, resulting in two distinct lobes (positive and negative) in the EMF waveform.

# Methodology
## Experimental Setup

The experimental setup consisted of a copper wire coil with number of coils $N=120$, a permanent horseshoe magnet, and a digital oscilloscope. We also used oscilloscope probes and a slab of cardboard to cushion the magnet's fall. The ends of the coil were connected directly to an input channel of the digital oscilloscope, as demonstrated in the following image:

![[Pasted image 20250605104836.png]]

## Procedure

1. Qualitative Observations: To observe the general characteristics of the induced EMF, the magnet was passed through the coil manually.

	- Varying Orientation: The magnet was passed through the coil with two different orientations (e.g., horseshoe end facing along the axis of the coil). Images of both waveforms were saved, and the shapes of the EMF pulses were described.
	- Varying Speed: The magnet was passed through the coil at different speeds (slow and fast). Observations were recorded on how the peak EMF voltages and pulse durations varied with speed.

2. Quantitative Measurements: For quantitative analysis, the magnet was dropped through the coil from various heights.

3. A soft cardboard slab was placed below the coil to cushion the magnet's landing and prevent damage. One partner held the coil, while the other dropped the magnet.

4. 3-5 different drop heights (3 cm, 6 cm, 9 cm) were chosen. These heights were measured from the bottom of the magnet to the top of the coil.

5. For each drop height (h):
    - The oscilloscope was set to DC coupling and single event trigger mode to capture a single EMF pulse. The trigger level was set appropriately (~50-100 mV) to avoid capturing noise, and the trigger slope was set to either rising or falling edge. Voltage and time scaling were adjusted to view the entire waveform without clipping.
    - The magnet was dropped through the coil, ensuring enough space below the coil to avoid any influence from the table on the magnet's fall before it completely exited the coil.
    - The peak positive ($\epsilon_{\text{peak+}}$) and peak negative ($\epsilon_{\text{peak-}}$) voltages of the induced EMF pulse were measured and recorded from the oscilloscope.
    - The approximate duration of each positive pulse ($\Delta t+$​) and negative pulse ($\Delta t-$​​) were measured and recorded.
    - This drop procedure was repeated 2-3 times for each height to ensure consistency and allow for averaging.

## Equipment Used & Measurement Details:

- Digital Oscilloscope: Used to capture, display, and measure the induced EMF waveform
- Copper Wire Coil (N=120)
- Permanent horseshoe magnet
- Ruler: Used to measure the drop height (h) from the bottom of the magnet to the top of the coil
- Peak Voltages ($\epsilon_{\text{peak+}}$​, $\epsilon_{\text{peak-}}$​): Measured directly from the oscilloscope's built-in measurement functions
- Pulse Durations ($\Delta t+$, $\Delta t-$​): Measured using the oscilloscope's cursors
# Results

This section presents the qualitative observations and quantitative data obtained from the experiment.

## Part 1. Qualitative Observations:

- Sketches or imported oscilloscope images of typical EMF pulses:

    - ![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXclFguCg-dxSRNxKDH-SkTCeiGS1iqVnUC2xlj9vK-v2lk1W_tnREYu7__dDYjbzAgxD_CUyOGGodlI_ndt6xWgBy7guqqbkLdycX-jBw72-oO0NIWseBYXt2jxvzVQbMRfNxjZTQ?key=NJDY3CtOSp_pl_YtHwvOnQ)

- Description of the pulse shape:

    - The typical EMF pulse observed when the magnet passed through the coil consisted of two main parts: an initial voltage pulse in one direction as the magnet entered the coil, immediately followed by a voltage pulse in the opposite direction as the magnet exited the coil. The shape of these pulses depended on the speed and orientation of the magnet.

- Observations on how the waveform changed with magnet direction/orientation:

    - The experiment involved passing the magnet through the coil with two different orientations. Reversing the magnet's orientation (e.g., North pole entering first versus South pole entering first) was expected to invert the polarity of the induced EMF waveform. For instance, if the first lobe was positive and the second negative for one orientation, reversing the magnet would result in the first lobe being negative and the second positive. The overall biphasic shape would remain.

- Observations on how peak EMF and pulse duration changed with qualitative variations in speed:

    - When the magnet was passed through the coil at a faster speed, the peak EMF (both positive and negative) was observed to be larger.
    - Conversely, the duration of the EMF pulses ($\Delta t+$​ and $\Delta t-$​) was observed to be shorter when the magnet moved faster. Slower speeds resulted in smaller peak EMFs and longer pulse durations.

## Part 2. Quantitative Data (Effect of Speed):

The number of turns in the coil ($N$) used for flux calculations was $120$. Entry speed ($v$) was calculated for each drop height ($h$) using $v=\sqrt{ 2gh }$, assuming $g=9.81 m/s^2$.

| Drop Height [cm] | Entry Speed [m/s] | Average $\epsilon_{\text{peak}+}$ [mV] | Average $\epsilon_{\text{peak}-}$ [mV] | Approx. $\Delta t_{+}$ [ms] | Approx. $\Delta t_{-}$ [ms] |
|------------------|-------------------|----------|----------|---------------------|---------------------|
|                3 |      0.7672027112 | 309   | -586  | 131              | 62               |
|                6 |       1.084988479 | 505   | -716  | 120              | 60               |
|                9 |       1.328834075 | 906   | -776  | 68               | 100              |

### Graphs

Average $\epsilon_{\text{peak}+}$ [mV] vs. Entry Speed [m/s]

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe3UZgkP3HPzc46GG5zay0ibVW5x8k7Yb8xo3yydIQSVc-pCp69H_qmyaJ5T883ChFsGHT7wh8PbTWFyeeOpIIJncXDwgyX5vUAc_gu-uUclsoXcPMAIeKmVYb8mKoOFVDVMiKRxg?key=NJDY3CtOSp_pl_YtHwvOnQ "Chart")**

Average $\epsilon_{\text{peak}-}$ [mV] vs. Entry Speed [m/s]

**![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXco9R7DnzG7vizIf_eGUI2X3eYvXtGpVmyk_wcrVkZ2EvrTE8qpMhmblLilCQbirUVCr9wLLvfJiT7F0laC4h5MNRwB8HJ1K9ClT1LCDAE9FJWxDw_xrpfT2wLl0fIz0YzdBJZriA?key=NJDY3CtOSp_pl_YtHwvOnQ "Chart")**

### Numerical Integrations and Flux Calculations

The wveform dt is obtained by dropping a magnet, horseshoe end facing the coil, from a height of $0$cm above the coil.

![[Pasted image 20250609100259.png]]

Fux Ccution from Integrted EMF Puse

| Waveform | $\Delta\Phi_{B}$,enter | Enter Area | N   | $\Delta\Phi_{B}$,enter | Exit Area |
|----------------|-----------|------------|-----|----------|-----------|
| Scope_0.csv    | -3.67E-05 |     0.0044 | 120 | 4.58E-05 |   -0.0055 |
| Scope_1_2.csv  | -3.83E-05 |     0.0046 | 120 | 4.50E-05 |   -0.0054 |
| Scope_1_F1.csv | -3.92E-05 |     0.0047 | 120 | 4.58E-05 |   -0.0055 |

# Discussion
## Waveform Analysis:

The observed shape of the induced EMF pulse is a direct consequence of Faraday's Law and Lenz's Law. As the magnet approaches and enters the coil, the magnetic flux through the coil changes, inducing an EMF. For instance, if the flux is increasing in one direction, an EMF is induced to create a current whose magnetic field opposes this increase. This results in the first lobe of the waveform (e.g., positive). As the magnet passes through the center and begins to exit, the flux changes again (e.g., decreases or increases in the opposite sense relative to the coil turns), inducing an EMF in the opposite direction to oppose this new change. This creates the second, oppositely polarized lobe of the waveform.

The effect of magnet orientation is to invert the polarity of the entire waveform. If, for one orientation, the entry pulse is positive and the exit pulse is negative, reversing the magnet would result in a negative entry pulse and a positive exit pulse. The fundamental biphasic shape remains.

## EMF vs. Speed:

The quantitative data clearly shows that the peak induced EMF increases with magnet speed. This is consistent with theoretical expectations based on Faraday's Law. A faster magnet causes a more rapid change in magnetic flux ($\frac{d\Phi_{B}}{dt}$) through the coil, directly leading to a larger induced EMF.

Conversely, the pulse duration ($\Delta t_{+}$​ and $\Delta t_{-}$​) generally decreased with increasing speed. For example, at 3 cm drop height (0.767 m/s), $\Delta t_{+}$​ was 0.131 s, while at 9 cm drop height (1.329 m/s), $\Delta t_{+}$ was 0.068 s. A faster magnet spends less time passing through the coil, so the period over which the flux changes is shorter.

## Flux Calculation:

The worksheet suggests that when a magnet passes completely through a coil, the total change in magnetic flux is ideally zero if the magnet starts and ends at positions where the induced EMF is negligible. This implies that the magnitudes of Area+ (integral of the first EMF pulse) and Area- (integral of the second EMF pulse) should be equal, with Area- being opposite in sign to Area+. Looking at the data:

- Scope_0.csv: Area+ = 0.0044 Vs, Area- = −0.0055 Vs. Sum = −0.0011 Vs.
- Scope_1_2.csv: Area+ = 0.0046 Vs, Area- = −0.0054 Vs. Sum = −0.0008 Vs.
- Scope_1_F1.csv: Area+ = 0.0047 Vs, Area- = −0.0055 Vs. Sum = −0.0008 Vs. The values of Area+ and Area- are not perfectly equal in magnitude and opposite in sign. Their sum, representing the net (Area+ + Area-), is not exactly zero. This deviation from the ideal scenario is expected due to experimental errors.

The calculated values $\Delta \Phi_{B,\text{enter}}$​ and $\Delta \Phi_{B,\text{exit}}$​ represent the change in magnetic flux through the coil specifically during the magnet's entry and exit phases, respectively. $\Delta \Phi_{B,\text{enter}}=−N_{1}​Area+$​​ represents the change from the initial flux (ideally zero) to the peak flux as the magnet enters. $\Delta \Phi_{B,\text{exit}}=−N_{1}​Area-$​​ represents the change from the peak flux back to the final flux (ideally zero) as the magnet exits. Ideally, $\Delta \Phi_{B,\text{enter}}$​ should be equal in magnitude and opposite in sign to $\Delta \Phi_{B,\text{exit}}$​, with one representing the establishment of peak flux (e.g., 0→Φpeak​) and the other its removal (Φpeak​→0). For Scope_0.csv: $\Delta \Phi_{B,\text{enter}}\approx−3.67×10−5 Wb$ and $\Delta \Phi_{B,\text{exit}}\approx​4.58×10−5 Wb$. These values are not perfectly equal in magnitude and opposite in sign, reflecting the discrepancy in Area+ and Area-.

## Sources of Error:

Several sources of experimental error could have affected the results:

- **Measuring drop height ($h$):** There may have been inconsistency in defining the exact top of the coil and bottom of the magnet. This would affect the calculated entry speed.
- **Reading oscilloscope values:** Uncertainty in cursor placement for measuring peak voltages ($\epsilon_{\text{peak}}$) and pulse durations ($\Delta t$).

- **Consistency of magnet drop:** The magnet might not have fallen perfectly vertically through the center of the coil each time, or it might have had a slight initial velocity if not dropped carefully from rest.
- **Assumptions in speed calculation:** The formula $v=\sqrt{ 2gh }$ assumes no air resistance and that the magnet is a point mass dropped from exactly height $h$. Air resistance would lead to a slightly lower actual speed.

- **Accuracy of numerical integration:** The oscilloscope's sampling rate and the algorithm used for integration can introduce errors. Electrical noise in the EMF signal could also affect the calculated area.

- **Defining start/end of pulse for integration:** If the integration limits ($t_{1}$,$t_{2}$​) don't precisely capture the entire pulse or include noise, the area will be inaccurate.
- **Coil and magnet imperfections:** Non-uniformity in the coil winding or magnet's field.

These errors could contribute to the observed differences in the magnitudes of Area+ and Area-, the deviations of their sum from zero, and variations in the calculated flux values.

## Relate Your Overall Findings to Faraday's Law of Induction:

The experiment's findings strongly support Faraday's Law of Induction. The observation that a moving magnet induces an EMF in the coil directly demonstrates the principle. The increase in peak EMF with increasing magnet speed provides evidence for the relationship $E\propto \frac{d\phi_{B}}{dt}$, as

a faster magnet produces a more rapid change in magnetic flux. The biphasic nature of the EMF pulse, explained by Lenz's Law (an integral part of Faraday's Law), further corroborates the theoretical framework. Numerical integration to calculate flux changes, though subject to experimental error, allows for a quantitative verification of the law by relating the time integral of EMF to the change in magnetic flux.

# Conclusion

This experiment successfully demonstrated the principles of electromagnetic induction due to the movement of a permanent magnet through a coil. The main objectives of the lab were achieved:

- The characteristics of the induced EMF were investigated qualitatively and quantitatively, showing a biphasic pulse whose amplitude and duration depend on the magnet's speed and orientation.

- Faraday's Law of Induction was verified through observations showing that the induced EMF increases with the rate of change of magnetic flux (i.e., with magnet speed).

- Magnetic flux changes were calculated numerically from the induced EMF waveform, demonstrating a digital method analogous to an analog integrator circuit.

Key results include the direct observation that a higher magnet speed leads to a larger peak induced EMF and a shorter pulse duration. The induced EMF waveform consistently showed two lobes of opposite polarity, corresponding to the magnet entering and exiting the coil. Flux calculations based on the numerical integration of the EMF waveform yielded values for the change in magnetic flux during entry and exit. While experimental errors led to some deviation from the ideal expectation that the positive and negative areas under the EMF curve would be perfectly equal and opposite, the overall results are consistent with Faraday's and Lenz's Laws.
