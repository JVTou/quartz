1.  
	   1.  We know that the z-component of the magnetic moment of an atom is:
        $$
        \mu_{z}=g\mu_{0}m_{j}
        $$
        With $m_{j}=-J, -J+1, -J+2 \cdots J-1,J$
        We also know that the average value of a our magnetic moment with a value $\mu_{z}$ for quantum number $J$ can be written as:
        $$
        \overline{\mu_{z}}=\frac{1}{Z}\sum_{j}g\mu_{0}m_{j}e^{ -\beta g\mu_{0}m_{j} }
        $$
        Let's try and express this with the partition function $Z$. The partition function $Z$ is defined as the sum of all the Boltzmann factors, or each state's probabilities, of a system. Here, the partition function is:
        $$
        Z=\sum_{s}e^{ -\beta E(s) }
        $$
        With $E=-g\mu_{0}BJ_{z}=-g\mu_{0}Bm_{j}$ we can develop the partition function so:
        $$
        \begin{aligned}
        Z & =\sum_{j}e^{ -\beta(-g\mu_{0}Bm_{j}) } \\
         & =\sum_{j}e^{ \beta g\mu_{0}Bm_{j} } \\
        \ln Z & =\sum_{j}\beta g\mu_{0}Bm_{j} \\
        \frac{ \partial \ln Z }{ \partial B } & = \sum_{j}\beta g\mu_{0}m_{j} \\
        \frac{1}{\beta}\frac{ \partial \ln Z }{ \partial B }  & = \sum_{j} g\mu_{0}m_{j} \\
         & =\frac{1}{\sum_{j} e^{ -\beta g\mu_{0}m_{j} }}\sum_{j} g\mu_{0}m_{j}\sum_{j} e^{ -\beta g\mu_{0}m_{j} } \\
         & =\frac{1}{Z}\sum_{j}g\mu_{0}m_{j}e^{ -\beta g\mu_{0}m_{j} } \\
        \frac{1}{\beta}\frac{ \partial \ln Z }{ \partial B } & =\overline{\mu_{z}}
        \end{aligned}
        $$
    2.  $\sinh(x)=\frac{e^{ x }-e^{ -x }}{2}$
        $$
        \begin{aligned}
        Z & =\sum_{j}e^{ \beta g\mu_{0}Bm_{j} } \\
         & =e^{ \beta g\mu_{0}B(-J) }+e^{ \beta g\mu_{0}B(-J+1) }+e^{ \beta g\mu_{0}B(-J+2) }+\cdots+e^{ \beta g\mu_{0}B(J-1) }+e^{ \beta g\mu_{0}B(J) } \\
         & =e^{ \beta g\mu_{0}B(-J) }+e^{ \beta g\mu_{0}B(-J) }e^{ \beta g\mu_{0}B }+\cdots+e^{ \beta g\mu_{0}B(J) }e^{ -\beta g\mu_{0}B }+e^{ \beta g\mu_{0}B(J) } \\
         & =\dots \\
         & =\sum_{j=0}^{2J+1}\left(e^{ \beta g\mu_{0}B }\right)^{m_{j}} \\
         & =\frac{1-\left(e^{ \beta g\mu_{0}B }\right)^{2J+1}}{1-\left(e^{ \beta g\mu_{0}B }\right)} \\
        \end{aligned}
        $$

        Factoring by $e^{ (J+1/2)\beta g\mu_{0}B }$ gives:
        $$
        \begin{aligned}
         & =\frac{e^{ -(1/2)(\beta g\mu_{0}B)}e^{ (J+1/2)\beta g\mu_{0}B }(e^{ -(J+1/2)\beta g\mu_{0}B }-e^{ 2\beta g\mu_{0}B })}{e^{ -1/2(\beta g\mu_{0}B) }(1-e^{ \beta g\mu_{0}B })} \\
         & =\frac{e^{ J\beta g\mu_{0}B }(e^{ -(J+1/2)\beta\mu_{0}B }-e^{ 2\beta g\mu_{0}B })}{e^{ -(1/2)\beta g\mu_{0}B }-e^{ (1/2)\beta g\mu_{0}B }} \\
         & =
        \end{aligned}
        $$
    3.  The total magnetization of a system of $N$ atoms is typically $M=N\overline{\mu_{z}}$
        We previously derived $\overline{\mu_{z}}$:
        $$
         \overline{\mu_{z}}=\frac{1}{\beta}\frac{ \partial \ln Z }{ \partial B }
        $$
        we also found found
        $$
        Z=\frac{\sinh\left[ \left( J+\frac{1}{2})\beta g\mu_{0}B \right) \right]}{\sinh\left[ \frac{1}{2}\beta g\mu_{0}B \right]}
        $$
        Let's start calculating $\overline{\mu_{z}}$:
        $$
        \begin{aligned}
        \ln Z & =\ln\frac{\sinh\left[ \left( J+\frac{1}{2})\beta g\mu_{0}B \right) \right]}{\sinh\left[ \frac{1}{2}\beta g\mu_{0}B \right]} \\
         & =\ln\sinh\left[ \left( J+\frac{1}{2})\beta g\mu_{0}B \right) \right]-\ln\sinh\left[ \frac{1}{2}\beta g\mu_{0}B \right] \\
        \end{aligned}
        $$
        Now taking the partial derivative with respect to $B$:
        $$
        \begin{aligned}
        \frac{ \partial \ln Z }{ \partial B } = & \frac{\left( J+\frac{1}{2} \right)\beta g\mu_{0}\cosh\left( \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right)}{\sinh\left( \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right)}-\frac{\left( \frac{1}{2} \right)\beta g\mu_{0}\cosh\left( \left( \frac{1}{2} \right)\beta g\mu_{0}B \right)}{\sinh\left( \left( \frac{1}{2} \right)\beta g\mu_{0}B \right)} \\
         & =\left( J+\frac{1}{2} \right)\beta g\mu_{0}\coth\left( \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right)-\left( \frac{1}{2} \right)\beta g\mu_{0}\coth\left( \left( \frac{1}{2} \right)\beta g\mu_{0}B \right)
        \end{aligned}
        $$
        Therefore, we can write $\overline{\mu_{z}}$ as:
        $$
        \begin{aligned}
        \overline{\mu_{z}} & =\left( J+\frac{1}{2} \right) g\mu_{0}\coth\left( \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right)-\left( \frac{1}{2} \right) g\mu_{0}\coth\left( \left( \frac{1}{2} \right)\beta g\mu_{0}B \right) \\
         & =g\mu_{0}J\left[ \frac{1}{J}\left[ \left( J+\frac{1}{2} \right)\coth\left[ \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right]-\frac{1}{2}\coth\left[ \frac{1}{2}\beta g\mu_{0}B \right] \right] \right] \\
         & =g\mu_{0}JB_{j}(\beta g\mu_{0}B)
        \end{aligned}
        $$
        And $M$ is therefore:
        $$
        M=Ng\mu_{0}JB_{j}(\beta g\mu_{0}B)
        $$
    4. 
	     ![[desmos-graph.png]]
        Red is $J=\frac{1}{2}$, blue is $J=1$ and orange is $J=\frac{7}{2}$.
    5.  We know that $\beta=\frac{1}{k_{B}T}$, so as $T\to0$, $\beta\to \infty$:
        $$
        \begin{aligned}
        \lim_{ \beta \to \infty } M & =\lim_{ \beta \to \infty } Ng\mu_{0}JB_{j}(\beta g\mu_{0}B) \\
         & =\lim_{ \beta \to \infty } Ng\mu_{0}J\left[ \frac{1}{J}\left[ \left( J+\frac{1}{2} \right)\coth\left[ \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right]-\frac{1}{2}\coth\left[ \frac{1}{2}\beta g\mu_{0}B \right] \right] \right]
        \end{aligned}
        $$
        We know that $\lim_{ \beta \to \infty }\coth\beta=1$, therefore:
        $$
        \lim_{ \beta \to \infty } M=\lim_{ \beta \to \infty } Ng\mu_{0}J\left[ \frac{1}{J}\left[ \left( J+\frac{1}{2} \right)-\frac{1}{2} \right] \right]=Ng\mu_{0}J
        $$
    6.  At high temperatures, $\beta\to0$, we need to determine an approximation for $\coth(\beta)$
		$$
		\coth(\beta)=\frac{e^{ \beta }+e^{ -\beta }}{e^{ \beta }-e^{ -\beta }}
	
		$$
		For $\beta\to0$:
		Taylor expansion of $e^{ \beta }=1+\beta+\frac{\beta^{2}}{2}+\frac{\beta^{3}}{3!}+\dots$
		Taylor expansion of $e^{ -\beta }=1-\beta+\frac{\beta^{2}}{2}-\frac{\beta^{3}}{3!}+\dots$
		$$
		\coth\beta \approx\frac{1+\beta+\frac{\beta^{2}}{2}+\frac{\beta^{3}}{3!}+1-\beta+\frac{\beta^{2}}{2}-\frac{\beta^{3}}{3!}}{1+\beta+\frac{\beta^{2}}{2}+\frac{\beta^{3}}{3!}-1+\beta-\frac{\beta^{2}}{2}+\frac{\beta^{3}}{3!}}\approx \frac{1+\frac{\beta^{2}}{2}}{\beta+\frac{\beta^{3}}{3}}\approx \frac{1}{\beta}\frac{1+\frac{\beta^{2}}{2}}{1+\frac{\beta^{2}}{3}}
		$$
		Another common expansion is $\frac{1}{1+x}\approx1-x+x^{2}+\dots$:
		$$
		\coth\beta \approx \frac{1}{\beta}\left( 1-\frac{\beta^{2}}{3} \right)\left( 1+\frac{\beta^{2}}{2} \right)= \frac{1}{\beta}\left( 1+\frac{\beta^{2}}{2}-\frac{\beta^{2}}{3}-\frac{\beta^{4}}{3!} \right)=\frac{1}{\beta}+\frac{\beta}{3}-\frac{\beta^{4}}{3!}\approx \frac{1}{\beta}+\frac{\beta}{3}
		$$
		So, at high temperatures, we can expect the magnetization to be approximately:
        $$
        \begin{aligned}
        M & =\lim_{ \beta \to 0 } Ng\mu_{0}J\left[ \frac{1}{J}\left[ \left( J+\frac{1}{2} \right)\coth\left[ \left( J+\frac{1}{2} \right)\beta g\mu_{0}B \right]-\frac{1}{2}\coth\left[ \frac{1}{2}\beta g\mu_{0}B \right] \right] \right] \\
        & =Ng\mu_{0}J \\
		 & \left[ \frac{1}{J}\left[ \left( J+\frac{1}{2} \right) \left( \frac{1}{\left( J+\frac{1}{2} \right)\beta g\mu_{0} B}+\frac{\left( J+\frac{1}{2} \right)\beta g\mu_{0}B}{3} \right) -\frac{1}{2}\left[ \frac{1}{\frac{1}{2}\beta g\mu_{0}B}+\frac{\frac{1}{2}\beta g\mu_{0}B}{3} \right] \right] \right] \\
		 & =Ng\mu_{0}J\left[ \frac{1}{J}\left[ \frac{J+\frac{1}{2}}{\left( J+\frac{1}{2} \right)\beta g\mu_{0}B}+\frac{\left( J+\frac{1}{2} \right)^{2}\beta g\mu_{0}B}{3} -\frac{1}{2}\left[ \frac{2}{\beta g\mu_{0}B}+\frac{\beta g\mu_{0}B}{6} \right]\right] \right] \\
		 & =Ng\mu_{0}J\left[ \frac{1}{J}\left[ \frac{1}{\beta g\mu_{0}B}+\frac{\left( J+\frac{1}{2} \right)^{2}\beta g\mu_{0}B}{3}-\frac{1}{\beta g\mu_{0}B}-\frac{\beta g\mu_{0}B}{12} \right] \right] \\
		 & =Ng\mu_{0}J\left[ \frac{1}{J}\left[ \frac{\left( J+\frac{1}{2} \right)^{2}\beta g\mu_{0}B}{3}-\frac{\beta g\mu_{0}B}{12} \right] \right] \\
		 & =Ng\mu_{0}J\left[ \frac{\beta g\mu_{0}B}{J}\left[ \left( J^{2}+J+\frac{1}{4} \right) \frac{1}{3}-\frac{1}{12} \right] \right] \\
		 & =Ng\mu_{0}J \frac{\beta g\mu_{0}B}{J}[J^{2}+J] \frac{1}{3} \\
		 & =Ng\mu_{0}J\frac{\beta g\mu_{0}B}{3}(J+1)
		\end{aligned}
		$$
		This implies that the magnetization $M$ is proportional to $\frac{B}{T}$, with the constant of proportionality $C=\frac{1}{3}Ng^{2}\mu_{0}^{2}J(J+1) \frac{1}{k}$
	1. When $J=\frac{1}{2}$, we can calculate the magnetization to be:
		$$
		\begin{aligned}
		M & =Ng\mu_{0} \frac{1}{2}\left[2\left[ \left( 1 \right)\coth\left[ \left( 1 \right)\beta g\mu_{0}B \right]-\frac{1}{2}\coth\left[ \frac{1}{2}\beta g\mu_{0}B \right] \right] \right] \\ \\
		\text{Let } \beta g\mu_{0}B=\kappa \\
		 & =Ng\mu_{0}\left[ \frac{e^{ \kappa }+e^{ -\kappa }}{e^{ \kappa }-e^{ -\kappa }}-\frac{1}{2} \frac{e^{ \kappa/2 }+e^{ -\kappa/2 }}{e^{ \kappa/2 }-e^{ -\kappa/2 }} \right] \\
		 & =Ng\mu_{0}\left[\frac{e^{ \kappa }+e^{ -\kappa }}{e^{ \kappa }-e^{ -\kappa }}-\frac{1}{2}\frac{\left(e^{ \kappa/2 }+e^{ -\kappa/2 }\right)\left(e^{ \kappa/2 }+e^{ -\kappa/2 }\right)}{e^{ \kappa }-e^{ -\kappa }}\right] \\
		 & =Ng\mu_{0}\left[\frac{2\left(e^{ \kappa }+e^{ -\kappa }\right)-e^{ \kappa }-2-e^{ -\kappa }}{2\left(e^{ \kappa }-e^{ -\kappa }\right)}\right] \\
		 & =Ng\mu_{0}\left[ \frac{e^{ \kappa }+e^{ -\kappa }-2}{2(e^{ \kappa/2 }+e^{ \kappa/2 })(e^{ \kappa/2 }-e^{ -\kappa/2 })} \right] \\
		 & =Ng\mu_{0}\left[ \frac{(e^{ \kappa/2 }-e^{ -\kappa/2 })^{2}}{2(e^{ \kappa/2 }+e^{ \kappa/2 })(e^{ \kappa/2 }-e^{ -\kappa/2 })} \right] \\
		 & =Ng\mu_{0}\left[ \frac{(e^{ \kappa/2 }-e^{ -\kappa/2 })}{2(e^{ \kappa/2 }+e^{ \kappa/2 })} \right] \\
		 & =Ng\mu_{0} \frac{1}{2}\tanh\left( \frac{\beta g\mu_{0}B}{2} \right)
		\end{aligned}
		$$
		Which is what we expected for an ideal 2 state paramagnet.
