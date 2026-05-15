---
title: Negative heat capacity
math: true
date: 2026-05-14 21:41:10
categories:
    - thermodynamics
tags:
    - negative heat capacity
excerpt:
    Introduction to negative heat capacity in astrophysical systems.
---

Velazquez, L. (2016). Remarks about the thermodynamics of astrophysical systems in mutual interaction and related notions. *Journal of Statistical Mechanics: Theory and Experiment*, *2016*(3), 033105. https://doi.org/10.1088/1742-5468/2016/03/033105

## Eddington's idea

From the virial theorem in a radial potential field $W\propto 1/r$ which reads
$$
\langle K\rangle=-\frac{\langle W\rangle}{2},
$$
we have the total energy
$$
\langle U\rangle=\langle K\rangle+\langle W\rangle=-\langle K\rangle.
$$
Assuming the equipartition relation between kinetic energy and temperature $\langle K\rangle=3NkT/2$, we have
$$
\langle U\rangle=-\frac{3NkT}{2}\Rightarrow C=\frac{\mathrm{d}\langle U\rangle}{\mathrm{d}T}=-\frac{3Nk}{2}<0,
$$
which argues that the heat capacity of astrophysical systems could be negative.

## Thirring stability conditions

Considering a closed system composed of two finite systems A and B, let us assume that the total energy $U_T$ and entropy $S_T$ of the closed system are additive quantities, i.e., $U_T=U_A+U_B$ and $S=S_A+S_B$. Maximization of entropy $S_T$ at constant energy $U_T$ demands the stability condition:
$$
\frac{\partial^2 S_T}{\partial U_A^2}=\frac{\partial^2 S_A}{\partial U_A^2}+\frac{\partial^2 S_B}{\partial U_B^2}<0 \Rightarrow \frac{C_A C_B}{C_A+C_B}>0,
$$
where $C_A$ and $C_B$ are heat capacities of these systems.

{% fold info @detailed derivation %}
$$
\frac{\partial S_T}{\partial U_A}=\frac{\partial S_A}{\partial U_A}-\frac{\partial S_B}{\partial U_B}=0\Rightarrow \frac{1}{T_A}=\frac{1}{T_B}\left(\equiv\frac{1}{T}\right),
$$
$$
\frac{\partial^2 S}{\partial U^2}=\frac{\partial}{\partial U}\left(\frac{1}{T}\right)=-\frac{1}{T^2}\left(\frac{\partial T}{\partial U}\right)=-\frac{1}{T^2 C}.
$$
{% endfold %}

## A paradox

According to Thirring stability conditions, two systems with negative heat capacities cannot remain in equilibrium.
But what about binary stars? Two separable astrophysical systems in mutual interaction could support an additive total entropy $S_T\simeq S_A+S_B$. However, their total energy $U_T$ cannot be expressed as the sum of their respective internal energies as $U_T\neq U_A+U_B$ because of the long-range character of gravitation.

So, it's necessary to perform a re-examination of Thirring stability analysis for astrophysical situations.

## Revisit thermal equilibrium condition

Consider two astrophysical systems A and B in mutual gravitational interaction. For each system, the internal degrees of freedom are the positions and their momenta $\{\vec{r}_i,\vec{p}_i\}$ relative to their own center of mass, while the collective degrees of freedom $(\vec{R},\vec{P})$ refer to the relative separation vector of the centers of mass and its momentum. The Hamiltonian $H$ of this closed system can be expressed as:
$$
H=H_A+H_B+W_{AB},
$$
$$
H_\alpha=\sum_{i_\alpha}\frac{1}{2m_{i_\alpha}}\vec{p}^2_{i_\alpha}-\sum_{i_\alpha<j_\alpha}\frac{Gm_{i_\alpha}m_{j_\alpha}}{|\vec{r}_{i_\alpha}-\vec{r}_{j_\alpha}|},\quad \alpha=A,B,
$$
$$
W_{AB}=\frac{1}{2\mu_{AB}}\vec{P}^2-\sum_{i_A i_B}\frac{Gm_{i_B}m_{i_A}}{|\vec{R}+\vec{r}_{i_A}-\vec{r}_{i_B}|}.
$$

Then the additivity of the total energy $U_T=U_A+U_B$ is now replaced by the following constraint:
$$
U_T=U_A+U_B+W(U_A,U_B|D),
$$
$$
\mathrm{d}U_T=\left[1+\left(\frac{\partial W}{\partial U_A}\right)\right]\mathrm{d}U_A+\left[1+\left(\frac{\partial W}{\partial U_B}\right)\right]\mathrm{d}U_B\equiv\phi_A^{-1}\mathrm{d}U_A+\phi_B^{-1}\mathrm{d}U_B,
$$
and the stability condition:
$$
\frac{\partial^2 S_T}{\partial U_A^2}<0\Rightarrow \phi_A\left[\frac{C_A+C_B}{C_AC_B}-\frac{1}{\eta}\left(\frac{\partial \phi_A}{\partial U_A}+\frac{\partial \phi_B}{\partial U_B}\right)\right]>0.
$$

## Stability of a binary system

Now expand the collective motions $W_{AB}$ using quadrupole terms
$$
W_{AB}=\frac{\vec{P}^2}{2\mu}-\frac{\alpha}{|\vec{R}|}-\frac{\alpha\Theta}{|\vec{R}|^6},
$$
where
$$
\mu=\frac{M_AM_B}{M_A+M_B},\alpha=GM_AM_B,\Theta=\frac{\xi_A(6\xi_A+1)q_A+\xi_B(6\xi_B+1)q_B}{2\xi_A\xi_B},
$$
$$
\xi_A=\frac{M_B}{M_A+M_B},\xi_B=\frac{M_A}{M_A+M_B},q_A=\frac{9}{16\pi^2}\frac{M_AkT_A}{G\rho_A^2},q_B=\frac{9}{16\pi^2}\frac{M_BkT_B}{G\rho_B^2}.
$$

The effective potential reads
$$
W_\text{ef}(R)=\frac{\vec{M}^2}{2\mu R^2}-\frac{\alpha}{R}-\frac{\alpha\Theta}{R^6}.
$$

![Fig11](F11.png)

Two critical values for quadrupole parameter $\Theta$:
$$
\Theta_c=\frac{1}{4}\left(\frac{2M^2}{5\mu a}\right)^5,\Theta_s=\frac{1}{24}\left(\frac{4M^2}{5\mu a}\right)^5.
$$

Stability and instability situations:
- $\Theta\le\Theta_c$: the binary system is always stable due to $U_C<0$;
- $\Theta_c <\Theta<\Theta_s$: the system only stable within a certain energy window $U_\text{min}\le U_C<U_\text{max}<0$, while the system is unstable and finally collapses to form a single structure within energy window $U_\text{max}<U_C<0$;
- $\Theta\ge\Theta_s$: the system is always unstable.
