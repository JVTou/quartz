---
date created: Wednesday, November 27th 2024, 9:33:05 am
date modified: Wednesday, March 11th 2026, 12:20:04 pm
---
# Exercise 4.2
## Part a

The continuity equation states that for any compressible fluid:

$$
\frac{ \partial \rho }{ \partial t } +\nabla \cdot(\rho \vec{u})=0
$$

Here, our velocity field is $\vec{u}=\left( \frac{\alpha x}{t},0,0 \right)$. Substituting into the continuity equation gives:

$$
\begin{aligned}
\frac{ \partial \rho }{ \partial t } +\nabla \cdot \left( \rho\frac{\alpha x}{t} \right)=0 \\
\frac{ \partial \rho }{ \partial t } +\frac{ \partial  }{ \partial x } \left( \frac{\rho \alpha x}{t} \right)=0 \\
\frac{ \partial \rho }{ \partial t } +\frac{ \partial \rho }{ \partial x } \frac{x}{t}+\frac{\rho\alpha}{t}=0
\end{aligned}
$$

Since we are assuming that the density field is spatially uniform, there is no change in density along any axis: $\frac{ \partial \rho }{ \partial x }=0$. We end up with a separable variable differential equation which we can solve:

$$
\begin{aligned}
\frac{ \partial \rho }{ \partial t } +\frac{\rho\alpha}{t}=0 \\
\frac{ \partial \rho }{ \partial t } =-\frac{\rho\alpha}{t} \\
\frac{ \partial \rho }{ \rho } =-\frac{\alpha}{t} \partial t \\
\ln\rho=-\alpha \ln t +C\\
\rho=Ct^{-\alpha}
\end{aligned}
$$

We apply our initial conditions, $\rho=\rho_{0}$ at $t=t_{0}$:

$$
\begin{aligned}
\rho_{0}=Ct_{0}^{-\alpha} \\
C=\frac{\rho_{0}}{t_{0}^{-\alpha}} \\
\rho=\frac{\rho_{0}}{t_{0}^{-\alpha}}t^{-\alpha}=\rho_{0}\left( \frac{t_{0}}{t} \right)^{\alpha}
\end{aligned}
$$

## Part B

Finding the unsteady acceleration $\frac{ \partial \vec{u} }{ \partial t }$:

$$
\begin{aligned}
\frac{ \partial  }{ \partial t } \left( \frac{\alpha x}{t},0,0 \right)=\left( -\frac{\alpha x}{t^{2}},0,0 \right)
\end{aligned}
$$

Finding the advective acceleration $(\vec{u}\cdot \nabla)\vec{u}$:

$$
\begin{aligned}
(\vec{u}\cdot \nabla)\vec{u}=\frac{\alpha x}{t}\frac{ \partial  }{ \partial x } (\vec{u})=\frac{\alpha x}{t} \left( \frac{\alpha}{t},0,0 \right)=\left( \left( \frac{\alpha}{t} \right)^{2}x,0,0 \right)
\end{aligned}
$$

Finding the particle acceleration $\frac{D\vec{u}}{Dt}$ using our previous results:

$$
\begin{aligned}
\frac{D\vec{u}}{Dt}&=\frac{ \partial \vec{u} }{ \partial t } +(\vec{u}\cdot \nabla)\vec{u} \\
&=\left( -\frac{\alpha x}{t^{2}},0,0 \right)+\left( \left( \frac{\alpha}{t} \right)^{2}x,0,0 \right) \\
&=\left( \frac{\alpha x(\alpha-1)}{t^{2}},0,0 \right)
\end{aligned}
$$

When $\alpha=1$, the particle acceleration becomes $0$, which means the particles follow the same velocity as the local flow around them.

# Exercise 4.38
## Part a

To find $u_{R}$, we will need the continuity equation in cylindrical coordinates:

$$
\frac{1}{R}\frac{ \partial }{ \partial R } (Ru_{R})+\frac{1}{R}\frac{ \partial u_{\phi} }{ \partial \phi } +\frac{ \partial u_{z} }{ \partial z } =0
$$

We know that $u_{\phi}=0$ and $u_{z}=-Az$. The continuity equation becomes:

$$
\begin{aligned}
\frac{1}{R}\frac{ \partial  }{ \partial R } (Ru_{R})+\frac{ \partial  }{ \partial z } (-Az)=0 \\
\frac{1}{R}\frac{ \partial  }{ \partial R } (Ru_{R})-A=0 \\
\frac{ \partial  }{ \partial R } (Ru_{R})=AR \\
Ru_{R}=\frac{AR^{2}}{2}+C \\
u_{R}=\frac{AR}{2}+\frac{C}{R}
\end{aligned}
$$

We want the flow field to be smooth, so to avoid any singularities at $R=0$ we set $C=0$:

$$
u_{R}=\frac{AR}{2}
$$

## Part B

