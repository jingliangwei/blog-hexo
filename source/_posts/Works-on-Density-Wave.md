---
title: Works on Density Wave
math: true
date: 2026-07-29 19:17:52
updated: 2026-08-22 22:13:00
categories:
    - fluid
tags:
    - density wave
---

- Lin, C. C., & Shu, F. H. (1964). On the spiral structure of disk galaxies. *The Astrophysical Journal*, *140*, 646. https://doi.org/10.1086/147955
- Goldreich, P., & Tremaine, S. (1979). The excitation of density waves at the Lindblad and corotation resonances by an external potential. *The Astrophysical Journal*, *233*, 857–871. https://doi.org/10.1086/157448
- Korycansky, D. G., & Pollack, J. B. (1993). Numerical calculations of the linear response of a gaseous disk to a protoplanet. *Icarus*, *102*(1), 150–165. https://doi.org/10.1006/icar.1993.1039
- Tanaka, H., Takeuchi, T., & Ward, W. R. (2002). Three-dimensional interaction between a planet and an isothermal gaseous disk. I. Corotation and Lindblad torques and planet migration. *The Astrophysical Journal*, *565*(2), 1257–1274. https://doi.org/10.1086/324713
- Tsang, D., & Lai, D. (2008). Super-reflection in fluid discs: Corotation amplifier, corotation resonance, Rossby waves and overstable modes. *Monthly Notices of the Royal Astronomical Society*, *387*(1), 446–462. https://doi.org/10.1111/j.1365-2966.2008.13252.x
- Baruteau, C., & Masset, F. (2008). On the corotation torque in a radiatively inefficient disk. *The Astrophysical Journal*, *672*(2), 1054–1067. https://doi.org/10.1086/523667
- Olver, F. W. J., Lozier, D. W., Boisvert, R. F., & Clark, C. W. (Eds.). (2010). *NIST handbook of mathematical functions*. Cambridge University Press. https://dlmf.nist.gov/
- Tsang, D. (2011). Protoplanetary disk resonances and type I migration. *The Astrophysical Journal*, *741*(2), 109. https://doi.org/10.1088/0004-637X/741/2/109
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

3. Baruteau and Masset (2008) worked out the equation of density wave in a non-barotropic / baroclinic disk (entropy $S=p\Sigma^{-\gamma}$) with the ideal equation of state ($p_0=\Sigma_0c_s^2/\gamma$)

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

6. Tanaka et al. (2002) worked on the 3D version of a global isothermal and barotropic disk.

    ![T02](T02.png)

    here $n$ is the vertical mode number, and $\mu\equiv\dfrac{\mathrm{d}\ln h}{\mathrm{d}\ln r}$ is the scale height radial gradient.
    When $n=\mu=0$, the Equation (13) in Goldreich and Tremaine (1979) is recovered.

## Boundary Conditions

