<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>
    
<script type="text/javascript"
        src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

# Unit 3: Theory of Vibrations

- [Introduction to Theory of Vibrations](#31-introduction-to-theory-of-vibrations)  
- [Sources of Vibrations](#32-sources-of-vibrations)  
- [Types of Vibrations](#33-types-of-vibrations)  
- [Degree of Freedom](#34-degree-of-freedom)  
- [Spring Action and Damping](#35-spring-action-and-damping)  
- [Equation of Motion of SDOF Systems](#36-equation-of-motion-of-sdof-systems)  
- [Undamped and Damped Systems under Transient Forces](#37-undamped-and-damped-systems-under-transient-forces)  
- [General Solution and Green’s Function](#38-general-solution-and-greens-function)  

## 3.1 Introduction to Theory of Vibrations  

**Vibration** is the **oscillatory motion** of a body about its equilibrium position.  
In earthquake engineering, vibration theory provides the foundation to understand how structures respond to ground motion.  

📌 **Engineering Relevance**  
- Earthquake loads are *dynamic* → structures vibrate.  
- Analysis of vibrations helps predict:  
  * Natural frequencies  
  * Mode shapes  
  * Response under dynamic loading (earthquakes, wind, machines)  

<iframe width="560" height="315" src="https://www.youtube.com/embed/vuWHzzZBuUc" title="YouTube video player" frameborder="0" allowfullscreen></iframe>  

## 3.2 Sources of Vibrations  

Vibrations in civil structures arise from:  

- **Natural Sources**  
  * Earthquakes 🌍  
  * Wind loading 🌬️  
  * Ocean waves 🌊  

- **Anthropogenic / Man-made Sources**  
  * Machine foundations (motors, turbines) ⚙️  
  * Traffic and railways 🚆  
  * Blasting, pile driving, construction activities 🏗️  

## 3.3 Types of Vibrations  

| **Type**           | **Description**                                                                 | **Example** |
|--------------------|---------------------------------------------------------------------------------|-------------|
| **Free Vibration** | System vibrates on its own after initial disturbance. No external force acts.   | A pendulum released from rest. |
| **Forced Vibration** | System vibrates under continuous external excitation.                          | Building subjected to wind or earthquake. |
| **Damped Vibration** | Amplitude decreases with time due to energy dissipation.                      | Car suspension system. |
| **Undamped Vibration** | Ideal case, no energy loss. Amplitude remains constant.                       | Theoretical spring–mass system. |
| **Transient Vibration** | Short-duration disturbance, response dies after some time.                  | Blast load on a structure. |
| **Steady-State Vibration** | Response matches excitation frequency (important in resonance studies). | Rotating machines. |

## 3.4 Degree of Freedom (DOF)  

- **Definition**: The **minimum number of independent coordinates** needed to describe the motion of a system.  
- **Examples**:  
  * A simple pendulum → 1 DOF (angle $\theta$).  
  * A rigid body in plane motion → 3 DOF.  

📌 **Importance in Structural Engineering**  
- Simplifies modeling.  
- Most earthquake analyses use **SDOF (Single Degree of Freedom)** or **MDOF (Multi-DOF)** models.  

<img width="450" src="https://github.com/user-attachments/assets/placeholder-DOF.png" />  

## 3.5 Spring Action and Damping  

- **Spring Action**: Restoring force proportional to displacement.  
  $$
  F_s = kx
  $$  
  where $k =$ stiffness, $x =$ displacement.  

- **Damping**: Resistance that reduces vibration amplitude by dissipating energy.  

  | **Type of Damping** | **Description** | **Example** |
  |----------------------|-----------------|-------------|
  | **Viscous Damping** | Force proportional to velocity: $F_d = c \dot{x}$ | Shock absorbers |
  | **Coulomb Damping** | Constant friction force, independent of velocity | Sliding surfaces |
  | **Structural Damping** | Energy loss within material | Concrete/steel structures |

## 3.6 Equation of Motion of SDOF Systems  

For a **spring–mass–damper system** under external force $F(t)$:  

<img width="400" src="https://github.com/user-attachments/assets/placeholder-springmass.png" />  

Equation:  

$$
m \ddot{x}(t) + c \dot{x}(t) + kx(t) = F(t)
$$

Where:  
- $m$ = mass  
- $c$ = damping coefficient  
- $k$ = stiffness  
- $x(t)$ = displacement  
- $F(t)$ = external force  

## 3.7 Undamped and Damped Systems under Transient Forces  

1. **Undamped Free Vibration** ($c=0$, $F(t)=0$):  
   $$
   m \ddot{x} + kx = 0
   $$  
   Solution:  
   $$
   x(t) = A \cos(\omega_n t) + B \sin(\omega_n t)
   $$  
   with $\omega_n = \sqrt{\tfrac{k}{m}}$ (natural frequency).  

2. **Damped Free Vibration** ($F(t)=0$):  
   $$
   m \ddot{x} + c \dot{x} + kx = 0
   $$  

   - Define **damping ratio**:  
     $$
     \zeta = \frac{c}{2 \sqrt{km}}
     $$  

   - Three cases:  
     * $\zeta < 1$ → underdamped (oscillatory decay)  
     * $\zeta = 1$ → critical damping (fastest return to equilibrium)  
     * $\zeta > 1$ → overdamped (no oscillation, slow return)  

3. **Forced/Transient Vibration**:  
   - System subjected to earthquake-like pulse or dynamic load.  
   - Response depends on **resonance**, damping, and force duration.  

## 3.8 General Solution and Green’s Function  

- The **general solution** of the SDOF equation combines:  
  * **Homogeneous solution** (free vibration)  
  * **Particular solution** (forced vibration)  

- **Green’s Function**:  
  A mathematical tool representing the system’s **impulse response**.  
  If $g(t,\tau)$ is Green’s function, then the response is:  

  $$
  x(t) = \int_0^t g(t-\tau)\, F(\tau) \, d\tau
  $$  

  📌 *Interpretation*: Response at time $t$ depends on the **history of applied forces**.  

---
