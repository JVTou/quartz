
# Introduction

This laboratory investigates transient voltage and current relationships for single time-constant circuits involving capacitors and inductors. Such circuits when excited by step voltages exhibit exponential responses that will be experimentally observed and analyzed to verify relevant circuit theory. The objective of this experiment is to analyze the transient behavior of RC and RL circuits, verifying theoretical time constants by measuring voltage responses over time.

# Part 1: Single Time Constant Resistor-Capacitor Integrator

When excited by a step change in voltage the capacitor either charges or discharges at a rate proportional to $e^{ -t/\tau }$ , where $\tau=RC$ is generally known as the time-constant.

We are looking to measure $\tau$ by using the following circuit, plotting a voltage vs. time plot across the capacitor with the lab oscilloscope.

![[Pasted image 20250221133036.png]]

## Theoretical Values

We measure our capacitor to have a capacitance of $C=96.9\text{ nF}$.

We use a resistor of $R=10\text{ kOhm}$.

Therefore, our time constant should be $\tau=RC=9.69=0.969\text{ ms}$

Our theoretical voltage for each multiple of $\tau$ is below:

$$
\begin{aligned}
&V_{C}(t)=V_{C}(\infty)+[V_{C}(0)-V_{C}(\infty)]e^{ -t/\tau } \\
&V_{C}(\tau)\approx6.32\text{ V} \\
&V_{C}(2\tau)\approx8.65\text{ V} \\
&V_{C}(3\tau)\approx9.50\text{ V} \\
&V_{C}(4\tau)\approx9.82\text{ V} \\
&V_{C}(5\tau)\approx9.93\text{ V}
\end{aligned}
$$

## Measured Data

We measure the following voltages for each multiple of $\tau$:

$$
\begin{aligned}
&V_{C}(\tau)\approx5.56\text{ V} \\
&V_{C}(2\tau)\approx8.06\text{ V} \\
&V_{C}(3\tau)\approx8.94\text{ V} \\
&V_{C}(4\tau)\approx9.44\text{ V} \\
&V_{C}(5\tau)\approx 9.87\text{ V}
\end{aligned}
$$

We plot our theoretical voltage in blue, and our measured voltages in green:

![[desmos-graph (2).png|550]]

Our values fall within the exponential pattern expected from a square waveform generated through our circuit.

The deviations in measured values could be attributed to:

- Component tolerances (resistor and capacitor values slightly different from nominal ratings).
- Measurement inaccuracies due to oscilloscope resolution.
- External noise affecting the circuit response.

The measured voltage values for the RC integrator circuit closely followed the expected exponential charging behavior. While there were slight deviations from the theoretical predictions, the overall trend confirmed the time-constant relationship.

# Part 2: Single Time Constant Resistor-Capacitor Differentiator

Since we are working with a differentiator, we expect it to differentiate the signal passing through the circuit $f(x)=10+(0-10)e^{ -x }$. Therefore our theoretical values will be:

$$
V_{R}(t)=\frac{d}{dx}f(x)
$$

## Theoretical Values

Our theoretical voltage for each multiple of $\tau$ is below:

$$
\begin{aligned}

&V_{R}(\tau)\approx 3.79\text{ V} \\

&V_{R}(2\tau)\approx 1.44\text{ V} \\

&V_{R}(3\tau)\approx 0.55\text{ V} \\

&V_{R}(4\tau)\approx 0.21\text{ V} \\

&V_{R}(5\tau)\approx 0.08\text{ V}

\end{aligned}
$$

## Recorded Data

We plot our recorded voltage in red, and our  our measured voltages in green:

![[desmos-graph (3).png|550]]

Doing an exponential regression on our recorded values, we find our measured voltages have a coefficient of determination $R^{2}=0.999$, and closely resemble our expected graph, up to a proportionality constant.

The RC differentiator circuit produced a voltage waveform that matched the theoretical derivative of the input signal. Our measured values demonstrated a strong exponential regression fit, verifying the circuit's ability to differentiate the input step function.

# Part 3: Single Time Constant Resistor-Inductor Circuit

Constructing a similar circuit with an inductor replacing the capacitor, we determine if it has similar properties to an RC integrator (time constant and generally similar waveforms). Since we cannot produce a step in our current, we drive our circuit with a step voltage from the lab’s signal generator, and expect our current to follow the integral of the voltage.

We are looking to measure $\tau$ by using the following circuit, plotting a voltage vs. time plot across the inductor with the lab oscilloscope:

![[Pasted image 20250304174445.png]]

## Theoretical Values

$$
\begin{aligned}
i_{L}(t)=i_{L}(\infty)+[i_{L}(0)-i_{L}(\infty)]e^{ -t/\tau } \\
\frac{di_{L}(t)}{dt}=-\frac{1}{\tau}[i_{L}(0)-i_{L}​(\infty)]e^{ t/\tau }
\end{aligned}
$$

$$
\begin{aligned}
v_{L}(t)=L \frac{di_{L}(t)}{dt} \\
v_{L}(t)=-R[i_{L}​(0)-i_{L}​(\infty)]e^{ -t/\tau } \\
\end{aligned}
$$

We know that our inductor to have an inductance of $L=10\text{ micro H}$.

We use a resistor of $R=0.435\text{ Ohm}$.

Therefore, our time constant should be $\tau=\frac{L}{R}=2.3\text{ microseconds}$. However, since our oscilloscope measures only voltage, we are unable to verify this constant. Instead, we will determine if the voltage waveform across the inductor follows waveforms similar to the capacitors, and determine its time constant.

## Measured Values

Driving our circuit with a $10\text{ Vpp}$ square voltage signal, at a frequency of $1\text{kHz}$, we calculate our time constants at different times in the decay. We calculate $\tau$ at its specified percentages of the peak voltage values [^1], knowing our measured peak voltage is $11.46\text{ V}$:

$$
\begin{aligned}

&\tau_{61\%}\approx 38.4 \text{ nanoseconds} \\
&2\tau_{37\%}\approx 150 \text{ nanoseconds} \\
&3\tau_{14\%}\approx 322 \text{ nanoseconds} \\
&4\tau_{5\%}\approx  573\text{ nanoseconds} \\
&5\tau_{2\%}\approx  739\text{ nanoseconds} \\

\end{aligned}
$$

We then plot voltage vs. time constants across our inductor and compare it to our theoretical voltage equation. We obtain our voltage values at each measured $\tau$ value above:

![[desmos-graph (4).png|550]]

$$
\begin{align}

&V_{L}(\tau)\approx 3.4 \text{ V} \\

&V_{L}(2\tau)\approx 6.31 \text{ V} \\

&V_{L}(3\tau)\approx  9.12\text{ V} \\

&V_{L}(4\tau)\approx 10.56\text{ V} \\

&V_{L}(5\tau)\approx 10.8\text{ V}

\end{align}
$$

We observe a correlation between our measured voltage and an exponentially increasing function, with a coefficient of determination $R^{2}=0.8307$. This indicates a strong possibility that the voltage in an RL circuit exponentially decays after a square pulse, proportional to a time constant $\tau$.

The RL circuit exhibited exponential behavior in response to a step voltage, similar to the RC integrator. The general trend of the voltage curve supported the theoretical model of inductor voltage decay.

# Conclusion

This experiment successfully demonstrated the transient behavior of single time-constant circuits, confirming theoretical predictions of exponential responses in RC and RL circuits. Despite minor measurement deviations, the observed results aligned well with expected time-constant relationships. These findings reinforce the fundamental principles governing capacitive and inductive circuit equations in transient conditions.

[^1]: Textbook Chapter 5 pg. 257
