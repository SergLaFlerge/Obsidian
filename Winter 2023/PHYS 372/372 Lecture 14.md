# Formalism of Quantum Mechanics

The formalism of quantum mechanics is based on two key constructs:
1. The wavefunction, which tells us the state of the physical system.
2. Operators, which are connected to observables.

One way to describe the wavefunction is to use Schrödinger's equation explicitly. Because of its nature, quantum mechanics using this formalism is called *wave mechanics*.

We could instead write the Schrödinger equation like

$$
i \hbar \pdv{t}C^{Q}(t) = \hat{H}C^{Q}(t).
$$

Where the $C$s are matrices. This is known, of course, as *matrix mechanics*.

Is there a more general formulation where we could use both as we see fit? The answer is yes, and we call it the *geometric approach*. This uses a special tool called the *Hilbert Space*.

First, let us look at Newton's Law: If you recall, there are different ways to describe $\vec{F}= m \vec{a}$. You could do it in the standard Cartesian coordinates, or if the problem has some sort of radial symmetry, you may describe it in polar coordinates instead.

Hilbert spaces usually have infinite dimensions, but we can pretend that there is some problem where the Hilbert space is only 2-dimensional.

Before, we had some states $\Psi (x, t)$ where their sum would be another solution. In other words $\Psi = \sum\limits_{n}C_{n}^{Q}(t)\psi_{n}(x, t)$. In our new approach, $\Psi (x, t)$ and $C_{n}^{Q}(t)$ are treated the same: they are functions and represent basis vectors of our Hilbert space.

The Hilbert space has many interesting properties, but we will only look at the ones that help us in this course. 
1. Its main feature, as stated before, is that it is generally $\infty$-dimensional. 
2. Here, the elements, or vectors of the Hilbert space will be represented by $\ket{\alpha}$. This is called a ket, but we won't worry about the name for now. 
3. Hilbert space is also linear, so addition and scalar multiplication is respected. 
4. Every element $\ket{\alpha}$ has a conjugate $\bra{\alpha}$.
5. There exists a generalization of the dot product called the inner product $\ip{\alpha}{\beta}$.

Next, we look at some properties of the inner product specifically:
1. The inner product is also linear, unsurprisingly. $\ip{\alpha}{b \beta + c \gamma}= b \ip{\alpha}{\beta}+ c \ip{\alpha}{\beta}$. $a, b, c$ can be complex, unlike our usual 3-D case.
2. $\ip{\alpha}{\alpha}= \norm{\alpha}^{2}$. This is called the norm squared of $\alpha$. This is a positive number, and is again a generalization of the notion of length of a vector in 3-D.
3. $\ip{\alpha}{\beta}= \ip{\beta}{\alpha}^{*}$.
4. Cauhcy-Shwartz inequality:$\norm{\ip{\alpha}{\beta}}^{2}\leq \norm{\alpha}^{2}+ \norm{\beta}^{2}$. Classic result from complex analysis.
5. The space is "complete," meaning you can write any function in terms of the basis vectors (which are also functions). You can even write any function as a sum of any elements in the space. The inner product space is complete with respect to the norm $\norm{\alpha}$.

## Dimension

The dimension is $N$ which is given by the number of linearly independent elements. To find the number of elements, we need to find the basis.

### Basis

The basis is composed of $N$ linearly independent elements, which shall be denoted $\ket{e_{j}}$ for $j \in \{1, \dots N \}$. We want 

$$
\ip{e_{j}}{e_{i}} = \delta_{ij}.
$$

Any vector $\ket{ \alpha}$ can be represented as a sum

$$
  \ket{ \alpha} = \sum\limits_{i}a_{i}\ket{ e_{i}},    
$$

and

$$
a_{i} = \ip{e_{i}}{\alpha}.
$$

We can do this because

$$
\ip{a_{i}}{\alpha} = \sum\limits_{i}a_{i}\underbrace{\ip{e_{j}}{e_{i}}}_{\delta_{ij}}  = a_{i}.
$$

Also:

$$
\begin{align}
\ip{\alpha}{e_{i}} & = a_{i}^{*} \to \bra{ \alpha} = \sum\limits_{i}a_{i}^{*}\bra{ e_{i}},\\[1em]
\ip{\alpha}{\beta} & = \sum\limits_{i}^{N}\sum\limits_{j}^{N}a_{i}^{*}b_{j}\underbrace{\ip{e_{i}}{{e_{j}}}}_{\delta_{ij}} = \sum\limits_{i}a_{i}^{*}b_{i}
\end{align}
$$