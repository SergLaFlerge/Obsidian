# What is continuum mechanics?

- It's very hard to calculate the motion of many body systems, so we look at Bulk Properties
- Continuum hypothesis: These bulk properties represent well the collective behavior of sufficiently large systems of particles so that it can be treated as a continuous quantity.

Let $f(\vec{x},\vec{u},t)$ be the probability of finding a particle  with pos $\vec{x}$ and velocity $\vec{u}$ at time $t$. Then, let $L\gg l$, where $l$ is the typical interparticle distance. Then the momentum of the fluid $M$ is

$$
M_{k,i}(\vec{x},t) \equiv \frac{1}{L^{3}}\int\dd[3]{x'}\int\dd[3]{u}u_{i}^{k}f(x',\vec{u},t).
$$

From this, $n\equiv M_{0}$ is the number density, $M_{1,i}/n\equiv \vec{u}$ is the velocity, and

$$
\frac{1}{2n}\sum\limits_{i=1}^{3}(M_{2,1}-u_{1}^{2})=e
$$

is the specific internal energy. All of these are bulk properties. We also have temperature $T$, pressure $P$, viscosity, and energy $E$. $n$ is also symbolized by $\rho$.

$P,\rho,T,e$ are related to each other by Equations of State (EOS).

One EOS we are already familiar with is the ideal gas equation:

$$
P=\frac{R}{\mu}\rho T,
$$

where $R/\mu = c_{P}-c_{V}$, with

$$
\begin{align}
c_{P} &= T\left(\pdv{S}{T}\right)_{P}\\[1em]
c_{P} &= T\left(\pdv{S}{T}\right)_{V},
\end{align}
$$

where $V$ is volume. We can then write the ideal gas equation as

$$
\begin{align}
P &=\left( \frac{c_{P}}{c_{V}}-1 \right)c_{V}\rho T \\[1em]
&=(\gamma-1)\rho e,\quad c_{V}T=e
\end{align}
$$

this is known as the $\gamma$-low EOS. We can also write the EOS as

$$
\begin{align}
P = (\Gamma_{3}-1)\rho e
\Gamma_{3}-1 = \left(\pdv{\ln{T}}{\ln{\rho}}\right)_{S}
\end{align}
$$