# Smooth Vector Fields

For $X, Y, Z$ vector fields examine $f, g \in C^{\infty}M$, we have
- $\comm{X}{Y} = -\comm{Y}{X}$.
- $\comm{X + Y}{Z}= \comm{X}{Z}+ \comm{Y}{Z}$.
- $\comm{fX}{gY}= f(Xg)Y-g(Yf)X + fg \comm{X}{Y}$.
-  $\comm{X}{\comm{Y}{Z}}+ \comm{Y}{\comm{Z}{X}}+ \comm{Z}{\comm{X}{Y}}= 0$.

If $X = 0$ the some isolated point $p \in M$, then $p$ is called a singular point of the smooth vector field $X$.

#### Lemma

A tangent vector field on a smooth $m-$manifold is smooth if and only if for any $p \in M$ there are local coordinates $(U, u^{i})$ such that

$$
\eval{X}_{U}= \xi^{i} \pdv{x^{i}},
$$

where $\xi^{i}$ are smooth functions on $U$.

#### Flow Box Lemma

If $X$ is a smooth tangent vector field on $M$ and $p$ is not a singular point of $X$, then there are coordinates $(W, w^{i})$ such that

$$
X = \pdv{x^{1}}.
$$

No proof for now.

## Smooth Distribution

Say there is a neighborhood $p \in U \subset M$ and smooth vector fields $X_{1}, ..., X_{h}$ forming a linearly independent set at each $q \in U$. Then

$$
\mathcal{L}^{h} := \text{span}\set{X_{1}, ..., X_{h}}
$$

is an $h-$dimensional distribution on $U \subset M$.

Is there a local coordinate system $(U, u^{i})$ such that

$$
\mathcal{L}^{h}(q) = \text{span}\left\{\pdv{u^{1}}, \cdots, \pdv{u^{h}}\right\}?
$$

If so, then 

$$
X_{(\alpha)} = a_{\alpha}^{\beta}\pdv{u^{\beta}}
$$

where the coefficients are smooth functions on $U$ with $\det[a_{\alpha}^{\beta}]\neq 0$. A consequence of this is that $\comm{X_{(\alpha)}}{X_{(\beta)}}\in \mathcal{L}^{h}(q)$.

## The Frobenius Condition

If $\mathcal{L}^{h}= \text{span}\set{X_{1}, ..., X_{h}}$ *and* $\comm{X_{(\alpha)}}{X_{(\beta)}}\in \mathcal{L}^{h}$, then $\mathcal{L}^{h}$ satisfies the Frobenius condition.

## Frobenius Theorem

Suppose $\mathcal{L}^{h}= \text{span}\set{X_{1},..., X_{h}}$ is an $h-$dimensional distribution in an open set $U$. Then $\exists$ a local coordinate system $(U, u^{i})$ such that

$$
\text{span}\left\{\pdv{u^{1}}, \cdots \pdv{u^{h}} \right\}
$$

*if and only if* $\mathcal{L}^{h}$ satisfies the Frobenius condition.