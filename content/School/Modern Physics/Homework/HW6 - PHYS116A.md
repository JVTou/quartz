# Junipero Verbeke
# Problem 1
$$ y'=\frac{2xy^2+x}{x^2y-y} $$
## a ##
$$ \begin{aligned}
\frac{y'}{2xy^2+x}&=\frac{1}{x^2y-y} \\
\frac{y'}{2y^2+1}&=\frac{x}{x^2y-y} \\
\frac{y'}{2y^2+1}y&=\frac{x}{x^2-1} \\
\frac{y}{2y^2+1}dy&=\frac{x}{x^2-1}dx \\
\int\frac{y}{2y^2+1}dy&=\int\frac{x}{x^2-1}dx \\
\frac{1}{4}\ln(2y^2+1)&=\frac{1}{2}\ln(x^2+1)+c \\
\sqrt[^4]{2y^2+1}&=c\sqrt{x^2-1} \\
2y^2&=(x^2-1)^2c^4-1 \\
y^2&=\frac{(x^2-1)^2c^4-1}{2} \\
y&=\frac{(x^2-1)c^2}{\sqrt{2}}-\frac{1}{\sqrt{2}} \\
y&=\frac{x^2-1}{\sqrt{2}}A-\frac{1}{\sqrt{2}} \\
\end{aligned} $$
## b
$$ \begin{aligned}
y&=\frac{(x^2-1)A}{\sqrt{ 2 }}-\frac{1}{\sqrt{ 2 }} \\
0&=\frac{(2-1)A}{\sqrt{ 2 }}-\frac{1}{\sqrt{ 2 }} \\
\frac{A}{\sqrt{ 2 }}&=\frac{1}{\sqrt{ 2 }} \\
A&=1
\end{aligned}
$$
# Problem 2
## a
$$ \begin{aligned}
ty'+2y&=4t^{2} \\
y'+\frac{2}{t}y&=4t\\
ye^{ \int 2/t \, dt  }&=\int 4te^{ \int 2/t \, dt  } \, dt +c\\
ye^{ \ln t^{2} }&=\int 4t^{3} \, dt+c\\
yt^{2}&=t^{4}+c\\
y&=t^{2}+\frac{c}{t^{2}}\\
2&=1+\frac{c}{1}\\
c&=1\\
y&=t^{2}+\frac{1}{t^{2}}
\end{aligned}
$$
## b
$$
\begin{aligned}
y'+\frac{2}{t}y&=\frac{\cos t}{t^{2}}\\
I=\int \frac{2}{t} \, dt =\ln t^{2}\\
yt^{2}&=\int \frac{\cos t}{t^{2}} \, dt +c\\
yt^{2}&=\int \cos t \, dt+c\\
yt^{2}&=\sin t+c\\
y&=\frac{\sin t}{t^{2}}+\frac{c}{t^{2}}\\
0&=\frac{\sin \pi}{\pi^{2}}+\frac{c}{\pi^{2}}\\
c=0\\
y&=\frac{\sin t}{t^{2}}
\end{aligned}
$$
## c
$$
\begin{aligned}
y'-2y=e^{ 2t }\\
e^{ I }=e^{ \int -2 \, dt  }=e^{ -2t }\\
ye^{ -2t }&=\int e^{ -2t }e^{ 2t } \, dt+c\\
y&=e^{ 2t }+ce^{ 2t }\\
2=1+c\\
c=1\\
y&=2e^{ 2t }
\end{aligned}
$$
# Problem 3
$$ \begin{aligned}
RI'+\frac{1}{c}I&=0 \\
I'+\frac{1}{RC}I&=0\\
ye^{ \int 1/RC \, dt  }&=\int 0\cdot e^{ \int 1/RC \, dt  } \, dt+c\\
ye^{ t/RC }&=c\\
y=c e^{ -t/RC }
\end{aligned}
$$
<iframe src="https://www.desmos.com/calculator/rg8nxt25d3?embed" width="500" height="500" style="border: 1px solid #ccc" frameborder=0></iframe>

# Problem 4
$$
\begin{aligned}
\frac{dv}{dt}+\frac{k}{m}v^{n}=0
\end{aligned}
$$
Working on the first case where $n=1$:
$$
\begin{aligned}
v'+\frac{k}{m}v&=0 \\
ve^{ \int k/m \, dt  }&=c \\
v=c e^{ (-k/m)t }\\
v_{0}=c e^{ 0 }\\
c=v_{0}\\
v&=v_{0}e^{ (-k/m)t }
\end{aligned}
$$
 Working on the second case where $n\neq 1$, using separable variables:
 $$
\begin{aligned}
mv'&=-kv^{n}\\
v^{-n} \frac{dv}{dt}&=-\frac{k}{m}dt\\
\frac{dv}{v^{n}}&=-\frac{k}{m}dt\\
\int \frac{1}{v^{n}} \, dv &= \int -\frac{k}{m} \, dt \\
\frac{v^{1-n}}{1-n}&=-\frac{k}{m}t+c\\
v^{1-n}&=-\frac{k}{m}t(1-n)+c(1-n)\\
v&=\sqrt[1-n]{ -\frac{k}{m}t(1-n)+c(1-n) }\\
v(t=0)=\sqrt[1-n]{ c(1-n) }=v_{0}\Leftrightarrow c=\frac{v_{0}^{1-n}}{1-n}\\
v&=\sqrt[1-n]{ -\frac{k}{m}t(1-n)+v_{0}^{1-n} }
\end{aligned}
$$
So $v$ as a function of time is:
$$
v=\begin{cases}
			v_{0}e^{ (-k/m)t }, & \text{if $n=1$}\\
            \sqrt[1-n]{ -\frac{k}{m}t(1-n)+v_{0}^{1-n} }, & \text{if $n\neq 1$}
		 \end{cases}
$$
To calculate $v$ as a function of distance, we can write:
$$
\frac{dv}{dt}=\frac{dv}{dx} \frac{dx}{dt}=\frac{dv}{dx}v
$$
We rewrite our original equation using this new identity for $\frac{dv}{dt}$:
$$
\begin{aligned}
m \frac{dv}{dx}v&=-kv^{n}\\
\frac{dv}{dx}v^{1-n}&=-\frac{k}{m} \\
v^{1-n}dv & =-\frac{k}{m}dx \\
\end{aligned}
$$
We study the two cases: first when $v$ is a first order diff. eq. ($n=2$) and the case where $v$ is not a first order diff. eq. ($n\neq 2$).

First, when $n=2$:
$$
\begin{aligned}
\int v^{-1} \, dv & =\int -\frac{k}{m} \, dx \\
\ln v & =-\frac{k}{m}x+c \\
v & =e^{ (-k/m)x }\cdot c \\
v(t=0) & =c=v_{0} \\
v & = e^{ -(k/m)x }v_{0}
\end{aligned}
$$
When $n\neq 2$:
$$
\begin{aligned}
\int v^{1-n} \, dv  & = \int -\frac{k}{m} \, dx \\
\frac{v^{2-n}}{2-n}&=-\frac{k}{m}x+c\\
v^{2-n}&=-\frac{k}{m}x(2-n)+c(2-n)\\
v&=\sqrt[2-n]{ -\frac{k}{m}x(2-n)+c(2-n) }\\
v(x=0)=\sqrt[2-n]{ c(2-n) }=v_{0}\Leftrightarrow c=\frac{v_{0}^{2-n}}{2-n}\\
v&=\sqrt[2-n]{ -\frac{k}{m}x(2-n)+v_{0}^{2-n} }
\end{aligned}
$$
So $v$ as a function of distance is:
$$
v=\begin{cases}
			v_{0}e^{ (-k/m)x }, & \text{if $n=2$}\\
            \sqrt[2-n]{ -\frac{k}{m}x(2-n)+v_{0}^{2-n} }, & \text{if $n\neq 2$}
		 \end{cases}
$$
# Problem 5
## a
The intensity of the light at a distance $s$ below the ocean's surface is:
$$ \begin{aligned}
\frac{dI}{ds} & =\mu I \\
\frac{dI}{ds}-\mu I & =0 \\
Ie^{-\mu s} & =c \\
I(s=0)=c e^{ -\mu \cdot 0 }=c=I_{0} \\
I & =I_{0}e^{ -\mu s } \\
\end{aligned}
$$
## b
If we take $\mu=10^{-2}\text{ ft}^{-1}$, we can calculate the intensity of the beam at different depths:
- At 1 ft., the intensity will be:
$$
I(s=1)=\frac{I_{0}}{e^{ (10)^{-2} }}
$$
- At 50 ft., the intensity will be:
$$
I(s=50)=\frac{I_{0}}{e^{ 50\cdot(10)^{-2} }}
$$
- At 500 ft., the intensity will be:
$$
I(s=500)=\frac{I_{0}}{e^{ 500\cdot(10)^{-2} }}
$$
- At a mile, the intensity will be:
$$
I(s=5280)=\frac{I_{0}}{e^{ 5280\cdot(10)^{-2} }}
$$
## c
The half-value thickness of a substance with a linear absorption coefficient of $\mu$ is:
$$
\begin{aligned}
I=\frac{1}{2}I_{0} \\
\frac{1}{2}I_{0}=I_{0}e^{ -\mu s } \\
e^{ -\mu s }=\frac{1}{2} \\
-\mu s=\ln \frac{1}{2} \\
s=\frac{\ln \frac{1}{2}}{-\mu}
\end{aligned}
$$ 
If we take $\mu=10^{-2}\text{ ft}^{-1}$, we calculate that the beam will have half of its original intensity at:
$$
s=\frac{\ln \frac{1}{2}}{-10^{-2}}
$$
# Problem 6
An expression for the concentration of pollutants in the lake over time is $c(t)=\frac{Q(t)}{V}$. We also know that the rate of change of pollution is $\frac{dQ(t)}{dt}=rk+P-rc(t)$
## a
First finding an expression of $Q(t)$:
$$\begin{aligned}
Q'(t)+\frac{r}{V}Q & =rk+P \\
Qe^{ \int r/V \, dt  } & =\int (rk+P)e^{ \int r/V \, dt  } \, dt+c \\
Qe^{ rt/V } & =\int (rk+P)e^{ rt/V } \, dt+c  \\
 & =\frac{V}{r}(rk+P)e^{ rt/V }+c \\
Q & =\frac{V}{r}(rk+P)+c e^{ -rt/V }
\end{aligned}
$$
Now using this expression of $Q(t)$ in our expression for $c(t)$:
$$\begin{aligned}
c(t) & =\frac{Q}{V} \\
 & =\frac{1}{r}(rk+P)+\frac{c}{V}e^{ -rt/V } \\
c(0)=c_{0}=\frac{1}{r}(rk+P)+\frac{c}{V} \\
c=Vc_{0}-V\left( k+\frac{P}{r} \right) \\
c(t) & =k+\frac{P}{r}+\left( c_{0}-k-\frac{P}{r} \right)e^{ -rt/V }
\end{aligned}
$$
The limiting concentration, found as $t\to \infty$, is:
$$
\lim_{ t \to \infty } c(t)=k+\frac{P}{r}
$$
## b
If $K=0$ and $P=0$, then we can rewrite $\frac{dQ}{dt}$ as:
$$ \begin{aligned}
Q'(t) & =-rc(t) \\
 & =-\frac{rQ(t)}{V} \\
Q'(t)+\frac{r}{V}Q(t) & =0\\ \\
Q(t)e^{ \int r/V \, dt  }=c \\
Q(t)=c e^{ -(r/V)t }
\end{aligned}
$$
We know that $c(t)=\frac{Q}{V}$ and, therefore:
$$ \begin{aligned}
c(t)=\frac{c e^{ -(r/V)t }}{V}
\end{aligned}
$$
Applying the initial conditions to $c(t)$ gives:
$$
c(0)=c_{0}=\frac{c}{V}
\Leftrightarrow
c=Vc_{0}
$$
Therefore $c(t)=c_{0}e^{ -rt/V }$.
We want t for $c(t)=\frac{1}{2}c_{0}$:
$$ \begin{aligned}
c_{0}e^{ -rt/V }=\frac{1}{2}c_{0} \\
e^{ -rt/V }=\frac{1}{2} \\
-\frac{rt}{V}=\ln \frac{1}{2} \\
t=\ln \frac{1}{2} \left( -\frac{V}{r} \right) \\
t=\frac{V}{r}\ln 2
\end{aligned}
$$
We also want $t$ for $c(t)=0.1c_{0}$:
$$
\begin{aligned}
c_{0}e^{ -rt/V }=0.1c_{0} \\
e^{ -rt/V }=0.1 \\
-\frac{rt}{V}=\ln \frac{1}{10} \\
t=\frac{V}{r}\ln 10
\end{aligned}
$$
# Problem 7
## a
$$
4y''-y=0
$$
Characteristic equation: $4r^{2}-1=0\Leftrightarrow r=\pm \frac{1}{2}$
General solution: $y(t)=Ae^{ t/2 }+Be^{ -t/2 }$

$y(-2)=Ae^{ -1 }+Be^{ -1 }=1\Leftrightarrow A=e-Be^{2}$

$y'(-2)=\frac{A}{2}e^{ -1 }-\frac{B}{2}e^{ 1 }=-1$
$-1=\frac{e-Be^{2}}{2}e^{ -1 }-\frac{B}{2}e^{ 1 }=\frac{1}{2}-\frac{1}{2}Be-\frac{1}{2}Be$
$-Be=-\frac{3}{2}$
$B=\frac{3}{2}e^{ -1 }$

$A=e-Be^{2}=e-\frac{3}{2}e^{ -1 }e^{ -2 }=e-\frac{3}{2}e=-\frac{1}{2}e$

Particular solution: $y=-\frac{1}{2}e^{ 1+t/2 }+\frac{3}{2}e^{ -(t/2)-1 }$
## b
$$
9y''-12y'+4y=0
$$
Characteristic equation: $9r^{2}-12r+4=0\Leftrightarrow r=\frac{2}{3}$
General solution: $(A+tB)e^{ (2/3)t }$

$y(0)=(A+0\cdot B)e^{ (2/3)\cdot0 }=2\Leftrightarrow A=2$

$y'(t)=\frac{2}{3}Ae^{ (2/3)t }+Be^{ (2/3)t }+tB \frac{2}{3}e^{ (2/3)t }$
$y'(0)=\frac{2}{3}A+B=-1$
$B=-1-\frac{2}{3}A=-1-\frac{4}{3}=-\frac{7}{3}$

Particular solution: $y=\left( 2-\frac{7}{3}t \right)e^{ (2/3)t }$
## c
$$
y''-2y'+5y=0
$$
Characteristic equation: $r^{2}-2r+5=0\Leftrightarrow r=1\pm4 i$
General solution: $y=e^{ t }(c_{1}\sin 4t+c_{2}\cos 4t)$

$y\left( \frac{\pi}{2} \right)=e^{ \pi/2 }(c_{1}\sin 2\pi+c_{2}\cos 2\pi)=0$
$e^{ \pi/2 }c_{2}=0$
$c_{2}=0$

$y'\left( \frac{\pi}{2} \right)=e^{ \pi/2 }c_{1}\sin \frac{4\pi}{2}+e^{ \pi/2 }4c_{1}\cos \frac{4\pi}{2}=2$
$e^{ \pi/2 }4c_{1}=2$
$c_{1}=\frac{1}{2}e^{ -\pi/2 }$

Particular solution: $y=e^{ t }\frac{1}{2}e^{ -\pi/2 }\sin 4t$
