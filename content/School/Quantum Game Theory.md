---
theme: serif
date created: Monday, May 19th 2025, 10:39:09 pm
date modified: Thursday, July 24th 2025, 6:35:51 pm
---

## Quantum Games

**Junipero Verbeke**
##### University of California, Santa Cruz

---
### The Dawn of Game Theory

* **What is Game Theory?**
    * Mathematical framework for strategic interactions.
    * Players ($N$), Strategies ($S_i$), Payoff functions ($\pi_i$ or $E_i$).
    * Assumption: Rational players maximizing their own payoff.
* How do quantum mechanics impact strategies compared to classical decision-making?
* Are quantum strategies more profitable? We'll look at the example of the prisoner's dilemma

---

### Classical Game Theory

* **Hypothesis:** Quantum strategies offer advantages, potentially solving classically insoluble games and providing at least equal payoff.
---

#### Key Classical Concepts

|               | Cooperate          | Defect                |
| ------------- | ---------------------- | ------------------------- |
| Cooperate | (3, 3) -Pareto Optimal | (0, 5)                    |
| Defect    | (5, 0)                 | (1, 1) - Nash Equilibrium |

* **The Dilemma:**
    * NE is not PO (e.g., Prisoner's Dilemma) -> individual rationality leads to collective suboptimal outcome.

---

### Introducing Quantum Mechanics to Games - Why Quantize?

* **Classical Limitations:** Assumes strategies from well-defined sets, classical probability.
* **Quantum Potential:**
    * Access to quantum resources (superposition, entanglement).
    * Fundamental alteration of the strategic landscape.
    * Potential for advantages unobtainable classically.

---

#### Quantum Representation - The Building Blocks

* **Qubits:**
    * Map classical strategies (Cooperate/Defect) to basis states $\ket{0}$ and $\ket{1}$.
* **Superposition:**
    * Qubit state: $\alpha\ket{0} + \beta\ket{1}$ (where $|\alpha|^2 + |\beta|^2 = 1$).
    * Allows players to consider multiple strategies simultaneously.

---
![[Pasted image 20250602212522.png]]
---
### Quantum Advantage in Action

* **Quantum Prisoner's Dilemma:**
    * Initial entangled qubits
    * Quantum strategy: Unitary operation $\hat{U} = \begin{pmatrix} \cos(\theta/2) & i\sin(\theta/2) \\ i\sin(\theta/2) & \cos(\theta/2) \end{pmatrix}$
        * $\theta = 0$: Cooperation (C)
        * $\theta = \pi/2$: Defection (D)
    * With sufficient entanglement, a new QNE can emerge where both players effectively "cooperate" (e.g., applying $\hat{Q}$ with $\theta=0$). This resolves the classical dilemma: NE is PO.

---

### Quantifying the Quantum Advantage

* **General Principle:** The expected payoff for a player using an optimal quantum strategy is always greater than or equal to the payoff with an optimal classical (mixed) strategy.

* **Reason:** Quantum mechanics expands the available strategy space without removing any classical options.

---

#### Conclusion

* **New Tools:** Superposition and entanglement create novel strategies and equilibrium structures.
* **Resolving Dilemmas:** Quantum games can solve classical paradoxes like the Prisoner's Dilemma, leading to mutually beneficial outcomes.
* **Superior Outcomes:** Quantum strategies provide tools for outcomes unattainable classically, often resulting in improved, sometimes Pareto optimal, payoffs.
