# Immersion, Submersions, and Embeddings

Say we have $f:M \rightarrow N$. Let the linear map $f_{*}:T_{p}^{*}M\rightarrow T_{f (p)}^{*}N$ have rank $r$. Define $r$ to be the rank of $f$. We consider the case where $f_{*}$ is non-degenerate:
- If $f_{*}$ is surjective at every $p \in M$, then $f$ is a submersion.
- If $f_{*}$ is injective at every $p \in M$, then $f$ is an immersion.
- If $f$ is a homeomorphism onto its image, then it is a topological embedding.
- If a topological embedding is smooth, then it is a smooth embedding.

>[!Examples]+ Example
>Take $f:\mathbb{R}\rightarrow \mathbb{R}^{2}$ with $f (t)= (2 \cos t, \sin 2 t)$. Then
>
>$$
\begin{align}
\dv{f}{t} & = 2 (-\sin{t}, \cos 2 t).
\end{align}
>$$
>
>This $\dd{f}$ is a row vector, and it has full rank everywhere ($\dd{f}\neq (0, 0)$ anywhere), so $f$ is immersed. However, $f$ is not embedded, as we have a self-intersection.

Another example is in the handwritten notes, but it is not more insightful.

# Embedded (Regular) Submanifolds

Say we have a standard embedding of $\mathbb{R}^{m}$ in $\mathbb{R}^{n}$, with $m < n$.
- Consider $\mathcal{U}$ to be an open set in $\mathbb{R}^{n}$.
- Also consider $S = \set{(x^{1}, x^{2}, ..., x^{m}, x^{m + 1}, ..., x^{n})\in \mathcal{U}\mid x^{m + 1}= c^{m + 1}, ..., x^{n}= c^{n}}$, where $c^{\alpha}$ are constants
For any choice of constants $c^{\alpha}$, we say that $S$ is an *$m-$slice (or just a slice)* of $\mathcal{U}$.

### Hypersurfaces

If for each $p \in S$ there is a smooth chart $(\mathcal{U}, \varphi), \; \in \mathcal{U}$, such that $\mathcal{U}\cap S$ is an $m-$slice of $\mathcal U$, then $S$ is an *embedded submanifold* of dimension $m$ (and so of *co-dimension* $m-n$). A co-dimension 1 submanifold is called a *hypersurface*.

# Inverse Function Theorem

## Inverse Function Theorem in $\mathbb{R}^{n}$

Let $\mathcal{O}\subset \mathbb{R}^{n}$ be open and let $x^{i}$ be coordinates on $\mathcal{O}$. If at $x_{0}\in \mathcal{O}$ the Jacobian determinant

$$
\det \eval{\dv{f^{i}}{x^{j}}}_{x_0} \neq 0,
$$

then there is a neighborhood $x_{0}\in U \subset \mathcal{O}$ such that $V = f (U)\subset \mathbb{R}^{n}$ is a neighborhood of $f (x_{0})$ and $f$ has a smooth inverse of $V$

## Inverse Function Theorem in M

Let $M$ and $N$ be smooth manifolds. Let $f:M \rightarrow N$ be a smooth mapping. If $f_{*}:T_{p}M \rightarrow T_{f (p)}N$ is an isomorphism at $p \in M$, then there is a neighborhood $U$ around $p$ such that $V = f (U)$ is a neighborhood around $f (p)$ and $\eval{f (p)}_{U}:U \rightarrow V$ is a diffeomorphism

#### Corollary

Let $f:M \rightarrow N$ with $\dim M = m < n = \dim N$ be a smooth mapping such that $f_{*}:TM \rightarrow TN$ is non-degenerate at $p$. Then there exist coordinates $(U, u^{i})$ around $p\in M$ and $(V, v^{i})$ around $f (p)\in N$ with $f (U)\subset V$ such that 

$$
\begin{align}
\begin{cases}
v^{i}(f (x))& = u^{i}(x)\qc 1 \leq i \leq m \\[1 em]
v^{\gamma}(f (x))&  = 0 \qc m + 1 \leq \gamma \leq n
\end{cases}\qc 
x \in \mathbb{U}.
\end{align}
$$

In other words the image of $M$ under $f$ can be regarded as the solution to the system of $n-m$ equations $v^{m + 1}= \cdots = v^{n}$ in $N$, and the coordinates $x^{1}\cdots x^{m}$ on $M$ become the coordinates in this image.