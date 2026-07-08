---
title: Weakly Nonlinear Wave Packets and the Nonlinear Schrödinger Equation
math: true
date: 2026-07-07 21:30:03
categories:
    - fluid
tags:
    - nonlinear Schrödinger equation
    - multiple scales
---

Dias, F., & Bridges, T. (2005). Weakly nonlinear wave packets and the nonlinear Schrödinger equation. In R. Grimshaw (Ed.), *Nonlinear waves in fluids: Recent advances and modern applications* (pp. 29–67). Springer. https://doi.org/10.1007/3-211-38025-6_2

<!-- more -->

## The method of multiple scales

A derivation of the NLS (nonlinear Schrödinger) equation from the KdV (Korteweg-de Vries) equation based on the method of multiple scales.

- The KdV equation
    $$
    \mathcal{L}(u)+\mathcal{N}(u,u)=u_t+u_{xxx}+6uu_x=0,\quad(x\in\mathbb{R},t\ge0,u(x,t)\in\mathbb{R}).
    $$
    Introducting a small parameter $\epsilon$, and the slow scales $X=\epsilon x,T=\epsilon t,\tau=\epsilon^2 t$
    $$
    u=\epsilon(u_0+\epsilon u_1+\epsilon^2 u_2+\cdots)=\epsilon u_0+\epsilon^2 u_1+\epsilon^3 u_2+\cdots,
    $$
    $$
    \begin{aligned}
    \mathcal{L}&=\partial_t+\partial_{xxx} \\
    &=\left(\frac{\partial}{\partial t}+\epsilon\frac{\partial}{\partial T}+\epsilon^2\frac{\partial}{\partial \tau}\right)+\left(\frac{\partial}{\partial x}+\epsilon\frac{\partial}{\partial X}\right)^3 \\
    &=\left(\frac{\partial}{\partial t}+\frac{\partial^3}{\partial x^3}\right)+\epsilon\left(\frac{\partial}{\partial T}+3\frac{\partial^3}{\partial x^2\partial X}\right)+\epsilon^2\left(\frac{\partial}{\partial\tau}+3\frac{\partial^3}{\partial x\partial X^2}\right)+\cdots \\
    &\equiv\mathcal{L}^{(0)}+\epsilon\mathcal{L}^{(1)}+\epsilon^2\mathcal{L}^{(2)}+\cdots,
    \end{aligned}
    $$
    $$
    \begin{array}{ll}
    \mathcal{O}(\epsilon) & \mathcal{L}^{(0)}u_0=0, \\
    \mathcal{O}(\epsilon^2) & \mathcal{L}^{(0)}u_1=-\mathcal{L}^{(1)}u_0-3\partial_x(u_0^2), \\
    \mathcal{O}(\epsilon^3) & \mathcal{L}^{(0)}u_2=-\mathcal{L}^{(2)}u_0-\mathcal{L}^{(1)}u_1-6\partial_x(u_0u_1)-3\partial_X(u_0^2).
    \end{array}
    $$

- At $\mathcal{O}(\epsilon)$: $\mathcal{L}^{(0)}u_0=0$
    the eigen mode
    $$
    u_0(x,t)=\psi_0(X,T)\exp[i(kx-\omega t)]+\text{c.c.}
    $$
    with the dispersion relation (decided by the linear operator $\mathcal{L}^{(0)}$)
    $$
    \omega=-k^3.
    $$
    the phase velocity $c=\omega/k$
    the group velocity $c_g=\mathrm{d}\omega/\mathrm{d}k=-3k^2$

