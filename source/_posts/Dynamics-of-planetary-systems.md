---
title: Dynamics of planetary systems
math: true
date: 2026-04-19 13:43:25
categories:
    - planetary science
tags:
    - epicycle
excerpt:
    The epicycle approximation of nearly circular orbits.
---

Tremaine, S. (2023). *Dynamics of planetary systems*. Princeton University Press.

Ogilvie, G. I. (2020, May). *Dynamics of Astrophysical Discs*. Department of Applied Mathematics and Theoretical Physics, University of Cambridge. https://www.damtp.cam.ac.uk/user/gio10/dad.html

## Orbital elements

- The six orbital elements:
    semimajor axis $a$,
    eccentricity $e$,
    inclination $I$,
    longtitude of the ascending node $\Omega$,
    argument of periapsis $\omega$ ( or longtitude of periapsis $\varpi\equiv\Omega+\omega$ ),
    and mean anomaly $\ell$ ( or mean longtitude $\lambda\equiv\varpi+\ell$ ).

- Delaunay variables:
    $$
    \begin{array}{ll}
    \ell,&\Lambda\equiv(GMa)^{1/2}, \\
    \omega,&L=[GMa(1-e^2)]^{1/2}, \\
    \Omega,&L_z=L\cos I.
    \end{array}
    $$

## The epicycle approximation

- The perturbation frequency in two directions $\kappa_R,\kappa_z$
    $$
    \ddot{x}+\kappa_R^2 x=0,\quad\ddot{z}+\kappa_z^2 z=0,
    $$
    with the average frequency in azimuthal direction $\kappa_\phi$.

- The epicyclic orbit:
    $$
    \begin{align}
    R(t)&=a(1+e\cos(\kappa_R t+\eta)), \notag \\
    \phi(t)&=\kappa_\phi t-\frac{2\kappa_\phi e}{\kappa_R}\sin(\kappa_R t+\eta)+\phi_0. \notag
    \end{align}
    $$

![epicycle](epicyclic_orbit_with_ellipse.gif)

{% fold info @python script %}
The `python` script to generate this .gif
``` py
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation, PillowWriter
from matplotlib.patches import Ellipse

# ==================== Parameters ====================
a = 1.0
e = 0.05
kappa_R = 1
kappa_phi = 1.1
eta = 0.0
phi0 = 0.0

T_max = 7 * np.pi / kappa_phi
n_frames = 700
t = np.linspace(0, T_max, n_frames)

# Star positions
def star_positions(t):
    R = a + a * e * np.cos(kappa_R * t + eta)
    phi = kappa_phi * t - (2 * kappa_phi * e / kappa_R) * np.sin(kappa_R * t + eta) + phi0
    x = R * np.cos(phi)
    y = R * np.sin(phi)
    return x, y

x_star, y_star = star_positions(t)

# Guiding centre
x_guide = a * np.cos(kappa_phi * t)
y_guide = a * np.sin(kappa_phi * t)

# Reference circles
theta_circle = np.linspace(0, 2*np.pi, 200)
x_guide_circle = a * np.cos(theta_circle)
y_guide_circle = a * np.sin(theta_circle)

# Epicycle ellipse axes
radial_semiaxis = a * e
tangential_semiaxis = a * (2 * kappa_phi * e / kappa_R)

# ==================== Find periapsis points ====================
r_star = np.sqrt(x_star**2 + y_star**2)
periapsis_indices = []
for i in range(1, len(r_star)-1):
    if r_star[i] < r_star[i-1] and r_star[i] < r_star[i+1]:
        periapsis_indices.append(i)
if len(periapsis_indices) == 0:
    min_idx = np.argmin(r_star)
    periapsis_indices = [min_idx]

# ==================== Setup figure ====================
dpi = 200
fig, ax = plt.subplots(figsize=(8, 8), dpi=dpi)
ax.set_aspect('equal')
margin = 1.5 * a * (1 + e)
ax.set_xlim(-margin, margin)
ax.set_ylim(-margin, margin)
ax.set_xlabel('x', fontsize=12)
ax.set_ylabel('y', fontsize=12)
ax.set_title('Epicyclic Motion: Star, Guiding Centre, and Epicycle Ellipse', fontsize=14)
ax.grid(alpha=0.3)

# Static plots
ax.plot(x_star, y_star, color='lightgray', linewidth=1.5, label='star orbit path')
ax.plot(x_guide_circle, y_guide_circle, '--', color='gray', linewidth=1.5, label='guiding centre orbit')

# Moving artists
star_point, = ax.plot([], [], 'ro', markersize=4, label='star')
star_trail, = ax.plot([], [], 'r-', linewidth=1.5, alpha=0.7)
guide_point, = ax.plot([], [], 'bo', markersize=3, label='guiding centre')

# Epicycle ellipse
epicycle_ellipse = Ellipse((0, 0), width=2*radial_semiaxis, height=2*tangential_semiaxis,
                           angle=0, facecolor='cyan', edgecolor='blue',
                           alpha=0.3, linewidth=1.5)
ax.add_patch(epicycle_ellipse)

# Periapsis markers (scatter, same visual size as star)
periapsis_markers = ax.scatter([], [], s=25, c='green', marker='o', zorder=5, label='periapsis')

time_text = ax.text(0.02, 0.95, '', transform=ax.transAxes, fontsize=12,
                    bbox=dict(facecolor='white', alpha=0.7, edgecolor='none'))

ax.legend(loc='upper right', fontsize=10)

# ==================== Animation ====================
def init():
    star_point.set_data([], [])
    star_trail.set_data([], [])
    guide_point.set_data([], [])
    epicycle_ellipse.center = (0, 0)
    epicycle_ellipse.angle = 0
    periapsis_markers.set_offsets(np.empty((0, 2)))
    time_text.set_text('')
    return star_point, star_trail, guide_point, epicycle_ellipse, periapsis_markers, time_text

def update(frame):
    # Star and its trail (last 50 points)
    star_point.set_data([x_star[frame]], [y_star[frame]])
    start_idx = max(0, frame - 49)
    star_trail.set_data(x_star[start_idx:frame+1], y_star[start_idx:frame+1])
    
    # Guiding centre
    gx, gy = x_guide[frame], y_guide[frame]
    guide_point.set_data([gx], [gy])
    
    # Epicycle ellipse oriented along radial direction
    epicycle_ellipse.center = (gx, gy)
    angle_deg = np.degrees(np.arctan2(gy, gx))
    epicycle_ellipse.angle = angle_deg
    
    # Periapsis markers: show all points that have been reached up to current frame
    coords = [(x_star[i], y_star[i]) for i in periapsis_indices if i <= frame]
    if coords:
        periapsis_markers.set_offsets(np.array(coords))
    else:
        periapsis_markers.set_offsets(np.empty((0, 2)))
    
    time_text.set_text(f't = {t[frame]:.2f}')
    return star_point, star_trail, guide_point, epicycle_ellipse, periapsis_markers, time_text

ani = FuncAnimation(fig, update, frames=n_frames, init_func=init,
                    blit=True, interval=50)

# Save with the same DPI as the figure
ani.save('epicyclic_orbit_with_ellipse.gif',
         writer=PillowWriter(fps=20), dpi=dpi)
plt.close(fig)
print("GIF saved as 'epicyclic_orbit_with_ellipse.gif'")
```
{% endfold %}

