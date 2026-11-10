---
title: Heating at the ground model
math: true
date: 2026-11-02 19:38:44
updated: 2026-11-02 19:38:44
categories:
    - planetary science
tags:
    - thermal tide
---

- Dobrovolskis, A. R., & Ingersoll, A. P. (1980). Atmospheric tides and the rotation of Venus: I. Tidal theory and the balance of torques. *Icarus*, *41*(1), 1–17. https://doi.org/10.1016/0019-1035(80)90156-6

<!-- more -->

## Introduction

- Body gravitational tide -> synchronous state
- Earth's torque much weaker than solar body tide
- Atmosphere thermal tide to balance

![](fig1.png)

## Numerical calculations

- Three major difficulties:
    1. uncertainties in the basic state;
    2. ignorance of the heating distribution;
    3. nonseparability of the tidal equations in latitude and height.

### Governing equations

- The governing equations:

    | Parameters | Expression |
    |:---|:---|
    | $\theta$ | colatitude |
    | $\phi$ | longitude |
    | $x=-\ln(p/\bar{p}_0)$ | "height" |
    | $t$ | time |
    | $a$ | radius of Venus |
    | $\omega_\text{V}$ | sidereal rotation rate of Venus |
    | $\Omega$ | the tidal potential |
    | $\psi=gz+\Omega$ | total geopotential |
    | $\eta={\rm d}x/{\rm d}t$ | vertical velocity |
    | $u=a({\rm d}\theta/{\rm d}t)_p$ | north-south velocity / meridional velocity |
    | $v=a\sin\theta({\rm d}\phi/{\rm d}t)_p$ | east-west velocity / zonal velocity |

    mean part + variation

    $$
    \psi(\theta,x,\phi,t)=\bar{\psi}(\theta,x)+{\rm Re}\sum_{\sigma,s}\delta\psi^{\sigma,s}(\theta,x)\,e^{i(\sigma_{\rm V}t+s\phi)}\tag{2}
    $$
    with angular time frequency of a point fixed on the surface $\sigma_{\rm V}$,
    zonal wavenumber $s$.

    The mean rotation rate of the atmosphere $\omega$ and the Doppler-shifted tidal frequency $\sigma$
    $$
    \begin{aligned}
    \omega(\theta,x)&=\omega_{\rm V}+\overline{\mathrm{d}\phi}/{\rm d}t=\omega_{\rm V}+\bar{v}/a\,\sin\theta, \\
    \sigma(\theta,x)&=\sigma_{\rm V}+s\bar{v}/a\,\sin\theta
    \end{aligned}
    \tag{3}
    $$

    Eq. (4): hydrostatic/heat equation = solar heating $\kappa\delta J$ + heat transport (stratification $\Gamma$, horizontal winds)
    with $\kappa=R/c_p\approx 0.20$

- The classical theory for Earth:
    separation of variables in latitude and height.

    The horizontal structure: Hough modes $\Theta_l^{\sigma,s}$ with eigenvalues $h_l^{\sigma,s}$ so-called the equivalent depths

    Then the four linearized equations (hydrostatic/heat + continuity + zonal/meridional momentum) $\xrightarrow{\text{eliminate}\ \delta u\ {\rm and}\ \delta v}$ Eq. (6,7): solar heating $\delta J_l$, vertical velocity $\delta\eta_l$, geopotential $\delta\psi_l$

- EGM (equivalent gravity mode):
    height-dependent equivalent depth $h_l^{\sigma,s}(x)$

    The four linearized equations (hydrostatic/heat + continuity + zonal/meridional momentum) $\xrightarrow{\text{eliminate}\ \delta u\ {\rm and}\ \delta v}$ Eq. (8,9)

    when $\omega$ is constant ($\bar{v}=0$) Eq. (8,9) $\rightarrow$ Eq. (6,7)

    - Two approximation of the equivalent depth (both $\sim\sigma^2(x)$):
        1. Green (1965)
            $$
            h_l=\frac{a^2}{g}\frac{\sigma^2-s_0^2\omega^2}{l(l+1)}\tag{11}
            $$
            with $s_0=0.95$ for diurnal tides and $s_0^2=2.0$ otherwise.
        2. Dobrovolskis (1978)
            $$
            h_l=\frac{a^2\sigma^4}{g}\frac{1}{\sigma^2l(l+1)+2s\omega\sigma-8\Pi\omega^2}\tag{12}
            $$

    - Boundary conditions:

        $\delta\eta_l^{\sigma,s}=0$ at $x=0$;

        all tidal waves either were evanescent or propagated energy upwards at great height.

