#### Lemma 3.8

Let $\lambda$ be an eigenvalue of $\alpha$ and $\nu\neq \lambda$ another complex number. Then the $\mathbb{C}-$linear map

$$
\begin{align}
(\alpha-\nu \cdot \text{id}_{V})^{m}:\; K_{\lambda} & \rightarrow K_{\lambda}\\
v & \mapsto (\alpha-\nu \cdot \text{id}_{V})^{m}(v)
\end{align}
$$

Is an isomorphism for all integers $m \geq 0$.

**Proof:**

Since a $\mathbb{C}-$linear map of a finite dimensional $\mathbb{C}-$vector space into itself is an isomorphism if and only if it is one to one, so we only need to prove that, for any $v \neq 0 \in K_{\lambda}$, we have $(\alpha-\nu \cdot \text{id}_{V})^{m}(v)\neq$. Since $v \in K_{\lambda}$, there is some $d \geq 1$ such that $(\alpha-\lambda\cdot \text{id}_{V})^{d}(v)= 0$.

On the other hand, because $\lambda \neq \nu$, the polynomials $(T-\lambda)^{d}$ and $(T-\nu)^{m}$ have no common roots. By the Euclidean algorithm, there are polynomials $h (T)$ and $k (T)$ such that $1 = h (T)\cdot (T-\nu)^{m}+ k (T)\cdot (T-\lambda)^{b}$. We then have

$$
\begin{align}
v & = \text{id}_{V}(v)\\
& = [h (\alpha)\cdot (\alpha-\nu \cdot \text{id}_{V})^{m}+ k (\alpha)\cdot (\alpha-\lambda \cdot \text{id}_{V})^{d}](v)\\
& = h (\alpha)\left((\alpha-\nu\cdot \text{id}_{V})^{m}(v)\right) + k (A)\left((\alpha-\lambda \cdot \text{id}_{V})^{b}(v) \right)\\
& = h (\alpha)\left((\alpha-\nu \cdot \text{id}_{V})^{m}(v) \right).
\end{align}
$$

Therefore $(\alpha-\nu \cdot \text{id}_{V})^{m}(v)\neq v$ since $v \neq 0$.

We get the following corollary by induction:

#### Corollary

Let $\lambda$ be an eigenvalue of $\alpha$ and $\nu_{1}, ..., \nu_{r}$ be complex numbers all of which are not $\lambda$. Then the $\mathbb{C}-$linear map

$$
\begin{align}
K_{\lambda} & \rightarrow K_{\lambda}\\
v & \mapsto \left[\prod_{i = 1}^{r}(\alpha-\nu_{i}\cdot \text{id}_{V})^{m_{i}} \right](v)
\end{align}
$$

is a linear isomorphism $\forall \; m_{1}, ... m_{r}\in \mathbb{Z}_{0}^{+}$

## Theorem 3.9

Let $\alpha:V \rightarrow V$ be a $\mathbb{C}-$linear map with characteristic polynomial $P_{\alpha}(T)= \prod_{i = 1}^{l}(T-\lambda_{i})^{\mu_{i}}$, i.e. $\lambda_{1}, ...,\lambda_{l}$ are all different eigenvalues of $\alpha$. Then
1. If $V \in K_{\lambda_{i}}$ for some $1 \leq i \leq l$ we have $$(\alpha-\lambda_{i}\cdot \text{id}_{V})^{\mu_{i}}(v)= 0.$$
2. Every vector $V \in V$ can be uniquely written as a sum $$v = v_{1}+ v_{2}+... v_{l}$$ with $v_{i}\in K_{\lambda_{i}}$ for $i = 1, ..., l$.

**Proof:**

1. By the corollary above $$\begin{align}\left[\prod_{j \neq i}(\alpha-\lambda_{j}\cdot \text{id}_{V})^{\mu_{j}} \right](x)\neq 0 \end{align}$$ for all $x \neq 0$ in $K_{\lambda_{i}}$. So if $x = (\alpha-\lambda_{i}\cdot \text{id}_{V})^{\mu_{i}}(v)\neq 0$, then $$\begin{align}0& \neq \left[\prod_{j \neq i}(\alpha-\lambda_{j}\cdot \text{id}_{V})^{\mu_{j}} \right]((\alpha-\lambda_{i}\cdot \text{id}_{V})^{\mu_{i}}(V))\\ & = \left[\prod_{j = 1}^{l}(\alpha-\lambda_{j}\cdot \text{id}_{V})^{\mu_{j}} \right](v)\\ & = P_{\alpha}(\alpha)(v). \end{align}$$  So the assumption $(\alpha-\lambda_{i}\cdot \text{id}_{V})^{mu_{i}}(v)\neq 0 \Rightarrow P_{\alpha}(\alpha)(v)\neq 0$, which contradicts the Cayley-Hamilton Theorem, so $(\alpha-\lambda_{i}\cdot \text{id}_{V})(v)= 0$.
2. Existence has been proven already via decomposition of vectors into generalized eigenvectors, so all we need is to show uniqueness. Assume $$\sum\limits_{i = 1}^{l}v_{i}= v = \sum\limits_{i = 1}^{l}w_{i} $$ with $v_{i}, w_{i}\in K_{\lambda_{i}}$ for all $1 \leq i \leq l$. If we fix $i$, we get $$v_{i}-w_{i}= \sum\limits_{j \neq i}(w_{j}-v_{j}).$$ By 1. we have $(\alpha-\lambda_{j}\cdot \text{id}_{V})^{\mu_{j}}(w_{j}-v_{j})= 0$ for all $1 \leq j \leq l$. Using the fact that polynomials in $\alpha$ commute with each other, we have $$\left[\prod_{k \neq i}(\alpha-\lambda_{k}\cdot \text{id}_{V})^{\mu_{k}} \right](w_{j}-v_{j})= 0$$ for all  $j \neq i$. Hence $$\left[\prod_{k \neq i}(\alpha-\lambda_{k}\cdot \text{id}_{V})^{\mu_{k}} \right]\left(\sum\limits_{j \neq i}(w_{j}-v_{j}) \right)= \sum\limits_{j \neq i}\left[\prod_{k \neq i}(\alpha-\lambda_{k}\cdot \text{id}_{V})^{\mu_{k}} \right](w_{j}-v_{j})= 0$$ and so $$\left[\prod_{k \neq i}(\alpha-\lambda_{k}\cdot \text{id}_{V})^{\mu_{k}} \right](v_{i}-w_{j})= 0.$$ But by the corollary above, the linear map just above is an isomorphism on $K_{\lambda_{i}}$ and so $v_{i}-w_{i}= 0$, i.e. $v_{i}= w_{i}$ for all $i$.

