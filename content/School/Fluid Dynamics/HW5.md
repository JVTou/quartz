# Keg Drainage Problem
## Part A

Bernoulli's principle for nearly-steady flows relates different physical qualities of the beer at two positions in the keg. Here, we chose the two positions to be $z_{1}=h_{0}$ and $z_{0}=0$.

$$
\frac{1}{2}\rho_{beer}  \left( \frac{dh}{dt}  \right)^{2}+p_{1}+\rho_{beer} gh(t)=\frac{1}{2}\rho_{beer} u^{2}+p_{2}+\rho_{beer} gz_{0}
$$

Here, we take $p_{1}=p_{atmos}+\rho_{air} g(h_{0}-h(t))$ to account for the column of air above the beer, while $p_{2}=p_{atmos}$ at the exit of the keg. Substituting these values into Bernoulli's equation above gives:

$$
\begin{aligned}
&\frac{1}{2}\rho_{beer} \left( \frac{dh}{dt}  \right)^{2}+p_{atmos}+\rho_{air} g(h_{0}-h(t))+\rho_{beer} gh(t) \\
&=\frac{1}{2}\rho_{beer} u^{2}+p_{atmos}+\rho_{beer} gz_{0} \\
&\frac{1}{2}\rho_{beer}\left( \frac{dh}{dt} \right)^{2}+\rho_{air} gh_{0}-\rho_{air}gh(t)+\rho_{beer}gh(t)=\frac{1}{2}\rho_{beer} u^{2} \\
&u=\sqrt{ \frac{2g(h(t)\rho_{beer}+\rho_{air}(h_{0}-h(t)))+\rho_{beer}\left( \frac{dh}{dt}  \right)^{2}}{\rho_{beer}} }
\end{aligned}
$$

The mass flux of the liquid in the keg is:

$$
\frac{dh}{dt} A_{1}=uA_{0}
$$

Where $A_{1}$ is the surface area of the beer's surface and $A_{0}$ is the surface area of the spout. Therefore the evolution of the liquid depth $h(t)$ can be found by solving the following differential equation:

$$
\frac{dh}{dt}=\frac{A_{0}}{A_{1}}\sqrt{ \frac{2g(h(t)\rho_{beer}+\rho_{air}(h_{0}-h(t)))+\rho_{beer}\left( \frac{dh}{dt}  \right)^{2}}{\rho_{beer}} }
$$

First, let's try to isolate $\frac{dh}{dt}$:

$$
\begin{aligned}
&\left( \frac{dh}{dt} \right)^{2}=\left( \frac{A_{0}}{A_{1}} \right)^{2} \left(2g\left( h(t)+\frac{\rho_{air}}{\rho_{beer}}(h_{0}-h(t)) \right)+\left( \frac{dh}{dt}  \right)^{2}\right) \\
&\left( \frac{dh}{dt} \right)^{2}\left( 1-\left( \frac{A_{0}}{A_{1}} \right)^{2} \right)=2g\left( h(t)+\frac{\rho_{air}}{\rho_{beer}}(h_{0}-h(t)) \right) \\
\end{aligned}
$$

Let's make the assumption, as we did in lecture, that $A_{1}\gg A_{0}$:

$$
\frac{dh}{dt}=\sqrt{ 2g\left( h(t)+\frac{\rho_{air}}{\rho_{beer}}(h_{0}-h(t)) \right) }
$$

Then, using separation of variables, we get:

$$
\frac{dh}{\sqrt{ 2g\left( h(t)+\frac{\rho_{air}}{\rho_{beer}}(h_{0}-h(t)) \right) }}=dt
$$

If we assume $\rho_{air}\ll \rho_{beer}$, we notice we get the same result as in lecture:

$$
\begin{aligned}
&\frac{dh}{\sqrt{ 2gh(t) }}=dt \\
&\frac{dh}{dt}=u=\sqrt{ 2gh(t) }
\end{aligned}
$$

## Part B

However, taking into account $\rho_{air}$ gives a time to empty the keg of:

$$
\begin{aligned}
T&=\int_{0}^{h_{0}} \frac{1}{\sqrt{ 2gh(t) }} \, dt +\int_{0}^{h_{0}} \frac{1}{\sqrt{ \frac{2g\rho_{air}}{\rho_{beer}}(h_{0}-h(t)) }} \, dt \\
&=\frac{1}{\sqrt{ 2g }}2\sqrt{ h_{0} }+\sqrt{ \frac{2h_{0}\rho_{air}}{g\rho_{beer}} } \\
&=\sqrt{ \frac{2h_{0}}{g} }+\sqrt{ \frac{2h_{0}\rho_{air}}{g\rho_{beer}} }
\end{aligned}
$$

