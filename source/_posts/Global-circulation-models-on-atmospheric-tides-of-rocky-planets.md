---
title: Global circulation models on atmospheric tides of rocky planets
math: true
date: 2026-11-12 15:37:27
updated: 2026-11-12 15:37:27
categories:
    - planetary science
tags:
    - global circulation models
    - thermal tide
---

- Leconte, J., Wu, H., Menou, K., & Murray, N. (2015). Asynchronous rotation of Earth-mass planets in the habitable zone of lower-mass stars. *Science*, *347*(6222), 632–635. https://doi.org/10.1126/science.1258686
- Salazar, A. M., & Wordsworth, R. (2024). The feasibility of asynchronous rotation via thermal tides for diverse atmospheric compositions. *The Planetary Science Journal*, *5*, Article 218. https://doi.org/10.3847/PSJ/ad74ef
- Navon, R., Galanti, E., Lebonnois, S., Millour, E., & Kaspi, Y. (2026). Surface thermal tides and radiative adjustment in Venus's deep atmosphere. *Journal of Geophysical Research: Planets*, *131*, Article e2026JE009679. https://doi.org/10.1029/2026JE009679

<!-- more -->

The papers applying **global circulation models** (GCM) on atmospheric tides of rocky planets.

## Leconte 2015

Using the Laboratoie de Météorologie Dynamique (LMD) Generic Model to study the frequency dependence of the atmospheric thermal torque.

![](Leconte_15_fig1.png)

And develop a periodically heated thermal slab model,
$$
\tilde{p}_2=-q_o\frac{1}{1+i\sigma/\omega_o}
$$
$$
{\rm Im}(\tilde{p}_2)=q_o\frac{\sigma/\omega_o}{1+(\sigma/\omega_o)^2}
$$

## Salazar 2024

The further research of Leconte 2015.

> The atmospheric thermal tide is caused by large-scale mass redistribution of a planet's atmosphere due to differential stellar heating over the diurnal cycle.

$\nabla T$ $\rightarrow \delta m$ or $\delta p$ $\rightarrow \mathcal{T}_{\rm a}$

### GCM Results

Gain intuition on the effect of atmospheric properties on the strength of the thermal tide.

Four parameters of the atmosphere:
(1) longwave optical depth $\tau_{\rm LW}$
(2) shortwave optical depth $\tau_{\rm SW}$
(3) absorbed shortwave/stellar radiation (ASR)
(4) atmospheric surface pressure $p_s$

![](Salazar_24_fig2.png)

- $\tau_{\rm LW}$:
    $\tau_{\rm LW}$ increases, the torque increases till $\tau_{\rm LW}\sim 1$ and then decreases.
    (1) the strengthening of large-scale atmospheric circulation (strengthen the process of $\nabla T\rightarrow\delta p_s$)
    (2) the weakening of zonal temperature gradients (weaken the torque)
- $\tau_{\rm SW}$:
    $\tau_{\rm SW}$ increases, the torque decreases.
    (1) the heating move from surface to high-atmosphere
    (2) stabilizing the atmosphere against large-scale circulation
- ASR:
    ASR decreases, the torque stays roughly constant.
    (1) decreasing ASR decreases the heating and the amplitude
    (2) a cooler planet with a longer thermal equilibrium timescale which increases the lag angle
- $p_s$:
    $p_s$ increases, the torque increases.

### Simple Model

Give a analytical expression to explain the results from GCM.

- Linearize energy equation Eq. (7),
    define the mean temperature $\sigma_{\rm SB}\bar{T}^4=\bar{F}+F_{\rm LW}^-(\tau_{\rm LW})$,
    using the relation of temperature and pressure anomaly Eq. (19,20,25),
    we have
    $$
    \tilde{p}_2=-q_o\frac{1}{1+i\sigma/\omega_o}\tag{31}
    $$
    $$
    q_o=\frac{1}{24}\sqrt{\frac{15}{2\pi}}\frac{S_o(1-\alpha){\rm e}^{-\tau_{\rm SW}}}{\bar{F}+F_{\rm LW}^-(\tau_{\rm LW})}\chi p_s\frac{U_s}{U_{so}}\tag{32}
    $$
    with $S_o$ is the stellar constant,
    $\alpha$ is the albedo of the planet,
    $\bar{F}$ is the average equatorial surface instellation,
    $F_{\rm LW}^-$ is the downwelling of longwave flux,
    $\chi=0.17$ is the fraction of the atmosphere thermally coupled to the surface in the base state,
    $U_s$ is the average wind speed on the dayside,
    and $U_{so}$ is the surface wind speed in the base state.

- The thermal torque
    $$
    T_a=\frac{3}{2}K_aq_o\frac{\sigma/\omega_o}{1+(\sigma/\omega_o)^2}\tag{36}
    $$
    with the thermal equilibrium frequency
    $$
    \omega_o=\frac{4\sigma_{\rm SB}\bar{T}^3}{C}\tag{30}
    $$

The comparison of the analytic model with the GCM results:

![](Salazar_24_fig3.png)

## Navon 2026

Using the Laboratoie de Météorologie Dynamique (LMD) [Venus Planetary Climate Model (VPCM)](http://www-venus.lmd.jussieu.fr/)

### VPCM Simulations

Including
(1) solar and infrared heating;
(2) cloud structure;
(3) atmospheric composition;
(4) planetary boundary layer processes.

### Atmospheric Response Timescale and Phase Offset

- The longitude of the surface diurnal tide
    $$
    \Phi_{\rm model}=\frac{\int_{\varphi_1}^{\varphi_2}|p´(\varphi)|\varphi\,{\rm d}\varphi}
    {\int_{\varphi_1}^{\varphi_2}|p´(\varphi)|\,{\rm d}\varphi}\tag{2}
    $$

- The radiative adjustment timescale $\tau_{\rm R}$, characterizes the time required for an atmospheric layer to relax toward radiative equilibrium following a perturbation
    $$
    \tau_{\rm R}=\frac{\tau_{\rm IR}mC_p}{4\sigma T_e^3}\tag{3}
    $$
    where $m=\int_0^h\rho\,{\rm d}z$ is the column mass of a layer of depth $h$,
    $C_p$ is the specific heat at constant pressure,
    $T_e$ is the mean temperature,
    and $\tau_{\rm IR}=1$ is the effective infrared optical depth across the layer.

    These can be derived from the linear perturbation of the energy equation, similar to the Eq. (30) $\omega_o$ in Salazar & Wordsworth (2024).

- The relation of adjustment timescale and phase lag
    $$
    \Phi_{\rm model}=\tau_{\rm R}\frac{2\pi}{\rm LOD}\tag{4}
    $$
    where ${\rm LOD}$ is the length of day.

### Results

- VD $=116.75$ days $\Rightarrow$ $\tau_{\rm R}\sim9.4$ days $\Rightarrow$ $z\sim1100$ m

    ![](Navon_26_fig1.png)

- The $\Phi_{\rm model}$ dependence of LOD

    ![](Navon_26_fig2.png)

    $$
    \frac{1}{\rm LOD}=\frac{1}{P_{\rm orbit}}+\frac{1}{P_{\rm rotation}}
    $$

    ![](Navon_26_fig3.png)

- Three main modes:
    (1) diurnal
    (2) semi-diurnal
    (3) $35$-day

    ![](Navon_26_fig6.png)

- The structure of $35$-day mode:
    satisfies the dispersion relation of internal gravity waves (IGW)

    ![](Navon_26_fig7.png)

![](Navon_26_fig8.png)

- The main characteristics above are similar in the simulations with realistic topography.

    ![](Navon_26_fig9.png)

