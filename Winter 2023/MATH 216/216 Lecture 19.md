Let us backtrack a little bit. Say we have a function $f:D \rightarrow \mathbb{R}$ for $D \subset \mathbb{R}\neq \varnothing$. Recall that $f$ is continuous at $a$ if $\lim_{x \rightarrow a}f (x)= f (a)$, and more generally $\forall$ sequences $(x_{n})\in D$ with $x_{n}\rightarrow a$, we have $f (x_{n}\rightarrow f (a))$.

#### Lemma 14

$f$ is continuous at $a$ if and only if $\forall \; \epsilon 0$, $\exists \; \delta > 0$ such that that, $\forall \; x \in \comm{a-\delta}{a +\delta}\cap D$, $\abs{f (x)-f (a)}< \epsilon$. $f$ does not "jump" at $a$. If $f$ were to "jump" at $a$, we say that $f$ is discontinuous.

>[! Proof]-
>Assume the above definition is true. Let $(x_{n})$ with any sequence $\in D$ with $x_{n}\rightarrow a$. $\forall \; \epsilon> 0$, pick $\delta> 0$ as above. Then $\exists \; N \in \mathbb{N}$ such that $\abs{x_{n}-a}< \delta\; \forall \; n \geq N$. Again by the above, $\abs{f (x_{n})-f (a)}< \epsilon$. This implies $f (x_{n})\rightarrow f (a)$, i.e. $f$ is continuous at $a$.
>
>Suppose the above was false, i.e. $\exists \; \epsilon_{0}> 0$ such that no $\delta> 0$ "works", i.e. $\forall \; \delta > 0 \;\exists\; x \in \comm{a-\delta}{a + \delta}\cap D$ such that $\abs{f (x)-f (a)}\geq \epsilon_{0}$. Take $\delta = \frac{1}{n}$. Then $\forall \; n \in \mathbb{N}\; \exists \; x_{n}\in \comm{a-\frac{1}{n}}{a + \frac{1}{n}}\cap D$ such that $\abs{f (x_{n})-f (a)}\geq \epsilon_{0}> 0$. Clearly $x_{n}\rightarrow a$, yet $\abs{f (x_{n})-f (a)}\geq \epsilon_{0}$, which implies $f (x_{n})\cancel{\rightarrow}f (a)$, which is a contradiction.

>[! Examples]+ Example 15
>Let $C_{f}$ be the set of "continuity points" of $f$, i.e. $C_{f}= \set{a \in D \mid f\; \text{is continuous at}\; a}$.
>1. $f (x)= \lfloor x \rfloor$, $D = \mathbb{R}$. If $a \notin \mathbb{Z}$, $\exists \; \epsilon > 0$ such that $\comm{a-\epsilon}{a + \epsilon}\cap \mathbb{Z}= \varnothing$. This implies $f$ is constant in side this interval, which means $a \in C_{f}$. If $a \in \mathbb{Z}$, then $f (a)= a, \; f (a + \frac{1}{2n})= a \rightarrow a, \; f (a-\frac{1}{2n})\rightarrow a-1 \neq a$, which implies $\lim_{x \rightarrow a}f (x)$ does not exist, so $a \notin C_{f}$.
>2. $$
g (x) =
\begin{cases}
x \quad \text{if}\; x \in \mathbb{Q} \\
1 \quad \text{if}\; x \in \mathbb{R}\smallsetminus \mathbb{Q}
\end{cases}
>$$
>if $a \neq 1$: $\exists (r_{n})\in \mathbb{Q}$ with $r_{n}\rightarrow a$, and $g (r_{n})= r_{n}\rightarrow a$. Also $\exists \; (x_{n})\in \mathbb{R}\smallsetminus \mathbb{Q}$ with $x_{n \rightarrow a}$, but $g (x_{n})= 1 \rightarrow 1$, so $\lim_{x \rightarrow a}g (x)$ does not exist. $(a \notin C_{g})$. If however $a = 1$, then with any sequence $(x_{n})$ with $x_{n}\rightarrow 1$ we have $\abs{g (x_{n})-g (1)}= \abs{g (x)-1 \leq x_{n}-1}\rightarrow 0$. Therefore $g (x)$ is continuous at $a = 1$. $C_{g}= \set{1}$.

