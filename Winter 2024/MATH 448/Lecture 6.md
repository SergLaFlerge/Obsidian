Recall the pushforward:

$$
\eval{\left(\psi_{*}\pdv{x^{i}} \right)}_{\psi (p)} = \pdv{\tilde{x}^{a}}{x^{i}}\pdv{\tilde{x}^{a}}.
$$

For two manifolds $M$ and $N$, a vector field $X\in M$, a one-form $\tilde{\omega}\in N$, and a diffeomorphism $\psi:M \rightarrow N$, a pushforward $\psi_{*}$ on $X$will bring $X$ to $N$ as $\psi_{*}X$. A pullback $\psi^{*}$ on $\tilde{\omega}$ will bring $\tilde{\omega}$ to $M$ as $\psi_{*}\omega$. This is easily seen in an image, which I will hopefully add at some point. We also have

$$
\begin{align}
X & = X^{a}\dd{a} \\[1 em]
\psi_{*}X & = \tilde{X}= \tilde{X}^{a}\partial_{a}^{2} \\[1 em]
\tilde{X}_{a} & = X^{i}\pdv{\tilde{x}^{a}}{x^{i}} \\[1 em]
\omega_{i} & = \tilde{\omega}_{a}\pdv{\tilde{x}^{a}}{x^{i}}.
\end{align}
$$

Pushforwards are represented in a basis by Jacobian matrices, and are sometimes called *differentials*.

If $\psi_{*}$ is sewer surjective, i.e. $\dim M \geq \dim N$, and every vector in $T_{\psi (p)}N$ is the image of some vector in $T_{p}M$, the mapping is called a *submersion*.

### Lemma

Let $\psi:M \rightarrow N$ be a diffeomorphism. Let $f \in C^{\infty}(M)$ and $\omega \in T^{*}M$. Then

$$
\begin{align}
\psi^{*}\dd{f} & = \dd{(f \circ \psi)} \\[1 em]
\psi^{*}(f \omega) & = (f \circ \psi)\psi^{*}\omega.
\end{align}
$$

#### Corollary

Let $\tilde{x}^{a}$ be coordinates near $\psi (p)$. Then

$$
\begin{align}
\psi^{*}\omega & = \psi^{*}(\omega_{a}\dd{\tilde{x}^{a}}) \\[1 em]
& = (\omega_{a}\circ \psi)\psi^{*}\dd{\tilde{x}^{a}} \\[1 em]
& = (\omega_{a}\circ \psi)\dd{(\tilde{x}^{a}\circ \psi)}.
\end{align}
$$

Proof: Let $p \in M$, $X \in TM$, $\dd{f}\in T^{*}M$. Then

$$
\begin{align}
\ev{\psi^{*}\dd{f}, \omega}_{p} & = \ev{\dd{f}, \psi_{*}X}_{\psi (p)}\qc \text{definition of $\psi^{*}\dd{f}$}\\[1 em]
& = (\psi_{*}X)(f) \qc \text{definition of $\dd{f}$} \\[1 em]
& = X (\psi^{*}f) \qc \text{definition of $\psi_{*}$}\\[1 em]
& = X (f \circ \psi)\\[1 em]
& = \ev{\dd{(f \circ \psi)}, X}_{p}\; \forall \; X\\[1 em]
\implies \psi^{*}\dd{f} & = \dd{(f \circ \psi)}.
\end{align}
$$

That proves the first statement. The second is trivial:

$$
\begin{align}
\psi^{*}(f \omega) & = (\psi^{*}f)\psi^{*}\omega \\[1 em]
& = (f \circ \psi)\psi^{*}\omega,
\end{align}
$$

which concludes the proof.

>[!examples]+  Example 
>Take $\psi:\mathbb{R}^{3}\rightarrow \mathbb{R}^{2}:(x, y, z)\mapsto (u, v)= (xy, yz)$. Let $\omega = v^{2}\dd{u}+ u^{3}\dd{v}$. Compute $\psi^{*}\omega \in T^{*}\mathbb{R}^{3}$.
>
> $$
\begin{align}
\psi^{*}\omega & = (\omega_{a}\circ \psi)\dd{(\tilde{x}^{a}\circ \psi)}\qc \text{from the corollary} \\[1 em]
\omega_{u}\circ \psi & = v^{2}(x, y, z) = (yz)^{2} \\[1 em]
\omega_{v}\circ \psi & = u^{3}(x, y, z) = (xx)^{3} \\[1 em]
\dd{u} & = \dd{(xy) = y \dd{x}} + x \dd{y} \\[1 em]
\dd{v} & = \dd{(yz) = z \dd{y}} + y \dd{z} \\[1 em]
\implies \psi^{*}\omega & = (yz)^{2}(y \dd{x}+ x \dd{y}) + (xy)^{3}(z \dd{y}+ y \dd{z}) \\[1 em]
& = (yz)^{3}\dd{x} + (x(yz)^{2}+ (xy)^{3}z)\dd{y} + x^{3}y^{4}\dd{z}.
\end{align}
>$$
>
>next,
>
>$$
\begin{align}
\ev{\partial_{x},  \;\psi^{*}\dd{u}} & = \ev{\psi_{*}\partial_{x}, \; \dd{u}} \\[1 em]
& = \ev{\partial_{x}, \; y \dd{x}+ x \dd{y}} \\[1 em]
\implies y & = \ev{\psi_{*}\partial_{x}, \; \dd{u}}.
\end{align}
>$$
>
>Also,
>
>$$
\begin{align}
\ev{\partial_{x}, \; \psi^{*}\dd{v}} & = \ev{\psi_{*}\partial_{x}, \; \dd{v}} \\[1 em]
& = \ev{\partial_{x}, \; z \dd{y}+ y \dd{z}} \\[1 em]
& = 0.
\end{align}
>$$
>
>$\psi_{*}\partial_{x}$ has $u$-component $y$ and $v$-component $0$. Therefore $\psi_{*}\partial_{x}= y \partial_{u}$. If we do the same for $\partial_{y}$ and $\partial_{z}$, we end up with a matrix:
>
>$$
\psi_{*}=
\begin{bmatrix}
y & x & 0 \\
0 & z & y
\end{bmatrix},
>$$
>
>which has rank 2, except for when $y = 0$. Therefore $\psi$ is a submersion for $y \neq 0$.