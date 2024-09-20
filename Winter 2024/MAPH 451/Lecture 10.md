# Singular Perturbation Theory

We use this method for when we have non-analytic dependence on $\epsilon$. That is, when $\epsilon$ is attached to the highest order derivative.

Example: Navier-Stoke's Equation

The NS equation reads

$$
\pdv{\vec{u}}{t} + (\vec{u}\cdot \nabla)\vec{u} -\nu \nabla^{2}\vec{u}=-\nabla \rho.
$$

For small viscosity fluids, $\nu$ can be interpreted as a small parameter. Another example is the Schrödinger equation:

$$
\frac{-\hbar^{2}}{2 m}\nabla^{2}\Psi + V \Psi = -i \hbar \pdv{\Psi}{t},
$$

where $\hbar^{2}/2 m$ can be considered to be the small parameter.

## Boundary Layer Theory

Consider

$$
\epsilon y'' + (1 + x)y' + y = 0 \qc y (0)= y (1)= 1, \; \epsilon \ll 1.
$$

We "know" that the boundary layer is at $x = 0$. We then make the guess

$$
\begin{align}
y (x)\underset{x \rightarrow 0}{\sim} \exp \left(\frac{-x}{\delta} \right) \\[1 em]
\delta (\epsilon)\underset{\epsilon \rightarrow0}{=} 0.
\end{align}
$$

Then,

$$
\begin{align}
y'' & \gg y' \gg y \\[1 em]
\frac{y}{\delta^{2}} & \gg \frac{y}{\delta} \gg y.
\end{align}
$$

We now have an inner region $x < \delta$ and an outer region $x > \delta$, with corresponding $y_{i}$ and $y_{o}$. Let us start with the outer region: As before,

$$
\begin{align}
y_{o} = \sum\limits_{n = 0}^{\infty}\epsilon^{n}y_{n}^{o} \\[1 em]
\epsilon_{0}:\quad (1 + x)y^{o}_{0}\,' + y^{o}_{0} & = 0 \implies y_{0}^{o}= \frac{C}{1 + x}, \; y (1)= 1 \implies C = 2 \\[1 em]
\epsilon^{2}:\quad (1 + x)y_{1}^{o}\,' + y_{1}^{o} & = -y_{0}^{o},'' = -4 (1 + x)^{3} \\
y_{1}^{o} & = 2 (1 + x)^{3}-[2 (1 + x)]^{-1}.
\end{align}
$$

Now for the inner region. Let $z = x/\epsilon$. Then

$$
\begin{align}
\dv{y_{i}}{x} & = \frac{1}{\epsilon}\dv{y_{i}(z)}{z} =  \frac{1}{\epsilon}\dot{y}_{i} \\[1 em]
y''_{i} & = \frac{1}{\epsilon^{2}}\ddot{y}_{i}.
\end{align}
$$

In the new variables, we have

$$
\begin{align}
\cancelto{\neq 0}{\frac{1}{\epsilon}}[\ddot{y}_{i}+ (1 + z \epsilon)\dot{y}_{i}+ \epsilon y_{i}] & = 0 \\[1 em]
y_{i}(z) & = \sum\limits_{n = 0}^{\infty}\epsilon^{n}y_{i}^{n}
\end{align}
$$

$$
\begin{align}
\epsilon^{0}:\quad \ddot{y}_{0}^{i} + \dot{y}_{0}^{i} & = 0 \implies y_{0}^{i} = A + C_{0}(e^{-z}-1), \; y (0)= 1 \implies A = 1,\; C_{0}= 0 \\[1 em]
\epsilon^{1}:\quad \ddot{y}_{1}^{i} + \dot{y}_{1}^{i} & = -z y_{0}^{i}-y_{0}^{i}, \; y_{1}^{i}(0) = 0 \\
y_{1}^{i} & = -z + C_{0}\left(\frac{-z^{2}e^{-z}}{2}+ z \right) + C_{1}(e^{-z}-1)
\end{align}
$$

We now have to use our free constants $C_{0}$ and $C_{1}$ to match $y_{i}$ and $y_{o}$. To do so, we first find a "matching region" where both approximations give the same result. For the inner region, we have $z \epsilon \ll 1$ and therefore $x \ll 1$, while for the outer region we have $\epsilon \ll x$. Our matching region is then $\epsilon \ll x \ll 1$. Expanding in $x$ and neglecting $e^{-z}$ (since $z \gg 1$ so $e^{-z}\ll1$), our outer solution yields, in $\epsilon^{0}$,

$$
\begin{align}
y^{o} & = 2 (1 + x)^{-1} \\[1 em]
& \approx 2 + \order{x} + \order{\epsilon}
\end{align}
$$

while the inner solution yields

$$
\begin{align}
y_{i} & = 1 + C_{0}(\cancel{e^{-z}}-1) + \order{\epsilon} \\[1 em]
& \approx 1-C_{0} + \order{\epsilon} \implies C_{0} =-1.
\end{align}
$$

Therefore

$$
y_{o} \approx y_{i}\approx y_{m} = 2,
$$

with $y_{m}$ being the matching solution.

We can do the same in $\epsilon^{1}$, but the solution has a different matching region: $x^{2}\ll \epsilon \implies \epsilon \ll x \ll \sqrt{\epsilon}$. To $n-$th order, the region becomes $\epsilon \ll x \ll \epsilon^{\frac{n}{n + 1}}$.

## Uniform Approximation

To patch together our 3 solution into one $y_{u}$, we have

$$
y_{u} = y_{i}+ y_{o} -y_{m}.
$$

This guarantees a smooth patching along all three regions.