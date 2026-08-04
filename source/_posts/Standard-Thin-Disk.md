---
title: Standard Thin Disk
math: true
date: 2026-07-03 16:26:01
updated: 2026-07-03 16:26:01
categories:
    - disk
tags:
    - black hole
    - accretion disk
---

- Shakura, N. I., & Sunyaev, R. A. (1973). Black holes in binary systems. Observational appearance. *Astronomy & Astrophysics*, *24*, 337–355.

<!-- more -->

## Mechanisms of Angular Momentum Transfer

Magnetic field, turbulence, <s>molecular</s> and <s>radiative</s> viscosity.

The tangential stresses due to the turbulence and magnetic field
$$
-w_{r\phi}\sim\rho v_s^2\left(\frac{v_t}{v_s}\right)+\rho v_s^2\left(\frac{H^2}{4\pi\rho v_s^2}\right)=\alpha\rho v_s^2
$$
can be characterized by only one parameter $\alpha$.

## The Structure of the Disk

The energy flux, radiated from surface unit of the disk in unit of the time
$$
\begin{aligned}
    Q&=\frac{1}{2}W_{r\phi} R\frac{\mathrm{d}\omega}{\mathrm{d}R} \\
    &=\frac{3}{8\pi}\dot{M}\frac{GM}{R^3}\left[1-\left(\frac{R_0}{R}\right)^{1/2}\right]
\end{aligned}\tag{2.6}
$$

Define parameters
$$
m=\frac{M}{M_\odot},\quad\dot{m}=\frac{\dot{M}}{\dot{M}_\text{cr}}=\frac{\dot{M}}{3\times10^{-8}\dfrac{M_\odot}{\text{yr}}}\left(\frac{M_\odot}{M}\right)
$$
$$
r=\frac{R}{3R_g}=\frac{1}{6}\frac{Rc^2}{GM}=\frac{M_\odot}{M}\frac{R}{9\text{ km}}
$$

## Radiation Spectrum of the Disk

### Local Radiation Spectrum

1. In the outer $r>800\alpha^{4/57}m^{-46/57}\dot{m}^{37/57}$ regions
    free-free processes give the main contribution to the opacity a planckian spectrum of radiation
    $$
    F(x)=B(x)=\frac{2\pi h}{c^2}\left(\frac{kT}{h}\right)^3\frac{x^3}{e^x-1},\quad\text{where }x=\frac{h\nu}{kT}\tag{3.1}
    $$
    The corresponding flux of energy is
    $$
    Q=\int F(x)\mathrm{d}x=\frac{c}{4}bT_s^4\,\frac{\text{erg}}{\text{cm}^2\text{ s}}
    $$

2. In the intermediate region
    $800 \alpha^{4/57}m^{-46/57}\dot{m}^{37/57}>r>25\alpha^{2/9}\dot{m}^{2/3}$
    where Thomoson scattering dominates the opacity
    1. In the case of a homogeneous medium with a sharp boundary
        $$
        F(x)=\sqrt{\frac{3\varkappa(x)n}{\sigma_Tm_P}}B(x)\sim\text{const }\sqrt{n}T^{5/4}\frac{x^{3/2}e^{-x}}{(1-e^{-x})^{1/2}}\tag{3.2}
        $$
        $$
        Q=1.8\times10^{-4}\sqrt{n}T^{2.25}\,\frac{\text{erg}}{\text{cm}^2\text{ s}}
        $$
    2. In the case of exponential varying atmosphere $n=n(z_1)e^{-z/H_0}$
        $$
        \begin{aligned}
        F(x)&=\left(\frac{3\varkappa(x)}{\sigma_T^2m_P^2H_0}\right)^{1/3}B(x) \\
        &\sim\text{const }H_0^{-1/3}T^{11/6}x^2\frac{e^{-x}}{(1-e^{-x})^{1/3}}
        \end{aligned}\tag{3.3}
        $$
        $$
        Q=1.3\times10^4H_0^{-1/3}T^{17/6}\,\frac{\text{erg}}{\text{cm}^2\text{ s}}\sim T^{2.5}
        $$
    
    the coefficient of free-free absorption
    $$
    \varkappa(x)=\frac{4.1\times10^{-23}(1-e^{-x})}{T^{7/2}x^3}\text{cm}^5
    $$
