1. 
   1. Here we derive the Fermi energy for $E=pc$. The allowed energies in the system are:
	$$
	\epsilon=pc
	$$
	With
	$$
	p=\begin{cases}
	p_{x}=\frac{hn_{x}}{2L} \\
	p_{y}=\frac{hn_{y}}{2L} \\
	p_{z}=\frac{hn_{z}}{2L}
	\end{cases}
	$$
	So we rewrite $\epsilon$ as:
	$$
	\epsilon=\frac{hc}{2L}n
	$$
	The Fermi energy is the energy of a state that is on the outermost bounds of our $n$-space, so
	$$
	\epsilon_{F}=\frac{hc}{2L}n_{max}
	$$
	The total number of occupied states is $N=\frac{\pi n_{max}^{3}}{3}$ or $n_{max}=\left( \frac{3N}{\pi} \right)^{1/3}$ and the volume is $V=L^{3}$ or $L=V^{1/3}$, which we can use to rewrite the Fermi energy as:
	$$
	\epsilon_{F}=\frac{hc}{2} \left( \frac{3N}{\pi V} \right)^{1/3}
	$$
	2. The total energy of the system is found by summing all possible energies, which ends up being an integral over the spherical coordinates of our system:
	$$
	\begin{aligned}
	U & =2\iiint\epsilon dn_{x}dn_{y}dn_{z}=2 \\
	 & =\int_{0}^{n_{max}} \frac{hc}{2L}nn^{2} \, dn \int_{0}^{\pi/2} \sin\theta \, d\theta \int_{0}^{\pi/2}  \, d\phi    \\
	 & =2 \frac{1}{4}n_{max}^{4}(-\cos\theta)\rvert_{0}^{\pi/2} \frac{\pi}{2} \frac{hc}{2L} \\
	 & =\frac{1}{4}n_{max}^{4}\pi  \frac{hc}{2L} \\
	 & =\frac{3}{4}Nn_{max} \frac{hc}{2L} \\
	 & =\frac{3}{4}N\epsilon_{F}
	\end{aligned}
	$$
2. 
   1. With electrons, we can write their energy and distance from the origin as
		$$
		\begin{cases}
		\epsilon=\frac{p^{2}}{2m_{e}}=\frac{h^{2}n^{2}}{4A} \frac{1}{2m_{e}}=\frac{h^{2}n^{2}}{8Am_{e}} \\
		n=\sqrt{ \frac{8Am_{e}}{h^{2}} }\sqrt{ \epsilon } \\
		dn=\sqrt{ \frac{8Am_{e}}{h^{2}} } \frac{1}{2\sqrt{ \epsilon }}d\epsilon
		\end{cases}
		$$
		We write the total energy $U$ of all the electrons in our space as:
		$$
		\begin{aligned}
		U & =2\int_{0}^{n_{max}} \int_{0}^{\pi/2} \epsilon(n)n \, d\theta  \, dn \\
		 & =\pi \int_{0}^{n_{max}} \epsilon(n)n \, dn \\
		 & =\pi \int_{0}^{\epsilon_{F}} \frac{h^{2}n^{2}}{8Am_{e}}\sqrt{ \frac{8Am_{e}}{h^{2}} }\sqrt{ \frac{h^{2}n^{2}}{8Am_{e}} }\sqrt{ \frac{8Am_{e}}{h^{2}} } \frac{1}{2\sqrt{ \frac{h^{2}n^{2}}{8Am_{e}} }} \, dx \\
		 & =\pi \int_{0}^{\epsilon_{F}} \frac{h^{2}n^{2}}{8Am_{e}} \frac{8Am_{e}}{h^{2}} \frac{1}{2} \, d\epsilon \\
		 & = \int_{0}^{\epsilon_{F}} \frac{\pi}{2} \frac{8Am_{e}}{h^{2}}\epsilon \, d\epsilon  \\
		 & =\int_{0}^{\epsilon_{F}} \rho(\epsilon)\epsilon \, d\epsilon 
		\end{aligned}
		$$
		Therefore $\rho(\epsilon)=\frac{4\pi Am_{e}}{h^{2}}$.
	2. For photons, assuming their momentum $p$ obeys the same equations as electrons, have an energy and distance from the origin of:
		$$
		\begin{cases}
		\epsilon=pc=\frac{hn}{2L}c \\
		n=\frac{2L}{hc}\epsilon \\
		dn=\frac{2L}{hc}d\epsilon
		\end{cases}
		$$
		We write the total energy of all photons in our $n$-space as:
		$$
		\begin{aligned}
		U & =\pi \int_{0}^{n_{max}} \epsilon(n)n \, dn \\
		 & =\pi \int_{0}^{\epsilon_{F}} \frac{hn}{2L}c \frac{2L}{hc} \frac{hn}{2L}c \frac{2L}{hc} \, d\epsilon \\
		 & =\int_{0}^{\epsilon_{F}} \pi \left( \frac{hnc}{2L} \right)^{2} \left( \frac{2L}{hc} \right)^{2} \, d\epsilon \\
		 & =\int_{0}^{\epsilon_{F}} \pi n^{2} \, d\epsilon \\
		 & =\int_{0}^{\epsilon_{F}} \frac{\pi4A}{h^{2}c^{2}}\epsilon\epsilon d\epsilon \\
		 & =\int_{0}^{\epsilon_{F}}\rho(\epsilon)\epsilon \,d\epsilon
		\end{aligned}
		$$
		Therefore $\rho(\epsilon)=\frac{4\pi A}{h^{2}c^{2}}\epsilon$.
