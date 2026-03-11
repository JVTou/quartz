---
date created: Friday, February 28th 2025, 12:01:01 pm
date modified: Tuesday, February 24th 2026, 9:25:33 pm
---
# Question 3

We're trying to prove that

$$
P(X>s+t|X>s) = P(X>t)
$$

Knowing that $X \sim \text{exp}(\lambda)$, we can write $P(X>t)=1-F(t) = 1-(1-e^{ -\lambda x })=e^{ -\lambda x }$. We can then write the above equality as:

$$
P(X>s+t|X>s) = \frac{P(X> s+t)}{P(X> s)}=\frac{e^{ -\lambda(s+t) }}{e^{ -\lambda s }}=e^{ -\lambda t }=P(X> t)
$$

# Question 4

Given that $X =-\frac{\log(U)}{\lambda}$, we can write it's CDF as:

$$
\begin{aligned}
F(X)=P\left( -\frac{\log(U)}{\lambda}\leq x \right) \\
-\frac{\log(U)}{\lambda}\leq x  \\
\log(U)\geq -\lambda x \\
U \geq e^{ -\lambda x }
\end{aligned}
$$

Therefore $P\left( -\frac{\log(U)}{\lambda}\leq x \right)=P(U \geq e^{ -\lambda x })=1-P(U \leq e^{ -\lambda x })$

Since $U\sim Unif(0,1)$, we know that it's CDF is:

$$
P(U\leq u)=u,0\leq u\leq 1
$$

Therefore $1-P(U \leq e^{ -\lambda x })=1-e^{ -\lambda x }$ for $x\geq 0$ and $0$ otherwise. This matches the CDF of an exponential distribution $X\sim Exp(\lambda)$:

$$
F(x)=\begin{cases}
0 & x<0 \\
1-e^{ -\lambda x }&x\geq 0
\end{cases}
$$

# Question 5

To prove that $SZ\sim N(0,1)$, we will prove that $SZ$ follows the mean and variance of a normal distribution, and is symmetric about $0$.

Since $S$ and $Z$ are independent, their expectation is:

$$
E[SZ]=E[S]E[Z]=\left( \frac{1}{2}\cdot1+\frac{1}{2}\cdot (-1) \right)\cdot0=0
$$

 And the variance is:

$$
Var(SZ)=E[(SZ)^{2}]-E[SZ]^{2}=E[S^{2}]E[Z^{2}]-0^{2}=\left( \frac{1}{2}\cdot1^{2}+\frac{1}{2}\cdot (-1)^{2} \right)\cdot(1+0)=1
$$

$S$ is either $1$ or $-1$ with equal probability, which means it reflects $Z\sim N(0,1)$ across $0$.

Therefore $SZ$ follows the mean and variance of a normal distribution, and is symmetric about $0$: $SZ\sim N(0,1)$.