### Basic state

- Basic state:
    $\bar{T}(\theta,x)$, $\bar{p}(\theta,x)$, $\bar{\rho}(\theta,x)$
    $\bar{v}(\theta,x)$
    $\Gamma(\theta,x)$, $\bar{S}(\theta,x)$

- 4 models (A,B,C,D) on $\bar{v}$ as Fig. 2

    4 models on $\Gamma$ and $\bar{S}$ as Fig. 3

    $\Gamma\Rightarrow \bar{T}$ $\xrightarrow{p=p_0 e^x + {\rm Eq. (1)}}$ $\bar{\rho}$

### Heating distribution

- Total flux $F$ Eq. 13
    The heating rate $J=J_\odot(x)\sum_{\sigma,s}\cdots$ Eq. 15: mean term $(0,0)$ + diurnal term $(\omega+n,1)$ + semidiurnal term $(2\omega+2n,2)$

- Heating models (Fig. 4):
    Model I: uniform heating above the nominal level of the cloud top
    Model II: $\delta$ function within the cloud layer
    Model III: Gaussian profile with peaks at the nominal level of the cloud top

    Model IV: convective heating with convective-layer top at $x_c=5.0$
    Model V: convective heating with convective-layer top at $x_c=1.2$

    Model VI: diffusive thermal boundary layer with thermal skin depth of $4.4$
    Model VII: diffusive thermal boundary layer with thermal skin depth of $1.4$

    Model VIII: $\delta$ function just above the ground

### Results

- Numerical solution process:
    basic state (A,B,C,D) + heating model (I,...,VIII) + heating mode $(\sigma,s)$ + equivalent depth $h_l^{\sigma,s}$ (Eq, 11,12) + solve Eq. 8,9 for each EGM mode $l$

- Table 1: average of four basic state, for the diurnal and semidiurnal tides

![](tab1.png)

## Heating at the ground

- Heating distribution
    $$
    J(x)=\frac{g}{P_0}F\delta(x-0^+)\tag{16}
    $$

- The surface pressure variation for each mode $(\sigma,s)$
    $$
    \delta p_0^{\sigma,s}=\bar{\rho}_0\delta\psi(0^-)=-\frac{g}{R\bar{T}_0}\frac{\kappa F^{\sigma,s}}{i\sigma_{\rm V}}=i\frac{\kappa F^{\sigma,s}}{\sigma_{\rm V}H_0}\tag{18}
    $$
    with $H_0=RT_0/g$ is the atmospheric scale heigth at the ground.

- Fig. 5: surface pressure and temperature variations
- Fig. 6: surface wind field ($\delta u,\delta v$)

## Tidal torques and conclusions

- Body gravitational tide:
    solar tidal potential $\Omega_\odot$ Eq. 21
    bulge's height $Z(\theta,\phi_\odot)$ Eq. 23
    potential of the bulge $\Omega_{\rm V}(\theta,\phi_\odot)$ Eq. 24
    body torque
    $$
    \begin{aligned}
    \mathcal{T}_{\rm g}&=M_\odot\left(\frac{a}{r}\right)^3\frac{\partial}{\partial\phi_\odot}\Omega_{\rm V}(\pi/2,0) \\
    &=-\frac{3}{2}kGM_\odot^2\frac{a^5}{r^6}\sin\epsilon \\
    &\approx -2.0\times10^{18}\frac{k}{Q}\,{\rm J}
    \end{aligned}
    \tag{25}
    $$

- Atmosphere thermal tide:
    torque $-\rho\dfrac{\partial}{\partial\phi_\odot}\Omega_\odot$
    $$
    \mathcal{T}_{\rm a}=\pi^{3/2}\frac{M_\odot}{M_{\rm V}}\frac{a^6}{r^3}\frac{1}{4}\frac{\kappa F_0}{\sigma H_0}\approx 1.8\times10^{16}\,{\rm J}\tag{28}
    $$

- The atmospheric and body tides balance if $Q=28$ with $k=0.25$.

![](fig7.jpg)
