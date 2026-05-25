---
title: Quintic Formula
math: true
date: 2026-05-17 13:18:49
categories:
    - mathematics
tags:
    - quintic formula
    - algebra
---

Ideas from Youtube vedio: https://youtu.be/BSHv9Elk1MU?si=jpgd7e8tOTUTmqLX

<!-- more -->

Also see the visual Youtube vedio: https://youtu.be/9HIy5dJE-zQ?si=Wu3Qy9d0OF5dXm2j

Why there is 'no' quintic formula? (A proof without Galois theory)

## Fundamental theorem of algebra

Fundamental theorem of algebra:
A degree $n$ polynomial equation has $n$ solutions in the complex plane. (counting repeated roots)

A visual proof:
Considering a degree $n$ polynomial $p(z)=az^n+bz^{n-1}+\cdots+c$. While $z$ is large enough, the polynomial is mainly depend on the largest term $p(z)\sim az^n$. Then when $\arg(z)$ varies from $0$ to $2\pi$, the polynomial will rotate the origin $n$ times in a orbit near circle. See the figure using $f(z)=z^2-z-2$ as an example below.

![z=10](z=10.gif)

Then we decrease the amplitude of $z$, and the trajectory of the $f(z)$ will finally approach the constant term in the polynomial $c$.

![z=3](z=3.gif)
![z=2](z=2.gif)
![z=1](z=1.gif)
![z=0.5](z=0.5.gif)
![z=0.1](z=0.1.gif)

And through the whole process, the trajectory will cross the origin at $n$ times (here $n=2$), which mean there are $n$ solutions in the complex plane for a degree $n$ polynomial equation.


{% fold info @python script %}
```py
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation

# ================== parameters ==================
theta_vals = np.linspace(0, 2 * np.pi, 200)
z_size = 0.1
z_vals = z_size * np.exp(1j * theta_vals)
f_vals = z_vals**2 - z_vals - 2

z_x = z_vals.real
z_y = z_vals.imag
f_x = f_vals.real
f_y = f_vals.imag

# set the limits for the plot
lim = 12
# all_x = np.concatenate([z_x, f_x])
# all_y = np.concatenate([z_y, f_y])
# margin = max(np.abs(all_x).max(), np.abs(all_y).max()) * 0.1
# lim = max(np.abs(all_x).max(), np.abs(all_y).max()) + margin

# ================== create figure ==================
fig, ax = plt.subplots(figsize=(8, 8))
ax.set_title(r"$z = $" + str(z_size) + r"$e^{i\theta}$ and $f(z)=z^2 - z - 2$", fontsize=12)
ax.set_xlim(-lim, lim)
ax.set_ylim(-lim, lim)
ax.set_aspect('equal')
ax.grid(alpha=0.3)
ax.axhline(0, color='k', lw=0.5)
ax.axvline(0, color='k', lw=0.5)

circle_line, = ax.plot(z_x, z_y, 'b-', lw=1, alpha=0.7, label=r"$|z|=$" + str(z_size))

point_z, = ax.plot([], [], 'ro', markersize=6, label=r"$z(\theta)$")

traj_line, = ax.plot(f_x, f_y, 'g-', lw=1.5, alpha=0.8, label=r"$f(z)$")

point_f, = ax.plot([], [], 'mD', markersize=5, label=r"$f(z(\theta))$")

ax.legend()

# ================== init function ==================
def init():
    point_z.set_data([], [])
    point_f.set_data([], [])
    return point_z, point_f

# ================== update function ==================
def update(frame):
    point_z.set_data([z_x[frame]], [z_y[frame]])
    
    point_f.set_data([f_x[frame]], [f_y[frame]])
    
    return point_z, point_f, traj_line

# ================== generate animation ==================
ani = FuncAnimation(fig, update, frames=len(theta_vals),
                    init_func=init, blit=True, interval=20, repeat=True)

ani.save("z=" + str(z_size) + ".gif", writer="pillow", fps=30)

plt.show()
```
{% endfold %}

## The symmetry of roots

- Quintic formula:
    $$
    z^5+bz^4+cz^3+dz^2+ez+f=(z-z_1)(z-z_2)(z-z_3)(z-z_4)(z-z_5)
    $$
    $$
    (b,c,d,e,f)\rightarrow(z_1,z_2,z_3,z_4,z_5)
    $$

- For $z^2=w$:
    If we change the $w$ continuously, for example $w=4e^{i\theta}$, and you will find that the solution $(z_1,z_2)$ can be both $(2,-2)$ and $(-2,2)$, when $w=4$.
    ![z1_z2_w](z1_z2_w.gif)
    In other word, the solution $z=z(w)$ is multivalued function, which mean there is no quadratic solution without square root ($\pm\sqrt{w}$ is multivalued).

    The visual symmetry of square root help us to prove the theorem
    {% note info %}
    *Theorem*: The quadratic equation cannot be solved with a rational function of $a,b,c$.

    *Proof*: Imagine $z_1=\dfrac{-b+\cdots}{2a}+\cdots$ could be written without roots.
    Then it is a continuous single-valued function.
    Now consider $(z-2e^{i\theta})(z+2e^{i\theta})=0$. Smoothly changing $\theta=0$ to $\theta=\pi$, we guarantee $z_1$ must change (by continuity). (See the figure before)
    But the equation and hence $a,b,c$ are unaltered, so $z_1$ has not changed (by single-valuedness).
    {% endnote %}

