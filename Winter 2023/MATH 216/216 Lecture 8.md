#### Lemma 33

$A_{j}$ countable $\forall \; j \in \mathbb{N}$. The claim is that the union of all sets $\bigcup_{j \in \mathbb{N}} A_{j}= \{a \mid a \in A_{j}\; \text{for at least one}\; j \in \mathbb{N} \}$.

**Proof:**

$\forall \; j \in \mathbb{N}\;\exists\; f_{j}:\mathbb{N}\rightarrow A_{j}$ that is onto. Let $A = \bigcup_{j \in \mathbb{N}}A_{j}$. Then we can define $f:\mathbb{N}\rightarrow A$ as follows:

$$
\begin{align}
f (1) & = f_{1}(1)\\
f (2) & = f_{1}(2)\\
f (3) & = f_{2}(1)\\
& \vdots\\
\forall \; a& \in A_{j}
\end{align}
$$

so there exists $n \in \mathbb{N}$ such that $f (n)= a$. I.e., $f$ is onto. As a consequence, we get

#### Theorem 34

$\mathbb{Q}$ is countable.

**Proof:**

Consider $f:\mathbb{N}\rightarrow \mathbb{Z}$ with 

$$
\begin{align}
f (n) & =
\begin{cases}
\frac{n}{2} \quad \text{if $n$ is even}\\
-\frac{n-1}{2} \quad \text{if $n$ is odd}.
\end{cases}\\
f (1)& = 0 \\
f (2) & = 1 \\
f (3) & = -1 \\
f (4) & = 2 \\
& \vdots
\end{align}
$$

is bijective $\Rightarrow \mathbb{Z}$ is countable. $\forall \; A_{j}\in \mathbb{N}$ let $A_{j}= \{\frac{k}{j}\mid k \in \mathbb{Z}\smallsetminus \{0\} \}$ and $k, j$ have no common factors. Then $A_{j}$'s are countable by lemma 33.

We will see in the next chapter that $\mathbb{R}$ is uncountable!

#### Remark 35

Let $A= \{a \in \mathbb{R}\mid a \;\text{is algebraic} \}$. Clearly, $\mathbb{Q}\subseteq \mathbb{A}\subset \mathbb{R}$. It turns out that $\mathbb{A}$ is an ordered field for which $AP$ is valid, but $LUB$ is **not**. Moreover, it's not hard to is see that $\mathbb{A}$ is countable. Therefore, $\mathbb{R}\smallsetminus \mathbb{A}\neq \varnothing$; in fact, many interesting numbers in analysis are elements of $\mathbb{R}\smallsetminus \mathbb{A}$, otherwise known as transcendental.

Moving from $\mathbb{Q}$ to ${R}$, what have we gained? We get the least upper bound principle and all its profound consequences (many of which we will explore later on).

We have lost the ability to list these numbers in a reasonable way.

# Chapter 3: Sequences

Sequences are the perfect tool to explore the jungle that is $\mathbb{R}$. First, some basic definitions and properties.

## Definitions and Properties

#### Definition 1

Let $A \neq \varnothing$ be a set. A sequence (in $A$) is any function $a:\mathbb{N}\rightarrow A$ where we write $a (n)$ as $a_{n}$. Formally, a sequence is a function $a:\mathbb{N}\rightarrow a ; \; n \mapsto a (n)= a_{n}$. Practically, we write it as $(a_{n})$. For us, we will mostly consider $A \subset \mathbb{R}$, i.e. we consider real sequences. Sometimes we consider $(a_{n})_{n \geq n_{0}}$. We think of $(a_{n})$ is an infinite list of objects (numbers)

**Example 2:**

1. $a_{n} = \frac{1}{n}\; \forall \; n \in \mathbb{N}$.
2. $a_{n}= (-1)^{n}\; \forall \; n \in \mathbb{N}$ (formulas).
3. Let $a_{n}$ be the $n$-th prime number (verbal description).
4. $a_{1}= 2, \; a_{n + 1}= \frac{1}{2}(a_{n}+ \frac{2}{a_{n}})\; \forall \; n \in \mathbb{N}$ (recursively).

#### Definition 3

A sequence $(a_{n})$ in $\mathbb{R}$ is *bounded* if the set $\{a_{n}\mid n \in \mathbb{N} \}$ is bounded

**Example 3:**

1. $a_{n}= \frac{1}{n}$ is bounded, is $0 < \frac{1}{n}< 1$.
2. $a_{n}= (-1)^{n}\in \{-1, 1 \}$ is clearly bounded. Don't confuse $(a_{n}) = (a_{1}, \; a_{2}, ...)$ with $\{a_{n}\mid n \in \mathbb{N} \}$.
3. $a_{n}= p_{n}$ is unbounded.
4. $a_{1}= 2, \; a_{n + 1}= \frac{1}{2}(a_{n}+ \frac{2}{a_{n}})$ is also bounded.

#### Definition 4

A sequence $(a_{n})\in \mathbb{R}$ *converges* to $a \in \mathbb{R}$ if $\forall \; \epsilon \geq 0 \; \exists \; N \in \mathbb{N}$ such that $\abs{a_{n}-a}< \epsilon \; \forall\; n \geq N$. The sum $a \in \mathbb{R}$ is known as the *limit* of $(a_{n})$.

$$
a = \lim_{n \rightarrow \infty}a_{n}.
$$

A sequence $A$ converges, or is convergent, if $\lim_{n \rightarrow \infty}a_{n}= a$ for some $a \in \mathbb{R}$. Otherwise it is known as divergent.

#### Remark 5

This is the **most** important definition in MATH 216!

$\infty$ is *deeply* ingrained in this definition. It appears twice above, like $\forall \; \epsilon > 0$ gives an unlimited number of choices, and for every single one, it must hold true. Similarly for $\forall \; n \in N$.

Usually, $N$ depends on $\epsilon$, and the smaller the $\epsilon$, the larger the $N$.

If $(a_{n})$ is modified for finitely many $n$, then this does **not** affect the convergence or divergence of $(a_{n})$, nor its limit if the limit exists. More formally, if $(\tilde{a}_{n})$ is such that $a_{n}\neq \tilde{a}_{n}$ for finitely many indices, then $(a_{n})$ converges or diverges if and only if $\tilde{a}$ also converges or diverges, and $\lim_{n \rightarrow \infty}a_{n}= \lim_{n \rightarrow \infty}\tilde{a}_{n}$. We only care about the "tail" of the sequence.

**Example 5:**

1. $a_{n}= \frac{1}{n}$. $\forall \; \epsilon > 0, \; \exists \; N \in \mathbb{N}$ such that $N > \frac{1}{\epsilon}$ by $AP$.  $0 < \frac{1}{n}\leq \frac{1}{N}< \epsilon \Rightarrow \abs{\frac{1}{n}-0}= \frac{1}{n}< \epsilon \Rightarrow \lim_{n \rightarrow \infty}\frac{1}{n}= 0$. 