---
date created: Thursday, January 30th 2025, 12:25:10 pm
date modified: Wednesday, March 11th 2026, 12:20:20 pm
---
In this lab, we will develop an intuition for Kirchoff’s two fundamental Laws on voltage and current, KVL and KCL, which form the basis of all circuit theory. Our general train of thought is to study the application of KVL and KCL in 3 different contexts:

- Several simple lumped linear DC circuits
- A second series of circuits exploring differential and common-mode voltages
- A final third set introducing non-linear resistances
# Part 1: Verification of Basic Laws and Derived Quantities

The beginning of the lab deals with verifying KVL and KCL in a network of lumped resistors called a “T-Network”:

![[Pasted image 20250124133119.png]]

We call $I_{1}$ the current and $V_{1}$ the voltage passing through $R_{1}$, $I_{2}$ the current and $V_{2}$ the voltage passing through $R_{2}$, $I_{3}$ the current and $V_{3}$ the voltage passing through $R_{3}$.

We setup the lab DC power supply to generate a DC voltage of $V_{in}=+10\text{ V}$ between the input nodes of our circuit. We use the DMM to take DC voltage, current and resistance measurements with the following configurations:

![[Pasted image 20250131134555.png]]

![[Pasted image 20250131134604.png]]

![[Pasted image 20250131134630.png]]

## Verification of KCL and KVL

With the short circuit in our circuit, $R_{2}$ and $R_{3}$ combine for an equivalent resistance of $R_{2,3}=\frac{1}{\frac{1}{R_{2}} + \frac{1}{R_{3}}}=490.75\,\Omega$

To verify KVL, we wrote equations for our loop in our circuit:

$$
\begin{aligned}
I_{1}R_{1}+I_{1}R_{eq}=10\text{ V}
\end{aligned}
$$

We expect a current of $I_{1}=\frac{10V}{R_{1}+R_{eq}}=\frac{10V}{1474.7\Omega}=0.006\text{ A}$

We measure $I_{1}=5.9\text{ mA}$, which confirms KVL.

To verify KCL, we write the equation for our single node:

$$
I_{1}+I_{2}+I_{3}=\frac{V_{1}}{R_{1}}+\frac{V_{2}}{R_{2}}+\frac{V_{3}}{R_{3}}=0
$$

We measure:

- $V_{1}=6.66\text{ V}$
- $V_{2}=-3.33\text{ V}$
- $V_{3}=-3.33\text{ V}$
Which gives $\frac{V_{1}}{983\Omega}+\frac{V_{2}}{981\Omega}+\frac{V_{3}}{982\Omega}\approx0\text{ V}$
This confirms KCL in our circuit.

## Measuring Resistances

We measures the experimental resistances of $R_{1}$, $R_{2}$ and $R_{3}$. Theoretically, the values marked on the resistors are:

- $R_{1}=1000\pm5\%\,\Omega$
- $R_{2}=1000\pm5\%\,\Omega$
- $R_{3}=1000\pm5\%\,\Omega$

We measure our resistance values as:

- $R_{1}=983\,\Omega$
- $R_{2}=981\,\Omega$
- $R_{3}=982\,\Omega$

These are the same values as marked on the resistances, confirming our measurements.

## Power Verification

The power equation we are using is:

$$
P=\frac{V^{2}}{R}
$$

Across each of the resistors, we have the following power dissipation:

- $P_{1}=\frac{V_{1}^{2}}{R_{1}}=\frac{6.66^{2}}{983}=0.045\text{ W}$
- $P_{2}=\frac{V_{2}^{2}}{R_{2}}=0.011\text{ W}$
- $P_{3}=\frac{V_{3}^{2}}{R_{3}}=0.011\text{ W}$
Our total power dissipation, as measured at our power supply, is $0.071\text{ W}$. Our total measured power dissipation is $0.045+2\cdot 0.011=0.068\text{ W}$.
They are a little different, because measuring power dissipation at the resistors does not take into account the resistance of the wires in the circuit.

## Verifying Equivalent Resistance

The theoretical equivalent resistance between the two input nodes would be the sum of the resistances in the circuit:

$$
R_{eq}=R_{1}+\frac{1}{\frac{1}{R_{2}}+\frac{1}{R_{3}}}=983+\frac{1}{\frac{1}{981}+\frac{1}{982}}\approx 1473.4 \Omega
$$

We measure $1482.4\Omega$, which confirms that our calculations are correct.

## Verifying Current and Voltage Divider Theorems

The current divider theorem states that:

$$
\begin{aligned}
I_{2}=\frac{R_{3}}{R_{2}+R_{3}} I_{1} =\frac{1000}{1000+1000}6\cdot 10^{-3}=3\text{ mA}\\
I_{3}=\frac{R_{2}}{R_{2}+R_{3}} I_{1}=\frac{1000}{1000+1000}6\cdot 10^{-3}=3\text{ mA}
\end{aligned}
$$

We measure the following currents:

$$
\begin{aligned}
I_{2}= 3.33\text{ mA}\\
I_{3}=3.41 \text{ mA}
\end{aligned}
$$

And the voltage divider theorem states that, after we add $R_{2}$ and $R_{3}$ in parallel to create $R_{2,3}$, the voltage $V_{2,3}$ across $R_{2,3}$ is:

$$
\begin{aligned}
V_{2,3}=\frac{R_{2,3}}{R_{1}+R_{2,3}} V_{in} =\frac{490.75}{1000+490.75}\cdot10=3.29\text{ V}\\
V_{1}=\frac{R_{1}}{R_{1}+R_{2,3}} V_{in}=\frac{1000}{1000+490.75}\cdot10=6.71\text{ V}
\end{aligned}
$$

