Last time, we were left with

$$
\begin{align}
\hat{\vec{L}}^{2}\psi_{\lambda \mu} & = \lambda\psi_{\lambda \mu}\\[1em]
\hat{L}_{z} \psi_{\lambda \mu} & = \mu \psi_{\lambda \mu}.
\end{align}
$$

Applying the ladder operator:

$$
\begin{align}
\hat{L}_{z}(\hat{L}_{+}\psi_{\lambda \mu}) & = \comm{\hat{L}_{z}}{\hat{L}_{+}}\psi_{\lambda \mu}\psi_{\lambda \mu} + \hat{L}_{+}\hat{L}_{z}\psi_{\lambda \mu} \\[1em]
& = \hbar \hat{L}_{+}\psi_{\lambda \mu} + \hat{L}_{+} \mu \psi_{\lambda \mu} \\[1em]
& = (\mu + \hbar)\hat{L}_{+}\psi_{\lambda \mu} \\[1em]
& = \hbar(m + 1) \hat{L}_{+}\psi_{\lambda \mu} \\[1 em]
\therefore \mu & = \hbar m.
\end{align}
$$

What we then have, is that

$$
\begin{align}
\hat{L}_{z}(\hat{L}_{+}\psi_{\lambda \mu}) & = \hbar (m + 1)(\hat{L}_{+}\psi_{\lambda \mu}) \\
\hat{L}_{z}(\hat{L}_{-}\psi_{\lambda \mu}) & = \hbar (m-1)(\hat{L}_{-}\psi_{\lambda \mu}).
\end{align}
$$

Because we only have a finite amount of angular momentum, at some point $\hat{L}_{+}\psi_{\lambda \mu_{\text{max}}}= 0$, with $m_{\text{max}}=l$ and $\mu = \hbar m$. Let us now rewrite $\hat{L}^{2}$ in terms of our ladder operators:

$$
\begin{align}
\hat{L}_{-}\hat{L}_{+} & = (\hat{L}_{x}-i \hat{L}_{y})(\hat{L}_{x}+ i \hat{L}_{y}) \\[1em]
& = \hat{L}_{x}^{2}-i \hat{L}_{y}\hat{L}_{x}+ \hat{L}_{x}i \hat{L}_{y} + \hat{L}_{y}^{2} \\[1 em]
& = \hat{L}_{-}\hat{L}_{+}+ \hat{L}_{z}^{2}+ \hbar \hat{L}_{z},
\end{align}
$$

and so

$$
\begin{align}
\hat{\vec{L}}^{2}\psi_{\lambda \mu_{\text{max}}} & = \hat{L}_{z}^{2}\psi_{\lambda \mu_{\text{max}}} + \hbar \hat{L}_{z}\psi_{\lambda \mu_{\text{max}}}\\[1 em]
& =\mu_{\text{max}}(\mu_{\text{max}}+ \hbar)\psi_{\lambda \mu_{\text{max}}} \\[1 em]
& = \hbar m (\hbar m + \hbar)\psi_{\lambda \mu_{\text{max}}} \\[1 em]
& = \hbar^{2}l (l + 1)\psi_{\lambda \mu_{\text{max}}}.
\end{align}
$$

The same can be done with $\mu_{\text{min}}$. Then, $m_{\text{max}}= + l$ and $m_{min}=-l$. If we look at the difference, $m_{\text{max}}-m_{min}= 2l$, and we find that $l$ can be and integer *or* half-integer!

Recall that, in spherical coordinates,

$$
\begin{align}
\hat{\vec{L}}& = -i \hbar \left(\pdv{\theta}\hat{n}_{\phi}-\frac{1}{\sin \theta}\pdv{\phi}\hat{n}_{\theta} \right), \\[1 em]
\hat{n}_{\phi} & = -\sin \phi\; \hat{n}_{x} + \cos \phi \; \hat{n}_{y} \\
\hat{n}_{\theta} & = \cos \theta \cos \phi \; \hat{n}_{x} + \cos \theta \sin \phi \; \hat{n}_{y}-\sin \theta \; \hat{n}_{z},
\end{align}
$$

