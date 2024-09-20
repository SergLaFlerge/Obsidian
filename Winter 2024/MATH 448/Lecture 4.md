# Tangent Vectors to a Curve

Till now, tangent vectors $X \in T_{p}M$ and derivations

### Definition

Let $f \in C^{\infty}M$ and a differentiable curve in $\mathbb{R}^{n}$ $x:(-\epsilon, \epsilon)\rightarrow \mathbb{R}$. $\gamma (t)= \phi^{-1}\circ x (t)$ is a curve on $M$.

If $Xf:= \eval{\dv{t}f (\gamma (t))}_{t = 0}$, with $\gamma (0)= p$, then $X:C^{\infty}M\rightarrow \mathbb{R}$ is a tangent vector to a curve $\gamma$. Since $X$ is linear and a derivation, we know $X \in T_{p}M$.

Why are elements (in general) of $T_{p}M$ called tangent vectors? We know that tangents to curves live in $T_{p}M$. I.e.

$$
Xf:= \eval{\dv{t}f (\gamma (t))}_{t = 0}
$$

By the chain rule, we have

$$
\begin{align}
Xf & = \dv{t}f (\gamma (t)) = \eval{\dv{x^{i}}{t}}_{t = 0}\pdv{x^i}(f \circ \phi^{-1}) \\[1 em]
& = \eval{\dv{x^{i}}{t}}_{t = 0}\partial_{i}f \\[1 em]
X & = X^{i}\partial_{i} =  \eval{\dv{x^{i}}{t}}_{t = 0}\partial_{i}.
\end{align}
$$

Every $X \in T_{p}M$ is tangent to some curve:

$$
\gamma (t) = \phi^{-1}x (t)\qc x^{i}(t) = x_{0}^{i}+ tX^{i},
$$

Therefore

$$
\dv{x^{i}}{t} = X^{i}
$$

So any $X = X^{i}\partial_{i}$ is a tangent vector to $\phi^{-1}(x)$, $x^{i}+ tX^{i}$

# Vector Fields

For smooth vector fields $X, Y$ and any smooth $f$, we define the Lie bracket by

$$
\begin{align}
\comm{X}{Y}f & := X (Yf)-Y (Xf) \\[1 em]
& = \left(X^{i}\pdv{Y^{j}}{x^{i}}+ Y^{i}\pdv{X^{j}}{x^{i}} \right)\dv{f}{x^{j}} \\[1 em]
\implies \comm{X}{Y} & \in T_{p}M.
\end{align}
$$

For smooth vector fields $X, Y, Z$ on $M$, and $a, b \in \mathbb{R}$, we have several properties:
- Bilinearity: $\comm{aX + bY}{Z}= a \comm{X}{Z}+ b \comm{Y}{Z}$.
- $\comm{X}{Y}$ is smooth vector field.
- $\comm{X}{Y}=-\comm{Y}{X}$.
- Coordinate vector fields commute, i.e. $\comm{\partial_{i}}{\partial_{j}}= 0$.
- Jacobi's identity holds: $\comm{\comm{X}{Y}}{Z}+ \comm{\comm{Y}{Z}}{X}+ \comm{\comm{Z}{X}}{Y}= 0$.
- Vector fields form a *Lie Algebra*.

## Cotangent Spaces

Let $\set{e_{i}}$ be a basis for $T_{p}M$, so

$$
X \in T_{p}M \implies X = X^{i}e_{i}.
$$

(Remark: A basis for $TM$ need not commute:$\comm{e_{i}}{e_{j}}\neq 0$. This is called an anholonomic basis.)(coordinate vectors commute, so they are holonomic)

Define a linear mapping

$$
E^{i}:T_{p}M \rightarrow \mathbb{R}
$$

by

$$
E^{i}(X)= X^{i}\rightarrow \text{i-th component with respect to $\set{e_{i}}$ for $T_{p}M$}.
$$

Then $\set{E^{i}}$ is a linearly opponent set.

Proof: Say $0 = a_{i}E^{i}$. If we act on the basis $\set{e_{j}}$, we have

$$
\begin{align}
0 & = a_{i}E^{i}(e_{j})  \\[1 em]
& = a_{i}\delta_{j}^{i} \\[1 em]
& = a_{j} \\[1 em]
\implies a_{i}E^{j}& = 0.
\end{align}
$$

We define $T_{p}^{*}M:= \text{span}\set{E^{i}}$ as the dual or cotangent space. Elements are called co-vectors or 1-forms.