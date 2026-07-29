---
title: >-
  The excitation of density waves at the Lindblad and corotation resonances by
  an external potential
math: true
date: 2026-07-25 21:32:48
categories:
  - fluid
tags:
  - density wave
---

- Goldreich, P., & Tremaine, S. (1979). The excitation of density waves at the Lindblad and corotation resonances by an external potential. *The Astrophysical Journal*, *233*, 857–871. https://doi.org/10.1086/157448
- Armitage, P. J. (2020). *Astrophysics of planet formation* (2nd ed.). Cambridge University Press. https://doi.org/10.1017/9781108344227
- Feldman, S. I., & Lin, C. C. (1973). A forcing mechanism for spiral density waves in galaxies. *Studies in Applied Mathematics*, *52*(1), 1–20. https://doi.org/10.1002/sapm19735211

<!-- more -->

## Basic Equations

The unperturbed state:
  - angular velocity $\Omega(r)$
  - velocity $\boldsymbol{v}_0=r\Omega(r)\hat{e}_\theta$
  - surface density $\sigma_0$
  - gravitational potential (of central star) $\varphi_0(r)$
  - external potential (e.g. gravitation from planet) $\varphi_1$
  - sound speed $c_0$

The perturbed values:
  - velocity $\boldsymbol{v}_1$
  - surface density $\sigma_1$
  - gravitational potential $\varphi_1^D$

The homogeneous free-wave solution
  $$
  \varphi_1^D(r)=\Phi(r)\exp\left[i\int^r k(s)\mathrm{d}s\right]\exp[i(m\theta-\omega t)]
  $$
  with dispersion relation
  $$
  D+(kc_0)^2-2\pi G\sigma_0|k|=0\tag{18a}
  $$
  where $D=\kappa^2-(m\Omega-\omega)^2$

- Leading wave $k<0$
  Trailing wave $k>0$

- Lindblad resonance $D=0$
  corotation resonance $m\Omega-\omega=0$

  temporal angular frequency $\omega$
  pattern speed $\Omega_p$
  $\omega=m\Omega_p$

  take Keplerian rotation as example, i.e., $\Omega_p=r_p^{-3/2}$, $\Omega=\kappa=r^{-3/2}$
  $D=(\kappa-m\Omega+m\Omega_p)(\kappa+m\Omega-m\Omega_p)=[(1-m)r^{-3/2}+mr_p^{-3/2}][(1+m)r^{-3/2}-mr_p^{-3/2}]$
  the inner Lindblad resonance $r_\text{ILR}=r_p\left(\dfrac{m-1}{m}\right)^{2/3}$
  the outer Lindblad resonance $r_\text{OLR}=r_p\left(\dfrac{m+1}{m}\right)^{2/3}$
  $m\Omega-\omega=0$ gives the corotation resonance $r_\text{CR}=r_p$

  the sign of $D$ is

  | $0<r<r_\text{ILR}$ | $r=r_\text{ILR}$ | $r_\text{ILR}<r<r_\text{OLR}$ | $r=r_\text{OLR}$ | $r>r_\text{OLR}$ |
  |:---:|:---:|:---:|:---:|:---:|
  | $D<0$ | $D=0$ | $D>0$ | $D=0$ | $D<0$ |

  for 'long waves', from
  $$
  |k|=\frac{\pi G\sigma_0}{c_0^2}-\left[\left(\frac{\pi G\sigma}{c_0^2}\right)^2-\frac{D}{c_0^2}\right]^{1/2}\tag{19}
  $$
  if $D<0$, the waves will decay exponentially.

## Lindblad Resonances

The torque that the external potential exerts on the disk is
| inner Lindblad resonance | outer Lindblad resonance |
|:---:|:---:|
| negative | positive |

so the angular momentum is transported from ILR to OLR by the long waves while the matter only oscillates locally.

The matter at ILR loses angular momentum and migrates inward, while the matter at OLR gains angular momentum and migrates outward.

{% note info %}
Note that the Lindblad 'resonance' is **not a true resonance** of a fluid disk, but only a region where the disk is strongly coupled to the external potential.
{% endnote %}

## Corotation Resonances

Without self-gravity: no density waves can propagate between the inner and outer Lindblad resonances

With self-gravity:
Only short trailing waves are excited with the same strength on both side of corotation.

![Fig 7.1 (Armitage, 2020)](F7.1.png)
![Fig 7.2 (Armitage, 2020)](F7.2.png)

## Discussion

Feldman and Lin (1973) were the first to show that an external potential excites the short trailing wave at corotation.

In stellar disk / particle disk, the short wave cannot propagate past the Lindblad resonance due to Landau damping.
