Let's start with $f:D \rightarrow \mathbb{R}$ with $D$ an interval. A $C^{1}$ function, also known as continuously differentiable function implies $f':D \rightarrow \mathbb{R}$ is also continuous. A smooth function is then $C^{\infty}$. Let us see some examples.

>[! Examples]+ Example 7
>Recall that $\exp:\mathbb{R}\rightarrow \mathbb{R}^{+}$ is continuous, and strictly increasing. Fix $a \in \mathbb{R}$. Then
>
>$$
\begin{align}
\exp (x) -\exp (a) & = \sum\limits_{n = 1}^{\infty}\frac{x^{n}-a^{n}}{n!}
\end{align}
>$$
>
>Recall from example 3 that, $\forall \; 0 < \abs{x-a}\leq 1$,
>
>$$
\begin{align}
\abs{\frac{x^{n}-a^{n}}{x-a}}\leq \abs{x-a}(1 + \abs{a})^{n}.
\end{align}
>$$
>
>Then, for $0 < \abs{x-a}\leq 1$,
>
>$$
\begin{align}
\frac{\exp (x)-\exp (a)}{x-a} -\sum\limits_{n = 1}^{\infty}\frac{na^{n-1}}{n!} & = \sum\limits_{n = 1}^{\infty}\left(\frac{x^{n}-a^{n}}{x-a}-na^{n-1} \right) \frac{1}{n!} \\[1 em]
\abs{\frac{\exp (x)-\exp (a)}{x-a}-\exp (a)} & \leq \sum\limits_{n = 1}^{\infty}\abs{x-a}\frac{(1 + \abs{a})^{n}}{n!} \\[1 em]
& = \leq \abs{x-a}\exp (1 + \abs{a}) \\[1em]
\lim_{x \rightarrow a} & = \frac{e^{x}-e^{a}}{x-a} = e^{a}
\end{align}
>$$
>
> And so $\exp$ is $C^{\infty}$.

>[! Examples]+ Example 8
>Now we look at the inverse of $\exp$, $\log (x)$. We know that $\log$ is continuous and strictly increasing. Since $\exp' (a)= \exp (a)\neq 0$, by Corollary 6,
>
>$$
\begin{align}
\log' (e^{a)}= \frac{1}{\exp' (a)} \\[1 em]
\frac{1}{\exp (a)},
\end{align}
>$$
>
>and therefore $\log' (x) = \frac{1}{x}\; \forall \; x \in \mathbb{R}^{+}$.
>By induction, $\log^{(n)}(x)= (-1)^{n+ 1}\frac{(n-1)!}{x^{n}}$.

>[! Examples]+ Example 9
>1. $f (x)= x^{a}= e^{a \log{x}}\implies f$ is $C^{\infty}$. $f' (x)= e^{a \log x}\cdot a \cdot \frac{1}{x}= ax^{a-1}$ 
>2. $g (x)= a^{x}, \; a \in \mathbb{R}^{+}$, $g (x)= e^{x \log a}\implies f$ is $C^{\infty}$. $g' (x)= e^{x \log{a}}\cdot \log{a}= a^{x}\log{a}$.

## Facts About Differentiable Functions

We want to use $f'$ to understand the local behaviors of a differentiable function $f:D \rightarrow \mathbb{R}$.

We say that $f:D \rightarrow \mathbb{R}$ *attains a local maximum (or  minimum)* at $a \in D$ if $\exists \; \epsilon > 0$ such that $f (x)\leq f (a)\; \forall \; x \in[a-\epsilon, a + \epsilon]\cap D$ ($f (x) \geq f (a) \; \forall \; x \in[a-\epsilon, a + \epsilon]\cap D$). $f$ attains a *strict* local min of $a$ if it attains a local max or min *and* $f (x)\neq f (a)\; \forall \; x \in[a-\epsilon, a + \epsilon]\cap D \smallsetminus \set{a}$.

#### Theorem 10

First derivative test.

Assume $f:D \rightarrow \mathbb{R}$ is differentiable at $a$ in the interior $D^{\circ}$. If $f$ attains a local maximum or minimum at $a$, then $f' (a)= 0$.

>[! Proof]-
>Pick $a \in D^{\circ}$, assume $f$ attains a local maximum or minimum at $a$. Because $a \in D^{\circ}, \; \exists \; \epsilon > 0$ such that $[a-\epsilon, a + \epsilon]\subset D$ *and* $f (x)\leq f' (a)\; \forall \; x \in[a-\epsilon, a + \epsilon]$. For all $a-\epsilon < x \leq a + \epsilon$, we have $\frac{f (x)-f (a)}{x-a}< 0$, and as $x \rightarrow 0$, $f' (a)\leq 0$.
>For all $a-\epsilon \leq x < a + \epsilon$, we have $\frac{f (x)-f (a)}{x - a}\geq 0$, and as $x \rightarrow 0$, $f' (a)\geq 0$. Mashing both together we get that $f' (a)= 0$.

