There are tree principles about convergent sequences that we care about:
1. Monotone and bounded implies convergence.
2. If a sequence is bounded, there exists a convergent subsequence.
3. Cauchy property $\Leftrightarrow$ convergent. Cauchy means $\forall \; \epsilon > 0 \; \exists \; N \in \mathbb{N}$ such that $\abs{a_{m}-a_{n}}< \epsilon$ for all $m, n \geq N$.

#### Theorem 35

Four every sequence $(a_{n})$ in  $\mathbb{R}$, the following are equivalent:
1. $(a_{n})$ is convergent.
2. $(a_{n})$ is Cauchy.

> [!proof]-
> 1 implies 2 by lemma 34. To see why 2 implies 1, assume $(a_{n})$ is Cauchy. Then $(a_{n})$ is bounded by lemma 34. Therefore there exists a convergent subsequence $(a_{n_{j}})$, say $\lim_{j \rightarrow \infty}a_{n_{j}}= a$.
> 
> Claim: $a_{n}\longrightarrow a$. Reason: $\forall \; \epsilon > 0 \; \exists \; n \in \mathbb{N}$ such that $\abs{a_{m}-a_{n}}< \epsilon/2\; \forall m, n \geq N$ (so $(a_{n})$ is Cauchy). Therefore $\exists j \in \mathbb{N}$ such that $n_{j}\geq N$ and $\abs{a_{n_{j}}-a}< \epsilon/2$ (so $a_{n_j}\rightarrow a$). Then, for all $n \geq N$,
> 
> $$
\abs{a_{n}-a} \leq \abs{a_{n}-a_{n_{j}}} + \abs{a_{n_{j}}-a} < \epsilon,
>$$ 
> i.e. $a_{n}\rightarrow a$.

Theorem 35 is great because it separates the tasks of deciding about convergence and finding the limit.

>[!examples]+  Example 36
>Define $(a_{n})\in \mathbb{R}$ as
>$$
\begin{align}
a_{1}& = 1\\
a_{n + 1} & = a_{n}+ \frac{(-1)^{n}}{n + 1}\qq{} \forall \; n \in \mathbb{N}.
\end{align}
>$$
>$a_{1}= 1, \; a_{2}= 1-\frac{1}{2}, \; a_{3}= 1-\frac{1}{2}+ \frac{1}{3}...$ so $a_{n}$ is **not** monotone. In fact,
>$$
a_{n} = \sum\limits_{j = 1}^{n}\frac{(-1)^{j + 1}}{j}.
>$$
>If $n > m$, then
>$$
\begin{align}
a_{n}-a_{m} & = \frac{(-1)^{m + 2}}{m + 1}+ \frac{(-1)^{m + 3}}{m + 2}+ \cdots \frac{(-1)^{n}}{n}\\[1em]
(-1)^{m}(a_{n}-a_{m}) & = \frac{1}{m + 1}-\frac{1}{m + 2}+ \cdots \frac{(-1)^{n-m + 1}}{n}< \frac{1}{m + 1}\\[1em]
-\frac{1}{n} &<(-1)^{m}(a_{n}-a_{m})< \frac{1}{m + 1}.
\end{align}
>$$
>This implies
>$$
\begin{align}
\abs{a_{n}-a_{m}}< \frac{1}{m + 1}< \epsilon \quad \forall \; m, m > \frac{1}{\epsilon}.
\end{align}
>$$
>This implies $(a_{n})$ Cauchy, and therefore convergent by Theorem 35. In other words,
>$$
\exists \; \lim_{n \rightarrow \infty}a_{n} = \sum\limits_{j = 1}^{\infty}\frac{(-1)^{j + 1}}{j}.
>$$

#### Remark 37