We measure the following voltages:

$$
\begin{aligned}
V_{2,3}= 3.33\text{V}\\
V_{1}=6.66\text{V}
\end{aligned}
$$

# Part 2: Single-Ended and Differential Circuits

We construct the following Wheatstone circuit using the same resistance for $R_{1,2,3}=1000\pm5\%\,\Omega$, and excite the circuit using the lab power supply set to $+10\text{ V}$ at $V_{1}$. The power rating of the resistances ($\frac{1}{8}\text{ W}$) is respected: $P=\frac{V^{2}}{R}=\frac{100}{1000}=0.1\text{ W}< \frac{1}{8}=0.125 \text{ W}$.

![[Pasted image 20250131140525.png]]

## Comparing Single-ended Voltages to Differential and Common-mode Voltages

Single-ended voltages have only one property, namely their voltage with respect to the common node. Our Wheatstone circuit has the following single-ended branches:

![[Pasted image 20250131142812.png]]

After setting the potentiometer $R_{4}=1000\,\Omega$, we measure $V_{1},V_{2},V_{3}$:

- $V_{1}\approx9.99\text{ V}$
- $V_{2}\approx 4.96\text{ V}$
- $V_{3}\approx5.04\text{ V}$

Differential voltages have two properties: their differential voltage(which is $V_{d}=V_{2}-V_{3}$) and their common-mode voltage (which is equal to $V_{cm}=\frac{V_{2}+V_{3}}{2}$). We measure $V_{d}$ and $V_{cm}$:

- $V_{d}\approx 77\text{ mV}=V_{2}-V_{3}$
- $V_{cm}\approx \frac{4.96+5.04}{2}=5\text{ V}=\frac{V_{2}+V_{3}}{2}$
This confirms the properties of differential voltage.

## Measuring the Resistances

We measure the resistances using the DMM:

- $R_{1}=983\,\Omega$
- $R_{2}=981\,\Omega$
- $R_{3}=982\,\Omega$

## Changing the Potentiometer Resistance

We are interested in how the differential $V_{d}$ and common-mode $V_{cm}$ voltage changes when we trim the potentiometer $R_{4}$. We take a series of $5$ measurements, changing and measuring $R_{4}$ each time, and plotting $V_{cm}$ vs. $V_{2}$ and $V_{cm}$ vs. $V_{3}$:

![[Common Mode Voltage vs. V2.svg]]

![[Common Mode Voltage vs. V3 (1).svg]]

We also plot $V_{d}$ vs. $\frac{R_{4}}{R_{3}}$, our x-axis (resistance values) is put on a log scale since our resistance values are exponentially increasing:

![[Differential Voltage vs. Bridge Resistor Ratio R4_R3.svg]]

We see that the differential voltage depends primarily on the ratio of the bridge resistors $\frac{R_{4}}{R_{3}}$, while the common-mode voltage depends primarily on the single-ended voltage magnitude of $V_{3}$ only.

# Part 3: Non-Linear Resistances

We are experimentally investigating the non-linear volt-amp ratio of a simple incandescent lamp. We will show that an incandescent lamp does not have a constant current response to varying DC voltage, and by extension does not obey the superposition principle.

## Lamp Resistance Analysis

We first plot the current response of an ordinary $R=1000\,\Omega$ resistor to $10$ different DC voltage values:

![[Current with ordinary resistor [Amps] vs. DC Voltage [Volts].svg]]

We note that the plot is linear.

We then plot the current response of our lamp to the same $10$ different DC voltage values:

![[Current with lamp [Amps] vs. DC Voltage [Volts].svg]]

We note that the plot is non-linear.

Therefore, we can see that our lamp's conductance slope varies with each applied DC voltage: the resistance of our lamp is non-linear. We also see the fixed resistance’s slope is a constant: our resistance stays constant with each DC voltage.

## Superposition Analysis

A system is said to be linear if its output response is directly proportional to the excitation at its input.

The principle of superposition says that for any linear system, the response (output) to the sum of two inputs is simply the sum of the responses to each input applied separately. Mathematically, if a device or circuit is linear, then the superposition principle says:

$$
\text{Response}\bigl(x_1 + x_2\bigr) \;=\; \text{Response}\bigl(x_1\bigr) \;+\; \text{Response}\bigl(x_2\bigr)
$$

For a linear device such as our resistor, this would entail:

$$
I(V_{1}+V_{2})=I(V_{1})+I(V_{2})
$$

Which is the case, since we have

$$
\begin{aligned}
&I(5)=0.005 \text{ mA}\\
&I(2.5)+I(2.5)=0.0025 \text{ mA}+0.0025 \text{ mA}\\
\implies &I(10)=I(5)+I(5)
\end{aligned}
$$

However, we see that this is not the case for our lamp, since

$$
\begin{aligned}
&I_{\text{lamp}}(5)=0.119 \text{ mA} \\
&I_{\text{lamp}}(2.5)+I_{\text{lamp}}(2.5)= 0.083 \text{ mA}+0.083 \text{ mA}\\
&I_{\text{lamp}}(5)\neq I_{\text{lamp}}(2.5)+I_{\text{lamp}}(2.5) \\
\end{aligned}
$$

Therefore, the response of the lamp does not obey the principle of superposition, which confirms the fact that the lamp is a non-linear circuit element.

# Conclusion

Through this lab, we studied examples of how linear circuit elements combine to create simpler equivalencies, and proved these equivalencies by measurements. We also saw the different ways voltage could be interpreted, as measured at a single point with a common mode reference, or at two different points in a circuit to create a differential voltage. Finally, we explored non-linear circuit elements showing that not all circuits obey the superposition principle.
