Recall that

$$
\sum\limits_{n = 0}^{\infty}a_{n} = (s_{1}, s_{2}, ...).
$$

#### Lemma 41

If $\sum\limits_{n = 1}^{\infty}a_{n}$ converges, then $a_{n}\rightarrow 0$.

> [!proof]-
> sum $\sum\limits_{n = 1}^{\infty}$ converges, implying that $(S_{n})$ is Cauchy. This implies $\forall \; \epsilon > 0 \; \exists \; n \in \mathbb{N}$ such that $\abs{S_{n}-S_{n-1}}< \epsilon \; \forall n \geq N$, i.e. $\abs{a_{n}}\rightarrow 0$.

Note: Lemma 41 is very simple, but equally crude, in the sense that its converse is *not* is true, i.e. $\sum\limits_{n = 1}^{\infty}a_{n}$ may diverge even though $a_{n}\rightarrow 0$. For example,

$$
\sum\limits_{n = 1}^{\infty}\frac{1}{n}
$$

is divergent, and yet $\frac{1}{n}\rightarrow 0$. More can be said if more information about $(a_{n})$ is available, e.g. if $(a_{n})$ or $(\abs{a_{n}})$ is monotone.

#### Theorem 42

Known as the alternating series test.

Assume $(a_{n})$ is monotone. Then the following are equivalent:
1. $\sum\limits_{n = 1}^{\infty}(-1)^{n + 1}a_{n}$ is convergent.
2. $a_{n}\rightarrow0$.

> [!proof]-
> We know$(1)\Rightarrow (2)$ always, by the previous lemma. To see that $(2)\Rightarrow (1)$, assume $a_{n}\rightarrow 0$. We then have two possibilities:
> 1. $a_{n}$ is decreasing to $0$, which implies $a_{n}\geq 0 \; \forall \; n \in \mathbb{N}$.
> 2. $a_{n}$ is increasing to $0$, in which case we consider $(-a_{n})$ and go back to $(1)$.
> The goal is to see that $(S_{n})$ is Cauchy.
> 
> $\forall \; \epsilon > 0 \; \exists \; N \in \mathbb{N}$ such that $0 \leq a_{n}< \epsilon\; \forall \; n \geq N$. For $n > m$,
> $$
\begin{align}
S_{n} & = a_{1}-a_{2}+ a_{3}... + (-1)^{n + 1}a_{n} \\
S_{n}-S_{m} & = (-1)^{m + 2}a_{m + 1}+... + (-1)^{n + 1}a_{n} \\
& = (-1)^{m}(a_{m + 1}-a_{m + 2}+ a_{m + 3}+... + (-1)^{n-m + 1}a_{n}) \\[1em]
(-1)^{m}(S_{n}-S_{m}) & = a_{m + 1}-a_{m + 2}+ a_{m + 3}-a_{m + 4}+... + (-1)^{n-m + 1}a_{n}. \\
\Rightarrow 0& \leq (-1)^{m}(S_{n}-S_{m})\leq a_{m + 1}\\[1em]
\abs{S_{n}-S_{m}}&\leq \abs{a_{m + 1}}\leq \epsilon
\end{align}
>$$

As an example,

$$
\begin{align}
&\sum\limits_{n = 1}^{\infty}\frac{(-1)^{n + 1}}{n} \\[1em]
a_{n}& = \frac{1}{n}\rightarrow 0 \\[1em]
&\Rightarrow \sum\limits_{n = 1}^{\infty}\frac{(-1)^{n + 1}}{n} \qq{convergent.}
\end{align}
$$

Fro our proof: $\abs{S_{n}-S_{m}}\leq \frac{1}{m + 1}\; \forall \; n > m$. As $n \rightarrow \infty$, $\abs{S-S_{m}}\leq \frac{1}{m + 1}$.

If $(a_{n})$ is monotone and $\sum\limits_{n = 1}^{\infty}a_{n}$ converges then $a_{n}\rightarrow 0$ and $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}$ also converges

#### Definition 44

A series $\sum\limits_{n = 1}^{\infty}a_{n}$ is *absolutely convergent* or *converges absolutely* if $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}$ is convergent. Otherwise written $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}< \infty$, the sequence of partial sums of $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}$ is bounded.

#### Lemma 45

If the series $\sum\limits_{n = 1}^{\infty}a_{n}$ is absolutely convergent then it is convergent.

> [!proof]-
> Assume the series converges absolutely. Then, $\forall \; \epsilon > 0 \;\exists\; n \in \mathbb{N}$ such that
> $$
\begin{align}
\abs{a_{m + 1}}+... + \abs{a_{n}} & < \epsilon \\[1em]
\abs{S_{n}-S_{m}} & = \abs{\sum\limits_{j = m + 1}^{\infty}a_{j}} \leq \sum\limits_{j = m + 1}^{\infty}\abs{a_{j}} < \epsilon.
\end{align}
>$$
>
>This implies $(S_{n})$ is Cauchy, and so  $\sum\limits_{n = 1}^{\infty}a_{n}$ is convergent.

