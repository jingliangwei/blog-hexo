---
title: Linearized primitive equation model on atmospheric tides of Venus
math: true
date: 2026-11-10 22:16:41
updated: 2026-11-10 22:16:41
categories:
tags:
---

- Pechmann, J. B. (1983). *Thermal tides in the atmosphere of Venus* (Doctoral dissertation). California Institute of Technology. https://doi.org/10.7907/5cd0-3q63
- Staniforth, A. N., & Daley, R. W. (1977). A finite-element formulation for the vertical discretization of sigma-coordinate primitive equation models. *Monthly Weather Review*, *105*(9), 1108–1118. [https://doi.org/10.1175/1520-0493(1977)105<1108:AFEFFT>2.0.CO;2](https://doi.org/10.1175/1520-0493(1977)105<1108:AFEFFT>2.0.CO;2)

<!-- more -->

## Ch 2. Numerical Model

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
