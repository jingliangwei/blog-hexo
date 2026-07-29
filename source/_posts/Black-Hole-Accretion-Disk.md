---
title: Black Hole Accretion Disk
math: true
date: 2026-06-30 15:28:48
categories:
    - disk
tags:
    - black hole
    - accretion disk
---

- Abramowicz, M. A., & Fragile, P. C. (2013). Foundations of black hole accretion disk theory. *Living Reviews in Relativity*, *16*(1), Article 1. https://doi.org/10.12942/lrr-2013-1

<!-- more -->

## Parameters

| Parameters | Expression |
|:---|:---|
| total mass | $M_*$ |
| total angular momentum | $J_*$ |
| rescaled mass | $M=\dfrac{GM_*}{c^2}$ |
| rescaled angular momentum | $a=\dfrac{J_*}{M_* c}$ |
| relative thickness | $h=\dfrac{H}{R}$ |
| dimensionless accretion rate | $\dot{m}=\dfrac{0.1\dot{M}c^2}{L_\text{Edd}}$ |
| optical depth | $\tau$ |
| importance of advection | $q=\dfrac{Q_\text{adv}}{Q_\text{rad}}$ where $Q$ represents an energy flux |
| importance of radiation pressure | $\beta=\dfrac{P_\text{gas}}{P_\text{gas}+P_\text{rad}}$ |
| location of inner edge | $r_\text{in}$ |
| accretion efficiency | $\eta$ |
| marginally stable orbit </br>(innermost stable circular orbit) | $r_\text{ms}$ |
| marginally bound orbit | $r_\text{mb}$ |
| energy | $\mathcal{E}\equiv-\eta^\mu p_\mu=-p_t$ |
| angular momentum | $\mathcal{L}\equiv\xi^\mu p_\mu=p_\phi$ |
| specific angular momentum | $\ell\equiv\dfrac{\mathcal{L}}{\mathcal{E}}=-\dfrac{p_\phi}{p_t}=-\dfrac{u_\phi}{u_t}$ |
| angular velocity measured by ZAVO </br>(Zero Angular Velocity Observer) | $\Omega=\dfrac{u^\phi}{u^t}=\dfrac{\mathrm{d}\phi}{\mathrm{d}t}$ |
| redshift factor | $A=u^t$, $-A^{-2}=g_{tt}+2\Omega g_{t\phi}+\Omega^2 g_{\phi\phi}$ |

There are 4 types of accretion disks:
- Thick Disk
    $$
    h>1,\dot{m}\gg1,\tau\gg1,q\sim1,\beta\ll1,r_\text{in}\sim r_\text{mb},\eta\ll0.1
    $$
- Thin Disk
    $$
    h\ll1,\dot{m}<1,\tau\gg1,q=0,\beta\sim1,r_\text{in}=r_\text{ms},\eta\sim0.1
    $$
- Slim Disk
    $$
    h\sim1,\dot{m}\gtrapprox1,\tau\gg1,q\sim1,\beta<1,r_\text{mb}<r_\text{in}<r_\text{ms},\eta<0.1
    $$
- Advection-Dominated Accretion Flow (ADAF)
    $$
    h<1,\dot{m}\ll1,\tau\ll1,q\sim1,\beta=1,r_\text{mb}<r_\text{in}<r_\text{ms},\eta\ll0.1
    $$

## General Principles

The fundamental conservation laws that govern the behavior of all matter, namely the conservation of rest mass and conservation of energy-momentum
$$
\nabla_\mu(\rho u^\mu)=0,\quad \nabla_\mu T_\nu^\mu=0.
$$
Here $\rho$ is the rest mass density, $u^\mu$ is the four velocity of matter, and $T_\nu^\mu$ is the stress energy tensor which can be written as,
$$
\begin{aligned}
    (T_\nu^\mu)_\text{GEN}&=(T_\nu^\mu)_\text{FLU}+(T_\nu^\mu)_\text{VIS}+(T_\nu^\mu)_\text{MAX}+(T_\nu^\mu)_\text{RAD}, \\
    (T_\nu^\mu)_\text{FLU}&=(\rho u^\mu)(Wu_\nu)+\delta_\nu^\mu P, \\
    (T_\nu^\mu)_\text{VIS}&=\nu_*\sigma_\nu^\mu, \\
    (T_\nu^\mu)_\text{MAX}&=F^{\mu\alpha}F_{\alpha\nu}-\frac{1}{4}\delta_\nu^\mu F_{\alpha\beta}F^{\alpha\beta}, \\
    (T_\nu^\mu)_\text{RAD}&=\frac{4}{3}Eu^\mu u_\nu+u^\mu F_\nu+u_\nu F^\mu,