Some key observations about sequences in any ordered field $\mathbb{F}$:
1. LUB is valid in $\mathbb{F}$.
2. Every monotone bounded sequence in $\mathbb{F}$ is convergent.
3. The nested interval property holds in $\mathbb{F}$.
4. Every bounded sequence in $\mathbb{F}$ has a convergent subsequence.
5. Every Cauchy sequence in $\mathbb{F}$ is convergent.
6. Bonus: $\mathbb{F}= \mathbb{R}$. (In essence, "up to isomorphism").

In a sense, we can think of $\mathbb{R}$ as "complete". It is the unbroken number line. It can be shown that the six points above are actually all equivalent.

# Infinite Series

Let $(a_{n})$ be a sequence in $\mathbb{R}$. The (infinite) series $\sum\limits_{n = 1}^{\infty}a_{n}$ is simply the sequence

$$
\begin{align}
(s_{n}) & = (s_{1}, s_{2}s_{3}), ...\\[1em]
s_{1} & = a_{1}, \; s_{2} = a_{1}+ a_{2}, \; s_{3} = a_{1} + a_{2} + a_{3}, ... \\[1em]
s_{n} & = a_{1}+ \cdots a_{n} = \sum\limits_{j = 1}^{n}a_{j}.
\end{align}
$$

$s_{n}$ is referred to as the $n$-th partial sum. If $(s_{n})$ is convergent, then $\sum\limits_{n = 1}^{\infty}a_{n}$ *also* denotes $\lim_{n \rightarrow \infty}s_{n}$.

Note: The symbol $\sum\limits_{n = 1}^{\infty}a_{n}$ always has one meaning, namely $(s_{n})$. If $(s_{n})$ is convergent, *only then* does it have a second meaning, namely $\lim_{n \rightarrow \infty}\sum\limits_{j = 1}^{\infty}a_{j}$. This potential doable usage will not cause any confusion.

#### Remark 39

Philosophically, sequences and series are the same, in essence. Given any sequence $(a_{n})$, we can write it as the series $\sum\limits_{n = 1}b_{n}$, with $b_{1}= a_{1}$, $b_{n}= a_{n}-a_{n-1}\; \forall n \geq 2$. Conversely, every series is by definition the sequence partial sums. Still, it's good to have both concepts!

>[! Examples]+ Example 40
>1. $$\sum\limits_{n = 1}^{\infty}(-1)^{n + 1}= 1-1 + 1-1 + \cdots = \frac{1 + (-1)^{n + 1}}{2}.$$
>2.  Very important: Fix $a \in \mathbb{R}$, let $a^{0}= 1$. Consider $$\sum\limits_{n = 0}^{\infty}a^{n}= 1 + a + a^{2}+ a^{3}+ \cdots.$$ $$S_{n} = 1 + a + a^{2}+ \cdots + a^{n}.$$ If a = 1, $S_{n}= n + 1\rightarrow \infty$ so it is divergent. If $a \neq 1$, $$\begin{align}aS_{n} & = a + a^{2}+ \cdots + a^{n}+ a^{n + 1}\\ aS_{n}-S_{n}& = a^{n + 1}-1\\ S_{n} & = \frac{1}{1-a}+ \frac{a^{n + 1}}{a-1}.\end{align}$$ This is known as the *geometric series*. Here, $$\lim_{n \rightarrow \infty}S_{n}= \begin{cases}\frac{1}{1-a}\qq{for} & \abs{a}< 1 \\[1em] \text{DNE} \qq{for} & \abs{a}\geq 1 \end{cases}.$$
>3.  Also very important: $$S_{n} = \sum\limits_{n = 1}^{\infty}\frac{1}{n}.$$ This is known as the harmonic series. $(S_{n})$ is actually not bounded, and it is not convergent.
>4. Consider $$S_{n} = \sum\limits_{n = 1}^{\infty}\frac{1}{n^{2}}.$$ This series, unlike the harmonic series, is bounded and convergent. So what is its limit? This was an open problem for a long time, but it was solved in 1734 by L. Euler (who else).