- The apsidal precession rate is
    $$
    \frac{\Delta\phi}{\Delta t}=\kappa_\phi-\kappa_R.
    $$

    {% fold info @derivation %}
    The minimum radius (periapsis) occurs at time intervals $\Delta t=2\pi/\kappa_R$, corresponding to
    $$
    \begin{aligned}
    \Delta\phi&=\frac{2\pi}{\kappa_R}\kappa_\phi \\
    &=2\pi\left(\frac{\kappa_\phi}{\kappa_R}-1\right)+2\pi \\
    &=2\pi\left(\frac{\kappa_\phi}{\kappa_R}-1\right) \text{ mod } 2\pi.
    \end{aligned}
    $$
    The apsidal precession rate is therefore
    $$
    \frac{\Delta \phi}{\Delta t}=\kappa_\phi-\kappa_R.
    $$
    {% endfold %}

## The three-body problem

### The circular restricted three-body problem

- Effective potential
    $$
    \Phi_{\text{eff}}(\boldsymbol{x})=-\frac{Gm_0}{|\boldsymbol{x}-\boldsymbol{x}_0|}-\frac{Gm_1}{|\boldsymbol{x}-\boldsymbol{x}_1|}-\frac{1}{2}|\boldsymbol{\Omega}\times\boldsymbol{x}|^2.
    $$
![Roche Potential](Roche_potential.png)

- Hill radius:

    when $m_1\ll m_0$, the collinear Lagrange points L1 and L2 are separated from the mass $m_1$ by the Hill radius,
    $$
    r_\text{H}\equiv a\left(\frac{m_1}{3m_0}\right)^{1/3}.
    $$

- Jacobi constant (total energy)
    $$
    E_\text{J}\equiv\frac{1}{2}|\dot{\boldsymbol{x}}|^2+\Phi_{\text{eff}}(\boldsymbol{x}).
    $$

- Poincaré map / surface of section:

    considering the orbits crossing the locus $x_b=0$ and $\dot{x}_b>0$, so a point in the $(x_a,\dot{x}_a)$ plane can represent a crossing. The point $(x_a,\dot{x}_a)$ defines the orbit and also defines the next crossing $(x_a',\dot{x}_a')$, which we call the Poincaré map, i.e., $\mathbf{P}(x_a,\dot{x}_a)=(x_a',\dot{x}_a')$.

## The disturbing function

- The interaction potential
    $$
    \Phi_{ij}(\boldsymbol{r}_i,\boldsymbol{r}_j)=-\frac{Gm_im_j}{\Delta_{ij}},
    $$

    $$
    \begin{aligned}
        \begin{aligned}
        \frac{1}{\Delta_{12}}=
        \end{aligned} & 
        \begin{aligned}
        \ \frac{1}{2a_2}\sum_{m=-\infty}^{\infty}b_{1/2}^m\cos(m\lambda_1-m\lambda_2)+\frac{\epsilon}{a_2}\sum_{m=-\infty}^{\infty}
        \end{aligned} \\
        & 
        \biggl\{\left[\frac{1}{4}\alpha b_{3/2}^{m+2}+\frac{1}{2}\alpha^2b_{3/2}^{m+1}-\frac{3}{4}\alpha b_{3/2}^m\right]e_1\cos[m\lambda_1-(m+1)\lambda_2+\varpi_1] \\
     & +\left[\frac{1}{4}\alpha b_{3/2}^{m-1}+\frac{1}{2}b_{3/2}^{m}-\frac{3}{4}\alpha b_{3/2}^{m+1}\right]e_{2}\cos[m\lambda_{1}-(m+1)\lambda_{2}+\varpi_{2}]\biggr\} \\
     & +\epsilon^2\sum_{m=-\infty}^\infty X_m+\mathrm{O}(\epsilon^3),
    \end{aligned}
    $$
    where $\alpha=a_1/a_2<1$, and $b_s^m(\alpha)$ is a Laplace coefficient.