- At $\mathcal{O}(\epsilon^2)$: $\mathcal{L}^{(0)}u_1=-\mathcal{L}^{(1)}u_0-3\partial_x(u_0^2)$
    the solvability condition ( remove the eigen mode term in RHS of the equation )
    $$
    \mathcal{L}^{(1)}u_0=0\Rightarrow(\partial_T+c_g\partial_X)u_0=0
    $$
    on the time scale $T$, the wave packet is just transported at the group velocity and thus depends only on the variable $\xi=X-c_gT$.
    ![wave packet](wave_animation.gif)

    {% fold info @python script %}
    choose the function
    $$
    \begin{aligned}
    f(x,t)&=\psi(X,T)\cos(kx-\omega t) \\
    &=\psi(X-c_g T)\cos(kx-\omega t) \\
    &=\sin[\epsilon(x-c_g t)]\cos(kx-\omega t) \\
    &=\sin[\epsilon(x+3k^2 t)]\cos(kx+k^3 t)
    \end{aligned}
    $$
    set $\epsilon=0.1, k=1$ so we have $\omega=-k^3=-1$
    phase velocity $c=\omega/k=-1$
    group veloctiy $c_g=\mathrm{d}\omega/\mathrm{d}k=-3k^2=-3$
    ```py
    import numpy as np
    import matplotlib.pyplot as plt
    from matplotlib.animation import FuncAnimation
    
    # Parameter settings
    epsilon = 0.1
    k = 1.0
    
    x = np.linspace(-20, 100, 1000)
    t_frames = np.linspace(0, 100, 300)
    
    # Create the plot window
    fig, ax = plt.subplots(figsize=(10, 6))
    ax.set_xlim(-20, 100)
    ax.set_ylim(-1.1, 1.1)
    ax.set_xlabel('x')
    ax.set_ylabel('f(x,t)')
    ax.grid(True)
    
    # Initialize three curves: f(x,t) and the two envelope lines
    line_f, = ax.plot([], [], 'b-', lw=2, label='f(x,t)')
    line_env_pos, = ax.plot([], [], 'r--', lw=1.5, label='envelope')
    line_env_neg, = ax.plot([], [], 'r--', lw=1.5)
    
    # Create legend once and fix its position
    # bbox_to_anchor=(1, 1) places the legend at the upper-right corner of the axes,
    # with a small offset to avoid overlapping with the title.
    ax.legend(loc='upper right', bbox_to_anchor=(1.0, 1.0), frameon=True)
    
    # Initialization function (clear data)
    def init():
        line_f.set_data([], [])
        line_env_pos.set_data([], [])
        line_env_neg.set_data([], [])
        return line_f, line_env_pos, line_env_neg
    
    # Update function for each frame
    def update(frame):
        t = t_frames[frame]
        # Compute the waveform
        y_f = np.sin(epsilon * (x + 3 * k**2 * t)) * np.cos(k * x + k**3 * t)
        # Envelope (amplitude)
        env = np.sin(epsilon * (x + 3 * k**2 * t))
        y_env_pos =  env
        y_env_neg = -env
    
        line_f.set_data(x, y_f)
        line_env_pos.set_data(x, y_env_pos)
        line_env_neg.set_data(x, y_env_neg)
    
        ax.set_title(f't = {t:.2f}')
        return line_f, line_env_pos, line_env_neg
    
    # Create the animation (interval 50ms, i.e., 20 frames per second)
    # If legend still jitters, try setting blit=False (though slower)
    ani = FuncAnimation(fig, update, frames=len(t_frames), init_func=init,
                        blit=True, interval=50)
    
    # Save the animation (requires ffmpeg)
    ani.save('wave_animation.gif', writer='ffmpeg', fps=20)
    
    # plt.show()
    ```
    {% endfold %}

    Then solve for $u_1$:
    $$
    \mathcal{L}^{(0)}u_1=-3\partial_x(\phi_0^2e^{2i(kx-\omega t)}+\text{c.c.})\tag{2.10}
    $$
    the general solution is
    $$
    u_1=A_2(X,T)e^{2i(kx-\omega t)}+\text{c.c.}+\psi_1 e^{i(kx-\omega t)}+\text{c.c.}+A_0(X,T)
    $$
    the term $\psi_1 e^{i(kx-\omega t)}$ can be incorporated into the term $\psi_0 e^{i(kx-\omega t)}$ by defining $\psi=\psi_0+\epsilon\psi_1$.
    $$
    \left\{
    \begin{aligned}
    u_0&=\psi e^{i(kx-\omega t)}+\text{c.c.}, \\
    u_1&=A_2(X,T)e^{2i(kx-\omega t)}+\text{c.c.}+A_0(X,T),
    \end{aligned}
    \right.
    $$
    $$
    u_1\rightarrow\mathcal{O}(\epsilon^2)\text{(2.10)}\Rightarrow A_2=\frac{-3(2ik)\psi^2}{-2i\omega+(2ik)^3}=\frac{\psi^2}{k^2}.
    $$

- At $\mathcal{O}(\epsilon^3)$: $\mathcal{L}^{(0)}u_2=-\mathcal{L}^{(2)}u_0-\mathcal{L}^{(1)}u_1-6\partial_x(u_0u_1)-3\partial_X(u_0^2)$
    the solvability condition
    $$
    -\partial_\tau\psi-3ik\partial_{XX}\psi-6ik|\psi|^2\psi/k-6ikA_0\psi=0\tag{2.13}
    $$
    Equating the coefficients of the oscillation free (time average) terms in (2.13)
    $$
    -\partial_T A_0-6\partial_X|\psi|^2=0\Rightarrow A_0=-\frac{2|\psi|^2}{k^2}
    $$
    noting that $\mathrm{d}^2\omega/\mathrm{d}k^2=-6k$, (2.13) leads to the cubic NLS equation
    $$
    i\frac{\partial\psi}{\partial\tau}+\frac{1}{2}\frac{\mathrm{d}^2\omega}{\mathrm{d}k^2}\frac{\partial^2\psi}{\partial\xi^2}+\frac{6}{k}|\psi|^2\psi=0.
    $$

## The water-wave problem

- The governing equations:
    for incompressible, inviscid and irrotational fluid
    the conservation of mass $\Delta \phi=0$ ( $\boldsymbol{u}=\nabla\phi(x,y,z,t)$ )
    the Bernoulli's equation
    $$
    \frac{\partial\phi}{\partial t}+\frac{1}{2}|\nabla\phi|^2+gz+\frac{p-p_0}{\rho}=0.
    $$
- The flow domain:
    the free surface $F(x,y,z,t)\equiv\eta(x,y,t)-z=0$
    the solid bottom $z=-h$
- Boundary conditions:
    the kinematic condition on the free surface: $DF/Dt=0\Rightarrow$ $\eta_t+\phi_x\eta_x+\phi_y\eta_y-\phi_z=0$ (the free surface is a streamline)
    the dynamic condition on the free surface:
    $$
    \phi_t+\frac{1}{2}\left(\phi_x^2+\phi_y^2+\phi_z^2\right)+g\eta-\frac{\sigma}{\rho}C=0
    $$
    where $C$ is the curvature of the free surface.
    the boundary condition at the bottom: $\phi_z(x,y,-h,t)=0$

To summarize, solve for $\eta(x,y,t)$ and $\phi(x,y,z,t)$
$$
\begin{aligned}
\Delta\phi\equiv\phi_{xx}+\phi_{yy}+\phi_{zz}&=0,\text{ for }(x,y,z)\in\mathbb{R}\times\mathbb{R}\times[-h,\eta], \\
\eta_t+\phi_x\eta_x+\phi_y\eta_y-\phi_z&=0,\text{ on }z=\eta(x,y,t), \\
\phi_t+\frac{1}{2}\left(\phi_x^2+\phi_y^2+\phi_z^2\right)+g\eta-\frac{\sigma}{\rho}C&=0,\text{ on }z=\eta(x,y,t), \\
\phi_z&=0,\text{ on }z=-h
\end{aligned}
$$

### Linearization of the 2D problem

Looks for solutions which are periodic in $x$ with wave number $k$ and in $t$ with frequency $\omega$.
Introduce dimensionless variables:
$$
(x^*,z^*)=(kx,kz),\quad\eta^*=\frac{\eta}{a},\quad t^*=\omega t,\quad\phi^*=\frac{k}{\omega a}\phi,
$$
where $a$ denotes the amplitude of the wave.

Dropping the stars, the surface wave problem linearized around the equilibrium state $\eta=0,\boldsymbol{u}=\boldsymbol{0}$ reads:
$$
\begin{aligned}
\phi_{xx}+\phi_{zz}&=0,\text{ for }(x,z)\in\mathbb{R}\times[-kh,0], \\
\eta_t-\phi_z&=0,\text{ on }z=0, \\
\phi_t+\left(\frac{gk}{\omega^2}\right)\eta-\left(\frac{\sigma k^3}{\rho\omega^2}\right)\eta_{xx}&=0,\text{ on }z=0, \\
\phi_z&=0,\text{ on }z=-kh
\end{aligned}
$$

assume $\eta(x,t)=\cos(x-t+\Theta)$, we can obtain
$$
\phi(x-t,z)=\frac{1}{\tanh(kh)}\sin(x-t+\Theta)\frac{\cosh(z+kh)}{\cos(kh)}
$$
and the dynamic condition yields the dispersion relation for linearized 2D capillary-gravity periodic waves in water of finite depth
$$
\omega^2-gk\tanh(kh)\left(1+\frac{\sigma k^2}{\rho g}\right)=0.
$$

- Interpretation of the group velocity:
    1. the travel velocity of the envelope;
    2. the speed of propagation of energy.

### For 3D waves

- The extension of the dispersion relation to three-dimensional waves is
    $$
    \omega^2-g|\boldsymbol{k}|\tanh(|\boldsymbol{k}h|)\left(1+\frac{\sigma|\boldsymbol{k}|^2}{\rho g}\right)=0
    $$
    where $|\boldsymbol{k}|=\sqrt{k^2+l^2}$.


