# The Jordan Normal Form

## Reminder on Similar Matrices

Let $A$ be an $n \times n$ matrix with coefficients in $F$. This defines an $F-$linear map

$$
\begin{align}
\alpha_{A}:F^{n}&\rightarrow F^{n}\\
v & \mapsto A \cdot v.
\end{align}
$$

If $v_{1}, ..., v_{n}$ is a basis of $F^{n}$, we can express $A \cdot v_{j}$ in terms of the above basis,

$$
A \cdot v_{j}= \sum\limits_{i = 1}^{n}b_{ij}\cdot v_{i}.
$$

We say a matrix $B$ is *similar* to $A$ if there exists an invertible matrix $S$ such that

$$
B = S^{-1}\cdot A\cdot S.
$$

$S_{ij}$ is the matrix whose columns are the vectors $v_{1}, ..., v_{n}$, i.e.,

$$
\begin{align}
v_{j}= \sum\limits_{i = 1}^{n}s_{ij}\cdot e_{i}=
\begin{pmatrix}
s_{1j} \\ s_{2j} \\ \vdots \\ s_{nj}
\end{pmatrix}.
\end{align}
$$

The vectors $e_{1}, ..., e_{n}$ is the "standard" basis of $F^{n}$.

We can go in the reverse direction as well: let $T$ be an invertible matrix and $C = T^{-1}\cdot A \cdot T$. Then by definition $C \sim A$. Because $T$ is invertible, its column vectors form another basis of $F^{n}$, and $C = (c_{ij})$ is the matrix of $\alpha_{A}$ with respect to this new basis.

## The Case of $2 \times 2$ Matrices

Let

$$
\begin{align}
A =
\begin{pmatrix}
a & b \\ c & d
\end{pmatrix}
\end{align}
$$

be a complex $2 \times 2$ matrix. Its corresponding $\mathbb{C}-$linear map is given by

$$
\begin{align}
\alpha_{A}:\mathbb{C}^{2}&\rightarrow \mathbb{C}^{2}\\
x & \mapsto A \cdot x.
\end{align}
$$

Because every polynomial in $\mathbb{C}$ has a root, we have

$$
P_{A}(T)= (T-\lambda_{1})\cdot (T-\lambda_{2}),
$$

where $\lambda_{1, \lambda_{2}}$ are the eigenvalues of $A$, which may be equal.

If $\lambda_{1}\neq \lambda_{2}$, then $A$ is diagonalizable, i.e. similar to a diagonal matrix. In fact,  if $v_{1}, v_{2}$ are the eigenvectors for $\lambda_{1}$ and $\lambda_{2}$ respectively, then since $\lambda_{1}\neq\lambda_{2}$ the vectors $v_{1}, v_{2}$ form a basis of $\mathbb{C}^{2}$. With respect to this basis, the matrix of $\alpha_{A}$ is

$$
\begin{align}
\begin{pmatrix}
\lambda_{1} & 0 \\ 0 & \lambda_{2}
\end{pmatrix}.
\end{align}
$$

If $\lambda_{1}= \lambda_{2}$, then the matrix may or may not be diagonalizable. We set $\lambda:= \lambda_{1}$.  If there are two eigenvectors $v, w$ that are linearly independent, then the matrix of $\alpha_{A}$ with respect to the basis $v, w$ is

$$
\begin{align}
\begin{pmatrix}
\lambda & 0  \\ 0 & \lambda
\end{pmatrix},
\end{align}
$$

and so $A$ can still be diagonalized.