\end{aligned}
$$
Here $W$ is enthalpy, $\delta_\nu^\mu$ is Kronecker delta tensor, $P$ is pressure, $\nu_*$ is kinematic viscosity, $\sigma_\nu^\mu$ is shear, $F^{\mu\nu}$ is Faraday electromagnetic field tensor, $E$ is radiation energy density and $F^\mu$ is radiation flux.

## Thick Disks

- Polish doughnuts
    $(T_\nu^\mu)_\text{VIS}=(T_\nu^\mu)_\text{MAX}=(T_\nu^\mu)_\text{RAD}=0$
    assume for the stress energy tensor and four velocity,
    $$
    \begin{aligned}
        T_\nu^\mu=(T_\nu^\mu)_\text{FLU}&=\rho Wu^\mu u_\nu+P\delta_\nu^\mu, \\
        u^\mu&=A(\eta^\mu+\Omega\xi^\mu),
    \end{aligned}
    $$
    the equation for the equipressure surfaces, $P(r,\theta)=\text{const}$, may be written as $r_P(\theta)$ with the function $r_P(\theta)$ given by
    $$
    -\frac{\mathrm{d}r_P}{\mathrm{d}\theta}=\frac{\partial_\theta P}{\partial_r P}=\frac{(1-\ell\Omega)\partial_\theta\ln A+\ell\partial_\theta\Omega}{(1-\ell\Omega)\partial_r\ln A+\ell\partial_r\Omega}.
    $$

![Fig 4](Fig4.png)

## Thin Disks

### Equations in the Kerr geometry

1. Mass conservation (continuity)
2. Radial momentum conservation
3. Angular momentum conservation
4. Vertical equilibrium
5. Energy conservation

### The eigenvalue problem

The thin disk equations can be reduced to a set of two ordinary differential equations for two dependent variables, e.g., the Mach number $\mathcal{M}=-V/c_S=-V\Sigma/P$ and the angular momentum $\mathcal{L}=u_\phi$
$$
\frac{\mathrm{d}\ln\mathcal{M}}{\mathrm{d}\ln r}=\frac{\mathcal{N}_1(r,\mathcal{M},\mathcal{L})}{\mathcal{D}(r\mathcal{M},\mathcal{L})}\frac{\mathrm{d}\ln\mathcal{L}}{\mathrm{d}\ln r}=\frac{\mathcal{N}_2(r,\mathcal{M},\mathcal{L})}{\mathcal{D}(r\mathcal{M},\mathcal{L})}
$$
At the "sonic" point ( $\mathcal{D}(r,\mathcal{M},\mathcal{L})=0$ ) $r_\text{sonic}$, the extra regularity conditions $\mathcal{N}_i(r,\mathcal{M},\mathcal{L})=0$ are satisfied only for one particular value $\mathcal{L}_\text{in}$, which is the eigenvalue of the problem.

### Solutions

