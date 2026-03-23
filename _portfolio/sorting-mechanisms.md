---
title: "Sorting of Chiral Active Particles in Anisotropic Potentials"
excerpt: "Investigating chirality-dependent localization in a harmonic and double-well potential landscape."
collection: portfolio
---

### Model Description
[cite_start]The separation of active particles based on their chirality represents a central problem in active matter physics, with direct relevance to microfluidic transport and biophysical sorting mechanisms. To investigate chirality-dependent dynamics, we consider a chiral active Brownian particle moving in an anisotropic potential landscape:

$$U(x,y) = \frac{1}{2}k x^{2} - \frac{\lambda_{1}}{2}y^{2} + \frac{\lambda_{2}}{4}y^{4}$$

This configuration provides harmonic confinement in the $x$-direction and a double-well structure in the $y$-direction, with minima at $y^\star = \pm \sqrt{\lambda_{1}/\lambda_{2}}$.

### Governing Equations
[cite_start]The overdamped dynamics of a single chiral active Brownian particle under this potential are governed by the following stochastic differential equations:

$$\dot{x}(t) = v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t)$$
$$\dot{y}(t) = v_0 \sin\phi(t) + \lambda_1 y(t) - \lambda_2 y^3(t) + \sqrt{2D_t}\,\xi_y(t)$$
$$\dot{\phi}(t) = \Omega + \sqrt{2D_r}\,\eta_\phi(t)$$

[cite_start]Where $v_0$ is the self-propulsion speed and $\Omega$ denotes the intrinsic chirality (angular velocity).

### Steady-State Analysis
By neglecting translational and rotational noise, we can determine the deterministic orbits. [cite_start]At long times $(t \gg 1/k)$, the transients decay, yielding the steady-state oscillatory motion:

$$x_{\mathrm{ss}}(t) = \frac{v_0}{k^2 + \Omega^2} \Big[k\cos(\Omega t + \phi_0) + \Omega\sin(\Omega t + \phi_0)\Big]$$

$$y_{\mathrm{ss}}(t) = y^\star + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin(\Omega t + \phi_0) - \Omega \cos(\Omega t + \phi_0)\Big]$$

[cite_start]For an aligned initial orientation $\phi_0 = 0$, the solution simplifies to show how the particle localizes based on the sign of its chirality:

$$y_{\mathrm{ss}}(t) = \operatorname{sgn}(\omega)\sqrt{\frac{\lambda_1}{\lambda_2}} + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin\Omega t - \Omega \cos\Omega t \Big]$$

### Key Insights
* [cite_start]**Chirality-Based Localization:** Particles with different signs of $\Omega$ settle into different wells of the potential, enabling spatial sorting.
* [cite_start]**Suppression of Excursions:** The oscillation amplitude around $y^\star$ decreases with increasing $\lambda_1$ or $\Omega$, indicating that stronger confinement or faster chirality suppresses transverse excursions.

---
*This work was accepted for presentation at the **International Soft Matter Conference (ISMC 2026)** in Goa, India.*
