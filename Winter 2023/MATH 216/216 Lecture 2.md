# Proofs Continued

#### Theorem 4

For any 2 positive real numbers $a, b$, let $AM (a, b)= (a + b)/2$ be the arithmetic mean of $a$ and $b$. Then

$$
\begin{align}
AM \left(\frac{1}{a}, \frac{1}{b}\right) \geq \frac{1}{AM (a, b)}
\end{align}
$$

and the equality is strict unless  $a = b$.

**Proof:** (Preliminary version).

What we want is

$$
\frac{\frac{1}{a}+ \frac{1}{b}}{2}\geq \frac{1}{\frac{a + b}{2}}.
$$

We just want to play with this, see what happens:

$$
\begin{align}
\frac{b + a}{ab}& = \frac{1}{a}+ \frac{1}{b}\geq \frac{4}{a + b}\\
a^{2}+ ab + b^{2}& = (a + b)^{2}\geq 4ab \\
(a-b)^{2} &\geq 0.
\end{align}
$$

This is a true statement, but we arrived at this statement using the theorem we want to prove. But now, we can say

$$
\begin{align}
(a + b)^{2}-4ab & = (a-b)^{2}\geq 0 \\
& \Rightarrow (a + b)^{2} \geq 4ab \\
AM (1/a, 1/b)& = \frac{1}{2}\left(\frac{1}{a}+ \frac{1}{b}\right) = \frac{a + b}{2ab}\geq \frac{2}{ab}= \frac{1}{AM (a, b)}
\end{align}
$$

And this proves our statement.

#### Theorem 5

Let $k, l$ be integers, $l \neq 0$, then

$$
\frac{k^2}{l^{2}}\neq 2
$$

**Proof:**  Suppose S2 is false, i.e. $k^2/l^{2}= 2$.

This implies that

$$
k^{2}= 2l^{2}.
$$

By [[216 Lecture 1#^8ad4d0|Theorem 1]], $2 \mid k$, i.e. $k = 2j$ for some integer $j$. Is

$$
\begin{align}
k^{2}& = 4j^{2}= 2l^{2}\\
l^{2}& = 2j^{2}
\end{align}
$$

which implies that $2 \mid l$, but $k$ and $l$ are not common factors, so we arrive at a contradiction.

The main challenges of this course are
- Rigor
- Symbolism/jargon
- Abstraction

They are all indispensable. To help with all these,
- Clear logical thinking, practice, etc.
- Practice
- Think of concrete examples

A few important symbols:
- S1$\Rightarrow$ S2, if S1 then S2
- S1 $\Leftrightarrow$ S2, S1 if and only if S2
- You know all the rest.

# Sets and Functions

A set is a collection of distinct objects, called the "elements" of the set.

Two important aspects of this "definition":
1. A set contains each of its elements *only once*, and the order doesn't matter
2. For every set $A$ and every object $a$ we can, at least in principle, decide whether $a \in A$.

This definition is very general, but we will use it only for numbers and functions and such. We can define sets in many ways:
- Verbally:
	- $\mathbb{Z}$, the set of integers
	- $\mathbb{N}$, the set of natural numbers.
- Write down a defining property:
	- $\mathbb{N}= \{k \in \mathbb{Z}:d < 0\}$
- List enough elements to get an idea
	- $\mathbb{N}= \{1, 2, 3, ... \}$

There are a few special sets, such as $\varnothing$, the empty set. Set specific symbols include
- $A \subset B$
- $A = B$
- $A \cap B$
- $A \cup B$
- $A \smallsetminus B$
- $|A|$, $\#A$— cardinality of $A$.

We will see many sets, and we will also see many functions.

## Functions

A function $f$ from $A$ to $B$, where $A, B$ are non-empty. You can think of $f$ as a rule from moving an element of $A$ to $B$. It assigns to *every* element of $A$, a *unique* element on $B$. We write function as

$$
\begin{align}
f: \begin{cases} A \rightarrow B \\
a \mapsto b
\end{cases}
\end{align}
$$

Or we can simply write $f:A \rightarrow B$ in this course. We can define function using
- Formulae $(f:\mathbb{N})\rightarrow \mathbb{N}$ with $f (n)= n^2$
- We can also describe a function verbally ($f (n)= n$th prime number)

Few notions on functions:

$$
f:A \rightarrow B
$$

$A$ is called the domain of $f$.

$B$ is called the codomain or target.

$f (A)$, the image of the entire set, is called the range.

$\forall C \subset A$, $f (C)$ is called the image of $C$.

$\forall B \subset D$, $f^{-1}(D)$ is called the pre-image of $D$

### Properties of Functions

We have a standard function $f:A \rightarrow B$, $A, B$ non-empty.

1. One-to-one (injective) if $\forall b \in B$, the set $f^{-1}(b)$ contains at most *one* element. (1-1)
2. Onto (surjective) if $\forall b \in B$, the set $f^{-1}(b)$ contains *at least* one element. 
3. Bijective if it is both injective and surjective.

If $f:A \rightarrow B$  is injective, we can define an inverse function within its range $f^{1}:f (A) \rightarrow A$ which is itself defined by $f^{-1}(b)= a\in A$. This only makes sense if $f$ is injective or bijective. Note: $f^{-1}(D)$ always makes sense $\forall \; D \subset B$, but $f^{-1}(b)$ only makes sense if $f$ is injective or bijective.

We will use function for many different purposes. For example, comparing the "size" of sets; if $f$ is a 1-1 function from $A$ to $B$, then we know that $B$ is at least as large as $A$, so $A$ is "not larger" than $B$. If $f$ was instead onto, then we think of $B$ being at least as large as $A$, so $A$ is "not smaller" than $B$. 