Two remarks:
1. The assumption that $a \in D^{\circ}$ is *essential*, since otherwise $f$ may attain a maximum or minimum at the endpoint, in which case $f'(a)$ may not equal to $0$.
2. If $a \in D^{\circ}$ and $f' (a)= 0$, then $f$ may or may not attain a local maximum or minimum at $a$. With $f (x) = x^{3}, \; D =[-1, 1]$, $f' (0)= 0$, but $f (0)$ is neither a maximum or a minimum.

We need further information to ensure we get what we're looking for.

#### Lemma 12

Rolle's Theorem

Let $f:D \rightarrow \mathbb{R}$ be differentiable, $D \subset \mathbb{R}$ is an interval, and we take $a, b \in D$, with $a < b$. If $f (a)= f (b)$, then $f' (c)= 0$ for $c \in]a, b[$.

>[! Proof]-
>$f:[a, b]\rightarrow \mathbb{R}$ is continuous. $f$ attains a maximum or minimum on $[a, b]$. Let $y = \min f ([a, b])$ and $z \max f ([a, b])$. Then $y \leq f (x)\leq z\; \forall \; x \in[a, b]$. Distinguish three, non-disjoint cases:
>1. $y < f (a)= f (b)$. Therefore $\exists \; c \in (a, b)$ such that $f (c)= y$, so $f$ attains a local min at $c \implies f' (c)= 0$ by Theorem 10.
>2. $z > f (a)= f (b)$. Therefore $\exists \; c \in (a, b)$ such that $f (c)= z$, so $f$ attains a local max at $c\implies f' (c)= 0$.
>3. $y = z = f (a)= f (b)$. Then $f (x) = f (a)=$ constant. Then $\forall \; x \in (a, b)$ we have that $f' (c)= 0\; \forall \; c \in (a, b)$. For example pick $\frac{a + b}{2}$.


#### Theorem 13

Let $f:D \rightarrow \mathbb{R}$ be a differentiable function, with $D \subset \mathbb{R}$ an interval, and $a, b \in D$, and $a < b$. Then

$$
\frac{f (b)-f (a)}{b-a} = f' (c)
$$

For some $c \in (a, b)$.

>[! Proof]-
>Consider the auxilliary function $g:D \rightarrow \mathbb{R}$ given by
>
>$$
\begin{align}
g (x) & = f (x)-\frac{f (b)-f (a)}{b-a}(x-a) \\[1 em]
g (a) & = f (a)\qc g (b) = f (b)-\frac{f (b)-f (a)}{b-a}(b-a) = f (a)= g (a).
\end{align}
>$$
>
>By Lemma 12, $\exists \; c \in (a, b)$ such that $g' (c)= 0= \frac{f (b)-f (a)}{b-a}=$, which implies $f' (c)= \frac{f (b)-f (a)}{b-a}$.

This is known as the Mean Value Theorem, or MVT.

#### Corollary 14

Let $f:D \rightarrow \mathbb{R}$ be a differentiable function, with $D \subset \mathbb{R}$ an interval.

If $f' (x)= 0 \; \forall \; x \in D$, then $f$ is constant, i.e. $f (x)= d\; \forall \; x \in D$.

>[! Proof]-
>Fix any $a \in D$. For every $x \in D \smallsetminus \set{a}$, then by MVT
>
>$$
\begin{align}
\frac{f (x)-f (a)}{x-a} & = f' (c) \\[1 em]
\implies f (x) & = f (a)\; \forall \; x \in D.
\end{align}
>$$

If $f$ has higher derivatives, $f'', \; f^{(3), ...}$ then Theorem 10 and Theorem 13 can be refined

#### Theorem 15

Second derivative test

Assume that $f$ is twice differentiable (or $C^{2}$). If $f' (a)= 0$ and $f'' (a)> 0$, then $f$ attains a strict local minimum at $a$. If $f'' (a)< 0$, then $f$ attains a local maximum.

>[! Proof]
>We focus on the minimum case, but the maximum is analogous. Assume that $f' (a)= 0, \; f'' (a)> 0$. We claim that $\exists \; \delta_{1} > 0$ such that $f' (x)> 0 \; \forall \; x \in (a, a + \delta_{1})$. Reason: If this was not the case, there would exists a sequence $(a_{n})$ that is strictly decreasing, and as $a_{n}\rightarrow 0$, $f' (a_{n})\leq 0$. Then
>
>$$
\frac{f' (a_{n})-f' (a)}{a_{n}-a}\leq 0 \qc \forall \; n
>$$
>
>and that implies $f'' (a)\leq 0$, which contradicts our first assumptions. Then, $\forall \; x, y \in (a, a + \delta)\cap D$ with $x < y$, we have $\frac{f (y)-f (x)}{y-x}= f' (c)> 0 \implies f (y)> f (x)$, which implies $f$ is strictly increasing on $(a, a + \delta)$. Similarly, $\exists \; \delta_{2}$ such that $f' (x)< 0 \; \forall \; x \in (a-\delta_{2}, a)\cap D$. $f$ is then strictly decreasing on $(a-\delta_{2}, a)$, so $f (x)> f (a)\; \forall \; x \in (a-\delta_{2}, a)\cap D$.
>With $\delta:= \min \set{\delta_{1}, \delta_{2}}> 0$, we have $f (x)> f (a)$.