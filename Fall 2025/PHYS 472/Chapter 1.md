# Angular Momentum Addition

Recall the orbital momentum operator $\hat{ \bar{L}} = \hat{ \bar{\mathcal{r}}}\times\hat{ \bar{p}}$ and $\comm{\hat{ L}_{x}}{\hat{ L}_{y}} = i \hbar \hat{ L}_{z}$. In spherical coordinates, the eigenfunctions are the spherical harmonics $\mathcal{Y}_{l}^{m}(\theta, \phi)$. If we look the the associated quantum numbers for $\hat{ \bar{L}}$ and $\hat{ L}_{z}$, we obtain

$$
\begin{align}
 \hat{ \bar{L}}^{2} \ket{ l\;m} & = \hbar^{2}l (l + 1)\ket{ l\;m} \\[1 em]
\hat{ L}_{z} \ket{ l \; m} & = \hbar m \ket{ l \; m},   
\end{align}
$$

where $l \geq 0$ is an integer and $m =-l,-l + 1,\; ... \;, l-1, l$ can take up $2l + 1$ values. 

## Matrix Representation

[[Angular Momentum Addition]]

A ket $\ket{ l \; m}$ can be assigned a $2 l + 1$-dimensional vector, and our operators can be assigned a square matrix with the same dimensions.

### Spin

Spin is the intrinsic or internal angular momentum of point particles. There is no classical equivalent. For it we introduce the spin operator $\hat{ \bar{S}}$, which behaves similarly to $\hat{ \bar{L}}$, but acts on $\ket{ s \; m}$ instead:

$$
\begin{align}
 \hat{ \bar{S}}^{2} \ket{ s \; m} & = \hbar^{2}s (s + 1)\ket{ s \; m} \\[1em]
  \hat{ S}_{z}\ket{ s \; m} & = \hbar m \ket{ s \; m}.  
\end{align}
$$

The main difference between  $s$ and $l$ is that $s$  can be half-integer, and can also be $\leq 0$. This is why spin has not classical analog. For $s = 1/2$, we get the Pauli spin matrices $\sigma_{i}$.

## Adding Spins

If we have a system of multiple particles, the eigenstates of the Hamiltonian will often be the eigenstates of the total momentum, so we need a way to accurately add both $\hat{ \bar{S}}$ and $\hat{ \bar{L}}$, and combinations thereof. For 2 particles, we formally have that

$$
\hat{ \bar{S}} = \hat{ \bar{S}}_{1} + \hat{ \bar{S}}_{2},
$$

where each spin operator acts on only one of the particles.

The total state can be understood as a "direct product" of spinors:

$$
\ket{ s_{1}m_{1}\; s_{2}m_{2}} = \ket{ s_{1}\; m_{1}}\ket{ s_{2}\; m_{2}},
$$

where it is understood that there is a tensor product $\otimes$ between the kets. For 2 spin-1/2 particles, we then obtain 4 possible states: three with $s = 1$ corresponding to $m = 0, \pm 1$, and one with $s = 0$ corresponding to $m = 0$.

In order to properly describe the states with $m = 0$, we need to see how they are composed of the different $\uparrow \downarrow$ and $\downarrow \uparrow$ states (linear combination). We can do so by simply applying a ladder operator to the top-most state (in this case $\ket{ 1 \; 1}$) to obtain $\ket{ 1 \; 0}$.

Recall that $\hat{ S}_{-}\ket{ s \; m}= \hbar \sqrt{s (s + 1)-m (m-1)}\ket{ s \; m-1}$. Then, if the total ladder operator is the sum of the individual ladder operators acting on each particle, we have

![[Pasted image 20251018142125.png]]

To get the other state, we enforce the orthogonality of states, from which we get

$$
\ket{ 0 \; 0} = \frac{1}{\sqrt{2}}(\downarrow \uparrow-\uparrow \downarrow). 
$$

In the process of doing this, we also obtain the correct normalization condition. The four total states are now correctly described using linear combinations of the individual states. repeated application of the ladder-down (or up) operator to obtain other states is a process in which we get not only the correct states, but the coefficients that normalize that state. These coefficients are known as the Clebsch-Gordan coefficients.

## Generalizations

This can be done with spins, orbital momenta, or a combination of both. The general formula is then

$$
\ket{ j \; m} = \sum\limits_{m_{1}}C_{m_{1}\;m_{2} \;m}^{l\;\;\; \;s\;\; \;j} \ket{ l \; m_{1}}\ket{ s \; m_{2}}.
$$

In practical applications, one would substitute $\ket{ l \; m_{1}}$ by $\mathcal{Y}_{l}^{m}(\theta, \phi)$ and $\ket{ s \; m_{2}}$ by a spinor. Then

$$
\begin{align}
 \ket{ j \; m} = \begin{bmatrix}
u (\theta, \phi) \\
 v (\theta, \phi)
\end{bmatrix} 
\end{align}
$$

is a linear combination of spherical harmonics.