3. 
   1. We can write the energy levels and $n$-space of our system as:
		$$
		\begin{aligned}
		\epsilon & =nhf \\
		n & =\frac{\epsilon}{hf} \\
		dn & =\frac{1}{hf}d\epsilon
		\end{aligned}
		$$
		The degeneracy of each level is the density of states times each level:
		$$
		\rho(n)dn=(n+1)(n+2) \frac{1}{2}dn
		$$
		If we take $n\gg 1$, we can approximate the above equation as:
		$$
		\begin{aligned}
		\rho(n)dn & =\frac{1}{2}n^{2}dn \\
		\rho(\epsilon)d\epsilon & =\frac{\epsilon^{2}}{(hf)^{2}} \frac{1}{2} \frac{1}{hf} d\epsilon \\
		\rho(\epsilon) & =\frac{\epsilon^{2}}{2(hf)^{3}}
		\end{aligned}
		$$
	2. To calculate our condensation temperature, we need to calculate the total number of atoms $N$:
		$$
		\begin{aligned}
		N & =\int_{0}^{\infty} g(\epsilon) \frac{1}{e^{ (\epsilon-\mu)/kT }-1} \, d\epsilon  \\
		 & =\int_{0}^{\infty} \frac{\epsilon^{2}}{2(hf)^{3}} \frac{1}{e^{ (\epsilon-\mu)/kT }-1} \, d\epsilon 
		\end{aligned}
		$$
		We take a gander and estimate $\mu=0$, and make a change of variables: $x=\frac{\epsilon}{kT}$ and $dx=\frac{1}{kT}d\epsilon$:
		$$
		\begin{aligned}
		N & =\int_{0}^{\infty} \frac{\epsilon^{2}}{2(hf)^{3}} \frac{1}{e^{ x }-1} kT \, dx  \\
		 & =\int_{0}^{\infty} \frac{\epsilon^{2}}{2(hf)^{3}} \frac{1}{e^{ x }-1} kt \, dx \\
		 & =\int_{0}^{\infty} \frac{(xkT)^{2}}{2(hf)^{3}} \frac{1}{e^{ x }-1} kT \, dx \\
		 & =\int_{0}^{\infty} \frac{(kT)^{3}}{2(hf)^{3}} \frac{x^{2}}{e^{ x }-1} \, dx \\
		 & = \frac{(kT)^{3}}{2(hf)^{3}}\int_{0}^{\infty}  \frac{x^{2}}{e^{ x }-1} \, dx \\
		 & \approx \frac{2.404}{2} \left( \frac{kT}{hf} \right)^{3}
		\end{aligned}
		$$
		We isolate $T$, which can be written $T_{c}$ as it is the condensation temperature, which gives:
		$$
		T_{c}=\left( \frac{N}{1.202} \right)^{1/3} \frac{hf}{k}
		$$
	3. We want to show that these two expressions are roughly equivalent:
		$$
		\begin{aligned}
		T_{c}=\left( \frac{N}{1.202} \right)^{1/3} \frac{hf}{k}
		\end{aligned}
		$$
		$$
		kT_{c}=0.527\left( \frac{h^{2}}{2\pi m} \right)\left( \frac{N}{V} \right)^{2/3}
		$$
		We know that the total energy of a simple harmonic oscillator is:
		$$
		E_{SHO}=\frac{1}{2}m(2\pi f)^{2}a^{2}=\frac{1}{2}\kappa a^{2}
		$$
		We set this total energy equal to the the energy equivalent of condensation temperature gives:
		$$
		\frac{1}{2}\kappa a^{2}=kT_{c}
		$$
		We isolate to find $a$:
		$$
		\begin{aligned}
		a & =\sqrt{ \frac{2kT_{c}}{\kappa} } \\
		\end{aligned}
		$$
		And use $T_{c}$ from the previous question:
		$$
		\begin{aligned}
		a & =\sqrt{ \frac{2k}{\kappa} }\sqrt{ \left( \frac{N}{1.202} \right)^{1/3} \frac{hf}{k} } \\
		 & =\sqrt{ \frac{2hf}{\kappa}\left( \frac{N}{1.202} \right)^{1/3} }
		\end{aligned}
		$$
		Which we can put back into our equation $E_{SHO}=kT_{c}$:
		$$
		\begin{aligned}
		\frac{1}{2}\kappa a^{2} & =\frac{1}{2}\kappa \frac{2hf}{\kappa}\left( \frac{N}{1.202} \right)^{1/3} \\
		 & =hf \left( \frac{N}{1.202} \right)^{1/3} \\
		 & =E_{SHO}
		\end{aligned}
		$$
4. 
   1. The entropy per photon is the total entropy divided by the number of photons:
		$$
		\begin{aligned}
		 & N(T)=\frac{2.404}{\pi^{2}}V\left( \frac{k_{B}T}{\hbar c} \right)^{3} \\
		 & S(T)=\frac{32\pi^{5}}{45}V\left( \frac{kT}{hc} \right)^{3}k
		\end{aligned}
		$$
		Therefore:
		$$
		\frac{S(T)}{N(T)}=\frac{\frac{32\pi^{5}}{45}V\left( \frac{kT}{hc} \right)^{3}k}{\frac{2.404}{\pi^{2}}V\left( \frac{k_{B}T}{\hbar c} \right)^{3}}
		$$