So our idea to prove there is 'no' quintic formula can be:
{% note info %}
*Theorem*: The quintic equation cannot be solved using a single root of $b,c,d,e,f$.

*Proof*: Imagine $z_1=\dfrac{\cdots+\sqrt[n]{\cdots}}{\cdots}+\cdots$ could be written with just one roots.
Then it is a continuous tamely multi-valued function.
Now consider $(z-z_1)(z-z_2)(z-z_3)(z-z_4)(z-z_5)=0$. Smoothly and cleverly swapping these, we guarantee $z_1$ must change (by continuity).
But hopefully $b,c,d,e,f,\sqrt[n]{\cdots}$ are unaltered, so $z_1$ has not changed (by tameness?).
{% endnote %}

So our goal turn to: Can we swap the solutions $z_i$ without changing $n$th roots of coefficients $b,c,d,e,f$?

## Roots aren't enough for cubic/quartic/...

Consider a $n$th root $\sqrt[n]{r(b,c,d,e,f)}$, and the five solutions set

| values | $\alpha$ | $\beta$ | $\chi$ | $\delta$ | $\epsilon$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| solutions | $z_1$ | $z_2$ | $z_3$ | $z_4$ | $z_5$ |

If we take a continuously change of $r$, which add $+2\pi m$ onto the phase of $r$ and swap $\alpha$ and $\beta$, i.e.,

| values | $\alpha$ | $\beta$ | $\chi$ | $\delta$ | $\epsilon$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| solutions | $z_2$ | $z_1$ | $z_3$ | $z_4$ | $z_5$ |

and then add $+2\pi n$ onto the phase of $r$ which swap $\beta$ and $\chi$, we have

| values | $\alpha$ | $\beta$ | $\chi$ | $\delta$ | $\epsilon$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| solutions | $z_2$ | $z_3$ | $z_1$ | $z_4$ | $z_5$ |

and then undo the first step, i.e., $-2\pi m$ onto the phase of $r$ and swap $\alpha$ and $\beta$ back,

| values | $\alpha$ | $\beta$ | $\chi$ | $\delta$ | $\epsilon$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| solutions | $z_3$ | $z_2$ | $z_1$ | $z_4$ | $z_5$ |

and finally undo the second step, i.e., $-2\pi n$ onto the phase of $r$ and swap $\bata$ and $\chi$ back,

| values | $\alpha$ | $\beta$ | $\chi$ | $\delta$ | $\epsilon$ |
|:---:|:---:|:---:|:---:|:---:|:---:|
| solutions | $z_3$ | $z_1$ | $z_2$ | $z_4$ | $z_5$ |

So the $r$ keep unchanged while the five solutions set rearranged.
This process is a commutator $\sigma\tau\sigma^{-1}\tau^{-1}$.

{% note info %}
Therefore we have prove that: There is no cubic/quartic/... formula with only one $n$th root.
{% endnote %}

## Nested roots for cubic and quartic

Nested roots, e.g., $\sqrt[3]{\dfrac{2b^3-9abc+27a^2d+\sqrt{(2b^3-9abc+27a^2d)^2-4(b^2-3ac)^3}}{2}}$

One comutator keep the inner root unchanged, but the outer root is not guaranteed unchanged.

We can take commutator of commutators, i.e., (comm.1)(comm.2)(comm.1)$^{-1}$(comm.2)$^{-1}$, and this one will guarantee the outer root unchanged.

- Prove all commutators of commutators permuting three points are trivial.

    $$
    (\sigma\tau\sigma^{-1}\tau^{-1})(\pi\rho\pi^{-1}\rho^{-1})(\tau\sigma\tau^{-1}\sigma^{-1})(\rho\pi\rho^{-1}\pi^{-1})
    $$
    | single operator $\sigma,\tau,\pi,\rho$ | commutator $(\sigma\tau\sigma^{-1}\tau^{-1})$ | commutator of commutators |
    |:---:|:---:|:---:|
    | 1 2 3 <br> 1 3 2 <br> 2 1 3 <br> 2 3 1 <br> 3 1 2 <br> 3 2 1 | 1 2 3 <br> 2 3 1 <br> 3 1 2 | 1 2 3 |
    | all 3 point permutations | cyclic permutations | nothing |

    {% note info %}
    (all 3 point permutations -> cyclic permutations -> nothing) is called derived series in Galois theory.
    {% endnote %}

- The quartic formula has roots of roots of roots:

    It can be proved that the commutators-of-commutators-of-commutators are trivial.

## Onto the quintic

We want to prove that: The solutions to the quintic cannot be expressed using any finite number of nested roots, i.e., there are commutators of commutators of commutators of commutators of commutators ... which mix up five points!

Proof:
consider the operation below
![rho123](rho123.jpg)
The cyclic permutation of 3 points can be the commutator of two other such permutations of 3 points
$$
\rho_{123}=\sigma\tau\sigma^{-1}\tau^{-1}
$$
$$
\sigma=\alpha\beta\alpha^{-1}\beta^{-1},\tau=\gamma\delta\gamma^{-1}\delta^{-1},\cdots
$$
and this can generate a infinite series commutator of commutators that mix up the five points.
QED.
