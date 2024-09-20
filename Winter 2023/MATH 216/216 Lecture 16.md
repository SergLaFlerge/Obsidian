Recall that $\sum\limits_{n = 1}^{\infty}a_{n}$ converges absolutely if $\sum\limits_{n = 1}^{\infty}\abs{a}_{n}< \infty$. We combined the comparison lemma and the geometric series to make a test for absolute convergence for some $\sum\limits_{n = 1}^{\infty}a_{n}$.

If we take $\abs{a_{n}}$ and compare it to the $n$-th term of the geometric series $r^{n}$, we could interpret this in a few different ways. For example, $\sqrt[n]{\abs{a_{n}}}\approx r$. This is known as the *root test*. We could also compare $\abs{\frac{a_{n + 1}}{a_{n}}}\approx r$. This is known as the ratio test.

#### Theorem 49

Let $(a_{n})$ be a sequence in $\mathbb{R}$, and let $r:=\limsup_{n \rightarrow\infty}\sqrt[n]{\abs{a_{n}}}\in \set{0}\;\cup\; \mathbb{R}^{+}\; \cup \; \set{\infty}$.
1. If $0 \leq r < 1$, then the series $\sum\limits_{n = 1}^{\infty}a_{n}$ is absolutely convergent.
2. If $r > 1$, then $\sum\limits_{n = 1}^{\infty}$ is divergent.

>[!proof]-
>1. Note $r < \frac{r + 1}{2}< 1$. Therefore $\exists \; N \in \mathbb{N}$ such that $\sqrt[n]{\abs{a_{n}}}< \frac{r + 1}{2}\; \forall \; n \geq N$. Then $\abs{a_{n}}< \left(\frac{r + 1}{2} \right)^{n}\; \forall \; n \geq N$. $$\begin{align}\sum\limits_{n = 1}^{\infty}\abs{a_{n}} & = \sum\limits_{n = 1}^{N-1}\abs{a_{n}}+ \sum\limits_{n = N}^{\infty}\abs{a_{n}}< \infty \end{align}$$ so $\sum\limits_{n = 1}^{\infty}a_{n}$ is absolutely convergent.
>2. $r > \frac{r + 1}{2}> 1$. This implies $\sqrt[n]{\abs{a_{n}}}< \frac{r + 1}{2}$ for infinitely many $n \in \mathbb{N}$. Therefore $\exists \; n_{1}< n_{2}< n_{3}<...$ such that $\sqrt[n_{j}]{\abs{a_{n_{j}}}}> \frac{r + 1}{2}\; \forall \; j$. Therefore $\abs{a_{n_{j}}}> \left(\frac{r + 1}{2} \right)^{n_{j}}> 1 \; \forall \; j$. This implies $a_{n}$ does not approach $0$, and so the sum is divergent.

>[!examples]+ Example 50
>1. $a_{n}= \frac{1}{n!}$. We know that, for every $b \in \mathbb{R}, \; b > 1$, that $\frac{n!}{b_{n}}\rightarrow \infty$. Therefore $\exists \; N \in \mathbb{N}$ such that $\frac{n!}{b^{n}}\geq 1 \; \forall \; n \geq N$. Then, $\forall \; n \geq N$, $$0 \leq \sqrt[n]{\abs{a_{n}}}= \frac{1}{\sqrt[n]{n!}}\leq \frac{1}{\sqrt[n]{b^{n}}}= \frac{1}{b}$$ and $0 \leq \limsup \sqrt[n]{\abs{a_{n}}}\leq \frac{1}{b}$. So the series converges absolutely.
>2. For the harmonic series, the test is inconclusive, as we get an $r = 1$. The root test would not distinguish between $\frac{1}{n}$ and $\frac{1}{n^{2}}$, even though we know that the former diverges and the latter converges.

Often, it is easier to apply an alternative test:

#### Corollary 51

Let $(a_{n})$ be a sequence in $\mathbb{R}\smallsetminus \set{0}$, and sum that $r:= \lim_{n \rightarrow\infty}\abs{\frac{a_{n + 1}}{a_{n}}}$ exists.
1. If $0 \leq r < 1$, then $\sum\limits_{n = 1}^{\infty}a_{n}$ is absolutely convergent.
2. If $r > 1$, then $\sum\limits_{n = 1}^{\infty}$ is divergent.

Our final goal of this chapter is to further discuss the aspects of absolute convergence.

#### Definition 52

Let $(a_{n})$ and $(b_{n})$ with two sequences  in $\mathbb{R}$. The *Cauchy Product* of the series $\sum\limits_{n = 1}^{\infty}a_{n}$ and $\sum\limits_{n = 1}^{\infty}b_{n}$ is the series $\sum\limits_{n = 1}^{\infty}c_{n}$, where

$$
\begin{align}
c_{n} & = \sum\limits_{j = 1}^{\infty}a_{j}b_{n + 1-j}\\[1em]
& = \sum\limits_{i, j \in \mathbb{N},i + j = n + 1}a_{i}b_{j}= a_{1}b_{n}+ a_{2}b_{n-1}+... + a_{n-1}b_{n2}+ a_{n}+ b_{1}.
\end{align}
$$

