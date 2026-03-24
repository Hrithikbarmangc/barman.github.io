---
title: "Confinement-Induced Delay in Active Brownian Motion"
excerpt: "Emergence of temporal delay and correlations in confined chiral active particle dynamics."
collection: portfolio
mathjax: true
---

### Overview

We investigate how spatial confinement modifies the dynamics of chiral active Brownian particles, leading to the emergence of **temporal delay** and **non-trivial correlations**. 

Our key finding is that even in overdamped dynamics, confinement induces a **finite lag between propulsion and spatial response**, purely due to the interplay of **chirality and trapping**.

---

### Model and Method

We consider a chiral active Brownian particle confined in a harmonic potential $U(x,y) = \frac{1}{2}k(x^2 + y^2)$. The overdamped dynamics are governed by:

$$\dot{x}(t) = v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t)$$

$$\dot{y}(t) = v_0 \sin\phi(t) - ky(t) + \sqrt{2D_t}\,\xi_y(t)$$

$$\dot{\phi}(t) = \Omega + \sqrt{2D_r}\,\eta(t)$$

---

### Mean Position Dynamics

The ensemble-averaged position evolution, derived from the formal solution of the Langevin equations, is given by:

$$
\begin{aligned}
\langle \mathbf{r}(t)\rangle 
&= \mathbf{r}(0) e^{-\mu k t} \\
&\quad + \beta e^{-\mu k t} \Bigg[
e^{\alpha t} 
\begin{pmatrix} 
\alpha\cos\psi(t) + \Omega\sin\psi(t) \\ 
\alpha\sin\psi(t) - \Omega\cos\psi(t) 
\end{pmatrix}
-
\begin{pmatrix} 
\alpha\cos\psi(0) + \Omega\sin\psi(0) \\ 
\alpha\sin\psi(0) - \Omega\cos\psi(0) 
\end{pmatrix}
\Bigg]
\end{aligned}
$$

<img src="{{ '/images/trajectory.png' | relative_url }}" style="width:100%;">
*Figure 1: Particle trajectories and mean position evolution under confinement.*

---

### Mean Squared Displacement (MSD)

The full time-dependent MSD for a particle starting at the origin is:

$$\langle \Delta r^2(t) \rangle = \frac{4D_t}{k}(1-e^{-2kt}) + \frac{2v_0^2}{(k+D_r)^2 + \Omega^2} \left[ \frac{k+D_r}{k D_r} (1-e^{-kt}) - \frac{(k+D_r)(1-e^{-(k+D_r)t}\cos\Omega t) - \Omega e^{-(k+D_r)t}\sin\Omega t}{(k+D_r)^2 + \Omega^2} \right]$$

In the stationary limit ($t \to \infty$):

$$\langle r^2 \rangle_{ss} = \frac{2D_t}{k} + \frac{v_0^2}{k(k+D_r) [1 + (\frac{\Omega}{k+D_r})^2]}$$

<img src="{{ '/images/msd.png' | relative_url }}" style="width:100%;">
*Figure 2: Mean squared displacement showing confinement-induced saturation.*

---

### Position Cross-Correlation

The hallmark of chirality is the cross-correlation $C_{xy}(t) = \langle x(t)y(0) - y(t)x(0) \rangle$. For $D_r \to 0$:

$$C_{xy}(t) = \frac{v_0^2}{k^2 + \Omega^2} \left[ e^{-kt} \sin\Omega t - \frac{\Omega}{k} e^{-kt} (1 - \cos\Omega t) \right]$$

<img src="{{ '/images/correlation.png' | relative_url }}" style="width:100%;">
*Figure 3: Cross-correlation showing chirality-induced temporal asymmetry.*

---

### Delay Function

We define the delay time $\tau_d$ as the time required for the spatial response to reach its maximum after a change in orientation. From the extremum of the correlation function, we find:

$$\tau_d = \frac{1}{\Omega} \tan^{-1}\left(\frac{\Omega}{k}\right)$$

This reveals that **delay emerges purely from confinement** $k$ and chirality $\Omega$, even in the absence of physical inertia.

<img src="{{ '/images/delay.png' | relative_url }}" style="width:100%;">
*Figure 4: Delay function illustrating temporal lag in confined dynamics.*

---

### Key Insights

* **Inertial Mimicry:** Confinement induces a response delay in overdamped systems.
* **Symmetry Breaking:** Chirality generates time-asymmetric cross-correlations.
* **Saturation:** The MSD reaches a steady-state value determined by the trap strength $k$.
* **Emergent Timescale:** $\tau_d$ defines a new characteristic timescale for confined active matter.

---
*This work demonstrates that confinement alone can generate delay in active matter systems without requiring inertia.*
