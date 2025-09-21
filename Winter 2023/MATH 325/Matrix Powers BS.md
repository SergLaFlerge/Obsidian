# Square Roots of Diagonalizable $2 \times 2$ Matrices

Let $A$ be a complex $2 \times 2$ matrix. We want to find a matrix $B$, such that $B^{2}= B \cdot B = A$. If

$$
A = \begin{bmatrix}
a & 0 \\
0 & b
\end{bmatrix}
$$

is diagonal matrix, it is easy to find such a matrix $B$:

$$
\begin{bmatrix}
\sqrt{a} & 0 \\
0 & \sqrt{b}
\end{bmatrix}^{2}
=
\begin{bmatrix}
a & 0 \\
0 & b
\end{bmatrix},
$$

Where $\sqrt{a}, \sqrt{b}\in \mathbb{C}$ are square roots of $a$ and $b$, respectively. From this with also get a solution if $A$ is not diagonal, but diagonalizable. We then have an invertible matrix $S$, such that $S^{-1}\cdot A \cdot S= \begin{bmatrix}c & 0 \\ 0 & d \end{bmatrix}$ for some complex numbers $c, d$. Then

$$
\begin{bmatrix}
\sqrt{c} & 0 \\
0 & \sqrt{d}
\end{bmatrix}^{2}
=
\begin{bmatrix}
c & 0 \\
0 & d
\end{bmatrix}.
$$

Therefore,

$$
A =
\left[S \cdot
\begin{bmatrix}
\sqrt{c} & 0 \\
0 & \sqrt{d}
\end{bmatrix}
\cdot S^{-1}
\right]^{2}.
$$