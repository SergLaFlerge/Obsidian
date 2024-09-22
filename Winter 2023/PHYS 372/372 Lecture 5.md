Quick summary of the past few lectures:
1. For a time-independent potential $V (x)$, if $V (\infty)= \infty$, our solution is a linear superposition of stationary states.
2. With any operator $\hat{Q}$, $\hat{Q}\psi_{n}^{Q} = q_{n}\psi_{n}^{Q}$, and $\Psi = \sum\limits_{n}C_{n}(t)\psi_{n}^{Q}(x)$.
3. The coefficients $|C_{n}|^2$ are directly related to a probability.
4. $\Psi$ collapses when a measurement is made, $C_{n}^{Q}(t_{0})= 1$, and all others go to zero.
5. In the limit of large quantum numbers, $\langle x \rangle$ and $\langle p \rangle$ are described classically.
6. Given $V (x)$, you can find $E_{n}, \; C_{n},\; \psi_{n}$. You can change basis to find $\langle Q \rangle, \; \sigma_{Q}$.

A condition that we'll need for the finite square well is that

$$
\frac{\partial \Psi}{\partial x}= \text{continuous}.
$$

This will be important later.

# The Harmonic Oscillator

A potential $V (x)$ may not look very nice. It may have many peaks and valleys. These valleys are known as stable equilibria, and they are the places where a particle is most likely to be found. We can approximate these valleys as quadratic equations, and this approximation naturally leads to the idea of harmonic oscillators.

We can expand any potential using a Taylor series expansion:

$$
V (x) = V (x_{0}) +\eval{\pdv{V}{x}}_{x_{0}} (x-x_{0})+ \frac{1}{2}\cdot \eval{\pdv [2]{V}{x}}_{x_{0}}(x-x_{0})^{2}+ \order{x^{3}}.
$$

The first term is irrelevant, as it simply represents a shift of the potential, and we only care about potential *differences*. Because we will be near the equilibrium, the second term (first order derivative) will be approximately zero, so it can be ignored as well. That leaves us with the second order term to worry about.

$$
\begin{align}
V (x) & \approx \frac{k}{2}(x-x_{0})^{2}\\
F (x) & \approx -k (x-x_{0}).
\end{align}
$$

Which is exactly what we would expect from a simple harmonic oscillator.

Now we solve Schrödinger's equation in the simple harmonic oscillator. Without loss of generality, let $x_{0}= 0$. Then,

$$
\begin{align}
\hat{H}\psi_{n} & = E \psi_{n}\\
\left(-\hbar^{2}\dv[2]{x} + \frac{1}{2}m \omega^{2}x^{2} \right)\psi_{n} & = E_{n}\psi_{n}\\
\omega & = \sqrt{\frac{k}{m}}\\
V (\pm \infty) & = 0 \\
\psi (\pm \infty)  & = 0.
\end{align}
$$

If this is anything like the infinite square well, then we expect to have a discrete spectrum of solutions. Before we continue with our solution, we shall introduce the concept of operators, which will massively simplify the work we need to do to obtain our solution.

## Ladder Operators

The ladder operators $\hat{a}_{+}, \; \hat{a}_{-}$ are a set of differential operators. These operators have a special property that we'll explain later. For now, the ladder operators are

$$
\hat{a}_{\pm} = \frac{1}{\sqrt{2\hbar m \omega}}(\mp i\hat{p} + m \omega x).
$$

$\hat{a}_{+}$ and $\hat{a}_{-}$ are called the raising (or creation) operator and lowering (or annihilation) operator, respectively. These names will make sense once we apply them our problem.

Let us explore some properties:

$$
\begin{align}
(\hat{a}_{+})^{*} & = \hat{a}_{-}\\
\hat{a}_{+}^{\dagger} & = \hat{a}_{-}.
\end{align}
$$

So the complex conjugate of one is the other. This also gives us a hint about their commutativity:

$$
\begin{align}
[\hat{a}_{+}, \hat{a}_{-}] = 1 \qq{(proof in notes.)}
\end{align}
$$

So the ladder operators *do not commute*. Something fascinating happens when we examine one of the terms in the commutator (for example, $\hat{a}_{-}\hat{a}_{+}$):

$$
\begin{align}
\hat{a}_{-}\hat{a}_{+} & = \frac{1}{2 \hbar \omega m}(\hat{p}^{2}-i \omega \comm{\hat{x}}{\hat{p}}+ (m \omega x)^{2})\\
& = \frac{1}{2 \hbar \omega m}(\hat{p}^{2}+ m \omega \hbar + (m \omega x^{2}))\\
& =\frac{1}{\hbar \omega}\left(\frac{\hat{p}^{2}}{2m}+\frac{mx^{2}\omega^{2}}{2} \right) + \frac{1}{2}\\
& = \frac{1}{\hbar \omega}\hat{H} + \frac{1}{2}\\
& \Downarrow\\
\hat{H} & = \hbar \omega (\hat{a}_{-}\hat{a}_{+}-1/2)\\
& = \hbar \omega (\hat{a}_{+}\hat{a}_{-}+ 1/2).
\end{align}
$$

Immediately we can see how this helps with our problem:

$$
\begin{align}
\hat{H}\psi_{n} & = E_{n}\psi_{n}\\
\hbar \omega (\hat{a}_{+}\hat{a}_{-}+ 1/2)\psi_{n}& = E_{n}\psi_{n}.
\end{align}
$$

So if $\psi_{n}$ is a solution, then so is $\hat{a}_{+}\psi_{n}$, and so on and so forth.

$$
\begin{align}
\hat{H}(\hat{a}_{+}\psi_{n}) & = E_{n} \psi_{n}\\
& = \hbar \omega (\hat{a}_{+}\hat{a}_{-}+ 1/2)(\hat{a}_{+}\psi_{n})\\
& = \hbar \omega (\hat{a}_{+}\hat{a}_{-}\hat{a}_{+}+ 1/2 \hat{a}_{+})\psi_{n}\\
& = \hbar \omega \hat{a}_{+}(\hat{a}_{-}\hat{a}_{+}+ 1/2)\psi_{n}\\
& = \hbar \omega \hat{a}_{+}(1 + \hat{a}_{+}\hat{a}_{-}+ 1/2)\psi_{n}\\
& = \hbar \omega \hat{a}_{+}(1 + \hat{H}/\hbar \omega)\psi_{n}\\
& = \hat{a}_{+}(\hat{H}+ \hbar \omega)\psi_{n}\\
& = (E_{n}+ \hbar \omega) (\hat{a}_{+}\psi_{n}).
\end{align}
$$

So applying $\hat{a}_{+}$ to $\psi_{n}$ gave us the eigenfunction with eigenvalue $E_{n}$, increased by $\hbar \omega$. The operator has raised the energy of the system, hence the name "raising operator."