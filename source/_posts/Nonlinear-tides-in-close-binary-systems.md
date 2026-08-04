---
title: Nonlinear tides in close binary systems
math: true
date: 2026-07-02 16:05:47
updated: 2026-07-02 16:05:47
categories:
    - planetary science
tags:
    - binary
    - nonlinear tides
---

- Weinberg, N. N., Arras, P., Quataert, E., & Burkart, J. (2012). Nonlinear tides in close binary systems. *The Astrophysical Journal*, *751*(2), 136. https://doi.org/10.1088/0004-637X/751/2/136

<!-- more -->

## Statement of the Problem

A primary star of mass $M$ and radius $R$ subject to a tidal acceleration from the secondary of mass $M'$.
In a spherical coordinate system $(r,\theta,\phi)$ centered on the primary, take the orbit of the secondary to be $(D(t),\pi/2,\Phi(t))$, where $D(t)$ is the separation and $\Phi(t)$ is the true anomaly corresponding to a Keplerian orbit with the semimajor axis $a$, eccentricity $e$, and orbital period $P_\text{orb}=2\pi[a^3/G(M+M')]^{1/2}$.

The tidal acceleration $\boldsymbol{\nabla} U\propto\varepsilon(GM/R^2)$ with a small dimensionless strength of the tidal acceleration relative to internal gravity
$$
\varepsilon=\frac{M'}{M}\left(\frac{R}{a}\right)^{3}
$$

## Equations of Motion

$\boldsymbol{x}'$ is the position of a fluid element in the perturbed star
$\boldsymbol{x}$ is the position of the same fluid element in the background state
$\boldsymbol{\xi}$ is the Lagrangian displacement vector
$\boldsymbol{x}'=\boldsymbol{x}+\boldsymbol{\xi}(\boldsymbol{x},t)$

Write the internal forces due to pressure, buoyancy, and perturbed gravity
that are linear in $\boldsymbol{\xi}$ as $\boldsymbol{f}_1[\boldsymbol{\xi}]$
and those due to leading-order nonlinear interactions as $\boldsymbol{f}_2[\boldsymbol{\xi},\boldsymbol{\xi}]$

The external forcing terms due to the companion lead to the tidal acceleration
$$
\boldsymbol{a}_\text{tide}=-\boldsymbol{\nabla} U-(\boldsymbol{\xi}\cdot\boldsymbol{\nabla})\boldsymbol{\nabla} U.
$$

Gathering terms, the second-order equation of motion including linear forces, three-wave nonlinear interactions and tidal forcing is
$$
\rho\ddot{\boldsymbol{\xi}}=\boldsymbol{f}_1[\boldsymbol{\xi}]+\boldsymbol{f}_2[\boldsymbol{\xi},\boldsymbol{\xi}]+\rho\boldsymbol{a}_\text{tide}.\tag{4}
$$

There are two approaches to solve:
(1) expand quantities relative to the star's unperturbed background state;
(2) expand quantities relative to the star's linearly perturbed state.

### Method 1

Expand using
$$
\boldsymbol{\xi}(\boldsymbol{x},t)=\sum_a q_a(t)\boldsymbol{\xi}_a(\boldsymbol{x})e^{-i\omega_a t}.
$$
The eigenmode labeled $a$ is specified by its frequency $\omega_a$, eigenfunction $\boldsymbol{\xi}_a(\boldsymbol{x})$, and total amplitude $q_a$.

A set of coupled oscillator equations for each mode:
$$
\begin{aligned}
    \dot{q}_a+i\omega_a q_a=&-\gamma_a q_a + i\omega_a U_a(t) \\
    &+i\omega_a\sum_b U_{ab}^*(t)q_b^* \\
    &+i\omega_a\sum_{bc}\kappa_{abc}^*q_b^*q_c^*.
\end{aligned}\tag{6}
$$
The terms on the right-hand side represent linear damping ( $\gamma_a$ ), the linear ( $U_a$ ) and nonlinear ( $U_{ab}$ ) tidal force, and three-wave coupling ( $\kappa_{abc}$ ).

$$
\begin{aligned}
    U_a(t)&=-\frac{1}{E_0}\int\mathrm{d}^3x\,\rho\boldsymbol{\xi}_a^*\cdot\boldsymbol{\nabla}U \\
    &=\sum_k U_a^{(k)}e^{-ik\Omega t}
\end{aligned}
$$
$$
U_{ab}(t)=-\frac{1}{E_0}\int\mathrm{d}^3x\,\rho\boldsymbol{\xi}_a\cdot(\boldsymbol{\xi}_b\cdot\boldsymbol{\nabla})\boldsymbol{\nabla}U
$$
$$
\kappa_{abc}=\frac{1}{E_0}\int\mathrm{d}^3x\,\boldsymbol{\xi}_a\cdot\boldsymbol{f}_2[\boldsymbol{\xi}_b,\boldsymbol{\xi}_c]
$$

### Method 2

$q_{a,\text{lin}}$ is the linear amplitude
$r_a\equiv q_a-q_{a,\text{lin}}$
$\boldsymbol{\xi}=\boldsymbol{\xi}_\text{lin}+\boldsymbol{\xi}_\text{nl}$
$$
    \rho\ddot{\boldsymbol{\xi}}_\text{lin}=\boldsymbol{f}_1[\boldsymbol{\xi}_\text{lin}]-\rho\boldsymbol{\nabla} U
$$
$$
\begin{aligned}
    \rho\ddot{\xi}_\text{nl}=&\boldsymbol{f}_1[\boldsymbol{\xi}_\text{nl}]+\boldsymbol{f}_2[\boldsymbol{\xi}_\text{lin},\boldsymbol{\xi}_\text{lin}]+2\boldsymbol{f}_2[\boldsymbol{\xi}_\text{lin},\boldsymbol{\xi}_\text{nl}] \\
    &+\boldsymbol{f}_2[\boldsymbol{\xi}_\text{nl},\boldsymbol{\xi}_\text{nl}]-\rho[(\boldsymbol{\xi}_\text{lin}+\boldsymbol{\xi}_\text{nl})\cdot\boldsymbol{\nabla}]\boldsymbol{\nabla}U.
\end{aligned}
$$

Expand using
$$
\boldsymbol{\xi}_\text{nl}(\boldsymbol{x},t)=\sum_a r_a(t)\boldsymbol{\xi}_{a}(\boldsymbol{x})e^{-i\omega_{a} t}.
$$

The equation for each mode's nonlinear amplitude
$$
\begin{aligned}
    \dot{r}_a+(i\omega_a+\gamma_a)r_a={}&i\omega_a(V_a^*+K_a^*) \\
    &+i\omega_a\sum_b(U_{ab}^*+2K_{ab}^*)r_b^* \\
    &+i\omega_a\sum_{bc}\kappa_{abc}^*r_b^*r_c^*.
\end{aligned}\tag{20}
$$

$$
V_a(t)\equiv-\frac{1}{E_0}\int\mathrm{d}^3x\,\rho\boldsymbol{\xi}_a\cdot(\boldsymbol{\xi}_\text{lin}\cdot\boldsymbol{\nabla})\boldsymbol{\nabla}U
$$
$$
K_a(t)\equiv\frac{1}{E_0}\int\mathrm{d}^3x\,\boldsymbol{\xi}_a\cdot\boldsymbol{f}_2[\boldsymbol{\xi}_\text{lin},\boldsymbol{\xi}_\text{lin}]
$$
$$
K_{ab}(t)\equiv\frac{1}{E_0}\int\mathrm{d}^3x\,\boldsymbol{\xi}_a\cdot\boldsymbol{f}_2[\boldsymbol{\xi}_\text{lin},\boldsymbol{\xi}_b]
$$

There are three types of three-wave coupling are
(1) linear-linear coupling (LLC)
(2) linear-nonlinear coupling (LNC)
(3) nonlinear-nonlinear coupling (NNC)

## Linear Tide

The linear equation:
$$
\dot{q}_a+i\omega_a q_a=-\gamma_a q_a+i\omega_a U_a(t),
$$
whose steady-state solution is
$$
q_{a,\text{lin}}(t)=\sum_{k=-\infty}^\infty \frac{\omega_a U_a^{(k)}}{\omega_a-k\Omega-i\gamma_a}e^{-ik\Omega t}.
$$

The linear response can be broken up into a zero frequency equilibrium tide and a dynamical tide, $q_{a,\text{lin}}(t)=q_{a,\text{eq}}(t)+q_{a,\text{dyn}}(t)$, where
$$
q_{a,\text{eq}}(t)\equiv\sum_{k=-\infty}^\infty U_a^{(k)}e^{-ik\Omega t}
$$
and
$$
\begin{aligned}
    q_{a,\text{dyn}}(t)&\equiv q_{a,\text{lin}}(t)-q_{a,\text{eq}}(t) \\
    &=\sum_{k=-\infty}^\infty \left(\frac{k\Omega+i\gamma_a}{\omega_a-k\Omega-i\gamma_a}\right)U_a^{(k)}e^{-ik\Omega t}.
\end{aligned}
$$

## Stability Analysis

$$
\dot{r}_b+(i\omega_b+\gamma_b)r_b=i\omega_b\sum_c[U_{bc}^*(t)+2K_{bc}^*(t)]r_c^*
$$
Plug in $r_b(t)=Q_b(t)e^{i\omega t/2}$ and similarly for $r_c$
$$
\dot{Q}_b+(i\Delta_b+\gamma_b)Q_b=i\sum_c\left(\frac{\omega_b}{\omega_c}\right)^{1/2}\Gamma_{bc}^*Q_c^*
$$
here $\Delta_k=\omega_k+\omega/2$ is the daughter detuning, define the daughter pair "driving rate"
$$
\Gamma_{bc}\equiv\sqrt{\omega_b\omega_c}(U_{bc}+2K_{bc})
$$

Writing these equations as $\dot{\boldsymbol{Q}}=H\boldsymbol{Q}$, the solutions are $\boldsymbol{Q}\propto\exp(st)$.
The system is unstable if there is an $s$ such that $\text{Re}(s)>0$.
