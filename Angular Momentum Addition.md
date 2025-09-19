Two key things to remember:
1. For a particle with total angular momentum $\mathcal{l}$, $\mathcal{l}$ remains *fixed*.
2. The $z-$component can take on any integer value $-l, ... , l$.

We already talked about how a ket $\ket{\mathcal{l}\; m}$ can be assigned to some vector of dimension $2l+1$. We also know that 

$$
\begin{align}
\hat{L}^{2} \ket{\mathcal{l} \; m} &= \hbar^{2}\mathcal{l}(\mathcal{l}+1)\ket{\mathcal{l} \; m}.  
\end{align}
$$

We want to figure out what $\hat{L}^{2}$ is as a matrix based on the above. Since by point 1 $l$ is fixed, that means $l(l+1)$ is also fixed, i.e. it has the same value regardless of the value of $m$. Therefore

$$
\begin{align}
\hat{L}^{2} &= \hbar^{2}l(l+1)*\text{Id}_{2l+1}.
\end{align}
$$

Where Id is the $2l+1$ identity matrix.


You can also naively think of "canceling" the $\ket{l \; m}$ on both sides. since the LHS is a matrix, what remains on the RHS must also be a matrix, and so for the RHS constant to be a matrix is to multiply it by the identity matrix.

For the $\hat{L}_{z}$ component, the only difference is that $m$ is *not* fixed. It has to take into account all $2l+1$ values of $m$. We can see that from 

$$
\begin{align}
\hat{L}_{z} \ket{l \; m} = \hbar m \ket{l \; m}.  
\end{align}
$$

so the matrix is not just some constant times the identity matrix. It is instead a diagonal matrix that contains every possible value of $m$:

$$
\begin{align}
\hat{L}_{z} = \hbar 
\begin{bmatrix}
l & 0 & 0 & \cdots & 0 \\
0 & l-1 & 0 & \cdots & 0 \\
0 & 0 & \ddots & \cdots & 0 \\
\vdots & \vdots & \vdots & -l+1 & 0 \\
0 & 0 & 0 & 0 & -l
\end{bmatrix}
\end{align}
$$