- Outgoing wave / radiative boundary condition (Tsang & Lai, 2008): outgoing wave in the WKB limit
    $$
    \delta h=\sqrt{S/k}\exp\left(i\int_{r_\text{OL}}^r k\,\mathrm{d}r+\frac{\pi}{4}\right)\tag{TL08.48}
    $$
    $$
    \delta h'=\left(ik+\frac{S'}{2S}-\frac{k'}{2k}\right)\delta h.\tag{TL08.85}
    $$
    also see Miranda and Rafikov (2019)
    $$
    \delta h'_m=\left[ik+\frac{1}{2}\frac{\mathrm{d}}{\mathrm{d}r}\ln\left(\frac{D_S}{r\Sigma k}\right)\right]\delta h_m\tag{MR19.50,51}
    $$

- Reflecting boundary condition (Su & Wei, 2025): Eulerian perturbation $\delta u_r=0$ (SW25.19)
  
  Confining boundary condition (Su & Wei, 2025): Lagrangian perturbation $\mathrm{D}P=\delta P+\xi_r\dfrac{\mathrm{d}P}{\mathrm{d}r}=0$ (SW25.20)

## Analytical Solutions

- Tsang & Lai (2008) gave a analytical solutions at section 3.
    In short, the wave equation near Lindblad resonance can be written as
    $$
    V''+\left(1-\frac{7}{36z^2}\right)V=0.\tag{TL08.28}
    $$
    denote $V=\sqrt{z}w$ and yield Bessel's equation
    $$
    z^2 w''+zw'+(z^2-\nu^2)w=0,\quad \nu=\frac{2}{3}
    $$
    and the solutions and asymptotic expansions (Airy functions) are given in the mathematical handbook (Olver et al., 2010).
    (Equations (9.6.12),(9.7.6),(9.7.8),(9.7.10),(9.7.12) in the handbook)

    {% note info %}
    The wave equation (TL08.28) only control the wave near OLR, which gives the Airy solutions (local solutions).
    But for $r\gg r_\text{OL}$ or $r\ll r_\text{OL}$, we have $|z|\gg 1$, and wave equation becomes harmonic wave equation, so assume the local solutions propagate away.
    {% endnote %}

## Torques and AMF

the net torque on the disk: 
$$
T_\text{tot}=\int_{r_\text{in}}^{r_\text{out}}\frac{\mathrm{d}T}{\mathrm{d}r}\mathrm{d}r,\quad \frac{\mathrm{d}T}{\mathrm{d}r}=\frac{\mathrm{d}F_A}{\mathrm{d}r}
$$
contains three parts ($\mathrm{d}F_A/\mathrm{d}r=0$ in adiabatic disk):
the outer Lindblad torque: $T_\text{OLR}=F_A(x\rightarrow\infty)$
the inner Lindblad torque: $T_\text{ILR}=-F_A(x\rightarrow-\infty)$
the corotation torque: $T_\text{CR}=-[F_A(+0)-F_A(-0)]$

{% note info %}
$$
\begin{aligned}
T_\text{tot}=\int_{r_\text{in}}^{r_\text{out}}&=\int_{r_\text{in}}^{-0}+\int_{+0}^{r_\text{out}} \\
&=-F_A(r_\text{in})+F_A(-0)-F_A(+0)+F_A(r_\text{out}) \\
&=T_\text{ILR}+T_\text{CR}+T_\text{OLR}
\end{aligned}
$$
{% endnote %}

- Goldreich & Tremaine (1979) calculated the torque on the disk by determining the angular momentum flux (AMF) exerted only by the inhomogeneous wave (i.e. Equation (39) in Miranda and Rafikov (2020))

    ![GT79 Torque at Lindblad resonance](GT79_T_LR.png)
    ![GT79 Torque at corotation resonance](GT79_T_CR.png)

    here they ignore the temperature gradient, and ignore the density gradient in Lindblad torque.

- Korycansky and Pollack (1993) used numerical method to give the Lindblad torque (here $a,b$ represent $\sigma\propto r^{-a}$, $c\propto r^{-b}$, i.e., consider the density gradient and temperature gradient.)

    ![KP93 Torque at Lindblad resonance](KP93_T_L.png)

    agree with the results from Goldreich & Tremaine (1979), but there is difference in the corotation torque.

- Tanaka et al. (2002) gave the new analytical corotation torque to explain the difference from (Korycansky & Pollack ,1993) to (Goldreich & Tremaine, 1979)

    ![T02 T_CR](T02_T_C.png)

- Miranda and Rafikov (2020) gave the torque on the disk with $\beta$ cooling:

    - AMF:
        $$
        F_J(r)=r^2\Sigma(r)\oint\delta u_r(r,\phi)\delta u_\phi(r,\phi)\mathrm{d}\phi,\tag{MR20.36}
        $$
    - the torque density:
        $$
        \frac{\mathrm{d}T}{\mathrm{d}r}=-r\oint \Sigma\frac{\partial\Phi_\text{p}}{\partial \phi}\mathrm{d}\phi,\tag{MR20.39}
        $$
    now with cooling, $\mathrm{d}F_A/\mathrm{d}r\neq0$ and $\dfrac{\mathrm{d}T}{\mathrm{d}r}\neq\dfrac{\mathrm{d}F_A}{\mathrm{d}r}$

    the one-sided Lindblad torques are

    ![one-sided T_L](MR20_T_L_oneside.png)

    ![T_L,C](MR20_T_L_C.png)


## Reflection and Transmission

- Tsang & Lai (2008) worked out the reflection coefficient $\mathcal{R}$ and transmission coefficient $\mathcal{T}$ at section 4.
- Tsang (2011) found that the reflected density waves by the inner edge of PPD can stop Type I migration.
