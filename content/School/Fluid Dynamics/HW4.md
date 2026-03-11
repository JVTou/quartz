## Streamfunctions

The formula for divergence in polar coordinates is:

$$
\vec{\nabla} \cdot \vec{u}=\frac{1}{r}\frac{ \partial ru_{r} }{ \partial r } +\frac{1}{r}\frac{ \partial u_{\phi} }{ \partial \phi }
$$

The relation between streamfunction and $\vec{u}$ in polar coordinates is:

$$
\begin{aligned}
u_{r}=\frac{1}{r}\frac{ \partial \psi }{ \partial \phi } \\
u_{\phi}=-\frac{ \partial \psi }{ \partial r }
\end{aligned}
$$

1. With $u_{r}=\frac{M}{r}$ and $u_{\phi}=0$:

$$
\vec{\nabla}\cdot\vec{u}=\frac{1}{r}\frac{ \partial  }{ \partial r } \left( r \frac{M}{r} \right)+\frac{1}{r}\frac{ \partial  }{ \partial \phi }0=\frac{1}{r}\frac{ \partial  }{ \partial r } M=0
$$

Calculating the streamfunction:

$$
\begin{aligned}
u_{r}=\frac{1}{r}\frac{ \partial \psi }{ \partial \phi } =\frac{M}{r} \\
\frac{ \partial \psi }{ \partial \phi } =M \\
\psi=M\phi
\end{aligned}
$$

![[Drawing 2024-10-29 20.40.00.excalidraw]]

The streamlines are radial lines from the origin corresponding to a constant value of the streamfunction.

1. With $u_{r}=\frac{Ua^{2}}{r^{2}}\cos \phi$ and $u_{\phi}=\frac{Ua^{2}}{r^{2}}\sin \phi$:

$$
\vec{\nabla}\cdot\vec{u}=\frac{1}{r}\frac{ \partial  }{ \partial r } \left( r \frac{Ua^{2}}{r^{2}}\cos \phi \right)+\frac{1}{r}\frac{ \partial  }{ \partial \phi }\left( \frac{Ua^{2}}{r^{2}}\sin \phi \right)=-\frac{Ua^{2}}{r^{3}}\cos \phi+\frac{1}{r}\frac{Ua^{2}}{r^{2}}\cos \phi=0
$$

Calculating the streamfunction:

$$
\begin{aligned}
u_{r}=\frac{1}{r}\frac{ \partial \psi }{ \partial \phi } = \frac{Ua^{2}}{r^{2}}\cos \phi\\
\frac{ \partial \psi }{ \partial \phi } =\frac{Ua^{2}}{r}\cos \phi \\
\psi=\frac{Ua^{2}}{r}\sin \phi
\end{aligned}
$$

Verifying with $u_{\phi}$:

$$
\begin{aligned}
u_{\phi}=-\frac{ \partial \psi }{ \partial r } =\frac{Ua^{2}}{r^{2}}\sin \phi \\
\frac{ \partial \psi }{ \partial r } =-\frac{Ua^{2}}{r^{2}}\sin \phi \\
\psi=\frac{Ua^{2}}{r}\sin \phi
\end{aligned}
$$

![[Drawing 2024-10-29 21.24.43.excalidraw]]

1. With $u_{r}=U\left( 1-\frac{a^{2}}{r^{2}} \right)\cos \phi$ and $u_{\phi}=-U\left( 1+\frac{a^{2}}{r^{2}} \right)\sin \phi$:

$$
\begin{aligned}
\vec{\nabla}\cdot\vec{u}=&\frac{1}{r}\frac{ \partial  }{ \partial r } \left( U\left( 1-\frac{a^{2}}{r^{2}} \right)\cos \phi \right)+\frac{1}{r}\frac{ \partial  }{ \partial \phi }\left( -U\left( 1+\frac{a^{2}}{r^{2}} \right)\sin \phi \right) \\
=&U\left( 1+\frac{a^{2}}{r^{2}} \right) \frac{\cos \phi}{r}-\frac{\cos \phi}{r}U\left( 1+\frac{a^{2}}{r^{2}} \right) \\
=&0
\end{aligned}
$$

