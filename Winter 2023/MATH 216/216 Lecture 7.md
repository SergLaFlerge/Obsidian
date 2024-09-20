#### Theorem 25

$\forall \; a \in \mathbb{R}^{+}, \; n \in \mathbb{N}$, $\exists! \; x \in \mathbb{R}^{+}$ such that $x^{l}= a$. (We write this as either $a^{1/l}$ or $\sqrt[l]{a}$).

Moreover, if $a \leq b$ then $a^{1/l}\leq b^{1/l}$.

**Proof:** Consider a set $A= \{x \in \mathbb{R}^{+}\mid x^{l}< a\}$. We know $A$ is non-empty, bounded above, and $s = \sup A$ satisfies $s^{l}= a$.

By the Archimedean Principle, there exists $m \in \mathbb{N}$ such that 

$$
\begin{align}
\frac{1}{m} & < a\\
\Rightarrow \left(\frac{1}{m}\right)^{l}& = \frac{1}{m^{l}}\leq \frac{1}{m}\leq a.
\end{align}
$$

This implies $\frac{1}{m}\in A$. Again by AP $\exists \; n \in \mathbb{N}$ such that $n > a$, and $n^{l}> n > a$, so $n$ is an upper bound of $A$. By the least upper bound property, $\sup A$ exists.

Fix any $s \in \mathbb{R}^{+}$, and consider two cases:
1. $s^{l}> a$, implying $s \notin A$ so $A$ is an upper bound of $A$. Then $\exists \; m \in \mathbb{N}$ such that $m > \frac{1}{s}$ and $m > \frac{ls^{l-1}}{s^{l}-a}$. Then $$\left(s-\frac{1}{m}\right)^{l}= s^{l}\left(1-\frac{1}{ms} \right)\leq s^{l}\left(1-\frac{l}{ms} \right) = s^{l}- \frac{ls^{l-1}}{m}.$$ This implies $(s-\frac{1}{m})^{l}> a$. So $s-\frac{1}{m}< s$, but is still an upper bound of $A$.
2. $s^{l}< a$, implying $s \in A$. Then $\exists \; n \in \mathbb{N}$ such that $n > \frac{1}{s}$ and $n > \frac{2^{l}s^{l-1}}{a-sl}$. Then $$\left(s + \frac{1}{n} \right)^{l}= s^{l}\left(1 + \frac{1}{ns} \right)^{l} = s^{l}\sum\limits_{j = 0}^{l} \; _{l}C_{j}\frac{1}{(ns)^{j}} < 2^{l}-1 < 2^{l}$$ so $$\left(s + \frac{1}{n} \right)^{l}< s^{l}\left(1 + \frac{2^{l}}{ns} \right) = s + \frac{2^{l}s^{l-1}}{n},$$ and $$\left(s + \frac{1}{n} \right)^{l}< a$$ and $s + \frac{1}{n}\in A$.

Now let $s = \sup A$. By case 1, $s^{l}\leq A$, but by case 2, $s \geq a$, so $s^{l}= a$, i.e. $s \in \mathbb{R}^{+}$ is a solution to $x^{l}= a$.

Assume $a \leq b$,

$$
\begin{align}
x = a^{1/l} & \Rightarrow x^{l}= a \\
y = b^{1/l} & \Rightarrow y^{l} = b
\end{align}
$$

We need to show $x \leq y$. Suppose $x > y$. This implies $x^{2}= x \cdot x > x \cdot y > y^{2}$ therefore $a = x^{l}> y^{l}= b$, which is a contradiction. For convenience, $0^{1/l}= 0 \; \forall \; l \in \mathbb{N}$.

We close this chapter by a short informal discussion an the size of sets.

Recall that for *finite* sets $A, B$, if

$$
|A|\geq|B|
$$

Implies the existence of a 1-1 function $f:B \rightarrow A$.

#### Proposition 26

A set $A$ is infinite if there exists a 1-1 function $f:\mathbb{N}\rightarrow A$. Informally, this is saying that $\mathbb{N}$ is the smallest infinite set.

#### Definition 27

A set $A$ is
1. Countably infinite if there exists a bijective function $f:\mathbb{N}\rightarrow A$.
2. Countable if it is finite (possibly empty) or countably infinite.
3. Uncountable if it is not countable.

#### Proposition 28

A set $A$ is countable if and only if there exists an onto function $f:\mathbb{N}\rightarrow A$. Informally, this is saying that $\mathbb{N}$ is the largest countable set.

**Note:** If $A \subset B$ and $A$ is uncountable, then $B$ is also uncountable. On the other hand, if $B$ is countable, then $A$ must also be countable.

To decide whether numbers like $-\sqrt{2}, \; \sqrt [3]{11}$ are rational, we is develop one simple tool: Given $l \in \mathbb{N}$ and $c_{0},\; c_{1}, ... c_{l}\in \mathbb{Z}$, the expression $c_{l}x^{l}+ c_{l-1}x^{l-1}+ \cdots + c_{1}x + c_{0}$ is an integer polynomial with degree $l$.

#### Definition 29

A number $a \in \mathbb{R}$ is called *algebraic* if $p (a)= 0$ for some integer polynomial $p$; otherwise $a$ is *transcendental*.

Every $a \in \mathbb{Q}$ is algebraic:

$$
\begin{align}
a & = \frac{k}{m}\\
p (x) & = mx-k \\
p (a) & = 0.
\end{align}
$$

The two numbers above are also algebraic.

#### Theorem 30

Let $p (x)= c_{l}x^{l}+ c_{l-1}x^{l-1}+ \cdots c_{1}x + c_{0}$ be an integer polynomial. If $p (k/m)= 0$, where $k \in \mathbb{Z}, \; m \in \mathbb{N}$ have no common factor. Then
- $k$ divides $c_{0}$.
- $m$ divides $c_{l}$.

**Proof:** 

$$
\begin{align}
0 & = m^{l}p (k/m) = m^{l}\left( c_{l}\frac{k^{l}}{m^{l}} + c_{l-1}\frac{k^{l-1}}{m^{l-1}} + \cdots + c_{1}\frac{k}{m}+ c_{0} \right)\\
& = c_{l}k^{l} + c_{l-1}k^{l-1} + \cdots c_{1}k + c_{0}m^{l}.
\end{align}
$$

From here, $m \mid c_{l}k^{l}$ so $m \mid c_{l}$ and $k \mid c_{0}ml$ and $k \mid c_{0}$.

You know this from MATH 228.

Don't forget to rearrange this later.

#### Lemma 31

For every $j \in \mathbb{N}$, let $A_{j}$ be countable. Then the set $\bigcup_{j \in \mathbb{N}}A_{j} = \{a \mid a \in A_{j}$ for at least one $j \in \mathbb{N}\}$