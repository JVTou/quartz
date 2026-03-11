---
date created: Thursday, May 29th 2025, 10:53:58 pm
date modified: Thursday, May 29th 2025, 11:58:55 pm
---
# Introduction

$\vec{J}=\sigma \vec{E}$

Essentially, this law states that the current density is directly proportional to the electric field that drives it, and the direction of current flow is the same as the direction of the electric field.

$\nabla \cdot \vec{J}=-\frac{d\rho}{dt}$

the equation states that the net outflow of current from a point (divergence of $J$) is equal to the rate of decrease of charge density at that point.

Conductive paper is a useful analog for plotting equipotential lines and electric field lines because the mathematical equations governing steady current flow in a 2D conductive sheet are similar to those governing electrostatics in a 2D charge-free region:

- Lines of constant voltage measured on the conductive paper directly correspond to electrostatic equipotential lines.
- Lines of current flow ($J$) in the paper correspond to electric field lines ($E$) in the analogous electrostatic setup.

# Part I. Resistance Measurement

After coating a $4" \times4"$ square of resistive paper with silver paint, we measure its resistance using the multimeter on two opposite edges: $R_{sq}=0.63k\Omega$. Cutting the square down to $2" \times2"$, we measure the resistance again: $R_{sq}=0.58k\Omega$.

The measured value does not depend on the size of the square, which is expected from the equation for the resistance of a square conductive sheet, which depends only on thickness $t$ and resistivity $\rho$:

$$
R_{sq}=\frac{\rho}{t}
$$

The error between our tow measurements may have arisen from a couple factors:

- The "square" might not be perfectly square, affecting the $\frac{L}{L}$ cancellation.
- The paper's conductivity ($\sigma$) or thickness ($t$) might not be perfectly uniform across its area.

# Part II. Coaxial line

The purpose of this experiment is to map the equipotential lines for a coaxial cable geometry (two concentric circular electrodes) using conductive paper and to experimentally determine its capacitance per unit length.

![[IMG_0650 1.jpg]]

 Some possible reasons which lead to the discrepancy between the theoretical result and your measurement are:

 - Inner and outer circles not perfectly concentric.
-  Paint not applied uniformly, or electrodes not perfectly circular.

The resistance between the inner and outer electrodes is $R_{coax}=3.16k\Omega$. The calculated capacitance per unit length of a coaxial in this experimental measurement is $C_{res} =7.005\times10^{-11}$ F/m. Its corresponding theoretical capacitance is $C_{res} =4.01\times10^{-11}$ F/m. There is significant discrepancy, which could be due to the factors mentioned above.

# Part III. Transmission line

The purpose of this experiment is to map the equipotential lines for a two-wire transmission line geometry using conductive paper and to experimentally determine its capacitance per unit length.

![[IMG_0651.jpg]]

The resistance between the two wires is $R_{wire}=6.5k\Omega$, and we calculate the capacitance per unit length of transmission line in this experimental measurement to be $C_{res}=3.405\times10^{-11}$ F/m. Its corresponding theoretical capacitance is $C_{res}=1.65\times10^{-11}$ F/m. We note that there is a significant difference between the two values, which can be explained by:

- The silver paint might not have uniform conductivity across its application
- The radius of the wire may vary across its perimeter

# Part IV Image Method

This experiment recreated the previous setup with a single wire parallel to an infinite conducting ground plane. The method of images allows us to replace the ground plane with an "image" charge (or wire) of opposite polarity, located symmetrically behind the plane, reducing the problem to a two-wire system in free space. The 2V equipotential line is on the same line as in the previous image. The method of images yields the same equipotential as found in the two-wire line.

The setup of one wire and a ground plane is electrostatically equivalent to having the original wire and an image wire at the same distance on the other side of where the plane was. This is precisely the setup of a two-wire line, where the ground plane corresponds to the zero-potential symmetry plane midway between the two wires of opposite potential.

# Conclusion

This lab successfully utilized conductive paper to demonstrate fundamental electrostatic principles.

Key findings include:

- The resistance of a conductive square sheet ($R_{sq}$​) was largely independent of its size, as theoretically expected, with minor variations attributed to material and geometric non-uniformities. Values obtained were $0.63kΩ$ for a $4"×4"$ square and $0.58kΩ$ for a $2"×2"$ square.
- Equipotential lines for coaxial and two-wire transmission line geometries were successfully mapped, visually demonstrating the field distributions.
- For the coaxial line, an experimental capacitance per unit length of $7.005\times10^{-11}$ F/m was found, differing significantly from the theoretical $C_{res} =4.01\times10^{-11}$ F/m.
- Similarly, for the two-wire transmission line, the experimental capacitance per unit length was $3.405\times10^{-11}$ F/m compared to a theoretical $C_{res}=1.65\times10^{-11}$ F/m. These discrepancies highlight the impact of electrode imperfections and other experimental errors.
- The method of images was effectively validated, showing that the 2V equipotential line in a wire-and-plane setup corresponded to that of the analogous two-wire system.

In conclusion, while conductive paper proved a useful tool for qualitative visualization of electrostatic fields and verification of concepts like the method of images, the quantitative determination of parameters like capacitance is sensitive to experimental precision and material uniformity.
