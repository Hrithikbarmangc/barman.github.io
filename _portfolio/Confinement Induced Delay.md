---
title: "Confinement-Induced Delay in Active Brownian Motion"
excerpt: "Investigating delay effects in confined active particle dynamics using trajectory statistics and correlation measures."
collection: portfolio
mathjax: true
---

### Model Description

We study the emergence of delay in the dynamics of active Brownian particles under spatial confinement. Confinement alters particle trajectories and induces non-trivial temporal correlations, which are crucial for understanding transport in crowded and structured environments.

The system consists of an active Brownian particle confined within a potential landscape, where geometric constraints influence its motion and lead to delayed response behavior.

---

### Governing Equations

The overdamped dynamics are described by:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) + F_x(x,y) + \sqrt{2D_t}\,\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) + F_y(x,y) + \sqrt{2D_t}\,\xi_y(t) \\
\dot{\phi}(t) &= \sqrt{2D_r}\,\eta(t)
\end{aligned}
$$

where:
- $$v_0$$ is the self-propulsion speed  
- $$D_t$$ and $$D_r$$ are translational and rotational diffusion coefficients  
- $$F_x, F_y$$ represent confinement forces  
- $$\xi_x, \xi_y, \eta$$ are Gaussian white noises  

---

### Trajectory and Mean Position

The confined geometry leads to modified particle trajectories compared to free motion. Over time, the particle exhibits restricted exploration and anisotropic displacement.

We analyze:
- Individual trajectories  
- Ensemble-averaged mean position $$\langle x(t) \rangle, \langle y(t) \rangle$$  

<img src="{{ '/images/trajectory_mean_position.png' | relative_url }}" style="width:100%;">

*Figure 1: Particle trajectories and evolution of mean position under confinement.*

---

### Mean Squared Displacement (MSD)

To quantify transport properties, we compute the mean squared displacement:

$$
\mathrm{MSD}(t) = \langle [\mathbf{r}(t) - \mathbf{r}(0)]^2 \rangle
$$

Confinement leads to:
- initial ballistic regime  
- crossover to diffusive behavior  
- eventual saturation due to spatial restriction  

<img src="{{ '/images/msd_plot.png' | relative_url }}" style="width:100%;">

*Figure 2: Mean squared displacement showing confinement-induced suppression of diffusion.*

---

### Cross-Correlation and Delay

To characterize temporal correlations, we compute the cross-correlation function:

$$
C_{xy}(t) = \langle x(0)\,y(t) \rangle
$$

The presence of confinement introduces:
- phase lag between coordinates  
- delayed response in particle motion  

We define a delay function based on the shift in correlation peaks:

$$
\tau_d = \arg\max_t \, C_{xy}(t)
$$

<img src="{{ '/images/cross_correlation_delay.png' | relative_url }}" style="width:100%;">

*Figure 3: Cross-correlation function and extracted delay time under confinement.*

---

### Key Insights

- Confinement-induced delay: Spatial constraints introduce a measurable lag in the system’s dynamical response.
- Suppressed diffusion: MSD saturates at long times due to restricted motion.
- Correlated dynamics: Cross-correlation reveals coupling between spatial degrees of freedom.
- Emergent timescale: The delay time $$\tau_d$$ acts as a characteristic timescale of confined dynamics.

---

- *This work investigates confinement-induced delay effects in active Brownian motion using trajectory statistics and correlation analysis.*
