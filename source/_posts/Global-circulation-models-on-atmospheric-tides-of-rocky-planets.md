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
