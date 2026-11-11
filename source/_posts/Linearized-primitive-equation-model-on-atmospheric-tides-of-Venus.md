---
title: Linearized primitive equation model on atmospheric tides of Venus
math: true
date: 2026-11-10 22:16:41
updated: 2026-11-11 16:20:41
categories:
tags:
---

- Pechmann, J. B. (1983). *Thermal tides in the atmosphere of Venus* (Doctoral dissertation). California Institute of Technology. https://doi.org/10.7907/5cd0-3q63
- Staniforth, A. N., & Daley, R. W. (1977). A finite-element formulation for the vertical discretization of sigma-coordinate primitive equation models. *Monthly Weather Review*, *105*(9), 1108–1118. [https://doi.org/10.1175/1520-0493(1977)105<1108:AFEFFT>2.0.CO;2](https://doi.org/10.1175/1520-0493(1977)105<1108:AFEFFT>2.0.CO;2)

<!-- more -->

## Ch 2.1 Numerical Model

Assuming all tidal fields as small perturbations from a basic or mean state, and neglect all terms which are second order or higher in the perturbations, so this model is named **linearized primitive equation** (LPE) model.

### Basic Equations

- $\vec{V}=$ horizontal velocity vector,
    $\zeta=\hat{k}\cdot\nabla\times\vec{V}=$ vertical component of vorticity,
    $D=\nabla\cdot\vec{V}=$ horizontal divergence,
    $T=$ temperature,
    $q=\ln p_s$,
    $\Phi=gz=$ geopotential,
    vertical coordinate $\sigma=p/p_s$, vertical motion $\dot{\sigma}$
    $$
    \begin{align}
    \hat{k}\cdot\nabla\times \text{(horizontal momentum equation)}&\Rightarrow \zeta_t=\cdots\tag{2.1} \\
    \nabla\cdot \text{(horizontal momentum equation)}&\Rightarrow D_t=\cdots\tag{2.2} \\
    \text{(thermodynamic equation)}&\Rightarrow T_t=\cdots\tag{2.3} \\
    \text{(continuity equation)}&\Rightarrow q_t=\cdots\tag{2.4} \\
    \text{(hydrostatic equation)}&\Rightarrow \Phi_\sigma=\cdots\tag{2.5}
    \end{align}
    $$
- Boundary conditions
    $$
    \dot{\sigma}=0\quad{\rm at}\quad \sigma=1\quad{\rm and}\quad \sigma=0
    $$

- Replace $\Phi$ by $W=-\int_0^\sigma D\,{\rm d}\sigma$
    $$
    \begin{align}
        \zeta_t&=G\tag{2.14} \\
        \sigma W_{\sigma\sigma t}+R\nabla^2(T-\sigma T_\sigma^* q)&=\sigma H_\sigma\tag{2.15} \\
        T_t-\sigma T_\sigma^* q_t-\gamma^* W&=J\tag{2.16} \\
        q_t-W^s&=K\tag{2.17}
    \end{align}
    $$

- Perturbations:
    temperature
    $$
    T(\sigma,\lambda,\phi,t)=T^*(\sigma)+T_1(\sigma,\lambda)+T'(\sigma,\lambda,\phi,t)
    $$
    zonal wind
    $$
    u=a\cos[\lambda\Omega(\sigma,\lambda)]+u'(\sigma,\lambda,\phi,t)
    $$
    meridional wind
    $$
    v=v'(\sigma,\lambda,\phi,t)
    $$

- Adding thermal forcing $Q'$ and dissipation of Rayleigh friction $\tau_{\rm R}$ and Newtonian cooling $\tau_{\rm N}$
    $$
    \begin{align}
        \zeta'_t+\zeta'/\tau_{\rm R}&=G' \tag{2.18}\\
        \sigma W'_{\sigma\sigma t}+\sigma (W'_\sigma/\tau_{\rm R})_\sigma+R\nabla^2(T'-\sigma T_\sigma^*q')&=\sigma H_\sigma'\tag{2.19} \\
        T'_t-\sigma T_\sigma^*q_t'+T'/\tau_{\rm N}-\sigma T_\sigma^*q'/\tau_{\rm N}-\gamma^*W'&=J'+Q'\tag{2.20} \\
        q_t'-{W^s}'&=K'\tag{2.21}
    \end{align}
    $$

### Discretization in Time

- Define notation
    $$
    \bar{F}^t=\frac{F|_{t+\Delta t}+F|_{t-\Delta t}}{2}
    $$
    $$
    F_t=\frac{F|_{t+\Delta t}-F|_{t-\Delta t}}{2\Delta t}
    $$

### Horizontal Discretization

