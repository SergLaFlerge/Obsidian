# Classical Field Theory

In a field theory, we work with Lagrangians that have $\infty$ degrees of freedom.

## Classical to Quantum Mechanics

We start in a phase space with coordinates $(q,p)$. We can "quantize" this phase space through some operation that translates us into a Hilbert Space. That gives us our familiar classical and quantum counterparts. Basically, we get our hats in our variables.

## Special Relativity

Recall vectors are of the form $A^{\mu}$ and covectors have the form $A_{\nu}$. They are related by a metric $g_{\mu\nu}$. The metric has the property that $g_{\mu\nu}g^{\mu\alpha} = \delta_{\nu}^{\alpha}$. For us, we will take 
<br>
$$
g_{\mu\nu} = \begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & -1 & 0 & 0 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & -1
\end{bmatrix}.
$$

This is "Wrong," as when we take the length of a vector, it comes out as negative. The GR convention is $-g_{\mu\nu}$ gives the correct positive result.

In QFT, we use functionals, which are similar to functions. just like how functions map numbers to numbers, functionals map functions to numbers. A very common functional we are already familiar with is the delta function. Indeed:

$$
\int_{-\epsilon}^{\epsilon}\cdots\delta(x-x_{0})\dd{x} = \text{number.}
$$

We are using calculus of variations. We don't take derivatives of functionals, we take variations. for a function $F$, the so-called first variation is notated as $\delta F$. Some common rules:

$$
\begin{align}
\frac{\delta f(x)}{\delta f(y)} &= \delta(x-y)\\ [1em]
\frac{\delta f^{2}(x)}{\delta f (y)} &= 2f(x)\cdot \delta f(x).
\end{align}
$$

## Principle of Least Action

We have fairly robust knowledge of this. By minimizing the Action $\mathcal{A}$, we obtain the Euler-Lagrange equation:

$$
\dv{t}\left(\pdv{L}{\dot{q}_{r}} \right) = \pdv{L}{q_{r}}.
$$

However, we cannot use Lagrangians directly to do QFT, as it is a strictly classical object. For this we need the Hamiltonian, which is related to the Lagrangian via the Legendre transform, which takes $(q,\dot{q})\to (q,p)$.

