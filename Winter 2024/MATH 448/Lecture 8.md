Let $f:M \rightarrow N$, with $\dim M = m < n = \dim N$ be a smooth mapping such that $f_{*}:TM \rightarrow TN$ is non-degenerate at $p$. Then there exists coordinates $(U, u^{i})$ near $p \in M$ and $(V, v^{i})$ near $f (p)\in N$ such that

$$
\begin{align}
v^{i}(f (x)) & = u^{i}(x)\qc 1 \leq i \leq m \\[1 em]
u^{r}(f (x)) & = 0 \qc m + 1 \leq r \leq n.
\end{align}
$$

Define 

$$
\begin{align}
\tilde{f}^{a}(u^{1}, ..., u^{m}, w^{m + 1}, ..., w^{n}) =
\begin{cases}
f^{i}(u^{1}, ..., u^{m}) \qc 1 \leq i \leq m \\[1 em]
w^{r} + f^{r}(u^{1}, ..., u^{m}) \qc m + 1 \leq r \leq n
\end{cases}.
\end{align}
$$

This implies $\tilde{f}^{a}$ is non-degenerate, and so $\tilde{f}^{a}_{*}$ is also non-degenerate.

By the inverse function theorem, $M$ is then smoothly embedded in $N$ and in fact we get local coordinates $(V, v^{a})= (f (U), (u^{i}, w^{i}))$. A smooth embedding implies non-degenerate $f$ and a homeomorphism onto its image.

# Tangent Space for an Embedded (Sub-)Manifold

Say the inclusion $i:S \hookrightarrow M$ is a smooth embedding. Consider the pushforward $i_{*}:T_{p}S \rightarrow T_{i (p)M}$. We can identify $T_{p}S$ with its image in $T_{i (p)}M$ under $i_{*}$.

#### Lemma

Say $S \hookrightarrow M$ is an embedded submanifold and $p \in S$. $T_{p}S$ is defined as a subspace of $T_{p}M$ by

$$
T_{p}S = \set{X \in T_{p}M\mid Xf = 0 \;\text{if}\; \eval{f}_{s}= 0, \; f \in C^{\infty}(M)}.
$$

If $X \in T_{p}S$ and if $\eval{f}_{s = 0}$, then $Xf = 0$. Proof: Let $\tilde{X}= i_{*}X$, $x \in T_{p}S$, so $\tilde{X}\in T_{i (p)M}$. If $f \in C^{\infty}(M)$ vanishes on $i (S)$, then $f \circ i = 0$. Then $\tilde{X}f = (i_{*}X)(f)= X (f \circ i) = X (0)= 0$.

If $\tilde{X}f = 0\; \forall \; \eval{f}_{S}= 0$, then $\tilde{X}_{i (p)}\in T_{p}S \subset T_{i (p)}M$. Proof: Choose coordinates $(x^{1}, ..., x^{n})$ on $U \subset M$ such that $S$ is defined by $x^{m + 1}= \cdots = x^{m}= 0$. Then $(x^{1}, ..., x^{m})$ are coordinates on S. Write

$$
X = X^{i}\pdv{x^{i}}.
$$

Let $X$ act on $f^{j?Ing = x^{j}\varphi (x)}$, where $\varphi (x)= 1$ near $p \in U$ and $0$ outside $U$:

$$
\begin{align}
X (x^{j}\varphi) & = X (x^{j})\varphi + X (\varphi)x^{j} \\[1 em]
& = X^{i}\pdv{x^{j}}{x^{i}}\varphi + xX^{j}(\varphi) \\[1 em]
\eval{X (x^{j})}_{p} & = X^{i}\delta_{i}^{j} = X^{j}.
\end{align}
$$

We assume $Xf= 0$ wherever $\eval{f}_{S}= 0$, which implies

$$
\begin{align}
X^{j}& = 0 \qc \text{for} \; m + 1 \leq j \leq n \\[1 em]
X & = X^{i}\pdv{x^{i}} \in T_{p}S \subset{T_{i(p)}M}
\end{align}
$$