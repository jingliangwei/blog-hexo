---
title: Thermal tides in asynchronously rotating hot Jupiters
math: true
date: 2026-11-21 14:08:13
updated: 2026-11-21 14:08:13
categories:
    - planetary science
tags:
    - thermal tide
    - hot Jupiters
---

- Auclair-Desrotour, P., & Leconte, J. (2018). Semidiurnal thermal tides in asynchronously rotating hot Jupiters. *Astronomy & Astrophysics*, *613*, A45. https://doi.org/10.1051/0004-6361/201731683

<!-- more -->

## Introduction

There is no solid surface in hot Jupiters. Can the atmospheric bulge still exist?

Arras & Socrates (2010) argue for a strong thermotidal torque in the range of forcing periods $1$-$30$ days due to the propagation of resonant internal waves, which ignored the rotation of the planet and dissipative processes such as radiative cooling.

This work revisit the study by Arras & Socrates (2010) with rotation and radiative cooling.

$\text{\S}2,3$ build the analytical theory, while $\text{\S}4,5,6$ give the results.

## Tidal waves dynamics

### Setup

- A deep convective envelope + a superficial, stably stratified atmosphere
    $$
    \rho_0(p_0)={\rm e}^{-p_0/p_{\rm b}}\left(\frac{p_0}{a^2}\right) +
        \left(1-{\rm e}^{-p_0/p_{\rm b}}\right)\left(\frac{p_0}{K_c}\right)^{1/\Gamma_1} \tag{2}
    $$

- Background distributions: $p_0,\rho_0,T_0$
    mass $M(r)=4\pi\int_0^r r'^2\rho_0(r')\,{\rm d}r'$
    pressure height $H=p_0/g\rho_0$
    sound velocity $c_s=\sqrt{\Gamma_1p_0/\rho_0}$
    the Brunt-Väisälä frequency $N^2=-g\left[\dfrac{\mathrm{d}\ln\rho_0}{\mathrm{d}r}-\dfrac{1}{\Gamma_1}\dfrac{\mathrm{d}\ln p_0}{\mathrm{d}r}\right]$
    radiative frequency $\sigma_0=2\sigma_\star\left[\left(\dfrac{p_0}{p_\star}\right)^{1/2}+\left(\dfrac{p_0}{p_\star}\right)^2\right]$

- Reduced altitude
    $$
    x=\int_0^r \frac{\mathrm{d}r'}{H(r')}\tag{10}
    $$
    is also given by $x=-\ln(p_0/p_s)$

![](fig2.png)

### Structure and regimes of tidal waves

The tidal gravitational potential $U$, tidal force $\vec{F}=\nabla U$

- Primitive equations:
    momentum equation Eq. (11)
    equation of mass conservation Eq. (12)
    equation of energy Eq. (13)
    equation of perfect gas Eq. (14)

- Fourier series:
    $$
    f(t,r)=\sum_{m,\sigma} f^{m,\sigma}(x,\theta){\rm e}^{i(\sigma t+m\varphi)}\tag{15}
    $$
    the semi-diurnal tide $m=2,\sigma=2(\Omega-n_{\rm orb})$

- Perturbed equations:
    momentum equation on $\theta$ Eq. (16)
    momentum equation on $\varphi$ Eq. (17)
    momentum equation on $r$ Eq. (18)
    continuity equation Eq. (19)
    equation of energy Eq. (20) with reduced pressure fluctuation $y=\delta p/\rho_0$.

- Horizontal structure: Hough modes $\Theta(\theta)$
    $$
    f^{m,\sigma}(x,\theta)=\sum_n f_n^{m,\sigma}(x)\Theta_n^{m,\nu}(\theta)\tag{21}
    $$
    with the spin parameter $\nu(\sigma)=\dfrac{2\Omega}{\sigma}$

- Vertical structure: Eq. (18-20)
    introduce the displacement $\vec{xi}$ so that $\vec{V}=\partial_t\vec{\xi}$
    $\Rightarrow$ ODEs Eq. (31,32)

- The Lamb frequency of the $n$-mode (the cutoff frequency of horizontally propagating acoustic modes)
    $$
    \sigma_{s;n}=\sqrt{\Lambda_n}\frac{c_s}{r}\tag{39}
    $$
    The acoustic parameter comparing the tidal frequency to the Lamb frequency
    $$
    \varepsilon_{s;n}(x)=\frac{\sigma-i\Gamma_1\sigma_0}{\sigma-i\sigma_0}\frac{\sigma^2}{\sigma_{s;n}^2}\tag{40}
    $$

    The regimes of tidal waves:

    ![](fig4.png)

