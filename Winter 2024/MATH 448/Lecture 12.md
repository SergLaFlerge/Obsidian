#### Definition

Let $T$ be an $(r_{1}, s_{1})-$tensor and $Q$ an $(r_{2}, s_{2})-$tensor. Then

$$
\begin{align}
 &(T \otimes Q)(v^{*1}, \cdots, v^{*r_{1}+ r_{2}}, v_{1}, \cdots v_{s_{1}+ s_{2}}) = \\
&T (v^{*1}, \cdots v^{*r_{1}}, v_{1}, \cdots v_{s_{1}})\cdot Q (v^{*_{1}+ 1}, \cdots, v^{*r_{1}+ r_{2}}, v_{s_{1}+ 1}, \cdots, v_{s_{1}+ s_{2}}). 
\end{align}
$$

## Tensor Contraction

$T_{s}^{r}$ can be thought of as a matrix. Say $T$ is a reducible $(r, s)-$tensor,

$$
T = v_{1}\otimes \cdots \otimes v_{r}\otimes v^{*1}\otimes \cdots \otimes v^{*s},
$$

$v_{i}\in V$, $v^{*j}\in V^{*}$. The *contraction* $CT$ of $T$ on $i$ and $j$ is defined to be the $(r-1, s-1)-$tensor

$$
\ev{v_{i}, \; v^{*j}}\cdot v \otimes_{1}\otimes \cdots \otimes v_{i + 1}\otimes \cdots \otimes v_{r}\otimes v^{*1}\otimes \cdots \otimes v^{*j-1}\otimes v^{*j + 1}\otimes j^{*s}.
$$

If $T$ is an arbitrary $(r, s)-$tensor, then it can be written as a linear combination of reducible $(r, s)-$tensors, say

$$
T = \sum\limits_{\mu}c_{\mu}T_{\mu},
$$

for coefficients $c_{\mu}$ and some reducible tensor $T_{\mu}$. Then

$$
CT = \sum\limits_{\mu}c_{\mu}CT_{\mu}.
$$

For example, if $T^{i}_{j}$ is a $(1, 1)-$tensor, then

$$
CT = T^{i}_{i} = \trace \set{v \rightarrow T (v)}
$$

## Symmetric and Antisymmetric Tensors

A contravariant tensor $T$ is symmetric if it takes the same value when any two of its components are interchanged.

$T$ is antisymmetric (or skew, or alternating) if it picks up a minus sign when any two of its components are interchanged.

Same applies to covariant tensors.

Given an arbitrary $r-$contravariant tensor $T$, we define its symmeterization by

$$
ST (v_{1}^{*},\cdots, v_{r}^{*}) = \frac{1}{r!}\sum\limits_{\sigma \in S_{r}}T (\sigma (v_{1}^{*}, \cdots v_{r}^{*})),
$$

where $S_{r}$ is the group of permutations of $r$ elements. The antisymmeterization is defined similarly:

$$
AT (v_{1}^{*},\cdots, v_{r}^{*}) = \frac{1}{r!}\sum\limits_{\sigma \in S_{r}}\text{sgn}(\sigma)T (\sigma (v_{1}^{*}, \cdots, v_{r}^{*})),
$$

with $\text{sgn}(\sigma)= 1$ for even permutations and $\text{sgn}(\sigma)=-1$ for odd permutations.

>[! Examples]+ Example
>Let $T$ be an $(0, 2)-$tensor.
>
>$$
\begin{align}
T: V \times V & \rightarrow \mathbb{R} \\[1 em]
ST (u, v) & = \frac{1}{2}(T (u, v)+ T (v, u)) \\[1 em]
(ST)_{ij} & = \frac{1}{2}(T_{ij}+ T_{ji}) = T_{(ij)} \\[1 em]
AT (u, v) & = \frac{1}{2}(T (u, v)-T (v, u)) \\[1 em]
(AT)_{ij} & = \frac{1}{2}(T_{ij}-T_{ji}) = T_{[ij]}
\end{align}
>$$

## Wedge Product

The space of (totally) antisymmetric $r-$tensors is denoted by $\Lambda^{r}(V)$. If $\xi \in \Lambda^{r}(v)$, we say that $r$ is the degree of $\xi$.

$\Lambda^{r}(V)$ is a subspace of $T_{s}^{r}$.

A necessary and sufficient condition for an $r-$tensor to be in $\Lambda^{r}(V)$ is for its components in a basis to be antisymmetric under interchange of every two component indices.

Let $\xi\in \Lambda^{k}(V)$ and $\eta \in \Lambda^{r}(V)$. We define the *wedge product* (or *exterior product*) of $\xi$ with $\eta$ by

$$
\begin{align}
\xi \wedge \eta = A (\xi \otimes \eta) = \frac{1}{(k + r)!}\sum\limits_{\sigma \in S_{k + r}}\xi \otimes \eta (\sigma (\cdots))\text{sgn}(\sigma)\in \Lambda^{k + r}(V).
\end{align}
$$

>[! Examples]+ Example
>Let $\alpha, \beta, \gamma \in V^{*}$ and $u, v, w \in V$. Then
>
>$$
\begin{align}
\Omega & = \beta \wedge \gamma \\[1 em]
\Omega (u, v) & = \frac{1}{2}[\beta (u) \gamma (v)-\beta (v)\gamma (u)] \\[1 em]
(\alpha \wedge \Omega)(u, v, w) & = \alpha \wedge (\beta \wedge \gamma) = \frac{1}{6}(\cdots).
\end{align}
>$$

### Properties

Let $\xi_{1}, \xi_{2}, \xi \in \Lambda^{k}(V)$, $\eta_{1}, \eta_{2}, \eta \in \Lambda^{r}$, $\zeta \in \Lambda^{s}(V)$. Then
- $(\xi_{1}+ \xi_{2})\wedge \eta = \xi_{1}\wedge \eta + \xi_{2}\wedge \eta$.
- $\xi \wedge (\eta_{1}+ \eta_{2}) = \xi \wedge \eta_{1}+ \xi \wedge \eta_{2}$.
- $\xi \wedge \eta= (-1)^{kr}\eta \wedge \xi$.
- $(\xi \wedge \eta)\wedge{\zeta}= \xi \wedge (\eta \wedge \zeta)= \xi \wedge \eta \wedge \zeta$.

These likewise hold for $\Lambda^{*i}= \Lambda^{i}(V^{*})$.