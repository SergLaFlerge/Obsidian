We have one more case for 2-dimensional systems: $\lambda_{i}= a + b_{i}, \; \lambda_{1}= \lambda_{2}^{*}$. In this case,

$$
\bar{\epsilon}(t) = Ce^{\lambda_{\Re}}[\sin (\lambda_{\Im}t + \phi)+ \cos (\lambda_{\Im}t + \phi)].
$$

These solutions give "spiral points", where the point is stable for $\lambda_{\Re}< 0$ and unstable for $\lambda_{\Re}> 0$. 

## Limit Cycles

Take for example

$$
\begin{align}
\dot{y}_{1} & = y_{1} + y_{2} -y_{1}(y_{1}^{2}+y_{2}^{2}) \\[1 em]
\dot{y}_{2} & = -y_{1} + y_{2} -y_{2}(y_{1}^{2}+ y_{2}^{2}).
\end{align}
$$

In this system, we have a critical point at $y_{1}= y_{2}= 0$. Meaning

$$
\begin{align}
\mathbb{M} & =
\begin{bmatrix}
1 & 1 \\
-1 & 1
\end{bmatrix} \\[1 em]
(1-\lambda)^{2}+ 1 & = 0 \\[1 em]
\lambda_{1, 2} & = 1 \pm i.
\end{align}
$$

This is an unstable spiral. What happens when $y_{1}, y_{2}\rightarrow \infty$? Let $z = (y_{1}^{2}+ y_{2}^{2})> 0$. Then

$$
\begin{align}
(1) =
\begin{cases}
\dot{y}_{1} & = -y_{1}z \\[1 em]
\dot{y}_{2} & = -y_{2}z.
\end{cases}
\end{align}
$$

What if we just let $z = 1$? This has little motivation, but the result is quite interesting:

$$
\begin{align}
(2) =
\begin{cases}
\dot{y}_{1} & = -y_{1}z \\[1 em]
\dot{y}_{2} & = -y_{2}
\end{cases},
\end{align}
$$

from which we get

$$
\begin{align}
\mathbb{M} & =
\begin{bmatrix}
0 & 1 \\
-1 & 0
\end{bmatrix}.
\end{align}
$$

As one can see, (1) will go towards $0$ from a circle of very large radius, while (2) will go towards infinity. Since vector fields cannot intersect, they both start to deviate at some radius, which in this case is exactly at radius $1$. $z = 1$ is therefore known as a *limit cycle*.

![[MPAH 451 Limit Cycle.svg|center]]

Plot of the limit cycle from above

<br>

# 3-dimensional Systems

We start this section with a study on the Lorenz (or Strange) attractor. For this, we will use our canonical coordinate system $x, y, z$. The system is as follows:

$$
\begin{align}
\dot{x} & = -\sigma (x-y) \\[1 em]
\dot{y} & = x (\rho-z) -y \\[1 em]
\dot{z} & = xy-\beta z
\end{align}
$$

For now, let us set $\sigma = 3$, $\beta = 1$, and let $\rho > 0$ be a free parameter. We now have

$$
\begin{align}
\dot{x} & = -3 (x-y) \\[1 em]
\dot{y} & = x (\rho-z) -y \\[1 em]
\dot{z} & = xy-z
\end{align}
$$

The first — and most obvious — critical point lies on $x = y = z = 0$. Another critical point comes about when $x = y = \pm \sqrt{z}, \; z = \rho-1$. Clearly $z$ must be positive, which means $\rho > 1$. For $\rho < 1$, we have only the first critical point, as the other one is imaginary. Since the number of grows as $\rho$ increases past $1$, we get what is called a (pitchfork) bifurcation.

Let's now linearize the equation:

$$
\begin{align}
\dot{\epsilon}_{x} & = -3 \epsilon_{x} + 3 \epsilon_{y} \\[1 em]
\dot{\epsilon}_{y} & = \rho \epsilon_{x} -\epsilon_{y} \\[1 em]
\dot{\epsilon}_{z} & = -\epsilon_{z} \\[1 em]
\mathbb{M} & =
\begin{bmatrix}
-3 & 3 & 0 \\
\rho & -1 & 0 \\
0 & 0 & -1 
\end{bmatrix} \\[1 em]
0 & = (\lambda + 1)[(\lambda + 3)(\lambda + 1)-3 \rho] \\[1 em]
\lambda & = -1, \;-2 \pm \sqrt{4-3 (1-\rho)}.
\end{align}
$$

We have two cases for the second and third roots: If $\rho > 1$, the root is positive, but if $\rho < 1$, we have a negative root.
- $\rho < 1$ implies $\lambda_{i}< 0$, so we have a stable point.
- $\rho > 1$ implies $\lambda_{1}> 0, \; \lambda_{2, 3}> 0$, so we get a saddle point.

In the case that $x = y = r$, we then have $z = \rho-1 = r^{2}$ for $\rho 1$. Our system of equations then becomes

$$
\begin{align}
\dot{\epsilon}_{x} & = -3 \epsilon_{x} + 3 \epsilon_{y} \\[1 em]
\dot{\epsilon}_{y} & = \epsilon_{x} -\epsilon_{y} -r \epsilon_{z} \\[1 em]
\dot{\epsilon}_{z} & = r \epsilon_{x} + r \epsilon_{y} -\epsilon_{z} \\[1 em]
\mathbb{M}& =
\begin{bmatrix}
-3 & -3 & 0 \\
1 & -1 & -r \\
r & r & -1
\end{bmatrix} \\[1 em]
0 & = \lambda^{3} + 5 \lambda^{2} + (4 + r)\lambda + 6 r^{2}.
\end{align}
$$

This is not factorable, so let us examine the two limits $r \rightarrow  0$ and $r \rightarrow \infty$. For $r \rightarrow 0$, we get

$$
\begin{align}
\lambda (\lambda^{2}+ 5 \lambda + 4) & = 0 \\[1 em]
\lambda = (-)0,-1,-4.
\end{align}
$$

Therefore $\lambda_{i}< 0$, and we have a stable point. For $r \rightarrow \infty$, we have

$$
\begin{align}
r^{2}\lambda + 6 r^{2} & = 0 \\
\lambda & = -6.
\end{align}
$$

We only get one root, but need two more for a complete solution. The reason behind this is due to the proportionality between $\lambda$ and $r$. If $\lambda < r$, we get the above, but if $\lambda \sim r$, we have

$$
\begin{align}
\lambda^{3} + r^{2}\lambda & = 0 \\[1 em]
\lambda = \pm ir + \frac{1}{2}.
\end{align}
$$

We now have $\lambda_{1, 2}= \pm ir + 1/2$ and $\lambda_{3}=-6$. It is this $1/2$ that makes the strange attractor strange.