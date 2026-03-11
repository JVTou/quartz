---
date created: Monday, April 7th 2025, 12:25:38 pm
date modified: Wednesday, March 11th 2026, 12:20:19 pm
---
# Problem 7.4

If we have $v_{1}(t)=4\cos(2\pi \times 10^3t+30^\circ)$V, and $v_{2}$ lags $v_{1}$ by a phase angle of $60^\circ$:

$$
v_{2}(t)=4\cos(2\pi\times10^3t+30^\circ-60^\circ)=4\cos(2\pi\times10^3t-30^\circ)\text{V}
$$

The below graph shows $v_{1}$ in red and $v_{2}$ in blue:

![[desmos-graph (5).png]]

# Problem 7.10
1. $z_{1}=3+4j=\sqrt{ 3^{2}+4^{2} }e^{ j\arctan(4/3) }=5e^{ 0.93j }$
2. $z_{2}=-6+8j=\sqrt{ (-6)^{2}+8^{2} }e^{ \arctan (8/-6)j}=10e^{ -0.93j }$
3. $z_{3}=-6-4j=7.2e^{ 0.59j }$
4. $z_{4}=2j=2e^{ \pi/2j }$
5. $z_{5}=(2+j)^{2}=2.24^{2}e^{ 0.46\cdot2j }$
6. $z_{6}=(3-2j)^{3}=3.6^{3}e^{ -0.59\cdot3j }$
7. $z_{7}=\sqrt{ -1+j }=\sqrt{ 1.4 }e^{ -0.79/2j }$

# Problem 7.29

We know the following values for our resistor and capacitor in our circuit:

- $R=20\Omega$
- $C=1\mu F$
- $i_{s}(t)=12\cos(2\pi\times10^4t-60^\circ)mA$

![[Pasted image 20250305164049.png]]

The phasor representation of our current is $I_{s}=12e^{ -60^\circ j }$.

Using current division, we know that:

$$
I_{C}=\frac{R}{R+\frac{1}{j\omega C}}I_{s}=\frac{20}{20+\frac{1}{j\cdot10^4\cdot 10^{-6}}}12e^{ -60^\circ j }=\frac{240e^{ -60^\circ j}}{20-10^{2}j}=\frac{240e^{ -60^\circ j}}{102e^{ -78.69^\circ j }}=\frac{40}{17}e^{ 18.69^\circ j}\text{A}
$$

Going back to the time domain:

$$
i_{C}(t)=\mathrm{Re}[I_{C}e^{ 10^4jt }]=\frac{40}{17}\cos(10^4t+0.33)\text{ A}
$$

# Problem 7.57

Our first step is to transform our circuit to the phasor domain. Accordingly:

- $Z_{C}=\frac{1}{j\omega C}=-\frac{j}{10^5\cdot10^{-6}}=-10j$
- $V_{\text{left source}}=21\text{ V}$
- $V_{\text{right source}}=10.5\text{ V}$
![[7.57 Circuit]]
Our current equations are:
- $I_{1}=\frac{V_{1}-V_{3}}{Z_{C}}=\frac{V_{1}-V_{3}}{-10j}=\frac{V_{3}-V_{1}}{10j}$
- $I_{2}=\frac{V_{1}-21}{5}$
- $I_{3}=\frac{V_{1}-V_{2}}{5}$
- $I_{4}=\frac{V_{2}-V_{3}}{-10j}$
- $I_{x}=\frac{V_{2}-V_{3}}{-10j}=\frac{V_{3}-V_{2}}{10j}$
- $I_{5}=\frac{V_{3}+21-V_{1}}{5}$
- $I_{6}=\frac{V_{3}-V_{2}}{-10j}=\frac{1}{10}(V_{3}-V_{2})j$

KCL dictates that, at our left node:

$$
\begin{aligned}
I_{1}+I_{2}+I_{3}=0 \\
\frac{V_{3}-V_{1}}{10j}+\frac{V_{1}-21}{5}+\frac{V_{1}-V_{2}}{5}=0 \\
\left( \frac{2}{5}+\frac{1}{10 }j \right)V_{1}-\frac{1}{5}V_{2}-\frac{1}{10}jV_{3}=\frac{21}{5}
\end{aligned}
$$

Similarly, at our right node:

$$
\begin{aligned}
-I_{3}+I_{4}+I_{x}=0 \\
-\frac{V_{1}-V_{2}}{5}+\frac{V_{2}-V_{3}}{-10j}+\frac{V_{3}-V_{2}}{10j}=0 \\
-\frac{1}{5}V_{1}+\left( \frac{1}{5}+\frac{2}{10}j \right)V_{2}-\frac{2}{10}jV_{3}=0
\end{aligned}
$$

Finally, at our bottom node:

$$
\begin{aligned}
I_{5}+I_{6}-I_{1}=0 \\
\frac{V_{3}+21-V_{1}}{5}+\frac{1}{10}(V_{3}-V_{2})j-\frac{V_{3}-V_{1}}{10j}=0 \\
\left( -\frac{1}{5}-\frac{1}{10}j \right)V_{1}-\frac{1}{10}jV_{2}+\left( \frac{1}{5}+\frac{2}{10}j \right)V_{3}=-\frac{21}{5}
\end{aligned}
$$

Solving this system of equations gives:

$$
\begin{aligned} V_1 &\approx -7.41 + 8.65j \\ V_2 &\approx 2.47 + 11.12j \\ V_3 &\approx 4.94 + 1.24j \end{aligned}
$$

Therefore:

$$
I_{x}=\frac{1}{10}(V_{2}-V_{3})j=\frac{1}{10}(2.47 + 11.12j-4.94 + 1.24j)j=−0.988−0.247j
$$

Or in polar form:

$$
I_{x}=1.02e^{ 194.04^\circ j}
$$

Going back to the time domain:

$$
\mathrm{Re}[I_{x}e^{ 10^5jt }]=1.02\cos(3.39+10^5t)\text{ A}
$$
