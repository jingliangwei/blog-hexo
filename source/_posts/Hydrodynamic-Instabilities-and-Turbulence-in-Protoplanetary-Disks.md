---
title: Hydrodynamic Instabilities and Turbulence in Protoplanetary Disks
math: true
date: 2026-07-21 22:34:53
updated: 2026-07-21 22:34:53
categories:
    - disk
tags:
    - instability
    - protoplanetary disk
---

- Lyra, W., & Umurhan, O. M. (2019). The initial conditions for planet formation: Turbulence driven by hydrodynamical instabilities in disks around young stars. *Publications of the Astronomical Society of the Pacific*, *131*(1001), 072001. https://doi.org/10.1088/1538-3873/aaf5ff

<!-- more -->

- Linear instability: any perturbation $\delta u\rightarrow 0$ leads to $\delta A\rightarrow \infty$

    Nonlinear instability: only perturbation $\delta u$ satisfing condition leads to $\delta A\rightarrow \infty$

- Restoring mechanism

- Linear growth:
    $\delta A\propto e^{\gamma t}$
    growth rate: $\gamma$

- Turbulence, chaos
- Energy cascade

![Energy cascade (Lyra & Umurhan, 2019)](energy_cascade.png)

## In Fluid

- Rayleigh-Taylor Instability (RTI)
    gravity
    (magnetic field, surface tension)

- Kelvin-Helmholtz Instability (KHI)
    shear strain
    (buoyancy) Richardson number $\text{Ri}=\dfrac{\text{buoyancy}}{\text{shear}}$

## In Accretion Disk

- Magnetorotational Instability (MRI)
    Alfvén wave
    Keplerian shear
    magnetic tension

- Gravitational Instability (GI)
    gravito-turbulence
    Toomre Q: $Q\sim\dfrac{c_s\Omega}{\pi G\Sigma}\lessapprox 1$
    GI -> clumps on sprials

## In Protoplanetary Disk

- Vertical Shear Instability (VSI)
    on $R-z$ plane, stratified-rotational instability
    interial waves
    -> RWI vortices

![VSI (Lyra & Umurhan, 2019)](VSI.png)

- Rossby Wave Instability (RWI)
    on $R-\phi$ plane
    Rossby wave
    $\dfrac{(\nabla\times\vec{v})_z}{\rho}$, $\rho$ jumps
    -> local vortices, cannot turbulence solely

- Convective Overstability (COS)
    on $R-z$ plane
    negative entropy gradient
    epicyclic escillation -> convection
    convection cells

- Subcritical Baroclinic Instability (SBI)
    on $R-\phi$ plane
    Nonlinear instability
    -> vortices with RWI

- Zombie Vortex Instability (ZVI)
    Nonlinear instability
    vortex -> boundary layer -> new vortex
    with RWI, SBI

- Streaming Instability (SI)
    dust (cm) -> planetesimal (km)
    $\nabla_r P$ streaming motion
    gas-dust drag, Coriolis force
    streaming motion v.s. epicyclic motion
    - metallicity threshold: $z=\Sigma_\text{dust}/\Sigma_\text{gas}$ -> clumping / planetesimal