3. In the inner part of the disk $r<25\alpha^{2/9}\dot{m}^{2/3}$
    the processes of comptonization effect strongly the shape of the emitted spectrum
    $$
    F(x)\sim x^3e^{-x},\quad Q=\frac{cd(r)}{4}T^4,\quad d(r)\ll b.\tag{3.4}
    $$

### Distribution of the Surface Temperature

The average energy of each photon
$$
\bar{x}=\frac{\int F_\nu\mathrm{d}\nu}{\int \dfrac{F_\nu}{h\nu}\mathrm{d}\nu}=\frac{\langle h\nu\rangle}{kT}
$$

1. In the outer regions $\bar{x}=2.7$
    $$
    T_s=3\times10^7 m^{-1/4}\dot{m}^{1/4}r^{-3/4}(1-r^{-1/2})^{1/4}\text{ K}\tag{3.5}
    $$
    $$
    T_s=\left[\frac{3GM\dot{M}}{8\pi\sigma R^3}\left(1-\sqrt{\frac{R_0}{R}}\right)\right]^{1/4}
    $$
2. In the intermedian region
    1. according to (3.3) (exponential) $\bar{x}=1.66$
        $$
        T_s=10^8\alpha^{1/75}\dot{m}^{28/75}m^{-19/75}r^{-141/150}(1-r^{-1/2})^{28/75}\text{ K}\tag{3.6}
        $$
    2. according to (3.2) (homogeneous) $\bar{x}=1.2$
        $$
        T_s=1.4\times10^9\alpha^{2/9}\dot{m}^{8/9}m^{-2/9}r^{-5/3}(1-r^{-1/2})^{8/9}\text{ K}\tag{3.7}
        $$
3. In the inner region $\bar{x}=3$
    1. if $y=\dfrac{kT(z_1)}{m_ec^2}\tau_T^2(z_1)>1$
        $$
        \begin{aligned}
        T_s&=1.4\times10^9 A^{-2/9}\alpha^{2/9}\dot{m}^{8/9}m^{-2/9}r^{-5/3}(1-r^{-1/2})^{8/9} \\
        &\simeq 5\times10^8\alpha^{1/5}\dot{m}^{4/5}m^{-1/5}r^{-3/2}(1-r^{-1/2})^{4/5}\text{ K}
        \end{aligned}\tag{3.8}
        $$
    2. if $\tau^*(u_0)=\sqrt{\tau_{ff}\tau_s}<1$
        $$
        T_s=10^{14}\alpha^{12/5}\dot{m}^{24/5}r^{-36/5}(1-r^{-1/2})^{24/5}\tag{3.9}
        $$

### Integral Spectrum of the Outgoing Disk Radiation

Integrating the local spectrum
$$
I_\nu=4\pi \int_{R_0}^{R_1}F_\nu[T_s(R)]R\mathrm{d}R
$$
where $R_1$ is the external boundary of the disk.

For a local planckian spectrum and dependence $T_s(R)$ (3.5), we obtain for $\nu\ll\dfrac{kT_0}{h}$
$$
I_\nu=\frac{16\pi^2 R_0^2 h}{c^2}\left(\frac{kT_0}{h}\right)^{8/3}\nu^{1/3}
$$
The spectral index of radiation $\gamma=\dfrac{\mathrm{d}\ln I_\nu}{\mathrm{d}\ln \nu}=\dfrac{1}{3}$

For $r\gg1$,
$\gamma=0.07$ for spectrum (3.3) and temperature (3.6), (intermediate, exponential)
$\gamma=0.04$ for spectrum (3.2) and temperature (3.7), (intermediate, homogeneous)
$\gamma=-1/3$ for spectrum (3.4) and temperature (3.8), (inner)
$\gamma=-1$ for spectrum (3.4) and temperature (3.9). (inner)
