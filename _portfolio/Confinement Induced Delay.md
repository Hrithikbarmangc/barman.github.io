---
title: "Confinement-Induced Delay in Active Brownian Motion"
excerpt: "Emergence of temporal delay and correlations in confined chiral active particle dynamics."
collection: portfolio
mathjax: true
---

<div style="text-align: center; margin: 25px 0;">
  <video width="60%" autoplay loop muted playsinline style="border-radius: 8px; border: 1px solid #333;">
    <source src="{{ '/images/active_particle_animation.mp4' | relative_url }}" type="video/mp4">
  </video>
  <p><strong> </strong> Visualization geometric lag between propulsion (green) and velocity (red) vectors.</p>
</div>

### Overview

We investigate how spatial confinement modifies the dynamics of chiral active Brownian particles leading to the emergence of temporal delay and non-trivial position correlations. 

Our key finding is that even in overdamped dynamics confinement induces a **finite lag between propulsion and spatial response**, purely due to the interplay of chirality and trapping.

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

The ensemble-averaged position $$\langle \mathbf{r}(t)\rangle$$ is derived as:

$$\langle \mathbf{r}(t)\rangle = \mathbf{r}(0)e^{-\mu k t} + \beta e^{-\mu k t} \left[ e^{\alpha t} \begin{pmatrix} \alpha\cos\psi(t) + \Omega\sin\psi(t) \\ \alpha\sin\psi(t) - \Omega\cos\psi(t) \end{pmatrix} - \begin{pmatrix} \alpha\cos\psi(0) + \Omega\sin\psi(0) \\ \alpha\sin\psi(0) - \Omega\cos\psi(0) \end{pmatrix} \right]$$

where we define $$\psi(t) = \phi_0 + \Omega t$$, $$\alpha = \mu k - D_r$$, and $$\beta = v_0/(\alpha^2 + \Omega^2)$$.

<img src="{{ '/images/35920222-1.png' | relative_url }}" style="width:100%;">

Figure 1:  Mean position magnitude for varying trap strength $$k$$ and chirality $$\Omega$$.

---

### Mean Squared Displacement (MSD)

The full time-dependent MSD, highlighting the transition from ballistic to localized behavior, is:

$$
\begin{aligned}
\langle r^2(t) \rangle &= \frac{2D_t}{\mu k}(1-e^{-2\mu k t}) + \frac{v_0^2\gamma}{(\gamma^2+\Omega^2)\mu k }(1-e^{-2\mu k t}) \\
&\quad + \frac{2v_0^2 e^{-\gamma t}}{(\gamma^2+\Omega^2)(\alpha^2+\Omega^2)} \left[ \Delta(e^{-\alpha t} - \cos\Omega t) - 2D_r \Omega \sin\Omega t \right]
\end{aligned}
$$

where the parameters are defined as:

$$
\gamma = \mu k + D_r, \quad \alpha = \mu k - D_r, \quad \Delta = (\mu k)^2 - D_r^2 + \Omega^2
$$

The stationary MSD at long times ($$t \to \infty$$) is:

$$
\langle r^2(t) \rangle_{ss} = \frac{2D_t}{\mu k} + \frac{v_0^2(\mu k + D_r)}{((\mu k + D_r)^2 + \Omega^2)\mu k}
$$


<img src="{{ '/images/msd_hollow_markers_scaling (1).png' | relative_url }}" style="width:100%;">

Figure 2:  Mean Squared Displacement (MSD) for varying trap strength $$k$$ and chirality $$\Omega$$. 

---

### Position Cross-Correlation

The position cross-correlation $$\langle x(t)y(t) \rangle$$ shows how the $$x$$ and $$y$$ coordinates of the particle are linked. This connection happens because the particle swims in circles  while being pulled by the trap .

The formula for the cross-correlation is:

$$
\langle x(t)y(t) \rangle = \frac{v_0^2 e^{-2\mu k t}}{\beta^2 + \Omega^2} \left[ \tau_1(t) - \tau_2(t) \right]
$$

To find the values for $$\tau_i(t)$$, use:

$$
\tau_i(t) = \frac{e^{s_i t}A_i(t) - A_i(0)}{s_i^2 + k_i^2}
$$

The term $$A_i(t)$$ is calculated as:

$$
A_i(t) = (\beta s_i - \Omega k_i)\sin(k_i t + 2\phi_0) - (\beta k_i + \Omega s_i)\cos(k_i t + 2\phi_0)
$$

#### Parameters
Plug these values into the equations above:

$$
\beta = \mu k - 3D_r, \quad s_1 = 2\mu k - 4D_r, \quad s_2 = \mu k - D_r, \quad k_1 = 2\Omega, \quad k_2 = \Omega
$$


<img src="{{ '/images/cross_correlation_uniform_ticks (2).png' | relative_url }}" style="width:100%;">

Figure 3: Position cross-correlation $$\langle x(t)y(t) \rangle$$ showing oscillatory behavior for varying chirality $$\Omega$$ (left) and trap strength $$k$$ (right).

---

###  **The Delay Function**: Geometric Lag

In this work, we quantify how confinement forces a lag between the particle's orientation and its actual velocity. We do this by measuring the breaking of time-reversal symmetry.

<img src="{{ '/images/my_plot.png' | relative_url }}" style="width:100%;">

Figure 4: Time evolution of propulsion angle $$\phi(t)$$ and velocity angle $$\Theta(t)$$ for free ($$k=0$$) and confined ($$k=10$$) systems.
#### 1. General Definition
The delay function $$C(t)$$ is defined as the difference between the forward and backward correlations of velocity $$\dot{\mathbf{r}}$$ and orientation $$\hat{\mathbf{n}}$$:

$$
C(t) = \langle \dot{\mathbf{r}}(t) \cdot \hat{\mathbf{n}}(0) \rangle - \langle \dot{\mathbf{r}}(0) \cdot \hat{\mathbf{n}}(t) \rangle
$$

For a free overdamped particle ($$k=0$$), this function is zero because the velocity follows the orientation perfectly. However, adding a trap breaks this symmetry.

#### 2. Expression for our Model
For a chiral active particle in a harmonic trap ($$k>0$$), we derive the following analytical expression:

$$
C(t) = \frac{-\mu k v_0}{\alpha^2 + \Omega^2} \left[ e^{-D_r t}(\alpha \cos\Omega t + \Omega \sin\Omega t) - \alpha e^{-\mu k t} \right]
$$

where the parameters are:

* $$\alpha$$ = $$\mu k$$ - $$D_r$$
* $$\Omega$$ is the chirality
* $$k$$ is the trap strength
<img src="{{ '/images/delay_function_toprow_k.png' | relative_url }}" style="width:100%;">

Figure 5: Comparison between theoretical (Th) and simulation (Sim) results for the delay function $$C(t)$$ at different trap strengths $$k$$.

---

### Key Findings

-  At long times ($$t \to \infty$$) the particle reaches a steady state where the MSD saturates to a constant value. In this high-time limit, the effective diffusion constant vanishes, indicating that the particle is trapped and its motion is localized within the potential. 

- The core physical mechanism behind the observed delay is the angular misalignment between the propulsion direction $$\hat{n}(t)$$ and the actual velocity vector $$\dot{r}(t)$$. While these vectors are perfectly aligned in a free system,the harmonic trap $$k$$ creates a persistent lag. This proves that a finite response time or "pseudo-inertia" can emerge purely from confinement and chirality, even in a completely overdamped system.

---
