Let $(a_{n})$ be a sequence in $\mathbb{R}$. Set $S [a_{n}]= \{a \in \mathbb{R}\cup \{-\infty, \infty \} \}$. Then $\exists$ a subsequence $(a_{n_{j}})$ of $(a_{n})$ such that $a_{n_{j}}\rightarrow a$.

> [!examples]+ Example
> $a_{n}= \frac{1}{n}$. Then $S [\frac{1}{n}]= \{0\}$ for all $j \in \mathbb{N}, \; n_{j}\geq j$. So $\frac{1}{n_{j}}\leq \frac{1}{j}$, and so $\lim_{j \rightarrow \infty}S [a_{n}]= 0$.

#### Lemma 26

If$(a_{n})$ converges to $a \in \mathbb{R}$, then $S [a_{n}]= \{a\}$

> [!proof]-
>  Let $\epsilon > 0$. Then there is $N \in \mathbb{N}$ such that $\abs{a_{n}-a}< \epsilon \; \forall \; n \geq{N}$. Let $(a_{n_{j}})$ be a subsequence of $(a_{n})$. Let $j \geq N$, then $n_{j}\geq j \geq N$, i.e. $\abs{a_{n_{j}}-a}< \epsilon$ for $j \geq{N}$, i.e. $$\lim_{j \rightarrow \infty}a_{n_{j}}= a.$$

> [!examples]+ Example
> Let $a_{n}= (-1)^{n}$.
> Let $n_{j}= 2j$, then $a_{n_{j}}= 1$, so $\lim_{j \rightarrow \infty}a_{n_{j}}= 1$.
> Let $n_{j}= 2j + 1$, then $a_{n_{j}} =-1$, so $\lim_{j \rightarrow \infty}a_{n_{j}}=-1$.
> So $\{-1, 1\}\subset S [(-1)^{n}]$.
> Now, let $a \in \mathbb{R}, \; \abs{a}\neq 1$. Assume that there is a subsequence $a_{n_{j}}$ such that $a_{n_{j}}\rightarrow a$. Then $\abs{a_{n_{j}}-a}= \abs{(-1)^{n_{j}}-a}\geq \min \{\abs{1 + a}, \abs{1-a} \}> 0$. This last separable is independent of $j$, so $a_{n_{j}}\cancel{\rightarrow}a$. 

> [!examples]+ Example
> Let $(a_{n})$ be increasing and unbounded. Then $S [a_{n}]= \{\infty \}$. Let $C > 0$. Then there is $N \in \mathbb{N}$ such that $a_{n}\geq C\; \forall \; n \geq N$. Let $(a_{n_{j}})$ be a subsequence of $(a_{n})$. For $j \geq N:\; a_{n_{j}}\geq a_{j}\geq C$ so $\lim_{j \rightarrow \infty}A_{n_{j}}= \infty$.

#### Lemma 28

Every sequence $(a_{n})$ has a monotone subsequence.

> [!proof]-
> We say that $l \in \mathbb{N}$ is a *peak*  for $(a_{n})$ if $a_{n}< a_{l}\; \forall n > l$.
> Set $A:= \{l \in \mathbb{N}\mid l\; \text{is a peak for}\; (a_{n}) \}$. There are two cases:
> 1. $A$ is finite. Set $n = \max A$. Let $n_{1}> n$. Then $n_{1}$ is not a peak for $(a_{n})$. This implies $\exists\; n_{2}> n_{1}$ such that $a_{n_{2}}> a_{n_{1}}$. Then $n_{2}$ is not a peak. So we obtain in increasing subsequence of $(a_{n})$.
> 2. $A$ is infinite. Pick $n_{1}< n_{2}<... \in A$. Then $a_{n_{1}}< a_{n_{2}}<...$ so $(a_{n_{j}})$ is a decreasing subsequence of $(a_{n})$.

#### Theorem 29

Every bounded sequence in $\mathbb{R}$ has a convergent subsequence.

#### Lemma 30

Let $(a_{n})$ be a sequence in $\mathbb{R}$. Then
1. $S [a_{n}]\neq \varnothing$.
2. $S [a_{n}]\subset \mathbb{R}$ if and only if $(a_{n})$ is bounded.
3. $S[a_{n}]= \{a\}$ for some $a \in \mathbb{R}\cup \{-\infty, \infty \}$ if and only if $\lim_{n \rightarrow \infty}a_{n}= a$.

