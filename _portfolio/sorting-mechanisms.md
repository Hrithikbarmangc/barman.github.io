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

![Potential Landscape]({{ site.baseurl }}/images/our_chiral_sorting_potential_colorbar_top_label.png)
*Figure 1: Potential energy landscape $U(x,y)$ showing the harmonic confinement in $x$ and the double-well structure in $y$.*

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

### Steady-State Analysis
By neglecting translational and rotational noise, we determine the deterministic orbits where particles accumulate. At long times ($t \gg 1/k$), the transients decay, yielding the steady-state oscillatory motion. For an aligned initial orientation $\phi_0 = 0$, the particle localizes in a specific well based on the sign of its chirality:

$$y_{\mathrm{ss}}(t) = \text{sgn}(\Omega)\sqrt{\frac{\lambda_1}{\lambda_2}} + \frac{v_0}{4\lambda_1^2 + \Omega^2} \Big[2\lambda_1 \sin\Omega t - \Omega \cos\Omega t \Big]$$

![Chiral Separation Snapshots]({{ site.baseurl }}/images/chiral_separation_snapshots_6.png)
*Figure 2: Time evolution showing the spatial separation of chiral active particles into their respective steady-state wells.*

### Sorting Efficiency
We quantify the efficiency of chiral sorting by measuring the fraction of particles that reach the correct potential well according to their chirality. Let $N_L$ and $N_R$ denote the numbers of left-handed ($-\Omega$) and right-handed ($+\Omega$) particles that successfully reach the corresponding wells. The sorting efficiency is defined as:

$$\eta = \frac{N_L + R_R}{N}$$

Where $N$ is the total number of particles. By construction, $0 \le \eta \le 1$, with $\eta = 1$ corresponding to perfect separation. We evaluated the sorting efficiency as a function of three main parameters: the initial particle orientation $\phi_0$, the potential curvature $\lambda_1$, and the magnitude of chirality $|\Omega|$.

![Combined Efficiency Plots]({{ site.baseurl }}/images/combined_efficiency_plots.png)
*Figure 3: Sorting efficiency $\eta$ as a function of (left) initial orientation $\phi_0/\pi$, (center) potential parameter ratio $\lambda_1/\lambda_2$, and (right) chirality magnitude $|\Omega|$.*

### Key Insights
* **Chirality-Based Localization:** The sign of $\Omega$ determines the choice of the stable minimum, enabling spatial sorting.
* **Suppression of Excursions:** Higher chirality $|\Omega|$ suppresses transverse excursions, leading to higher sorting precision.
* **Orientation Dependence:** Peak efficiency is achieved when the particle's initial propulsion is aligned with the potential's primary axes ($\phi_0 \approx 0$).

---
*This work was selected for presentation at the **International Soft Matter Conference (ISMC 2026)** in Goa, India.*
