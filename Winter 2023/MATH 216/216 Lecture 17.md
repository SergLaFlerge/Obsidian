Assuming we have a series such that $\sum\limits_{n = 1}^{\infty}\abs{a_{n}}< \infty$, we now know that if we permute the series, then

$$
\sum\limits_{n = 1}^{\infty}a_{n} = \sum\limits_{n = 1}^{\infty}a_{f (n)}
$$

for any bijection $f:\; \mathbb{N}\rightarrow \mathbb{N}$.

#### Theorem 56

Let $(a_{n})$ be a sequence in $\mathbb{R}$. Assume the series converges, but is not absolutely convergent. Then, given $s \in \mathbb{R}\;\cup\; \set{-\infty, \infty}$, there exists a bijection $f:\; \mathbb{N}\rightarrow \mathbb{N}$ such that $\sum\limits_{n = 1}^{\infty}a_{f (n)}= s$. This theorem is known as the **Riemann Rearrangement Theorem**.

>[!proof]-
>We only outline the basic idea (for full details, see other resources).
> We split $\mathbb{N}$ into two disjoint sets $A^{+}$ and $A^{-}$. $A^{+} = \set{n \in \mathbb{N}\mid a_{n}\geq 0}$ and $n_{1}^{+}< n_{2}+ <...$. Same for $A^{-}$. Both subsets are non-empty. For this proof, we need two observations:
> 1. $A^{+}, \; A^{-}$ are both infinite (Otherwise the series would converge absolutely) and $\sum\limits_{j = 1}^{\infty}a_{n^{+}_{j}}= \sum\limits_{j = 1}^{\infty}-a_{n^{-}_{j}}= \infty$ (otherwise the series would again converge absolutely, or not at all).
> 2. $a_{n}\rightarrow 0 \implies a_{n_{j}}^{+}, \; a_{n_{j}}^{-}\rightarrow 0$ as $j \rightarrow \infty$.
> 
> Now we proceed as follows. For $s \in \mathbb{R}$, we start adding $a_{n_{j}}^{+}$ until we surpass $s$ for the first time. Call $a_{n_{k}}^{+}$ the first term to pass $s$. Now we reverse direction and add negative terms $a_{n_{j}}^{-}$ until we once again pass $s$. Call $a_{n_{l}}^{-}$ the first term to do so. Continuing this way, we eventually get arbitrarily close to $s$ while using every entry of $(a_{n})$ only once (and hence we have constructed a bijection of $\mathbb{N}$). The turn-around points converge to $s$ therefore the rearranged series converges to $s$.

>[! Examples]+ Example 57
> Consider our old friend $\sum\limits_{n = 1}^{\infty}\frac{(-1)^{n+ 1}}{n}$, which converges, but no absolutely.
> 
>Call $a:= \sum\limits_{n = 1}^{\infty}\frac{(-1)^{n + 1}}{n}= 1-\frac{1}{2}+ \frac{1}{3}-...\approx 0.6932$. Let us rearrange so that $b:= 1 + \frac{1}{3}-\frac{1}{2}+ \frac{1}{5}+\frac{1}{7}-\frac{1}{4}+... \approx 1.040$. We will see later that $b = \frac{3}{2}a$, once we have more knowledge. The important message is that series that are convergent but not absolutely convergent behave very differently than finite sums.

This concludes our big chapter on series. They shall make a comeback, but more as tools rather than objects of study.

# Continuity of Real Functions

Recall the general concept of a function:

$$
f:
\begin{cases}
A & \rightarrow B \\
a & \mapsto f (a)
\end{cases},
$$

or just $f:\; A \rightarrow B$, with $A, B\neq \varnothing$. From now on, $A, B \subset \mathbb{R}$, and typically we will write $f:\; D \rightarrow \mathbb{R}$, with $B \subset \mathbb{R}$ and $D\neq \varnothing$.

We can get a "feel" for a function $f$ by considering its *graph*. A graph $f$ is a set of ordered pairs such that $\text{graph}\; f = \set{(x, f (x))\mid x \in D}$.

<br>
<br>

Try to draw one later

<br>
<br>

## A Few Geometric (Topological) Properties of Subsets of $\mathbb{R}$