- A single vertical structure equation
    Eq. (31-32) $\Rightarrow$ Eq. (41) of $y=\delta p/\rho_0$
    using $y_n=\Phi_n\Psi_n$ $\Rightarrow$
    $$
    \frac{\mathrm{d}^2\Psi_n}{\mathrm{d}x^2}+\hat{k}_n^2\Psi_n=\Phi_n^{-1} C\tag{48}
    $$
    using Eq. (50) to obtain $\delta\rho_n$ from $\Psi_n$

### Thermal and gravitational forcing

The pressure at the base of the radiative atmosphere is $p_b=100$ bar,
the pressure at the base of the heated layer is $p_\star=1$ bar.

- Distribution of total heat $J_\star$ Eq. (52)
    The gravitation potential in the accelerated reference frame of the planet $U_\star$ Eq. (53)

- Fourier series
    $$
    U_\star=\sum_{l,m,\sigma} U_l^{m,\sigma}(x) P_l^m(\cos\theta) {\rm e}^{i(\sigma t+m\varphi)}\tag{54}
    $$
    $$
    J_\star=\sum_{l,m,\sigma} J_l^{m,\sigma}(x) P_l^m(\cos\theta) {\rm e}^{i(\sigma t+m\varphi)}\tag{55}
    $$

- The quadrupolar component ($l=m=2$) $U_2^{2,\sigma},J_2^{2,\sigma}$

The semi-diurnal spin parameter is $\nu=1+\dfrac{2n_{\rm orb}}{\sigma}$

### Boundary conditions

- Upper boundary: free-surface condition Eq. (65)

- Lower boundary: rigid-wall condition $\xi_r=0$ $\Rightarrow$ Eq. (61,62) at the centre of the planet.

## Tidal torque and quadrupole

- Tidal torque = density perturbation $\times$ the zonal derivative of the tidal potential
    $$
    \mathcal{T}^{m,\sigma}=\mathfrak{R}\left\{\frac{1}{2}\int_V \partial_\varphi U^{m,\sigma} (\delta\rho^{m,\sigma})^*\,{\rm d}V\right\}\tag{66}
    $$

    the semi-diurnal tidal torque
    $$
    \mathcal{T}^\sigma_{\rm SDT}=2\pi\sqrt{\frac{3}{5}}\frac{M_\star}{M_\star+M_p}n_{\rm orb}^2\mathfrak{I}\left\{Q_2^{2,\sigma}\right\}\tag{73}
    $$
    wiht the quadrupole moment
    $$
    Q_2^{2,\sigma}=\sum_n A_{n,2}^{m,\nu}\int_0^R r^4\delta\rho_n^{2,\sigma}\,{\rm d}r\tag{74}
    $$

## Properties of thermally forced tidal waves

Isolate the thermal tide by setting $U=0$. There are thermal tide and gravitational tide in the atmosphere of hot Jupiters.

- Three cases:
    1. adiabatic without rotation (same as Arras & Socrates (2010))
    2. non-adiabatic without rotation
    3. non-adiabatic with rotation

Fig. 6 displays $\mathfrak{I}\{\delta \rho\}(x,\theta)$

There is a net separation between the radiative zone and the convective interior.

## Frequency spectra of the tidal torque

$U=0$ again in this section to isolate the thermal tide.

Fig. 9: semi-diurnal torque $\mathcal{T}_{\rm SDT}$ v.s. tidal period $\tau_{\rm tide}=\dfrac{2\pi}{|\sigma|}$

![](fig9.png)

- Left panel: non-rotation, strong radiative cooling $\tau_\star=0.1$ day v.s. weaker one $\tau_\star=10$ day.
    - Small tidal periods, internal gravito-acoustic waves, restored by the fluid compressibility
    - $\tau_{\rm tide}\sim 1$-$30$ days, pure gravity waves, damped by the radiative cooling
    - Long tidal periods (zero-frequency limit), equilibrium thermal tide, $\mathcal{T}_{\rm DST}\propto\sigma$

- Right panel: $\tau_\star=1$ day, static $\Omega=0$ v.s. traditional $\Omega\neq0$
    - $\tau_{\rm tide}\sim 1$-$30$ days, super-inertial, coupled with the gravity mode $n=0$, Coriolis effects weak.
    - Long tidal periods (low frequency range), sub-inertial waves, coupled with Rossby modes, tidal response reaches plateau.

## Spin evolution

- Fig. 10: $\eta=C_{\rm therm}/C_{\rm grav}$ in the zero-frequency limit

![](fig10.png)

- The convective interior can be treated similar to the body gravitational tide,
    the synchronization time scale $\tau_{\rm syn}^{\rm CZ}$ Eq. (81) due to gravitational tidal torque;

    For radiative zone,
    the synchronization time scale $\tau_{\rm syn}^{\rm RZ}$ Eq. (82) due to semidiurnal thermal torque.