>[!examples]+ Example 53
>Let $a_{n}= b_{n}= a^{n}, \; a \in \mathbb{R}$. Then $c_{n}= \sum\limits_{j = 1}^{n}a^{j}a^{n + 1-j}= a^{n + 1}\sum\limits_{j = 1}^{n}1 = na^{n + 1}$. Therefore the Cauchy product of $\sum\limits_{n = 1}^{\infty}a_{n}$ with itself is $\sum\limits_{n = 1}^{\infty}na^{n + 1}$.

The above example can be visualized as a lattice made up of the $i$-th and $j$-th components as $x$ and $y$ coordinates. But why would anyone come up with this definition?

To explain why, assume $\sum\limits_{n = 1}^{\infty}a_{n}$ and $\sum\limits_{n = 1}^{\infty}b_{n}$ both converge, and consider the following the (formal) expressions:

$$
\begin{align}
a_{1}+ a_{2}x + a_{3}x^{2}+... & = \sum\limits_{n = 1}^{\infty}a_{n}x^{n-1}\\[1em]
b_{1}+ b_{2}x + b_{3}x^{2} +... & = \sum\limits_{n = 1}^{\infty}b_{n}x^{n-1}.
\end{align}
$$

Consider $(a_{1}+ a_{2}x + a_{3}x^{2}+...)\cdot (b_{1}+ b_{2}x + b_{3}x^{2}+...)$ this can be expended as $a_{1}b_{1}+ x (a_{1}b_{2}+ a_{2}b_{1})+ x^{2}(a_{1}b_{3}+ a_{2}b_{2}+ a_{3}b_{1})+... = \sum\limits_{n = 1}^{\infty}c_{n}x^{n-1}$. Taking $x = 1$, we then obtain $\sum\limits{a_{n}}\cdot \sum\limits b_{n}= \sum\limits c_{n}$.

But, is this true? In general, no, but if the convergence of the sequences is absolute, then yes! So this already highlights a great fact about absolute convergence.

#### Theorem 54

Assume that the series of $(a_{n})$ and $(b_{n})$ both converge absolutely. Then the series that is the Cauchy product also converges absolutely, and the the sum of the Cauchy product is the product of the two series.

$$
\sum\limits_{n = 1}^{\infty}a_{n}\cdot \sum\limits_{n = 1}^{\infty}b_{n} =  \sum\limits_{n = 1}^{\infty}c_{n}.
$$

The proof is in the posted notes, but it provides nothing else for us.

>[! Examples]+ Example 53 Revisited
>$a_{n}=b_{n}= a^{n}$. Then
>$$
\begin{align}
\sum\limits_{n = 1}^{\infty}a_{n}& = \frac{a}{1-a}\quad \forall \; \abs{a}< 1\\[1em]
\left(\frac{a}{1-a} \right)^{2} & = \sum\limits_{n = 1}^{\infty}a_{n}\cdot \sum\limits_{n = 1}^{\infty}a_{n} = \sum\limits_{n = 1}^{\infty}c_{n} = \sum\limits_{n = 1}^{\infty}na^{n+1}\\[1em]
\sum\limits_{n = 1}^{\infty}na^{n}& = \frac{a}{(1-a)^{2}} \quad \forall \; \abs{a}< 1.
\end{align}
>$$
>This equality is not obvious!

Informally, Theorem 54 says that, as far as multiplication is concerned, infinite series behave like finite sums, provided that the series are absolutely convergent.

In a similar spirit, we consider one last aspect of finite sums versus infinite series — Does the order of summation matter?

#### Theorem 55

Let $(a_{n})$ be a sequence in $\mathbb{R}$. If this series converges absolutely, then, for every bijection $f:\mathbb{N}\rightarrow \mathbb{N}$, the series $\sum\limits_{n = 1}^{\infty}a_{f (n)}$ also converges absolutely and has the same value. In essence, if we were to "rearrange" the order of the terms, there would be no difference.

>[! Proof]-
>For convenience, let $a = \sum\limits_{n = 1}^{\infty}a_{n}$. Then $\forall \; \epsilon > 0, \; \exists \; n \in \mathbb{N}$ such that $\abs{\sum\limits_{n = 1}^{N_{1}}a_{n}-a}< \frac{\epsilon}{2}$, and $\sum\limits_{n = N_{1}}^{\infty}\abs{a_{n}}< \frac{\epsilon}{2}$ by absolute convergence. Consider $f^{-1}(\set{1, ..., N_{1}})\subset \mathbb{N}$, which is finite. Let $N_{2}\geq \max f^{-1}(\set{1, ..., N_{1}})$, i.e. $f (\set{1, ..., N_{2}})\supset \set{1, ..., N_{1}}$.
>$\forall \; n \geq N_{2}$, 
>$$
\abs{\sum\limits_{n = 1}^{N}a_{f (n)}-a}\leq \abs{\sum\limits_{n = 1}^{N}a_{f (n)}-\sum\limits_{n = 1}^{N_{1}}a_{n}}+ \underbrace{\abs{\sum\limits_{n = 1}^{N_{1}}a_{n}-a}}_{<\epsilon/2}
>$$