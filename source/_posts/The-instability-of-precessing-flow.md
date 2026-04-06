---
title: The instability of precessing flow
math: true
date: 2026-04-06 14:23:48
categories:
    - fluid
tags:
    - instability
    - precessing flow
    - rotating flow
    - inertial waves
excerpt:
    The shearing and elliptical instability of precessing flow.
---

[https://doi.org/10.1080/03091929308203609](https://doi.org/10.1080/03091929308203609)

[pdf with notes](The_instability_of_precessing_flow.pdf)

## Parameters

| Parameters | Expression |
|:---|:---|
| Oblateness | $\eta,c$: $r^2+(1+\eta)z^2=r^2+\dfrac{z^2}{c^2}=1$ |
| Precessional vector | $\boldsymbol{\Omega}=[\Omega_1,0,\Omega_3]^T$ |
| Shearing of the streamlines | $\varepsilon=\dfrac{\eta\mu}{2+(2+\eta)\mu^2}$ |
| Elliptical distortion of the streamlines | $\beta=\dfrac{\eta\mu^2}{2+(2+\eta)\mu^2}$ |
| Relative magnitude of elliptical over shearing | $\mu=\dfrac{2\Omega_1}{\eta+2(1+\eta)\Omega_3}$ |

## 1 Formulation

### Poincaré's solution

$$
\boldsymbol{u}=\boldsymbol{\omega}\times\boldsymbol{r}+\nabla A
$$
$$
\boldsymbol{\omega}=\hat{\boldsymbol{z}}-\frac{2+\eta}{\eta+2(1+\eta)\boldsymbol{\Omega}\cdot\hat{\boldsymbol{z}}}\hat{\boldsymbol{z}}\times(\hat{\boldsymbol{z}}\times\boldsymbol{\Omega})
$$
$$
A=\frac{\eta}{\eta+2(1+\eta)\boldsymbol{\Omega}\cdot\hat{\boldsymbol{z}}}(\boldsymbol{\Omega}\times\hat{\boldsymbol{z}}\cdot\boldsymbol{r})(\hat{\boldsymbol{z}\cdot\boldsymbol{r}})
$$

![Poincaré flow](poincare_flow.jpg)

### Derivation of equation

From $\boldsymbol{u}=u_x\hat{\boldsymbol{x}}+u_y\hat{\boldsymbol{y}}+u_z\hat{\boldsymbol{z}}$ to $\boldsymbol{u}=u\tilde{\boldsymbol{s}}+v\tilde{\boldsymbol{\phi}}+w\tilde{\bar{\boldsymbol{z}}}$

$$
\boldsymbol{u}=\frac{2+(2+\eta)\mu^2}{2\sqrt{1+\mu^2}}\sqrt{1-\beta^2}s\tilde{\boldsymbol{\phi}}=\bar{\Omega}s\tilde{\boldsymbol{\phi}} \tag{1.6}
$$

The momentum equation projecting onto $\tilde{\boldsymbol{l}},\tilde{\boldsymbol{m}},\tilde{\boldsymbol{n}}$ reads
$$
\begin{align}
\frac{\partial u}{\partial t}+&(\boldsymbol{u}\cdot\nabla)u-\frac{v^2}{s}-2\left(\frac{\Omega_3^*+\Omega_1^*\varepsilon}{\sqrt{1-\beta^2}}\right)v+\frac{1}{(1-\beta^2)}\left[1+\frac{2\varepsilon^2}{1+\beta}\right]\frac{\partial p}{\partial s} \\
=&\frac{2\varepsilon\cos\phi}{\sqrt{1+\beta}\sqrt{1-\beta^2}}\frac{\partial p}{\partial\bar{z}}+\frac{2\sin\phi}{\sqrt{1+\beta}}\left(\Omega_1^*-\frac{2\Omega_3^*\varepsilon}{\sqrt{1+\beta}}\right)w \\
&+\cos 2\phi\left\{\frac{2(\Omega_1^*\varepsilon+\Omega_3^*\beta)}{\sqrt{1-\beta^2}}v-\frac{1}{(1-\beta^2)}\left[\beta+\frac{2\varepsilon^2}{1+\beta}\right]\frac{\partial p}{\partial s}\right\} \\
&+\sin 2\phi\left\{\frac{2(\Omega_1^*\varepsilon+\Omega_3^*\beta)}{\sqrt{1-\beta^2}}u+\frac{1}{(1-\beta^2)}\left[\beta+\frac{2\varepsilon^2}{1+\beta}\right]\frac{1}{s}\frac{\partial p}{\partial \phi}\right\}
\end{align}
\tag{1.7}
$$
$$
\begin{align}
\frac{\partial v}{\partial t}+&(\boldsymbol{u}\cdot\nabla)v-\frac{uv}{s}+2\left(\frac{\Omega_3^*+\Omega_1^*\varepsilon}{\sqrt{1-\beta^2}}\right)u+\frac{1}{(1-\beta^2)}\left[1+\frac{2\varepsilon^2}{1+\beta}\right]\frac{1}{s}\frac{\partial p}{\partial \phi} \\
=&-\frac{2\varepsilon\sin\phi}{\sqrt{1+\beta}\sqrt{1-\beta^2}}\frac{\partial p}{\partial\bar{z}}+\frac{2\cos\phi}{\sqrt{1+\beta}}\left(\Omega_1^*-\frac{2\Omega_3^*\varepsilon}{1+\beta}\right)w \\
&+\cos 2\phi\left\{\frac{2(\Omega_1^*\varepsilon+\Omega_3^*\beta)}{\sqrt{1-\beta^2}}u+\frac{1}{(1-\beta^2)}\left[\beta+\frac{2\varepsilon^2}{1+\beta}\right]\frac{1}{s}\frac{\partial p}{\partial \phi}\right\} \\
&+\sin 2\phi\left\{-\frac{2(\Omega_1^*\varepsilon+\Omega_3^*\beta)}{\sqrt{1-\beta^2}}v+\frac{1}{(1-\beta^2)}\left[\beta+\frac{2\varepsilon^2}{1+\beta}\right]\frac{\partial p}{\partial s}\right\}
\end{align}
\tag{1.8}
$$
$$
\begin{align}
\frac{\partial w}{\partial t}+(\boldsymbol{u}\cdot\nabla)w+\frac{\partial p}{\partial \bar{z}}=&-\sin\phi\left[\frac{2\varepsilon}{\sqrt{1+\beta}\sqrt{1-\beta^2}}\frac{1}{s}\frac{\partial p}{\partial \phi}+2\Omega_1^*\sqrt{1+\beta}u\right] \\
&+\cos\phi\left[\frac{2\varepsilon}{\sqrt{1+\beta}\sqrt{1-\beta^2}}\frac{\partial p}{\partial s}-2\Omega_1^*\sqrt{1+\beta}v\right]
\end{align}
\tag{1.9}
$$

Consider small disturbances $\boldsymbol{u}$ upon the basic state $\boldsymbol{U}=\bar{\Omega}s\tilde{\phi}$ in a **frame rotating with this flow**,
$$
\frac{\partial \boldsymbol{u}^*}{\partial t^*}+2\hat{\boldsymbol{z}}\times\boldsymbol{u}^*+\bar{\nabla}p=\cdots\mathscr{L}(\cdots) \tag{1.11}
$$

### Scale of parameters

For the earth,
$$
\Omega_1=4\times 10^{-8}\ll\eta\approx\frac{1}{200}\ll 1
$$

The hierachy,
$$
\varepsilon^2,\beta\ll\varepsilon\ll 1 \tag{1.18}
$$

### Shearing and elliptical parts

$$
\begin{align}
\frac{\partial \boldsymbol{u}}{\partial t}+2\left[\begin{array}{c}-v \\ u \\ 0 \end{array}\right]+\bar{\nabla}p=&\varepsilon\left[e^{i(\phi+t)}\mathscr{L}_S(\boldsymbol{u},p)+e^{-i(\phi+t)}\mathscr{L}_S^*(\boldsymbol{u},p)\right] \\
&-\frac{1}{2}\beta\left[e^{2i(\phi+t)}\mathscr{L}_E(\boldsymbol{u},p)+e^{-2i(\phi+t)}\mathscr{L}_E^*(\boldsymbol{u},p)\right]
\end{align}\tag{1.22}
$$

## 2 The shearing instability

### Poincaré mode

The Poincaré mode $[\boldsymbol{u}(\boldsymbol{x},t),p(\boldsymbol{u},t)]=[\boldsymbol{Q}_{n,m,k}(\boldsymbol{x}),\Phi_{n,m,k}(\boldsymbol{x})]e^{i\lambda t}$ when $\varepsilon=\beta=0$
$$
\boldsymbol{Q}_{n,m,k}=\left[\begin{array}{c}
\dfrac{-i}{4-\lambda^2}\left(\lambda\Phi_r+\dfrac{2m}{r}\Phi\right) \\
\dfrac{1}{4-\lambda^2}\left(2\Phi_r+\dfrac{m\lambda}{r}\Phi\right) \\
\dfrac{i}{\lambda}\Phi_z
\end{array}\right]e^{i(m\phi+\lambda t)} \tag{2.1}
$$
the eigenfrequency $\lambda$
$$
\nu+2\sum_1^N \frac{\lambda^2c^2}{\lambda^2c^2-\bar{x}_j^2\{4-\lambda^2(1-c^2)\}}=\frac{mc^2\lambda}{2-\lambda} \tag{2.4}
$$

### Shearing resonance condition

Assuming $\varepsilon\neq 0$ and ignoring $\beta$ for this section, consider perturbation to the basic flow (1.6)
$$
\boldsymbol{u}=A(t)\boldsymbol{Q}_a+B(t)\boldsymbol{Q}_b+\varepsilon \boldsymbol{u}_1+\mathrm{O}(\varepsilon^2)
$$

Projecting equation (1.22) onto $\boldsymbol{Q}_a$ and $\boldsymbol{Q}_b$, the resonance conditions read,
$$
m_b=m_a+1
$$
$$
n_b=n_a
$$
$$
-2\varepsilon\sqrt{(1+\lambda_a)(1-\lambda_b)}|I|<\lambda_b-\lambda_a-1<2\varepsilon\sqrt{(1+\lambda_a)(1-\lambda_b)}|I|
$$

so the interaction integral read,
$$
\begin{align}
\langle\boldsymbol{Q}_a,e^{-i\phi}\mathscr{L}_S^*\rangle&=(1-\lambda_b)I,\\
\langle\boldsymbol{Q}_b,e^{i\phi}\mathscr{L}_S\rangle&=(1+\lambda_a)I^*
\end{align} \tag{2.7}
$$

## 3 The elliptical instability

In the case that $\varepsilon^2,\beta\ll\varepsilon\ll 1$
$$
\boldsymbol{u}=A\boldsymbol{Q}_a+B\boldsymbol{Q}_b+\varepsilon[\boldsymbol{v}_{11}e^{i(\lambda_a-1)t}+\boldsymbol{v}_{12}e^{i(\lambda_a+1)t}+\boldsymbol{v}_{13}e^{i(\lambda_b+1)t}]+\beta \boldsymbol{v}_2+\mathrm{O}(\varepsilon\beta)
$$

## 4 Exact linear solutions

Taking precessional vector $\boldsymbol{\Omega}=\Omega\hat{\boldsymbol{x}}$ (that is $\Omega_1=\Omega, \Omega_3=0$ ), the Poincaré's basic state can be written as
$$
\boldsymbol{U}=\left[\begin{array}{ccc}
    0 & -1 & 0 \\
    1 & 0 & -(1+\eta)\mu \\
    0 & \mu & 0
\end{array}\right]\boldsymbol{x}=\boldsymbol{A}\cdot\boldsymbol{x}\tag{4.1}
$$

The linearised disturbance equations in the **precessing frame** are
$$
\frac{\partial \boldsymbol{u}}{\partial t}+2\boldsymbol{\Omega}\times\boldsymbol{u}+\boldsymbol{A}\cdot\boldsymbol{x}\cdot\nabla\boldsymbol{u}+\boldsymbol{A}\cdot\boldsymbol{u}+\nabla p=\boldsymbol{0} \tag{4.2}
$$

The orthogonal vector spaces $\mathscr{V}_n$
$$
\mathscr{V}_n=\langle\boldsymbol{Q}_{nmk};-n\le m\le n,k=1,...,k_{max}(n,m)\rangle
$$

### 4.1 Linear velocities

$$
\mathscr{V}_2=\{\boldsymbol{Q}_{2,-1,1},\boldsymbol{Q}_{2,0,1},\boldsymbol{Q}_{2,1,1}\}
$$
$$
\boldsymbol{u}(\boldsymbol{x},t)=\sum_{i=1}^3 \alpha_i(t)\boldsymbol{u}_i(\boldsymbol{x})
$$
$$
\alpha_i(t)=\alpha_i e^{\sigma t}
$$
Three eigenfrequencies are
$$
\sigma_1=0,\quad \sigma_2=i\kappa,\quad \sigma_3=-i\kappa,\quad \kappa=\frac{1-c^2}{1+c^2}
$$

No instability in $\mathscr{V}_2$, need to consider quadratic disturbances.

### 4.2 Quadratic velocities

$$
\mathscr{V}_3=\{\boldsymbol{Q_{3,-2,1}},\boldsymbol{Q_{3,-1,1}},\boldsymbol{Q_{3,-1,2}},\boldsymbol{Q_{3,0,1}},\boldsymbol{Q_{3,0,2}},\boldsymbol{Q_{3,1,1}},\boldsymbol{Q_{3,1,2}},\boldsymbol{Q_{3,2,1}}\}
$$

![Figure 3](F3.png)

## 5 Unbounded sheared, circular streamlines

The unbounded basic flow is
$$
\boldsymbol{u}=\left[\begin{array}{ccc}
    0 & -1 & 0 \\
    1 & 0 & -2\varepsilon \\
    0 & 0 & 0
\end{array}\right]\boldsymbol{x}=\boldsymbol{D}\cdot\boldsymbol{x}\tag{5.1}
$$

The perturbation equation is
$$
\frac{\mathrm{d}\hat{\boldsymbol{u}}}{\mathrm{d}t}+\boldsymbol{D}\cdot\hat{\boldsymbol{u}}+2\boldsymbol{\Omega}\times\hat{\boldsymbol{u}}+i\boldsymbol{k}\hat{p}=0 \tag{5.3}
$$

### Floquet method

$$
\frac{\mathrm{d}\hat{u}_i}{\mathrm{d}t}=A_{il}\hat{u}_l
$$
this is a Floquet problem, $\hat{\boldsymbol{u}}$ has a growth rate
$$
\bar{\sigma}(\alpha,\varepsilon)=\frac{1}{2\pi}\ln|\mu|
$$
where $\mu$ is the eigenvalue of matrix $\boldsymbol{M}(2\pi)$.

![Figure 4](F4.png)

### Perturbation method

$$
\hat{\boldsymbol{u}}=[\hat{\boldsymbol{u}}_0(t)+\varepsilon\hat{\boldsymbol{u}}_1(t)+\mathrm{O}(\varepsilon^2)]e^{\sigma\varepsilon t}
$$
$$
\left\langle\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{1}{2}|\hat{\boldsymbol{u}}|^2\right)\right\rangle=\varepsilon\tan\alpha\left[\frac{\gamma+1}{2}\right]\left\langle\cos\left(\frac{4}{\gamma}-1\right)t\right\rangle+\mathrm{O}(\varepsilon^2)
$$
For $\varepsilon\rightarrow 0$, growth occurs only at $\gamma=4,2,\dfrac{4}{3},1$ or $\cos\alpha=\dfrac{1}{4},\dfrac{1}{2},\dfrac{3}{4},1$.

## 6 Discussion

Considering viscous, a pair of inertial waves can only grow if their joint rate of excitation exceeds the viscous decay rates.