2. 
	1. Maxwell distribution of speeds of molecules in an ideal gas:
		$$
		D(v)=\left( \frac{m}{2\pi kT} \right)^{3/2}4\pi v^{2}e^{ -mv^{2}/2kT }
		$$
		Root mean square of speeds is the root of the average speed squared:
		$$
		v_{rms}=\sqrt{ \bar{v}^{2} }
		$$
		And the average speed is the sum of all the molecules' speeds over the number of molecules:
		$$
		\begin{aligned}
		\bar{v}^{2} & =\sum_{\text{all }v}v^{2}D(v)dv \\
		 & =\int_{0}^{\infty} v^{2}D(v) \, dv  \\
		 & =\int_{0}^{\infty}v^{2}\left( \frac{m}{2\pi kT} \right)^{3/2}4\pi v^{2}e^{ -mv^{2}/2kT }dv \\
		 & \dots \\
		 & =\frac{3k_{b}T}{m}
		\end{aligned}
		$$
		Therefore $v_{rms}=\sqrt{ \frac{3k_{b}T}{m} }$ as we know from the average kinetic energy.
	2. Probability($v>250\pu{ m/s }$):
		$$
		\begin{aligned}
		= & 4\pi\left( \frac{m}{2\pi kT} \right)^{3/2}\int_{\pu{ 250m/s }}^{\infty} v^{2}e^{ -mv^{2}/2kT } \, dv  \\
		\end{aligned}
		$$
		At room temperature, oxygen has a $v_{max}=\sqrt{ \frac{2kT}{m} }=\pu{ 390.2m/s }$, and so we can write $x=v\sqrt{ \frac{m}{2kT} }=\frac{v}{v_{max}}$, and the integral becomes:
		$$
		=\frac{4}{\sqrt{ \pi }}\int_{\frac{v}{v_{max}}}^{\infty}x^{2}e^{ -x^{2} }  \, dx 
		$$
		Which, calculated with a computer, gives a probability of 0.84.
