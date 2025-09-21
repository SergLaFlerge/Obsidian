From last class,

$$
\ip{p'}{p} = \int_{-\infty}^{\infty}\psi_{p'}^{*}(x)\cdot \psi_{p}(x) \dd{x} = \abs{A}^{2}\int_{-\infty}^{\infty}\exp \left(\frac{i (p-p')}{\hbar}x \right)\dd{x}.
$$

Let us do a summary of the last few classes:

1. We now use vectors $\ket{\psi_{t}}$ that live in Hilbert space. Our physical observables are now Hermitian operators $\hat{Q}$. As such, we have $$i \hbar \pdv{t}\ket{\psi_{t}}= \hat{H}\ket{\psi_{t}}.$$
2.  $\ket{\psi_{t}}$ can be represented in terms of eigenvectors of $\hat{Q}$. We use 3 common basis: $\hat{x}$, which leaves us with the usual Schrödinger equation, $\hat{p}$, which gives a slightly different formulation, and a more general operator $\hat{Q}$. $\hat{p}$ gives continuous spectra, while $\hat{Q}$ gives discreet spectra.
3.  Hilbert space class some interest properties:
	1. A measurement implies collapse of $\ket{\psi_{2}}$.
	2. If $\sigma_{Q_{1}}= \sigma_{Q_{2}} = 0$, then $\comm{Q_{1}}{Q_{2}}= 0$.
	3. $Q_{1}, Q_{2}$ are incompatible if $\comm{Q_{1}}{Q_{2}}\neq 0$, and so $$\sigma_{Q_{1}}\sigma_{Q_{2}}\geq \left(\frac{1}{2 i}\ev{\comm{\hat{Q}_{1}}{\hat{Q}_{2}}} \right)$$

# 3-D Quantum Mechanics

In classical mechanics

$$
\begin{align}
\vec{r} & = (x, y, z) \\
\vec{p} & = (p_{x}, p_{y}, p_{z}) \\
H & = \frac{p^{2}}{2 m}+ V (\vec{r}).
\end{align}
$$

In quantum mechanics, however, we have

$$
\begin{align}
\vec{p} & \rightarrow \hat{\vec{p}} \\
p_{x} & \rightarrow \hat{p}_{x} & = -i \hbar \pdv{x} \\
p_{y} & \rightarrow \hat{p}_{y} & = -i \hbar \pdv{y} \\
p_{z} & \rightarrow \hat{p}_{z} & = -i \hbar \pdv{z},
\end{align}
$$

so $\vec{p}=-i \hbar \vec{\nabla}$. Therefore $\hat{\vec{p}}^{2}=-\hbar^{2} (\vec{\nabla})^{2}=-\hbar^{2} \Delta$.

In spatial coordinates, the Schrödinger equation becomes

$$
i \hbar \pdv{t}\Psi (\vec{r}, t) = \hat{H}(\hat{\vec{p}}, \hat{\vec{r}})\Psi (\vec{r}, t),
$$

with

$$
\hat{H} = \frac{-\hbar^{2}}{2 m}\nabla^{2}+ V (\vec{r}).
$$

We are also only considering time independent potentials in this case. The one good case for this is when we have a spherically symmetric potential, i.e. $V (\vec{r})= V (r)$ with $r = \abs{\vec{r}}$. This is analogous to the central force problem from classical mechanics. The first step will be to exploit the symmetry of the problem by working in spherical coordinates. That is

$$
\begin{align}
x & = r \sin (\theta) \cos (\phi) \\
y & = r \sin (\theta) \sin (\phi) \\
z & = r \cos (\theta),
\end{align}
$$

with $0 \leq \phi \leq 2 \pi$ being the azimuthal angle, and $0 < \theta < \pi$ being the polar angle. The Laplacian is written as

$$
\nabla^{2} = \frac{1}{r^{2}}\pdv{r}\left(r^{2}\pdv{r} \right) + \frac{1}{r^{2}} \frac{1}{\sin \theta}\pdv{\theta}\left(\sin \theta \pdv{\theta}\right) + \frac{1}{(r \sin \theta)^{2}}\pdv[2]{\phi}.
$$

The general solution is given by

$$\Psi (\vec{r}, t)= \exp \left(\frac{-iEt}{\hbar} \right)\psi (r, \theta, \phi).$$

The 3-D time independent Schrödinger equation is then

$$
\left(\frac{-\hbar}{2 m}\nabla^{2}+ V (r) \right)\psi (r, \theta, \phi) = E \psi (r, \theta, \phi).
$$

Solving the equation by separation of variables, we obtain

$$
\begin{align}
\left[\frac{1}{R} \pdv{r}\left(r^{2}\dv{R}{r} \right)-\frac{2 mr^{2}}{\hbar{2}}(V (r)-E) \right] & = C \\[1em]
\frac{1}{Y}\left[\frac{1}{\sin \theta}\pdv{\theta}\left(\sin \theta \pdv{Y}{\theta} \right)+ \frac{1}{\sin^{2}\theta} \pdv[2]{Y}{\phi}  \right] & = -C.
\end{align}
$$

For convenience, we will let $C = l (l + 1)$. Now, for the angular equation, we repeat the process and obtain

$$
\begin{align}
\frac{1}{\Theta}\left[\sin \theta \dv{\theta}\left(\dv{\Theta}{\theta} \right)\right] + l (l + 1)\cdot \sin \theta  & = D \\
\frac{1}{\Phi} \dv[2]{\Phi}{\phi} = -D,
\end{align}
$$

and like before, we will call $D = m^{2}$ (not to be confused with mass!). Solving the equations:

$$
\begin{align}
\Phi & = A_{\phi}e^{im \phi} \\
\Phi (0) & = \Phi (2 \pi)
\end{align}
$$

with $0 < \phi < 2 \pi$. This places a restriction on $m$: it must be in $\mathbb{Z}$.

The polar equation is a little more complicated. We do a variable substitution $\theta \rightarrow \cos \theta$, with allows us to do a power series solution. Solution like these are finite on $0 < \theta < \pi$ only for $l \in \mathbb{Z}$ *and* $\abs{m}\leq l$. Otherwise we end up having singularities at $\theta = 0$.

We end up with a set of "good" solution, called the *Legendre functions*:

$$
\Theta (\theta) = A_{\theta}P_{l}^{m}(\cos \theta),
$$

with

$$
P_{l}^{m} (x) = (1-x^{2})^{\abs{m}/2}\dv[m]xP_{l}(x),
$$

and

$$
P_{l}(x) = \frac{1}{2^{l}l!}\dv[l]{x}(x^{2}-1)^{l}.
$$

$P_{l}(x)$ are known as the Legendre polynomials.

For the normalization condition

$$
\int_{-\infty}^{\infty}\abs{\psi (r, \theta, \phi)}^{2}\dd{V} = 1,
$$

with $\dd{V}= r^{2}\sin \theta \dd{r}\dd{\theta}\dd{\phi}$. Because our equation is separable, we can separate the integrals and do each individually.

$$
\begin{align}
\int_{-\infty}^{\infty}\abs{R (r)}^{2}r^{2}\dd{r} & = 1 \\[1em]
\int_{0}^{\pi}\abs{\Theta (\theta)}^{2}\sin \theta \dd{\theta} & = 1 \\[1em]
\int_{0}^{2 \pi}\abs{\Phi (\phi)}^{2}\dd{\phi} & = 1 \\[2em]
A_{\phi} & = \frac{1}{\sqrt{2 \pi}} \\[1em]
A_{\theta} & = \left[\frac{2l + 1}{2}\frac{(l-\abs{m})!}{(l + \abs{m})!} \right]^{1/2}.
\end{align}
$$

Finding $A_{r}$ is complicated.