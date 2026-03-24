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

We consider a chiral active Brownian particle confined in a harmonic potential:

$$
U(x,y) = \frac{1}{2}k(x^2 + y^2)
$$

The overdamped dynamics are:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) - ky(t) + \sqrt{2D_t}\,\xi_y(t) \\
\dot{\phi}(t) &= \Omega + \sqrt{2D_r}\,\eta(t)
\end{aligned}
$$

---

### Mean Position Dynamics

The ensemble-averaged position evolves as:

$$
\begin{aligned}
\langle \mathbf{r}(t)\rangle
  &= \mathbf{r}(0)\,e^{-\mu k t} \\
  &\quad + \beta\, e^{-\mu k t} \Bigg[
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

The full time-dependent MSD is:

$$
\begin{aligned}
\langle r^2(t) \rangle 
&= \frac{2D_t}{\mu k}(1-e^{-2\mu k t})
+ \frac{v_0^2\gamma}{(\gamma^2+\Omega^2)\mu k }(1-e^{-2\mu k t}) \\
&\quad + \frac{2v_0^2 e^{-\gamma t}}{(\gamma^2+\Omega^2)(\alpha^2+\Omega^2)}
\Big[
\Delta\big(e^{-\alpha t }-\cos(\Omega t)\big)
-2D_r \Omega\sin(\Omega t)
\Big]
\end{aligned}
$$

The stationary MSD is:

$$
\langle r^2(t \to \infty) \rangle =
\frac{2D_t}{\mu k}
+ \frac{v_0^2(\mu k + D_r)}{((\mu k + D_r)^2+\Omega^2)\mu k}
$$

The long-time diffusion vanishes:

$$
D_L^{(\text{trap})} 
= \lim_{t \to \infty} \frac{\langle r^2(t)\rangle}{4t} = 0
$$

<img src="{{ '/images/msd.png' | relative_url }}" style="width:100%;">

*Figure 2: Mean squared displacement showing confinement-induced saturation.*

---

### Cross-Correlation

The position cross-correlation is defined as:

$$
\langle x(t)y(t) \rangle 
= v_0^2 e^{-2\mu k t} 
\int_0^t \int_0^t e^{\mu k (t_1 + t_2)}
\langle \sin \phi(t_1) \cos \phi(t_2) \rangle
\, dt_2 \, dt_1
$$

with angular correlation:

$$
\begin{aligned}
\langle \sin\phi(t_1)\cos\phi(t_2) \rangle &=
\frac{1}{2} e^{-D_r|t_1-t_2|} \sin\Omega(t_1-t_2) \\
&\quad + \frac{1}{2} e^{-D_r(t_1+t_2+2\min(t_1,t_2))}
\sin(2\phi_0 + \Omega(t_1+t_2))
\end{aligned}
$$

The final closed-form expression is:

$$
\langle x(t)y(t) \rangle =
\frac{v_0^2\,e^{-2\mu k t}}{\beta^2 +\Omega^2}
\Big(\tau_1(t) -\tau_2(t)\Big)
$$

where

$$
\tau_i(t)
= \frac{e^{s_i t}A_i(t) - A_i(0)}{s_i^2 + k_i^2}
$$

$$
A_i(t)= (\beta s_i - \Omega k_i)\sin(k_i t + 2\phi_0)
- (\beta k_i + \Omega s_i)\cos(k_i t + 2\phi_0)
$$

with parameters:

$$
\beta=\mu k-3D_r, \quad
s_1=2\mu k-4D_r, \quad
s_2=\mu k-D_r
$$

$$
k_1=2\Omega, \quad
k_2=\Omega
$$

<img src="{{ '/images/correlation.png' | relative_url }}" style="width:100%;">

*Figure 3: Cross-correlation showing chirality-induced temporal asymmetry.*

---

### Delay Function

The delay function is given by:

$$
C(t) = \frac{-\mu k v_0}{\alpha^2+\Omega^2}
\Big[
e^{-D_r t}\big(\alpha \cos\Omega t + \Omega \sin\Omega t\big) 
- \alpha e^{-\mu k t}
\Big]
$$

<img src="{{ '/images/delay.png' | relative_url }}" style="width:100%;">

*Figure 4: Delay function illustrating temporal lag in confined dynamics.*

---

### Key Insights

- Confinement induces delay in overdamped active systems  
- Chirality generates time-asymmetric correlations  
- MSD saturates due to trapping  
- Delay emerges without inertia  

---

- *This work demonstrates that confinement alone can generate delay in active matter systems without requiring inertia.*