then

$$
\begin{align}
\hat{L}_{z} & = -i \hbar \pdv{ \phi} \\[1 em]
\hat{L}_{x} & = -i \hbar \left(-\sin (\phi)\pdv{\theta} -\cos \phi \cot \theta \pdv{\phi} \right) \\[1 em]
\hat{L}_{y} & = -i \hbar \left(\cos \phi \pdv{\theta}-\sin \phi \cot \theta \pdv{\phi} \right) \\[1 em]
\hat{L}_{\pm} & = \pm \hbar e^{\pm i \phi}\left(\pdv{\theta}\pm \cot \theta \pdv{\phi} \right).
\end{align}
$$

Using the operators on $\psi_{\lambda \mu}$, we get

$$
\begin{align}
\hat{L}_{z}\psi_{\lambda \mu} & = -i \hbar \pdv{\phi}\psi_{\lambda \mu} = \mu \psi_{\lambda \mu} \\[1 em]
\pdv[2]{\phi}\psi_{\lambda \mu} & = -m^{2}\psi_{\lambda \mu} \\[1 em]
\hat{\vec{L}}^{2}\psi_{\lambda \mu} & = \left(\frac{1}{\sin \theta}\pdv{\theta}\sin \pdv{\theta} + \frac{1}{\sin^{2}\theta}\pdv[2]{\phi} \right)\psi_{\lambda \mu} = -l (l + 1)\psi_{\lambda \mu} \\[1 em]
\psi_{\lambda \mu} & = Y_{l}^{m}(\theta, \phi).
\end{align}
$$

To recap,  $n$ is known as the principal quantum number, related to the quantization of energy, $l$ is related to the momentum, and determines the "orbital" of our bound particle, and we now know the meaning of $m$, which is related to the quantization of angular momentum.

# Spin

What exactly *is* spin? In classical mechanics, $\vec{L}_{\text{tot}}= \vec{R}\times \vec{p} + \hat{I}\vec{\omega}$, where $\vec{R}$ is the orbital angular momentum, $\hat{I}$ is the mass distribution, and $\vec \omega$ is the angular velocity. The second component can be simplified a little bit, by letting $\hat{I}\vec{\omega}= I_{z}\omega \hat{n}_{z}$. Imagine you have a rotating object and you make it really, really small? Well, the theory breaks, and yet it is what we see in nature. So what can we do about it? This is something that can only be dealt with using matrix mechanics. There is no differential representation.

We introduce the *spin operator* $\hat{\bar{S}}$. We shall find that $\hat{\bar{S}}$ has a discreet spectrum, with $2 l + 1$ eigenstates. Also remember that $-l \leq m \leq l$, and because of that, we can use finite matrices to deal with spin.

## Representation

Just like angular momentum, $\comm{\hat{S}_{x}}{\hat{S}_{y}} = i\hbar \hat{S}_{z}$, and so on. We will use $s$ in place of $l$ to distinguish between the number related to $L$. It is otherwise the same, $-s \leq m \leq s$. Next

$$
\begin{align}
\hat{\bar{S}}^{2}\ket{sm} & = \hbar^{2}s (s + 1)\ket{sm} \\[1 em]
\hat{S}_{z} \ket{sm} & = \hbar m \ket{sm}.
\end{align}
$$

Again, just like $l$, we have $m_{\text{max}}-m_{\text{min}}= 2s$, and so $s$ is either an integer or a half-integer. If $s$ is an integer, the particle is called a *boson*, and if $s$ is half-integer, the particle is called a fermion.

$$
\begin{align}
\ket{s} & = \sum\limits_{m =-s}^{s}c_{m}(t)\ket{sm}
\end{align}
$$