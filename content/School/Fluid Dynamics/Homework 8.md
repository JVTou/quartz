# Problem 1
## Part A

Let's use this identity to separate our function into imaginary and real parts:

$$
\begin{aligned}
e^{ -inx }&=\cos nx-i\sin nx \\
U_{\infty}e^{ -ia }z&=U_{\infty}(\cos a-i\sin a)(x+iy) \\
&=U_{\infty}(x\cos a+iy\cos a-ix\sin a+y\sin a) \\
&=U_{\infty}(x\cos a+y \sin a)+iU_{\infty}(y\cos a-x\sin a)
\end{aligned}
$$

Therefore we can write our two potential functions as:

$$
\begin{aligned}
W=&\phi+i\psi \\
&\phi=U_{\infty}(x\cos a+y \sin a) \\
&\psi=U_{\infty}(y\cos a-x\sin a)
\end{aligned}
$$

## Part B

Checking that both $\phi$ and $\psi$ satisfy Laplace's equations:

$$
\begin{aligned}
\nabla^{2}\phi&=\frac{ \partial^{2} \phi }{ \partial x^{2} } +\frac{ \partial^{2}\phi }{ \partial y^{2} }=0  \\
&=\frac{ \partial  }{ \partial x } U_{\infty}\cos\alpha +\frac{ \partial  }{ \partial y }U_{\infty}\sin\alpha \\
&=0+0=0
\end{aligned}
$$

$$
\begin{aligned}
\nabla^{2}\psi&=\frac{ \partial^{2} \psi }{ \partial x^{2} } +\frac{ \partial^{2}\psi }{ \partial y^{2} }=0  \\
&=-\frac{ \partial  }{ \partial x } U_{\infty}\sin\alpha +\frac{ \partial  }{ \partial y }U_{\infty}\cos\alpha \\
&=0+0=0
\end{aligned}
$$

Checking that the potential functions satisfy the Cauchy-Riemann equations:

$$
\begin{aligned}
\frac{ \partial \phi }{ \partial x } &=\frac{ \partial \psi }{ \partial y }  \\
\frac{ \partial \phi }{ \partial y } &=-\frac{ \partial \psi }{ \partial x } 
\end{aligned}
$$

Checking the first equation:

$$
\begin{aligned}
\frac{ \partial \phi }{ \partial x } =U_{\infty}\cos\alpha \\
\frac{ \partial \psi }{ \partial y } =U_{\infty}\cos\alpha
\end{aligned}
$$

Checking the second equation:

$$
\begin{aligned}
\frac{ \partial \phi }{ \partial y }=U_{\infty}\sin\alpha \\
\frac{ \partial \psi }{ \partial x } =-U_{\infty}\sin\alpha \\
\frac{ \partial \phi }{ \partial y } =-\frac{ \partial \psi }{ \partial x } 
\end{aligned}
$$

## Part C

Finding the $u$ and $v$ components from $W(z)$:

$$
\begin{aligned}
\frac{dW}{dz}&=U_{\infty}e^{ -i\alpha } \\
&=U_{\infty}(\cos\alpha-i\sin\alpha)
\end{aligned}
$$

Since $u$ and $v$ are respectively the real and imaginary parts of $\frac{dW}{dz}$:

$$
\begin{aligned}
u=U_{\infty}\cos\alpha \\
v=-U_{\infty}\sin\alpha
\end{aligned}
$$

Finding the $u$ and $v$ components from $\phi$:

$$
\begin{aligned}
u&=\frac{ \partial \phi }{ \partial x } =U_{\infty}\cos\alpha \\
v&=-\frac{ \partial \phi }{ \partial x }=-U_{\infty}\sin\alpha 
\end{aligned}
$$

## Part D

This is a uniform steady flow since $u$ and $v$ are constants.

The direction of the flow is an angle $\theta$ from the x-axis: $\tan\theta=\frac{v}{u}=\frac{-\sin\alpha}{\cos\alpha}=-\tan\alpha$. Therefore the flow is at an angle of $\alpha$ from the x-axis.

The magnitude of the flow is $\sqrt{ u^{2}+v^{2} }=\sqrt{ U_{\infty}^{2}\cos ^{2}\alpha +U_{\infty}^{2}\sin ^{2}\alpha}=U_{\infty}$.

# Problem 3
## Part A

There are three potential flows that form the overall flow:

$$
\begin{aligned}
W&=W_{\text{uniform}}+W_{\text{source}}+W_{\text{sink}} \\
&=U_{\infty}z+\frac{m}{2\pi}\ln(z+a)-\frac{m}{2\pi}\ln(z-a)
\end{aligned}
$$

The velocity potential $\phi$ is found by taking the real part of each of our potential flows, and the stream function $\psi$ is the imaginary part. A useful identity here is $\ln z=\ln(x+iy)=\ln(\sqrt{ x^{2}+y^{2} })+i\arctan\left( \frac{y}{x} \right)$.

