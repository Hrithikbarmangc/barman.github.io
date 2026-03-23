---
title: "Sorting of Chiral Active Particles in Anisotropic Potentials"
excerpt: "Investigating chirality-dependent localization in a harmonic and double-well potential landscape."
collection: portfolio
---

### Model Description
The separation of active particles based on their chirality represents a central problem in active matter physics, with direct relevance to microfluidic transport and biophysical sorting mechanisms. To investigate chirality-dependent dynamics, we consider a chiral active Brownian particle moving in an anisotropic potential landscape:

$$U(x,y) = \frac{1}{2}k x^{2} - \frac{\lambda_{1}}{2}y^{2} + \frac{\lambda_{2}}{4}y^{4}$$

This configuration provides harmonic confinement in the $x$-direction and a double-well structure in the $y$-direction, with minima at $y^\star = \pm \sqrt{\lambda_{1}/\lambda_{2}}$.

### Governing Equations
The overdamped dynamics of a single chiral active Brownian particle under this potential are governed by the following stochastic differential equations:

$$\dot{x}(t) = v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t)$$
$$\dot{y}(t) = v_0 \sin\phi(t) + \lambda_1 y(t) - \lambda_2 y^3(t) + \sqrt{2D_t}\,\xi_y(t)$$
$$\dot{\phi}(t) = \Omega + \sqrt{2D_r}\,\eta_\phi(t)$$

Where $v_0$ is the self-propulsion speed and $\Omega$ denotes the intrinsic chirality (angular velocity).

### Steady-State Analysis
By neglecting translational and rotational noise, we determine the deterministic orbits where particles accumulate. At long times ($t \gg 1/k$ and $t \gg 1/2\lambda_1$), the transients decay, yielding the steady-state oscillatory motion:

$$x_{\mathrm{ss}}(t) = \frac{v_0}{k^2 + \Omega^2} \Big[k\cos(\Omega t + \phi_0) + \Omega\sin(\Omega t + \phi_0)\Big]$$

$$y_{\mathrm{ss}}(t) = y^\star + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin(\Omega t + \phi_0) - \Omega \cos(\Omega t + \phi_0)\Big]$$

For an aligned initial orientation $\phi_0 = 0$, the steady-state solution shows that the particle localizes in a specific well based on the sign of its chirality:

$$y_{\mathrm{ss}}(t) = Sgn(\Omega)\sqrt{\frac{\lambda_1}{\lambda_2}} + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin\Omega t - \Omega \cos\Omega t \Big]$$

### Key Insights
* **Chirality-Based Localization:** The sign of the intrinsic chirality $\Omega$ determines which of the two stable minima the particle occupies, effectively breaking parity symmetry.
* **Suppression of Excursions:** The oscillation amplitude around $y^\star$ decreases with increasing $\lambda_1$ or $\Omega$, indicating that stronger confinement or faster chirality suppresses transverse excursions, leading to higher sorting precision.

---
*This work was selected for presentation at the **International Soft Matter Conference (ISMC 2026)** in Goa, India.*
