---
title: Introduction to Perturbation Techniques
math: true
date: 2026-04-04 15:45:31
categories:
    - mathematics
tags:
    - perturbation
    - Floquet theory
excerpt:
    The Floquet theory to solve the Mathieu equation.
---

Reference book: *Introduction to Perturbation Techniques* by Ali Hasan Nayfeh.

[pdf with notes](Introduction_to_Perturbation_Techniques.pdf)

## 11. The Mathieu Equation

$$
\ddot{u}+(\delta+2\epsilon\cos 2t)u=0 \tag{11.2}
$$

### 11.2 The Floquet Theory

(11.2) is a second-order linear homogeneous equation, it possesses two linearly independent solutions $u_1(t)$ and $u_2(t)$ satisfying the initial conditions
$$
\begin{array}{cc}
    u_1(0)=1 & \dot{u}_1(0)=0 \\
    u_2(0)=0 & \dot{u}_2(0)=1
\end{array}\tag{11.13}
$$

The solutions have a period of $\pi$, the evolution equation in matrix notation is
$$
\boldsymbol{u}(t+\pi)=\boldsymbol{A}\boldsymbol{u}(t) \tag{11.20}
$$
$$
\boldsymbol{A}=\left[\begin{array}{cc}
    u_1(\pi) & \dot{u}_1(\pi) \\
    u_2(\pi) & \dot{u}_2(\pi)
\end{array}\right]\quad \boldsymbol{u}=\left[\begin{array}{c}
    u_1 \\
    u_2
\end{array}\right] \tag{11.21}
$$

Diagonalizing the matrix $\boldsymbol{A}$, we have a diagonal matrix $\boldsymbol{B}$ whose eigenvalues are given by
$$
\lambda^2-\text{tr}(\boldsymbol{A})\lambda+1=0 \tag{11.32}
$$
$$
\lambda_{1,2}=\frac{\text{tr}(\boldsymbol{A})\pm\sqrt{[\text{tr}(\boldsymbol{A})]^2-4}}{2} \tag{11.34}
$$

And the evolution equation gives
$$
\boldsymbol{v}(t+\pi)=\boldsymbol{B}\boldsymbol{v}(t) \tag{11.27}
$$
$$
\boldsymbol{B}=\boldsymbol{P}\boldsymbol{A}\boldsymbol{P}^{-1} \tag{11.29}
$$
$$
\boldsymbol{u}(t)=\boldsymbol{P}^{-1}\boldsymbol{v}(t) \tag{11.24}
$$

------

**(a)** When the diagonal matrix has the form
$$
\boldsymbol{B}=\left[\begin{array}{cc}
    \lambda_1 & 0 \\
    0 & \lambda_2
\end{array}\right] \tag{11.35}
$$

The evolution equation reads,
$$
\begin{array}{c}
    \boldsymbol{v}_1(t+\pi)=\lambda_1\boldsymbol{v}_1(t) \\
    \boldsymbol{v}_2(t+\pi)=\lambda_2\boldsymbol{v}_2(t)
\end{array} \tag{11.38}
$$

$$
\boldsymbol{v}_1(t+n\pi)=\lambda_1^n\boldsymbol{v}_1(t) \tag{11.39}
$$

So $\lambda_1=\lambda_2=\pm 1$ separate stable from unstable solutions and are usually referred to as *transition values*.

The exact solution is
$$
\boldsymbol{v}_{1,2}(t)=e^{\gamma_{1,2} t}\phi_{1,2}(t) \tag{11.46,11.48}
$$
where $\phi_{1,2}(t)$ is arbitrary function satisfing $\phi_{1,2}(t+\pi)=\phi_{1,2}(t)$, and the *characteristic exponent* is
$$
\gamma_{1,2}=\frac{1}{\pi}\ln \lambda_{1,2} \tag{11.44}
$$

------

**(b)** When $\boldsymbol{A}$ is not diagonalizable, the matrix $\boldsymbol{B}$ has the form
$$
\boldsymbol{B}=\left[\begin{array}{cc}
    1 & 0 \\
    1 & 1
\end{array}\right]
\text{ or }\left[\begin{array}{cc}
    -1 & 0 \\
    1 & -1
\end{array}\right] \tag{11.37}
$$

The solution is
$$
\begin{array}{c}
    \boldsymbol{v}_1(t)=e^{\gamma t}\phi_1(t) \\
    \phi_1(t+\pi)=\phi_1(t) \quad\text{and}\quad \gamma=\dfrac{1}{\pi}\ln \lambda
\end{array} \tag{11.50}
$$

$$
\boldsymbol{v}_2(t)=e^{\gamma t}[\phi_2(t)+\frac{t}{\pi\lambda}\phi_1(t)],\ \phi_2(t+\pi)=\phi_2(t) \tag{11.52}
$$

------

$$
\lambda_{1,2}=\frac{\text{tr}(\boldsymbol{A})\pm\sqrt{[\text{tr}(\boldsymbol{A})]^2-4}}{2} \tag{11.34}
$$

When $|\text{tr}(\boldsymbol{A})|>2$, the solutions contains one unbounded and another bounded with time.

![Figure 11-1](F11-1.png)

When $|\text{tr}(\boldsymbol{A})|<2$, the solutions are bounded.

![Figure 11-2](F11-2.png)
