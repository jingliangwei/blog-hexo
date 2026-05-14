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