Working on the real part:

$$
\begin{aligned}
&\mathrm{Re}(W_{\text{uniform}})=\mathrm{Re}(U_{\infty}(x+iy))=U_{\infty}x \\
&\mathrm{Re}(W_{\text{source}})=\mathrm{Re}\left( \frac{m}{2\pi}\ln(x+iy+a) \right)=\frac{m}{2\pi}\ln(\sqrt{ (x+a)^{2}+y^{2} }) \\
&\mathrm{Re}(W_{\text{sink}})=-\frac{m}{2\pi}\ln\sqrt{ (x-a)^{2}+y^{2} } \\
&\phi=\mathrm{Re}(W)=U_{\infty}x+\frac{m}{2\pi}\ln(\sqrt{ (x+a)^{2}+y^{2} })-\frac{m}{2\pi}\ln\sqrt{ (x-a)^{2}+y^{2} }
\end{aligned}
$$

Doing the imaginary part:

$$
\begin{aligned}
&\mathrm{Im}(W_{\text{uniform}})=U_{\infty}y \\
&\mathrm{Im}(W_{\text{source}})=\frac{m}{2\pi}\arctan\left( \frac{y}{x+a} \right) \\
&\mathrm{Im}(W_{\text{sink}})=-\frac{m}{2\pi}\arctan\left( \frac{y}{x-a} \right) \\
&\psi=\mathrm{Im}(W)=U_{\infty}y+\frac{m}{2\pi}\arctan\left( \frac{y}{x+a} \right)-\frac{m}{2\pi}\arctan\left( \frac{y}{x-a} \right)
\end{aligned}
$$

## Part B

The stagnation points occur at points in the flow where the velocity is $0$. Let's work with polar coordinates since I just realized it made things a lot easier.

The velocity $\vec{v}$ can be divided into the radial $u_{r}$ and tangential $u_{\theta}$ components:

The total radial velocity is:

$$
u_{r}=\frac{ \partial \phi }{ \partial r } =u_{r_{\text{uniform}}}+u_{r_{\text{source}}}+u_{r_{\text{sink}}}=U_{\infty}\cos\theta+\frac{m}{2\pi r_{1}}-\frac{m}{2\pi r_{2}}
$$

The total tangential velocity is:

$$
u_{\theta}=-\frac{ \partial \psi }{ \partial r }= u_{\theta_{\text{uniform}}}+u_{\theta_{\text{source}}}+u_{\theta_{\text{sink}}}=-U_{\infty}\sin\theta
$$

This will be $0$ for $\theta=0,\pi,2\boldsymbol{\pi}\dots n\pi$. Let's focus on the case where $\theta=0$: $\cos\theta=1$, i.e. along the positive x-axis. We can rewrite $r_{1}=r+a$ and $r_{2}=r-a$ and the radial velocity becomes:

$$
\begin{aligned}
u_{r}&=U_{\infty}+\frac{m}{2\pi r_{1}}-\frac{m}{2\pi r_{2}}=U_{\infty} +\frac{m}{2\pi(r+a)}-\frac{m}{2\pi(r-a)} =0\\
&\implies U_{\infty}2\pi(r^{2}-a^{2})+2\pi m(r-a)-2\pi m(r+a)=0 \\
&\implies U_{\infty}(r^{2}-a^{2})-2ma=0 \\
&\implies r^{2}=\frac{2ma+U_{\infty}a^{2}}{U_{\infty}} \\
&\implies r=\pm\sqrt{ \frac{2ma+U_{\infty}a^{2}}{U_{\infty}} }
\end{aligned}
$$

Therefore the stagnation points are located on the x-axis at: $(-\sqrt{ \frac{2ma+U_{\infty}a^{2}}{U_{\infty}} },0)$ and $(\sqrt{ \frac{2ma+U_{\infty}a^{2}}{U_{\infty}} },0)$

## Part C

To find the pressure along the y-axis, let's use Bernoulli's equation, since we know this flow is steady and formed by incompressible and irrotational potential flows.

$$
\begin{aligned}
p+\frac{1}{2}\rho|\vec{u}|^{2}=p_{\infty}+\frac{1}{2}\rho U_{\infty}^{2} \\
p=p_{\infty}+\frac{1}{2}\rho(U_{\infty}^{2}-|\vec{u}|^{2})
\end{aligned}
$$

We notice that the magnitude of the velocity in the y-direction is $0$, since the uniform flow is horizontal and the magnitude of the sink in the y direction is canceled by the magnitude of the source in the y direction. Therefore, the only component of the velocity is $U_{\infty}$, and the pressure along the y-axis becomes:

$$
p=p_{\infty}\frac{1}{2}\rho(U_{\infty}^{2}-U_{\infty}^{2})=p_{\infty}
$$
