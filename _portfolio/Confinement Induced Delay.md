---
title: "Confinement-Induced Delay in Active Brownian Motion"
excerpt: "Emergence of delay and temporal correlations in confined chiral active particle dynamics."
collection: portfolio
mathjax: true
---

### Overview

We investigate how spatial confinement modifies the dynamics of chiral active Brownian particles, leading to the emergence of **temporal delay** and **non-trivial correlations**.

Our key finding is that even in an overdamped system, confinement induces a **finite response lag** between propulsion and spatial motion. This delay arises purely from the interplay of **chirality and trapping**, without requiring inertia.

---

### Model and Method

We consider a chiral active Brownian particle confined in a harmonic potential:

$$
U(x,y) = \frac{1}{2}k(x^2 + y^2)
$$

The overdamped Langevin dynamics are:

$$
\begin{aligned}
\dot{x}(t) &= v_0 \cos\phi(t) - kx(t) + \sqrt{2D_t}\,\xi_x(t) \\
\dot{y}(t) &= v_0 \sin\phi(t) - ky(t) + \sqrt{2D_t}\,\xi_y(t) \\
\dot{\phi}(t) &= \Omega + \sqrt{2D_r}\,\eta(t)
\end{aligned}
$$

where:
- $$v_0$$ is propulsion speed  
- $$\Omega$$ is chirality  
- $$k$$ is trap strength  
- $$D_t, D_r$$ are noise strengths  

---

### Trajectories and Mean Position

Confinement modifies trajectories from free circular motion to damped oscillatory motion.

The ensemble-averaged position is:

$$
\begin{aligned}
\langle x(t) \rangle &= e^{-kt} \left[ x_0 + \frac{v_0}{k^2 + \Omega^2} (k \cos\phi_0 + \Omega \sin\phi_0) \right] \\
&\quad + \frac{v_0}{k^2 + \Omega^2} \left( k \cos(\Omega t + \phi_0) + \Omega \sin(\Omega t + \phi_0) \right)
\end{aligned}
$$

$$
\begin{aligned}
\langle y(t) \rangle &= e^{-kt} \left[ y_0 + \frac{v_0}{k^2 + \Omega^2} (k \sin\phi_0 - \Omega \cos\phi_0) \right] \\
&\quad + \frac{v_0}{k^2 + \Omega^2} \left( k \sin(\Omega t + \phi_0) - \Omega \cos(\Omega t + \phi_0) \right)
\end{aligned}
$$

<img src="{{ '/images/trajectory.png' | relative_url }}" style="width:100%;">

*Figure 1: Particle trajectories and mean position evolution under confinement.*

---

### Mean Squared Displacement (MSD)

The MSD is given by:

$$
\begin{aligned}
\mathrm{MSD}(t) &= \frac{2D_t}{k}(1 - e^{-2kt}) \\
&\quad + \frac{v_0^2}{k^2 + \Omega^2}
\left[
t - \frac{1 - e^{-kt}\cos(\Omega t)}{k}
+ \frac{\Omega}{k^2 + \Omega^2} e^{-kt}\sin(\Omega t)
\right]
\end{aligned}
$$

This shows:
- ballistic regime at short times  
- diffusive crossover  
- saturation due to confinement  

<img src="{{ '/images/msd.png' | relative_url }}" style="width:100%;">

*Figure 2: Mean squared displacement showing confinement-induced saturation.*

---

### Cross-Correlation

The full position cross-correlation is:

$$
\begin{aligned}
C_{xy}(t) &= \langle x(0)\,y(t) \rangle \\
&= \frac{v_0^2}{k^2 + \Omega^2} e^{-kt}
\left[
\sin(\Omega t) - \frac{\Omega}{k}(1 - \cos(\Omega t))
\right]
\end{aligned}
$$

This function is:
- asymmetric in time  
- exhibits phase lag  
- directly encodes chirality  

---

### Delay Function

We define the delay time as:

$$
\tau_d = \arg\max_t \, C_{xy}(t)
$$

For finite confinement:

$$
\tau_d \approx \frac{1}{\Omega} \tan^{-1}\left(\frac{\Omega}{k}\right)
$$

This reveals that:
- delay emerges from confinement  
- no inertia is required  
- $$k$$ and $$\Omega$$ jointly control the lag  

<img src="{{ '/images/delay.png' | relative_url }}" style="width:100%;">

*Figure 3: Cross-correlation and extracted delay time.*

---

### Key Insights

- Confinement induces delay in overdamped systems  
- Chirality generates time-asymmetric correlations  
- MSD saturation reflects suppressed transport  
- Delay defines a new emergent timescale  

---

- *This work demonstrates that confinement alone can generate delay in active matter systems without requiring inertia.*
