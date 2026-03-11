---
publish: true
date created: Friday, April 26th 2024, 1:51:51 pm
date modified: Monday, December 1st 2025, 12:43:47 pm
---

# Properties

The Dirac delta function is a distribution that represents unit impulses in functions. It has a defining equation:

$$
\int_{a}^{b} f(t)\delta(t-t_{0}) \, dt=\begin{cases}
f(t_{0})&a<t_{0}<b \\[10pt]
0&\text{otherwise}
\end{cases} 
$$

The Dirac delta function returns the value of the applied function at the specified value

## Derivative of a Dirac Delta Function

$$
\int_{-\infty}^{\infty} f(t)\delta^{(n)}(t-t_{0}) \, dt=(-1)^nf^{(n)}(t)
$$

# Equations

$$
\delta(f(x))=\sum_{i} \frac{\delta(x-x_{i})}{|f'(x_{i})|}
$$

With $f(x_{i})=0$ and $f'(x_{i}\neq 0)$
