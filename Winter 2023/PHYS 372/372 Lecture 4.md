Last time, we were left with

$$
\Psi (x, t) = \sum\limits_{n} \exp \left(\frac{-iE_{n}t}{\hbar}\right) C_{n}\psi_{n} (x).
$$

That's great, but how do we go about finding the $C_{n}$'s? We can exploit the fact that the $\psi_{n}$'s are orthogonal. This makes sense: If we've already established that linear combinations of individual $\psi_{n}$'s also form solutions, then they must be linearly independent. Mathematically,

$$
\begin{align}
\int_{-\infty}^{\infty} \psi^{*}_{n}\psi_{m}dx = \delta_{nm}.
\end{align}
$$

Assuming we know the equation of state, all we need to do is evaluate the integral

$$
C_{n}= \int_{-\infty}^{\infty}\psi^{*}\cdot \Psi (x, 0)dx.
$$

These coefficients have a special meaning:

$$
\begin{align}
|\Psi|^{2}& = \int_{-\infty}^{\infty} \Psi{*}\cdot \Psi dx \\
& = \sum\limits_{n}\sum\limits_{m}C^{*}_{n}\exp \left(\frac{-iE_{n}t}{\hbar}\right)\cdot C_{m}\exp\left(\frac{-iE_{m}t}{\hbar}\right) \cdot \overbrace{\int_{-\infty}^{\infty}\psi^{*}\cdot \psi dx}^{\delta_{nm}},
\end{align}
$$

so when $n = m$,

$$
|\Psi (x, t)|^{2} = \sum\limits_{n}|C_{n}|^{2}= |C_{1}|^{2}+|C_{2}|^{2}+... = 1
$$

The coefficients then tell us the probability of our particle being in that specific state.

## Observables Described by $\hat{Q}$

$$
\hat{Q} \psi_{n}^{Q} = q_{n}\psi^{Q} 
$$

$q_{n}$ is an eigenvalue, and  $\psi_{n}^{Q}$ is an eigenfunction. Any quantum observables written in terms of one operator can be written in terms of another operator

$$
\Psi (x, t) = \sum\limits_{n}C_{n}^{Q}(t)\psi_{n}^{Q}.
$$

Note how $\psi_{n} (x) \neq \psi_{n}^{Q}(x)$. They are different solutions for different eigenvalue problems. One is able to switch between two operators by changing basis and solving the eigenvalue problem in terms of the new operator. The first term here is the special Hamiltonian case, while the second term is a general case.

# The Infinite Square Well

![[372 Infinite Square Well |center]]

We have a region between $x = 0$ and $x = a$ with zero potential, and the rest of space has infinite potential. Mathematically,

$$
\begin{align}
V =
\begin{cases}
0, \; 0 \leq x  \leq a \\
\infty, \; \text{else}
\end{cases}
\end{align}
$$

This first region has what we call "free motion." This implies

$$
\begin{align}
\hat{H} & = \frac{p^{2}}{2m} \rightarrow \hat{H}\psi = E \psi \\[1em]
-\frac{\hbar^{2}}{2m}\frac{d^{2}}{dx^{2}}\psi & = E \psi.
\end{align}
$$

The solution for this region has the form

$$
\begin{align}
\psi & = A \sin (kx)+ B \cos (kx)\\
k & = \frac{\sqrt{2mE}}{\hbar}.
\end{align}
$$

In order to further refine our answer, we recall some physical and mathematical conditions:

**Physical Conditions:**
- $\psi$ is continuous
- $\psi (x)= 0$ for $V (x)= \infty$

**Mathematical Conditions**
- $\psi(0)= \psi (a)= 0$

With this, we can infer

$$
\begin{align}
\psi (0) & = 0 \Rightarrow B = 0 \\
\psi (x) & = A \sin (kx)\\
\psi (a) & = 0 \Rightarrow k = \frac{n \pi}{a}\\
& \therefore\\
	\psi (a) & = A \sin \left(\frac{n \pi}{a}x \right).
\end{align}
$$

We also know that

$$
\begin{align}
k & = \frac{\sqrt{2mE}}{\hbar} = \frac{n \pi}{a}\\[1em]
E_{n} & = \frac{n^{2}\hbar^{2}\pi^{2}}{2ma^{2}}
\end{align}
$$

Boundary conditions $\rightarrow$ discreet Hamiltonian spectrum.

$$
\psi = \sum\limits_{n}A_{n}\sin \left(\frac{n \pi}{a}x \right).
$$

To find $A_{n}$, we use the normalization condition,

$$
\begin{align}
\int_{-\infty}^{\infty}|\Psi (x, t)|^{2}dx & = |A_{n}|^{2}\underbrace{\int_{0}^{a}\sin^{2}\left(\frac{n \pi}{a}x \right) dx}_{a/2} = 1\\[1em]
A_{n}& = \sqrt{\frac{2}{a}}\cdot e^{i \varphi_{n}}.
\end{align}
$$

The complex component is there to generalize the answer, as our coefficient *could* be negative. It cancels out here, so

$$
\psi (x) = \sqrt{\frac{2}{a}}\sin \left(\frac{n \pi}{a}x \right).
$$

The general solution is then a linear combination of these individual solutions

$$
\begin{align}
\Psi (x, t) & = \sum\limits_{n} \exp\left(\frac{-iE_{n}}{\hbar}t \right) \psi_{n}(x)\\[1em]
\Psi (x, 0) & = \sum\limits_{n}C_{n}\sqrt{\frac{2}{a}}\sin \left(\frac{n \pi}{a}x \right)\\[1em]
C_{n} & = \sqrt{\frac{2}{a}}\int_{0}^{a}\sin \left(\frac{n \pi}{a}x \right) \sin \left(\frac{m \pi}{a}x \right) dx
\end{align}
$$