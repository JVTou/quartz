Let's look at cases where:

$$
\begin{aligned}
u(x)=\begin{cases}
0 & \text{for } 0\leq x\leq w \\
u_{0}  & \text{for }x>0 \text{ and } x>w
\end{cases}
\end{aligned}
$$

![[Excalidraw/Finite Well]]

There are two cases to consider in a finite well:

1. When $u(-L)=u(L)=u_{0}$
2. When $E<u_{0}$
# Case 1

$\psi_{I}(x)=Ae^{ k_{0}x }$

$\psi_{II}(x)=C\sin kx$

$\psi_{III}(x)=-Ae^{ -k_{0}x }$

# Case 2

$\psi_{I}(x)=Ae^{ k_{0}x }$

$\psi_{II}(x)=D\cos kx$

$\psi_{III}(x)=Ae^{ -k_{0}x }$

# Quantizing Energy in the Finite well
## Case 1

We have two boundary conditions:

1. $Ae^{ k_{0}L }=D\cos kL$
2. $Ak_{0}e^{ -k_{0}L }=kD\sin kL$
Dividing the boundary conditions gives:

$$
\frac{1}{k_{0}}=\frac{1}{k}\cot(kL)\implies k_{0}=-k\cot(kL)
$$

## Case 2

We also have two boundary conditions:

1. $Ae^{ -k_{0}L }=D\cos(kL)$
2. $Ak_{0}e^{ -k_{0}L }=kD\sin(kL)$
Again, dividing the boundary conditions gives:

$$
\frac{1}{k_{0}}=\frac{1}{k}\cot(kL)\implies k_{0}=k\tan(kL)
$$

## Outside the well
