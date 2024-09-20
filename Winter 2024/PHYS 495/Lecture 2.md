# The Hydrogen Atom

The hydrogen atom is the simplest object aside from an electron that we can work with. It is composed of a single positive nucleus and a single electron. Despite its simplicity, it makes for a great building block for other, more complex structures.

We seek to answer the question: in the presence of the proton, with what is the quantum state of the electron in the Coulomb potential?

Recall the time independent Schrödinger equation:

$$
\begin{align}
\left[\frac{-\hbar^{2}}{2 m}\nabla^{2}+ V (r) \right]\psi_{r} & = E \psi (r).
\end{align}
$$

Since this problem has radial symmetry, it would be convenient to work in spherical coordinates. In that case, the Laplacian is

$$
\nabla^{2} = \frac{1}{r^{2}}\pdv{r}\left(r^{2}\pdv{r} \right) + \frac{1}{r^{2}\sin \theta}\pdv{\theta}\left(\sin \theta \pdv{\theta} \right)-\frac{1}{r^{2}\sin^{2}\theta}\pdv[2]{\phi}
$$

The time independent Schrödinger equation is then

$$
\begin{align}
\frac{-\hbar^{2}}{2 m}\left[\frac{1}{r^{2}}\pdv{r}\left(r^{2}\pdv{r} \right) -\frac{1}{r^{2}}\hat{l}^{2} \right]\psi (r)  = [E-V (r)]\psi (r) \\[1 em]
\hat{l}^{2} = \frac{1}{\sin^{2}}\pdv{\theta}\left(\sin \theta \pdv{\theta} \right) - \frac{1}{\sin^{2}\theta}\pdv[2]{\phi}.
\end{align}
$$

From here, we get

$$
\begin{align}
\frac{-\hbar^{2}}{2 m}\left[\frac{1}{r^{2}}\pdv{r} \left(r^{2}\pdv{r} \right) +[V (r)-E] \right]\psi (r) & = \frac{-\hbar^{2}}{2 mr^{2}}\hat{l}^{2}\psi (r) \\[1 em]
\left[\pdv{r}\left(r^{2}\pdv{r} \right) + \frac{2 mr^{2}}{\hbar^{2}}[E-V (r)] \right] & = \hat{l}^{2}\psi (r).
\end{align}
$$

This suggests a separable solution of the form $\phi (r, \theta, \phi) =R (r) Y (\theta, \phi)$. Separating $R$, we obtain

$$
\begin{align}
\left[\pdv{r}\left(r^{2}\pdv{r} \right) + \frac{2mr^{2}}{\hbar^{2}}[E-V (r)] \right ]R(r) & = A\cdot R (r) \\[1 em]
 \hat{l}^{2} Y (\theta, \phi) & = A \cdot Y (\theta, \phi).
\end{align}
$$

We can further separate $Y (\theta, \phi)$ into $Y = \Theta (\theta)\Phi (\phi)$:

$$
\begin{align}
\frac{1}{\Theta (\theta)}\sin \theta \pdv{\theta} \left(\sin \theta \pdv{\theta} \right)\Theta (\theta)+ A^{2}\sin \theta & = \frac{1}{\Phi (\phi)}\pdv[2]{\Phi}{\phi} = m^{2} \\[1 em]
\pdv[2]{\Phi}{\phi} & = \Phi (\phi)m^{2} \\[1 em]
\Phi (\phi) & = e^{i m\phi}.
\end{align}
$$

The azimuthal dependence is only a phase factor. The polar dependence is much more complicated, and for that we turn to ladder operators. We start with the Cartesian representation of $\hat{l}^{2}$ is

$$
\begin{align}
\hat{l}_{x} & = i \left[\sin \phi \pdv{\theta} + \cot \theta \cos \phi \pdv{\phi} \right] \\[1 em]
\hat{l}_{y} & = i \left[-\cos \phi \pdv{\theta} + \cot \theta \sin \phi \pdv{\phi} \right] \\[1 em]
\hat{l}_{z} & = -i \pdv{\phi}.
\end{align}
$$

We can then define our considers classic raising and lowering operators as

$$
\begin{align}
\hat{l}_{\pm} & = \hat{l}_{x} \pm i\hat{l}_{y} = e^{\pm i \phi}\left[\pdv{\theta} \pm i \cot \theta \pdv{\phi} \right].
\end{align}
$$

We can now see what our $\hat{l}_{i}$s do to our wavefunction, starting with $\hat{l}_{z}$:

$$
\hat{l}_{z}Y (\theta, \phi) = mY (\theta, \phi),
$$

therefore $m$ is the eigenvalue of the z-component of the angular momentum. That is,

$$
\mel{Y}{\hat{l}_{z}}{Y} = \mel{Y}{m}{Y} = m.
$$

Now we have to see what our operators do to $\hat{l}_{z}Y$. For that, we use the commutation relations

$$
\begin{align}
\comm{\hat{l}_{z}}{\hat{l}_{\pm}} & = \pm \hat{l}_{\pm} = \hat{l}_{z}\hat{l}_{\pm} - \hat{l}_{\pm}\hat{l}_{z} \\[1 em]
\hat{l}_{z}\hat{l}_{\pm} & = \pm \hat{l}_{\pm} \pm \hat{l}_{\pm}\hat{l}_{z}.
\end{align}
$$

Then

$$
\begin{align}
\hat{l}_{z}\hat{l}_{\pm}Y & = (\pm \hat{l}_{\pm}\pm \hat{l}_{\pm}\hat{l}_{z})Y \\[1 em]
& = (\pm \hat{l}_{\pm}\pm \hat{l}_{\pm}m)Y \\[1 em]
\hat{l}_{z}\hat{l}_{\pm}Y & = (m \pm 1)\hat{l}_{\pm}Y \\[1 em]
\hat{l}_{z}\comm{\hat{l}_{\pm}}{Y} & = (m \pm 1)\comm{\hat{l}_{\pm}}{Y}.
\end{align}
$$

This tells us that the state $\comm{\hat{l}_{\pm}}{Y}$ has angular momentum along the z-direction of $m \pm 1\longrightarrow$ one more or one less an unit than $Y (\theta, \phi)$ itself, which justifies the names of "raising" and "lowering" operators.

Another property of these operators is that they commute with $\hat{l}^{2}$, which is the actual term in our Hamiltonian. That is,

$$
\begin{align}
\comm{\hat{l^{2}}}{\hat{l}_{z}} & = 0 \\[1 em]
\comm{\hat{l}^{2}}{\hat{l}_{\pm}} & = 0
\end{align}
$$

which dictates that the $Y$ states are simultaneous eigenfunctions of $\hat{l}^{2}, \; \hat{l}_{\pm}$, and $\hat{l}_{z}$.

We shall continue to type this out when the notes are out.