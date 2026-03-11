# Single Sinusoid

Suppose you had a function

$$
f(t)=A\cos\omega t
$$

The amplitude of the function is $A$ and the period is $\frac{2\pi}{\omega}$.

# Sum of Sinusoids

Suppose you had a function:

$$
f(t)=A\sin\omega t+A\sin\omega t
$$

The period of the function is the least common multiple between the periods of the terms of the function.

The amplitude is the the factor in front of the single sinusoidal term obtained after using trigonometric identities to transform the function.

## Example:

$f(t)=3\sin\left( 2t+\frac{\pi}{4} \right)+3\sin\left( 2t-\frac{\pi}{4} \right)$

The period of $\sin\left( 2t+\frac{\pi}{4} \right)$ is $\frac{2\pi}{2}=\pi$

The period of $\sin\left( 2t-\frac{\pi}{4} \right)$ is $\frac{2\pi}{2}=\pi$

The least common multiple between the two periods is $\pi$, therefore the period is $\pi$

To find the amplitude, we use the following transformation:

$$
\begin{aligned}
& \sin a+\sin b=2\sin\left( \frac{a+b}{2} \right)\cos\left( \frac{a-b}{2} \right) \\
=&2\sin\left( \frac{\left( 2t+\frac{\pi}{4}+2t-\frac{\pi}{4} \right)}{2} \right)\cos\left( \frac{\left( 2t+\frac{\pi}{4}-2t+\frac{\pi}{4} \right)}{2} \right) \\
=&6\sin t\cos \frac{\pi}{4} \\
=&3\sqrt{ 2 }\sin t
\end{aligned}
$$

Therefore the amplitude is $3\sqrt{ 2 }$
