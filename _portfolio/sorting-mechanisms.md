---
title: "Sorting of Chiral Active Particles in Anisotropic Potentials"
excerpt: "Investigating chirality-dependent localization in a harmonic and double-well potential landscape."
collection: portfolio
mathjax: true
---

### Model Description
The separation of active particles based on their chirality represents a central problem in active matter physics. We consider a chiral active Brownian particle moving in an anisotropic potential landscape:

$$U(x,y) = \frac{1}{2}k x^{2} - \frac{\lambda_{1}}{2}y^{2} + \frac{\lambda_{2}}{4}y^{4}$$

This configuration provides harmonic confinement in $x$ and a double-well structure in $y$, with minima at $y^\star = \pm \sqrt{\lambda_{1}/\lambda_{2}}$.

![Chiral Separation Snapshots]({{ site.url }}{{ site.baseurl }}/images/chiral_separation_snapshots_6.png)
*Figure 1: Time evolution showing the spatial separation of chiral active particles.*

### Governing Equations
The overdamped dynamics of a single chiral active Brownian particle under this potential are governed by:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) + \lambda_1 y(t) - \lambda_2 y^3(t) + \sqrt{2D_t}\,\xi_y(t) \\
\dot{\phi}(t) &= \Omega + \sqrt{2D_r}\,\eta_\phi(t)
\end{aligned}
$$

### Steady-State Analysis
At long times ($t \gg 1/k$), the particle localizes in a specific well based on the sign of its chirality:

$$y_{\mathrm{ss}}(t) = \text{sgn}(\Omega)\sqrt{\frac{\lambda_1}{\lambda_2}} + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin\Omega t - \Omega \cos\Omega t \Big]$$

![Chirality Magnitude Sorting]({{ site.url }}{{ site.baseurl }}/images/chiral_sorting_magnitude (1).png)
*Figure 2: Spatial distributions within the wells as a function of chirality magnitude.*

### Sorting Efficiency
The sorting efficiency ($\eta$) depends significantly on the initial orientation $\phi_0$.

<div style="display: flex; justify-content: space-between; align-items: center;">
  <img src="{{ site.url }}{{ site.baseurl }}/images/overall_efficiency_with_initial_angle.png" style="width: 49%; height: auto;" />
  <img src="{{ site.url }}{{ site.baseurl }}/images/overall_efficiency_numba.png" style="width: 49%; height: auto;" />
</div>
*Figure 3: Left: Efficiency vs Initial Angle. Right: Numerical mapping of global sorting efficiency.*

---
*Accepted for presentation at the **International Soft Matter Conference (ISMC 2026)**.*
