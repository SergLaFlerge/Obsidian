# Relativity Review

Remember the Lorentz transforms. We will be using 4-vectors so as to not have to write 4 equations every time we want to do a calculation. While normally, we would use something like $x_{\mu}$, this can be confused with muons, and so we will use $\underset{\sim}{x}$ sometimes as well.

$$
\underset{\sim}{x} = x^{\mu} = (x_{0}; x_{1}, x_{2}, x_{3})
$$

With

$$
x^{0} = ct, \; x^{1} = x, \; x^{2} = y, \; x^{3} = z.
$$

We can write a (Lorentz) transform from a frame $S$ to a second frame $S'$ using $\Lambda_{\nu}^{\mu}$. [[L2-Relativity.pdf#page=3|L2-Relativity, p.3]].

In particular, we can write

$$
x'^{\mu} = \Lambda_{\nu}^{\mu}x^{\nu} = \sum\limits_{\nu = 0}^{3}\Lambda_{\nu}^{\mu}x^{\nu}.
$$

Recall that $x_{\mu}$ is covariant while $x^{\mu}$ is contravariant. This is important because, to get a proper magnitude for these 4-vectors, we need  $x_{\mu}\cdot x^{\mu}$, where in particular there is an implied metric $g_{\mu \nu}$ sandwiched between them, where $g_{\mu \nu}=\text{diag}(1,-1,-1,-1)$. Therefore,

$$
\begin{align}
x^{\mu}x_{\mu} & = x^{\mu}g_{\mu \nu}x^{\nu} \\[1 em]
& = (x^{0})^{2} - (x^{1})^{2} -(x^{2})^{2} -(x^{3})^{3}.
\end{align}
$$

This value is constant, and so we can use it to categorize 4-vectors into three types:

1. Space-like $x^{\mu}x_{\mu} < 0$.
2. Time-like $x^{\mu}x_{\mu} > 0$.
3. Light-like $x^{\mu}x_{\mu} = 0$.

## 4-Velocity

To calculate velocity, we must use the object's time $\tau$. Then,

$$
\begin{align}
\vec{v} & = dv{x}{t} = \frac{1}{\gamma}\dv{x}{\tau} \\[1 em]
\dv{x}{\tau} & = \gamma \dv{x}{t}.
\end{align}
$$

As such, $\underset{\sim}{u} = \eta^{\mu} = (\gamma_{u}c; \gamma_{u}\vec{u})$. One can check that $\eta^{\mu}\eta_{\mu} = c^{2}$.

We do not use classical velocity because it is *not* a 4-vector, and so does not transform like one. [[L2-Relativity.pdf#page=8|L2-Relativity, p.8]]

In general, we don't even really use 4-velocity to begin with. Instead, we use 4-momentum. In this case, the 4-momentum  is defined as $p^{\mu}= m \eta^{\mu} = (\gamma mc ; \gamma m \vec{v})$.

The magnitude of 4 momentum is

$$
\begin{align}
p^{\mu}p_{\mu} & = \gamma^{2}m^{2}c^{2} -\gamma^{2}m^{2}v^{2} \\[1 em]
& = \gamma^{2}m^{2}c^{2}\left(1-\frac{v^{2}}{c^{2}} \right) \\[1 em]
& = m^{2}c^{2}.
\end{align}
$$

Don't forget that relativistic mass $(\gamma m)$ is absolutely **Wrong!**. [[L2-Relativity.pdf#page=10|L2-Relativity, p.10]]

For a rank $n$ tensor, we need to apply $n$ $\lambda$ factors in order to transform it. Same thing applies with index raising and lowering: To raise/lower $n$ indices, we apply $n$ metrics.

## Energy

We use momentum to calculate energy. In particular, we can rewrite 4-momentum as $p^{\mu}= (E/c:\vec{p})$. The invariant magnitude is then

$$
p^{\mu}p_{\mu} = \frac{E^{2}}{c^{2}}-p^{2} = m^{2}c^{2}.
$$

From here, we obtain Einstein's mass-energy relation:

$$
E^{2} = m^{2}c^{4} + p^{2}c^{2}.
$$

## Classical Collisions

There are two types of collisions:

- True collisions $A + B \to C + D (+ \cdots)$.
- Decays $A \to B + C (+ \cdots)$.

Classical collisions are simple, [[L2-Relativity.pdf#page=13|L2-Relativity, p.13]]. In classical collisions, mass and momentum remain constant.

## Relativistic Collisions

Similar principles apply. Total energy and momentum are constant, while kinetic energy may be gained, lost, or remain constant. It should be noted that in relativistic collisions, mass is rarely constant. We can, however, determine the energy and momentum of the initial state from the final state, and therefore also find the invariant mass.

Examples: [[L2-Relativity.pdf#page=15|L2-Relativity, p.15]], [[L2-Relativity.pdf#page=18|L2-Relativity, p.18]]

## Mandelstam Variables

For processes involving exclusively 2 particle to 2 particle scattering, we note three useful quantities that are Lorentz invariant. For $A + B \to C + D$,

$$
\begin{align}
s & = \frac{(p_{A}+ p_{B})^{2}}{c^{2}} \\[1 em]
t & = \frac{(p_{A}-p_{C})^{2}}{c^{2}} \\[1 em]
u & = \frac{(p_{A}-p_{D})^{2}}{c^{2}}.
\end{align}
$$

$s$ and $t$ represent center of mass energy squared and momentum transfer squared, respectively. These will be useful for when with consider Feynman diagrams.