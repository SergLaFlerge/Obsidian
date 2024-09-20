# The Tangent Bundle $TM$

Recall the total space:

$$
E = \bigcup_{p \in M}T_{p}M.
$$

there is also a projection $\pi:v|_{p}\rightarrow p$, and a local trivialization $\Phi:\pi^{-1}(U)\rightarrow U \times \mathbb{R}^{n}:v^{i}\pdv{x^{i}}\mapsto (p, (v^{1}, ..., v^{n})= (p, v))$

## Transition Functions

For two separate trivializations $U \times \mathbb{R}^{n}$ and $\overline{U}\times \mathbb{R}^{n}$ with non-empty intersection, we have, for transition functions $\Phi, \overline{\Phi}$,

$$
\overline{\Phi}\circ \Phi^{-1}(p, v) = \left(p, \underbrace{ \left( \eval{\pdv{\bar{x}^{1}}{x^{j}}}_{x}v^{j}\cdots \eval{\pdv{\bar{x}^{n}}{x^{j}}}_{x}v^{j} \right) }_{ \tau (p)v, \; \tau \in \text{ GL}(n, \mathbb{R}) } \right).
$$

# Cotangent Bundle $T^{*}M$

We now have $E = \bigcup_{{p \in M}}T_{p}^{*}M$, with projection $\pi \; \xi|_{p}\rightarrow p$, $p \in T_{p}^{*}M$. Now, for $U \subset M$, define

$$
\begin{align}
\Phi:\pi^{-1}(U) & \rightarrow U \times \mathbb{R}^{n} \\[1 em]
\xi_{i}\dd{x^{i}}|_{p} & \mapsto (p, (\xi_{1}, ..., \xi_{n})).
\end{align}
$$

Its respective transition functions are then

$$
\begin{align}
\overline{\Phi}\circ \Phi^{-1}(p, \xi) & = \left(p,  \left( \eval{\pdv{\bar{x}^{j}}{x^{1}}}_{\xi}\xi_{j}\cdots \eval{\pdv{\bar{x}^{ j}}{x^{n}}}_{\xi}\xi_{j} \right) \right) \\[1 em]
& = \left(p, \underbrace{ \left( \eval{\pdv{\bar{x}^{ 1}}{x^{j}}}_{\xi}\xi^{j}\cdots \eval{\pdv{\bar{x}^{n}}{x^{j}}}_{\xi}\xi^{n} \right) }_{ \tau (p)\xi, \; \tau \in \text{ GL}(n, \mathbb{R}) } \right).
\end{align}
$$

$(\tau (p)v)^{i}= J^{i}_{j}v^{j}$, with  $J$ being the Jacobian matrix. This implies $\tau (p)v = J \cdot v$, which is matrix multiplication on the left, while $(\tau (p)\xi)_{i}= J^{i}_{j}\xi_{i}=\xi \cdot J$, which is then matrix multiplication on the right.

# Tangent Bundles of Arbitrary Rank

We can now consider bundles of type $(k, l)$ for arbitrary $k$ and $l$.

>[! Examples]+ Example
>consider $(1, 1)$ tensor fields:$T = T^{i}_{j}\partial_{i}\otimes \dd{x^j}$. For $U \subset M$, the local trivializations have the form
>
>$$
\begin{align}
\Phi:\pi^{-1}(U) & \rightarrow \mathbb{R}^{n} \\[1 em]
T|_{p} & \mapsto (p, (T^{1}_{1}, ..., T^{n}_{n})).
\end{align}
>$$
>
>the trivialization functions are then
>
>$$
\overline{\Phi}\circ \Phi(p, T) = \left(p, \left(\pdv{\bar{x}^{i}}{x^{1}}\pdv{\bar{x}^{1}}{x^{j}}T^{j}_{i}, \cdots, \pdv{\bar{x}^{i}}{x^{n}}\pdv{\bar{x}^{n}}{x^{j}}T^{j}_{i} \right) \right)
>$$

The exterior vector bundle $\Lambda^{r}(M)$ is then $\bigcup_{p \in M}\Lambda^{r}(T_{p}M)$, and the exterior form bundle is $\Lambda^{r}(M^{*})= \Lambda^{*r}(M)= \bigcup_{p \in M}\Lambda^{r}(T^{*}_{p}M)$.

# Sections of Bundles

Let $f:M \rightarrow E$ be a smooth map, where $E$ is the total space of a vector bundle $\pi:EM$.

If $\pi \circ f:M \rightarrow M:p \mapsto p \; \forall \; p \in M$ (that is, $\pi \circ f$ is the identity mapping), then $f$ is a smooth section of $E$.
- $f$ assigns a $v|_{p}\in V$ to each $p \in M$.
- Sections of the ton gent bundle are vector fields.
- Sections of the cotangent bundle are $1-$forms.
- Sections of $\Lambda^{r}(M^{*})$ are differential forms of  degree $r$.

# Exterior Differentiation

We denote the space of sections by $A^{r}(M)= \Gamma (\Lambda^{r}(M))$, where $\Gamma (\cdot)$ is the space of sections of $(\cdot)$. Elements of $A^{r}(M)$ are called *exterior differential $r-$forms*. $A(M)$ is then

$$
A (M) = \sum\limits_{r = 0}^{m}A^{r}(M),
$$

where $m = \dim{M}$, and $A^{0}= C^{\infty}$. Elements of $A (M)$ are exterior  differential forms on $M$.

We can extend the [[Lecture 12#Wedge Product|wedge product]] to differential forms: For $\omega_{1}$ and $\omega_{2}$ differential forms, we have

$$
(\omega_{1} \wedge \omega_{2})|_{p} = \omega_{1}|_{p}\wedge_{2}|_{p}.
$$

The wedge product then defines a map $\wedge:A^{r}(M)\times A^{s}(M)\rightarrow A^{r + s}$.