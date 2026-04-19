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

## The epicycle approximation

- the perturbation frequency in two directions $\kappa_R,\kappa_z$
    $$
    \ddot{x}+\kappa_R^2 x=0,\quad\ddot{z}+\kappa_z^2 z=0
    $$
    with the average frequency in azimuthal direction $\kappa_\phi$

- the epicyclic orbit:
    $$
    \begin{align}
    R(t)&=a(1+e\cos(\kappa_R t+\eta)) \notag \\
    \phi(t)&=\kappa_\phi t-\frac{2\kappa_\phi e}{\kappa_R}\sin(\kappa_R t+\eta)+\phi_0 \notag
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
kappa_phi = 1.0
eta = 0.0
phi0 = 0.0

T_max = 2 * np.pi / kappa_phi
n_frames = 200
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

# Static plots (higher linewidth for clarity)
ax.plot(x_star, y_star, color='lightgray', linewidth=1.5, label='star orbit path')
ax.plot(x_guide_circle, y_guide_circle, '--', color='gray', linewidth=1.5, label='guiding centre orbit')

# Moving artists (slightly larger markers)
star_point, = ax.plot([], [], 'ro', markersize=4, label='star')
star_trail, = ax.plot([], [], 'r-', linewidth=1.5, alpha=0.7)
guide_point, = ax.plot([], [], 'bo', markersize=3, label='guiding centre')

# Epicycle ellipse
epicycle_ellipse = Ellipse((0, 0), width=2*radial_semiaxis, height=2*tangential_semiaxis,
                           angle=0, facecolor='cyan', edgecolor='blue',
                           alpha=0.3, linewidth=1.5)
ax.add_patch(epicycle_ellipse)

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
    time_text.set_text('')
    return star_point, star_trail, guide_point, epicycle_ellipse, time_text

def update(frame):
    star_point.set_data([x_star[frame]], [y_star[frame]])
    star_trail.set_data(x_star[:frame+1], y_star[:frame+1])
    gx, gy = x_guide[frame], y_guide[frame]
    guide_point.set_data([gx], [gy])
    epicycle_ellipse.center = (gx, gy)
    angle_deg = np.degrees(np.arctan2(gy, gx))
    epicycle_ellipse.angle = angle_deg
    time_text.set_text(f't = {t[frame]:.2f}')
    return star_point, star_trail, guide_point, epicycle_ellipse, time_text

ani = FuncAnimation(fig, update, frames=n_frames, init_func=init,
                    blit=True, interval=50)

# Save with the same DPI as the figure
ani.save('epicyclic_orbit_with_ellipse.gif',
         writer=PillowWriter(fps=20), dpi=dpi)
plt.close(fig)
print("GIF saved as 'epicyclic_orbit_with_ellipse.gif'")
```
{% endfold %}
