---
date created: Thursday, May 16th 2024, 5:23:54 pm
date modified: Monday, December 1st 2025, 12:28:52 pm
---
# Example

Find the general solution to:

$$
y''(x)-y'(x)-2y(x)=0
$$

# Method
- Expand $y$ as a series:

$$
y(x)=\sum_{n=0}^{\infty} a_{n}x^n
$$

- Differentiate your expansion to the order of your differential equation. Watch the indexes for your summation, they will only start when the terms are not $0$:

$$
\begin{aligned}

y'(x)=&\sum_{n=1}^{\infty} a_{n}nx^{n-1} \\

y''(x)=&\sum_{n=2}^{\infty} a_{n}n(n-1)x^{n-1}

\end{aligned}
$$

- Replace $y''(x)$, $y'(x)$ and $y(x)$ with their expansions in the original equation:

$$
\begin{aligned}
y''(x)-y'(x)-2y(x)&=0 \\
\sum_{n=2}^{\infty} a_{n}n(n-1)x^{n-1}-\sum_{n=1}^{\infty} a_{n}nx^{n}-2\sum_{n=0}^{\infty} a_{n}x^n&=0
\end{aligned}
$$

- Each $x$-term in our summation must have the same power of $n$. Change the index for each summation so that the $x$-term is the same in each summation. Here, $n\to n+1$ for the expansion of $y''$:

$$
\begin{aligned}
\sum_{n=2}^{\infty} a_{n}n(n-1)x^{n-1}-\sum_{n=1}^{\infty} a_{n}nx^{n}-2\sum_{n=0}^{\infty} a_{n}x^n&=0 \\
\sum_{n=1}^{\infty} a_{n+1}(n+1)nx^{n}-\sum_{n=1}^{\infty} a_{n}nx^{n}-2\sum_{n=0}^{\infty} a_{n}x^n&=0
\end{aligned}
$$

- For each summation to start at the same index for $n$, we write out the terms below the highest $n$-index for the sums preceding the sum with the highest $n$-index:

$$
\begin{aligned}
n=0:-2a_{0}&=0 \\
a_{0}&=0
\end{aligned}
$$

- Write the relationship for the coefficients at each subsequent term in the summation:

$$
$$