3. 
	1. We know the expression for chemical potential $\mu=\left( \frac{ \partial F }{ \partial N } \right)_{T,V}$
		With $F=-kT\ln Z=-kTN[\ln V+\ln Z_{int}-\ln N-\ln v_{Q}+1]$:
		$$
		\begin{aligned}
		\mu & =\frac{ \partial  }{ \partial N }_{T,V}\left(-kTN[\ln V+\ln Z_{int}-\ln N-1-\ln v_{Q}+1]\right)  \\
		 & =-kT\ln V-kt\ln Z_{int}+kt\ln N+kT\ln v_{Q} \\
		 & =-kT(\ln V+\ln Z_{int}-\ln N-\ln v_{Q}) \\
		 & =-kT\left( \ln \frac{VZ_{int}}{Nv_{Q}} \right)
		\end{aligned}
		$$
		If there are no internal contributions, $F=-NkT[\ln V-\ln N-\ln v_{Q}+1]$, which gives a chemical potential of:
		$$
		\begin{aligned}
		\mu & =-kT\left( \frac{ \partial  }{ \partial N }  \right)_{T,V}(N\ln V-N\ln N-N\ln v_{Q}+N) \\
		 & =-kT[\ln V-\ln N-1-\ln v_{Q}+1] \\
		 & =-kT(\ln V-\ln N-\ln v_{Q}) \\
		 & =-kT\ln\left( \frac{V}{Nv_{Q}} \right) \\
		v_{Q}=\left( \frac{h}{\sqrt{ 2\pi mkT }} \right)^{3} \\
		 & =-kT\ln\left[ \frac{V}{N} \frac{1}{\left( \frac{h}{\sqrt{ 2\pi mkT }} \right)^{3}} \right] \\
		 & =-kT\ln\left[ \frac{V}{N}\left( \frac{2\pi mkT}{h^{2}} \right)^{3/2} \right]
		\end{aligned}
		$$