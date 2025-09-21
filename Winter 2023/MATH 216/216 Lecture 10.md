>[!examples]+ Example 11
  >Fix $a \in \mathbb{R}^{+}, \; n \in \mathbb{N}$. We know $a^{1/n}\in \mathbb{R}^{+}$. Consider $(a_{n})$ when $a_{n}= a^{1/n}$. Does $(a_{n})$ converge? And if so, what is its limit? We discuss three important cases:
>1. $a = 1\Rightarrow a_{n}= 1 \; \forall \; n$.
2. $a > 1 \Rightarrow a_{n}> 1$. Then $$\begin{align}a = a_{n}^{n}= (1 + a_{n}-1) & \geq 1 + n (a_{n}-1 \\ 1 + \frac{a-1}{n}& \geq a_{n} > 1 \end{align}$$ therefore $a_{n}\rightarrow 1$ by squeeze theorem.
3. $0 < a < 1\Rightarrow \frac{1}{a}> 1$: Case 2 applies: $$\begin{align}a^{1/n}= \frac{1}{\frac{1}{a^{1/n}}}\rightarrow \frac{1}{1}= 1 \end{align}$$ by limit laws.
>
>So $\forall \; a \in \mathbb{R}^{+}$, $\lim_{n \rightarrow \infty}a^{1/n}= 1$.

**Example 12** What happens if we replace $a$ by $n$ or $n^{2}...$?

Fix $l \in \mathbb{N}$, consider

$$
\begin{align}
a_{n} = (n^{l})^{1/n} & = n^{l/n}\\
& = (n^{1/n})^{l}.
\end{align}
$$

We need only consider $b_{n}= n^{1/n}$. If $b_{n}\rightarrow b$, then $a_{n}\rightarrow b^{l}$.

Consider $b_{n}= n^{1/n}\geq 1$. Let

$$
c_{n}S-L = b_{n}-1\geq 0.
$$

For $n \geq 2$,

$$
\begin{align}
n & = b_{n}^{n}\\
& = (1 + c_{n})^{n}\\
& = \sum\limits_{j = 0}^{n}\; _{n}C_{j}\cdot c_{n}^{j}\\
& \geq \; _{n}C_{2}\cdot c_{n}^{2}\\
& = \frac{n (n-1)}{2}c_{n}^{2}.
\end{align}
$$

In summary, $\forall \; l \in \mathbb{N}$,

$$
\lim \sqrt [n]{n^{l}} = 1.
$$

#### Definition 13

A sequence $(a_{n})\in \mathbb{R}$ diverges to $\infty$  or $-\infty$ (or symbolically $\lim_{n \rightarrow \pm \infty}a_{n}\in \mathbb{R}$).

$\forall \; c \in \mathbb{R}\; \exists \; N \in \mathbb{N}$ such that $a_{n}> c\; \forall \; c\geq N$. Informally, $a_{n}\rightarrow \infty$ means $a_{n}$ is "to the right" of every $c \in \mathbb{R}$ eventually. This is the most benign form of divergence.

**Example 14** Let

$$
a_{n} = \frac{3n^{2}+ 2n + 1}{4n + 1}.
$$

Our suspicion is that $a_{n}\rightarrow \infty$. To see this, we do the usual massaging:

$$
\begin{align}
a_{n} & = \frac{\frac{3}{4}(4n-3)n + \frac{17}{4}n + 1}{4n-3}\\
& = \frac{3}{4}n + \frac{17n + 4}{4 (4n-3)}> \frac{3}{4}n \\
\Rightarrow a_{n}& > \frac{3}{4}n \; \forall \; n \Rightarrow a_{n}\rightarrow \infty.
\end{align}
$$

But how fast does $a_{n}\rightarrow \infty$?

$$
\begin{align}
|\frac{a_{n}}{n}-\frac{3}{4}|& = \frac{17n + 4}{4n (4n-3)}\\
& < \frac{17 (n + 1)}{16n (n-1)}\\
& \leq \frac{34n}{16n (n-1)}\\
& < \frac{3}{n-1}\rightarrow 0.
\end{align}
$$

In summary,

$$
\begin{align}
a_{n} & \rightarrow \infty \\
\frac{a_{n}}{n} & \rightarrow \frac{3}{4}.
\end{align}
$$

**Example 15** Definition 13 allows us to compare the "speed" of divergence (and convergence) of sequences. E.g, fix $l \in \mathbb{N}$, $a \in \mathbb{R}^{+}$ with $a > 1$, and consider $(n^{l}), \; (a^{n}), \; (n!), \; (n^{n})$. All four of these sequences diverge to $\infty$.

Claim:

$$
\frac{a^{n}}{n^{l}} \rightarrow \infty.
$$

Reason:

$$
\begin{align}
a^{n} & = (1 + a-1)^{n}\\
& = \sum\limits_{j = 0}^{n} \; _{n}C_{j}(a-1)^{j}\\
& > \; _{n}C_{l + 1}(a-1)^{l1}\\
& = \frac{n (n-1)... (n-l)}{(l + 1)!}(a-1)^{l + 1}\\
\frac{a^{n}}{n^{l + 1}} > \left(1-\frac{1}{n} \right)\left(1-\frac{2}{n} \right)\cdots \left(1-\frac{l}{n} \right)\frac{(a-1)^{l + 1}}{(l + 1)!}.
\end{align}
$$

$\exists \; n \geq l + 1 \in \mathbb{N}$ such that 

$$
\begin{align}
\left(1-\frac{1}{n} \right)\cdots \left(1-\frac{l}{n} \right)> \frac{1}{2}
\end{align}
$$

$\forall \; n \geq N$. This then implies

$$
\frac{a^{n}}{n^{l}}> \frac{n}{2}\cdot \frac{(a-1)^{l + 1}}{(l + 1)!}
$$

so $\frac{a^{n}}{n^{l}}\rightarrow \infty$. The same can be shown for the others. In fact, comparing the rest, we get that

$$
n^{l}\ll a^{n}\ll n! \ll n^{n.}
$$

These are referred to, respectively, as polynomial growth, exponential growth, and the other two are simply called super-exponential growth. The reciprocals are, unsurprisingly, the exact opposite:

$$
0 > n^{-n}\gg \frac{1}{n!}\gg a^{-n} \gg n^{l}
$$

# Three Principles of Convergence

We will have a deeper look at some properties of convergent sequences. Everything will hinge on LUB.

## Principle 1

"Bounded and monotone $\Rightarrow$ convergence."

#### Definition 16

A sequence $(a_{n})\in \mathbb{R}$ is
1. Increasing if $a_{n + 1}\geq a_{n}$.
2. Strictly increasing if $a_{n + 1}> a_{n}$.
3. Decreasing if $a_{n + 1}\leq a_{n}$.
4. Strictly decreasing if $a_{n + 1}< a_{n}$.

For all $n \in \mathbb{N}$. The sequence is called monotone or strictly monotone if it is increasing or decreasing, or strictly increasing or strictly decreasing respectively.

Recall that if $(a_{n})$ is convergent, then it is bounded, but the reverse was not necessarily true, but if $(a_{n})$ is *monotone* then the converse is indeed true!

#### Theorem 17

^269be4

For every monotone sequence $(a_{n})\in \mathbb{R}$, the following are equivalent:
1. $(a_{n})$ is convergent.
2. $(a_{n})$ is bounded.

**Proof:** $(i)\Rightarrow (ii)$ is always true by lemma 6. To see that $(ii)\Rightarrow (i)$, first assume $(a_{n})$ is *increasing*.

Let $A = \{a_{n}\mid n \in \mathbb{N} \}, \; \Rightarrow A \neq \varnothing$. By LUB, $\sup A$ exists. That is, $\forall \; \epsilon > 0, \; a-\epsilon$ is **not** an upper bound of $A$. Therefore $\exists \; n \in \mathbb{N}$ such that $a_{N}> a-\epsilon$.

$(a_{n})$ increasing implies $a_{n}\geq a_{N}> a-\epsilon \; \forall \; n \geq N$.

$$
\begin{align}
a-\epsilon & \geq a_{N} \leq a_{n} \leq a \\
-\epsilon & < a_{n}-a\leq 0 \\
\abs{a_{n}-a} & < \epsilon
\end{align}
$$

And so $a_{n}\rightarrow a$.

Theorem 17 is important because boundedness of $(a_{n})$ may be easier to proof prove than convergence; also, the theorem separates the task of deciding about convergence from the task of finding the limit.

>[!examples]+ Example 18
>$$
\begin{align}
a_{n+ 1} & = \frac{1}{2}\left(a_{n}+ \frac{2}{a_{n}} \right), \quad n \in \mathbb{N}\\
a_{1} & = 2.
\end{align}
>$$
>
>We know that $a_{n}> 0$, and in fact $a_{n}\geq \sqrt{2}$. We also know that $a_{n}\geq a_{n + 1}$, which implies that $(a_{n})$ is decreasing.
>
>$(a_{n})$ is bounded: $\sqrt{2}\leq a_{n}\leq 2 \; \forall \; n \in \mathbb{N}$. Then by Theorem 17, our sequence is convergent.