To solve [[4 Schrödinger's equation]], we use separation of variables, assuming the wave function $\Psi(x,t)$ is a product of a spatial and temporal part:

$$
\Psi(x,t)=\psi(x)\phi(t)
$$

Substituting this into Schrödinger's equation gives:

$$
\begin{aligned}
-\frac{\hbar^{2}}{2m}\phi(t) \frac{ \partial^{2} \psi(x) }{ \partial x^{2} } +U(x)\psi(x)\phi(t)=i\hbar \psi(x) \frac{ \partial \phi(t) }{ \partial t }  \\
-\frac{\hbar^{2}}{2m} \frac{1}{\psi(x)} \frac{ \partial^{2} \psi(x) }{ \partial x^{2} } +U(x)=i\hbar \frac{1}{\phi(t)} \frac{ \partial \phi(t) }{ \partial t }
\end{aligned}
$$

The two sides of the equation depend on only either $x$ or $t$, so they must be equal to some constant $C$:

$$
\begin{aligned}
C=
\begin{cases}
-\frac{\hbar^{2}}{2m} \frac{1}{\psi(x)} \frac{ \partial^{2} \psi(x) }{ \partial x^{2} } +U(x) &\text{ (positional part)}\\
i\hbar \frac{1}{\phi (t)} \frac{ \partial \phi(t) }{ \partial t } &\text{ (temporal part)}
\end{cases}
\end{aligned}
$$

# Solving for $\phi(t)$

The temporal part of the Schrödinger's equation with separated variables is:

$$
\begin{aligned}
C=i\hbar \frac{1}{\phi(t)} \frac{ \partial \phi(t) }{ \partial t }  \\
\frac{ \partial \phi(t) }{ \partial t } =\frac{i\hbar C}{\phi(t)}
\end{aligned}
$$

This is a first order linear differential equation, whose solution is:

$$
\phi(t)=e^{ -i(C/\hbar)t }
$$

Rewriting with Euler's formula gives:

$$
\phi(t)=\cos\left[ \left( \frac{C}{\hbar} \right)t \right]-i\sin\left[ \left( \frac{C}{\hbar } \right)t \right]
$$

$\frac{C}{\hbar}t$ must be in radians, so $\frac{C}{\hbar}$ must be in radians per second, i.e. $\frac{C}{\hbar}=\omega$

The [[2 Properties of matter waves#Fundamental wave-particle relationships|fundamental wave-particle relationships]] state that $E=\hbar \omega$, and thus $C=\hbar \omega=E$.

Therefore:

$$
\phi(t)=e^{ -i(E/\hbar)t }
$$

# Time-independent Schrödinger's Equation

Knowing that $C=E$, we can then write the Schrödinger's equation as:

$$
-\frac{\hbar^{2}}{2m} \frac{ \partial^{2} \psi(x) }{ \partial x^{2} } +U(x)=E\psi(x)
$$