- Using spherical harmonics
    $$
    F'(\sigma,\lambda,\phi,t)=\sum_{n=m}^N F_n'(\sigma,t)P_n^m(\lambda){\rm e}^{im\phi}
    $$
    then components with different zonal wavenumber $m$ will not interact.
    Solve for diurnal fields $m=1$, semidiurnal $m=2$ independently.

- At each time step, for each $n$, solve an elliptic boundary value problem in $\bar{W}_n^t$. Eq. (2.34)

### Vertical Discretization

- Using Châpeau basis functions $e^i(\sigma)$
    $$
    \bar{W}_n^t=\sum_{i=1}^{\text{NVPTS}}(\bar{W}_n^t)_i e^i(\sigma)
    $$
    with the number of vertical points $\text{NVPTS}$, $\sigma_1=0,\sigma_{\text{NVPTS}}=1$.

    Eq. (2.35) $\rightarrow$ Matrix form

### Method of Solution

To separating the forced solution from the stable free modes.

- Using a solar-fixed reference frame,
    increase the amplitude of the forced solution as a function of time.

    E.g.
    $$
    \frac{\partial u}{\partial t}+i\omega u=F\Rightarrow u(t)=\frac{F}{i\omega}(1-{\rm e}^{-i\omega t})
    $$
    will never converge to $F/i\omega$.
    $$
    \frac{\partial v}{\partial t}+i\omega v=Ft\Rightarrow v(t)=\frac{F}{i\omega}\left(t-\frac{1}{i\omega}(1-{\rm e}^{-i\omega t})\right)
    $$
    $v/t\rightarrow F/i\omega$ when $t\rightarrow\infty$.

## Ch 2.4 The Gravity Wave Model

- Assume the horizontal structure ${\rm e}^{ikx}$, and ignore the latitude dependence.
    Only valid near the equator.

    Eq. (2.18)-(2.21) $\Rightarrow$ Eq. (2.36)-(2.39)

## Ch 2.5 Conservation of Energy

- Eq. (2.37) Divergence $W$ $\Rightarrow$ Eq. (2.45)
    $$
    \begin{aligned}
    \frac{p_s}{gk^2}\Bigg\{
        \overbrace{
        \int_0^1\frac{1}{2}\frac{\partial}{\partial t}\left|\frac{\partial W'}{\partial \sigma}\right|^2 +
        \frac{k^2RT^*|_{\sigma=1}}{2}\frac{\partial|q'|^2}{\partial t}
        }^{\text{change rate of the perturbation kinetic energy}} +
        \overbrace{
        \int_0^1\frac{1}{\tau_{\rm R}}\left|\frac{\partial W'}{\partial \sigma}\right|^2{\rm d}\sigma
        }^{\text{kinetic energy loss due to Rayleigh friction}}  \\
        {}+
        \underbrace{
        {\rm Re}\int_0^1\frac{Rk^2}{\sigma}\langle W'\rangle\Pi'{\rm d}\sigma
        }_{\text{conversion from kinetic to thermal energy}} -
        \underbrace{
        {\rm Re}\int_0^1ik\dot{\sigma}'\frac{\partial\langle W'\rangle}{\partial \sigma}\frac{\partial u^*}{\partial \sigma}{\rm d}\sigma
        }_{\text{conversion from perturbation to mean energy}}=0
    \Bigg\}
    \end{aligned}
    \tag{2.45}
    $$

- Eq. (2.38) Thermodynamic $T$ $\Rightarrow$ Eq. (2.46)
    $$
    \begin{aligned}
    \frac{p_s}{g}{\rm Re}\int_0^1\Bigg\{
        \overbrace{
        \frac{1}{2}\frac{R}{\gamma^*\sigma}\frac{\partial}{\partial t}|\Pi'|^2
        }^{\text{change rate of thermal perturbation energy}}
        +
        \overbrace{
        \frac{1}{\tau_{\rm N}}\frac{R}{\gamma^*\sigma}|\Pi'|^2
        }^{\text{energy loss due to Newtonian cooling}}
        -
        \overbrace{
        \frac{R}{\sigma}\langle\Pi'\rangle W'
        }^{\text{conversion term}}
        \\
        {}-
        \underbrace{
        ik\frac{\langle\Pi'\rangle q'}{\sigma}(\sigma u^*-\hat{u}^*-\hat{u}^{*\sigma})
        }_{\text{conversion between perturbation and mean energy}}
        -
        \underbrace{
        \frac{R}{\gamma^*\sigma}\langle\Pi'\rangle Q'
        }_{\text{energy supplied by the forcing}}
    \Bigg\}{\rm d}\sigma=0
    \end{aligned}
    \tag{2.46}
    $$