We will study a few properties of sets $A \subset \mathbb{R}$, which later on will be the domains of functions, or particle parts thereof.

### 1: Openness/Closeness

A set is 
1. Open if, for every $x \in A, \; \exists \; \epsilon > 0$ such that $\comm{x -\epsilon}{x + \epsilon}\subset A$.
2. Closed if $\mathbb{R}\smallsetminus A$ is open.
3. Compact if it is closed and bounded.

By convention, $\varnothing, \mathbb{R}$ are both open and closed.

>[! Examples]+ Example 2
>$A =]0, 1[$. Given any $x \in A$, let $\epsilon = \frac{1}{2}\min \set{x, 1-x}> 0$. Then
>$$
\begin{align}
x-\epsilon & \geq x-\frac{x}{2}= \frac{x}{2}< 0 \\[1em]
x + \epsilon & \geq x + \frac{1-x}{2}< 1
\end{align}
>$$
>Therefore $A$ is open. The complement is then not open, as $\mathbb{R}\smallsetminus A =]-\infty, 0]\; \cup \;[1, \infty[$.
>
>$B =[0, 1]$. $\mathbb{R}\smallsetminus B=]-\infty, 0[\; \cup \;]1, \infty[$ which is open. Therefore $B$ is closed.
>
>$C =[0, 1[$ is half-open, since $\comm{0-\epsilon}{0 + \epsilon}\cancel{\subset}C$, implying $C$ is not open, but $1 \in \mathbb{R}\smallsetminus C$, so it is not closed either.
>
>$D =\mathbb{Q}$ is not open: $\forall \; x \in D, \; \epsilon > 0$, $\comm{x-\epsilon}{x + \epsilon}\; \cap \; (\mathbb{R}\smallsetminus D)\neq \varnothing$. By the same logic, $\mathbb{R}\smallsetminus D$ is not closed.

#### Lemma 3

Let $I \neq \varnothing$ and for every $i \in I$ let $A_{i}\subset \mathbb{R}$.
1. If $A_{i}$ is open for every $i$, then $A_{i} \cap A_{j}$ is open $\forall \; i, j \in I$, and $\bigcup_{i \in I}A_{i}:= \set{x \in \mathbb{R}\mid x \in A_{i}\; \text{for some}\; i \in I}$ is open.
2. If $A_{i}$ is closed $\forall\; i \in I$, then $A_{i}\cup A_{j}$ is closed $\forall \; i, j \in I$, and $\bigcap_{i \in I}A_{i}:= \set{x \in \mathbb{R}\mid x \in A_{i}\; \text{for all}\; i \in I}$ is closed.

>[! Proof]-
>1. For $A_{i}, A_{j}$ open, pick $x \in A_{i}\cap A_{j}$. Then  $x \in A_{i}$, $\exists\; \epsilon_{1}> 0$ such that $\comm{x-\epsilon_{1}}{x + \epsilon_{1}}\subset A_{i}$ and $x\in A_{j}$, $\exists \epsilon_{2}> 0$ such that $\comm{x-\epsilon_{2}}{x + \epsilon_{2}}\subset A_{j}$ with $\epsilon:= \min \set{\epsilon_{1}, \epsilon_{2}}> 0$. Pick any $x \in \bigcup_{i \in I}$. Clearly $\comm{x-\epsilon}{x + \epsilon}\subset A_{i}\cap A_{j}$. Therefore $\exists\; i_{0}\in I$ such that $x \in A_{j}$, which implies $\exists \; \epsilon > 0$ such that $\comm{x-\epsilon}{x + \epsilon}\subset A_{i_{0}}\subset \bigcup_{i \in I}A_{i}$. Therefore $\bigcup_{i \in I}A_{i}$ is open.
>2. Continued.

Take any $A \subset \mathbb{R}, \; A \neq \varnothing$. Then,
- $A^{\circ} = \bigcup_{V \subset A}V \subset A$, with $V$ open, is the largest open set $A$, called the *interior* of $A$.
- $\bar{A} = \bigcap_{W \supset A}W \supset A$, with $W$ closed, is the smallest closed set $\supset A$, called the *closure* of $A$.