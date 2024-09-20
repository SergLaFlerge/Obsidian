Say we have our standard set-up: $D \subset \mathbb{R}\qc f:D \rightarrow \mathbb{R}$ continuous.

If $D$ is compact,
- $f (D)$ is also compact (proved last week, Theorem 20).
- $f$ is *uniformly* continuous (should be Theorem 23).

If $D$ is an interval,
- $f (D)$ is an interval (should be Theorem 24).
- If $f$ is 1-1, then $f^{-1}:f (D)\rightarrow \mathbb{R}$ is continuous. (Should be Theorem 28).

#### Corollary 21

For $D \subset \mathbb{R}\qc f:D \rightarrow \mathbb{R}$ continuous, if $D$ is compact, then $f$ attains a minimum and maximum on $D$, i.e. $\exists \; a, b \in D$ such that $f (a)\leq f (x)\leq f (b)\; \forall \; x \in D$.

>[! Proof]-
>$f (D)$ is compact by Theorem 20. This implies that $f (D)$ has a minimum and maximum by Lemma 8.
>Let $c = \min f (D)$, $d = \max f (D)$. Then $\exists \; a, b \in D$ such that $f (a)= c$, $f (b)= d$, and $c \leq f (x)\leq d \; \forall \; x \in D$.

Note that Corollary 21 has 3 assumptions:
- $D$ is closed.
- $D$ is bounded.
- $f:D \rightarrow \mathbb{R}$ is continuous.

*All* three assumptions are essential. If $D$ was open, then we could not attain a maximum or minimum. If $D = \mathbb{R}$, then $D$ is closed, but a function like $f (x)= \frac{x \abs{x}}{1 + x^{2}}$, while continuous, does not attain a maximum or minimum. We could even make $D =[0, 1]$, which is compact, and have a non-continuous function. Therefore, all three assumptions are needed in order for Corollary 21 to be valid.

Recall that "$f:D \rightarrow \mathbb{R}$ continuous" means $\forall can \; \epsilon > 0$ and $\forall \; x \in D$, $\exists \; \delta= \delta (\epsilon, x)$ such that $x, y \in D$, $\abs{x-y}< \delta$ implies $\abs{f (x)-f (y)}< \epsilon$.

Note that in general $\delta$ may depend on $\epsilon$ *and* x! For example $D = \mathbb{R}^{+}$ and $f (x)= \frac{1}{x}$. In this domain, $f (x)$ is in fact continuous. Suppose that $\delta$ was independent of $x$, i.e. $\delta (\epsilon)< 1$. Consider $x = \delta, \; y = \frac{\delta}{2}$. Then

$$
\begin{align}
\abs{x-y} = \frac{\delta}{2}< \delta \\[1em]
\abs{f (x)-f (y)} = \abs{\frac{1}{\delta}-\frac{2}{\delta}} = \frac{1}{\delta}> 1
\end{align}
$$

for $\epsilon < 1$. Therefore $\delta$ *must* depend on $x$!

#### Definition 22

Let $D \subset \mathbb{R}$. A function $f:D \rightarrow \mathbb{R}$ is *uniformly continuous* if $\forall \; \epsilon > 0$, $\exists \; \delta > 0$ such that $x, y \in D, \; \abs{x-y}< \delta$ implies $\abs{f (x)-f (y)}< \epsilon$, i.e. $\delta$ is *independent* of $x$.

Clearly, if $f:D \rightarrow \mathbb{R}$ is uniformly continuous then $f$ is continuous. However, as the example above shows, the converse is generally *not* true.

A silver lining is that if $D$ is compact, then $f$ is automatically uniformly continuous.

#### Theorem 23

Let $D \subset \mathbb{R}\qc f:D \rightarrow \mathbb{R}$ continuous. If $D$ is compact then $f$ is uniformly continuous.

>[! Proof]-
>Suppose $f$ was not uniformly continuous. This implies $\exists \; \epsilon_{0}> 0$. $\forall \; n \in \mathbb{N}, \; \exists x_{n}, y_{n}\in D$ such that $\abs{x_{n}-y_{n}}< \frac{1}{n}$ but $\abs{f (x)-f (y)}> 3\epsilon_{0}$.
>
>$D$ compact implies $\exists$ subsequences $x_{n_{j}}, y_{n_{j}}$ such that $x_{n_{j}}\rightarrow x \in D$ and $y_{n_{j}}\rightarrow y \in D$. 
>
>$f$ continuous implies $\exists \; N \in \mathbb{N}$ such that $\abs{f (x_{n_{j}})-f (x)}< \epsilon_{0}$ and $\abs{f (y_{n_{j}})-f (y)< \epsilon_{0}}$ for all $j \geq N$. Then
>$$
\begin{align}
3 \epsilon_{0} & \leq \abs{f (x_{n_{j}})-f (y_{n_{j}})} \leq \underbrace{\abs{f (x_{n_{j}})-f (x)}}_{< \epsilon_{0}} + \abs{f (x)-f (y)} + \underbrace{\abs{f (y)-f (y_{n_{j}})}}_{< \epsilon_{0}}
\end{align}
>$$
>
>Which implies $\abs{f (x)-f (y)}> 3 \epsilon_{0}-2 \epsilon_{0}= \epsilon_{0}> 0$, but $\abs{x_{n_{j}}-y_{n_{j}}}< \frac{1}{n_{j}\rightarrow 0}$. Therefore
>$$
\abs{x-y} \leq \underbrace{\abs{x-x_{n_{j}}}}_{\rightarrow 0}+ \underbrace{\abs{x_{n_{j}}-y_{n_{j}}}}_{\rightarrow 0} + \underbrace{\abs{y_{n_{j}}-y}}_{\rightarrow 0},
>$$
>
>which implies $x = y$, but $f (x)\neq f (y)$, so $f$ *must* be continuous.

