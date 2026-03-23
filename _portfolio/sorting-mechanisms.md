---
title: "Chirality-Driven Sorting of Active Brownian Particles"
excerpt: "Investigating chirality-dependent localization in a harmonic and double-well potential landscape."
collection: portfolio
mathjax: true
---

### Model Description
The separation of active particles based on their chirality represents a central problem in active matter physics, with direct relevance to microfluidic transport and biophysical sorting mechanisms. To investigate chirality-dependent dynamics, we consider a chiral active Brownian particle moving in an anisotropic potential landscape:

$$U(x,y) = \frac{1}{2}k x^{2} - \frac{\lambda_{1}}{2}y^{2} + \frac{\lambda_{2}}{4}y^{4}$$

This configuration provides harmonic confinement in the $x$-direction and a double-well structure in the $y$-direction, with minima at $y^\star = \pm \sqrt{\lambda_{1}/\lambda_{2}}$.

### Governing Equations
The overdamped dynamics of a single chiral active Brownian particle under this potential are governed by the following stochastic differential equations:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) + \lambda_1 y(t) - \lambda_2 y^3(t) + \sqrt{2D_t}\,\xi_y(t) \\
\dot{\phi}(t) &= \Omega + \sqrt{2D_r}\,\eta_\phi(t)
\end{aligned}
$$

Where $v_0$ is the self-propulsion speed and $\Omega$ denotes the intrinsic chirality (angular velocity).

### Sorting Dynamics
The following snapshots illustrate the time evolution of the separation process. Particles with opposite handedness ($\pm \Omega$) are steered into opposite wells of the potential, effectively breaking parity symmetry.

![Chiral Separation Snapshots](/images/chiral_separation_snapshots_6.png)
*Figure 1: Time evolution showing the spatial separation of chiral active particles.*

### Steady-State Analysis
By neglecting translational and rotational noise, we determine the deterministic orbits where particles accumulate. At long times ($t \gg 1/k$ and $t \gg 1/2\lambda_1$), the transients decay, yielding the steady-state oscillatory motion:

$$x_{\mathrm{ss}}(t) = \frac{v_0}{k^2 + \Omega^2} \Big[k\cos(\Omega t + \phi_0) + \Omega\sin(\Omega t + \phi_0)\Big]$$

$$y_{\mathrm{ss}}(t) = y^\star + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin(\Omega t + \phi_0) - \Omega \cos(\Omega t + \phi_0)\Big]$$

For an aligned initial orientation $\phi_0 = 0$, the particle localizes in a specific well based on the sign of its chirality:

$$y_{\mathrm{ss}}(t) = \text{sgn}(\Omega)\sqrt{\frac{\lambda_1}{\lambda_2}} + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin\Omega t - \Omega \cos\Omega t \Big]$$

![Chirality Magnitude Sorting](/images/chiral_sorting_magnitude (1).png)
*Figure 2: Spatial distributions within the wells as a function of chirality magnitude.*

### Sorting Efficiency
The sorting efficiency ($\eta$) depends significantly on the initial orientation $\phi_0$ and the numerical parameters of the system.

<div style="display: flex; justify-content: space-between;">
  <img src="/images/overall_efficiency_with_initial_angle.png" width="49%" />
  <img src="/images/overall_efficiency_numba.png" width="49%" />
</div>
*Figure 3: Left: Efficiency vs Initial Angle. Right: Numerical mapping of global sorting efficiency.*

### Key Insights
* **Chirality-Based Localization:** The sign of $\Omega$ determines the choice of the stable minimum, enabling spatial sorting.
* **Suppression of Excursions:** The oscillation amplitude around $y^\star$ decreases with increasing $\lambda_1$ or $\Omega$, leading to higher sorting precision.
* **Orientation Dependence:** Peak efficiency is achieved when the particle's initial propulsion is aligned with the potential's primary axes.

---
*This work was selected for presentation at the **International Soft Matter Conference (ISMC 2026)** in Goa, India.*
