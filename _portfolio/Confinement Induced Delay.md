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

We consider a chiral active Brownian particle confined in a harmonic potential $$U(x,y) = \frac{1}{2}k(x^2 + y^2)$$. The overdamped Langevin dynamics are:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) - \mu k x(t) + \sqrt{2D_t}\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) - \mu k y(t) + \sqrt{2D_t}\xi_y(t) \\
\dot{\phi}(t) &= \Omega + \sqrt{2D_r}\eta(t)
\end{aligned}
$$


---

### Mean Position Dynamics

The ensemble-averaged position $\langle \mathbf{r}(t)\rangle$ is derived as:

$$\langle \mathbf{r}(t)\rangle = \mathbf{r}(0)e^{-\mu k t} + \beta e^{-\mu k t} \left[ e^{\alpha t} \begin{pmatrix} \alpha\cos\psi(t) + \Omega\sin\psi(t) \\ \alpha\sin\psi(t) - \Omega\cos\psi(t) \end{pmatrix} - \begin{pmatrix} \alpha\cos\psi(0) + \Omega\sin\psi(0) \\ \alpha\sin\psi(0) - \Omega\cos\psi(0) \end{pmatrix} \right]$$

where we define $$\psi(t) = \phi_0 + \Omega t$$, $$\alpha = \mu k - D_r$$, and $$\beta = v_0/(\alpha^2 + \Omega^2)$$.

<img src="{{ '/images/trajectory.png' | relative_url }}" style="width:100%;">
*Figure 1: Particle trajectories and mean position evolution under confinement.*

---

### Mean Squared Displacement (MSD)

The full time-dependent MSD, highlighting the transition from ballistic to localized behavior, is:

$$
\begin{aligned}
\langle r^2(t) \rangle &= \frac{2D_t}{\mu k}(1-e^{-2\mu k t}) + \frac{v_0^2\gamma}{(\gamma^2+\Omega^2)\mu k }(1-e^{-2\mu k t}) \\
&\quad + \frac{2v_0^2 e^{-\gamma t}}{(\gamma^2+\Omega^2)(\alpha^2+\Omega^2)} \left[ \Delta(e^{-\alpha t} - \cos\Omega t) - 2D_r \Omega \sin\Omega t \right]
\end{aligned}
$$

where the auxiliary parameters are defined as:

$$
\gamma = \mu k + D_r, \quad \alpha = \mu k - D_r, \quad \Delta = (\mu k)^2 - D_r^2 + \Omega^2
$$
The stationary MSD at long times ($$t \to \infty$$) is:

$$\langle r^2 \rangle_{ss} = \frac{2D_t}{\mu k} + \frac{v_0^2(\mu k + D_r)}{((\mu k + D_r)^2+\Omega^2)\mu k}$$

---

### Position Cross-Correlation

The position cross-correlation $\langle x(t)y(t) \rangle$ shows how the $x$ and $y$ coordinates of the particle are linked. This connection happens because the particle swims in circles (chirality $\Omega$) while being pulled by the trap ($k$).

The formula for the cross-correlation is:

$$
\langle x(t)y(t) \rangle = \frac{v_0^2 e^{-2\mu k t}}{\beta^2 + \Omega^2} \left[ \tau_1(t) - \tau_2(t) \right]
$$

To find the values for $\tau_i(t)$, use:

$$
\tau_i(t) = \frac{e^{s_i t}A_i(t) - A_i(0)}{s_i^2 + k_i^2}
$$

The term $A_i(t)$ is calculated as:

$$
A_i(t) = (\beta s_i - \Omega k_i)\sin(k_i t + 2\phi_0) - (\beta k_i + \Omega s_i)\cos(k_i t + 2\phi_0)
$$

#### Parameters
Plug these values into the equations above:

$$
\begin{aligned}
\beta &= \mu k - 3D_r \\
s_1 &= 2\mu k - 4D_r, \quad s_2 = \mu k - D_r \\
k_1 &= 2\Omega, \quad k_2 = \Omega
\end{aligned}
$$

---

### The Delay Function: Our Key Finding

In a free system ($k=0$), a particle's velocity and its propulsion direction are perfectly aligned. However, we found that when a trap is added ($k>0$), the velocity and orientation fall out of sync.

To measure this, we use a function $C(t)$ that tests for **Time-Reversal Asymmetry**. It compares how the velocity at time $t$ relates to the orientation at time $0$, versus the other way around.

The exact formula for this symmetry-breaking function is:

$$
C(t) = \frac{-\mu k v_0}{\alpha^2+\Omega^2} \left[ e^{-D_r t}(\alpha \cos\Omega t + \Omega \sin\Omega t) - \alpha e^{-\mu k t} \right]
$$

#### Key Takeaways
* **Geometric Delay:** Usually, "delay" in physics comes from mass or inertia. Here, the delay is created purely by the **harmonic trap** ($k$) and the **chirality** ($\Omega$).

---
*This work demonstrates that confinement alone can generate delay in active matter systems without requiring inertia.*
