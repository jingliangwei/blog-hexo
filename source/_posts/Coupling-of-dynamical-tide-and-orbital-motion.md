---
title: Coupling of dynamical tide and orbital motion
math: true
date: 2026-11-22 15:51:45
updated: 2026-11-22 15:51:45
categories:
    - planetary science
tags:
    - tide
    - orbital evolution
---

- Wei, X. (2025). Coupling of dynamical tide and orbital motion. *The Astrophysical Journal*, *981*(1), Article 1. https://doi.org/10.3847/1538-4357/adb1e5

<!-- more -->

## Mathematical Model

- Orbital evolution:
    $$
    \frac{\mathrm{d}L_o}{\mathrm{d}t}=-\frac{\langle D\rangle}{\omega_0-\omega_1},
    \frac{\mathrm{d}L_1}{\mathrm{d}t}=\frac{\langle D\rangle}{\omega_0-\omega_1},
    \frac{\mathrm{d}(E_o+E_1)}{\mathrm{d}t}=-\langle D\rangle
    \tag{2}
    $$
    with $L_o=M_2[GM_1a(1-e^2)]^{1/2}$ is the orbital angular momentum,
    $L_1=I_1\omega_1$ is the primary's spin angular momentum,
    $E_o=-GM_1M_2/(2a)$ is the orbital energy,
    and $E_1=I_1\omega_1^2/2$ is the primary's spin energy.

- The orbit average dissipation $\langle D\rangle=\frac{1}{2\pi}\int_0^{2\pi} D\,{\rm d}\theta$ 
    $$
    \langle D\rangle=\frac{D_0}{(1-e^2)^6}\left(1+\frac{15}{2}e^2+\frac{45}{8}e^4+\frac{5}{16}e^6\right)\tag{3}
    $$

- Shallow water model
    $$
    \left\{
    \begin{array}{l}
    \dfrac{\partial u_\theta}{\partial t}-2\omega_1\cos\theta u_\phi=\dfrac{1}{R_1}\dfrac{\partial}{\partial\theta}(-g\eta+V+\Psi)-\alpha u_\theta \\
    \dfrac{\partial u_\phi}{\partial t}+2\omega_1\cos\theta u_\theta=\dfrac{1}{R_1\sin\theta}\dfrac{\partial}{\partial\phi}(-g\eta+V+\Psi)-\alpha u_\phi \\
    \dfrac{\partial \eta}{\partial t}+\dfrac{h}{R_1\sin\theta}\left(\dfrac{\partial}{\partial\theta}(u_\theta\sin\theta)+\dfrac{\partial u_\phi}{\partial\phi}\right)=0
    \end{array}
    \right.
    \tag{4}
    $$
    with free-surface condition ${\rm d}\eta/{\rm d}t=u_r$,
    Rayleigh drag $-\alpha u_\theta$,$-\alpha u_\phi$,
    time-periodic tidal potential $V$,
    self-gravity potential $\Psi$.

    And the dynamical tidal dissipation
    $$
    D_0=\int_\Omega \rho\alpha(u_\theta^2+u_\phi^2)\,{\rm d}\Omega\tag{5}
    $$
