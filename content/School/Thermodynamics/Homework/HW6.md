1. 
	1. Clausius-Clapeyron equation:
		$$\begin{aligned}
		\frac{dP}{dT}&=\frac{L}{T\Delta V}\\
		&=\frac{L}{T(V_g-V_l)}
		\end{aligned}$$
		We know $V_g>>V_l$, so we drop $V_l$. Knowing this is an ideal gas, we write:
		$$\begin{aligned}
		PV_g&=nRT\\
		V_g&=\frac{nRT}{P}
		\end{aligned}$$
		 And use this value for $V_g$ in the Clausius-Clapeyron equation:
		$$
		\begin{aligned}
		\frac{dP}{dT}&=\frac{L}{T\frac{nRT}{P}}\\
		&=\frac{LP}{nRT^2}
		\end{aligned}
		$$
		
		Treating the above as a differential equation, we use separation of variables to solve for P:
		$$\begin{aligned}
		\frac{1}{P}dP&=\frac{L}{nRT^2}dT\\
		\int\frac{1}{P}dP&=\int\frac{L}{nRT^2}dT\\
		ln(P)&=-\frac{L}{nRT}+C\\
		P=C\cdot e^{-\frac{L}{nRT}}
		\end{aligned}
		$$
	2. 
	3. 
2. Van der Waals equation for a non-ideal gas:
	$$
	\left( P+\frac{aN^{2}}{V^{2}} \right)(V-Nb)=NkT
	$$
	1. The Van der Waals equation expressed above, solved for P:
		$$
		P=\frac{NKT}{V-Nb}-\frac{aN^{2}}{V^{2}}
		$$
		Taking $\frac{ \partial P }{ \partial V } _{T}=0$, we get:
		$$
		\left( \frac{ \partial P }{ \partial V }  \right)_{T_{c}}=-\frac{NkT_{c}}{(V_{c}-Nb)^{2}}+\frac{3aN^{2}}{V_{c}^{3}}=0
		$$
		Taking $\left( \frac{ \partial^{2} P }{ \partial V^{2} } \right)_{T_{c}}$, we get:
		$$
		\left( \frac{ \partial^{2} P }{ \partial V^{2} }  \right)_{T_{c}}=\frac{2NkT_{c}}{(V_{c}-Nb)^{3}}-\frac{9aN^{2}}{V_{c}^{4}}=0
		$$
		We can use the above to express $a$ in terms of $b$:
		$$
		a=\frac{NkT_{c}}{(V_{c}-Nb)^{2}} \frac{V_{c}^{3}}{3N^{2}}
		$$
		Using this expression for $a$, we find a value for $b$ in terms of $T_{c}$ and $V_{c}$:
		$$
		\begin{aligned}
		\frac{2NkT_{c}}{(V_{c}-Nb)^{3}}-\frac{9\frac{NkT_{c}}{(V_{c}-Nb)^{2}}\frac{V_{c}^{3}}{3N^{2}}N^{2}}{V_{c}^{4}}=0 \\
		\frac{2NkT_{c}}{(V_{c}-Nb)^{3}}-\frac{3NkT_{c}}{V_{c}(V_{c}-Nb)^{2}}=0 \\
		\frac{2V_{c}NkT_{c}-3NkT_{c}(V_{c}-Nb)}{V_{c}(V_{c}-Nb)^{3}}=0 \\
		\frac{2V_{c}NkT_{c}-3NkV_{c}T_{c}-3NkT_{c}Nb}{V_{c}(V_{c}-Nb)^{3}}=0 \\
		\frac{-NkV_{c}T_{c}-3NkT_{c}Nb}{V_{c}(V_{c}-Nb)^{3}}=0 \\
		-NkV_{c}T_{c}-3NkT_{c}Nb=0 \\
		b=-\frac{NkV_{c}T_{c}}{3N^{2}kT_{c}} \\
		b=-\frac{V_{c}}{3N}
		\end{aligned}
		$$
		With this value of $b$, we find a value for $a$ in terms of $T_{c}$ and $V_{c}$:
		$$
		\begin{aligned}
		a=\frac{NkT_{c}}{\left( V_{c}-N\left( -\frac{V_{c}}{3N} \right) \right)^{2}} \frac{V_{c}^{3}}{3N^{2}} \\
		a=\frac{NkT_{c}}{\left( V_{c}+\frac{V_{c}}{3} \right)^{2}} \frac{V_{c}^{3}}{3N^{2}} \\
		a=\frac{NkT_{c}}{\frac{16}{9}V_{c}^{2}} \frac{V_{c}^{3}}{3N^{2}} \\
		a=\frac{3kT_{c}V_{c}}{16N}
		\end{aligned}
		$$
	2. Finding an expression for $P_{c}$:
		$$
		\begin{aligned}
		P_{c}=\frac{NkT_{c}}{V_{c}-Nb}-\frac{aN^{2}}{V_{c}^{2}} \\
		P_{c}=\frac{NkT_{c}}{V_{c}-N\left( -\frac{V_{c}}{3N} \right)}-\frac{\left( \frac{3kT_{c}V_{c}}{16N} \right)N^{2}}{V_{c}^{2}} \\
		P_{c}=\frac{NkT_{c}}{V_{c}+N\frac{V_{c}}{3}}-\frac{3NkT_{c}}{16V_{c}} \\
		P_{c}=\frac{NkT_{c}}{V_{c}}\left( \frac{1}{1+\frac{N}{3}}-\frac{3}{16} \right) \\
		\end{aligned}
		$$
	3. Rewriting the Van der Waals equation with our new values:
		- $V_{c}=-3bN$
		- $T_{c}=\frac{16aN}{3kV_{c}}=\frac{16aN}{-9kbN}=-\frac{16a}{9kb}$
		- $P_{c}=\frac{NkT_{c}}{V_{c}}\left( \frac{3(13-N)}{16(N+3)} \right)=\frac{Nk(-\frac{16a}{9kb})}{-3bN}\left( \frac{3(13-N)}{16(N+3)} \right)=\frac{8a}{9b^{2}}\left( \frac{3(13-N)}{16(N+3)} \right)$
		and
		- $P=P'P_{c}$
		- $T=T'T_{c}$
		- $V=V'V_{c}$

$$
\begin{aligned}
\left( P+\frac{aN^{2}}{V^{2}} \right)(V-Nb)=NkT \\
\left( P'P_{c}+\frac{aN^{2}}{(V'V_{c})^{2}} \right)(V'V_{c}-Nb)=NkT'T_{c} \\
\left( P'\frac{8a}{9b^{2}}\left( \frac{3(13-N)}{16(N+3)} \right)+\frac{aN^{2}}{(V'(-3bN))^{2}} \right)(V'(-3bN)-Nb)=NkT'\left(-\frac{16a}{9kb}\right) \\
\left( P'\frac{8}{9b^{2}}\left( \frac{3(13-N)}{16(N+3)} \right)+\frac{N^{2}}{(V'^{2}9b^{2}N^{2})} \right)(3V'+1)=T'\left(\frac{16}{9}\right) \\
\left( P'\frac{1}{3b^{2}}\left( \frac{13-N}{2(N+3)} \right)+\frac{1}{V'^{2}9b^{2}} \right)(3V'+1)=T'\left(\frac{16}{9}\right)
\end{aligned}
$$