---
title: Coupling of dynamical tide and orbital motion
math: true
date: 2026-11-22 15:51:45
updated: 2026-11-26 19:31:00
categories:
    - planetary science
tags:
    - tide
    - orbital evolution
---

- Wei, X. (2025). Coupling of dynamical tide and orbital motion. *The Astrophysical Journal*, *981*(1), Article 1. https://doi.org/10.3847/1538-4357/adb1e5

- Wei, X. (2019). Surface tide on a rapidly rotating body. *Monthly Notices of the Royal Astronomical Society*, *484*, 3017–3021. https://doi.org/10.1093/mnras/stz187

<!-- more -->

---

- f-mode: surface gravity waves due to gravity with a free surface
    g-mode: internal gravity waves due to buoyancy force with stratification
    r-mode: inertial waves due to Coriolis force with rotation

## Mathematical Model

Wei (2025)

- Orbital evolution:
    $$
    \frac{\mathrm{d}L_o}{\mathrm{d}t}=-\frac{\langle D\rangle}{\omega_0-\omega_1},
    \frac{\mathrm{d}L_1}{\mathrm{d}t}=\frac{\langle D\rangle}{\omega_0-\omega_1},
    \frac{\mathrm{d}(E_o+E_1)}{\mathrm{d}t}=-\langle D\rangle
    \tag{W25.2}
    $$
    with $L_o=M_2[GM_1a(1-e^2)]^{1/2}$ is the orbital angular momentum,
    $L_1=I_1\omega_1$ is the primary's spin angular momentum,
    $E_o=-GM_1M_2/(2a)$ is the orbital energy,
    and $E_1=I_1\omega_1^2/2$ is the primary's spin energy.

- The orbit average dissipation $\langle D\rangle=\frac{1}{2\pi}\int_0^{2\pi} D\,{\rm d}\theta$ 
    $$
    \langle D\rangle=\frac{D_0}{(1-e^2)^6}\left(1+\frac{15}{2}e^2+\frac{45}{8}e^4+\frac{5}{16}e^6\right)\tag{W25.3}
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
    \tag{W25.4}
    $$
    with free-surface condition ${\rm d}\eta/{\rm d}t=u_r$,
    Rayleigh drag $-\alpha u_\theta$,$-\alpha u_\phi$,
    time-periodic tidal potential $V$,
    self-gravity potential $\Psi$.

    And the dynamical tidal dissipation
    $$
    D_0=\int_\Omega \rho\alpha(u_\theta^2+u_\phi^2)\,{\rm d}\Omega\tag{W25.5}
    $$

## Numerical solution for fluid

Wei (2019)

- Expansion for $u_\theta,u_\phi,\eta,\Psi$
    $$
    \eta=\mathfrak{R}\left[\sum_{n,m}\hat{\eta} P_n^m(\cos\theta) {\rm e}^{im(\phi-\omega t)}\right] \tag{W19.3}
    $$

- Dimensionless equations:
    $$
    \begin{array}{l}
    \epsilon\dfrac{\partial u_\theta}{\partial t}+\sqrt{\epsilon}\gamma u_\theta-2\epsilon\cos\theta u_\phi+a\dfrac{\partial\eta}{\partial\theta}=\dfrac{\partial V}{\partial\theta}; \\[7pt]
    \epsilon\dfrac{\partial u_\phi}{\partial t}+\sqrt{\epsilon}\gamma u_\phi+2\epsilon\cos\theta u_\theta+\dfrac{a}{\sin\theta}\dfrac{\partial\eta}{\partial\phi}=\dfrac{1}{\sin\theta}\dfrac{\partial V}{\partial \phi}; \\[7pt]
    \dfrac{\partial \eta}{\partial t}+\dfrac{h}{\sin\theta}\left[\dfrac{\partial}{\partial\theta}(u_\theta\sin\theta)+\dfrac{\partial u_\phi}{\partial\phi}\right]=0.
    \end{array}\tag{W19.4}
    $$
    here normalizing length with $R$,
    time with rotational timescale $\Omega^{-1}$,
    velocity with $\Omega R$,
    tidal potential with $gR$,
    and $\gamma$ (Rayleigh drag) with dynamical frequency $\sqrt{g/R}$.
    The parameter $\epsilon=\Omega^2 R/g$ represents the relative strength of rotation.

- In Eq. (W19.4), the longitude wavenumber $m$ can be decoupled
    but the Coriolis force couples the colatitude wavenumber $n$.
    A linear system
    $$
    \begin{array}{l}
    \displaystyle \sum_{n=m}^{m+N-1} \left[(\sqrt{\epsilon}\gamma-i\epsilon m\omega)P_n^m\hat{u}_\theta - 2\epsilon\cos\theta P_n^m\hat{u}_\phi + a\frac{\mathrm{d}P_n^m}{\mathrm{d}\theta}\hat{\eta}\right] = \hat{V}\frac{\mathrm{d}P_{n_0}^m}{\mathrm{d}\theta}, \\[7pt]
    \displaystyle \sum_{n=m}^{m+N-1} \left[2\epsilon\cos\theta P_n^m\hat{u}_\theta + (\sqrt{\epsilon}\gamma-i\epsilon m\omega)P_n^m\hat{u}_\phi + \frac{ima}{\sin \theta}P_n^m\hat{\eta}\right] = \frac{im}{\sin\theta}\hat{V}P_{n_0}^m, \\[7pt]
    \displaystyle \sum_{n=m}^{m+N-1} \left[\frac{h}{\sin\theta}\frac{\mathrm{d}}{\mathrm{d}\theta}(\sin\theta P_n^m)\hat{u}_\theta + \frac{ihm}{\sin\theta}P_n^m\hat{u}_\phi - im\omega P_n^m\hat{\eta}\right] = 0.
    \end{array}\tag{W19.5}
    $$
    for semi-diurnal tide $n_0=2$.
    $P_n^m=0$ for $n<m$.
    collocate on the $N$ zeros of $P_{m+N}^m$ to obtain a linear system $\boldsymbol{A}x=\boldsymbol{b}$ with a $3N$-by-$3N$ matrix $\boldsymbol{A}$
