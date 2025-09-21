Let's look at the specific example $a_{n}= P_{n}$. That is, $a_{n}$ is the $n-$th prime number. Pick any $a \in \mathbb{R}$. By $AP$, there exists $m \in \mathbb{N}$ such that $m \geq a + 1\; \forall n \geq m$. $a_{n}= P_{n}> n \geq m \geq a + 1\Rightarrow a_{n}-a \geq 1 \; \forall n \geq m$. This implies that for $0 < \epsilon < 1$ then $\abs{a_{n}-a}< \epsilon$ is *impossible*. Therefore $(P_{n})$ is divergent.

#### Lemma 6

A sequence $(a_{n})\in \mathbb{R}$ can have *at most* one limit; If $(a_{n})$ is convergent then it is bounded.

**Proof:**

Assume $a_{n}\rightarrow a, \; a_{n}\rightarrow b$. $\forall \; \epsilon > 0, \; \exists N \in \mathbb{N}$ such that $\abs{a_{n}-a}, \; \abs{a_{n}-b}< \epsilon$. Then

$$
\begin{align}
\abs{a-b}\leq \abs{a-a_{n}}+ \abs{a_{n}-b} < \epsilon + \epsilon = 2 \epsilon.
\end{align}
$$

For arbitrary $\epsilon > 0\Rightarrow \abs{a-b}= 0 \Rightarrow a = b$. 

$\exists \; M \in \mathbb{N}$ such that $\abs{a_{n}-a}< 1\; \forall \; n \geq M$. Therefore $\abs{a_{n}} = \abs{a_{n}-a + a}\leq \abs{a_{n}-a}+ \abs{a}$.

Let $C:= \max \{\abs{a_{1}}, \abs{a_{2}}, ..., \abs{a_{M-1}}, 1 + \abs{a} \}\in \mathbb{R}^{+}$.

$\abs{a_{n}}\leq C \; \forall \; n \in \mathbb{N}$. Therefore $(a_{n})$ is bounded. So a sequence like $((-1)^{n})$ is bounded, but not divergent.

# Theorem 7

Let $(a_{n}), (b_{n})$ be sequences in $\mathbb{R}$. If $a_{n}\rightarrow a, \; b_{n}\rightarrow b$is then
1. $a_{n}+ b_{n}\rightarrow a + b$.
2. $a_{n}b_{n}\rightarrow ab$.
3. $\frac{a_{n}}{b_{n}}\rightarrow \frac{a}{b}$, provided $b_{n}\neq 0 \; \forall n \in \mathbb{N}, \; b\neq 0$
4. $\abs{a_{n}}\rightarrow \abs{a}$.

**Proof:**

1 and 2 are on the upcoming homework. Let us prove 3.

We know $a_{n}\rightarrow a$ and $b_{n}\rightarrow b$. Our goal is that

$$
\frac{a_{n}}{b_{n}}\rightarrow \frac{a}{b}\;
$$

I.e.

$$
\abs{\frac{a_{n}}{b_{n}}}< \epsilon \quad \text{should have abs bars.}
$$

$b \neq 0 \Rightarrow \abs{b}> 0$. $\exists \; N \in \mathbb{N}$ such that $\abs{b_{n}-b}< \frac{1}{2}\abs{b}\; \forall \; n \geq N_{1}$,

$$
\abs{b} = \abs{b-b_{n}+ b_{n}}\leq \underbrace{\abs{b-b_{n}}}_{< (1/2)\abs{b}}+ \abs{b_{n}}
$$

This implies $\forall \; n \geq N_{1}, \; \abs{b_{n}}> \frac{1}{2}\abs{b}$.

$$
\begin{align}
|\abs{\frac{a_{n}}{b_{n}}-\frac{a}{b}}|& = \frac{\abs{a_{b}b-ab_{n}}}{b_{n}b}\\
& < \frac{\abs{a_{n}-a}\abs{b}+ \abs{a}\abs{b-b_{n}}}{\abs{b}^2}
\end{align}
$$

$\forall \; \epsilon > 0, \; \exists \; N_{2}$ such that $\abs{a_{n}-a}, \; \abs{b_{n}-b}< \epsilon$.

Let $N = \max \{N_{1}, N_{2}\}$. Then $\forall \; n \geq N$,

$$
\begin{align}
|\frac{a_{n}}{b_{n}}-\frac{a}{b}| &< 2 \frac{C_{\epsilon}\abs{b}+ C_{\epsilon}\abs{a}}{b^2}\\
& = \epsilon \underbrace{\left(2 \frac{C}{b^2}(\abs{a}+ \abs{b}) \right)}_{= 1}
\end{align}
$$

Therefore

$$
|\frac{a_{n}}{b_{n}}-\frac{a}{b}| < \epsilon
$$

$$
\Rightarrow \frac{a_{n}}{b_{n}} \rightarrow \frac{a}{b}.
$$

# Theorem 8

Let $(a_{n}), \; (b_{n})$ be real sequences, and $a_{n}\leq b_{n}\; \forall \; n \in \mathbb{N}$. If $a_{n}\rightarrow a$ and $b_{n}\rightarrow b$, then $a \leq b$.

**Proof:**

$a = a-a_{n}+ a_{n}\leq \abs{a-a_{n}}+ a_{n}$. $\forall \; \epsilon >, \; \exists \; N \in \mathbb{N}$ such that $\abs{a_{n}-a}, \; \abs{b_{n}-b}< \epsilon/2 \; \forall \; n \in \mathbb{N}$. Then

$$
\begin{align}
\abs{a-a_{n}} & < \frac{\epsilon}{2}\\
& < \frac{\epsilon}{2}+ a_{n}\leq \frac{\epsilon}{2}+ b_{n}\\
& = \frac{\epsilon}{2}+ b + b_{n}-b \\
& \leq \frac{\epsilon}{2}+ b + \abs{b_{n}-b}\\
& < \frac{\epsilon}{2}\\
& < \epsilon+ b \\
& \therefore \\
a& < \epsilon + b \\
a-b & < \epsilon \\
\Rightarrow a-b & \leq 0,
\end{align}
$$

i.e. $a \leq b$.

# Theorem 9

Let $(a_{n}), (b_{n}), (c_{n})$ be real sequences, and $a_{n}\leq b_{n}\leq c_{n}\; \forall \; n$. If $a_{n}\rightarrow a$ and $c_{n} \rightarrow a$ for some $a \in \mathbb{R}$, then $b_{n}\rightarrow a$.

**Proof:**

$\forall \; \epsilon> 0, \; \exists \; N \in \mathbb{N}$ such that $\abs{a_{n}-a}< \epsilon$, and $\abs{c_{n}-a}< \epsilon \; \forall \; n \geq N$. Then

$$
\begin{align}
a & = a-a_{n}+ a_{n}< \epsilon + a_{n}\leq \epsilon + b_{n}\\
& \leq \epsilon + c_{n}\\
& = \epsilon + a + c_{n}-a \\
& < 2 \epsilon + a\\[1em]
-\epsilon & < b_{n}-a< \epsilon \; \forall \; n \geq N \\
\Rightarrow \abs{b_{n}-a} &< \epsilon \; \forall \; n \geq N,
\end{align}
$$

i.e.

$$
\lim_{n \rightarrow \infty}b_{n}= 0
$$


This is the cut-off for the midterm. Test is 50 minutes, in class.

There will be a practice midterm on eclass, among other ways to practice, but it is the most representative. Notes should be used too as well as the homework. Focus on the midterm practice though. Practice midterm is much longer so don't be surprised.