Now, we study the case of $D$ being an *interval*.

Note that $D \subset \mathbb{R}$ is an interval $\Longleftrightarrow$ $\forall \; c, d \in D, \; c < d:\qc [c, d]\subset D$.

#### Theorem 24

For $D \subset \mathbb{R}\qc f:D \rightarrow \mathbb{R}$ continuous.

If $D$ is on an interval then $f (D)$ is on an interval. Why is Theorem 24 plausible?

>[! Proof]-
>Strategy: Given any $c, d \in f (D)$ with $c \leq d$, we must show that $[c, d]\subset f (D)$. Pick $c, d \in f (D)$ with $c < d$. Therefore $\exists \; a, b \in D$ such that $f (a)= c$ and $f (b)= d$. Assume WLOG that $a < b$. Since $D$ is an interval, $[a, b]\subset D$ is an interval. The goal from here: Given $c < z < d$, we want to find $y \in[a, b]$ such that $f (y)= z$.
>Consider $f (\frac{a + b}{2})= f (w)$. Then $f (w)\geq z$ or $f (w)< z$. If $f (w)< z$, we consider the right half of $[a, b]$. If $f (w)\geq z$, we have the left half of $[a, b]$. We rinse and repeat. This is known as the bisection method/bisection algorithm.
>
> Let $a_{1}= a$ and $b_{1}=b$, and for $n \in \mathbb{N}$ define
> $$
\begin{align}
a_{n + 1} & =
\begin{cases}
a_{n} \qc &f (w_{n}) \geq z \\
\frac{a_{n}+ b_{n}}{2}\qc &f (w_{n})< z
\end{cases} \\[1em]
b_{n + 1}& =
\begin{cases}
\frac{a_{n}+ b_{n}}{2} \qc &f (w_{n})\geq z \\
b_{n} \qc &f (w_{n}) < z
\end{cases}
\end{align}
>$$
>for $w_{n}= \frac{a_{n}b_{n}}{2}$.
>
>We obtain two sequences $(a_{n}), (b_{n})$. By induction $(a_{n})$ is increasing and $(b_{n})$ is decreasing. $a_{n}< b_{n}$, and $b_{n}-a_{n}= \frac{b-a}{2^{n-1}}$.
>
>Let $I_{n}=[a_{n}, b_{n}]$. The length of $I_{n}= \frac{b-a}{2^{n-1}}\rightarrow 0$. We obtain a sequence $(I_{n})$ of nested closed intervals. We know $\bigcap_{n \in \mathbb{N}}I_{n}\neq \varnothing$ by Theorem 20 of section 3. In fact, $\bigcap_{n \in \mathbb{N}I_{n}}= \set{y}$ for some $y \in[a, b]$ because length of $I_{n}\rightarrow 0$. This implies $a_{n}\rightarrow y$ *and* $b_{n} \rightarrow y$. Remembering that $f (b_{n}\geq z)$ and $f (a_{n}< z)$ for all $n \in \mathbb{N}$, we then get that $f (b_{n})\rightarrow f (y)\implies f (y)\geq z$ and $f (a_{n})\rightarrow f (y)\implies f (y)\leq z$. Therefore $f (y)= z$ and we have what we came for :).

#### Corollary 25

Let $D \subset \mathbb{R}$ and $f:D \rightarrow \mathbb{R}$ continuous. If $[a, b]\subset D$ with $a \leq b$ then $f$ attains every value between $f (a)$ and $f (b)$, i.e. $\forall \; z \in \mathbb{R}$ with $\min \set{f (a), f (b)}\leq z\leq \max\set{f (a), f (b)}, \; \exists \; c \in[a, b]$ such that $f (c)= z$.

>[! Proof]-
>This is obvious, because $f ([a, b])$ is an interval by Theorem 24 and therefore contains $f (a)$ and $f (b)$.

#### Corollary 26

Let $a < b$ and $f:[a, b]\rightarrow \mathbb{R}$ continuous. If $f (a)f (b)\leq 0$ then $f (c)$ for sum $c \in[a, b]$.

>[! Proof]-
>Also obvious, since $f ([a, b])$ is an interval, and $0 \in f ([a, b])$.

To prepare for our last theorem about continuous functions, we will call $f:D \rightarrow \mathbb{R}$ *strictly increasing* if $x < y, \; x, y \in D$ implies $f (x)< f (y)$. $f:D \rightarrow \mathbb{R}$ is *strictly decreasing* if $x < y \;, x, y \in D$ implies $f (x)> f (y)$. We will also call $f:D \rightarrow \mathbb{R}$ *strictly monotone* if it is either of the above.

#### Proposition 27

Let $D \subset \mathbb{R}$ be an interval. For every continuous $f:D \rightarrow \mathbb{R}$, the following are equivalent:
1. $f$ is strictly monotone.
2. $f$ is 1-1.

$1 \Rightarrow 2$ is pretty obvious, it is the other direction that is the more interesting.