Lemma 45 is simple and crude, with its converse not being true. Our previous example is not absolutely convergent.

> [!examples]+ Example 46
> Consider $\sum\limits_{n = 0}^{\infty}\abs{a^{n}}=\sum\limits_{n = 0}^{\infty}\abs{a}^{n}$, with $a \in \mathbb{R}$, and $\abs{a}< 1$. Let $a_{n}= a^{n}$. Then
> $$
\begin{align}
\sum\limits_{n = 0}^{\infty}\abs{a_{n}}& = \sum\limits_{n = 0}^{\infty}\abs{a}^{n} \\[1em]
& = \frac{1}{1-\abs{a}}.
\end{align}
>$$
>Therefore $\sum\limits_{n = 0}^{\infty}a^{n}$ is absolutely convergent $\forall \; \abs{a}< 1$.

#### Lemma 47

Let $(a_{n}), \; (b_{n})$ be sequences in $\mathbb{R}$, with $\abs{a_{n}}\leq b_{n}$. If $\sum\limits_{n = 1}^{\infty}b_{n}$ converges then $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}$ is absolutely convergent.

>[!proof]-
>The proof is rather obvious. The sequence of $\abs{a_{n}}$ is increasing and bounded, so if $\sum\limits_{n = 1}^{\infty}b_{n}$ is convergent, so is $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}$.

>[!examples]+ Example 48
>Consider $(S_{n})=\sum\limits_{n = 0}^{\infty}\frac{1}{n!}$, with $0! = 1$. $a_{n}= \frac{1}{n!}> 0$. Recall that $n! = n (n-1)\cdot... \cdot 2 \cdot 1 \geq 2^{n-1}$. Therefore
>$$
0 > a_{n}> \frac{1}{2^{n-1}}= \frac{2}{2^{n}}.
>$$
>We know that our second series is a geometric series, which converges to $4$. This implies that $\sum\limits_{n = 0}^{\infty}\frac{1}{n!}$ is absolutely convergent by Lemma 47.
>The question now is: What is its limit?

Recall that $(C_{n})$ with $c_{n}= \left(1 + \frac{1}{n}\right)^{n}\; \forall \; n \in \mathbb{N}$. $(c_{n})$ is strictly increasing and $c_{n}\rightarrow e$.

Let us compare $S_{n}$ and $(C_{n})$. We know that

$$
\begin{align}
C_{n} & = \left(1 + \frac{1}{n} \right) = \sum\limits_{j = 0}^{\infty}\binom{n}{j}\frac{1}{n^{j}} \\[1em]
& = 1 + 1 + \sum\limits_{j = 2}^{n}\frac{n}{n}\cdot \frac{n-1}{n}\cdots \frac{n-(j-1)}{n}\cdot \frac{1}{j!} \\[1em]
& = 1 + 1 + \left(1-\frac{1}{n} \right)\frac{1}{2!}+ \left(1-\frac{1}{ n} \right)\left(1-\frac{2}{n} \right)\frac{1}{3!}+... + \left(1-\frac{1}{n} \right)\left(1-\frac{2}{n} \right)\cdots \left(1-\frac{n-1}{n} \right)\frac{1}{n!}.
\end{align}
$$

Since every term is positive and less than $1$, we know that

$$
C_{n}\leq S_{n}.
$$

Fix any $l \in \mathbb{N}$:

$$
C_{n}\geq 1 + 1 +...+ \left(1-\frac{1}{n} \right)\cdots \left(1-\frac{l-1}{n} \right)\frac{1}{l!}.
$$

As $n \rightarrow\infty$,

$$
e \geq S_{l},
$$

and so by squeeze theorem,

$$
\lim_{n \rightarrow \infty}S_{n} = e
$$

This is great news, as $(S_{n})\rightarrow e$ extremely fast, and $e$ is a pretty important number. $(s_{n})$ also gives us something that $C_{n}$ can't: $e$ is irrational!

Suppose $e$ was rational, i.e.

$$
\begin{align}
e & = \frac{m}{l}.
\end{align}
$$

We know $2 < e < 3$. But now we know that

$$
\begin{align}
e = \frac{m}{l} & = \sum\limits_{n = 0}^{\infty}\frac{1}{n!} = 1 + 1 +... + \frac{1}{l!}+ \sum\limits_{l + 1}^{\infty}\frac{1}{n!} \\[1em]
m (l-1)! & = l! + \frac{l!}{1}+ \frac{l!}{2!}+... + \frac{l!}{l!} + \sum\limits_{n = l + 1}^{\infty}\frac{l!}{n!},
\end{align}
$$

which implies $c \in \mathbb{N}$ for $c = \sum\limits_{n = l + 1}^{\infty}\frac{l!}{n!}$. $c$ is then a geometric series, and

$$
c = \frac{1}{l + 1-1} = \frac{1}{l}
$$

which is a contradiction. It turns out that $e$ is not only irrational, but also **transcendental**. (C. Hermite, 1873). Proving this is way beyond our introductory analysis.