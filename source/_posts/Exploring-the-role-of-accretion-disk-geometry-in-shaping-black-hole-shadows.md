---
title: Exploring the role of accretion disk geometry in shaping black hole shadows
math: true
date: 2026-07-09 16:51:40
categories:
    - relativity
tags:
    - black hole
    - Schwarzschild metric
---

Wang, Z.-L. (2025). Exploring the role of accretion disk geometry in shaping black hole shadows. *Physical Review D*, *112*(6), 064052. https://doi.org/10.1103/fhqj-wgcm

<!-- more -->

## Accretion disk models

- Inner edge $r_\text{in}$ and half-opening angle $\psi_0$

    ![fig 1](fig1.png)

- Uniform motion of the disk matter, denoted by the four-velocity $U^\mu$
    1. Rotation-dominated flows:
        nearly Keplerian motion
        $$
        \Omega_\text{K}=\frac{U_\text{K}^\phi}{U^t_\text{K}}=\left(\frac{M}{r^3}\right)^{1/2}
        $$
        sub-Keplerian $\Omega=\kappa_\text{K}\Omega_\text{K}$ with $0<\kappa_\text{K}\le 1$
    2. Infall-dominated flows:
        the local radial velocity
        $$
        v^r_\text{ff}=\frac{U^r_\text{ff}}{U^t_\text{ff}}=-B(r)\left(\frac{2M}{r}\right)^{1/2}
        $$
        here $B(r)=1-2M/r$
        deviations from pure free fall $v^r=\kappa_\text{ff}v^r_\text{ff}$ with $0\le\kappa_\text{ff}<1$ (ADAF)
    3. Mixed flows:
        typical for thick disks at high accretion rates

- Emission profile and absorption
    - For an optically thick disk
        $$
        F_\text{em}(r)\approx\frac{\epsilon\dot{M}r}{4\pi}\left(-\Omega+\frac{r_\text{in}^2\Omega(r_\text{in})}{r^2}\right)\frac{\mathrm{d}\Omega}{\mathrm{d}r}
        $$
        where $\epsilon$ is a dimensionless efficiency parameter that characterizes the conversion of rotational energy into radiation due to viscous dissipation.
        $$
        F_\text{obs}=[g(r)]^4F_\text{em}(r)
        $$
    - For an optically thin disk
        $$
        \delta F_\text{em}\approx\frac{\epsilon\dot{M}}{4\pi\psi_0}\left(-\Omega+\frac{r_\text{in}^2\Omega(r_\text{in})}{r^2}\right)\frac{\mathrm{d}\Omega}{\mathrm{d}r}\sqrt{B}\delta l
        $$
        Radiative transfer:
        $$
        F(r_2)=F(r_1)e^{-\chi\delta l}\left[\frac{g(r_1)}{g(r_2)}\right]^4 +\delta F_\text{em}(r_2)
        $$
        where
        (1) $F(r_1)$ is the accumulated flux
        (2) $g(r)=\nu_\text{obs}/\nu_\text{em}(r)$ is the redshift factor
        (3) $\chi$ denotes the effective absorption coefficient. $\chi\rightarrow\infty$ for optically thick while $\chi\rightarrow0$ for optically thin.
