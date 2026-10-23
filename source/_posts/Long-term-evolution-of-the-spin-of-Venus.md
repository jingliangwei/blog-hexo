---
title: Long-term evolution of the spin of Venus
math: true
disableNunjucks: true
date: 2026-10-21 20:08:14
updated: 2026-10-23 16:14:14
categories:
    - planetary science
tags:
    - gravitational tide
    - thermal tide
    - spin-orbit resonance
---

- Correia, A. C. M., Laskar, J., & Néron de Surgy, O. (2003). Long-term evolution of the spin of Venus: I. Theory. *Icarus*, *163*(1), 1–23. https://doi.org/10.1016/S0019-1035(03)00042-3
- Goldreich, P., & Peale, S. (1966). Spin-orbit coupling in the solar system. *The Astronomical Journal*, *71*(6), 425–438. https://doi.org/10.1086/109947

<!-- more -->

## Introduction

Was Venus born retrograde or not?

Gold and Soter (1969) introduce thermal atmospheric tide to balance the gravitational tide, but can not prevent Venus' spin axis from rolling over to a prograde orientation.

Taking into account the dissipation of tides (both gravitational and thermal) and core-mantle friction, still required high values of the initial obliquity.

Laskar and Robutel (1993) discovered chaotic zone for Venus.

Correia and Laskar (2001) confirmed the present spin state of Venus is the most probable for almost any initial condition.

## The secular variations of Venus' spin axis

| Parameters | Expression |
|:---|:---|
| moments of inertia | $A\le B<C$ |
| canonical Andoyer's action variables | $(L,X)$ |
| angular momentum on the $C$ axis | $L=C\omega$ |
| angular momentum to the ecliptic | $X\simeq L\cos\varepsilon$ |
| the obliquity | $\varepsilon$ |
| their conjugate angles | $(\ell,-\psi)$ |
| the hour angle | $\ell$ |
| the general precession angle | $\psi$ |

- The averaged Hamiltonian $\bar{\mathcal{H}}$ (Eq. 1) contains
    the spin energy + the precession energy + the spin-orbit energy in the synchronous resonance + the planetary perturbations

- The conservative equations for precession:
    the Hamilton's equations to the Andoyer variables $(X,-\psi)$ give the evolution of $X$ and $\Psi=L\sin \varepsilon\,e^{i\psi}$
    hence the evolution of the obliquity $\varepsilon$

- Spin-orbit resonance:
    - the Hamilton's equations to $(L,\ell)$ give the evolution of rotation rate $\omega$ (Eq. 9)
        and the pendulum-like equation gives the width of resonance $\Delta\omega$ as (Eq. 10)
    - capture probabilities $P_{\rm cap}$ in (Eq. 13)
        illustration from Goldreich and Peale (1966) $P_{\rm cap}=\delta E/\Delta E$

        ![](capture_probabilities.png)
        ![](capture_probabilities2.png)
    - escape probabilities $P^+,P^-$ in (Eq. 15)

## Dissipative effects

### Gravitational tides

- The attraction of the Sun from the center of mass of Venus expressed using Legendre polynomials
    $$
    V^{\rm g}=\sum_{l=2}^\infty V_l^{\rm g}=-\frac{Gm_\odot}{r_\odot}\sum_{l=2}^\infty\left(\frac{r}{r_\odot}\right)^l P_l(\cos S)\tag{17}
    $$
- The tidal potential due to the distortion of the planet
    $$
    U^{\rm g}=\sum_{l=2}^\infty U_l^{\rm g}\tag{18}
    $$
- The Love number $k_l$ is defined by $U_l^{\rm g}=k_l V_l^{\rm g}$
- The phase lag $\delta^{\rm g}(\sigma)$ and the time lag $\Delta t^{\rm g}(\sigma)$
    $$
    \delta^{\rm g}(\sigma)=\frac{\sigma \Delta t^{\rm g}(\sigma)}{2}\tag{20}
    $$
    with the tidal frequency $\sigma$ (a linear combination of rotation rate $\omega$ and mean motion $n$)