Using a more general scaling: $m=M/M_\odot$ and $\dot{m}=\dot{M}c^2/L_\text{Edd}$.
- Outer region: $P=P_\text{gas}$, $\kappa=\kappa_\text{ff}$ (free-free opacity)
    $$
    \begin{aligned}
    F &= [7 \times 10^{26} \text{ erg~cm}^{-2}~\text{s}^{-1}](m^{-1} \dot{m})\,r^{-3}_*\, \mathcal{B}^{-1} \mathcal{C}^{-1/2} \mathcal{Q}, \\
    \Sigma &= [4 \times 10^5 \text{ g~cm}^{-2}] (\alpha^{-4/5}\,m^{2/10} \dot{m}^{7/10}_{0*})\,r^{-3/4}_*\, \mathcal{A}^{1/10} \mathcal{B}^{-4/5} \mathcal{C}^{1/2} \mathcal{D}^{-17/20} \mathcal{E}^{-1/20} \mathcal{Q}^{7/10}, \\
    H &= [4 \times 10^2 \text{ cm}] (\alpha^{-1/10}\,m^{18/20} \dot{m}^{3/20})\,r^{9/8}_* \,\mathcal{A}^{19/20} \mathcal{B}^{-11/10} \mathcal{C}^{1/2} \mathcal{D}^{-23/40} \mathcal{E}^{-19/40} \mathcal{Q}^{3/20}, \\
    \rho_0 &= [4 \times 10^2 \text{ g~cm}^{-3}] (\alpha^{-7/10}\,m^{-7/10} \dot{m}^{11/20})\,r^{-15/8}_* \,\mathcal{A}^{-17/20} \mathcal{B}^{3/10} \mathcal{D}^{-11/40} \mathcal{E}^{17/40} \mathcal{Q}^{11/20}, \\
    T &= [2 \times 10^8 \text{ K}] (\alpha^{-1/5}\,m^{-1/5} \dot{m}^{3/10})\,r^{-3/4}_*\, \mathcal{A}^{-1/10} \mathcal{B}^{-1/5} \mathcal{D}^{-3/20} \mathcal{E}^{1/20} \mathcal{Q}^{3/10}, \\
    \beta/(1-\beta) &= [3](\alpha^{-1/10}\,m^{-1/10} \dot{m}^{-7/20})\,r^{3/8}_*\,\mathcal{A}^{-11/20} \mathcal{B}^{9/10} \mathcal{D}^{7/40} \mathcal{E}^{11/40} \mathcal{Q}^{-7/20}, \\
    \tau_{ff}/{\tau}_{es} &= [2 \times 10^{-3}](\dot{m}^{-1/2})\,r^{3/4}_*\,\mathcal{A}^{-1/2} \mathcal{B}^{2/5} \mathcal{D}^{1/4} \mathcal{E}^{1/4} \mathcal{Q}^{-1/2},
    \end{aligned}
    $$
    where $r_*=rc^2/GM$.
- Middle region: $P=P_\text{gas}$, $\kappa=\kappa_\text{es}$ (electron-scattering opacity)
    $$
    \begin{aligned}
    F &= [7 \times 10^{26} \text{ erg~cm}^{-2}~\text{s}^{-1}](m^{-1} \dot{m})\,r^{-3}_*\, \mathcal{B}^{-1} \mathcal{C}^{-1/2} \mathcal{Q}, \\
    \Sigma &= [9 \times 10^4 \text{ g~cm}^{-2}](\alpha^{-4/5} m^{1/5} \dot{m}^{3/5})\,r^{-3/5}_*\, \mathcal{B}^{-4/5} \mathcal{C}^{1/2} \mathcal{D}^{-4/5} \mathcal{Q}^{3/5}, \\
    H &= [1 \times 10^3 \text{ cm}](\alpha^{-1/10} m^{9/10} \dot{m}^{1/5})\,r^{21/20}_*\,\mathcal{A} \mathcal{B}^{-6/5} \mathcal{C}^{1/2} \mathcal{D}^{-3/5} \mathcal{E}^{-1/2} \mathcal{Q}^{1/5}, \\
    \rho_0 &= [4 \times 10^1 \text{ g~cm}^{-3}](\alpha^{-7/10} m^{-7/10} \dot{m}^{2/5})\,r^{-33/20}_*\,\mathcal{A}^{-1} \mathcal{B}^{3/5} \mathcal{D}^{-1/5} \mathcal{E}^{1/2} \mathcal{Q}^{2/5}, \\
    T &= [7 \times 10^8 \text{ K}](\alpha^{-1/5} m^{-1/5} \dot{m}^{2/5})\,r^{-9/10}_*\,\mathcal{B}^{-2/5} \mathcal{D}^{-1/5}\mathcal{Q}^{2/5}, \\
    \beta/(1-\beta) &= [7 \times 10^{-3}](\alpha^{-1/10} m^{-1/10} \dot{m}^{-4/5})\,r^{21/20}_*\,\mathcal{A}^{-1} \mathcal{B}^{9/5} \mathcal{D}^{2/5} \mathcal{E}^{1/2} \mathcal{Q}^{-4/5}, \\
    \tau_{ff}/{\tau}_{es} &= [2 \times 10^{-6}](\dot{m}^{-1})\,r^{3/2}_*\,\mathcal{A}^{-1} \mathcal{B}^{2} \mathcal{D}^{1/2}\mathcal{E}^{1/2} \mathcal{Q}^{-1},
    \end{aligned}
    $$