> [!proof]-
> 1. Suppose that $(a_{n})$ is bounded. Then $S [a_{n}]\neq \varnothing$ by  Theorem 29. Suppose that $(a_{n})$ is not bounded above. Then there is $n_{1}\in \mathbb{N}$ such that $a_{n_{1}} \geq 1$. Then there is $n_{2}> n_{1}$ such that $a_{n_{2}}\geq 2$. Continuing this way, we obtain a subsequence $(a_{n_{j}})$ such that $a_{n_{j}}\geq j$. So $\lim_{j \rightarrow \infty}a_{n_{j}}= \infty\in S [a_{n}]$. Similarly, if $(a_{n})$ is not bounded, then $-\infty \in S [a_{n}]$.
> 2. Let $(a_{n})$ be bounded, i.e. there is $C \geq 0$ such that $\abs{a_{n}}\leq C\; \forall \; n \in \mathbb{N}$. Let $(a_{n_{j}})$ be a subsequence of $(a_{n})$ such that $a_{n_{j}}\rightarrow a$. This implies $\abs{a}\leq C$, so $S [a_{n}]\subset [-C, C]\subset \mathbb{R}$. Conversely, suppose that $(a_{n})$ is not bounded. WLOG, $(a_{n})$ is not bounded above. As for $1.$, we find a subsequence $(a_{n_{j}})$ of $(a_{n})$ such that $a_{n_{j}}\rightarrow \infty\in S [a_{n}]\smallsetminus \mathbb{R}$.
> 3. Suppose that $a_{n}\rightarrow a \in \mathbb{R}$. Then $S [1_{n}]= \{a \}$ by Lemma 26. If $a_{n}\rightarrow \infty$, then $a_{n_{j}}\rightarrow \infty$ for every subsequence $(a_{n_{j}})$ of $(a_{n})$ so that $S [1_{n}]=\{\infty\}$. Similarly for $a_{n}\rightarrow-\infty$. Conversely, suppose that $S [a_{n}]= \{0 \}$ for some $a \in \mathbb{R}\cup \{-\infty, \infty\}$. First, suppose that $(a_{n})$ is bounded. By $2.$,  $a \in \mathbb{R}$ . Assume that $a_{n}\cancel{\rightarrow}a$, i.e. there is $\epsilon_{0}> 0$ such that for every $j \in \mathbb{N}$, there is $n_{j}\geq j$ such that $\abs{a_{n_{j}}-a}\geq \epsilon_{0}$. WLOG: $n_{1}< n_{2}< n_{3}<...$ Then $a_{n_{j}}\cancel{\rightarrow}a$, which is a contradiction. All in all, $\lim_{n \rightarrow \infty}a_{n}= a$. Similarly for $a = \pm \infty$.

We can extend the order of $\mathbb{R}$ to $\mathbb{R}\cup \{-\infty, \infty\}$ by setting $-\infty < 0 < \infty\; \forall \; a \in \mathbb{R}$. So, every subset of $\mathbb{R}\cup \{-\infty, \infty\}$ has both a lower and an upper bound, and therefore a supremum and infimum.

#### Definition 31

For every sequence $(a_{n})\in \mathbb{R}$ set

$$
\begin{align}
\limsup_{n \rightarrow \infty}a_{n} :& = \sup S [a_{n}], \\
\liminf_{n \rightarrow \infty} a_{n} :& = \inf S[a_{n}].
\end{align}
$$

It is clear that

$$
\limsup_{n \rightarrow \infty} a_{n} \geq \liminf_{n \rightarrow \infty} a_{n},
$$

with equality holding if and only if the limit exists, i.e. if

$$
a = \lim_{n \rightarrow \infty}a_{n}.
$$

> [!examples]+ Example 32
> 1. $a_{n}= \frac{1}{n}$, $\limsup a_{n}= \liminf a_{n} = 0$. Here the limit exists.
> 2. $a_{n}= (-1)^{n}$, $\limsup a_{n}= 1, \; \liminf a_{n}=-1$, so the limit does not exist.
> 3. $a_{n}= (-1)^{n + 1}n$. So $(a_{n})= \{1,-2, 3, -4, ...\}$ . As $(a_{n})$ has no bounded subsequence, $S [a_{n}]\subset \{-\infty, \infty\}$ and $\limsup a_{2n}=-\infty$ and $\liminf a_{2n + 1}= \infty$. So $S [a_{n}] = \{-\infty, \infty\}$.


Question: Let $a_{n} = 1 + \frac{1}{2}+ \frac{1}{3}+... + \frac{1}{n}$. Is this convergent to some $a \in \mathbb{R}$?

#### Definition 33

A sequence $(a_{n})\in \mathbb{R}$ is called a *Cauchy sequence* if, for each $\epsilon > 0$, there is $N \in \mathbb{N}$ such that $\abs{a_{n}-a_{m}}< \epsilon\; \forall \; n, m \geq N$.

#### Lemma 34

Let $(a_{n})$ be a sequence in $\mathbb{R}$.
1. If $(a_{n})$ is convergent, then it is Cauchy.
2. If $(a_{n})$ is Cauchy, then it is bounded.

> [!proof]-
>  We prove 2 first. There is $N \in \mathbb{N}$ such that $\abs{a_{n}-a_{m}}< 2023$ for all $n, m \geq N$. This implies for all $n \geq N$ that $\abs{a_{m}}\leq \abs{a_{n}-a_{N}}+\abs{a_{N}}< 2023+ \abs{a_{N}}$. Set $C:= \max \{\abs{a_{1}}, ..., \abs{a_{N-1}}, 2023 + \abs{a_{N}} \}$. Then $\abs{a_{n}}\leq C \; \forall \; n \in \mathbb{N}$.
>  
>  To prove 1, let $a = \lim_{n \rightarrow \infty}a_{n}$. Let $\epsilon> 0$. Then there is $N \in \mathbb{N}$ such that $\abs{a_{n}-a}< \frac{\epsilon}{666}$ for all $n, m \geq N$. For $n, m \geq M$, $\abs{a_{n}-a_{m}}< \abs{a_{n}-a}< \frac{\epsilon}{666}$.

