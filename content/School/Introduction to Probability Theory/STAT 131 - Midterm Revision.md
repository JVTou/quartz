---
date created: Friday, February 28th 2025, 12:01:01 pm
date modified: Tuesday, February 24th 2026, 9:25:29 pm
---

We will use the law of total probability to find the probability of picking a yellow ball, with the events ${U_{i}}$ (choosing the $i^{th}$ urn) forming partitions of the sample space $\Omega$, and the events $Y\subset\Omega$ (Y: picking the yellow ball)

$$
\begin{aligned}
P(Y)&=\sum_{i=1}^3P(U_{i})P(Y|U_{i}) \\
&=P(U_{1})P(Y|U_{1})+P(U_{2})P(Y|U_{2})+P(U_{3})P(Y|U_{3}) \\
&=\frac{1}{2} \frac{2}{6} +\frac{1}{4} \frac{1}{6} + \frac{1}{4} \frac{3}{6} \\
&=\frac{1}{3}
\end{aligned}
$$

So the probability of picking a yellow ball is $\frac{1}{3}$.
