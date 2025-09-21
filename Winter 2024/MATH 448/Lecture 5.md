# Cotangent Spaces

Fix a basis for $T_{p}M$. Define $E^{i}:T_{p}M \rightarrow \mathbb{R}\qc X \mapsto X^{i}$. Then $\set{E^{i}}$ is linearly independent. We then define $T_{p}^{*}M$ as the span of $\set{E^{i}}$. $T_{p}^{*}M$ is the cotangent space at $p \in M$. Elements of $T_{p}^{*}M$ are called *cotangent vectors* or *1-forms*. It follows then that

$$
T^{*}M:= \bigcup_{p \in M}T_{p}^{*}M.
$$

## Duality

Given $\set{e_{i}}$, fix $\set{E^{i}}$ as above. Then

$$
\begin{align}
E^{i}e_{j} & = \delta_{j}^{i} \\[1 em]
\abs{\set{E^{i}}} & = n
\end{align}
$$

is called the *dual basis* to $\set{e_{j}}$. This gives a non-canonical (basis dependent) isomorphism between $T_{p}M$ and $T_{p}^{*}M$.

Define a pairing of individual vectors and covectors:

$$
\begin{align}
\ev{\omega, X} & = \ev{X, \omega}  = X^{i}\omega_{j}\ev{e_{i}, E^{j}}  = X^{i}\omega_{j}\delta_{i}^{j} \\[1 em]
& = X^{i}\omega_{j} = X\lrcorner \omega = i_{X}\omega,
\end{align}
$$

where the $i$ stands for the interior product. We denote by $\set{\dd{x^{i}}}$ the dual basis in $T_{p}^{*}M$ to coordinate basis $\set{\pdv{x^{i}}}$ for $T_{p}M$, such that

$$
\ev{\pdv{x^{i}}, \dd{x^{j}}} = \delta_{i}^{j}.
$$

# Exterior Derivative of a Function

Given $F:M \rightarrow \mathbb{R}$, define the linear mapping $\dd{f}:M \rightarrow \mathbb{R}$ by

$$
\begin{align}
\ev{\dd{f}, X} & = X (f)\qc X \in T_{p}M \\[1 em]
& = X^{i}\pdv{f}{x^{i}} \\[1 em]
& = X^{i}\partial_{i}f.
\end{align}
$$

$X^{i}\partial_{i}f$ is the "row vector" ($1 \times n$ matrix) representing $\dd{f}$, with entries $\pdv{f}{x^{i}}$:

$$
\begin{align}
\ev{\dd{f}, X} & = X^{i}\partial_{i}f \\[1 em]
& =
\begin{bmatrix}
\partial_{1}f & \partial_{2}f &  \cdots
\end{bmatrix} 
\cdot 
\begin{bmatrix}
X^{1} \\
X^{2} \\
\vdots
\end{bmatrix}.
\end{align}
$$

If $\omega \in T_{p}M$ is the differential of $\dd{f}$, then $\omega$ is called an *exact 1-form*,

$$
\omega = \dd{f}.
$$

This holds since the map $\dd{f}$ is linear, so $\dd{f}\in T_{p}^{*}M$.

# Pullbacks and Pushforwards

Say we have a diffeomorphism $\psi:M \rightarrow N$, where $\dim{M}$ need not equal $\dim{N}$. Let $l:N \rightarrow \mathbb{R}$ be a smooth function. We can then define a smooth function

$$
\psi^{*}f:M \rightarrow \mathbb{R},
$$

called the *pullback* of $f$ by $\psi$, by

$$
(\psi^{*}f)(p) = f (\psi (p)) = (f \circ \psi)(p)
$$

for $p \in M$. Next, let $X \in T_{p}M about$. We define a vector field  $\psi_{*}X \in T_{\psi (p)}N$, called the *pushforward* of $X$ by

$$
\eval{(\psi_{*}X)(f)}_{\psi (p)} = X (\psi^{*}f)(p).
$$

Finally, if $\omega \in T_{\psi (p)^{*}}N$, we define $\psi^{*}\omega \in T_{p}^{*}M$ to be the pullback of $\omega$ by

$$
\ev{X, \psi^{*}\omega}_{p} = \ev{\psi^{*}\omega, X}_{\psi (p)}.
$$

Pullbacks of vector fields are pushforwards by $\psi^{-1}$. Pushforwards are also called tangent maps.

## Pushforwards in Euclidean Space

Let $\phi:\mathbb{R}^{m}\rightarrow \mathbb{R}^{n}:p \mapsto \psi (p)$ be a diffeomorphism, and let $f:\mathbb{R}^{n}\rightarrow \mathbb{R}$. The coordinates in $\mathbb{R}^{m}$ are $x^{i}$ and the ones in $\mathbb{R}^{n}$ are $\tilde{x}^{i}= \psi^{i}(X)$.

$$
\begin{align}
\eval{\left(\psi_{*}\pdv{x^{i}} \right)}_{\psi (p)} & = \pdv{x^{i}}(\psi^{*}f) \\[1 em]
& = \eval{\pdv{x^{i}}(f \circ \psi)}_{p} \\[1 em]
& = \pdv{f}{\tilde{x}^{a}}\pdv{\psi^{a}}{x^{i}} \\[1 em]
\eval{\left(\psi^{*}\pdv{x^{i}} \right)}_{\psi (p)} & = \pdv{\psi^{a}}{x^{i}}\pdv{\tilde{x^{a}}} \\[1 em]
& = \pdv{\tilde{x}^{a}}{x^{i}}\pdv{\tilde{x}^{a}}.
\end{align}
$$

The matrix representing the linear mapping $\psi_{*}$ is just the Jacobian of $\psi$:

$$
\pdv{\psi^{a}}{x^{i}}.
$$

Example: Let $\psi:\mathbb{R}\rightarrow (0, \infty):x \mapsto \tilde{x}= e^{x}$. Then

$$
\pdv{\psi}{x} = e^{x}= \tilde{x},
$$

and so

$$
\psi_{*} \pdv{x} = \tilde{x}\pdv{\tilde{x}}.
$$

## Pushforwards Between Manifolds (in coordinates)

The calculation from above still applies to $\hat{\psi}= \tilde{\phi}\circ \psi \circ \phi^{-1}$:

$$
\begin{align}
\eval{\left( \psi_{*}\pdv{x^{i}} \right)}_{\psi (p)} & = \psi_{*}\left((\psi^{-1})_{*}\pdv{x^{i}} \right) \\[1 em]
& = (\tilde{\phi}^{-1})_{*}\left(\hat{\psi}_{*}\pdv{x^{i}} \right), \; \text{using $\phi^{-1}\circ \hat{\psi}= \tilde{\phi}\circ \psi $}\\[1 em]
& = (\tilde{\phi}^{-1})_{*}\eval{\left(\pdv{\psi^{a}}{x^{i}}\pdv{\tilde{x}^{a}} \right)}_{\psi (p)}\\[1 em]
& = \pdv{\hat{\psi}^{a}}{x^{i}}\eval{\pdv{\tilde{x}^{a}}}_{\psi (p)}
\end{align}
$$