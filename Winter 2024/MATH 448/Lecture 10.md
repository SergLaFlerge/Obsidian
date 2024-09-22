# Frobenius Theorem

Suppose $\mathcal{L}^{h}= \text{span}\set{X_{1}, ..., X_{h}}$ is an $h-$dimensional distribution (subspace of $TM$) in an open set $U \subset M$.

There exists a local coordinate system $(U, u^{i})$ such that $\mathcal{L}^{h}= \text{span}\set{\pdv{u^{i}}, \cdots, \pdv{u^{h}}}$ if and only if $\mathcal{L}^{h}$ obeys the Frobenius condition $\comm{X_{(i)}}{X_{(j)}}\in \mathcal{L}^{h}$

# Multilinear Algebra

We start with a field $\mathbb{F}$. With for us is simply $\mathbb{R}$, but could also $\mathbb{C}$for example.

A vector space $V$ over $\mathbb{F}$ (field of color scalars) is a set with two operations:
1. Addition.
2. Scalar multiplication with respect to $\mathbb{F}$.

Such that $(V, +)$ is an abelian group with identity 0 and, $\forall \; \alpha, \beta \in \mathbb{F}$ and $x, y\in V$. Then

- $\alpha (x + y) = \alpha x + \alpha y$
- $(\alpha + \beta)x = \alpha x + \beta x$
- $(\alpha \beta)x = \alpha (\beta x)$
- $0x = 0$, $1x = x$.

## Dual Space

Let $\dim V = n$, and let $f:V \rightarrow \mathbb{F}$ be a linear function, i.e. $f (\alpha u + \beta v)= \alpha f (u)+ \beta f (v)\; \forall \; \alpha, \beta \in \mathbb{F}$, $u, v \in V$.

Define $(f + g)(u)= f (u)+ g (u)$. The space of all such functions is itself a vector space over $\mathbb{F}$, called the dual space $V^{*}$.

Let $\set{e_{i}}$ be a basis for $V$, let $v = v^{i}e_{i}\in V$ and let $f \in V^{*}$, $f  (v)= v^{i}f (e_{i})$ so $f$ is determined by its values acting on $\set{e_{i}}$.

Define linear functions $E^{i}\in V^{*}$ such that $E^{i}(e_{j})= \delta^{i}_{j}$. Then

$$
E^{i}(v) = E^{i}(v^{j}e_{j})= v^{j}\delta^{i}_{j}= v^{i},
$$

and

$$
\begin{align}
f (v) & = f_{i}v^{i} = f_{i}E^{i}(v) \\[1 em]
\implies f (\cdot) & = f_{i}E^{i}(\cdot),
\end{align}
$$

and so $\set{E^{i}}$ is called the dual basis for $V^{*}$ and $\set{e_{i}}$.

## Interior Products and Duality

Define $\ev{\cdot, \cdot}:V \times V^{*}\rightarrow \mathbb{F}$,

$$
\ev{v, v^{*}} = v^{*}(v).
$$

$\ev{\cdot, \cdot}$ is linear in both arguments so it can also be written as $\ev{\cdot, \cdot}:V^{*}\times V \rightarrow \mathbb{F}$.