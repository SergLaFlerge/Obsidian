# Dirac Delta Function and the Schrödinger Equation for Bound Systems

We are already familiar with summation notation.

> [!PDF|note] [[L1-Review.pdf#page=3&selection=7,1,9,26&color=note|L1-Review, p.3]]
> Dirac delta function is an infinitely high, infinitely narrow spike at the origin.

We use the Dirac delta function inside an integral to "pick out" values of a function:

$$
\int_{-\infty}^{\infty}f (x)\delta (x-a) \dd{x} = f (a),
$$

for $f(x)$ continuous. We can also have a delta function of functions. In general,

$$
\delta (g (x)) =  \sum\limits_{i = 1}^{n}\frac{1}{\abs{g' (x_{i})}}\delta(x-x_{{i}}).
$$

The integral of the delta function is the Step Function:

$$
\theta (x) = \int_{-\infty}^{x}\delta{x'}\dd{x'}.
$$

## Schrödinger Equation

$$
\left(-\frac{\hbar^{ 2}}{2 m}\nabla^{ 2}+ V \right)\Psi (\vec{r}, t) = i \hbar\pdv{t}\Psi (\vec{r}, t).
$$

We will not be using the Schrödinger equation very much, as it is non-relativistic; The main result we care about is that, for a spherically symmetric bound system, we obtain quantized orbital angular momentum and quantized energy levels, which depend on certain quantum numbers $l, \; m \;, n$. The magnitude is given as $\abs{L}= \sqrt{l (l + 1)}\hbar$