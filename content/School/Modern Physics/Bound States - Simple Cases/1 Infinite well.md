# Potential Energy Function for an Infinite well

We are studying a particle confined to a 1-D box with impenetrable walls (they require infinite energy to pass through, i.e. you can't get through).

![[Infinite 1-D well]]

This implies that potential energy

$$
u(x)=\begin{cases}
0&\text{when }0\leq x\leq w\\
\infty&\text{when }|x|>w
\end{cases}
$$

This potential function $u(x)$ is also called a 1-D infinite well.

# Standing Wave Patterns

In the 1-D infinite well, we expect $\psi(x)$ to take a standing wave form. In general:

$$
\begin{aligned}
\psi(x)=A\sin(kx)+B\cos(kx)
\end{aligned}
$$

We want to find A, B and k. To do this, we use information about the bounds: we observe that $\psi(x=0)=\psi(x=w)=0$

$$
\begin{cases}
\text{At }x=0\text{, }\psi(0)=A\sin(k\cdot0)+B\cos(k\cdot0)=0\Leftrightarrow B=0\\
\text{At }x=w\text{, }\psi(w)=A\sin(kw)=0\Leftrightarrow kw=n\pi\text{ and }k_n=\frac{n\pi}{w}\text{ with }n=1,2,3\dots
\end{cases}
$$

This shows that, when energy is bounded, it becomes quantized into discrete values. At $n=1$, the energy is at its ground state (fundamental mode). At $n=2$, the energy is in its first excited state; at $n=3$, the energy is in its second excited state…

More generally:

$$
\begin{aligned}
\psi(x)=A\sin(k_nx)
\end{aligned}
$$

With $k_n=\frac{n\pi}{w}$.

To calculate $A$, we need to [[Normalization|normalize]] the wave function $\psi(x)$:

$$
\begin{aligned}
\int_0^w\psi^*(x)\psi(x)dx=1
\end{aligned}
$$

Let's focus on the left hand side of this equation:

$$
\begin{aligned}
\int_0^w\psi^*(x)\psi(x)dx&=\int_0^wA^2\sin^2(k_nx)dx\\
&=A^2\int_0^w\sin^2(k_nx)dx\\
\sin^2(\theta)=\frac{1-\cos(2\theta)}{2}\\
&=\frac{A^2}{2}\int_0^w\left[1-\cos(2k_nx)\right]dx\\
&=\frac{A^2}{2}\left[\int_0^wdx-\int_0^w\cos(2k_nx)dx\right]\\
&=\frac{A^2}{2}\left[w-\frac{\sin(2k_nx)}{2k_n}\biggr\rvert_0^w\right]\\
&=\frac{A^2}{2}\left[w-\frac{1}{2k_n}\left(\sin(2k_nw)-sin(2k_n\cdot0)\right)\right]\\
&=\frac{A^2}{2}\left[w-\frac{1}{2k_n}\sin(2k_nw)\right]\\
\sin(2k_nw)=\sin(2\frac{n\pi}{w}w)\\
=\sin(2n\pi)=0\\
&=\frac{A^2}{2}w
\end{aligned}
$$

Therefore:

$$
\begin{aligned}
&\frac{A^2}{2}w=1\Leftrightarrow A=\sqrt{\frac{2}{w}}\\
&\text{and}\\
&\psi_n(x)=\sqrt{\frac{2}{w}}\sin k_nx
\end{aligned}
$$

# Finding a Probability

To find the probability that a particle is in the third excited state ($n=4$) between two points $x_2$ and $x_1$ between 0 and w, we make the following probability calculation:

$$
\begin{aligned}
\int_{x_1}^{x_2}\psi^*(x)\psi(x)dx&=\int_{x_1}^{x_2}\left(\sqrt{\frac{2}{w}}\right)^2\sin^2(k_nx)dx\\
&=\frac{2}{w}\int_{x_1}^{x_2}\sin^2(k_nx)dx\\
&=\frac{1}{w}\int_{x_1}^{x_2}\left[1-\cos(2k_nx)\right]dx\\
&=\frac{1}{w}\left[\int_{x_1}^{x_2}-\int_{x_1}^{x_2}\cos(2k_nx)dx\right]\\
&=\frac{1}{w}\left[(x_2-x_1)-\frac{\sin(2k_nx)}{2k_n}\biggr\rvert_{x_1}^{x_2}\right]\\
&=\frac{1}{w}\left[(x_2-x_1)-\frac{1}{2k_n}\left(\sin(2k_nx_2)-sin(2k_nx_1)\right)\right]\\
k_n=\frac{n\pi}{w}\\
&=\frac{x_2-x_1}{w}-\frac{1}{2n\pi}\left[\sin(2\frac{n\pi}{w}x_2)-sin(2\frac{n\pi}{w}x_1)\right]
\end{aligned}
$$

Then use $n=4$ and the known values for $x_1$, $x_2$ and $w$.

Suppose that $w$ is unknown, but we know the total energy in a certain excited state $n$. Knowing that $u(x)=0$ in the well:

$$
\begin{aligned}
\text{KE}\psi(x)+\mu_0\psi(x)&=\text{E}\psi(x)\\
\text{E}=\text{KE}=\frac{(\hbar k)^2}{2m}
\end{aligned}
$$

Therefore E is quantized:

$$
\begin{aligned}
\text{E}_n=\frac{\hbar^2}{2m}\left(\frac{n\pi}{w}\right)^2
\end{aligned}
$$

And $w$ can be isolated to give:

$$
\begin{aligned}
w=\frac{\hbar n\pi}{\sqrt{2m\text{E}_n}}
\end{aligned}
$$

# Changing Energy Levels

To change energy levels, an electron obeys the [[2 De Broglie relationship]]