In practice, we rarely construct continuous functions from scratch. More often, we will build them using basic rules and "building blocks".

#### Theorem 16

If $f, g:D \rightarrow \mathbb{R}$ are both continuous at $a$ so are $f \pm g$, $f \cdot g$, and $\frac{f}{g}$ (provided that $g (a)\neq 0$).

>[! Proof]-
>This is "obvious" from the limit laws for sequences.

>[! Examples]+ Example 17
>- $f (x)= c =$ constant is continuous on $\mathbb{R}$.
>- $g (x)= x$: $\abs{g (x)-g (a)}= \abs{x-a}$ which is also continuous on $\mathbb{R}$.
>- $f \cdot g = cx$, $g \cdot g (x)= x^{2}...$ are all continuous on $\mathbb{R}$. Every polynomial function is continuous on $\mathbb{R}$.
>- Every rational function $\frac{f}{g}$ is continuous on $\mathbb{R}\smallsetminus \set{x \mid g (x)= 0}$.

>[! Examples]+ Example 18
>1. $f (x)= \abs{x}$, $D = \mathbb{R}$. $\abs{f (x)-f (a)}= \abs{\abs{x}-\abs{a}}\leq \abs{x-a}$. Therefore $f$ is continuous on $\mathbb{R}$.
>2. $g (x)= \sqrt{x}$, $x \geq 0$, $D =[0, \infty[$. If $a \geq 0$, then $\abs{g (x)-g (a)}= \abs{\sqrt{x}-\sqrt{a}}= \abs{\frac{x-a}{\sqrt{x}-\sqrt{a}}}\leq \frac{\abs{x-a}}{\sqrt{a}}$ so $g$ is continuous at $a$. If $a = 0$, $g (0)= 0$. Take any sequence $(x_{n})\in D$ with $x_{n}\rightarrow 0$. $\forall \; \epsilon > 0, \; \exists \; n \in \mathbb{N}$ . Such that $0 \leq x_{n}\leq \epsilon^{2}\; \forall \; n \geq N$ which implies $0 \leq \sqrt{x_{n}}< \epsilon \; \forall \; n \geq N$, so $g (x_{n})\rightarrow 0 = g (0)$. Therefore $g$ is continuous on $[0, \infty[$.

#### Theorem 19

Let $D, E \subset \mathbb{R}$ and $a \in D$. If $f:D \rightarrow \mathbb{R}$ is continuous at $a$with $f (D)\subset E$, and $g:E \rightarrow \mathbb{R}$ is continuous at $f (a)$, then the composition $g \circ f:D \rightarrow \mathbb{R}$ is continuous at $a$. The composition of continuous functions is also continuous.

>[! Proof]-
>Let $(x_{n})$ be by sequence in $D$ with $x_{n}\rightarrow a\Rightarrow (f (x_{n}))$ is a sequence in $E$, with $f (x_{n})\rightarrow f (a)$ because $f$ is continuous at $a$. This then implies $f (f (x_{n}))\rightarrow g (f (a))$ because $g$ is continuous at $f (a)$. Therefore $g \circ f$ is continuous at $a$.

For instance, if $f:\mathbb{R}\rightarrow \mathbb{R}$ is a polynomial, then $\sqrt{\abs{f}}$ is continuous on $\mathbb{R}$.

This shall be the cut-off for mid-term number 2.

# Midterm Info

Next Thursday, March 23.

Also 50 minutes.

Closed book.

Don't fuck up the multiple choice.

Practice midterm will be available and will be a very good idea of what to expect.

Remember the practice one will be longer so do not panic.

<br>
<br>

Laptop died so maybe consider looking at the notes after class.