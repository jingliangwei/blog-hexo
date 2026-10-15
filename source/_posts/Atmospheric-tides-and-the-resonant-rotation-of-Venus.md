---
title: Atmospheric tides and the resonant rotation of Venus
math: true
date: 2026-10-15 14:53:07
updated: 2026-10-15 14:53:07
categories:
    - planetary science
tags:
    - thermal tide
    - spin-orbit resonance
---

- Gold, T., & Soter, S. (1969). Atmospheric tides and the resonant rotation of Venus. *Icarus*, *11*(3), 356–366. https://doi.org/10.1016/0019-1035(69)90068-2

<!-- more -->

## Basic infomation of Venus

- The diurnal period: $P_{\rm sol,V}=116.75$ days
- The orbital period: $P_{\rm orb,V}=224.701$ days
- The (retrograde) sidereal period: $P_{\rm sid,V}=243.16$ days
- The synodic period of Venus and Earth: $S_{\rm VE}=583.92$ days

(Here days refer to the diurnal period of the Earth.)

Due to $5\cdot P_{\rm sol,V}=583.75\,{\rm days}\approx 583.92\,{\rm days}=S_{\rm VE}$,
the same side of Venus faces the Earth at each inferior conjunction.

## Introduction

$T_\oplus$: the action of the Earth upon the net permanent deformation (or transverse quadrupole moment) of Venus.

$T_\odot$: the constant drag of solar tidal friction on the body of Venus.

$T_\oplus$ only significant near inferior conjunction, while $T_\odot$ work constantly.

Need thermal atmospheric tides to balance the solar solid body tide $T_\odot$.

## Description of resonance and tides

- The transverse quadrupole moment of Venus: the shape, density inhomogeneities arising from mantle convection, and mascons (mass concentration)

- To maintain a resonant rotation: $T_\oplus\gtrapprox T_\odot$, but actually $T_\oplus\ll T_\odot$.
Simply assuming a large enough quadrupole moment for Venus requires a factor of 10 larger than that of Earth.

- Two observation:
    1. Arecibo Observatory place an upper bound upon the low-latitude surface relief of about $3$ km;
    2. Mariner V tracking data estimates the deviation from sphericity along the polar axis of at most a few hundred meters.

## Conventional resonant stability

- The principal moments of inertia for Venus are $A<B<C$, where $C$ is the moment about the spin axis.

![moment of inertia for Venus](moment_inertia.jpg)

- The torque from Earth, averaged over a synodic period, upon the permanent deformation of Venus is
$$
T_q=\frac{GM_\oplus M R^2}{2b^3}\frac{B-A}{C}K(q)
$$
where $G$ is the gravitational constant,
$M_\oplus$ is the Earth's mass,
$M$ and $R$ are the mass and radius of Venus,
$b$ is the astronomical unit (AU),
$(B-A)/C$ is a measure of the Venus transverse quadrupole moment,
and the dimensionless $K(q)$ are tabulated.

- The solid body tide:
$$
T_Q=-\frac{3}{2}\frac{k}{Q}\frac{GM_\odot^2 R^5}{a^6}=-5.3\times 10^{24}Q^{-1}\tag{3}
$$
here assume the tidal Love number $k=0.25$ same as the Earth,
and the quality factor $Q=100$ as Earth without surface water.

![Fig 3](fig3.jpg)

## Including atmospheric tides

- Why thermal instead of gravitational?
    gravitational surface pressure wave $\delta p=-\rho U$, with gravitational tidal potential due to the Sun or Moon of order $10^4\,{\rm cm}^2\,{\rm sec}^{-2}$;
    while thermal disturbance $\delta p=-\rho g\Delta z\dfrac{\delta T}{T}$, only need $10^{-2}\,{\rm K}$ to equivalent to that over a range $\Delta z$ of several kilometers.

- The semidiurnal pressure wave on Earth may by represented empirically
$$
\delta p=1.16\sin^3\theta\cos 2(\lambda-146^\circ)\,{\rm mb}
$$
where $\theta$ is co-latitude and $\lambda$ is longitude measured in the sense of rotation from the subsolar meridian.
![wave on Earth](wave_earth.png)

- Thermal tide on Venus:
$$
T_P=7.7\times 10^{22} P\tag{5}
$$
with $P\equiv -p_2\sin 2\epsilon_2$.

- The condition for $T_Q+T_P\approx 0$ is
$$
QP\approx 70\tag{6}
$$

![Fig 5](fig5.png)

- About Fig 5:
    1. Stability of a resonance is a necessary but not a sufficient condition for capture;
    2. In the absence of any interaction with the Earth, Venus would spin down to the rate where atmospheric torque just balanced body torque (point '0' in Fig 5);
    3. More pair of $P,Q$ can achieve the capture at $q=-5$;
    4. Venus is assembled initially with a spin in the range between fast retrograde and direct but slower than solar synchronous.
