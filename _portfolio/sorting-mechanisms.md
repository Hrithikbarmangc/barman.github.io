---
title: "Chirality-Driven Sorting of Active Brownian Particles"
excerpt: "Investigating chirality-dependent localization in a harmonic and double-well potential landscape."
collection: portfolio
mathjax: true
---

### Model Description

We investigate the sorting of chiral active Brownian particles in a structured potential landscape. Chirality-induced transport plays an important role in active matter systems, with applications in microfluidic separation and biological transport.

The system consists of a single chiral active particle moving in an anisotropic potential:

$$
U(x,y) = \frac{1}{2}k x^{2} - \frac{\lambda_{1}}{2}y^{2} + \frac{\lambda_{2}}{4}y^{4}
$$

This potential provides harmonic confinement in the $$x$$-direction and a double-well structure in the $$y$$-direction, with minima located at:

$$
y^\star = \pm \sqrt{\frac{\lambda_{1}}{\lambda_{2}}}
$$

<img src="{{ '/images/our_chiral_sorting_potential_colorbar_top_label (1).png' | relative_url }}" style="width:100%;">

Figure 1: Potential landscape showing harmonic confinement in $$x$$ and a bistable double-well structure in $$y$$.

---

### Governing Equations

The overdamped dynamics of a chiral active Brownian particle are described by:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) + \lambda_1 y(t) - \lambda_2 y^3(t) + \sqrt{2D_t}\,\xi_y(t) \\
\dot{\phi}(t) &= \Omega + \sqrt{2D_r}\,\eta(t)
\end{aligned}
$$

Here:
- $$v_0$$ is the self-propulsion speed  
- $$\Omega$$ is the intrinsic chirality (angular velocity)  
- $$D_t$$ and $$D_r$$ $are translational and rotational noise strengths  
- $$\xi_x, \xi_y, \eta$$ are Gaussian white noises  

---

### Deterministic Steady-State Behavior

In the absence of noise ($$D_t = D_r = 0$$), the dynamics become deterministic. After transient relaxation and symmetry breaking, the particle localizes in one of the two stable wells depending on the sign of its chirality.

For an initial orientation $$\phi_0 = 0$$, the long-time solution for the $$y$$-coordinate can be approximated as:

$$
y_{\mathrm{ss}}(t) =
\mathrm{sgn}(\Omega)\sqrt{\frac{\lambda_1}{\lambda_2}}
+
\frac{v_0}{4\lambda_1^2 + \Omega^2}
\left[
2\lambda_1 \sin(\Omega t) - \Omega \cos(\Omega t)
\right]
$$

This expression shows that:
- The **sign of $$\Omega$$ selects the well**
- The particle undergoes **oscillatory motion around the stable minimum**

<img src="{{ '/images/chiral_separation_snapshots_6.png' | relative_url }}" style="width:100%;">

*Figure 2: Time evolution showing chirality-dependent localization into opposite wells.*

---

### Sorting Efficiency

To quantify sorting performance, we define the efficiency as the fraction of particles that end up in the correct well corresponding to their chirality.

$$
\eta = \frac{N_{\mathrm{correct}}}{N}
$$

where:
- $$N_{\mathrm{correct}}$$ is the number of correctly sorted particles  
- $$N$$ is the total number of particles  

A particle is considered correctly sorted if:
- $$\Omega > 0$$ and $$y > 0$$ 
- $$\Omega < 0$$ and $$y < 0$$  

Thus, $$0 \le \eta \le 1$$, with $$\eta = 1$$ corresponding to perfect sorting.

We evaluate $$\eta$$ as a function of:
- Initial orientation $$\phi_0$$  
- Potential parameter ratio $$\lambda_1/\lambda_2$$  
-  Chirality magnitude \( |\Omega| \)

<img src="{{ '/images/combined_efficiency_plots.png' | relative_url }}" style="width:100%;">

Figure 3: Sorting efficiency $$\eta$$ as a function of (left) initial orientation $$\phi_0/\pi$$, (center) potential ratio $$\lambda_1/\lambda_2$$, and (right) chirality magnitude \( |\Omega| \).

---

### Key Insights

- Chirality-d riven localization: The sign of $$\Omega$$ determines which well the particle occupies.
- Enhanced sorting at high chirality: Increasing \( |\Omega| \) suppresses oscillatory excursions and improves accuracy.
- Role of initial orientation: Sorting efficiency depends strongly on $$\phi_0$$, with optimal alignment near $$\phi_0 \approx 0$$.
- Control via potential landscape: The ratio $$\lambda_1/\lambda_2$$ tunes the stability and separation efficiency.

---

*This work was selected for presentation at the **International Soft Matter Conference (ISMC 2026)**, Goa, India.*
