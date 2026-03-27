---
title: >-
  Theory and modeling of rotating fluids: convection, inertial waves and
  precession
math: true
date: 2026-03-26 22:15:53
update: 2026-03-27 23:30:00
categories:
  - fluid
tags:
  - rotating flow
  - inertial waves
excerpt:
  The inertial wave modes in rotating flow.
---

[https://doi.org/10.1017/9781139024853](https://doi.org/10.1017/9781139024853)

## 2 Introduction

### 2.1 Formulation

Equations:
$$
\frac{\partial \boldsymbol{u}}{\partial t}+2\hat{\boldsymbol{z}}\times\boldsymbol{u}+\nabla p=0 \tag{2.7}
$$
$$
\nabla\cdot\boldsymbol{u}=0 \tag{2.8}
$$

Assuming solutions:
$$
\boldsymbol{u}(\boldsymbol{r},t)=\boldsymbol{u}(\boldsymbol{r})e^{i2\sigma t},\ p(\boldsymbol{r},t)=p(\boldsymbol{r})e^{i2\sigma t} \tag{2.9}
$$

### 2.2 Frequency Bound

The half-frequency bound:
$$
-1\le \sigma \le 1
$$

### 2.5 The Poincaré Equation

$$
\nabla^2 p-\frac{1}{\sigma^2}(\hat{\boldsymbol{z}}\cdot\nabla)^2 p=0 \tag{2.47}
$$

## 3 Inertial Modes in Rotating Narrow-gap Annuli

### 3.1 Formulation

![Fig 3.1](3-1.jpg)

$$
2i\sigma\hat{\boldsymbol{x}}\cdot\boldsymbol{u}-2\hat{\boldsymbol{y}}\cdot\boldsymbol{u}+\frac{\partial p}{\partial x}=0 \tag{3.1}
$$
$$
2i\sigma\hat{\boldsymbol{y}}\cdot\boldsymbol{u}+2\hat{\boldsymbol{x}}\cdot\boldsymbol{u}+\frac{\partial p}{\partial y}=0 \tag{3.2}
$$
$$
2i\sigma\hat{\boldsymbol{z}}\cdot\boldsymbol{u}+\frac{\partial p}{\partial z}=0 \tag{3.3}
$$

### 3.2 Axisymmetric Inertial Oscillations

We often employ a triple index notation, for example, $\boldsymbol{u}_{mnk}$ and $\sigma_{mnk}$, to denote an axisymmetric oscillation mode:

| index | repersent |
|:---:|:---:|
| $m$ | the angular structure |
| $n$ | the vertical structure |
| $k$ | the radial structure |

The axisymmetric inertial oscillation mode:
$$
\hat{\boldsymbol{x}}\cdot\boldsymbol{u}_{0nk}=\left[\frac{k\pi}{2\Gamma(1-\sigma_{0nk}^2)}\right]\sin\left(\frac{k\pi y}{\Gamma}\right)\cos n\pi z \tag{3.13}
$$
$$
\hat{\boldsymbol{y}}\cdot\boldsymbol{u}_{0nk}=\left[\frac{i\sigma_{0nk} k\pi}{2\Gamma(1-\sigma_{0nk}^2)}\right]\sin\left(\frac{k\pi y}{\Gamma}\right)\cos n\pi z \tag{3.14}
$$
$$
\hat{\boldsymbol{z}}\cdot\boldsymbol{u}_{0nk}=-\left(\frac{in\pi}{2\sigma_{0nk}}\right)\cos\left(\frac{k\pi y}{\Gamma}\right)\sin n\pi z \tag{3.15}
$$
with the half-frequency
$$
\sigma_{0nk}=\pm\frac{n\Gamma}{\sqrt{(\Gamma n)^2+k^2}} \tag{3.16}
$$

### 3.4 Non-axisymmetric Inertial Waves

$$
\hat{\boldsymbol{x}}\cdot\boldsymbol{u}_{mnk}=\frac{1}{2}\left[\frac{n^2\pi^2}{\sigma_{mnk}}\sin\left(\frac{k\pi y}{\Gamma}\right)-\frac{km\pi}{\Gamma}\cos\left(\frac{k\pi y}{\Gamma}\right)\right]\cos n\pi z\  e^{imx} \tag{3.31}
$$
$$
\hat{\boldsymbol{y}}\cdot\boldsymbol{u}_{mnk}=\frac{i}{2}\left[\left(n^2\pi^2+m^2\right)\sin\left(\frac{k\pi y}{\Gamma}\right)\right]\cos n\pi z\  e^{imx} \tag{3.32}
$$
$$
\hat{\boldsymbol{z}}\cdot\boldsymbol{u}_{mnk}=-\frac{i}{2}\left[\frac{mn\pi}{\sigma_{mnk}}\sin\left(\frac{k\pi y}{\Gamma}\right)+\frac{nk\pi^2}{\Gamma}\cos\left(\frac{k\pi y}{\Gamma}\right)\right]\sin n\pi z\  e^{imx} \tag{3.33}
$$
with the half-frequency
$$
\sigma_{mnk}=\pm\frac{n\pi}{\sqrt{n^2\pi^2+m^2+(k\pi/\Gamma)^2}} \tag{3.34}
$$
