 > [!examples]+ Example 19
 > Consider the sequence
 > $$a_{n} =\left(1 + \frac{1}{n}\right)^{n}.$$
 > What is this thing? $$\begin{align}(a_{n}) & = \left(2, \frac{9}{4}, \frac{64}{27}, ... \right)\\[1em] & = (2, 2.25, 2.370, 2.44, ...) \end{align}$$ It appears that $a_{n}$ is increasing, and $a_{n}\geq 2$.
 > We state the following lemma: $$\forall \; n \in \mathbb{N}, \; 2 \leq \left(1 + \frac{1}{n} \right)^{n}\leq 3, $$ and $a_{n}\leq a_{n + 1}$.
 >
 > From Bernoulli's inequality, we get $$1 + nx \leq (1 + x)^{n}.$$ With $x = \frac{1}{n}$, we get $$\begin{align}1 + n \left(\frac{1}{n} \right) & \leq \left(1 + \frac{1}{n} \right)^{n}\\[1em] 2 &\leq \left(1 + \frac{1}{n} \right)^{n} \end{align}$$ To deal with the right hand side, we can apply the binomial theorem: $$\begin{align} a_{n}& = \left(1 + \frac{1}{n} \right)^{n}= \sum\limits_{j = 0}^{n}\binom{n}{j}i^{n-j}\cdot \left(\frac{1}{n} \right)^{j}\\[1em] & = \sum\limits_{j = 0}^{n}\frac{n!}{(n-j)! \cdot j!}\cdot \frac{1}{n^{j}}\\[1em] & = 1 + n \cdot \frac{1}{n}+ \frac{n!}{(n-2)!\cdot 2!}\cdot \frac{1}{n^{2}}+ \cdots + \frac{n!}{(n-n)! \cdot n!}\cdot \frac{1}{n^{n}}\\[1em] & = 2 + \left(1-\frac{1}{n}\right)\cdot \frac{1}{2!}+ \cdots + \left(1-\frac{1}{n} \right) \left(1-\frac{2}{n} \right) \cdots \left(1-\frac{n-1}{n} \right)\cdot \frac{1}{n!}. \end{align}$$ It follows that $n < n + 1$, for all $n \in \mathbb{N}$. Moreover, for $k = 1, 2, ..., n$, $$\left(1-\frac{k}{n} \right)\leq 1.$$ The last step above implies $$a_{n}\leq 2 + \frac{1}{2!}+ \frac{1}{3!}+ \cdots + \frac{1}{n!}.$$ Recall that $2^{n-1}< n!$ for $n \geq 3$. Therefore $\frac{1}{n!}< \frac{1}{2^{n-1}}$. Therefore $$a_{n}\leq 2 + \frac{1}{2}+ \frac{1}{2^{2}}+ \cdots + \frac{1}{2^{n-1}}= 3-\frac{1}{2^{n-1}}.$$ So $a_{n}$ is monotonically increasing and bounded above by $3$. By Theorem 17, $a_{n}$ converges, and it is known as Euler's  Number.
 
#### Theorem 20 (Nested Interval Property)

Let $I_{1}\supseteq I_{2} \supseteq I_{3}\supseteq...$ be a nested sequence of closed intervals. Then

$$
\bigcap_{n = 1}^{\infty}I_{n} = \{x \in \mathbb{R}\mid x \in I_{n} \; \forall \; n \in \mathbb{N} \}
$$

is not empty.

> [!proof]-
> Let $I_{n}= [a_{n}, b_{n}]$. Then $$I_{n}\supseteq I_{n + 1}\Rightarrow a_{n} \leq a_{n+ 1}\leq b_{n+ 1}\leq b_{n}.$$ As such, $(a_{n})$ is an increasing sequence bounded by $b$, and $(b)$ is a decreasing sequence bounded by $a$. By [[216 Lecture 10#Theorem 17|Theorem 17]] , both $(a_{n})$ and $(b_{n})$ converge: $$a = \lim_{n \rightarrow \infty}a_{n}, \; b = \lim_{n \rightarrow \infty}b_{n},$$ and by Theorem 8, $a \leq b\neq 0.$ Therefore, for all $n \in \mathbb{N}$, $[a, b]\subseteq I_{n}\Rightarrow [a, b] \subseteq \bigcap_{n = 1}^{\infty}I_{n}$.

#### Remark 21

The nested interval property does not hold for $\mathbb{Q}$.

> [!proof]-
>  Let $a_{n}$ be an increasing sequence in $\mathbb{Q}$ that converges to $\sqrt{2}$, and $b_{n}$ be a decreasing sequence in $\mathbb{Q}$ that converges to $\sqrt{2}$. Then
>  $$
>  \bigcap_{n = 1}^{\infty}[a_{n}, b_{n}]= [\sqrt{2}, \sqrt{2}]= \{\sqrt{2}\}
>$$
> and $\sqrt{2}\notin \mathbb{Q}$.

#### Theorem 22

$\mathbb{R}$ is not countable.

> [!proof]-
> We must show that *any* map $f:\mathbb{N}\rightarrow \mathbb{R}$ is not onto. It will be sufficient to show that
> $$
> B = f (\mathbb{N})\; \cap\; [0, 1]\neq [0, 1].
>$$
> Let $A= f^{-1}([0, 1])= \{n \in \mathbb{N}\mid f (n)\in [0, 1] \}.$ We reorder $A$ with the well ordering property to get $A = \{n_{1}, n_{2}, n_{3}, ... \}$ with $n_{k}< n_{k + 1}$. We have two cases:
> 1. $A$ is finite, which implies $B$ is finite. Therefore, $B \neq [0, 1]$ since $\{\frac{1}{n} \}\subseteq [0, 1]$ is infinite.
> 2. $A$ is infinite. Here, we construct a nested sequence of interval $$... \subseteq I_{n + 1}\subseteq I_{n}\subseteq ... \subseteq [0, 1]$$ such that $f (x_{k})\notin I_{k + 1}$. This would imply $f (x_{k})\notin \bigcap_{n = 1}^{\infty}I_{n}$, and $B \cap  (\cap I_{n})= \varnothing$.
> To this end, we split $I_{0}= [0, 1]$ into three parts: Left, Middle, and Right. If $f (n_{1})\in L$, then $I_{1}= R$. Otherwise $I_{1}= L$. To get $I_{2}$, we now cut $I_{1}$ into three parts, and repeat. If $f (n_{2})\in L (I_{1})$, then $I_{2}= R (I_{1})$, otherwise $I_{2}= L (I_{1})$. We continue recursively to get $I_{k}\subseteq I_{k + 1}$ and $f (n + 1)\notin I_{k + 1}$. Therefore $\exists \; \lambda \in [0, 1]\smallsetminus B$.

#### Remark 23

The power set of $\mathbb{N}$ is also uncountable! It can be shown that there is a bijection between $P (\mathbb{N})$ and $\mathbb{R}$.

#### Definition 24

Let $(a_{n})$ be a sequence. Let $1 \leq n_{1}< n_{2}< n_{3}...$ be any strictly increasing sequence of $\mathbb{N}$. Then we call $(a_{n})_{j = 1}^{\infty}$ a *subsequence* of $(a_{n})$.

If we view $(a_{n})$ as an ordered list, then a subsequence is simply an infinite sublist with all entries deleted unless $n = n_{j}$ for some $j \in \mathbb{N}$.