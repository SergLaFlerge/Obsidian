# What is Differential Geometry?
It certainly involves vector calculus, which is a generalization of single variable calculus to functions of the type

$$
f:\mathbb{R}^{n} \mapsto \mathbb{R}^{m}.
$$

Differential geometry asks: is it possible to generalize this further? The answer is yes! And this generalization takes us from functions to smooth manifolds.

Let us do a bit of background work first: A model space that we are familiar with is Euclidean n-space, denoted $\mathbb{R}^{n}$. If

$$
\begin{align}
x^{i}\in \mathbb{R}, \\[1 em]
(x^{1}, x^{2}, ... x^{n}) \in \mathbb{R}^{n}\equiv x
\end{align}
$$

Is a vector space of dimension n. This space has several properties: If $x$ and $y \in \mathbb{R}^{n}$, then $x + y \in \mathbb{R}^{n}$, and for $a \in \mathbb{R}$, we have $ax = a \cdot (x^{1}, x^{2}, ...)\in \mathbb{R}^{n}$. These are just the linear properties of any vector space. Furthermore, $\mathbb{R}^{n}$ is known as a *metric* space, which gives us a notion of distance between points in $\mathbb{R}^{n}$. This distance is given by

$$
d (x, y) = \sqrt{\sum\limits_{i = 1}^{n}(x^{i}-y^{i})^{2}}.
$$

Then, $d (x, y)\geq 0$, $d (x, y)= d (y, x)$, and $d$ follows the triangle inequality.

$\mathbb{R}^{n}$ is also known as a *topological space*: Let us start with an open ball in $\mathbb{R}^{n}$. This is defined as

$$
\mathrm{B}_{a}(x) = \{y \in \mathbb{R}^{n}\mid d (x, y) < a \}.
$$

A non-empty union of open balls around $x$ is known as a *neighborhood* of $x$. We may also define a closed ball,

$$
\overline{\mathrm{B}_{a}(x)} = \{y \in \mathbb{R}^{n}\mid d (x, y)\leq a \}.
$$

Notice the only difference is the equality appearing in $\overline{\mathrm{B}_{a}(x)}$. Now we can get far enough into topology for our purposes.

Let $\mathcal{J}$ be a subset of the power set of $\mathbb{R}^{n}$ such that
1. The empty set belongs to $\mathcal{J}$.
2. $\mathbb{R}^{n}$ belongs to $\mathcal{J}$.
3. All finite intersections of open balls belong to $\mathcal{J}$.
4. All unions of open balls are in $\mathcal{J}$.

 $\mathcal{J}$ is then a *topology* for $\mathbb{R}^{n}$, whose basis consists of open balls.

In this topology, $\mathcal{J}$ is also a *Hausdorff* space, meaning that, for $x \neq y$, there exists open balls around $x$ and $y$ such that their intersection is empty (they don't intersect.)

## Topological Manifolds

A homeomorphism is a bijection between topological spaces that maps open sets to open sets, whose inverse *also* maps open sets to open sets (which is the same as saying the mapping and its inverse are continuous.)

A topological space is called *second-countable* if its topology has a countable basis (1-1 correspondence to the natural numbers.)

A topological manifold of dimension n (or a topological n-manifold) is a second-countable Hausdorff space such that every point has neighborhoods (coordinate neighborhoods) homeomorphic to neighborhoods of a point in $\mathbb{R}^{n}$

*insert image one day*

A coordinate neighborhood $\mathcal{O}$ with its corresponding homeomorphism

$$
\varphi: M \supset U \mapsto \mathcal{O} \subset \mathbb{R}^{n}
$$

is called a *coordinate chart*. A collection of charts that covers $M$ is called an *atlas*.