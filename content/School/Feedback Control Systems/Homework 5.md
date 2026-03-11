---
date created: Tuesday, November 12th 2024, 7:55:08 pm
date modified: Wednesday, March 11th 2026, 12:20:12 pm
---
# 1. Root Locus for Design
## Part 1

The open loop transfer function for this control system is:

$$
\begin{aligned}
GK=\frac{K(s+1)}{s+13} \frac{s^{2}+81}{s^{2}(s^{2}+100)}
\end{aligned}
$$

From this transfer function, we observe:

- $5$ poles:
	- $s=0$ (multiplicity $2$)
	- $s=-13$
	- $s=\pm 10j$
- $3$ zeroes:
	- $s=-1$
	- $s=\pm9j$

Since we have $m=5$ poles and $n=3$ zeroes, we will have $m-n=2$ asymptotes, with the following angles:

$$
\begin{aligned}
\theta=\frac{(2l+1)\pi}{m-n} \\
l=0,1 \\
\theta=\frac{\pi}{2}, \frac{3\pi}{2}
\end{aligned}
$$

The center of asymptotes is:

$$
\alpha=\frac{\sum \text{ Real part of poles}-\sum\text{ Real part of zeros}}{m-n}=\frac{-13-(-1)}{2}=-6
$$

The departure angles are:

- For the pole at $s=10j$:

$$
\begin{aligned}
\left( -\phi_{d}-90-90-90-\arctan\left( \frac{10}{13} \right)+90+90+90+\arctan\left( \frac{10}{1} \right) \right)=180 \\
\phi_{d}=-\left( 180+\arctan\left( \frac{10}{13} \right)-\arctan(10) \right) \\
\phi_{d}\approx227\text{ degrees}
\end{aligned}
$$

- For the pole at $s=0$:

$$
\begin{aligned}
-\phi_{d}-90-(-90)+90+(-90)=180 \\
\phi_{d}=-180 \text{ degrees}
\end{aligned}
$$

The arrival angles are:

- For the zero at $s=9j$:

$$
\begin{aligned}
\frac{\left( -\phi_{arr}-90-\arctan\left( \frac{9}{1} \right)+90+90+90+\arctan\left( \frac{9}{13} \right) \right)}{2}=180 \\
\phi_{arr}=-\left( 360-180-\arctan\left( \frac{9}{13} \right)+\arctan(9) \right) \\
\phi_{arr}\approx131\text{ degrees}
\end{aligned}
$$

## Part 2

For the damping ratio $\zeta>0.5$, we need the closed-loop poles to be in the wedge defined by the line departing the origin to the left of $\arcsin(0.5)\approx30$ degrees. Looking at our plot, it appears that no value of $K$ will be able to achieve this, since the poles at $s=\pm10j$ never cross into that wedge.

## Part 3

To find $K$ such that $\zeta=0.707$, we know that we will need to find the values of $K$ such that the closed loop pole cross lines at an angle of $\arcsin(0.707)\approx 45$ degrees. Using Matlab, we find that this happens for gain of approximately $K\approx91.5$

## Part 4

# 2. Root Locus for Disturbance Rejection

## Part 1

The open loop transfer function is:

$$
G(s)=\frac{1}{s(s+1)}
$$

With $D(s)=K_{p}$, we add proportional control to our transfer function:

$$
G(s)K_{p}=\frac{K_{p}}{s(s+1)}
$$

The closed loop transfer function is then:

$$
\begin{aligned}
\frac{G(s)K_{p}}{1+G(s)K_{p}}&=\frac{\frac{K_{p}}{s(s+1)}}{1+\frac{K_{p}}{s(s+1)}} \\
&=\frac{K_{p}}{s(s+1)}\cdot \frac{s(s+1)}{s(s+1)+K_{p}} \\
&=\frac{K_{p}}{s^{2}+s+K_{p}}
\end{aligned}
$$

Our specifications requires the steady state error of a constant unit disturbance to be less than $0.8$. Since the closed loop system has no zeros at the origin, the steady state error response to a unit disturbance is:

$$
\begin{aligned}
e_{ss}=\frac{1}{1+K_{p}} <0.8\\
\frac{1}{0.8}-1<K_{p} \\
K_{p}> 0.25
\end{aligned}
$$

We also want $\zeta=0.707$. This means the root locus must have poles that lie at an angle of $\arcsin(0.707)\approx 45$ degrees. Here, the poles are at $s=\frac{-1\pm \sqrt{ 1-4K_{p} }}{2}=-\frac{1}{2}\pm \frac{1}{2}\sqrt{ 1-4K_{p} }$.

To have poles at $45$ degrees, we need the magnitudes of the real and imaginary part of the poles to be equal:

$$
\begin{aligned}
1-4K_{p}=-1 \\
K_{p}=0.25
\end{aligned}
$$

Therefore, our conditions make it impossible to design $D(s)$ with only a proportional controller, as $K_{p}$ would have to be equal to but also strictly greater than $0.25$.

## Part 2

With $D(s)=K_{p}+sK_{d}$, we write the open loop transfer function as:

$$
\frac{K_{p}+sK_{d}}{s(s+1)}
$$

And the closed loop transfer function as:

$$
\frac{\frac{K_{p}+sK_{d}}{s(s+1)}}{1+\frac{K_{p}+sK_{d}}{s(s+1)}}=\frac{K_{p}+sK_{d}}{s(s+1)+K_{p}+sK_{d}}= \frac{K_{p}+sK_{d}}{s^{2}+s(1+K_{d})+K_{p}}
$$