Calculating the streamfunction:

$$
\begin{aligned}
u_{r}=\frac{1}{r}\frac{ \partial \psi }{ \partial \phi } = U\left( 1-\frac{a^{2}}{r^{2}} \right)\cos \phi\\
\frac{ \partial \psi }{ \partial \phi } =rU\left( 1-\frac{a^{2}}{r^{2}} \right)\cos \phi \\
\psi=rU\left( 1-\frac{a^{2}}{r^{2}} \right)\sin \phi
\end{aligned}
$$

Verifying with $u_{\phi}$:

$$
\begin{aligned}
u_{\phi}=-\frac{ \partial \psi }{ \partial r } =-U\left( 1+\frac{a^{2}}{r^{2}} \right)\sin \phi\\
\frac{ \partial \psi }{ \partial r } =U\left( 1+\frac{a^{2}}{r^{2}} \right)\sin \phi\\
\psi=U\sin \phi\left( r-\frac{a^{2}}{r} \right)=rU\sin \phi\left( 1-\frac{a^{2}}{r^{2}} \right) \\
\end{aligned}
$$

![[Drawing 2024-10-29 21.48.22.excalidraw]]

If $r=a$, then the streamfunction becomes:

$$
\psi(a)=aU\sin \phi\left( 1-\frac{a^{2}}{a^{2}} \right)=0
$$

Since the streamfunction becomes a constant, it represents a streamline for $r=a$. The flow represented by this streamfunction looks like the type of flow that occurs around a solid object.

## Vorticity
1. The vertical vorticity for a 2d axisymetric flow is:

$$
\omega_{z}=\frac{1}{r}\frac{d}{dr}(ru_{\phi})
$$

Here, for $r\leq a$, we know that the Rankine vortex behaves like a solid body, i.e. $u_{\phi}=\Omega r$, with $\Omega$ a constant angular velocity. Substituting this into out vorticity gives:

$$
\omega_{z}=\frac{1}{r}\frac{d}{dr} (r^{2}\Omega)=\frac{2r\Omega}{r}=2\Omega
$$

We also know that for $r\geq a$, the Rankine vortex flow is irrotational, i.e. $\omega_{z}=0$.

1. The vertical vorticity of any general flow in cartesian coordinates is defined as the curl of the velocity in the x-y plane

$$
\omega_{z}=\frac{ \partial v }{ \partial x } -\frac{ \partial u }{ \partial y }
$$

We know that the velocity components $u$ and $v$ are related to the streamfunction:

$$
\begin{aligned}

u=\frac{ \partial \psi }{ \partial y }  \\

v=-\frac{ \partial \psi }{ \partial x }

\end{aligned}
$$

Substituting these values into our $\omega_{z}$ equation gives:

$$
\begin{aligned}

\omega_{z}&=-\frac{ \partial  }{ \partial x } \frac{ \partial \psi }{ \partial x }-\frac{ \partial  }{ \partial y } \frac{ \partial \psi }{ \partial y } \\

&=-\frac{ \partial^{2} \psi }{ \partial x^{2} } -\frac{ \partial^{2} \psi }{ \partial y^{2} }  \\

&=-\nabla^{2}_{h}\psi

\end{aligned}
$$

1. In plane polar coordinates, the Laplacian operator is:

$$
\nabla^{2}=\frac{1}{r}\frac{ \partial  }{ \partial r } \left( r\frac{ \partial  }{ \partial r }  \right)+\frac{1}{r^{2}}\frac{ \partial^{2}  }{ \partial \phi^{2} }
$$

Since the flow is axisymetric, the terms of $\psi$ in $\phi$ are not changing, therefore:

$$
\nabla^{2}\psi=\frac{1}{r}\frac{ \partial  }{ \partial r } \left( r\frac{ \partial \psi }{ \partial r }  \right)+\cancelto{ 0 }{ \frac{1}{r^{2}}\frac{ \partial^{2} \psi }{ \partial \phi^{2} }  }
$$

1. We know from previous questions that:

$$
   \begin{aligned}

\omega_{z}=-\nabla^{2}_{h}\psi=\frac{1}{r}\frac{d}{dr}(ru_{\phi}) \\

\nabla^{2}_{h}\psi=-\frac{1}{r}\frac{d}{dr} (ru_{\phi})

\end{aligned}
$$

In the $r\leq a$ region, $\omega_{z}=2\Omega$. Integrating this equation once gives:

$$
\begin{aligned}

2\Omega=\frac{1}{r}\frac{d}{dr} (ru_{\phi}) \\

\int 2\Omega r \, dr=\int \frac{d}{dr} (ru_{\phi}) \, dr \\

\Omega r^{2}=ru_{\phi}+C   \\

\end{aligned}
$$

For $r=0$, we want no vorticity, so we set $C=0$:

$$
u_{\phi}=\Omega r
$$

Finding a relation between $u_{\phi}$ and $\psi$:

$$
u_{\phi}=-\frac{1}{r}\frac{d\psi}{dr}
$$

Integrating this gives us $\psi$:

$$
\begin{aligned}

\Omega r=-\frac{1}{r}\frac{d\psi}{dr}  \\

-\Omega r^{2}=\frac{d\psi}{dr} \\

\psi=-\frac{\Omega r^{3}}{3}+C_{1}

\end{aligned}
$$

In the $r\geq a$ region, $\omega_{z}=0$. Integrating gives:

$$
\begin{aligned}

0=\frac{1}{r} \frac{d}{dr}(ru_{\phi}) \\

ru_{\phi}=\text{constant K} \\

u_{\phi}=\frac{K}{r}

\end{aligned}
$$

Integrating again:

$$
\begin{aligned}

\frac{K}{r}=-\frac{1}{r} \frac{d\psi}{dr} \\

\frac{d\psi}{dr}=-K \\

\psi=-Kr+C_{2}

\end{aligned}
$$

1. We want the velocity at the boundaries to be equal, i.e.:

$$
   \begin{aligned}

u_{\text{inner}}(r=a)=u_{\text{outer}}(r=a) \\

\Omega a=\frac{K}{a} \\

K=\Omega a^{2}

\end{aligned}
$$

We also want the streamfunction equal at the boundary, i.e.:

$$
\begin{aligned}

\psi_{\text{inner}}(r=a)=\psi_{\text{outer}}(r=a) \\

-\frac{\Omega a^{3}}{3}+C_{1}=-Ka+C_{2} \\

-\frac{\Omega}{3}a^{3}+\Omega a^{3}=C_{2}-C_{1} \\

a^{3}\left( \frac{2}{3}\Omega \right)=C_{2}-C_{1} \\

C_{2}=\frac{a^{3}2}{3}\Omega+C_{1}

\end{aligned}
$$

1. ![[Drawing 2024-10-30 08.11.03.excalidraw]]
2. The circulation is:

$$
\Gamma=\int_{0}^{2\pi} u_{\phi}r \, d\phi
$$

Since $u_{\phi}$ is constant along $\phi$, this equation becomes:

$$
\Gamma=2\pi u_{\phi}r
$$

For $r\leq a$, $u_{\phi}=\Omega r$, therefore the circulation is:

$$
\Gamma=2\pi\Omega r^{2}
$$

For $r\geq a$, $u_{\phi}=\frac{K}{r}$, therefore the circulation is:

$$
\Gamma=2\pi K
$$

1. The fact that the Rankine vortex changes velocities abruptly at $a$, coupled with the fact that there is no viscosity present at the boundary, prevents this model from fully capturing a real vortex. A real vortex would have a gradual change in velocity from the center outwards, and the viscosity would create turbulences and possibly secondary vortices.
