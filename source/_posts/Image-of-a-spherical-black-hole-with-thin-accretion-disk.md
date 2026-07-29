---
title: Image of a spherical black hole with thin accretion disk
math: true
date: 2026-05-29 17:15:11
categories:
    - relativity
tags:
    - black hole
    - Schwarzschild metric
---

- Luminet, J.-P. (1979). Image of a spherical black hole with thin accretion disk. *Astronomy and Astrophysics*, *75*(1-2), 228–235.

<!-- more -->

[pdf with notes](Image_of_a_spherical_black_hole_with_thin_accretion_disk.pdf)

## Image of a Bare Black Hole

- The Schwarzschild metric is
    $$
    \mathrm{d}s^2=-\left(1-\frac{2M}{r}\right)\mathrm{d}t^2+\left(1-\frac{2M}{r}\right)^{-1}\mathrm{d}r^2+r^2(\mathrm{d}\theta^2+\sin^2\theta\mathrm{d}\phi^2)
    $$
    the unit system is chosen such that $G=c=1$.
    The Schwarzschild radius $r_s=2M$.

- The trajectories of photon in the "equatorial" plane ( $\theta=\pi/2$ ) satisfy
    $$
    \left(\frac{1}{r^2}\frac{\mathrm{d}r}{\mathrm{d}\phi}\right)^2+\frac{1}{r^2}\left(1-\frac{2M}{r}\right)=\frac{1}{b^2}
    $$
    where $b=L/E$ is the impact parameter at infinity.

![Fig.1](fig1.png)

- Cirtical impact parameter $b_c=3\sqrt{3}M$, for $b<b_c$, rays are captured by the hole.

- The total deviation of the light ray $\mu$
    $$
    \mu=2\phi_\infty-\pi
    $$

    $$
    \phi_\infty=2\sqrt{\frac{P}{Q}}\int_{\zeta_\infty}^{\pi/2}(1-k^2\sin^2 x)^{-1/2}\mathrm{d}x
    $$

## Image of a Clothed Black Hole

![Fig.3](fig3.png)

- For a given emitter $M$, the observer will detect two images:
    a direct (or primary) image at $(b^{(\text{d})},\alpha)$
    a ghost (or secondary) image at $(b^{(\text{g})},\alpha+\pi)$

- The isoradial curve:
    Given $P$ (periastron)
    $$
    \cos\gamma=\cos\alpha(\cos^2\alpha+\cot^2\theta_0)^{-1/2}\tag{10}
    $$
    $$
    \frac{1}{r}=-\frac{Q-P+2M}{4MP}+\frac{Q-P+6M}{4MP}\text{sn}^2\left[\frac{\gamma}{2}\sqrt{\frac{P}{Q}}+F(\zeta_\infty,k)\right]\tag{13}
    $$
    $r=r(\gamma,P)=r(\alpha,P)\Rightarrow P=P(r,\alpha)$
    For a given angle $\theta_0$
    $$
    b=\frac{P^3}{P-2M}\tag{5}
    $$
    $b^{(\text{d})}=b^{(\text{d})}(P)=b^{(\text{d})}(r,\alpha)$
    For a constant $r$ from the hole, the isoradial curves we can see are $b^{(\text{d})}=b^{(\text{d})}(\alpha)$.

![Fig.4](fig4.png)
![Fig.5](fig5.png)
![Fig.6](fig6.png)

## Realistic Appearance of a Black Hole Accrection Disk

Consider the flux of radiation from the disk and the redshift $F^{\text{obs}}=F_S/(1+z)^4$

![Fig.9&10](fig9&10.png)
(The flux for the secondary image has not been depicted)
