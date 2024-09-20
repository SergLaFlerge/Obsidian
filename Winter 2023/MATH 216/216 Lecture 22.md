## The Exponential Function

Pick any real number $x \in \mathbb{R}$, and consider a series

$$
\sum\limits_{n = 0}^{\infty}\frac{x^{n}}{n!},
$$

where we take the standard convention that $x^{0}=0! = 1$. Let us call the terms of the series $a_{n}$. Applying the root test:

$$
\begin{align}
\sqrt[n]{\abs{a_{n}}} & = \sqrt[n]{\frac{\abs{x}^{n}}{n!}} \\[1em]
& = \frac{\abs{a_{n}}}{\sqrt[n]{n!}}\rightarrow 0
\end{align}
$$

independently of $x$! This implies our series is absolutely convergent $\forall \; x \in \mathbb{R}$. With obtain a function $\mathbb{R}\rightarrow \mathbb{R}$, called  $\exp(x)$, defined as our original series. We know that $\exp (0)=  1$. Also, $\exp (x)\geq 1 \; \forall \; x \geq 0$. We figure out that $\exp (1)= e$. But there is much more to this function.

#### Lemma 30

$\exp (x):\mathbb{R}\rightarrow \mathbb{R}$ is continuous.

>[! Proof]-
>Fix $a \in \mathbb{R}$, and consider $\abs{x-a}\leq 1$. Then,
>
>$$
\begin{align}
\exp (x)-\exp (a) & = \sum\limits_{n = 1}^{\infty}\frac{x^{n}-a^{n}}{n!}.
\end{align}
>$$
>
>Looking at $x^{n}-a^{n}$ for $n \in \mathbb{N}$, we see that
>
>$$
\begin{align}
x^{n}-a^{n} & = (x-a + a)^{n} \\[1em]
& = \sum\limits_{j = 0}^{n}\binom{n}{j}(x-0)^{j}a^{n-j}-a^{n} \\[1em]
& = (x-a) \sum\limits_{j = 1}^{n}\binom{n}{j}(x-a)^{j-1}a^{n-j} \\[1em]
\abs{x^{n}-a^{n}} & \leq \abs{x-a}\sum\limits_{j = 1}^{n}\binom{n}{j}\abs{n-j} \\[1em]
& = \abs{x-a}(1 + \abs{a})^{n}-\abs{a}^{n}\leq (1 + \abs{a})^{n} \\[1em]
\abs{x^{n}-a^{n}} & \leq (1 + \abs{a})^{n \abs{x-a}}\; \forall \; \abs{x-a}\leq 1 \\[1em]
\abs{exp (x)-\exp (a)} & \leq \sum\limits_{n = 1}^{\infty}\frac{\abs{x^{n}-a^{n}}}{n!} \\[1em]
& \leq \sum\limits_{n = 1}^{\infty}\frac{(1 + \abs{a})^{n}\abs{x-a}}{n!} \\[1em]
& = \abs{x-a}\exp (1 + \abs{a})-1 \\[1em]
\abs{\exp (x)-\exp (a)}& \leq \abs{x-a}\exp (1 + \abs{a}) \; \forall \; \abs{x-a}\geq 1
\end{align}
>$$
>
>so if $x_{n}\rightarrow a$, then $\abs{\exp (x_{n})-\exp (a)}\leq \abs{x_{n}-a}\exp (1 +\abs{a})\rightarrow 0$.
>Therefore $\exp (x)$ is continuous at a

#### Lemma 31

$\exp (x)\exp (y)= \exp (x + y)$

>[! Proof]-
>Use the Cauchy Product...
> 
> $$
\begin{align}
\exp (x) & = \sum\limits_{n = 0}^{\infty}\frac{x^{n}}{n!} = \sum\limits_{n = 1}^{\infty}\frac{x^{n-1}}{(n-1)!} = \sum\limits_{n = 1}^{\infty}a_{n} \\[1em]
\exp (y) & = \sum\limits_{n = 0}^{\infty}\frac{y^{n}}{n!}= \sum\limits_{n = 1}^{\infty}\frac{y^{n-1}}{(n-1)!} = \sum\limits_{n = 1}^{\infty}b_{n}.
\end{align}
>$$
>
>We know that
>$$
\sum\limits_{n = 1}a_{n}\cdot \sum\limits_{n = 1}b_{n} = \sum\limits_{n = 1}^{\infty}c_{n},
>$$
>and
>
>$$
\begin{align}
c_{n} & = \sum\limits_{j = 1}^{n}a_{j}b_{n + 1-j} \\[1em]
& = \sum\limits_{j = 1}^{n}\frac{x^{j-1}}{(j-1)!}\cdot \frac{y^{n + 1-j-1}}{(n+1-j-1)!} \\[1em]
& = \sum\limits_{j = 1}^{n}\frac{x^{j-1}}{(j-1)!}\cdot \frac{y^{n-j}}{(n-j)!} \\[1em]
& = \sum\limits_{i = 0}^{n}\frac{x^{i}}{i!}\cdot \frac{y^{n-1 - i}}{(n-1-i)!} \\[1em]
& =  \frac{1}{(n-1)!}\sum\limits_{i = 0}^{n-1}\frac{(n-1)!}{i! (n-1-i)!}x^{i}y^{n-1-i} \\[1em]
& = \frac{1}{(n-1)!}(x + y)^{n-1} \\[1em]
\therefore \sum\limits_{n = 1}^{\infty}c_{n}& = \sum\limits_{n = 1}^{\infty}\frac{(x + y)^{n-1}}{(n-1)!} \\[1em]
& = \sum\limits_{n = 0}^{\infty}\frac{(x + y)^{n}}{n!} = \exp (x + y)
\end{align}
>$$