# Dimensions of the Subspaces $K_{\lambda_{i}}$

Let $\alpha$ be as above, with characteristic polynomial $P_{\alpha} = \prod_{i = 1}^{l}(T-\lambda_{i})^{\mu_{i}}$. Let $(v_{j}^{(i)})_{1 \leq j \leq n_{i}}$ be a basis of $K_{\lambda_{i}}$for $i = 1, ... ,l$, and  let $B$ be the restriction of $\alpha$ to the $\alpha$-invariant subspace $K_{\lambda_{i}}$ with respect to this basis.

What are the eigenvalues of $B_{i}$? As seen in Lemma 3.8 above, for all $\nu \neq \lambda_{i}$, the $\mathbb{C}$-linear map

$$
K_{ \lambda_{i}} \longrightarrow K_{\lambda_{i}}\qc x \mapsto (\alpha-\nu \cdot \text{id}_{V})(x)
$$

is an isomorphism, and therefore $(\alpha-\nu \cdot \text{id}_{V})(x)\neq 0$ for all $x \in K_{\lambda_{i}}\smallsetminus \set{0}$. Another way to say this is that $(\alpha)(x)\neq \nu \cdot x$ for all $x \neq 0$ in $K_{\lambda_{i}}$ and all $\nu \neq \lambda_{i}$. However $B_{i}$ is the matrix of the $\mathbb{C}$-linear map $K_{\lambda_{i}}\longrightarrow K_{\lambda_{i}}, x \mapsto\alpha (x)$ with respect to the basis $(v_{j}^{(i)})_{1 \leq j \leq n_{i}}$, and so $\lambda_{i}$ is the only eigenvalue of $B_{i}$. Hence we have 

$$
P_{B_{i}}(T) = (T-\lambda_{i})^{n_{i}},
$$

where $n_{i}= \dim_{\mathbb{C}}K_{\lambda_{i}}$ for all $i = 1, ..., l$.

It follows from the theorem above that the union of the ordered set bases $(v_{j}^{(i)})_{1 \leq j \leq n_{i}}$  is a basis of $V$. In fact, if

$$
\sum\limits_{i = 1}^{\infty}\left(\sum\limits_{j = 1}^{\infty}a_{ij}\cdot v_{j}^{(i)} \right) = 0,
$$

then by uniqueness we have $\sum\limits_{j = 1}^{n_{i}}a_{ij}\cdot v_{j}^{(i)}= 0$ for all $i = 1, ..., l$, and so, because the vector $v_{1}^{(i)}, ..., v_{n_{i}}^{(i)}$ are all linearly independent, and $a_{ij}= 0\; \forall \; i, j$.

Then, by existence we see that these vectors generate $V$. This means that the union of these vectors is a basis for $V$. The matrix of $\alpha$ with respect to this basis is then

$$
\begin{bmatrix}
B_{1} & O_{n_{1}\times n_{2}} & \cdots & O_{n_{1}\times n_{l}} \\
O_{n_{2}\times n_{1}} & B_{2} &  & O_{n_{2}\times n_{l}} \\
\vdots &  & \ddots & \vdots \\
O_{n_{l}\times n_{1}} &  & \cdots & B_{l}
\end{bmatrix},
$$

And so we have

$$
P_{\alpha}(T) = \prod_{i = 1}^{l}P_{B_{i}}(T) = \prod_{i = 1}^{l}(T-\lambda_{i})^{n_{i}}
$$

using the equation from above. But we also have $P_{\alpha}(T)= \prod_{i = 1}^{l}(T-\lambda_{i})^{n_{i}}$, and this leads to the corollary below:

#### Corollary

Let $\alpha:\; V \rightarrow V$ be a $\mathbb{C}$-linear map with characteristic polynomial $P_{\alpha}(T)= \prod_{i = 1}^{l}(T-\lambda_{i})^{\mu_{i}}$, where $\lambda_{1}, ..., \lambda_{i}$ are all different eigenvalues of $\alpha$. Then $mu_{i}= \dim_{\mathbb{C}}K_{\lambda_{i}}$ for all $1 \leq i \leq l$.