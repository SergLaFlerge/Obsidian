Last time, we had

$$
\begin{align}
\ev{\cdot, \cdot}:V \times V^{*} & \rightarrow \mathbb{F} \\[1 em]
\ev{v, v^{*}} & = v^{*}(v)\qc v \in V, \; v^{*} \in V^{*}.
\end{align}
$$

This is in fact the interior product, which is linear in both arguments.

Suppose $\phi:V^{*}\rightarrow \mathbb{F}$ is an arbitrary linear function. Define $v_{i} = \phi (E^{i})e_{i}$, where $\set{e_{i}}$ is a basis for $V$ and $\set{E^{i}}$ is the dual basis for $V^{*}$ such that $\ev{e_{i}, E^{j}}= \delta_{i}^{j}$. Let $v^{*}\in V^{*}$ be arbitrary. Then

$$
\begin{align}
\ev{v, v^{*}} & = \ev{\phi (E^{i})e_{i},v_{j}^{*}E^{j}} \\[1 em]
& = \phi (E^{i})v_{j}^{*}\ev{e_{i}, E^{j}} \\[1 em]
& = \phi (E^{i})v_{j}^{*}\delta^{j}_{i} \\[1 em]
& = \phi (E^{i})v_{i}^{*} \\[1 em]
& = \phi (v^{*}) \implies \ev{v, \cdot} = \phi (\cdot),
\end{align}
$$

i.e. each $v \in V$ defines an $\mathbb{F}-$linear map.

$$
\ev{v, \cdot} = \phi (\cdot):V^{*}\rightarrow \mathbb{F}\quad \text{linearly},
$$

hence $V$ is a dual space to $V^{*}$.

# Covariant Tensors

A map is $r-$linear if it is linear in each of its $r$ arguments.

Let $\mathrm{L}(V_{1}, ..., V_{r}; \mathbb{F})$ denote the set $V_{1}\times \cdots \times V_{r}\rightarrow \mathbb{F}$ of $r-$linear maps. Define $(f + g)(v_{1}, \cdots, v_{r})= f (\cdots)+ g (\cdots)$, and $(\alpha f)(\cdots)= \alpha (f (\cdots))$ for $\alpha \in \mathbb{F}$.

Then $\mathrm{L}(V_{1}, \cdots, V_{r}:\mathbb{F})$ is a vector space over $\mathbb{F}$.

Let us restrict this to the case $V_{1}= \cdots = V_{r}= V$. The elements of $\mathrm{L}(V \underbrace{\cdots}_{r \; \text{times}}V:\mathbb{F})$ are called *covariant $r-$tensors*.

Symmetric covariant $2-$tensors are called bilinear forms.

# Tensor Product

For $\omega, \eta \in V^{*}$, define a map $\omega \otimes \eta:V \times V \rightarrow \mathbb{F}$ by

$$
(\omega \otimes \eta)(X, Y) = \omega (X)\eta (Y).
$$

$\omega \otimes \eta$ is a covariant 2-tensor, called the tensor product of $\omega$ with $\eta$.

Let $\Omega$ be a covariant $k-$tensor and $\Psi$ a covariant $r-$tensor, with $k < r$. Then

$$
\begin{align}
(\Omega \otimes \Psi)(X_{1}, ..., X_{k}, X_{k + 1}, ..., X_{k + r}) = \Omega (X_{1}, ..., X_{k}) \Psi (X_{k + 1}, ..., X_{r}).
\end{align}
$$

So $\Omega \otimes \Psi$ is a covariant $(k + r)-$tensor, called the tensor product of $\Omega$ with $\Psi$. The tensor product is
- Bilinear: $(\alpha_{1}\Omega_{1}+ \alpha_{2}\Omega_{2})\otimes \eta = \alpha_{1}\Omega_{1}\otimes \eta + \alpha_{2}\Omega_{2}\otimes \eta$, $\Omega \otimes (\alpha_{1}\eta_{1}+ \alpha_{2}\eta_{2})= \alpha_{1}\Omega \otimes \eta_{1}+ \alpha_{2}\Omega \otimes \eta_{2}$.
- Associative: $\Omega \otimes (\Psi \otimes \Phi)= (\Omega \otimes \Psi)\otimes \Phi = \Omega \otimes \Psi \otimes \Phi$,

Therefore the space $V^{*}\otimes W^{*}$ is the space of $\mathbb{F}-$linear comb nations of elements of the form $v^{*}\otimes w^{*}$, with $v^{*}\in V^{*}$ and $w^{*}\in W^{*}$.

An element that precisely has the form $v^{*}\otimes w^{*}$ is called *reducible*.

Choose bases $\set{E^{i}}$ for $V^{*}$ and $\set{F^{i}}$ for $W^{*}$. Then

$$
v^{*}\otimes w^{*} = v_{i}^{*}w_{j}^{*}E^{i}\otimes F^{j}.
$$

Any reducible element of $V^{*}\otimes W^{*}$ is a linear combination of $E^{i}\otimes F^{j}$, but *any* element of $V^{*}\otimes W^{*}$ is a linear combination of reducible elements. Hence *any* elements of $V^{*}\otimes W^{*}$ is a linear combination of the product $E^{i}\otimes F^{j}$, which implies $\set{E^{i}\otimes F^{j}}$ spans $V^{*}\otimes W^{*}$. Therefore $\set{E^{i}\otimes F^{j}}$ is a basis for $V^{*}\otimes W^{*}$. Showing linear independence is easy. Finally, $\dim (V^{*}\otimes W^{*})= \dim V{*}\cdot \dim W^{*}$.

# Tensors

Let $V$ be an $n-$dimensional space over $\mathbb{F}$. Consider the tensor product space

$$
V_{s}^{r}:= V \otimes \; \text{$r$ times}\; \otimes V \otimes V^{*}\otimes \; \text{$s$ times}\; \otimes V^{*}.
$$

$V_{s}^{r}$ is a vector space of dimension $r + s$. Elements of this space are called tensors of type $(r, s)$, of order $(r, s)$, or simply $(r, s)-$tensors. $r$ represents the contravariant order and $s$ represents the covariant order.
- $V_{0}^{0}= \mathbb{F}$ are scalars.
- $V_{0}^{1}= V$ are vectors or contravariant vectors.
- $V_{1}^{0}= V^{*}$ are covectors, covariant vectors, or 1-forms.

If $\set{e_{i}}$ is a basis for $V$ and $\set{E^{j}}$ is a basis for $V^{*}$, then

$$
\set{e_{i_{1}}\otimes \cdots \otimes e_{i_{r}}\otimes E^{j_{1}}\otimes \cdots \otimes E^{j_{s}}}
$$

is a basis for $V_{s}^{r}$. In particular, for $T \in V_{s}^{r}$, we have

$$
T = T_{j_{1}, j_{2}, ...,j_{s}}^{i_{1}, i_{2}, ..., i_{r}}e_{i_{1}}\otimes \cdots e_{i_{r}}\otimes E^{j_{1}}\otimes \cdots \otimes E^{j_{s}}.
$$

We can define a duality if $s = r$. Let $v_{1}, ..., v_{r}\in V$ and $v^{*1}, ..., v^{*r}\in V^{*}$:

$$
\ev{v_{1}\otimes \cdots \otimes v_{s}, \; v^{*1}\otimes \cdots \otimes v^{*s}} = \ev{v_{s}, \; v^{*1}}\cdots \ev{v_{s}, \; v^{*s}}.
$$