#### Theorem 6

Every number $n > 1$ can be written as a unique product of primes. That is, for $m \in \mathbb{N}$ there exist primes $p_{1}, p_{2}, ...$, such that $p_{1} \leq p_{2}\leq p_{3}\leq p_{m}$ and $p_{1}p_{2}... p_{m}= n$. This **prime factorization** of $n$ is unique (this is known as the fundamental theorem of arithmetic).

**Proof:** $S_{n}:2, 3, ..., n$ have a unique prime factorization. $S_{2}$ is true, so the base case is proven. For induction, assume $S_{n}$ is true. Consider $S_{n+ 1}$, and distinguish two cases:
1. $n + 1$ is prime $\Rightarrow$ has unique prime factorization.
2. $n + 1$ is not prime, i.e. $P (n + 1)< n + 1$. But $P (n + 1)\mid n + 1$, and $(n + 1)/P (n + 1)\leq n\Rightarrow$ has unique prime factorization. We have existence, now for uniqueness. 

Have **any** prime factorization of $n + 1$, say

$$
n + 1 = p_{1}p_{2}... p_{l}.
$$

We know $P (n + 1)\leq P_{1}$. Consider

$$
\tilde{n} = (p_{1}-p_{n + 1})p_{2}... p_{l},
$$

then:
1. $P (n + 1)\mid \tilde{n}$.
2. $P (n + 1)\mid P_{1}-P (n + 1)$.
3. $P (n + 1)\mid p_{1}$.

This implies $p_{1}= P(n + 1)$,

$$
\begin{align}
\frac{n + 1}{P (n + 1)}& = p_{2}... p_{l}\leq n \\
\frac{n + 1}{P (n + 1)} \; \text{has unique factorization}
\end{align}
$$

Which implies $n + 1$ has unique factorization. This completes the proof.

Another important application of $\mathbb{N}$: counting! One example of counting: Say we have $n$ objects, all similar and labeled. Given $j \in \mathbb{N}$, how many ways can you choose $j$ objects
1. If the order matters.
2. If the order doesn't matter.

Say $n = 3, j = 2$.
1. We have six combinations: $(1, 2), (2, 1), (1, 3), (3, 1), (2, 3), (3, 2)$.
2. If the order doesn't matter, we only have three.

In general, the number of selections if order matters is $n (n-1)(n-2)... (n-j + 1)$. If $j = n$, then we get $n!$. This can be thought of as the number of permutations. If $j > n$, then the number of objects is clearly zero.

For the other case, we have

$$
\frac{n (n-1)... (n-j + 1)}{j!}
$$

This has the familiar notation

$$
\begin{align}
\begin{pmatrix}
n \\ j
\end{pmatrix}.
\end{align}
$$

This is read as "$n$ choose $j$." Similar to the first case, if $j > n$, then we get zero, and if $j = n$, then we get $1$. We also adopt the convention that if $j = 0$, then we get $1$.

#### Theorem 7

For every natural number $n \in \mathbb{N}$,

$$
\begin{align}
\sum\limits_{j = 0}^{n}
\begin{pmatrix}
n \\ j
\end{pmatrix}
= 2^{n}.
\end{align}
$$

**Proof:** By induction, the base case holds trivially. For the induction step,

$$
\begin{align}
_{n + 1}C_{j} & = \frac{(n + 1)(n)(n-1)... (n-j + 1)}{j!}\\
& = \frac{n + 1}{n + 1-j}\cdot \frac{n (n-1)... (n-j + 1)}{j!}\\
& = \, _{n}C_{j}+  \, _{n}C_{j-1}.
\end{align}
$$

$$
\begin{align}
\sum\limits_{j = 0}^{n + 1}& = 1 + \sum\limits_{j = 0}^{n + 1}\, _{n + 1}C_{j}\\
& = 1 + \sum\limits_{j = 0}^{n + 1} \, _{n}C_{j} + \sum\limits_{j = 1}^{n + 1} \, _{n}C_{j-1}\\
& = \sum\limits_{ j = 0}^{n} \, _{n}C_{j}+ \sum\limits_{j = 0}^{n} \, _{n}C_{j}\\
& = 2 \cdot \sum\limits_{j = 0}^{n} \, _{n}C_{j}\\
& = 2^{n + 1}
\end{align}
$$

and this completes the proof.

#### Corollary

For every $n \in \mathbb{N}$, the set $\{1, 2, ..., n \}$ has precisely $2^{n}$ subsets. This follows from the proof we just did; the number of $j-$element subsets is exactly $_{n}C_{j}$, and the sum of **all** subsets is exactly $2^{n}$.

We have two shortcomings of $\mathbb{N}$:
1. Addition: given $m, n \in \mathbb{N}$, $x + m = n$ may or may not be solvable. For example, $x + 6 = 2$ is not solvable.
2. Multiplication: given $m, n \in \mathbb{N}$, $xm = n$ may again be solvable or unsolvable, for example $4 \cdot x = 1$ is not solvable.

These problems bring us to the next set of numbers: the integers

# The Integers $\mathbb{Z}$

The set $\mathbb{Z}$ of integers is simply $\mathbb{Z}= \{0, \pm1, \pm2, \pm3, ... \}$. Not very much changes with the addition of these numbers, but we are now able to solve the first problem that the natural numbers have. Addition is now *closed*, thanks to the addition of the neutral additive element $0$ ($x + 0 = x$). We now also have an additive inverse for every element in $\mathbb{Z}$, $(x + (-x))= 0$. There is also a change to the ordering: For $m \leq n$: $ml \leq nl$ only if $l > 0$. If $l < 0$, our inequality flips.

In going from $\mathbb{N}$ to $\mathbb{Z}$, we have gained closure of addition, but we have lost the well ordering principle. This is not a huge loss, thankfully.

We will only prove one theorem for the integers, but it is an important result.

#### Theorem 8

For two integers $k, l$, and positive integer $n$,

$$
(k + l)^{n}= \sum\limits_{j = 0}^{n} \, _{n}C_{j}\cdot k^{n-j}\cdot l^{j}.
$$

**Proof:**

For $n = 1$,

$$
\begin{align}
\sum\limits_{j = 0}^{1} \, _{1}C_{0}\cdot a^{1-j}\cdot b^{j} = (a + b).
\end{align}
$$

For the induction step:

$$
\begin{align}
(a + b)^{n + 1} & = (a + b)(a + b)^{n}\\
& = (a + b)\cdot \sum\limits_{j = 0}^{n} \, _{n}C_{j}\cdot a^{n-j}\cdot b^{j}\\
& = \sum\limits_{j = 0}^{n} \, _{n}C_{j}\cdot a^{n + 1-j}\cdot b^{j}+ \sum\limits_{j = 0}^{n} \, _{n}C_{j}\cdot a^{n-j}\cdot b^{j + 1}\\
& = a^{n + 1}+ \sum\limits_{j = 1}^{n + 1} \, _{n}C_{j}\cdot a^{n + 1-j}\cdot b^{j}+ \sum\limits_{j = 1}^{n + 1} \, _{n}C_{j}\cdot a^{n-(j-1)}\cdot b^{j}\\
& \vdots \\
& = \sum\limits_{j = 0}^{n + 1} \, _{n + 1}C_{j}\cdot a^{n + 1-j}\cdot b^{j}
\end{align}
$$