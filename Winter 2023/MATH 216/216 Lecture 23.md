#### Definition 1

A function $f:D \rightarrow \mathbb{R}$ is *differentiable* at $a\in D$ if

$$
\lim_{x \rightarrow a}\frac{f (x)-f (a)}{x-a}
$$

exists (in $\mathbb{R}$). The number above is called the *derivative* of $f$ at $a$, denoted $f' (a), \; \dv{f}{x}(a), \;\eval{\dv{f}{x}}_{x = a}$, and so on. The function $f:D \rightarrow \mathbb{R}$ is differentiable (on $D$) if it is differentiable at every $a \in D$; in this case, we obtain a new function, $f':D \rightarrow \mathbb{R}\qc x \mapsto f' (x)$, which is known as *the first derivative* of $f$.

**Note:** In definition 1, we consider $\frac{f (x)-f (a)}{x-a}$ as a function of $D \smallsetminus \set{a}$; but $a \in \overline{D \smallsetminus \set{a}}$, so the limit makes sense!

#### Lemma 2

If $f:D \rightarrow \mathbb{R}$ is differentiable at $a \in D$, then $f$ must be continuous at $a$.

>[! Proof]-
>Let $(x_{n})$ be any sequence, and assume $f$ is differentiable at $a$. The sequence is in $D \smallsetminus \set{a}$, with $x_{n}\rightarrow a$. By convergence, $\exists \; n \in \mathbb{N}$ such that $\abs{x_{n}-a}< \frac{\epsilon}{1 + \abs{f' (a)}}\; \forall \; n \geq N$ and $\abs{\frac{f (x_{n})-f (a)}{x_{n}-a}}\leq 1$. Comparing $f (x_{n})-f (a)$, we have $\abs{f (x_{n})-f (a)}= \abs{\left(\frac{f (x_{n})-f (a)}{x_{n}-a} -f' (a\right)(x_{n}-a)+ f' (a)(x_{n}-a)}$.
>
>$$
\begin{align}
\abs{f (x_{n})-f (a)} & \leq \abs{\frac{f (x_{n})-f (a)}{x_{n}-a}}\abs{x_{n}-a}+ \abs{f' (a)}\abs{x_{n}-a} \\[1em]
& \leq (1 + \abs{f' (a)})\abs{x_{n}-a} < \epsilon,
\end{align}
>$$
>
>i.e., $f (x_{n})\rightarrow f (a)$, so $f$ is continuous at $a$.

>[! Examples]+ Example 3
>1. $f (x)= x^{l}$, $l \in \mathbb{N}$, $D = \mathbb{R}$. Fix $a \in \mathbb{R}$. Then
>	1. $l = 1$: $\frac{f (x)-f (a)}{x-a}= \frac{x-a}{x-a}= 1$.
>	2. $l \geq 2$: $f (x)-f (a)= x^{l}-a^{l}= (x-a + a)^{l}-a^{l}$. $$\begin{align}f (x)-f (a) & =  \sum\limits_{j = 1}^{l}\binom{l}{j}(x-a)^{j}l^{l-y}\\[1em] & = l (x-a)a^{l-1}+ \sum\limits_{j = 2}^{l}\binom{l}{j}(x-a)^{j}a^{l-j}. \end{align}$$ Then, if $0 < \abs{x-a}\leq 1$ then $$\begin{align}\frac{f (x)-f (a)}{x-a}-la^{l-1}& = \sum\limits_{j = 2}^{l}\binom{l}{j}(x-a)^{j-1}a^{l-j}\\[1em] & = (x-a)\sum\limits_{j = 2}^{l}\binom{l}{j}(x-a)^{j-2}a^{l-j}\\[1em] & \leq \abs{x-a}\sum\limits_{j = 2}^{l}\binom{l}{j}\abs{a}^{l-j}\\[1em] & \leq \abs{x-a}(1 + \abs{a})^{l}, \end{align}$$ so $f$ is differentiable, and $f' (x)= lx^{l-1}\; \forall\; x \in \mathbb{R}$.
>2. $f (x)= 1 + \sqrt{x}, \; D =[0, \infty[$, where $f$ is continuous. For $a > 0$, $$\begin{align} \frac{f (x)-f (a)}{x-a} & = \frac{\sqrt{x}-\sqrt{a}}{(\sqrt{x}-\sqrt{a})(\sqrt{x}+ \sqrt{a}}\\[1 em] & = \frac{1}{\sqrt{x}+ \sqrt{a}} \rightarrow \frac{1}{2 \sqrt{a}}. \end{align}$$ For $a = 0$, the function is not differentiable.

First, we have to establish some basic properties of derivatives.

#### Theorem 4

If $f, g:D \rightarrow \mathbb{R}$ are both differentiable at $a \in D$, then
1. $f \pm g$ is differentiable at $a$, with $(f \pm g)'(a) =f' (a)\pm g' (a)$.
2. $fg$ is differentiable at $a$, with $(fg)' (a)= f' (a)g (a)+ f (a)g' (a)$
3. $\frac{f}{g}$ is differentiable at $a$, provided that $g (a)\neq 0$, with $\left(\frac{f}{g} \right)'= \frac{f' (a)g (a)-g' (a)f (a)}{g (a)^{2}}$.

>[! Proof]-
>1. Immediate from limit laws.
>2. $$\begin{align}\frac{f (x)g (x)-f (a)g (a)}{x-a} & = \frac{(f (x)-f (a))g (x)+f (a)(g (x)-g (a))}{x-a} \\[1 em] & = \frac{f (x)-f (x)}{x-a}g (x)+ f (a)\frac{g (x)-g (a)}{x-a}\\[1em] & = f' (a)g(a) + f (a)g (a). \end{align}$$
>3. $$\begin{align}\frac{\frac{f (x)}{g (x)}-\frac{f (a)}{g (a)}}{x-a} & = \frac{f (x)g (a)-f (a)g (x)}{g (a)g (x)(x-a)}\\[1 em] & = \frac{1}{g (a)g (x)}\frac{(f (x)-f (a))g (a)-f (a)(g (a)-g (x))}{x-a}\\[1 em] & = \frac{1}{g (a)g (x)}\left[\frac{f (x)-f (a)}{x-a}g (a)-f (a)\frac{g (x)-g (a)}{x-a} \right]\\[1 em] & = \frac{f' (a)g (a)-f (a)g' (a)}{g (a)^{2}}.\end{align}$$

Next we consider the composition of functions:

#### Theorem 5

Let $f:D \rightarrow \mathbb{R}$, $g:E \rightarrow \mathbb{R}$, and assume that $f (D)\subset E$. If $f$ is differentiable at $a\in D$ and $g$ is differentiable at $f (a)\in E$, then $(g \circ f)$ is differentiable at $a$, and

$$
(g \circ f)' = g' (f (a))f' (a).
$$

>[! Proof]-
>Let's consider an auxiliary function $h:E \rightarrow \mathbb{R}$, given by
>
>$$
h (y) =
\begin{cases}
\frac{g (y)-g (f (a))}{y-f (a)}\qc y& \neq f (a) \\
g' (f (a))\qc y & =f (a)
\end{cases}.
>$$
>
>$g$ is differentiable at $f (a)$, which implies $\lim_{y \rightarrow a}h (y)= g' (f (a))= h (f (a))$, i.e. $h$ is continuous at $f (a)$. Also, $g (y)-g \circ f (a)= h (y)(y-f (a))\; \forall \; y \in E$. Therefore $g \circ f (x)-g \circ f (a)= h (f (x))(f (x)-x (a))\; \forall \; x \in D$. Therefore
>
>$$
\begin{align}
\frac{g \circ f (x)-g \circ f (a)}{x-a} & = h (f (x))\frac{f (x)-f (a)}{x-a}\qc \forall \; x \in D \smallsetminus \set{a},
\end{align}
>$$
>
>and so as $x \rightarrow a$, the above goes to $g' (f (a))f'(a)$.

#### Corollary 6

Assume $f:D \rightarrow \mathbb{R}$ is a continuous, 1-1 function (or strictly monotone). If $f' (a)\neq 0$, then $f^{-1}:f (D)\rightarrow \mathbb{R}$ is differentiable at $f (a)$, with

$$
(f^{-1})'(f (a)) = \frac{1}{f' (a)}.
$$

>[! Proof]-
>We know that $f^{-1}(x):f (D)\rightarrow \mathbb{R}$ is continuous and strictly monotone.
>
>Let $(b_{n})$ be any sequence in $f (D)\smallsetminus \set{f (0)}$with $b_{n} \rightarrow f (a)$. We know that $f^{-1}(b_{n})$ then converges to $f^{-1}(f (a))= a$ because $f^{-1}$ is continuous. $f^{-1}(b_{n})\in D \smallsetminus \set a$. Then, the quotient approaches $f' (a)$ but $f$ is differentiable at $a$, which implies that
>
>$$
\frac{f^{-1}(b_{n})-a}{b_{n}-f (a)} \rightarrow \frac{1}{f' (a)}.
>$$

**Note:** If $f:D \rightarrow \mathbb{R}$ is differentiable, then $f':D \rightarrow \mathbb{R}$ may be continuous (differentiable), in which case $f$ is said to be *continuously differentiable*, or $C^{1}$, for short. If $f'$ is then differentiable, $f$ is twice differentiable, or $C^{2}$. We can iterate this $n$ times, with $f^{(n)}$ being called the n-th derivative, as long as it exists. Then the function is $C^{n}$. If $f$ is has continuous derivatives of all orders, then $f$ is $C^{\infty}$, which is also known as smooth.