$$
\begin{align}
\comm{\hat{S}_{x}}{\hat{S}_{y}} & = i\hbar \hat{S}_{z} \\[1 em]
\hat{S}^{2}\ket{sm} & = \hbar^{2}s (s + 1)\ket{sm} \\[1 em]
\hat{S}_{z} \ket{sm} & = \hbar m \ket{sm} \\[1 em]
\ket{S} & = \sum\limits_{m =-s}^{s}C_{m}(t)\ket{sm}
\end{align}
$$

$s$ is allowed to be an integer or half-integer. Let us consider $\bar{C}(t)$ as a row vector, i.e. $\bar{C}(t)=[C_{s}, C_{s-1}, \cdots C_{-s}]^{T}$. $\bar{C}(t)$ has dimension $2 s + 1$. Then, using the definition of $\ket{S}$, we can write $\ket{ss}=[1, 0, 0, \cdots, 0]^{T}$, $\ket{s (s-1)}=[0, 1, 0, \cdots, 0]^{T}$, and so on. $\hat{S}^{2}$ and $\hat{S}_{z}$ are then $(2 s + 1)\times (2 s + 1)$ matrices, with

$$
\begin{align}
\mel{sm'}{\hat{S}^{2}_{mm'}}{sm} & = \hbar^{2}s(s + 1)\underbrace{\ip{sm'}{sm}}_{\delta_{m' m}} \\[1 em]
\hat{\vec{S}}^{2} & = \hbar^{2}s (s + 1)\cdot I_{2 s + 1},
\end{align}
$$

with $I_{2 s + 1}$ being the $2 s+ 1$ dimensional identity matrix. Similarly for $\hat{S}_{z}$:

$$
\begin{align}
S_{z\;\text{min}} & = \mel{sm'}{\hat{S}_{z}}{sm} = \hbar m \underbrace{\ip{sm'}{sm}}_{\delta_{m'm}} \\[1 em]
S_{z} & = \hbar \begin{bmatrix}
s & 0 & 0 & 0 \\
0 & s-1 & 0 & 0 \\
0 & 0 & \ddots & \vdots \\
0  & 0 & \cdots & -s
\end{bmatrix}.
\end{align}
$$

Using ladder operators, we can explore more properties. Applying $\hat{S}_{+}$ gives

$$
\hat{S}_{+}\ket{sm} = b_{sm}\ket{s (m + 1)}.
$$

We can find the norm of $\hat{S}_{+}\ket{sm}$:

$$
\begin{align}
\bra{\hat{S}_{+}sm} & = \bra{sm}(\hat{S}_{+})^{\dagger} \\[1 em]
\norm{\hat{S}_{+}} & = \mel{sm}{\hat{S}_{-}\hat{S}_{+}}{sm} \\[1 em]
& = \mel{sm}{\hat{\vec{S}}^{2}-\hat{S}_{z}^{2}-\hbar \hat{S}_{z}}{sm} \\[1 em]
& = (\hbar^{2}s (s + 1)-\hbar^{2}m^{2}-\hbar^{2}m)\ip{sm} \\[1 em]
& = \ip{\hat{S}_{+}sm} \\[1 em]
& = b_{sm}b_{sm}\ip{s (m + 1)} \\[1 em]
\abs{b_{sm}}^{2} & = \hbar^{2}[s (s + 1)-m (m + 1)].
\end{align}
$$

Then

$$
\begin{align}
(S_{+})_{m' m} & = \mel{sm'}{\hat{S}_{+}}{sm} \\[1 em]
\hat{S}_{+} & =\begin{bmatrix}
0 & b_{s (s-1)} & 0 & 0 \\
0 & 0 & b_{s (s-2)} & 0 \\
0 & 0 & 0 & \ddots \\
0 & 0 & 0 & 0
\end{bmatrix}
\end{align}
$$

## Spin 1/2 Case

We look at the case where $s = \frac{1}{2}$ and $m = \pm \frac{1}{2}$. Dimensionality of our matrices is given by $2 s + 1$, so we will have simple $2 \times 2$ matrices. $b_{\frac{1}{2}, \frac{1}{2}}= \hbar \left( \frac{1}{2}\left( \frac{1}{2}+ 1 \right)-\frac{1}{2}\left( \frac{1}{2}+ 1 \right) \right)= 0$, and $b_{\frac{1}{2},-\frac{1}{2}} = \hbar$. Then

$$
\begin{align}
\hat{S}_{z} & = \frac{\hbar}{2}\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix} \\[1 em]
\hat{S}_{+} & = \hbar\begin{bmatrix}
0 & 1 \\
0 & 0
\end{bmatrix} \\[1 em]
\hat{S}_{-} & =  \hbar\begin{bmatrix}
0 & 0 \\
1 & 0
\end{bmatrix} \\[1 em]
\hat{S}_{x} & = \frac{\hat{S}_{+}+ \hat{S}_{-}}{2} = \frac{\hbar}{2}\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix} \\[1 em]
\hat{S}_{y}& = \frac{\hat{S}_{+}-\hat{S}_{-}}{2i} = \frac{\hbar}{2}\begin{bmatrix}
0 & -i \\
i & 0
\end{bmatrix}
\end{align}
$$

The matrices $\hat{S}_{xyz}$ can be written as $\hat{S}_{xyz}= \frac{\hbar}{2}\sigma_{xyz}$, with

$$
\begin{align}
\sigma_{x} & = \begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix} \\[1 em]
\sigma_{y} & = \begin{bmatrix}
0 & -i \\
i & 0
\end{bmatrix} \\[1 em]
\sigma_{z} & = \begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}.
\end{align}
$$

These are known as the *Pauli spin matrices*. From here, we just need to solve a simple eigenvalue problem:

$$
\begin{align}
\frac{\hbar}{2}\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} & = 
\pm \frac{\hbar}{2}\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} \\[1 em]
\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} & =\begin{bmatrix}
 1 \\
0
\end{bmatrix} \\[1 em]
\begin{bmatrix}
\alpha \\
\beta
\end{bmatrix} & =\begin{bmatrix}
 0 \\
1
\end{bmatrix}.
\end{align}
$$

Rinse and repeat for all the other spin matrices. The two eigenvectors are called spin-up and spin-down respectively. Since an electron has spin 1/2, something-something for later.