This is quite powerful, in that we can deduce many properties of $\exp (x)$ from it:
1. $\exp (0)= 1$.
2. $\exp (x-x)= \exp (x)\exp (-x)$.
3. $\exp (-x)= \frac{1}{\exp (x)}$.
4. $\exp (x)\neq 0$.
5. $\exp (x)\geq 1 \; \forall \; x \geq 0$.
6. $0 < \exp (x)< 1 \; \forall \; x < 0$.

Because $\exp (1)= e$, that means $\exp (2)= e^{2}$, and so for $n \in \mathbb{N}$, we have $\exp (n)= e^{n}$. We can actually extend this to the real numbers, and define $e^{x}:= \exp (x)\qc x \in \mathbb{R}$.

If $y > x$, then $\exp (y)= \exp (y-x + x)$, which is always increasing.

We know that $2 < e < 3$, and so

$$
\begin{align}
\exp (n) = e^{n}> 2^{n}\rightarrow \infty \\[1em]
\exp (-n) = e^{-n} < 2^{-n}\rightarrow 0.
\end{align}
$$

$\exp(x)$ is continuous, so $\exp (\mathbb{R})$ is an interval by Theorem 24, and its range is $\mathbb{R}^{+}$

#### Theorem 32

The function $\exp (x):\mathbb{R}\rightarrow \mathbb{R}$, known as the *exponential function* is a continuous, strictly increasing bijection.

#### Corollary 33

The function $\exp^{-1}:= \log:\mathbb{R}\rightarrow \mathbb{R}$, known as the *(natural) logarithm* is also a continuous, strictly increasing bijection, with

$$
\log{xy}= \log (x)+ \log{y}.
$$

>[! Proof]
>$\exp:\mathbb{R}\rightarrow \mathbb{R}^{+}$ is a continuous bijection. Since $D = \mathbb{R}$ is an interval, Theorem 28 applies so $\exp^{-1}$ is also continuous.
>
>Pick any $x, y \in \mathbb{R}^{+}$. Then $\exists$ a unique $a, b \in \mathbb{R}$ such that $x = \exp (a)$ and $a = \log{x}$, and $y = \exp (b)$ and $b = \log{y}$. Then
>
>$$
\begin{align}
xy & = \exp (a) \exp (b) = \exp (a + b) \\[1em]
\log (xy) & = a + b = \log (x)+ \log (y).
\end{align}
>$$

#### Remark 34

Usage of $\exp$ (and $\log$)system allows us to define arbitrary powers $a^{b}\qc a \in \mathbb{R}^{+}, b \in \mathbb{R}$ in a convenient way that is consistent with our earlier definition of $a ^{r}$ for $r \in \mathbb{Q}$:

$$
a^{b} := \exp (b \log a).
$$

Natural question: What is $a^{b + c}$?

$$
\begin{align}
a^{b + c} & = \exp ((b + c)\log a) \\
& = \exp (b \log a)+ \exp (c \log a) \\
& = a^{b}a^{c}.
\end{align}
$$

What about $a^{bc}$?

$$
\begin{align}
a^{bc} & = \exp (bc \log a) \\
& = \exp (c \log (a^{b})) \\
& = (a^{b})^{c} = (a^{c})^{b}
\end{align}
$$

This is the end of our big continuity chapter, we now look at our final, very related chapter:

# Differentiation of Real Functions

Let $D \subset \mathbb{R}$, with $D \neq \varnothing$ and $f:D \rightarrow \mathbb{R}$ continuous for $a \in D$.

$\forall \; \epsilon > 0, \; \exists \; \delta > 0$ such that $\abs{f (x)-f (a)}< \epsilon$ provided that $x \in D$, and $\abs{x-a}< \delta$.

For $(x_{n})\in D, \; x_{n}\rightarrow a \implies x (x_{n})\rightarrow f (a)$. A natural follow up question: How small is $\abs{f (x)-f (a)}$ compared to $\abs{x-o}$? Let us look at the ratio:

$$
\frac{f (x)-f (a)}{x-a},
$$

or

$$
\frac{f (x_{n})-f (a)}{x_{n}-a}.
$$