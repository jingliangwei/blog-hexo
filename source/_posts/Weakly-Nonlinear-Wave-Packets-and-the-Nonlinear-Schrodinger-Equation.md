---
title: Weakly Nonlinear Wave Packets and the Nonlinear Schrödinger Equation
math: true
date: 2026-07-07 21:30:03
categories:
    - fluid
tags:
    - nonlinear Schrödinger equation
    - multiple scales
---

Dias, F., & Bridges, T. (2005). Weakly nonlinear wave packets and the nonlinear Schrödinger equation. In R. Grimshaw (Ed.), *Nonlinear waves in fluids: Recent advances and modern applications* (pp. 29–67). Springer. https://doi.org/10.1007/3-211-38025-6_2

<!-- more -->

## The method of multiple scales

A derivation of the NLS (nonlinear Schrödinger) equation from the KdV (Korteweg-de Vries) equation based on the method of multiple scales.

- The KdV equation
    $$
    \mathcal{L}(u)+\mathcal{N}(u,u)=u_t+u_{xxx}+6uu_x=0,\quad(x\in\mathbb{R},t\ge0,u(x,t)\in\mathbb{R}).
    $$
    Introducting a small parameter $\epsilon$, and the slow scales $X=\epsilon x,T=\epsilon t,\tau=\epsilon^2 t$
    $$
    u=\epsilon(u_0+\epsilon u_1+\epsilon^2 u_2+\cdots)=\epsilon u_0+\epsilon^2 u_1+\epsilon^3 u_2+\cdots,
    $$
    $$
    \begin{aligned}
    \mathcal{L}&=\partial_t+\partial_{xxx} \\
    &=\left(\frac{\partial}{\partial t}+\epsilon\frac{\partial}{\partial T}+\epsilon^2\frac{\partial}{\partial \tau}\right)+\left(\frac{\partial}{\partial x}+\epsilon\frac{\partial}{\partial X}\right)^3 \\
    &=\left(\frac{\partial}{\partial t}+\frac{\partial^3}{\partial x^3}\right)+\epsilon\left(\frac{\partial}{\partial T}+3\frac{\partial^3}{\partial x^2\partial X}\right)+\epsilon^2\left(\frac{\partial}{\partial\tau}+3\frac{\partial^3}{\partial x\partial X^2}\right)+\cdots \\
    &\equiv\mathcal{L}^{(0)}+\epsilon\mathcal{L}^{(1)}+\epsilon^2\mathcal{L}^{(2)}+\cdots,
    \end{aligned}
    $$
    $$
    \begin{array}{ll}
    \mathcal{O}(\epsilon) & \mathcal{L}^{(0)}u_0=0, \\
    \mathcal{O}(\epsilon^2) & \mathcal{L}^{(0)}u_1=-\mathcal{L}^{(1)}u_0-3\partial_x(u_0^2), \\
    \mathcal{O}(\epsilon^3) & \mathcal{L}^{(0)}u_2=-\mathcal{L}^{(2)}u_0-\mathcal{L}^{(1)}u_1-6\partial_x(u_0u_1)-3\partial_X(u_0^2).
    \end{array}
    $$

- At $\mathcal{O}(\epsilon)$: $\mathcal{L}^{(0)}u_0=0$
    the eigen mode
    $$
    u_0(x,t)=\psi_0(X,T)\exp[i(kx-\omega t)]+\text{c.c.}
    $$
    with the dispersion relation
    $$
    \omega=-k^3.
    $$
    the phase velocity $c=\omega/k$
    the group velocity $c_g=\mathrm{d}\omega/\mathrm{d}k=-3k^2$

- At $\mathcal{O}(\epsilon^2)$: $\mathcal{L}^{(0)}u_1=-\mathcal{L}^{(1)}u_0-3\partial_x(u_0^2)$
    the solvability condition ( remove the eigen mode term in RHS of the equation )
    $$
    \mathcal{L}^{(1)}u_0=0\Rightarrow(\partial_T+c_g\partial_X)u_0=0
    $$
    on the time scale $T$, the wave packet is just transported at the group velocity and thus depends only on the variable $\xi=X-c_gT$.
    Then solve for $u_1$:
    $$
    \mathcal{L}^{(0)}u_1=-3\partial_x(\phi_0^2e^{2i(kx-\omega t)}+\text{c.c.})\tag{2.10}
    $$
    the general solution is
    $$
    u_1=A_2(X,T)e^{2i(kx-\omega t)}+\text{c.c.}+\psi_1 e^{i(kx-\omega t)}+\text{c.c.}+A_0(X,T)
    $$
    the term $\psi_1 e^{i(kx-\omega t)}$ can be incorporated into the term $\psi_0 e^{i(kx-\omega t)}$ by defining $\psi=\psi_0+\epsilon\psi_1$.
    $$
    \left\{
    \begin{aligned}
    u_0&=\psi e^{i(kx-\omega t)}+\text{c.c.}, \\
    u_1&=A_2(X,T)e^{2i(kx-\omega t)}+\text{c.c.}+A_0(X,T),
    \end{aligned}
    \right.
    $$
    $$
    u_1\rightarrow\mathcal{O}(\epsilon^2)\text{(2.10)}\Rightarrow A_2=\frac{-3(2ik)\psi^2}{-2i\omega+(2ik)^3}=\frac{\psi^2}{k^2}.
    $$

- At $\mathcal{O}(\epsilon^3)$: $\mathcal{L}^{(0)}u_2=-\mathcal{L}^{(2)}u_0-\mathcal{L}^{(1)}u_1-6\partial_x(u_0u_1)-3\partial_X(u_0^2)$
    the solvability condition
    $$
    -\partial_\tau\psi-3ik\partial_{XX}\psi-6ik|\psi|^2\psi/k-6ikA_0\psi=0\tag{2.13}
    $$
    Equating the coefficients of the oscillation free (time average) terms in (2.13)
    $$
    -\partial_T A_0-6\partial_X|\psi|^2=0\Rightarrow A_0=-\frac{2|\psi|^2}{k^2}
    $$
    noting that $\mathrm{d}^2\omega/\mathrm{d}k^2=-6k$, (2.13) leads to the cubic NLS equation
    $$
    i\frac{\partial\psi}{\partial\tau}+\frac{1}{2}\frac{\mathrm{d}^2\omega}{\mathrm{d}k^2}\frac{\partial^2\psi}{\partial\xi^2}+\frac{6}{k}|\psi|^2\psi=0.
    $$

