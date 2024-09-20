#### Lemma

For any two non-empty sets, the following are equivalent:
1. We have a 1-1 function from $A$ to $B$.
2. There is an onto function from $A$ to $B$.

**Proof:** To prove $(i)\Rightarrow (ii)$, we assume $f:A \rightarrow B$ is 1-1, and pick some $a_{0}\in A$. We define a function $g:B \rightarrow A$ as

$$
\begin{align}
g (b)& =
\begin{cases}
a \; \text{if}\; b = f (a) \\
a_{0} \; \text{if}\; b \notin f (A)
\end{cases}
\end{align}
$$

We claim that $g$ is onto. Reason:

$$
g (f (a))= a \; \forall \; a \in A
$$

To prove $(ii) \Rightarrow (ii)$, assume $g:B \rightarrow B$ is onto:

$$
\forall \; a \in A, \; g^{-1}(\{a \})= \{b \in B:g (b)= a \}\neq \varnothing
$$

We can define a mucks $f:A \rightarrow B$ by just letting $f (a)$ be **any** element of $g^{-1}(\{a \})$.

We claim that $f$ is 1-1. Reason: Assume $f ren a = f (\tilde{a}))\Rightarrow g (f (a))= g (f (\tilde{a}))\Rightarrow a = \tilde{a}$

That's the end of the introductory chapter.

# Numbers

We have several kinds of numbers:
## The natural numbers $(\mathbb{N})$.
1. We can add natural numbers. This operation is associative and commutative.
2. We can multiply natural numbers. This operations is associative and commutative. 
3. It is also distributive.
4. There is a neutral element $1_{\mathbb{N}}$.
5. The natural numbers are ordered. In  Other words, they are transitive.
6. Order is compatible with addition and multiplication.
7. The natural numbers are "well ordering." Every subset of natural numbers contains a smallest element (the well ordering axiom).

### Theorem 2

There is no largest prime number. For every $n \in \mathbb{N}$ there exists a prime $p > n$.

**Proof:** If $n = 1$, take $p = 2$. Let $p_{1}, ..., p_{m}$ be all primes $p \leq n$.

Consider $\tilde{n}= p_{1}p_{2}\cdots p_{m}+ 1$. Note that $p_{1}\nmid\tilde{n}$. On the other hand, $P (\tilde{n})$ is a prime and divides $\tilde{n}$. This implies $p (\tilde)\neq p_{1}p_{2}\cdots p_{m}$, which implies that $p (\tilde{n})$.

This proof only works because of the well ordering that we mentioned. For us, however, its most. Important use is in the Principle of Mathematical Induction.

### Theorem 3

Assume a set $A \subset \mathbb{N}$ loss two properties:

1. $n_{0}\in A$.
2. if $n \geq n_{0}$ and $n \in A$, then $n + 1 \in A$.

Then $A \supset \{n_{0}n_{0}+ 1, ... \}= \{n \in \mathbb{N}:n \geq n_{0}\}$

**Proof:** Let $B = \{n_{0}, n_{0}+ 1, ... \}\smallsetminus A$. We claim that $B$ is non-empty. From well orderedness, $B$contains a smallest element, say $n$.

Note: 

$$
\begin{align}
n > n_{0}\\
n-1 \geq n_{0}\\
\Rightarrow n-1 \in A \Rightarrow n \in A
\end{align}
$$

We use Theorem 3 as follows:

For every $n \in \mathbb{N}$, let $S_{n}$ be **some** statement. Assume we know that $S_{n_{0}}$ is true and if $f \geq n_{0}$ and $S_{n}$ is true. Then $s_{n + 1}$ is true.

#### Example 4

Prove 

$$
1^{2}+ 2^{2}+ 3^{2}+ \cdots + n^{2}=\frac{n (n + 1)(2n + 1)}{6}.
$$

We start with the base case, $n_{0}= 1$:

$$
1^{2}= \frac{1 + 2 + 3}{6}= 1.
$$

Now, we assume

$$
1^{2}+ \cdots + n^{2}= \frac{n (n + 1)(2n + 1)}{6}
$$

for *some* $n$.

$$
\begin{align}
\sum\limits_{i = 1}^{n + 1} & = j^{2}+ (n + 1)^2\\
& = \frac{n (n + 1)(2n + 1)}{6}+ (n + 1)^{2}\\
& = \vdots \\
& =  \frac{(n + 1)(n + 2)(2(n + 1)+ 1)}{6}
\end{align}
$$

#### Example 5

Show that $2^{n}\geq n^{2}\; \forall n \geq 4$

Base case: $n_{0}=4$, $2^{4} \geq 4^{2}$. Now assume $2^{n}\geq n^{2}$:

$$
\begin{align}
2^{n + 1}= 2 \cdot 2^{n}& \geq (n + 1)^{2}+ 2n^{2}-(n + 1)^{2}\\
& = (n + 1)^{2}+ n^{2}-2n-3
\end{align}
$$