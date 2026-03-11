# Deriving Schrödinger's Equation for a Free-particle

A free-particle has no potential energy, since it does not have any interactions, by definition. Applying conservation of energy to a free-particle gives:

$$
\begin{aligned}
\text{KE}\psi_{(x,t)}+\cancelto{0}{\text{U}\psi_{(x,t)}}=\text{E}\psi_{(x,t)}
\end{aligned}
$$

Applying the kinetic energy operator

$\text{KE}=-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}$ to

$\psi(x,t)$ gives:

$$
\begin{aligned}
\text{KE}\psi(x,t)&=-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}\psi(x,t)\\
-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}\psi(x,t)&=-\frac{\hbar^2}{2m}\left(-k^2\right)\psi(x,t)\\
k^2\psi(x,t)&=-\frac{\partial^2}{\partial x^2}\psi(x,t)
\end{aligned}
$$

Applying the total energy operator

$\text{E}=i\hbar\frac{\partial}{\partial t}$ to $\psi(x,t)$

gives:

$$
\begin{aligned}
\text{E}\psi(x,t)&=i\hbar\frac{\partial}{\partial t}\psi(x,t)\\
i\hbar\frac{\partial}{\partial t}\psi(x,t)&=i\hbar(-i)\omega\psi(x,t)\\
\omega\psi(x,t)&=\frac{1}{-i}\frac{\partial}{\partial t}\psi(x,t)\\
\omega\psi(x,t)&=i\frac{\partial}{\partial t}\psi(x,t)
\end{aligned}
$$

Using these new values for $\text{KE}\psi_{(x,t)}$ and $\text{E}\psi_{(x,t)}$ in the conservation of energy for a free-particle gives Schrödinger's equation for a free-particle:

$$
\begin{aligned}
-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}\psi(x,t)=i\hbar\frac{\partial}{\partial t}\psi(x,t)
\end{aligned}
$$

If there are interactions, this equation generalizes to Schrödinger's equation in one dimension:

$$
\begin{aligned}
-\frac{\hbar^2}{2m}\frac{\partial^2}{\partial x^2}\psi(x,t)+u(x)\psi(x,t)=i\hbar\frac{\partial}{\partial t}\psi(x,t)
\end{aligned}
$$

[[Normalization]]

[[Expectation]]
