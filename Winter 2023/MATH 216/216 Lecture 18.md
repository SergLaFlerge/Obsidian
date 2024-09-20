Last time, we introduced three notions that apply to a set. Openness, closeness, and compactness. For every set $A$, there is a largest open set $A^{\circ}\subset A$, called the interior of $A$, and a smallest closed set $\bar{A}\supset A$ called the closure of $A$. For example, let

$$
\begin{align}
A & =]0, 1[ \\
B & = [0, 1] \\
C & = [0, 1[ \\
D & = \mathbb{Q},
\end{align}
$$

then $A^{\circ}= A$, $\bar{A}= B$. $B^{\circ}= A$, $\bar{B}= B$. $C ^{\circ}= A$, $\bar{C}= B$. $D^{\circ}= \varnothing$, $\bar{D}= \mathbb{R}$.

#### Proposition 4

For every is set $A \subset \mathbb{R}$,
1. $A^{\circ}= \set{x \in \mathbb{R}\mid\exists \; \epsilon\;\text{such that}\; \comm{x-\epsilon}{x + \epsilon}\subset A}$.
2. $\bar{A}= \set{x \in \mathbb{R}\mid\comm{x-\epsilon}{x + \epsilon}\cap A \neq \varnothing \; \forall \; \epsilon > 0}= \set{x \in \mathbb{R}\mid\exists \; (x_{n})\; \text{such that}\; x_{n}\rightarrow{x}}$.
3. $\mathbb{R}\smallsetminus A^{\circ}= \overline{\mathbb{R}\smallsetminus A}$ and $\mathbb{R}\smallsetminus A = (\mathbb{R}\smallsetminus A)^{\circ}$.

We now want to describe closeness and compactness of $A \subset \mathbb{R}$ by means of sequences.

#### Lemma 5

$A \subset \mathbb{R}, \; A \neq \varnothing$ is closed. This implies that if $(x_{n})$ is a sequence in $A$ and $x_{n}\rightarrow x$. Then $x \in A$ (or, $A$ is closed under taking limits).

>[!proof]-
>Assume $A$ is closed. Let $(x_{n})$ be a sequence in $A$, with $x_{n}\rightarrow x\in \mathbb{R}$. Pick any $y \in \mathbb{R}\smallsetminus A$, which open by definition. Then $\exists \; \epsilon > 0$ such that $\comm{y-2 \epsilon}{y + 2 \epsilon}\cap A \neq \varnothing$. Therefore $\exists \; N$ such that $\abs{x_{N}-x}< \epsilon$. Then
>$$
\begin{align}
\abs{y-x_{N}}\leq \abs{y-x}+ \abs{x-x_{N}} \\[1em]
\abs{y-x}\geq \abs{y-x_{N}}-\abs{p-x_{N}}> \epsilon \\[1em]
y \neq x \\[1em]
x \in A.
\end{align}
>$$
>Suppose $A$ was not closed, i.e. $\mathbb{R}\smallsetminus A$ was not open. This would imply $\exists \; x \in \mathbb{R}\smallsetminus A$ such that $\comm{x-\frac{1}{n}}{x + \frac{1}{n}}\cap A \neq \varnothing\; \forall \; n \in \mathbb{N}$.
>For every $n \in \mathbb{N}$, pick $x_{n}\in \comm{x-\frac{1}{n}}{x + \frac{1}{n}}\cap A$. This implies $x_{n}\in \mathbb{A}$, $\abs{x_{n}-x}\leq \frac{1}{n}$. This in turn implies $x_{n}\rightarrow x \in \mathbb{R}\smallsetminus A$, which is a contradiction. Therefore $A$ is closed.

#### Lemma 6

$A \subset \mathbb{R}, \; A \neq \varnothing$ is compact. This implies that if $(x_{n})$ in $A$ has a convergent subsequence, i.e. $\exists$ subsequence $(x_{n_{j}})$ of $(x_{n})$, $\exists \; x \in A$ such that $\lim_{j \rightarrow \infty}x_{n_{j}}= x$. The proof is in the notes, but it uses the main idea from above plus Bolzano-Weierstrass theorem.

#### Remark 7

Many textbooks use the definition above as the definition for compactness. We went the other way. Doesn't really matter.

#### Lemma 8

If $A \subset \mathbb{R}, \; A \neq \varnothing$ is compact, then $A$ has a minimum and a maximum.

>[! Proof]
>$A$ compact $\implies$ $A$ is bounded, so $a:= \inf A$, and $b:= \sup A$ exists in $\mathbb{R}$.
>
>$\forall \; n \in \mathbb{N}$, $a + \frac{1}{n}$ is not a lower bound of $A$. This implies
>$$
\begin{align}
[a, a + \frac{1}{n}[\cap A \neq \varnothing \; \forall \; n \in \mathbb{N} \\[1em]
\exists\; x_{n}\in[a, a + \frac{1}{n}[\cap A \\[1em]
x_{n}\rightarrow a \in A,
\end{align}
>$$
>because $A$ is closed. Therefore $a = \min A$. Same for $b$.

# Limits and Continuity of Real Functions

For some function $f:\; D \rightarrow \mathbb{R}\qc D \subset \mathbb{R}, D \neq \varnothing$, if $a \in \bar{D}$ then $\exists \; (x_{n})\in D$ with $x_{n} \rightarrow a$, so we can consider $(f (x_{n}))$.

Note: If $a \in \bar{D}$ then either $a \in \overline{D \smallsetminus \set{a}}\Leftrightarrow \; \exists \; (x_{n})\in D \smallsetminus \set{a}$ such that $x_{n}\rightarrow a$, in which case $a$ is called an *accumulation point*. Or $a \in \overline{D \smallsetminus \set{a}}\Leftrightarrow \exists \; \epsilon > 0$ such that $\comm{a-\epsilon}{a + \epsilon}\cap D = \set{a}$, in which case $a$ is called an *isolated point*.

#### Definition 9

Let $f:D \rightarrow \mathbb{R}\qc a \in \bar{D}$, and $b \in \mathbb{R}\cup \set{-\infty, \infty}$.
1. If $a$ is an accumulation point of $D$ then $\lim_{x \rightarrow a}f (x)= b$ means that $f (x_{n}\rightarrow b)$ for every sequence $(x_{n})\in D \smallsetminus \set{a}$ and $x_{n}\rightarrow a$.
2. If $a$ is an isolated point of $D$ then $\lim_{x \rightarrow a}f (x)= b$ simply means that $f (a)= b$.
3. In $(1)$ and $(2)$, $b$ is the *limit* of $f$ as $x \rightarrow a$.
4. If $D$ is unbounded above then $\lim_{x \rightarrow \infty}f (x)= b$ means that $\lim_{n \rightarrow \infty}= b$ for every sequence $(x_{n})$ in $D$ with $x_{n}\rightarrow \infty$.

The same applies to unbounded below.

#### Remark 10

All familiar limit laws for sequence carry over to functions. That is

$$
\begin{align}
\lim_{x\rightarrow a}(f (x)\pm g (x)) & = b \pm c \\[1em]
\lim_{x \rightarrow a} f (x)\cdot g (x) & = b \cdot c.
\end{align}
$$

>[!examples]+ Example 11
>Consider the following functions $f (x)\frac{x^{3}-7x + 6}{x-1}$. This makes sense $\forall \; x \neq 1$, therefore $D = \mathbb{R}\smallsetminus \set {1}$. $a = 1 \notin D$, but $1 \in \bar{D}$.
>Note that 
>$$
f (x) = \frac{(x-1)(x^{2}+ x-6)}{x-1} = x^{2}+ x-6 \quad \forall \; x \in D.
>$$
> This implies $\lim_{x \rightarrow 1}f (x) =-4$.
> 
> Given any $c \in \mathbb{R}$, we could define $\tilde{f}:\; \mathbb{R}\rightarrow \mathbb{R}$ as $\tilde{f}= \set{f (x)\; \text{if}\; x \neq 1 \qc c \; \text{if}\; x= 1}$. So now we have $1 \in \tilde{D}$ and $\tilde{f} (1)= c$, but $\lim_{x \rightarrow 1}\tilde{f}(x)=-4$. The value $c = 4$ is the one value of $c$ that makes sense to pick here, as we then "patch" the hole and make $\tilde{f}(x)$ continuous.

>[! Examples]+ Example 12
>Consider $f (x)= \frac{x \abs{x}}{1 + x^{2}}$. Here $D = \mathbb{R}$.
>$$
f (x) =
\begin{cases}
1-\frac{1}{1 + x^{2}}\qc \text{if}\; &x \geq 0 \\[1em]
-1 + \frac{1}{1 + x^{2}}\qc \text{if}\; &x < 0
\end{cases}
>$$
>If $x_{n}\rightarrow \infty$ then $f (x_{n})\rightarrow 1$, so $\lim_{x \rightarrow 1}f (x)= 1$.
>If $x_{n}\rightarrow-\infty$ then $f (x_{n})\rightarrow-1$, so $\lim_{x \rightarrow-\infty}f (x)=-1$.

#### Definition 13

Let $D \subset \mathbb{R}$ and $a \in D$. A function $f:\; D \rightarrow \mathbb{R}$  is *continuous* at $a$ if $\lim_{x \rightarrow}f (x)= f (a)$; It is continuous on $D$ if it is continuous at every point in $D$.

A useful alternative description of continuity is as follows:

#### Lemma 14

Let $D \subset \mathbb{R}$ and $a \in D$. A function $f:\; D \rightarrow \mathbb{R}$ is continues at $a$ implies and is implied by,

$\forall \; \epsilon >0, \; \exists \; \delta > 0$ such that $\abs{f (x)-f (a)}< \epsilon\; \forall \; x \in \comm{a-\delta}{x + \delta}\cap D$.