- Inner region: $P=P_\text{rad}$, $\kappa=\kappa_\text{es}$
    $$
    \begin{aligned}
    F &= [7 \times 10^{26} \text{ erg~cm}^{-2}~\text{s}^{-1}](m^{-1} \dot{m})\,r^{-3}_*\, \mathcal{B}^{-1} \mathcal{C}^{-1/2} \mathcal{Q}, \\
    \Sigma &= [5 \text{ g~cm}^{-2}](\alpha^{-1} \dot{m}^{-1})\,r^{3/2}_*\, \mathcal{A}^{-2}\mathcal{B}^{3} \mathcal{C}^{1/2}\mathcal{E} \mathcal{Q}^{-1}, \\
    H &= [1 \times 10^5 \text{ cm}](\dot{m})\,\mathcal{A}^2 \mathcal{B}^{-3} \mathcal{C}^{1/2} \mathcal{D}^{-1} \mathcal{E}^{-1} \mathcal{Q}, \\
    \rho_0 &= [2 \times 10^{-5} \text{ g~cm}^{-3}](\alpha^{-1} m^{-1} \dot{m}^{-2})\,r^{3/2}_*\,\mathcal{A}^{-4} \mathcal{B}^{6} \mathcal{D} \mathcal{E}^{2} \mathcal{Q}^{-2}, \\
    T &= [5 \times 10^7 \text{ K}](\alpha^{-1/4} m^{-1/4})\,r^{-3/8}_*\,\mathcal{A}^{-1/2}\mathcal{B}^{1/2} \mathcal{E}^{1/4}, \\
    \beta/(1-\beta) &= [4 \times 10^{-6}](\alpha^{-1/4} m^{-1/4} \dot{m}^{-2})\,r^{21/8}_*\,\mathcal{A}^{-5/2} \mathcal{B}^{9/2} \mathcal{D} \mathcal{E}^{5/4} \mathcal{Q}^{-2}, \\
    (\tau_{ff}\tau_{es})^{1/2} &= [1 \times 10^{-4}](\alpha^{-17/16} m^{-1/16} \dot{m}^{-2})\,r^{93/32}_*\,\mathcal{A}^{-25/8} \mathcal{B}^{41/8}\mathcal{C}^{1/2} \mathcal{D}^{1/2}\mathcal{E}^{25/16} \mathcal{Q}^{-2}.
    \end{aligned}
    $$

The radial functions $\mathcal{A},...,\mathcal{Q}$ are defined in terms of $y=\sqrt{r/M}$ and $a_*=a/M$ as:
$$
\begin{aligned}
\mathcal{A}&=1+a_*^2y^{-4}+2a_*^2y^{-6}, \\
\mathcal{B}&=1+a_*y^{-3}, \\
\mathcal{C}&=1-3y^{-2}+2a_*y^{-3}, \\
\mathcal{D}&=1-2y^{-2}+a_*^2y^{-4}, \\
\mathcal{E}&=1+4a_*^2y^{-4}-4a_*^2y^{-6}+3a_*^4y^{-8}, \\
\mathcal{Q}_0&=\frac{1+a_*y^{-3}}{y(1-3y^{-2}+2a_*y^{-3})^{1/2}},
\end{aligned}
$$
$$
\begin{aligned}
\mathcal{Q}&=\mathcal{Q}_0\left[y-y_0-\frac{3}{2}a_*\ln\left(\frac{y}{y_0}\right)-\frac{3(y_1-a_*)^2}{y_1(y_1-y_2)(y_1-y_3)}\ln\left(\frac{y-y_1}{y_0-y_1}\right)\right] \\
&-\mathcal{Q}_0\left[\frac{3(y_2-a_*)^2}{y_2(y_2-y_1)(y_2-y_3)}\ln\left(\frac{y-y_2}{y_0-y_2}\right)-\frac{3(y_3-a_*)^2}{y_3(y_3-y_1)(y_3-y_2)}\ln\left(\frac{y-y_3}{y_0-y_3}\right)\right].
\end{aligned}
$$
Here $y_0=\sqrt{r_\text{ms}/M}$, and $y_1,y_2,y_3$ are the three roots of $y^3-3y+2a_*=0$; that is
$$
\begin{aligned}
y_1&=2\cos[(\cos^{-1}a_*-\pi)/3], \\
y_2&=2\cos[(\cos^{-1}a_*+\pi)/3], \\
y_3&=-2\cos[(\cos^{-1}a_*)/3].
\end{aligned}
$$

