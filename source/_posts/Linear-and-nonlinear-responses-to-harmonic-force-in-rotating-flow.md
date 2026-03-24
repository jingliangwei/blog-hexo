---
title: Linear and nonlinear responses to harmonic force in rotating flow
date: 2026-03-24 12:08:00
math: true
categories:
    - fluid
tags:
    - rotating flow
    - linear solution
excerpt:
    The linear solution for rotating flow under a harmonic force.
---

link: [http://doi.org/10.1017/jfm.2016.267](http://doi.org/10.1017/jfm.2016.267)

[pdf with notes](linear-and-nonlinear-responses-to-harmonic-force-in-rotating-flow.pdf)

## Equations

$$
\frac{\partial \boldsymbol{u}}{\partial t}+\boldsymbol{u}\cdot\nabla\boldsymbol{u}=-\nabla p+E\nabla^2\boldsymbol{u}+2\boldsymbol{u}\times\hat{\boldsymbol{z}}+\boldsymbol{f}
$$

where the Ekman number $E=\nu/(\Omega l^2)$ is the ratio of viscous time scale over rotational time scale.

$$
\boldsymbol{f}=\text{Re}\{\hat{\boldsymbol{f}}e^{i(\boldsymbol{k}\cdot\boldsymbol{x}-\omega t)}\},\quad \nabla\times\boldsymbol{f}=k\boldsymbol{f}
$$

## Linear regime

$$
\frac{\partial \boldsymbol{u}}{\partial t}=-\nabla p+E\nabla^2\boldsymbol{u}+2\boldsymbol{u}\times\hat{\boldsymbol{z}}+\boldsymbol{f}
$$

Assuming $\boldsymbol{u}=\text{Re}\{\hat{\boldsymbol{u}}e^{i(\boldsymbol{k}\cdot\boldsymbol{x}-\omega t)}\},p=\text{Re}\{\hat{p}e^{i(\boldsymbol{k}\cdot\boldsymbol{x}-\omega t)}\}$, and the solution is

$$
\hat{\boldsymbol{u}}=\frac{ik\hat{\boldsymbol{f}}}{2k_z+k(\omega+iEk^2)}
$$