We will first check to see if the fluid is incompressible to see if we can use Bernoulli to find the pressure. If the fluid is incompressible, then $\vec{\omega}=\nabla \times \vec{u}= 0$:

$$
\nabla \times \vec{u}=\left( \frac{1}{R}\frac{ \partial u_{z} }{ \partial \phi } -\frac{ \partial u_{\phi} }{ \partial z } ,\frac{ \partial u_{R} }{ \partial z } -\frac{ \partial u_{z} }{ \partial R } , \frac{1}{R}\left( \frac{ \partial (Ru_{\phi}) }{ \partial R }  -\frac{ \partial u_{R} }{ \partial \phi } \right) \right)=(\omega_{R},\omega_{\phi},\omega_{z})
$$

We know that $u_{\phi}=0$, $u_{z}=-Az$ and $u_{R}=\frac{AR}{2}$:

$$
\begin{aligned}
\omega_{R}=\frac{1}{R}\frac{ \partial (-Az) }{ \partial \phi } -\frac{ \partial  }{ \partial z }0 =0\\
\omega_{\phi}=\frac{ \partial  }{ \partial z } \frac{AR}{2}-\frac{ \partial (-Az) }{ \partial R }=0 \\
\omega_{z}=\frac{1}{R}\left( \frac{ \partial (R\cdot0) }{ \partial R }  -\frac{ \partial }{ \partial \phi }\frac{AR}{2} \right)=0
\end{aligned}
$$

Therefore $\vec{\omega}=0$ and the flow is irrotational. We can use Bernoulli to find the pressure:

$$
\frac{1}{2}\rho|\vec{u}|^{2}+p+\rho gz=\text{constant}
$$

There is no body force, therefore $\rho gz=0$. The Bernoulli equation gives:

$$
\begin{aligned}
\frac{1}{2}\rho|\vec{u}|^{2}+p=\text{constant} \\
\frac{1}{2}\rho\left( \frac{A^{2}R^{2}}{4}+0+(-Az)^{2} \right)+p=\text{constant} \\
\frac{1}{2}\rho\left( \frac{A^{2}R^{2}}{4}+A^{2}z^{2} \right)+p=\text{constant}
\end{aligned}
$$

At the origin $R=0, z=0$, the pressure is $p_{0}$:

$$
\begin{aligned}
\frac{1}{2}\rho(0+0)+p_{0}=\text{constant} \\
p_{0}=\text{constant}
\end{aligned}
$$

Therefore the pressure is:

$$
p=p_{0}-\frac{1}{2}\rho\left( \frac{A^{2}R^{2}}{4}+A^{2}z^{2} \right)
$$

# Exercise 4.48
## Part a

Simplifying the continuity equation for conservation of mass with $\vec{u}=(u,0,0)$

$$
\begin{aligned}
\frac{ \partial \rho }{ \partial t } +\nabla \cdot(\rho \vec{u})=0 \\
\frac{ \partial \rho }{ \partial t } +\frac{ \partial  }{ \partial x } (\rho u)=0 \\
\frac{ \partial \rho }{ \partial t } +u\frac{ \partial \rho }{ \partial x } +\rho\frac{ \partial u }{ \partial x }=0
\end{aligned}
$$

Since gravity acts in the $x$-direction, we use the conservation equation for momentum in the $x$-direction:

$$
\begin{aligned}
\rho \frac{D u_i}{D t} &= -\frac{\partial p}{\partial x_j} + \rho g_j + \mu \frac{\partial^2 u_i}{\partial x_j^2} + \left( \mu_v + \frac{1}{3} \mu \right) \frac{\partial}{\partial x_j} \frac{\partial u_m}{\partial x_m} \\
\rho \left( \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} \right) &= -\frac{\partial p}{\partial x} + \rho g_x + 2\mu \frac{\partial^2 u}{\partial x^2}
\end{aligned}
$$

## Part B

If the fluid is incompressible, we know that $\nabla \cdot \vec{u}=0$, i.e. $\frac{ \partial u }{ \partial x }=0$. $\vec{u}$ depends only on time and is spatially uniform.

Knowing this, we can simplify the continuity equation:

$$
\begin{aligned}
\frac{ \partial \rho }{ \partial t } +u\frac{ \partial \rho }{ \partial x } +\rho\frac{ \partial u }{ \partial x }=\frac{ \partial \rho }{ \partial t } +u\frac{ \partial \rho }{ \partial x } =0
\end{aligned}
$$

We can also simplify the momentum equation:

$$
\begin{aligned}
\rho \left( \frac{\partial u}{\partial t} + u \frac{\partial u}{\partial x} \right) &= -\frac{\partial p}{\partial x} + \rho g_x + 2\mu \frac{\partial^2 u}{\partial x^2} \\
\rho \frac{ \partial u }{ \partial t } =-\frac{ \partial p }{ \partial x } +\rho g_{x}
\end{aligned}
$$
