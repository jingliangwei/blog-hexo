---
title: Works on Density Wave
math: true
date: 2026-07-29 19:17:52
categories:
    - fluid
tags:
    - density wave
---

- Lin, C. C., & Shu, F. H. (1964). On the spiral structure of disk galaxies. *The Astrophysical Journal*, *140*, 646. https://doi.org/10.1086/147955
- Goldreich, P., & Tremaine, S. (1979). The excitation of density waves at the Lindblad and corotation resonances by an external potential. *The Astrophysical Journal*, *233*, 857–871. https://doi.org/10.1086/157448
- Tsang, D., & Lai, D. (2008). Super-reflection in fluid discs: Corotation amplifier, corotation resonance, Rossby waves and overstable modes. *Monthly Notices of the Royal Astronomical Society*, *387*(1), 446–462. https://doi.org/10.1111/j.1365-2966.2008.13252.x
- Baruteau, C., & Masset, F. (2008). On the corotation torque in a radiatively inefficient disk. *The Astrophysical Journal*, *672*(2), 1054–1067. https://doi.org/10.1086/523667
- Tsang, D. (2014). Linear corotation torques in non-barotropic disks. *The Astrophysical Journal*, *782*(2), 112. https://doi.org/10.1088/0004-637X/782/2/112

- Miranda, R., & Rafikov, R. R. (2019). Multiple spiral arms in protoplanetary disks: Linear theory. *The Astrophysical Journal*, *875*(1), 37. https://doi.org/10.3847/1538-4357/ab0f9e
- Miranda, R., & Rafikov, R. R. (2020). Planet–disk interaction in disks with cooling: Basic theory. *The Astrophysical Journal*, *892*(1), 65. https://doi.org/10.3847/1538-4357/ab791a

- Su, Z., & Wei, X. (2025). Gravitational instability in protoplanetary disk with cooling: 2D global analysis. *The Astrophysical Journal*, *983*(2), 89. https://doi.org/10.3847/1538-4357/adc0ff

<!-- more -->

## Main Wave Equations

1. Lin and Shu (1964) were the first to name 'density wave'

2. Goldreich and Tremaine (1979) worked out the equation of density wave in a barotropic disk (uniform entropy, $p=p(\sigma)$)

    ![GT79](GT79.png)

    $\varphi_1$ is the potential of perturber; $\varphi_1^D$ is the perturbed potential; $\eta_1=c_s^2(\sigma_1/\sigma)$ is the enthalpy (represent pressure $p_1$).

    also see Tsang and Lai (2008) for the version without self-gravity

    ![TL08](TL08.png)

    $\delta h$ is the enthalpy.

3. Baruteau and Masset (2008) worked out the equation of density wave in a non-barotropic disk (entropy $S=p\Sigma^{-\gamma}$) with the ideal equation of state ($p_0=\Sigma_0c_s^2/\gamma$)

    ![BM08](BM08.png)

    $\Phi$ is the potential of perturber; $\Psi=p_1/\Sigma_0$; $\mathcal{S}=\dfrac{1}{\gamma}\dfrac{\mathrm{d}\ln S_0}{\mathrm{d}\ln r}$

4. Tsang (2014) worked out the equation of density wave in a non-barotropic disk without the ideal EoS

    ![T14](T14.png)
    with the radial Brunt-Väisälä frequency
    $$
    N_r^2\equiv-\frac{1}{\Sigma^2}\left(\frac{\mathrm{d}P}{\mathrm{d}r}\right)\left(\frac{1}{c_s^2}\frac{\mathrm{d}P}{\mathrm{d}r}-\frac{\mathrm{d}\Sigma}{\mathrm{d}r}\right)
    $$
    $$
    \frac{1}{L_S}\equiv-\frac{\Sigma N_r^2}{\mathrm{d}P/\mathrm{d}r}
    $$

    {% note info %}
    - Equation (15) of Tsang (2014) turns to Equation (16) of Baruteau and Masset (2008) if the adiabatic index $\gamma=c_s^2\Sigma/P$ is constant, then define two-dimensional entropy $S\equiv P/\Sigma^\gamma$, such that
    $$
    N_r^2=-\frac{1}{\gamma\Sigma}\frac{\mathrm{d}P}{\mathrm{d}r}\frac{\mathrm{d}\ln S}{\mathrm{d}r},\quad \frac{1}{L_S}=\frac{1}{\gamma}\frac{\mathrm{d}\ln S}{\mathrm{d}r}
    $$
    - In the barotropic limit ($N_r^2\rightarrow 0,L_s\rightarrow\infty$) Equation (13) from Goldreich and Tremaine (1979) is recovered.
    {% endnote %}

    also see Miranda and Rafikov (2019)
    ![MR19](MR19.png)


5. Miranda and Rafikov (2020) worked out the density wave equation with $\beta$ cooling
    
    ![MR20a](MR20a.png)
    ![MR20b](MR20b.png)
    ![MR20c](MR20c.png)

    {% note info %}
    - $t_c\rightarrow\infty$: adiabatic disk as 4. Equation (15) of Tsang (2014) or Equation (6) of Miranda and Rafikov (2019);
    - $t_c\rightarrow 0$: locally isothermal disk.
    {% endnote %}

## Boundary Conditions

- Outgoing wave boundary condition (Tsang & Lai, 2008): outgoing wave in the WKB limit
    $$
    \delta h=\sqrt{S/k}\exp\left(i\int_{r_\text{OL}}^r k\,\mathrm{d}r+\frac{\pi}{4}\right)
    $$
    $$
    \delta h'=\left(ik+\frac{S'}{2S}-\frac{k'}{2k}\right)\delta h.
    $$
    also see Miranda and Rafikov (2019)
    $$
    \delta h'_m=\left[ik+\frac{1}{2}\frac{\mathrm{d}}{\mathrm{d}r}\ln\left(\frac{D_S}{r\Sigma k}\right)\right]\delta h_m
    $$

- Reflecting boundary condition (Su & Wei, 2025): Eulerian perturbation $\delta u_r=0$
  
  Confining boundary condition (Su & Wei, 2025): Lagrangian perturbation $\mathrm{D}P=\delta P+\xi_r\dfrac{\mathrm{d}P}{\mathrm{d}r}=0$
