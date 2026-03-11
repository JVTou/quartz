# Definition

A traveling wave (time-dependent wave) is modeled by the equation:

$$
\psi_{\vec{x},t}=\psi_{\text{max}}e^{i(kx-\omega t)}
$$

# Satisfying the Wave Equation

In general, wave equations satisfy the following relationship:

$$
\frac{\partial^2\psi_{(x,t)}}{\partial x^2}=\frac{1}{v^2}\frac{\partial^2\psi_{(x,t)}}{\partial t^2}
$$

Let's check to see if the traveling wave equation satisfies the wave equation, starting with the left side:

$$
\begin{aligned}
\frac{\partial^2\psi_{(x,t)}}{\partial x^2}
&=\frac{\partial}{\partial x}\left[\frac{\partial}{\partial x}\psi_{max}e^{i(kx-\omega t)}\right]\\
&=\frac{\partial}{\partial x}\left[ik\psi_{max}e^{i(kx-\omega t)}\right]\\
&=(ik)^2\left[\psi_{max}e^{i(kx-\omega t)}\right]\\
&=-k^2\psi_{(x,t)}\\
\frac{\partial^2\psi_{(x,t)}}{\partial x^2}&=-k^2\psi_{(x,t)}
\end{aligned}
$$

Verifying the right side of the wave equation

$$
\begin{aligned}
\frac{\partial^2\psi_{(x,t)}}{\partial t^2}
&=\frac{\partial}{\partial t}\left[\frac{\partial}{\partial t}\psi_{max}e^{i(kx-\omega t)}\right]\\
&=\frac{\partial}{\partial t}\left[-i\omega\psi_{max}e^{i(kx-\omega t)}\right]\\
&=-\left(i\omega\right)^2\psi_{max}e^{i(kx-\omega t)}\\
\frac{\partial^2\psi_{(x,t)}}{\partial t^2}&=-\omega^2\psi_{(x,t)}
\end{aligned}
$$

We also know from the above equation that:

$$
\psi_{(x,t)}=-\frac{1}{\omega^2}\frac{\partial^2\psi_{(x,t)}}{\partial t^2}
$$

Substituting this new identity for $\psi_{(x,t)}$ into the left side of the wave equation gives:

$$
\begin{aligned}
\frac{\partial^2\psi_{(x,t)}}{\partial x^2}
&=-k^2\left(-\frac{1}{\omega^2}\frac{\partial^2\psi_{(x,t)}}{\partial t^2}\right)\\
\frac{\partial^2\psi_{(x,t)}}{\partial x^2}
&=\frac{k^2}{\omega^2}\left(\frac{\partial^2\psi_{(x,t)}}{\partial t^2}\right)
\end{aligned}
$$

Which satisfies the wave equation for $\frac{\omega}{k}=v$
