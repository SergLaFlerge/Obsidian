 Say we have a differentiable structure $M$, with $U \subset M$, and a map $\varphi_{U}: U \mapsto \mathcal{O}\subset \mathbb{R}^{n}$, where both $M$ and $\mathcal{O}$ are coordinate neighborhoods. Then $M$ is a topological manifold, with $(\varphi_{U_{a}},U_{a})$, where the collection of $U_{a}$ open sets covers $M$. The $\varphi_{U_{a}}$ are invertible (and so are homeomorphisms), $M$ is Hausdorff, and $M$ is second-countable.

## Transition Mappings

Let $\mathcal{O}_{1}$, $\mathcal{O}_{2}$ be open in $\mathbb{R}^{n}$, and $U_{1}, \; U_{2}$ be open in $M$, with $U_{1}\cup U_{2}$ non-empty. The compositions $\varphi_{2}\circ \varphi_{1}^{-1}$ are called *transition mappings*, with $\varphi$ a map from $M$ to some copy of $\mathbb{R}^{n}$.

Define

$$
\begin{align}
x^{i} & = \varphi_{1}(p) \\
y^{i} & = \varphi_{2}(p),
\end{align}
$$

with $p \in U_{i}$. Then,

$$
y^{i} = (\varphi_{2}\circ \varphi_{1}^{-1})(x)
$$

is a transition mapping. Transition mappings induce coordinate transformations. We can take coordinate neighborhoods in $M$, bring them to a copy of $\mathbb{R}^{n}$, do stuff on it, and move it to another copy of $\mathbb{R}^{n}$ through a coordinate transformation.

## Differentiable, Smooth, and Analytic Manifolds

Two charts $(U_{1}, \varphi_{1})$ and $(U_{2}, \varphi_{2})$ are said to be $C^{k}$-compatible (respectively $C^{\infty}$ and $C^{\omega}$-compatible) if the transition mapping $\varphi_{2}\circ \varphi_{1}^{-1}$ and its inverse is also $C^{k}$ (respectively $C^{\infty}$ and $C^{\omega}$.)

A $C^{k}$ differentiable structure on $M$ is a collection of charts $A = \{(\varphi_{U}, U), (\varphi_{V}, V), ... \}$ such that
1. $A$ covers $M$.
2. Any two charts in $A$ are $C^{k}$-compatible.
3. $A$ is maximal (any $C^{k}$-compatible chart is in $A$)(compatible may also be called admissible.)

$C^{\infty}, \; C^{\omega}$ are defined similarly. Unless otherwise sated, we will be working with smooth manifolds during the course.

### Simple Examples

- $M = \mathbb{R}^{n}$. Then $(M, \text{Id})$ is a covering of $M$ by $\mathbb{R}^{n}$. This single-chart cover atlas is called the standard differentiable structure of $\mathbb{R}^{n}$.
- Graphs of continuous functions $$f:U \mapsto \mathbb{R}\qc U \subset \mathbb{R}^{n}$$
	- The graph $\Gamma (f):= \set{(x, y)\in \mathbb{R}^{n}\times \mathbb{R}\mid x \in U, \; q = f (x)}$.
- $\pi:\mathbb{R}^{n}\times \mathbb{R}\mapsto \mathbb{R}^{n}:(x, y)\mapsto x$ is continuous so its restriction to $\Gamma (f)$ is also continuous. Then $\varphi^{-1}:x \mapsto (x, f (x))$ is continuous since $f$ is also continuous, and so $\varphi$ is a homeomorphism, and $(U,{\varphi})$ is a single-chart atlas.
- n-spheres $\mathbb{S}^{n}= \set{(x^{1}, x^{2}, ..., x^{n + 1})\in\mathbb{R}^{n + 1}\mid(x^{1})^{2}+ (x^{2})^{2}+ \cdots + (x^{n + 1})^{2}= 1}$. For $i \in [1, n + 1]\subset \mathbb{N}$, the subset  of $\mathbb{S}^{n}$ with $x^{i}> 0$ is an open hemisphere in $\mathbb{S}^{n}$. These open hemispheres cover $\mathbb{S}^{n}$ and so are homeomorphic to $\mathbb{R}^{n}$.
- Take two smooth manifolds $M$ and $N$, possibly of different dimensions. Take a mapping $f:M \mapsto N$. If $f$ is a homeomorphism, then $M$ and $N$ are homeomorphic. Let $(U, \varphi_{U})$ be a chart in $U$ with $p \in U$, and let $(V, \psi_{V})$ be a chart in $V$ with $f (p)\in V$. Define $$F:= \psi_{V}\circ f \circ \varphi_{U}:\varphi_{U}(U)\mapsto \psi_{V}(V).$$ If $F$ is smooth at  $\varphi_{U}(p)$, then we say that $f$ is smooth at $p$. $f$ maps $M$ to $N$ while $F$ takes the image of $M$ in a copy of $\mathbb{R}^{N}$ to another copy of $\mathbb{R}^{n}$ that is the image of $N$.

A smooth homeomorphism with a smooth inverse is called a *diffeomorphism*, and $M$ and $N$ are said to be *diffeomorphic*.

Homeomorphisms define an equivalence class of manifolds. If $N$ and $L$ are homeomorphic and $M$ and $N$ are homeomorphic, then $M$ and $L$ are also homeomorphic. This also applies to diffeomorphisms.