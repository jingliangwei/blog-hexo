---
title: Thermotidal torque on rocky planets with thin atmosphere
math: true
date: 2026-11-16 19:36:11
updated: 2026-11-16 19:36:11
categories:
    - planetary science
tags:
    - thermal tide
    - Lamb waves
---

- Auclair-Desrotour, P., Farhat, M., Boué, G., & Laskar, J. (2026). An analytical framework for atmospheric tides on rocky planets. I. Formulation. *Astronomy & Astrophysics*, *713*, Article A142. https://doi.org/10.1051/0004-6361/202558507
- Auclair-Desrotour, P., Laskar, J., Farhat, M., & Boué, G. (2026). *An analytical framework for atmospheric tides on rocky planets. II. Semidiurnal thermotidal torque*. arXiv. https://doi.org/10.48550/arXiv.2611.07060

<!-- more -->

## Paper I

The analytical solution for pressure perturbation.

### Tidal dynamics

Using reduced altitude $x=-\ln(p_0/p_s)$, where $p_s$ designates surface pressure.

- The primitive equations:
    Eq. (12,13,14): the $\theta,\varphi,z$ components of the momentum equation
    Eq. (15): the mass conservation
    Eq. (16): the thermodynamic equation (with Newtonian cooling $\sigma_{\rm C}$)
    Eq. (17): the linearised ideal gas law

- Fourier component: $F(x,\theta,\varphi,t)=\mathfrak{R}\{F_0\tilde{F}(x,\theta){\rm e}^{i(\sigma t+m\varphi)}\}$

- Introduce $G=-\dfrac{1}{\Gamma_1 p_0}\dfrac{\mathrm{d}p}{\mathrm{d}t}$
    Eq. (14-17) $\Rightarrow$ Eq. (39-42) $\Rightarrow$ Eq. (45) of $\tilde{G}(x)=\phi(x)\Psi_n(x)$

- Hough functions: $\tilde{F}(x,\theta)=\sum_n\tilde{F}_n(x)\Theta_n^{m,\nu}(\cos\theta)$
    with $\nu=2\Omega/\sigma$ the spin parameter

    Eq. (45) $\Rightarrow$ Eq. (54): the wave equation of vertical structure.

### Closed-form ab initio solution

- Atmospheric parameters:
    reduced stratification number $\gamma=\dfrac{N_B^2 H}{g}$
    reduced vertical variation rate characterising the atmospheric structure $\zeta=\dfrac{\mathrm{d}\beta}{\mathrm{d}x},\beta=\dfrac{gH}{V_0^2}$
    $\kappa=\dfrac{\Gamma_1-1}{\Gamma_1}$, with $\Gamma_1=C_p/C_V$

    - isentropic atmosphere: $\gamma=0,\zeta=-\kappa$
    - isothermal atmosphere: $\gamma=\kappa,\zeta=0$

- Heating: $\tilde{J}_n=\dfrac{\kappa J_s}{\sigma gH}{\rm e}^{-b_{\rm H}x}$

- Analytical expressions:
    homogeneous propagating wave term + thermal forcing term + gravitational forcing term
    $$
    \Psi_n=\mathcal{A}_n {\rm e}^{ik_nx}+\Psi_{n;\mathrm{H}}{\rm e}^{-(\lambda+b_{\rm H})x}+\Psi_{n;\mathrm{G}}{\rm e}^{-\lambda x}
    $$
    Eq. (82,83,84)

    $\Rightarrow$ $\tilde{V}_{\theta n},$ $\tilde{V}_{\varphi n},$ $\tilde{V}_{r n},$ $\delta\tilde{p}_{n},$ $\delta\tilde{\rho}_{n},$ $\delta\tilde{T}_{n}$ Eq. (87-92)

- The resonance of tidally excited Lamb waves:
    occurs for values of tidal frequencies $\sigma_{\mathcal{L};n}$ minimising the denominator of $\mathcal{A}_n$ in absolute value
    $$
    \sigma_{\mathcal{L};n}=\frac{1}{R}\sqrt{\frac{gH_s|\Lambda_n^{m,\nu}|}{1-\gamma}}\tag{97}
    $$

### Model limitations

- The whole planet, including the atmosphere, is assumed to rotate as a solid body. Winds and jets are ignored.

- The background fields (pressure, temperature, density, and perssure scale height) are assumed to vary across the vertial direction solely.

## Paper II

The analytical expression for thermotidal torque.

### Theory

- The thermotidal torque
    $$
    \mathcal{T}_z=\lim_{\Delta t\rightarrow+\infty}\frac{1}{\Delta t}\int_0^{\Delta t}\int_\mathcal{S}\partial_\varphi U_T\frac{R^2\delta p_s}{g}{\rm d}S\,{\rm d}t
    $$
    $$
    \mathcal{T}_z=\frac{8\pi}{5}c_f\frac{M_\star}{M}\frac{R^6}{a^3}\mathfrak{I}\{\delta p_{\text{s;eq}}^\sigma\}
    $$
    with $c_f$ is a dimensionless shape factor that quantifies the degree to which the latitudinal structure of semidiurnal pressure variations resembles a quadrupolar pattern.

- Multipole expansion of stellar irradiance

Define the normalised tidal frequency $X=\dfrac{\sigma}{\sigma_{\mathrm{L};n}}$,
damping rate $\varepsilon=\dfrac{\sigma_{\rm C}}{\sigma_{\mathrm{L};n}}$,
and thermotidal pressure variation $\delta\tilde{p}_{\rm T}=\dfrac{\kappa\eta\delta F_n}{p_sH_s\sigma_{\mathrm{L};n}}$

- The surface pressure variation, taking $x=0$ in $\delta\tilde{p}_n$
    for isentropic atmosphere
    $$
    \delta\tilde{p}_{\mathrm{s};n}=\frac{S_n\delta\tilde{p}_{\rm T}}{\varepsilon[(1+\kappa)X^2-S_n]+iX(X^2-S_n)}\tag{27}
    $$
    for isothermal atmosphere
    $$
    \delta\tilde{p}_{\mathrm{s};n}=\frac{iS_n\delta\tilde{p}_{\rm T}}{(X-i\varepsilon)[S_n+\Gamma_1(ik_n-\frac{1}{2})X^2]}\tag{33}
    $$

- Application to the present-day Earth:
    length of the day (LOD) $\text{LOD}=\dfrac{4\pi}{\sigma}$

    ![](paper2_fig2.jpeg)

- Consequences of phase-shifted tidal heating
    $\tilde{J}_n(x)=\tilde{J}_n^0(x){\rm e}^{-i\sigma t_{\rm H}}$ with constant time lag $t_{\rm H}$.

    ![](paper2_fig3.jpeg)

### Frequency behaviour

$\mathfrak{I}\{\delta\tilde{p}_{\text{s};n}(-X)\}=-\mathfrak{I}\{\delta\tilde{p}_{\text{s};n}(X)\}$, so only study the positive frequencies part.

![](paper2_fig4.jpeg)

- $X\sim 1$: second-order bandpass filter
    $$
    \delta\tilde{p}_{\text{s};n}=\frac{A_0{\rm e}^{-i\varphi_{\rm lag}}}{1+iQ(X-\frac{1}{X})}\tag{51}
    $$

- $X\ll 1$: first-order lowpass filter
    $$
    \delta\tilde{p}_{\text{s};n}=-\frac{\delta\tilde{p}_{\rm T}}{\varepsilon+iX}\tag{66}
    $$
    same as the results of Leconte et al. (2015)
