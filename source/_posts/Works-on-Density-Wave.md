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

<!-- more -->

## Main Analytical Works

1. Lin and Shu (1964) were the first to name 'density wave'

2. Goldreich and Tremaine (1979) worked out the equation of density wave in a barotropic disk (uniform entropy)

    ![GT79](GT79.png)

    $\varphi_1$ is the potential of perturber; $\varphi_1^D$ is the perturbed potential; $\eta_1=c_s^2(\sigma_1/\sigma)$ is the enthalpy (represent pressure $p_1$).

    also see Tsang and Lai (2008) for the version without self-gravity

    ![TL08](TL08.png)

    $\delta h$ is the enthalpy.

3. Baruteau and Masset (2008) worked out the equation of density wave in a non-barotropic disk with the ideal equation of state ($p_0=\Sigma_0c_s^2/\gamma$)

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
