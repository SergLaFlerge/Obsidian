# The Real Numbers $\mathbb{R}$

The real numbers are an ordered field that has the [[216 Lecture 5#^f9e9d8|least upper bound property]].

#### Remark 15

1. $\mathbb{R}$ exists.
2. $\mathbb{R}$ is unique.
3. Neither 1. nor 2. will be of concern. We will treat the least upper bound property as an axiom (just as the properties of addition, multiplication, an order which are inherited from $\mathbb{Q}$.) This is also known as the completeness axiom.

We visualize $\mathbb{R}$ as the unbroken number line. This. allows us to solve equations such as $x^{2}= 2$.

Before we start exploring the real numbers, we recall some important tools:
- Absolute value
- intervals

## Absolute Value

The **absolute value** of some number $a \in \mathbb{R}$ is defined as

$$
\begin{align}
|a|=
\begin{cases}
a, \; a \geq 0 \\
-a, \; a \leq 0
\end{cases}
\end{align}
$$

#### Lemma 17

For all $a, b \in \mathbb{R}$,
1. $|a|\geq 0$ and $|-a|\geq 0$.
2. $|a|= 0 \Leftrightarrow a = 0$.
3. $|a + b|\leq|a|+|b|$ (triangle inequality).
4. $|a\cdot b|=|a|\cdot|b|$.

#### Corollary 18

For all $a, b, c \in \mathbb{R}$:
1. $||a|-|b|| \leq|a-b|$.
2. $|a-b|\leq|a-c|+|c-b|$.

## Intervals

For any $a, b\in \mathbb{R}$, we consider

$$
[a, b] := \{k \in \mathbb{R}\mid a \leq x \leq b\}.
$$

This is a closed interval. If $a \geq b$, then $[a, b]= \varnothing$. If $a = b$, then $[a, b]= \{a\}$. For open intervals, we use

$$
] a, b [ := \{x \in \mathbb{R}\mid a < x < b\}.
$$

We can mix these two intervals to make a half-open or half-closed interval. We should also consider unbounded intervals,

$$
]-\infty, b] := \{x \in \mathbb{R}\mid x \leq b\}
$$

Which are always at least half-open or half-closed, or open.

With all these tools, we can begin exploring the real numbers — everything hinges on the least upper bound axiom, which also has a "twin:"

#### Proposition 19

For every set $A \subset \mathbb{R}$ with $A \neq \varnothing$ that is bounded with below has a largest lower bound, i.e., $\inf A$ exists in $\mathbb{R}$.

## Theorem 20

For every $a \in \mathbb{R}$ there exists $n \in \mathbb{N}$ such that $n > a$. Informally, $\mathbb{R}$ is "not that big." This is known as the Archimedean property (AP for short) of $\mathbb{R}$.

**Proof:** Suppose $\exists \; a \in \mathbb{R}$ such that $a \geq n\; \forall\; \in \mathbb{N}$. This implies $a$ is the supremum for $\mathbb{N}:= A \neq \varnothing$. By LUB, $A$ has a least upper bound, say $s$

$$
s = \sup A
$$

Therefore, $\exists \; n \in \mathbb{N}$ such that $n-1 < n$, $s < n + 1 \in \mathbb{N}$. Therefore, $s$ is **not** an upper bound.

#### Corollary 21

For every $a, b \in \mathbb{R}^{+}$:
1. $\exists \; m \in \mathbb{N}$ such that $1/m < 0$.
2. $\exists \; n \in \mathbb{N}$ such that $na > b$.

**Proof:**
1. Since $1/a \in \mathbb{R}^{+}$, by  AP $\exists \; m \in \mathbb{N}$ such that $$\begin{align}\frac{1}{a} &< m \\ 1 &< am \\ \frac{1}{m} & < a. \end{align}$$
2. Apply 1. to $a/b$, and then $b < na$.

#### Corollary 22

If $a \in \mathbb{R}$ and $a \leq 1/n$ for $n \in \mathbb{N}$, then $a \geq 0$.

**Proof:** Suppose $a > 0$. Then $1/n < a$ for some $n \in \mathbb{R}$ by corollary 21.

#### Corollary 23

For every $a, b \in \mathbb{R}$, with $a < b$:
1. $\exists \; r \in \mathbb{Q}$ such that $a < r < b$ ($\mathbb{Q}$ is "dense" in $\mathbb{R}$).
2. $\exists \; c \in \mathbb{R}\smallsetminus \mathbb{Q}$ such that $a < r < b$ ($\mathbb{R}\smallsetminus \mathbb{Q}$ is dense in $\mathbb{R}$).

Next, we study powers of $a \in \mathbb{R}^{+}$

## Powers of $a \in \mathbb{R}^{+}$

We define

$$
\begin{align}
a^{n} & = \underbrace{a \cdot a \cdot a... \cdot a}_{n- \text{times}}\\
a^{-n} & = (a^{-1})^{n} = \frac{1}{\underbrace{a \cdot a \cdot a... \cdot a}_{n-\text{times}}}.
\end{align}
$$

From this, we have two basic properties:
1. $a^{k + l}= a^{k}\cdot a^{l}$.
2. $a^{kl}= (a^{k})^{l}= (a^{l})^{k}$.

Now we want to define $a^{r}, \; r \in \mathbb{Q}$. Eg $a^{2/3}$. Note that if $r = k/l$ then we only have to define $a^{1/l}$, because then $a^{r}= (a^{1/l})^{k}$. Essentially, we want an answer to the equation $x^{l}= a$, for example $x^{2}= 2$. This equation has no solution in $\mathbb{Q}$.

We will see soon that an equation like $x^{2}= 2$, or more generally, $x^{l}= a$ has a unique solution in $\mathbb{R}^{+}$ (which we denote $\sqrt{2}$ and $a^{1/l}$.)

#### Lemma 24

For every $a \in \mathbb{R}$ with $a \geq-1$, and every $n \in \mathbb{N}$,

$$
(1 + a)^{n} \geq 1 + na.
$$

This is known as the Bernoulli inequality.

**Proof:** by induction. Base case $n = 1$ is trivial. Now for the induction step:

$$
\begin{align}
(1 + a)^{n + 1}& = (1 + a)\cdot (1 + a)^{n}\geq (1 + a)\cdot (1 + na)\\
& = 1 + (n + 1)a + na^{2}\\
& \geq 1 + (n + 1)a\\
&&\checkmark
\end{align}
$$