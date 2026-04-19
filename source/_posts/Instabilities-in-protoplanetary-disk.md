---
title: Instabilities in protoplanetary disk
math: true
date: 2026-04-19 14:48:39
categories:
    - disk
tags:
    - instability
    - protoplanetary disk
excerpt:
    The instabilities in protoplanetary disk.
---

Huang, P., & Bai, X.-N. (2025). The interplay between dust dynamics and turbulence induced by the vertical shear instability. *The Astrophysical Journal*, *986*(1), 76. https://doi.org/10.3847/1538-4357/add345

Huang, P., & Bai, X.-N. (2025). Dust clumping in outer protoplanetary disks: The interplay among four instabilities. *The Astrophysical Journal Letters*, *986*(1), L13. https://doi.org/10.3847/2041-8213/adcebb

## Evolutions

The dust is treated as a single pressureless fluid, characterized by the stopping time $T_s$, the interaction term between the gas and the dust fluid can be find in the equations:
$$
\frac{\partial\rho_g\boldsymbol{v}_g}{\partial t}+\nabla\cdot(\rho_g\boldsymbol{v}_g\boldsymbol{v}_g+P)=\rho_g\nabla\Phi+\rho_d\frac{\boldsymbol{v}_d-\boldsymbol{v}_g}{T_s}\tag{2}
$$
$$
\frac{\partial\rho_d\boldsymbol{v}_d}{\partial t}+\nabla\cdot(\rho_d\boldsymbol{v}_d\boldsymbol{v}_d)=\rho_d\nabla\Phi+\rho_d\frac{\boldsymbol{v}_g-\boldsymbol{v}_d}{T_s}\tag{4}
$$

## Instabilities

- VSI (vertical shear instability): for nonbarotropic ($\nabla\rho_g\times\nabla P\neq 0$) disk, there is a weak vertical shear
$$
2R\Omega_g\frac{\partial \Omega_g}{\partial z}=-\frac{(\nabla\rho_g\times\nabla P)}{\rho_g^2}\cdot\hat{\phi}
$$
lead to weak zonal flows.

- SI (streaming instability): the dust streaming motion (due to radial perssure gradient) back-reaction to the gas.
- RWI (Rossby wave instability): the maximum of "entropy modified inversed vortensity", with strong radial pressure variations.
- KHI (Kelvin-Helmholtz instability): velocity shear across an interface.
