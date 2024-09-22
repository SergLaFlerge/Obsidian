# Derivations

A derivation on a vector space $F_{p}$ of functions at $p \subset M$ is a linear map that obeys the Leibniz (product) rule:

$$
\begin{align}
X (fg) & = f (p)\eval{X(g)}_{p} +  \eval{X (f)}_{p} g (p) \\[1 em]
X: F_{p} & \rightarrow \mathbb{R}.
\end{align}
$$

Just like how we don't write brackets for every derivative, we often just write $Xf$ instead of $X (f)$. There are three properties to a derivation:
- $Xf$ is linear, that is, it respects addition and scalar multiplication.
- If $f  = c =$ constant, then $X (1)= X (1 \cdot 1)= 1 \cdot X (1)+ X (1)\cdot 1 = 2 X (1)$, which implies $X (1)= 0$, and so $X (c)= 0$ for any constant using scalar multiplication.
- If $f (p)= g (p)= 0$, then $\eval{X (fg)}_{p}= 0$.

## Tangent Spaces

A tangent space $T_{p}M$ to $M$ at $p$ is the set of derivations at $p$. The elements are tangent vectors at $p$.

### Coordinate Vectors

Given a coordinate neighborhood about $p \in M$ defining coordinates $x^{i}= \phi^{i}(\cdot)$ on the neighborhood $U$, let $f$ be any $C^{\infty}$ function at $p$. Let $x^{i}= (x^{1}, ..., x^{n)=}\phi^{i}(q)$. Define now $\partial_{i}$ by

$$
\begin{align}
(\partial_{i}f)(p) :& = \pdv{x^{i}}(f \circ \phi^{-1})(x) \\[1 em]
f: M & \rightarrow \mathbb{R}^{n}.
\end{align}
$$

Often we will write $f (x)$ to mean $f (\phi^{-1}(x))$, as the inverse map is implied by the nature of the structure. From that, we can also say that $(U, \phi)$ and $(U, x^{i})$ are equivalent. We will also use, when convenient, Einstein summation convention, where repeated indices are assumed to be summed over.

We call this $\partial_{i}$ a coordinate vector. Coordinate vectors form the basis for $T_{p}M$, as they are derivations. We now proceed with two claims:

#### Claim 1

The set $\set{\partial_{i}\mid_{p}, i = 1, ..., n}$ is linearly independent.

Proof: let

$$
0 = v^{i}\partial_{i}\mid_{p}.
$$

Let this act on $\phi:U \rightarrow \mathcal{O}$:

$$
0 = v^{i}\partial_{i}(\phi^{i})(p) = v^{i}\pdv{x^{j}}{x^{i}} = v^{i}\delta_{i}^{j} = v^{j}.
$$

Thus $v^{j}= 0$ by acting on each $x^{j}$ in turn. As such, the $\partial_{i}$ are independent.

#### Claim  2

$\set{\partial_{i}, i = 1, ..., n}$ spans $T_{p}(M)$.

Proof: Let $X \in T_{p}(M)$ and let $x^{i}$ be coordinate functions of $p \in M$. Let $\phi^{i}(p)= a^{i}$ and $\phi^{i}(q)= x^{i}$ for some neighborhood $U$ about $p$ and $q \in U$.

Define numbers $v^{i}= X (x^{i})= X (q)$ and

$$
\begin{align}
f&: M \rightarrow \mathbb{R}^{n} \\[1 em]
F&: f \circ \phi^{-1}: \mathbb{R}^{n}\rightarrow \mathbb{R}.
\end{align}
$$

Taylor's theorem gives

$$
F (x) = F (a) + \sum\limits_{i = 1}^{n}(x^{i}-a^{i})\eval{\pdv{F}{x^{i}}}_{a}+ \sum\limits_{i = 1}^{n}(x^{i}-a^{i})\eval{g_{i}(x-a)}_{x = a}.
$$

Since $g (0)= 0$, have

$$
\begin{align}
Xf & = XF (a)+ \sum\limits_{i = 1}^{n}(X (x^{i})-\cancelto{0}{X (a^{i})}\eval{\pdv{F}{x^{i}}}_{a} \\[1 em]
& = v^{i}\eval{\pdv{F}{x^{i}}}_{a} \\[1 em]
& = (v^{i}\partial_{i})(f) \\[1 em]
X & = v^{i}\partial_{i}.
\end{align}
$$

Any arbitrary $X \in T_{p}M$ is be written as

$$
X = v^{i}\partial_{i},
$$

hence $\set{\partial_{i}}$ spans $T_{p}M$.

### Theorem

Let $M$ be an $n-$manifold. For any $P \in M$, the tangent space $T_{p}M$ at $p$ is $n-$dimensional. If $(x^{1}, ..., x^{n})$ are local coordinates at $p$, the coordinate vector fields $\set{\partial_{1}, ..., \partial_{n}}$ forms a basis for $T_{p}M$.

### Definition

Let $F_{p}$ be a suitable space of functions at $p \in M$, i.e. $C^{\infty}_{p}$. Let $x (t):(-\epsilon, \epsilon)\rightarrow \mathcal{O}\in \mathbb{R}^{n}$ be a differentiable curve in $\mathbb{R}^{n}$. Then $\gamma (t)= (\phi^{-1}(x))(t)$ is a curve in $U \subset M$.

Let $p = \gamma (0)$. If

$$
Xf = \dv{t}(f (\gamma (t)))
$$

for every $f \in F_{p}$, then the mapping $X:F_{p}\rightarrow \mathbb{R}$ is a tangent vector of the curve $\gamma$ at $p$.