## Part C

The percentage difference between the lecture time result and the above is (assuming $\rho_{air}\approx1.225$ and $\rho_{beer}\approx 1000$):

$$
\frac{\sqrt{ \frac{2h_{0}}{g} }+\sqrt{ \frac{2h_{0}\rho_{air}}{g\rho_{beer}} }}{\sqrt{ \frac{2h_{0}}{g} }}=1+\frac{\sqrt{ \frac{2h_{0}1.125}{g1000} }}{\sqrt{ \frac{2h_{0}}{g} }}=1+\sqrt{ \frac{1.125}{1000} }
$$

Which is an difference of around $3.35\%$ more time to empty the keg than the lecture result.

# Siphoning Process

## Part A

A good way to prime the connector tube is to place one end inside our gas, then poke a hole through the other end and blow through it. This will increase the velocity of the air on the cross section of the tube we are blowing across, and by applying Bernoulli's principle, we can see that it will create a pressure gradient in the direction of which the gas will start flowing.

In the below drawing, we increase $v_{2}$, which creates the pressure gradient $P_{2}<P_{1}$. The gas will then start flowing towards $P_{2}$

![[Drawing 2024-11-11 20.16.04.excalidraw]]

## Part B

While the siphon is active, we can use Bernoulli's principles at points $B$ and $C$ to get the outlet velocity:

$$
P_{B}+\frac{1}{2}\rho v_{A}^{2}+\rho gh_{A}=P_{C}+\frac{1}{2}\rho v_{C}^{2}+\rho gh_{C}
$$

With:

- $h_{A}=H+L$, the maximum height of the liquid in the siphon
- $h_{C}=0$ the reference height
- $P_{B}=P_{C}=P_{atm}$
- $v_{A}=\frac{dh}{dt}\approx 0$, from the problem
- $v_{C}=v$ the velocity we are looking for

The Bernoulli equation simplifies to:

$$
\begin{aligned}
\rho g(H+L)=\frac{1}{2}\rho v_{C}^{2} \\
v_{C}=\sqrt{ 2 g(H+L)}
\end{aligned}
$$

However, if we consider the hydrostatic air pressure, we have to take it into account when looking at the variation between the air pressure at points $A$ and $B$. The hydrostatic equation is:

$$
\begin{aligned}
\frac{dP}{dz}=-\rho_{air}g \\
\int_{P_{A}}^{P_{B}}  \, dP=-\rho_{air}g\int_{H}^{H+L}  \, dz   \\
P_{B}-P_{A}=-\rho_{air}gL
\end{aligned}
$$

Using the above in Bernoulli's equation gives:

$$
P_{B}+\frac{1}{2}\rho v_{B}^{2}+\rho gh_{B}=P_{C}+\frac{1}{2}\rho v_{C}^{2}+\rho gh_{C}
$$

With:

- $P_{B}=P_{A}-\rho_{air}gL$
- $P_{A}=P_{C}=P_{atm}$
- $v_{B}\approx 0$ because of the small cross-sectional area and since it's at the peak of the siphon
- $h_{C}=0$
- $h_{B}=H+L$

Substituting these values into Bernoulli's equation:

$$
\begin{aligned}
P_{atm}-\rho_{air}gL+\rho g(H+L)=P_{atm}+\frac{1}{2}\rho v_{C}^{2} \\
-\rho_{air}gL+\rho g(H+L)=\frac{1}{2}\rho v_{C}^{2} \\
v_{C}=\sqrt{ 2g\left( \frac{-\rho_{air}}{\rho}L+(H+L) \right) }
\end{aligned}
$$

## Part C

For the siphon to work, the gas must stay liquid in the tube, and therefore, $P_{B}$ must be greater than the vapor pressure of gas:

$$
\begin{aligned}
P_{B}\geq P_{vapor} \\
P_{atm}-\rho_{air}gL\geq P_{vapor} \\
L\leq \frac{P_{atm}-P_{vapor}}{\rho_{air}g}
\end{aligned}
$$

## Part D

If we are considering the liquid being siphoned to be water (at constant room temperature), $P_{vapor}\approx3.17 kPa$. With:

- $P_{atm}\approx 101.3 kPa$
- $\rho_{air}\approx 1.225 \frac{kg}{m^{3}}$
- $g\approx 9.81 \frac{m}{s^{2}}$

$$
L\leq \frac{101.3-3.17}{1.225*9.81}\approx 8166m
$$
