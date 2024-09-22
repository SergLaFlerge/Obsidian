# Heisenberg Matrix Mechanics

Why use matrix mechanics?
1. Well, it is the most understandable realization of the geometric concept of quantum mechanics. At the end of the day, quantum mechanics is really the theory of Hermitian operators in Hilbert space. The operators are the physical observables, while the Hilbert space represents the quantum space
2. It gives a clear relation between different representations of quantum mechanics.
3. It is used for numerical calculations, so it is useful for practical applications.
4. Frank is crazy about this stuff, so might as well learn it.

What is the main idea? Pretty simple: Recall that the quantum state is described by a wavefunction

$$
\Psi (x, t) = \sum\limits_{n}C_{n}^{Q}(t)\psi_{n}^{Q} (x),
$$

where $\hat{Q}\psi_{n}^{Q}= q_{n}\psi_{n}^{Q}$. We can then express $C_{n}^{Q}$ as

$$
C_{n}^{Q} = \int_{-\infty}^{\infty}\psi_{n}^{*Q}(x)\Psi (x, t)\dd{x}.
$$

Why couldn't we just skip this intermediate step? Let's write down an equation for $C_{n}^{Q}(t)$. It should be equivalent to the Schrödinger equation

$$
\begin{align}
i \hbar \pdv{t}\Psi (x, t) & = \hat{H}\Psi (x, t) \\[1em]
\int_{-\infty}^{\infty}\psi_{n}^{*Q}(x)i \hbar \pdv{t}\Psi (x, t)\dd{x} & = \int_{-\infty}^{\infty}\hat{H}\Psi (x, t) \\[1em]
i \hbar \pdv{t}C_{n}^{Q}(t)& = \sum\limits_{m}\int_{-\infty}^{\infty}\psi_{n}^{*Q}(x)\hat{H}C_{m}^{Q}(t)\psi_{n}^{Q}(x)\dd{x} \\[1em]
i \hbar \pdv{t}\Psi (x, t)C_{n}^{Q}& = \sum\limits_{m}H_{nm}C_{m}^{Q}(t),
\end{align}
$$

where $H_{nm}$ is the matrix element of the Hamiltonian matrix $\hat{H}$. We can then introduce the matrix $\bar{C}(t)^{Q}(t)= (C_{1}^{Q}, C_{2}^{Q}, ...)^{T}$. Then

$$
\begin{align}
i \hbar \pdv{t}\bar{C}^{Q}(t) & = \hat{H}\bar{C}^{Q}(t).
\end{align}
$$

This is the *matrix form* of the Schrödinger equation in the basis of the eigenfunctions of an operator $\hat{Q}$. Naturally, for different $\hat{Q}$, we will have different $\bar{C}^{Q}$ and $\hat{H}$, but the physics will remain the same regardless of the basis. The expectation value of an observable $Q'$ is represented as $\ev{\hat{Q}'}$ or $\ev{\hat{Q}'}{\psi_{t}}$, and

$$
\ev{\hat{Q}'}{\psi_{t}} = \bar{C}^{\dagger Q}\hat{Q}'\bar{C}^{Q}(t),
$$

where $\bra{\psi_{t}}= \bar{C}^{\dagger Q}$ and $\hat{Q}'\ket{\psi_{t}}= \hat{Q}'\bar{C}^{Q}(t)$, and a

$$
\hat{Q}'_{mn} = \int_{-\infty}^{\infty}\psi_{n}^{*Q}(x) \hat{Q}'\psi_{m}^{Q}(x)\dd{x}.
$$

If we look back at Newton's Law $\ddot{\vec{m}}= \vec{F}(\vec{x})$, we may choose $\vec{m}$ to have some basis that describes it as a linear combination of the basis vectors. We can change the basis, but the trajectory of $\vec{m}$ does not change. This structure is very similar to what we now have in our rewritten Schrödinger equation. The main difference is that with Newton's law, we have only $3$ dimensions, whereas in the Hilbert space of quantum mechanics, we (usually) have infinitely many dimensions.

If we let $\infty = 3$ for a minute, we can see that for basis vectors $\ket{e_{1}^{Q}}, \; \ket{e_{2}^{Q}}, \; \ket{e_{3}^{Q}}$, we can write $\ket{\psi_{t}}$ as

$$
\ket{\psi_{t}} = C_{1}^{Q}\ket{e_{1}^{Q}}+ C_{2}^{Q}\ket{e_{2}^{Q}}+ C_{3}\ket{e_{3}^{Q}}.
$$

Obviously this follows for higher dimensional problems. As we'd expect, if we changed the basis, our $C_{n}$'s would change, but the "trajectory" would remain the same. Using these coefficients, we can write

$$
\begin{align}
\int_{-\infty}^{\infty}\abs{\Psi (x, t)}^{2}\dd{x}& =  \ip{\psi_{t}} \\[1em]
& = \bar{C}^{\dagger Q}(t)\bar{C}^{Q}(t) \\[1em]
& = \sum\limits_{n}\abs{C_{n}(t)}^{2}= 1.
\end{align}
$$

Because we cannot change this fact, we also cannot change the basis by "squeezing" or "stretching", only rotating. Therefore the only different between any two representations of $Q$ is the different between the basis in the Hilbert space.

The formal solution of our matrix equation is given by

$$
\bar{C}^{Q}(t) = \exp\left(-i \frac{\hat{H}t}{\hbar}\right)\bar{C}^{Q}(0).
$$

The exponential term is often called $\hat{U}$ and is known as the evolution operator. $\hat{U}$ is unitary, meaning $\hat{U}^{\dagger}= \hat{U}^{-1}$, and $\hat{U}^{\dagger}\cdot \hat{U}= 1$. This tells us that the norm of a quantum state does not depend on time. This makes sense, as

$$
\begin{align}
\ket{\psi_{t}} & = \hat{U}(t)\ket{\psi_{t}} \\[1em]
\ip{\psi_{t}} & = \ev{\hat{U}^{\dagger}(t)\cdot \hat{U}(t)}{\psi_{t = 0}} \\[1em]
& = \ip{\psi_{t}} = 1.
\end{align}
$$

How to deal with the matrix in the exponential? Series expansionnnn.

$$
\exp \left(-i \frac{\hat{H}t}{\hbar} \right) = 1-\frac{i \hat{H}t}{\hbar}+ \frac{1}{2!}\left(\frac{i t}{\hbar} \right)^{2}\hat{H}^{2}+ \cdots
$$

Let us choose $\hat{Q}= \hat{H}$. Then

$$
\hat{H} = \begin{bmatrix}
E_{1} & 0 & 0 & \cdots \\
0 & E_{2} & 0 & 0 \\
0 & 0 & E_{3} & 0 \\
\vdots & 0 & 0 & \ddots
\end{bmatrix}.
$$

This works because $\hat{H}$ is diagonalizable. Powers of diagonal matrices are just the powers of the elements in the matrix. Therefore

$$
\hat{U} = \begin{bmatrix}
e^{-i \frac{E_{1}}{\hbar}t} & 0 & 0 & \cdots \\
0 & e^{-i \frac{E_{2}}{\hbar}t} & 0 & 0 \\
0 & 0 & e^{-i{\frac{E_{3}}{\hbar}t}} & 0 \\
\vdots & 0 & 0 & \ddots
\end{bmatrix},
$$

and so the formal solution is then

$$
C_{n}(t)^{H}= \exp \left(-i \frac{E_{n}}{\hbar}t \right)C_{n}^{H}(0).
$$