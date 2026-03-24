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

We consider a chiral active Brownian particle confined in a harmonic potential $U(x,y) = \frac{1}{2}k(x^2 + y^2)$. The overdamped Langevin dynamics are:


$$\dot{x}(t) = v_0 \cos\phi(t) - \mu k x(t) + \sqrt{2D_t}\xi_x(t)$$ \\
$$\dot{y}(t) = v_0 \sin\phi(t) - \mu k y(t) + \sqrt{2D_t}\xi_y(t)$$ \\
$$\dot{\phi}(t) = \Omega + \sqrt{2D_r}\eta(t)$$

---

### Mean Position Dynamics

The ensemble-averaged position $\langle \mathbf{r}(t)\rangle$ is derived as:

$$\langle \mathbf{r}(t)\rangle = \mathbf{r}(0)e^{-\mu k t} + \beta e^{-\mu k t} \left[ e^{\alpha t} \begin{pmatrix} \alpha\cos\psi(t) + \Omega\sin\psi(t) \\ \alpha\sin\psi(t) - \Omega\cos\psi(t) \end{pmatrix} - \begin{pmatrix} \alpha\cos\psi(0) + \Omega\sin\psi(0) \\ \alpha\sin\psi(0) - \Omega\cos\psi(0) \end{pmatrix} \right]$$

where we define $\psi(t) = \phi_0 + \Omega t$, $\alpha = \mu k - D_r$, and $\beta = v_0/(\alpha^2 + \Omega^2)$.

<img src="{{ '/images/trajectory.png' | relative_url }}" style="width:100%;">
*Figure 1: Particle trajectories and mean position evolution under confinement.*

---

### Mean Squared Displacement (MSD)

The full time-dependent MSD, highlighting the transition from ballistic to localized behavior, is:

$$\langle r^2(t) \rangle = \frac{2D_t}{\mu k}(1-e^{-2\mu k t}) + \frac{v_0^2 (\mu k + D_r)}{((\mu k + D_r)^2 + \Omega^2) \mu k} (1-e^{-2\mu k t}) + \frac{2v_0^2 e^{-(\mu k + D_r)t} [ (\mu k - D_r)\cos\Omega t + \Omega \sin\Omega t ]}{((\mu k + D_r)^2 + \Omega^2)((\mu k - D_r)^2 + \Omega^2)}$$

The stationary MSD ($t \to \infty$) is:

$$\langle r^2 \rangle_{ss} = \frac{2D_t}{\mu k} + \frac{v_0^2(\mu k + D_r)}{((\mu k + D_r)^2+\Omega^2)\mu k}$$

---

### Cross-Correlation and Delay

The position cross-correlation $C_{xy}(t)$ reveals the broken symmetry. We define the delay function as:

$$C(t) = \frac{-\mu k v_0}{\alpha^2+\Omega^2} \left[ e^{-D_r t}(\alpha \cos\Omega t + \Omega \sin\Omega t) - \alpha e^{-\mu k t} \right]$$

The extracted delay time $\tau_d$ at which this correlation is maximized is:

$$\tau_d = \frac{1}{\Omega} \tan^{-1}\left(\frac{\Omega}{\mu k}\right)$$

---

### Key Insights

* **Inertial Mimicry:** Confinement induces a response delay in overdamped systems without physical mass.
* **Symmetry Breaking:** Chirality generates time-asymmetric cross-correlations.
* **Emergent Timescale:** The delay $\tau_d$ defines how the particle "remembers" its orientation in a trap.

---
*This work demonstrates that confinement alone can generate delay in active matter systems without requiring inertia.*