## Slim Disks

In the thin disks, the accretion is radiatively efficient.
As the accretion rate is large, the radial velocity is large and the disk is thick enough, to trigger another cooling mechanism: advection.
Without the assumptions of radiative efficiency and Keplerian angular momentum, it is no longer possible to find an analytic solution to the system of equations.

![Fig 7](Fig7.png)

## ADAFs

The ADAF, or advection-dominated accretion flow, solution also involves cooling. It usually has low luminosity while the slim disk has high luminosity, because nearly all of the viscously dissipated energy is advected into the black hole rather than radiated.

Using scaling: $r_*=rc^2/GM$, $m=M/M_\odot$ and $\dot{m}=\dot{M}c^2/L_\text{Edd}$.
$$
\begin{aligned}
v &= [-3.00 \times 10^{10} \text{ cm~s}^{-1}]\alpha c_1 r_*^{-1/2}, \\
\Omega &= [2.03 \times 10^5 \text{ s}^{-1}] c_2 m^{-1} r_*^{-3/2}, \\
c_S^2 &= [9.00 \times 10^{20} \text{ cm~s}^{-2}] c_3 r_*^{-1}, \\
\rho &= [1.07 \times 10^{-5} \text{ g~cm}^{-3}] \alpha^{-1} c_1^{-1} c_3^{-1/2} m^{-1} \dot{m} r_*^{-3/2}, \\
P &= [9.67 \times 10^{15} \text{ g~cm}^{-1}~\text{s}^{-2}] \alpha^{-1} c_1^{-1} c_3^{1/2} m^{-1} \dot{m} r_*^{-5/2}, \\
B &= [4.93 \times 10^8 \text{ G}] \alpha^{-1/2} (1-\beta_m)^{1/2} c_1^{-1/2} c_3^{1/4} m^{-1/2} \dot{m}^{1/2} r_*^{-5/4}, \\
q^+ &= [2.94 \times 10^{21} \text{ erg~cm}^{-3}~\text{s}^{-1}] \epsilon^\prime c_3^{1/2} m^{-2} \dot{m} r_*^{-4}, \\
\tau_\mathrm{es} &= [1.75] \alpha^{-1} c_1^{-1} \dot{m} r_*^{-1/2},
\end{aligned}
$$
where $v$ is the radial infall velocity and $q^+$ is the viscous dissipation of energy per unit volume.
The constants $c_1,c_2,c_3$ are given by
$$
\begin{aligned}
c_1&=\frac{(5+2\varepsilon')}{3\alpha^2}g(\alpha,\varepsilon'), \\
c_2&=\left[\frac{2\varepsilon'(5+2\varepsilon')}{9\alpha^2}g(\alpha,\varepsilon')\right]^{1/2}, \\
c_3&=\frac{2(5+2\varepsilon')}{9\alpha^2}g(\alpha,\varepsilon'),
\end{aligned}
$$
where
$$
\begin{aligned}
\varepsilon'&=\frac{1}{f_\text{adv}}\left(\frac{5/3-\gamma_g}{\gamma_g-1}\right), \\
g(\alpha,\varepsilon')&\equiv\left[1+\frac{18\alpha^2}{(5+2\varepsilon')^2}\right]^{1/2}-1,
\end{aligned}
$$
and the parameter $f_\text{adv}$ represents the fraction of viscously dissipated energy which is advected. The remaining amount $1-f_\text{adv}$ is radiated locally.
