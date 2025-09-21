In going from $\mathbb{N}$ to $\mathbb{Z}$, we obtained closure under addition and subtraction, but we still need to fix multiplication. For this, we introduce yet another set of numbers:

## The Rational Numbers $\mathbb{Q}$

The set of rational numbers is closed under addition and multiplication (and naturally subtraction and division.) The set $\mathbb{Q}$ is defined by

$$
\mathbb{Q} = \left\{\frac{k}{l}:\; k, l \in \mathbb{Z}\right\}.
$$

The rational numbers have all the same properties as the integers, with one little twist/upgrade, which is the closure of multiplication. Every number in $\mathbb{Q}\smallsetminus \{0 \}$ has a multiplicative inverse. Arithmetic and order in $\mathbb{Q}$ are pretty nice. Addition is commutative, associative, has a neutral element, and has an inverse element. Same thing for multiplication. Addition and multiplication are compatible in the distributive law.

The rational numbers are considered a **field**. They are also ordered. Given two rational numbers, they are either the same, or one is bigger than the other. This order is compatible with addition and multiplication. Because of this, $\mathbb{Q}$ is actually an ordered field. Even better. Every ordered field $\mathbb{F}$ contains $\mathbb{Q}$ (or more precisely, it contains an isomorphic copy of $\mathbb{Q}$). Thus, $\mathbb{Q}$, in a way, is the smallest ordered field possible.

Once again, moving from $\mathbb{Z}$ to $\mathbb{Q}$, we have gained universal solvability, but we have lost the simple "discreet" structure of $\mathbb{Z}$. There are no numbers between $1$ and $2$ in $\mathbb{Z}$, but in $\mathbb{Q}$, we have an infinite number of, numbers. In a way, $\mathbb{Q}$ is a bit of a mess.

$\mathbb{Q}$ is a beautiful field, but it is not enough for us, because $\mathbb{Q}$ has lots of "holes." To explain this properly, we need a few new terms.

#### Definition 12

A subset $A\neq \varnothing$ of $\mathbb{Q}$ (or any other ordered field $\mathbb{F}$) is **bounded above** and **bounded below** bounded above means there exists a number $s \in \mathbb{Q}$ such that $Q \leq s \; \forall \\; Q \in A$, and same for bounded below, but for numbers less than or equal to.

The smallest (or least) upper bound, or the largest lower bound of $A$ are called the supremum and the infimum respectively, assuming that either are both exist. They are denoted $\sup A$ and $\inf A$.

If either or both exist and if that number belongs to $A$, then we call them a maximum and the minimum, respectively. These are denoted $\max A$ and $\min A$

**Example:** Consider the set $A = \{r \in \mathbb{Q}|\; r > 1, \; r^{2}< 2 \}\subset \mathbb{Q}$. Clearly the set is not empty.

We start with the infimum. The largest lower bound is $1$, the reasoning is that $1$ is a lower bound by definition. From there we have to show that there is no bigger $s$ that can be a lower bound. Consider $s_{n}= 1 + 1/n \in \mathbb{Q}, \; > 1$.

$$
\begin{align}
s_{n}^{2} & = 1 + \frac{2}{n}+ \frac{1}{n^{2 }}= 2-1 + \frac{2}{n}+ \frac{1}{n^{2}}\\
& = 2-\frac{n (n-2)-1}{n^{2}}\\
& \leq p-\frac{2}{n^{2}} \;  \text{if} \; n \geq 3 \\
& < 2
\end{align}
$$

If $n \geq 3$ then $n (n-2)-1 \geq 2$. This implies

$$
\begin{align}
s_{n}^{2} & < 2 \; \forall \; n \geq 3 \\
s_{n} \in A \; \forall \; n \geq 3
\end{align}
$$

Pick only $t > 1, \; t \in \mathbb{Q}$,  and $n > 1/(t-1)$. This implies

$$
t > 1 + STKPRA*BG{1}{n}= s_{n}\in A
$$

This implies that the largest lower bound must be $1$, i.e. $\inf A = 1$. Since $1 \notin A$, $A$ does not have a minimum, only an infimum.

We now claim that $A$ has no supremum. Reason: $A$ surgeon certainly has lots of upper bounds, like $3/2$. Fix any $s > 1$, and consider three cases:

1. $s^{2}< 2$. Consider $$\begin{align} t & = s + \frac{2-s^{2}}{4s}\in \mathbb{Q}, \; > s \\ t^{2} & = s^{2}+ \frac{1}{2}(2-s^{2})+ \frac{(2-s^{2})^{2}}{16s^{2}}\\ & = 2-\frac{1}{2}(2-s^{2})+ \frac{(2-s^{2})}{16s^{2}}\\ & = 2-(2-s^{2})\left(\frac{1}{2}-\frac{2-s^{2}}{16s^{2}}\right) \end{align}$$ and this implies $$t^{2}< 2.$$
2. $s^{2}> 2$. Consider $$\begin{align}t & = s-\frac{s^{2}-2}{4s}\; < s \\ t^{2} & = 2 + (s^{2}-2)\frac{9s^{2}-2}{16s^{2}}> 2s + (s^{2}-2)\cdot \frac{7}{16s^{2}} \end{align}$$ and this implies $t^{2}> 2$ so $t$ is an upper bound, but $t < s$, so $s$ is not the smallest upper bound of $A$.
3. $s^{2}= 2$, which is not even in $\mathbb{Q}$.

Why is this important? Well, many important objects in science are products resulting from a limiting process from other familiar objects. To be practical, this "limit" should be a number, not something esoteric... The above example illustrates exactly what we mean when we say that $\mathbb{Q}$ contains holes.

To solve this problem we need to enlarge our universe of numbers one more time:

## The Real Numbers $\mathbb{R}$

#### Definition 14

The real numbers, denoted by $\mathbb{R}$ is an ordered field with one additional property: It has no holes. Every set $A\neq \varnothing$ that is bounded above has a supremum (least upper bound). This is called the Least Upper Bound property (LUB). ^f9e9d8

#### Remark

It is not obvious at all that an ordered field be the LUB property does exist. The first construction of such fields, using only the property of $\mathbb{Q}$ (or $\mathbb{N}$) are due to Cantor and Dedelkind, circa $1875$.

There is essentially only one ordered field with the property LUB! This is not very obvious either, but neither of these statements are really our business.