The characteristic equation is now $s^{2}+s(1+K_{d})+K_{p}$. The roots of this equation are:

$$
s=\frac{-(1+K_{d})\pm \sqrt{ (1+K_{d})^{2}-4K_{p} }}{2}=-\frac{1}{2}(1+K_{d})
\pm \frac{1}{2}\sqrt{ (1+K_{d})^{2}-4K_{p} }
$$

Our specifications requires the steady state error of a constant unit disturbance to be less than $0.8$. Since this is a type $0$ system, the steady state error will be:

$$
\begin{aligned}
\frac{1}{1+K_{p}}<0.8 \\
K_{p}> \frac{1}{0.8}-1=0.25
\end{aligned}
$$

We also want $\zeta=0.707$. This means the root locus must have poles that lie at an angle of $\arcsin(0.707)\approx 45$ degrees, i.e. their real and imaginary parts must be equal. Here, the poles are at $s=-\frac{1}{2}(1+K_{d})\pm \frac{1}{2}\sqrt{ (1+K_{d})^{2}-4K_{p} }$.

$$
\begin{aligned}
-\frac{1}{2}(1+K_{d})=\frac{1}{2}\sqrt{ (1+K_{d})^{2}-4K_{p} } \\
(1+K_{d})^{2}=(1+K_{d})^{2}-4K_{p} \\
K_{p}=0
\end{aligned}
$$

# 3. Golden Nugget Airlines
## Part 1

The open loop transfer function of our system is:

$$
\frac{K}{s+10} \frac{s+3}{s^{2}+4s+5}
$$

The final value theorem gives a steady state error due to a step disturbance $\frac{M_{0}}{s}$ of:

$$
\begin{aligned}
e_{ss}&=\lim_{ s \to 0 } s\frac{\frac{M_{0}}{s}}{1+G(s)} \\
&=\frac{M_{0}}{1+\frac{K}{s+10} \frac{s+3}{s^{2}+4s+5}}=\frac{M_{0}}{1+\frac{3K}{50}}
\end{aligned}
$$

With a maximum value of $M_{0}=0.6$, and the specification to keep the steady state error under $0.02$ rad:

$$
\begin{aligned}
&\frac{0.6}{1+\frac{3K}{50}}<0.02 \\
&K=\frac{\left( \frac{0.6}{0.02}-1 \right)*50}{3}\approx483.33
\end{aligned}
$$

## Part 2

# 4. Lead Compensation
## Part 1

The open loop transfer function has poles at $s=\pm j$ and $s=-p$

The closed loop transfer function of this system with unity feedback, with $G(s)=\frac{1}{s^{2}+1}$ and the lead $K(s)=K \frac{s}{s+p}$ is:

$$
\begin{aligned}
\frac{GK}{1+GK}&=\frac{\frac{1}{s^{2}+1} K \frac{s}{s+p}}{1+\frac{1}{s^{2}+1} K \frac{s}{s+p}} \\
&=\frac{\frac{Ks}{(s^{2}+1)(s+p)} }{\frac{(s^{2}+1)(s+p)+Ks}{(s^{2}+1)(s+p)}} \\
&=\frac{Ks}{(s^{2}+1)(s+p)+Ks}
\end{aligned}
$$

The characteristic equation is:$(s^{2}+1)(s+p)+Ks=0$. Since we want poles at $s=-2\pm 2j$, we must place the lead's pole $p$ such that the root locus graph will pass through those poles. Rule $3$ for root locus will help us. Using it for $s=-2+2j$, we get:

$$
\begin{aligned}
\sum\text{Angles of zeros}-\sum\text{Angles of poles}=-180 \\
\text{Lead Angle}=-180-\left( -\left( \arctan\left( -\frac{1}{2} \right)+\arctan\left( -\frac{3}{2} \right) \right) \right) \\
\text{Lead Angle}\approx-97.125 \text{ degrees}
\end{aligned}
$$

Since the lead's zero is at the origin, this makes it easier to calculate the value of $p$:

$$
\begin{aligned}
\theta_{0}=\arctan\left( \frac{2}{2} \right)=45 \\
-97.125=\theta_{zero}-\theta_{pole} \\
\theta_{pole}=45+97.125=142.125 \\
\arctan\left( \frac{2}{p+2} \right)=142.125 \\
\frac{2}{p+2}=-0.675 \\
p=-4.963
\end{aligned}
$$

Adding up all the lengths to find $K$, for $s=-2+2j$:

- The magnitude of the zero at the origin is $∣−2+2j∣=(−2)2+(2)2=8=22| -2 + 2j | = \sqrt{(-2)^2 + (2)^2} = \sqrt{8} = 2\sqrt{2}$​.
- The magnitude of the pole at $s=+j$ is $5\sqrt{(-2)^2 + (2 - 1)^2} = \sqrt{5}$​.
- The magnitude of the pole at $s=−j$ is $=13\sqrt{(-2)^2 + (2 + 1)^2} = \sqrt{13}$​.
- The magnitude of the compensator pole at $s=−p$ is $\sqrt{(-2 + p)^2 + (2)^2}=\sqrt{ (−2+4.963)^2+4​ }​$​.

The root locus states: $|K(s)G(s)|=1$:

$$
K=\frac{\sqrt{ 5 }\sqrt{ 13 }\sqrt{ (-2+4.963)^{2}+4 }}{2\sqrt{ 2 }}\approx10.19
$$
