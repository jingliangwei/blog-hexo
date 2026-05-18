---
title: 'Chaotic dynamics in a strained rotating flow: a precessing plane fluid layer'
math: true
date: 2026-05-18 13:21:06
categories:
    - fluid
tags:
    - instability
    - precessing flow
    - rotating flow
    - inertial waves
---

Mason, R. M., & Kerswell, R. R. (2002). Chaotic dynamics in a strained rotating flow: A precessing plane fluid layer. *Journal of Fluid Mechanics*, *471*, 71–106. https://doi.org/10.1017/S0022112002001994

<!-- more -->

## The inertial waves

The inertial waves which statisfy
$$
\frac{\partial\vec{u}}{\partial t}+2\hat{z}\times\vec{u}+\nabla p=0,
$$
$$
\nabla\cdot\vec{u}=0,\quad w(x,y,\pm\frac{1}{2})=0,
$$
are
$$
\left[\begin{array}{c} u \\ v \\ w \\ p\end{array}\right]=
\left(
\begin{array}{c}
k^2(k_x\lambda-2ik_y)\cos(n\pi[z+\frac{1}{2}])/4k_\perp^2 \\
k^2(k_y\lambda+2ik_x)\cos(n\pi[z+\frac{1}{2}])/4k_\perp^2 \\
-ik_z\sin(n\pi[z+\frac{1}{2}])/\lambda \\
\cos(n\pi[z+\frac{1}{2}])
\end{array}
\right)
\exp(i(k_xx+k_yy+\lambda t)).\tag{4.4}
$$

{% note info %}
The derivation:
$$
\left\{
\begin{array}{l}
\dfrac{\partial\vec{u}}{\partial t}+2\hat{z}\times\vec{u}+\nabla p=0 \\
\left[
    \begin{array}{c}
    \vec{u} \\
    p
    \end{array}
\right]=
\left[
    \begin{array}{c}
    u \\
    v \\
    w \\
    p
    \end{array}
\right]\exp(i(k_xx+k_yy+\lambda t))
\end{array}
\right.\Rightarrow
\left\{
\begin{array}{l}
u=u(p) \\
v=v(p) \\
w=w(p)
\end{array}
\right.\rightarrow \nabla\cdot\vec{u}=0 \Rightarrow p
$$
{% endnote %}