If $A$ is not diagonalizable, that means the dimension of the eigenspace for $\lambda$ is $1$. Let $v$ be an eigenvector for $\lambda$ and $w' \in \mathbb{C}^{2}$ be any other vector, such that $v, w'$ is a basis of $\mathbb{C}^{2}$. Then, $\alpha_{A}(v)= A \cdot v = \lambda \cdot v$ and $\alpha_{A}(w')= b \cdot v + c \cdot w'$ for some complex numbers $b, c$. The matrix of $\alpha_{A}$with respect to this basis is

$$
\begin{align}
\begin{pmatrix}
\lambda & b \\ 0& c
\end{pmatrix}.
\end{align}
$$

Since the matrix is similar to $A$, it must have the same characteristic polynomial $P_{A}(T)= (T-\lambda)^{2}$, and so $c = \lambda$. Therefore $A$ is similar to

$$
\begin{align}
B':=
\begin{pmatrix}
\lambda & b \\ 0 & \lambda
\end{pmatrix}.
\end{align}
$$

We know that $b \neq 0$, since the matrix would then be diagonalizable, since the eigenspace would have dimension $2$.

We now replace the basis $v, w'$ by $v, b^{-1}\cdot w'= w$. Then we have $\alpha_{A}(v)= \lambda \cdot v$, and

$$
\begin{align}
\alpha_{A}(w) & = \alpha_{A}(b^{-1}\cdot w')\\
& = b^{-1}\cdot \alpha_{A}(w')\\
& = b^{-1}\cdot (\lambda \cdot w' + b \cdot v)\\
& = \lambda \cdot w + v,
\end{align}
$$

And the matrix of $\alpha_{A}$ with respect to to this basis is

$$
\begin{align}
\begin{pmatrix}
\lambda & 1 \\ 0 & \lambda
\end{pmatrix}.
\end{align}
$$

Hence, if $A$ is not diagonalizable, $A$ is similar to a so called $2 \times 2-$*Jordan block*, i.e. there exists a basis of $\mathbb{C}^{2}$, such that the linear map $\alpha_{A}$ has the above matrix, where $\lambda$ is the only eigenvalue of $A$, with respect to this basis.

Such a basis is called a *Jordan basis* for $A$. We will discuss these later with a more precise definition.

**Example:** Let

$$
\begin{align}
A =
\begin{pmatrix}
1 & 2 \\ -2 & 5
\end{pmatrix}
\in M_{2 \times 2}(\mathbb{C}).
\end{align}
$$

Then we have

$$
P_{A}(T) = (T-3)^{2},
$$

so $\lambda = 3$ is the only eigenvalue of $A$. Its corresponding eigenvector is

$$
\begin{align}
v =
\begin{pmatrix}
1 \\ 1
\end{pmatrix}.
\end{align}
$$

We can then extend this to a basis $\mathbb{C}^{2}$ by adding

$$
\begin{align}
w' =
\begin{pmatrix}
0 \\ 1
\end{pmatrix}.
\end{align}
$$

Computing $\alpha_{A}(v)= 3 \cdot v$, and

$$
\alpha_{A}(w')= A \cdot w' = 2 \cdot v + 3 \cdot w'.
$$

We now replace the basis of $v, w'$ by $v, w$, where $w = w'^{-1}$, so

$$
\begin{align}
v =
\begin{pmatrix}
1 \\ 1
\end{pmatrix}
\quad \text{and}\quad w =
\begin{pmatrix}
0 \\ \frac{1}{2}
\end{pmatrix},
\end{align}
$$

And compute $\alpha_{A}(v)= 3 \cdot v$ and $\alpha_{A}(w)= v + 3 \cdot w$, so $\alpha_{A}$ has the matrix

$$
\begin{align}
B =
\begin{pmatrix}
3 & 1 \\ 0 & 3
\end{pmatrix}
\end{align}
$$

With respect to this basis. This matrix is similar to $A$ and we have

$$
B = S^{-1}\cdot A \cdot S
$$

for $S = (v  \quad w)$.

## Generalized Eigenvalues

Let $V$ be a finite dimensional complex vector space and $\alpha:V \rightarrow V$ a $\mathbb{C}-$linear map. A complex number $\lambda$ is called a *generalized eigenvalue* of $\alpha$ if there is an integer $l \geq 1$, and a non-zero vector $v \in V$, such that

$$
(\alpha-\lambda \cdot \text{id}_{V})^{l}(v)= 0.
$$

$v$ is then called a *generalized eigenvector* for $\lambda$. The union of the zero vector and all the generalized eigenvectors for the generalized eigenvalue $\lambda$ is denoted by $K_{\lambda}$, or more precisely $K_{\lambda}(\alpha)$. We call this the *generalized eigenspace* for the eigenvalue $\lambda$ (this is really a subspace of $V$, as we will see later.)

Similarly, the union of the zero vector and the set of all the eigenvectors of $\lambda$ is denoted by $E_{\lambda}$, or $E_{\lambda}(\alpha)$. We call this the *eigenspace* for the eigenvalue $\lambda$ of $\alpha$.

**Example:** If $V = \mathbb{C}^{n}$ and $\alpha = \alpha_{A}:\mathbb{C}^{n}, \; v \mapsto A \cdot v$, for some $n \times n$ matrix $A$,  then

$$
(\alpha_{A}-\lambda \text{id}_{V})(v) = (A-\lambda \cdot I_{n})\cdot v = A \cdot v-\lambda \cdot v,
$$

and so $(\alpha_{A}-\lambda \cdot \text{id}_{V})^{l}(v) = (A - \lambda \cdot I_{n})^{l}\cdot v$. In this case a generalized eigenvalue (respectively the eigenvector) of $\alpha_{A}$ is also called a generalized eigenvalue (respectively eigenvector is) of the matrix $A$.

It should be clear that an eigenvalue is also a generalized eigenvalue, and vice versa. Let $v$ be a generalized eigenvector for the generalized eigenvalue $\lambda$ of $\alpha$, and say we have $(\alpha-\lambda \cdot \text{id}_{V})^{l}(v)= 0$ for some $l \geq 1$. Assuming that $l$ is the smallest with this property, then it is intuitive that $v' = (\alpha- \lambda \cdot \text{id}_{V})^{l-1}(v)\neq 0$ and $(\alpha-\lambda \cdot \text{id}_{V})^{l}(v')=(\alpha-\text{id}_{V})^{l}= 0$. The latter equation implies $\alpha (v')= \lambda \cdot v'$, and therefore $v'$ is an eigenvector for $\lambda$, i.e. $\lambda$ is an eigenvalue. 

On the other hand, eigenvectors for $\lambda$ are generalized eigenvectors, but generalized eigenvectors for $\lambda$ need not be eigenvectors of $\alpha$. As an example, consider the $\mathbb{C}-$linear map $\alpha_{A}:\; \mathbb{C}^{2}\rightarrow \mathbb{C}^2$, $v \mapsto A \cdot v$, where $A$ is the $2 \times 2$ matrix

$$
\begin{align}
\begin{pmatrix}
1 & 1 \\ 0 & 1
\end{pmatrix}.
\end{align}
$$

The only eigenvalue is $\lambda = 1$, which is then also its only generalized eigenvalue. We then have 

$$
\begin{align}
A \cdot
\begin{pmatrix}
0 \\ 1
\end{pmatrix}
=
\begin{pmatrix}
1 \\ 1
\end{pmatrix}
\end{align}
$$

and so

$$
\begin{align}
v =
\begin{pmatrix}
0 \\ 1
\end{pmatrix}
\end{align}
$$

Is not an eigenvector of $A$. However,

$$
\begin{align}
I_{n}-A=
\begin{pmatrix}
0 & -1 \\ 0 & 0
\end{pmatrix},
\end{align}
$$

and therefore $(I_{n}-A)^{2}= 0$, which has the consequence that $(I_{n}-A)^{2}\cdot v = 0$, i.e. $v$ is a generalized eigenvector, but not an eigenvector.

#### Lemma

The set $K_{\lambda}= K_{\lambda}(\alpha)\subset V$ is a linear subspace which is $\alpha-$invariant.

**Proof:** We already know from a previous example that $K_{\lambda}$ is $\alpha-$invariant, so we only need to show that it is a $\mathbb{C}-$linear subspace, i.e. we have to verify that if $\mu, \nu \in \mathbb{C}$ and $v, w \in K_{\lambda}$, then $\mu \cdot v + \nu \cdot w$ is also in $K_{\lambda}$.

Since $v, w \in K_{\lambda}$ there are integers $k, l \geq 1$, such that $(\alpha-\lambda \cdot \text{id}_{V})^{k}(v) = 0$ and $(\alpha-\lambda \cdot \text{id}_{V})^{l}(w) = 0$. It then follows that since $\alpha$ and $(\alpha- \lambda \cdot \text{id}_{V})^{k + l}$ is $\mathbb{C}-$linear,

$$
\begin{align}
(\alpha-\lambda \cdot \text{id}_{V})^{k + l}\cdot (\mu \cdot v+ \nu \cdot w) & = \mu \cdot (\alpha-\lambda \cdot \text{id}_{V})^{k + l}\cdot v + \nu \cdot (\alpha-\lambda \cdot \text{id}_{V})^{k + l}\cdot w \\
& = \mu \cdot (\alpha-\lambda \cdot \text{id}_{V})^{l}[(\alpha-\lambda \cdot \text{id}_{V})^{k}\cdot v] + \nu \cdot (\alpha-\lambda \cdot \text{id}_{V})^{k}[(\alpha-\lambda \cdot \text{id}_{V})^{l}\cdot w]\\
& = 0,
\end{align}
$$

and so $\mu \cdot v+ \nu \cdot w \in K_{\lambda}$, therefore $K_{\lambda}$ is $\mathbb{C}-$linear, therefore the lemma is true.

## Decomposition of a Vector Into a Sum of Generalized Eigenvectors

If $\alpha:V \rightarrow V$ is a $\mathbb{C}-$linear map then any $v$ in the finite dimensional vector space $V$ can be written as a sum of generalized eigenvectors of $\alpha$. We now represent the characteristic polynomial of $\alpha$ by

$$
P_{\alpha}(T) = \prod_{i = 1}^{l}(T-\lambda_{i})^{\mu_{i}},
$$

where $\lambda_{1}, ..., \lambda_{l}$ are all *different* eigenvalues of $\alpha$. By the Cayley-Hamilton theorem, we know that $P_{\alpha}(\alpha)(v)= 0$ for some $v \in V$.

If $\alpha$ has only one eigenvalue $\lambda = \lambda_{1}$, then $P_{\alpha}(T)= (T-\lambda)^{\mu}$, where $\mu = \mu_{1}= \dim_{\mathbb{C}}V$, and so

$$
P_{\alpha}(\alpha)(v) = (\alpha-\lambda-\text{id}_{V})^{\mu}(v) = 0.
$$

In other words, every $v \in V$ is in the generalized eigenspace $K_{lambda}$, and we get the trivial decomposition $v = v$.

Now, let's assume that $\alpha$ has at least two eigenvalues, i.e. $l \geq 1$. Then

$$
\begin{align}
0 & = P_{\alpha}(\alpha)(v)= \left[\prod_{i = 1}^{l}(\alpha-\lambda_{i}\cdot \text{id}_{V})^{\mu_{i}}\right] (v)\\[1em]
& = (\alpha-\lambda_{i}\cdot \text{id}_{V})^{\mu_{i}}\left(\left[\prod_{j \neq i}(\alpha-\lambda_{j}\cdot \text{id}_{V})^{\mu_{j}}\right] (v)\right)
\end{align}
$$

for all $1 \leq i \leq l$. Hence we have $(\alpha-\lambda_{i} \cdot \text{id}_{V})^{\mu_{i}}([\prod_{j \neq i}(\alpha-\lambda_{j}\cdot \text{id}_{V})^{\mu_{j}}](v))= 0$ and therefore the right term is either $0$, or it is a generalized eigenvector for $\lambda_{i}$.

Since for $r \neq s$, $\lambda_{r}\neq \lambda_{s}$, the polynomials

$$
f_{i}(T):= \prod_{j \neq i}(T-\lambda_{j})^{\mu_{j}}, \; i =  1, ..., l
$$

do not have a common root. Therefore by a corollary from complex analysis there are polynomial $k_{1}(T), ..., k_{l}(T)$ such that

$$
1 = \sum\limits_{i = 1}^{l}k_{i}(T)\cdot f_{i}(T).
$$

These are all the tools needed to prove the decomposition.

As seen above, the vector $f_{i}(\alpha)(v)$ lies in the generalized eigenspace $K_{\lambda_{i}}$ for all $1 \leq i \leq l$, and so as $K_{\lambda_{i}}$ is $\alpha-$invariant, $k_{i}(\alpha)(f_{i}(\alpha)(v))$ is also $\alpha-$invariant. Therefore we have by the equation above

$$
v = \text{id}_{V}(v)= \sum\limits_{i = 1}^{l}k_{i}(\alpha)(f_{i}(\alpha)(v)),
$$

so setting $v_{i}= k_{i}(\alpha)(f_{i}(\alpha)(v))$, we can write

$$
v = v_{1} + v_{2}+... + v_{l}
$$

with $v_{i}\in K_{\lambda_{i}}$.