- The torque:
    $$
    \left\{
    \begin{array}{l}
    \displaystyle \frac{{\rm d}L}{{\rm d}t}=-\frac{Gm_\odot^2 R^5}{a^6}\sum_\sigma b^{\rm g}(\sigma)\,\Lambda_\sigma^{\rm g}\left(\frac{X}{L},e\right) \\
    \displaystyle \frac{{\rm d}X}{{\rm d}t}=-\frac{Gm_\odot^2 R^5}{a^6}\sum_\sigma b^{\rm g}(\sigma)\,\Xi_\sigma^{\rm g}\left(\frac{X}{L},e\right)
    \end{array}
    \right.
    \tag{21}
    $$
- The factor $b^{\rm g}(\sigma)$
    $$
    b^{\rm g}(\sigma)=k_2\sin [2\delta^{\rm g}(\sigma)]=k_2\sin[\sigma\,\Delta t^{\rm g}(\sigma)]\tag{24}
    $$
    $$
    b^{\rm g}(\sigma)={\rm sign}(\sigma)\frac{k_2}{\sqrt{Q_\sigma^2+1}}\simeq{\rm sign}(\sigma)\frac{k_2}{Q_\sigma}\tag{26}
    $$
- The quality factor $Q$ ("specific" dissipation)
    $$
    Q_\sigma=\frac{2\pi E}{\Delta E}=\cot [2\delta^{\rm g}(\sigma)]\tag{25}
    $$
    where $E$ is the total tidal energy stored in the planet
    and $\Delta E$ is the energy dissipated per cycle.

The relations of $\delta^{\rm g}$, $\Delta t^{\rm g}$, $Q_\sigma$ with the tidal frequency $\sigma$ are unknown.
So different models are considered.

- *The constant-$Q$ model*
    $$
    b^{\rm g}(\sigma)={\rm sign}(\sigma)\frac{k_2}{Q}\tag{27}
    $$
- *The viscous model (or "weak friction" model)*: constant-time-lag $\Delta t$ for $\sigma\Delta t\ll1$
    $$
    b^{\rm g}(\sigma)=k_2\sin(\sigma\Delta t)\simeq k_2\sigma\Delta t\tag{28}
    $$
- *Interpolated model*
    $$
    b^{\rm g}(\sigma)={\rm sign}(\sigma)\frac{k_2}{Q}[1-(1-Q/Q_n)^{|\sigma|/n}]\tag{29}
    $$

### Thermal atmospheric tides

- The gravitational potential in the atmosphere
    $$
    V^{\rm a}=-G\int_{(\mathcal{M})}\frac{{\rm d}\mathcal{M}}{|\vec{r}-\vec{r}'|}\tag{30}
    $$
    express the density $\rho_{\rm a}$ in the atmosphere mass element ${\rm d}\mathcal{M}$ by the surface pressure $p_s$, we have
    $$
    V^{\rm a}=-\frac{1}{\bar{\rho}}\sum_{l=0}^{+\infty}\frac{3}{2l+1}\tilde{p}_l\left(\frac{R}{r}\right)^{l+1}P_l(\cos S)\tag{34}
    $$
- The semidiurnal terms ($l=2$)
    $$
    U^{\rm a}=-\frac{3}{5}\frac{\delta\tilde{p}}{\bar{\rho}}\left(\frac{R}{r}\right)^3P_2(\cos S)\tag{35}
    $$
    where $\delta\tilde{p}\equiv \tilde{p}_2$
- The torque:
    $$
    \left\{
    \begin{array}{l}
    \displaystyle \frac{{\rm d}L}{{\rm d}t}=-\frac{3m_\odot R^3}{5\bar{\rho}a^3}\sum_\sigma b^{\rm a}(\sigma)\,\Lambda_\sigma^{\rm a}\left(\frac{X}{L},e\right) \\
    \displaystyle \frac{{\rm d}X}{{\rm d}t}=-\frac{3m_\odot R^3}{5\bar{\rho}a^3}\sum_\sigma b^{\rm a}(\sigma)\,\Xi_\sigma^{\rm a}\left(\frac{X}{L},e\right)
    \end{array}
    \right.
    \tag{36}
    $$
- The factor $b^{\rm a}(\sigma)$ is now
    $$
    b^{\rm a}(\sigma)=\delta\tilde{p}(\sigma)\sin[2\delta^{\rm a}(\sigma)]=\delta\tilde{p}(\sigma)\sin[\sigma\Delta t^{\rm a}(\sigma)]\tag{38}
    $$
    the amplitudes of the pressure variations on the ground $\delta\tilde{p}(\sigma)=|\delta\tilde{p}(\sigma)|e^{\pm i(\pi/2)}$ add a supplementary phase lag of $\pm \pi/2$, so that
    $$
    b^{\rm a}(\sigma)=-|\delta\tilde{p}(\sigma)|\sin[2\delta^{\rm a}(\sigma)]\tag{42}
    $$

- *"heating at the ground" model*: give a expression for $\delta\tilde{p}(\sigma)$
    $$
    \delta\tilde{p}(\sigma)=i\frac{5}{16}\frac{\gamma}{|\sigma|}\frac{gF_s}{c_p\bar{T}_s}\tag{44}
    $$
- *interpolating function model*:
    $$
    \delta\tilde{p}(\sigma)=i\frac{5}{16}\frac{\gamma}{|\sigma|}\frac{gF_s}{c_p\bar{T}_s}(1-e^{-10^3(2\sigma/n)^2})\tag{46}
    $$

### Core-mantle friction

- The main torques:
    1. $\vec{N}$, nonradial inertial pressure forces of the mantle over the core;
    2. viscous friction;
    3. electromagnetic friction;

- Effective friction effect $\vec{\Phi}$ depends only on one parameter $\kappa$
    $$
    \vec{\Phi}\simeq-\kappa(\vec{\omega}_c-\vec{\omega})=-\kappa\vec{\delta}\tag{47}
    $$

- The inertial torque
    $$
    \vec{N}=\vec{\omega}_c\times\vec{L}_c-\vec{P}_c\tag{48}
    $$
    rotation-inertia (free-precession) tendency + external precessional torque

- The evolution of the core-mantle system (Eq. 49)
- The secular evolution of the spin of Venus (Eq. 52)

- The effective friction coupling constant $\kappa$:
    - laminar case $\kappa({\rm lam.})$
    - turbulent case $\kappa({\rm turb.})$

## Dynamical evolution

### Obliquity calculus

The evolution of the obliquity $\varepsilon$
- for the CMF effect (Eq. 60)
- for tidal effects (Eq. 61)
- for planetary perturbations (Eq. 63)

### Tidal effects

- The gravitational tides alone lead the planet's spin to the synchronous state ($\omega=n,\varepsilon=0$)

    ![](grav_tide_effect.png)

- The thermal atmospheric tides alone

    ![](thermal_tide_effect.png)

### CMF effects

![](cmf_effect.png)

- CMF v.s. tidal effect:
    dimensionless parameter $\varrho$
    $$
    \varrho=\frac{\beta}{\xi n^{5/2}}\tag{82}
    $$
    with $\beta$ the core-mantle friction parameter in Eq. 77
    $\xi=\dfrac{3Gm_\odot^2 R^5}{Ca^6}\dfrac{k_2}{Q_n}$ the strength of the tides in Eq. 65

### Evolution final states

In this section, they assume the present measured period $\mathcal{P}_{o}=243.0185\pm0.0001$ days is a final state and do not consdier the planetary perturbations.

- Obliquity final states:
    In the slow rotation regime ($\omega\sim n$), CMF effect controls the obliquity evolution,
    there are only two stable positions $\varepsilon=0^\circ$ and $\varepsilon=180^\circ$.
    The critical point is $\varepsilon=90^\circ$.

- Rotation final states:

    ![](four_final_rotation_states.png)

    letting ${\rm d}\omega/{\rm d}t=0$ for $\varepsilon=0,\pi$ give the retrograde state with $\mathcal{P}^-=243.02$ days and the direct state with $\mathcal{P}^+=76.83$ days.

- Error to the final direct rotation rate:
    $$
    \delta \mathcal{P}^+_{\rm f}\simeq\left(\frac{\mathcal{P}^+_{\rm f}}{\mathcal{P}_o}\right)^2\delta\mathcal{P}_o\simeq\frac{\delta\mathcal{P}_o}{10}\tag{93}
    $$

- Phase lags and $Q$ factor:
    the relation of $\delta^{\rm g}$, $\delta^{\rm a}$ and $Q_\sigma$

- Atmospheric tides dissipation model
    assume the time lag ratio $\Delta t^{\rm a}(\sigma)/\Delta t^{\rm g}(\sigma)$ fixed with the tidal frequency

    ![](fig6.png)

- Relation among the tidal dissipation $Q$, the initial rotation rate $\omega_{\rm i}$ and the time needed to reach a final state $\Delta t_{\rm f}$
    Eq. 103 valid before reach the slow rotation regime at $t=t_{\rm r}$
    estimate $\Delta t_{\rm f}=t_{\rm r}-t_{\rm i}$
    $$
    \Delta t_{\rm f}\simeq Q\omega_{\rm i}/c \tag{105}
    $$

### Effect of the planetary perturbations

The planetary perturbations lead to a forced obliquity
$$
\varepsilon=\varepsilon_e+\delta \varepsilon\tag{106}
$$
$\delta \varepsilon$ leads to CMF effect in (Eq. 79)
so that a modified of (Eq. 102) is Eq. 107
${\rm d}\omega/{\rm d}t=0$ gives
$$
|\delta\omega|=n\varrho\left(\frac{n}{|\omega|}\right)^{5/2}\delta\varepsilon^2\tag{110}
$$

### Formation of the atmosphere

Without atmosphere, Venus evolve to a synchronous or near-synchronous rotation equilibrium.
After formation of atmosphere, Venus evolve toward one of the four final states, but the probability of states depends on the formation time of atmosphere.

