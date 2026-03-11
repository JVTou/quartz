---
date created: Thursday, April 11th 2024, 10:08:23 am
date modified: Wednesday, March 11th 2026, 12:17:58 pm
---
# 2$\pi$-periodic Functions

If $f(x)=f(x+2\pi)$, and is a well-behaved function, then:

$$
f(x)=\sum_{n=-\infty}^{\infty}c_{n}e^{ inx }
$$

With:

$$
c_{m}=\frac{1}{2\pi}\int_{0}^{2\pi} f(x)e^{ -imx } \, dx 
$$

## Example

$f(x)=x$ for $-\pi<x<\pi$

Since $f(x)$ is $2\pi$ periodic, we can represent it with:

$$
f(x)=\sum_{n=-\infty}^{\infty}c_{n}e^{ inx }
$$

Let's calculate $c_{n}$:

$$
\begin{aligned}
c_{n}&=\frac{1}{2\pi}\int_{-\pi}^{\pi} f(x)e^{ -inx } \, dx  \\
&=\frac{1}{2\pi}\int_{-\pi}^{\pi} xe^{ -inx } \, dx \\
\end{aligned}
$$

Using integration by parts, we get:

$$
\begin{aligned}
c_{n}&=\frac{1}{2\pi} \frac{ix}{n}e^{ -inx }\bigg\rvert^{\pi}_{-\pi}-\frac{1}{2\pi}\int_{-\pi}^{\pi} \frac{i}{n}e^{ -inx } \, dx \\
&=
\end{aligned}
$$

# 2l-periodic Functions

If $f(x)=f(x+2l)$, and is a well-behaved function, then:

$$
f(x)=\sum_{n=-\infty}^{\infty}c_{n}e^{ in\pi x/l }
$$

With:

$$
c_{m}=\frac{1}{2l} \int_{-l}^{l} f(x)e^{ -im\pi x/l } \, dx
$$

# Cosine and Sine Series

We can also express periodic functions with sums of sine and cosine functions:

$$
f(x)=\frac{a_{0}}{2}+\sum_{n=1 }^{\infty} \left(a_{n}\cos\left( \frac{n\pi x}{l} \right)+b_{n}\sin\left( \frac{n\pi x}{l} \right)\right)
$$

With:

$$
\begin{aligned}
a_{n}&=\frac{1}{l}\int_{-l}^{l} f(x)\cos\left( \frac{n\pi x}{l} \right) \, dx  \\
b_{n}&=\frac{1}{l}\int_{-l}^{l} f(x)\sin\left( \frac{n\pi x}{l} \right) \, dx
\end{aligned}
$$

- If the function is even, $b_{n}=0$
- If the function is odd, $a_{n}=0$
