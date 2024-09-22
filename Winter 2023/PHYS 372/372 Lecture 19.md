# Continuous Spectra

Last week, we dealt with "good" Hermitian operators. The energy spectrum with eigenstates related by $q_{{n}}\qc \in \mathbb{N}$. These are normalizable, that is, $\ip{\psi_{{n}}^{Q}}= 1$. This is for energy, what about $\hat{x}$ or $\hat{p}$?

## Momentum Operator

$$\hat{p}=-i \hbar \pdv{x}$$

We shall treat this as an eigenvalue-eigenfunction problem, that is

$$
\hat{p}\psi_{p}(x) = p \psi_{p}(x),
$$

where $p$ is just a number solving the equation gives

$$
\psi_{p}(x) = A \exp \left(\frac{ipx}{\hbar} \right).
$$

Because this is not square integrable, this solution does not belong in Hilbert space. What we'll do is start by rewriting $\psi_{p}\rightarrow \ket{p}$. Then, the problem becomes

$$
\hat{p}\ket{p} = p \ket{p}.
$$

How to deal with this? Let's do a formal analysis.
- Orthogonality: $\ip{p'}{p}$
	$$
\ip{p'}{p} \equiv \int_{-\infty}^{\infty} \psi^{*}_{p}\psi_{p}\dd{x} = \abs{A}^{2}\int_{-\infty}^{\infty}\exp \left(\frac{i (p-p')}{\hbar}x \right)\dd{x}	
$$

Notice that if $p \neq p'$, the integral goes to zero, while if $p' = p$ the integral diverges.

- Fourier analysis:
	$$
\begin{align}
\psi (x) & = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\phi (k')e^{ikx}\dd{k'} \\[1em]
\phi (k) & = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\psi_{x}e^{-ikx}\dd{x} \\[1em]
& = \int_{-\infty}^{\infty}\left(\int_{-\infty}^{\infty}\frac{1}{2 \pi}\exp (i (k'-k)x)\dd{x} \right)\phi (k')\dd{k'} \\[1em]
& = \int_{-\infty}^{\infty}\delta (k-k')\dd{k} \\[1em]
& = \int_{-\infty}^{\infty}\frac{ \delta (k-k')}{\hbar}\dd{p}= 1.
\end{align}
$$

If $A = \frac{1}{\sqrt{2 \pi \hbar}}$ then $\ip{p'}{p}= \delta (p-p')$. This makes sense as $\ip{\psi_{n}}{\psi_{m}}= \delta_{nm}$, so we've seen nothing new.

We can now do an expansion of $\Psi (x, t)$ in the basis of $\psi_{p}(x)$, now rewritten with $\ket{\psi_{t}}$ and $\ket{p}$.

$$
\begin{align}
\ip{p}{\psi_{t}} & = \int_{-\infty}^{\infty}\psi_{p}^{*}\Psi (x, t)\dd{x} \\[1em]
& = \frac{1}{\hbar^{2}\sqrt{2 \pi}}\int_{-\infty}^{\infty}\exp \left(\frac{-ipx}{\hbar} \right)\Psi (x, t)\dd{x} \\[1em]
& = \frac{1}{\hbar^{ 1/2}}\phi \left(\frac{p}{\hbar}, t \right).
\end{align}
$$

This is a Fourier transform of $\phi (k, t)$ for $\Psi (x, t)$. We call this $\widetilde{\Psi}(p, t)$.

What we have now is that $\widetilde{\Psi}(p, t)\leftrightarrow C_{n}^{Q}$, where $p$ is a "continuum index". We can now transform between $\Psi (x, t)$ and $\widetilde{\Psi}(p, t)$ by

$$
\Psi (x, t) = \int_{-\infty}^{\infty}e^{ikx}\phi (k, t)\dd{k} = \int_{-\infty}^{\infty}\psi_{p}(x)\cdot \widetilde{\Psi}(p, t)\dd{p}.
$$

In Dirac notation,

$$
\ket{\psi_{t}} = \int_{-\infty}^{\infty}\ip{p}{\psi_{t}}\ket{p}\dd{p} \leftrightarrow \ket{\psi_{t}} = \sum\limits_{n}\ip{\psi_{n}^{Q}}{\psi_{t}}\ket{\psi_{t}}.
$$ 

### Momentum Representation of Operators

For discreet cases, we could write this down as a matrix,

$$
T_{mn}=  \mel{\psi_{m}}{\hat{T}}{\psi_{n}} = \int_{-\infty}^{\infty}\psi_{m}^{*} (x)\hat{T}(\hat{x}, \hat{p})\psi_{n} (x)\dd{x}.
$$

For the continuous case, we then have

$$
\begin{align}
\ev{T} & = \ev{\hat{T}}{\psi_{t}} \\[1em]
& = \bar{c}^{\dagger Q} \hat{T}\bar{c}^{Q} \\[1em]
& = \sum\limits_{n, m}c_{n}^{*Q}(t)T_{mn}c_{m}^{Q}(t) \\[1em]
& = \sum\limits_{n,m}\ip{\psi_{t}}{\psi_{m}^{Q}}\mel{\psi_{m}^{Q}}{\hat{T}}{\psi_{n}^{Q}}\ip{\psi_{n}^{Q}}{\psi_{t}}.
\end{align}
$$

To make this continuous, simply change the sums into integrals:

$$
\begin{align}
\ev{T} & = \int_{-\infty}^{\infty} \int_{-\infty}^{\infty}\underbrace{\ip{\psi_{t}}{p'}}_{\widetilde{\Psi}^{*}(p', t)} \mel{p'}{\hat{T}}{p} \underbrace{\ip{p}{\psi_{t}}}_{\widetilde{\Psi}(p, t)}\dd{p'} \dd{p}.
\end{align}
$$

Here,

$$
\begin{align}
\mel{p'}{\hat{T}}{p} & \equiv T_{p' p} = \int_{-\infty}^{\infty}\psi_{p'}^{*}(x)\hat{T}(\hat{x}, \hat{p})\psi_{p}(x) \dd{x} \\[1em]
T_{p' p} & = \frac{1}{2 \pi \hbar}\int_{-\infty}^{\infty}e^{\frac{i (p-p')x}{\hbar}}T (x, p)\dd{x},
\end{align}
$$

where $\hat{x}\psi_{p}(x) = x \psi_{p}(x)$, $\hat{p}\psi_{p}(x)= p \psi_{p}(x)$, and so $\hat{T}(\hat{x}, \hat{p})\psi_{p}(x)= T (x, p)\psi_{p}(x)$. The first integral above is known as the *kernel* of $T$.

From all this, we have

$$
\ev{Q} = \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}\widetilde{\Psi}^{*}(p', t)Q_{p' p}\widetilde{\Psi}(p, t)\dd{p'}\dd{p},
$$

where $\widetilde{\Psi}(p, t)$ is the Fourier transform of $\Psi (x, t)$, and

$$
Q_{p' p} = \frac{1}{2 \pi \hbar}\int_{-\infty}^{\infty}e^{\frac{-i (p-p')}{\hbar}x}Q (x, p)\dd{x}.
$$

If we consider the operator $\hat{x}$, we can repeat the same process. With $\hat{x}\ket{x}= x \ket{x}$ and $\psi_{x'}(x) = \delta{(x-x')}$, we then have

$$
\ip{x'}{\psi_{x'}} = \int_{-\infty}^{\infty}\underbrace{\psi_{x'}^{*}}_{\delta(x-x')}\Psi (x, t)\dd{x} = \Psi (x, t).
$$