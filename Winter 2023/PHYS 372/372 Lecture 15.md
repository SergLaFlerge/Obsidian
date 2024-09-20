Just like in $3$-D, we can write and vector $\ket{\alpha}$ as

$$
\ket{\alpha} = \sum\limits_{i = 1}a_{i}\ket{e_{i}}.
$$

We can write the inner product of two vectors $\bra{\alpha}$ and $\ket{\beta}$ as

$$
\begin{align}
\ip{\alpha}{\beta} & = \sum\limits_{i = 1}a_{i}^{*}\bra{e_{i}}\sum\limits_{j = 1}b_{j}\ket{e_{j}}\\[1em]
& = \sum\limits_{i}a_{i}^{*}b_{i}.
\end{align}
$$

We can think of this multiplication as multiplication of matrices. That is,

$$
\hat{a} = (a_{1},a_{2},a_{3}...)
$$

and

$$
\hat{a}^{\dagger} = 
\begin{pmatrix}
a_{1} \\ a_{2} \\ a_{3} \\ \vdots
\end{pmatrix}
$$

So how do we describe these objects with operators?

## Operators

Operators here will be linear transformations. Call it $\hat{T}$. Then,

$$
\ket{\alpha} \overset{\hat{T}}{\longrightarrow} \ket{\alpha'} \equiv \ket{\hat{T}\alpha}.
$$

Obviously since it is linear, it obeys the rules of linearity. We can also use the Hermitian Conjugate $\hat{T}^{\dagger}$, where

$$
\ip{\alpha}{\hat{T}\beta} = \ip{\hat{T}^{\dagger}\alpha}{\beta}.
$$

Since this is a Hermitian operator, we know it is of the form $Q^{\dagger} =Q$.

### Operators as Matrices

$$
\begin{align}
\ket{\alpha} & = \sum\limits_{i=1}a_{i}\ket{e_{i}}\\[1em]
\ket{\alpha'} & = \ket{\hat{T}\alpha} = \sum\limits_{i=1}a_{i}'\ket{e_{i}}\\[1em]
a_{i}' &= \sum\limits_{i=1}\hat{T}_{ij}a_{j}\\[1em]
\hat{a}' & = \hat{T}\hat{a}.
\end{align}
$$

How is that operator related to the Hermitian Conjugate $\hat{T}^{\dagger}$? Well,

$$
\begin{align}
\ip{\alpha}{\hat{T}\beta} & = \ip{\hat{T}^{\dagger}\alpha}{\beta}\\
& = \ip{\beta}{\hat{T}^{\dagger}\alpha}^{*}.
\end{align}
$$

If we then let $\ket{\alpha} = \ket{e_{i}}$ and $\ket{\beta} = \ket{e_{j}}$, then 

$$
\begin{align}
\ip{\beta}{\hat{T}^{\dagger}\alpha} & = T_{ji}^{\dagger}\\
\ip{\alpha}{\hat{T}\beta} & = T_{ij}^{*}\\
T_{ji}^{\dagger}& = T_{ij}^{*T}.
\end{align}
$$

## Properties of Operators in Hilbert Space

We make the following claims:
1. $\ip{\alpha}{\hat{Q}}\alpha$ is real, and $\ip{\alpha}{\hat{Q}\alpha}^{*} = \ip{\hat{Q}\alpha}{\alpha} =\ip{\alpha}{\hat{Q}^{\dagger}\alpha} =\ip{\alpha}{\hat{Q}\alpha}$.
2. $\hat{Q}$ has $N$ eigenvalues and eigenvectors. $\ket{\hat{Q}e_{n}^{Q}}=q_{n}\ket{e_{n}^{Q}}$, for $n=\set{1, ...,N}$.
3. If $\hat{Q}$ is "good"(or bounded), then $\ket{e_{n}^{Q}}$ forms a basis in Hilbert Space.
4. In the basis $\ket{e_{i}^{Q}}$, the operator is diagonal. $Q_{ij}=q_{j}\delta_{ij}$.

# Dirac Notation

$\ket{\hat{T}\alpha}\rightarrow \hat{T}\ket{\alpha}$. We then call $\ket{\alpha}$ a "ket" vector. Then $\bra{\hat{T}\alpha}\rightarrow \bra{\alpha}\hat{T}^{\dagger}$, and we call $\bra{\alpha}$ a "bra" vector. We will know define

$$
\begin{align}
\ip{\hat{T}\alpha}{\beta} & \equiv  \mel{\alpha}{\hat{T}}{\beta}\\[1em]
T_{ij} & \equiv \mel{e_{i}}{\hat{T}}{e_{j}}.
\end{align}
$$

A main property of the Hilbert space is that it is "square-integrable." That is,

$$
\int_{-\infty}^{\infty}\abs{\alpha (x)}^{2}\dd{x} < \infty.
$$

We want our $Q$ states to behave the same way. Let us define the inner product as

$$
\ip{\alpha}{\beta} = \int_{-\infty}^{\infty}\alpha{*}(x)\beta (x)\dd{x}.
$$

Then, the solutions to the Schrödinger equation all live in Hilbert space!

$$
\begin{align}
\Psi (x, t) &  \longrightarrow \ket{\psi_{t}}.
\end{align}
$$

So with have a quantum state that corresponds to elements (vectors) of the Hilbert space.

## Mapping Quantum Mechanics to Hilbert Space

1. $\Psi (x, t)\longrightarrow \ket{\psi_{t}}$.
2. $\hat{Q}(\hat{x}, \hat{p})\longrightarrow\hat{Q}$.
3. $\hat{Q}\psi_{n}^{Q}= q_{n}\psi_{n}^{Q}(x)\longrightarrow \hat{Q}\ket{\psi_{n}^{Q}}q_{n}\ket{\psi_{n}^{Q}}$.
4. $\int \psi^{*}\psi' \dd{x}\longrightarrow \ip{\psi_{t}}{\psi_{t}'}$.
5. $\int \abs{\Psi (x, t)}^{2}\dd{x}\longrightarrow \ip{\psi_{t}}$.
6. $\langle Q \rangle = \int_{-\infty}^{\infty}\psi^{*}\hat{Q}\psi \dd{x}\longrightarrow \ev{\hat{Q}}{\psi_{t}}$.
7. $\Psi (x, t)= \sum\limits_{n}C_{n}^{Q}(t)\psi_{n}(x)\longrightarrow \ket{\psi_{t}}= \sum\limits_{n}C_{n}^{Q}(t)\ket{\psi_{n}^{Q}}$.
8. $\int_{-\infty}^{\infty}\psi_{n}^{Q}\psi_{m}^{Q}\dd{x}= \delta_{nm} \longrightarrow \ip{\psi_{n}^{Q}}{\psi_{m}^{Q}}= \delta_{nm}$.
9. $\int_{-\infty}^{\infty}\psi_{n}^{*Q}(x)\hat{T}(\hat{x}, \hat{p})\psi_{m}^{Q}\dd{x}\longrightarrow \mel{\psi_{n}^{Q}}{\hat{T}}{\psi_{m}^{Q}}= T_{mn}$
