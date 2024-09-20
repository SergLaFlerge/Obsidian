# Lecture 1

Analysis is just calculus for grown ups.

Tips for success:

1. Attend class and take careful notes.
2. Do the homework!
3.  When in doubt, just ask :)

# Foundations

## Logic

A statement in math a declarative sentence that is either true or false. For example:

- 5 is an odd integer (true).
- 4 is a prime number (false).
- Edmonton is nice. 
- This statement is false (paradox).

The first two statements are the type which we are interested in. More specifically, we are interested in logical relations between statements. For instance, consider the following statements about any integer $k$:

1. 2 divides $k$ (true if $k$ is even, false otherwise).
2. 2 divides $k^2$ (same thing).

**Claim:** 1 implies 2 ($1 \Rightarrow 2$ ).
If 1 is true, then 2 is also true.
1 is sufficient for 2.
1 only if 2.
2 is necessary for 1.

These are all equivalent statements. The reason is that if $k = 2 \cdot l$, then $k^{2}= 4 \cdot l^{2}= 2 (2l^{2})$, so 2 divides $k^2$ (i.e. 2 is true). The converse is also true; if $2 \mid k^2$, then $2 \mid k$, and the  reason is similar.

In summary, $1 \Leftrightarrow 2$ which can be read as

1 is equivalent to 2
1 if and only if 2
1 is necessary and sufficient for 2

We have now proved our first theorem:

#### Theorem 1

^8ad4d0

For every integer $k$, the following are equivalent:

1. $2 \mid k$
2. $2 \mid k^2$

Remark: Theorem 1 remains true if 2 is replaced by 3, or any prime number, or even with any $p \cdot q$ where $p$ and $q$ are prime numbers, and $p \neq q$.

We claim that theorem 1 is false if 2 is replaced by 4. To see this, consider these statements

3. $4 \mid k$
4. $4 \mid k^2$

If $3 \Rightarrow4$, then $k = 4l$, and $k^{2}= 16l^2$. But in general, 4 does not imply 3. All we need is a number where 4 is true, and 3 is false. The solution is that any integers in the form of $2 \mod 4$ will have this property.

We will see many true statements in MATH 216; they will take one of the following forms:

- Theorems: Very important, with proof, or an outlined proof.
- Lemmas: A sort of auxiliary.
- Corollary: Immediate consequence of a theorem or lemma.
- Proposition: Requires proof, but will not be given in this course.
- Axiom: Basic truth.

## Proofs

In MATH 216, we insist on proofs.

A proof is a complete, transparent explanation of why the statement is true. Using only

1. True statements proved earlier, or
2. Axioms.

Why are proofs so important in analysis? Because we almost always deal with infinity, explicit or otherwise. Theorem 1 already deals with infinity implicitly. Intuition also often fails when dealing with infinity.

**Example** Can we make sense of $a = 1-\frac{1}{2}+ \frac{1}{4}-\frac{1}{8}+...$? We can break $a$ in different ways:

$$
\begin{align}
a & = 1 + \left(\frac{-1}{2}+ \frac{1}{4}\right)+ \left(\frac{-1}{8}+ \frac{1}{16}\right)< 1 \\[1em]
a & = 1-\frac{1}{2} + \left(\frac{1}{4}-\frac{1}{8}\right) > \frac{1}{2}
\end{align}
$$

Algebraically,

$$
\begin{align}
a & = 1-\frac{1}{2}\left(1-\frac{1}{2}+ \frac{1}{4}+...\right) = 1-\frac{1}{2}a \\
\frac{3}{2}a & = 1 \\
a & = \frac{2}{3}
\end{align}
$$

If we apply the same ideas to its inverse, something goes horribly wrong. For $c = 1-\frac{1}{2}+ \frac{1}{3}-\frac{1}{4}+...$ applying the same ideas gives

$$
\begin{align}
c  &< 1 \\
c &> \frac{1}{2}
\end{align}
$$

The point is that infinity is tricky to work with. Our intuition is often wrong. Expressions containing infinity in one form or another must be treated with great care. This is exactly what a proof is needed for.

We will see many proofs in MATH 216. In this introduction, we point out the most basic distinction between proofs: **Direct v.s. Indirect**.

For a direct proof of $1 \Rightarrow 2$, assume 1 is true and use valid and sound reasoning to arrive at 2.

For indirect proofs (also known as proof by contradiction, $1 \nRightarrow 2$), assume 1 is true, and show using valid and sound reasoning that 1 is false by arriving at a contradiction. Every proof in this class will fall into one of these two categories