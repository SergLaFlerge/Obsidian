### Theorem

Let $\xi \in \Lambda^{r}(V)$, with $\dim V = n$ and let $\set{e_{i}}$ be a basis for $V$.
- If $r > n$ then $\xi = 0$.
- If $r \leq n$, then $\set{e_{i_{1}}\wedge \cdots \wedge e_{i_{r}} \mid 1 \leq i_{1} \leq \cdots \leq i_{r} \leq \cdots \leq i_{n}}$ is a basis for $\Lambda^{r}(V)$ and $$\dim (\Lambda^{r}(V))= \frac{n!}{r! (n-r)!}.$$

In particular, $e_{1}\wedge \cdots \wedge e_{n}\neq 0$, and $\dim (\Lambda{n}(V))= 1$.

From this, we get another duality:

Let $v_{1}, ..., v_{r}\in V$, $v^{*1}, ..., v^{*r}\in V^{*}$. Then

$$
\begin{align}
v_{1}\wedge \cdots \wedge v_{r}\in \Lambda^{r}(V) \\[1 em]
v^{*1}\wedge \cdots \wedge v^{*r} \in \lambda{r}(V^{*}),
\end{align}
$$

where

$$
\begin{align}
\ev{\ev{\cdot, \cdot}}:\Lambda^{r}(V)\wedge \Lambda^{r}(V^{*}) & \mapsto \mathbb{R} \\[1 em]
\ev{\ev{v_{1}\wedge \cdots \wedge v_{n}, \; v^{*1}\wedge \cdots \wedge v^{*r}}} & = \det (\ev{v_{i}, v^{*j}}).
\end{align}
$$

Notice that this dual, and our previous dual for general $r-$tensors disagree by a factor of $r!$.

#### Lemma

The set $S = \set{v_{1}, \cdots, v_{r}}\subset V$ is not linearly independent if and only if

$$
v_{1}\wedge \cdots \wedge v_{r} = 0.
$$

#### Cartan's Lemma

Suppose $S = \set{v_{1}, \cdots v_{r}}\subset V$ , $W = \set{w_{1}\cdots w_{r}}\subset V$, and $S$ is linearly independent. If

$$
0 = \sum\limits_{i = 1}^{r}v_{i}\wedge w_{i},
$$

then each element off $W$ is a linear combination of elements in $S$, i.e.

$$
w_{j} = \sum\limits_{j = 1}^{r}c_{ij}v_{j},
$$

where the $c_{ij}$ are symmetric.

#### Lemma

Suppose $S = \set{v_{1}, \cdots, v_{r}}\subset v_{r}$ is linearly independent, and $W \in \Lambda^{p}(V)$. Then

$$
w = v_{1}\wedge \psi_{1}+ \cdots + v_{r}\wedge \psi_{r}
$$

for some $\psi_{1}\cdots \psi_{r}\in \Lambda^{p-1}(V)$ if and only if

$$
v_{1}\wedge \cdots \wedge v_{r}\wedge w = 0.
$$

#### Lemma

Suppose $S = \set{v_{\alpha}, w_{\alpha}\mid 1 \leq \alpha \leq k}$ is a linearly independent set of vectors in $V$. Also suppose $S' = \set{v'_{\alpha}, w'_{\alpha}\mid 1 \leq \alpha \leq k}$ is another set of vector such that

$$
\sum\limits_{\alpha = 1}^{k} v_{\alpha}\wedge w_{\alpha} = \sum\limits_{\alpha= 1}^{k}v'_{\alpha}\wedge w'_{\alpha}.
$$

Then the elements of $S'$ are a linear combination of elements in $S$, and $S'$ is a linearly independent set.