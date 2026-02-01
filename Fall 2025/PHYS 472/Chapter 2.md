# Identical Particles

In real life, we tend to deal with systems of many particles. We consider the simplest case of a two-particle system. The wavefunction is then a function of the positions of both particles, as well as both of their spins. Ignoring spins, the wavefunction $\Psi (t, \bar{r}_{1}, \bar{r}_{2})$ satisfies the Schrödinger equation with a Hamiltonian given by

$$
H =-\frac{\hbar^{2}}{2 m_{1}}\laplacian_{1} - \frac{\hbar^{2}}{2 m_{2}}\laplacian_{2} + V (\bar{r}_{1}, \bar{r}_{2}, t),
$$

with the normalization condition

$$
\iint\abs{\Psi (t, \bar{r}_{1}, \bar{r}_{2})}\dd{\bar{r}_{1}}\dd{\bar{r}_{2}} = 1.
$$

We consider two cases:
1. Time independent interaction, $\pdv{V}{it}= 0$, in which we have separation of variables and $\Psi (t, \bar{r}_{1}, \bar{r}_{2})= \exp[(-iEt)/\hbar]\psi (\bar{r}_{1}, \bar{r}_{2})$, and
2.  Central force $V (\bar{r}_{1}, \bar{r}_{2})= V (\abs{\bar{r}_{1}-\bar{r}_{2}})= V (r)$. Here we can introduce coordinates $\bar{R}$ and $\bar{r}$, with

$$
\begin{align}
 \bar{r}_{1} & = \bar{R}+ \frac{\mu \bar{r}}{m_{1}} \\[1 em]
\bar{r}_{2} & = \bar{R} - \frac{\mu \bar{r}}{m_{2}} \\[1 em]
\mu & = \frac{m_{1}m_{2}}{m_{1}+ m_{2}},
\end{align}
$$

where $\mu$ is the reduced mass, and now

$$
H =-\frac{\hbar^{2}}{2 (m_{1}+ m_{2})}\laplacian_{\bar{R}} -\frac{\hbar^{2}}{2 \mu}\laplacian_{\bar{r}} + V (r).
$$

We can then separate the variables again. Here, we get two separate equations (with total energy $E = E_{R}+ E_{r}$):

![[Pasted image 20251018160816.png]]

For three or more particles, this separation can only be done when you neglect the interaction between particles. We probably won't have to worry about it

## Distinguishable and Identical Particles

We stick to the case of two non-interacting particles, but now incorporate their spins. The total wavefunction of the system is then

$$
\psi (\bar{r}_{1}, \bar{r}_{2}, s_{1}, s_{2}) = \psi (\bar{r}_{1}, s_{1})\psi (\bar{r}_{2}, s_{2}).
$$

Say particle one is in state $\ket{ n}$ and particle two is in state $\ket{ m}$. If the particles are distinguishable, the wavefunction of the system is just the product between both:

$$
\psi_{n}(\bar{r}_{1}, s_{1})\psi_{m}(\bar{r}_{2}, s_{2}).
$$

If both particles are identical, however, we can not determine which particle is in which state. If we assign one state to one particle, and another to the second particle, the system's total state should not change if we exchange the two particles.

We can introduce an "exchange operator" $\hat{ P}$ that does this exchange. Since the system must not change for identical particles when the operator is applied, we have $\hat{ P}\psi = e^{i \alpha}\psi$; the exchange operator changes the phase of the system. Since $\hat{ P}^{2}= 1$, that means $e^{i \alpha}= \pm 1$.

If the particles are bosons, the sign is positive. If the particles are fermions, the sign is negative. This is just given, the origin comes from relativistic quantum mechanics. Because of the existence of this exchange phase, the simple solution from before is not valid for identical particles. We should then consider the eigenstates of $\hat{ P}$. For $\ket{ n}\neq \ket{ m}$, we have

![[Pasted image 20251018163735.png]]

If $\ket{ n}= \ket{ m}$, we have $\psi_{-}= 0$, which is exactly the manifestation of the *Pauli exclusion principle*. The above ensures that two fermions can not be in the same quantum state.

This (anti)symmetry property of the wavefunctions dramatically affects the spectrum of the eigenstates. As an example, put two spin-1/2 particles inside an infinite square well of width $a$. The Hamiltonian does not depend on spin, which means we can separate the spin dependence. Since there are also no inter-particle interactions, we can separate that dependence as well. We then have

$$
\Psi (x_{1}, \bar{s}_{1}, x_{2}, \bar{s}_{2}) = \psi (x_{1})\chi (\bar{s}_{1})\psi (x_{2})\chi (\bar{s}_{2}).
$$

We then get for $\psi_{1}$ and $\psi_{2}$ the usual solutions to the infinite square well

$$
\begin{align}
 \psi_{n}(x_{1}) & = N \sin\left(\frac{x_{1}\pi n}{a} \right) \\[1 em]
\psi_{m}(x_{2}) & = N \sin\left(\frac{x_{2}\pi m}{a} \right) \\[1 em]
E & = \frac{\hbar^{2}\pi^{2}}{2 ma^{2}}(n^{2}+ m^{2}).
\end{align}
$$

Each $n, m$ has four possible spin configurations, which we have seen before. Let us focus on the ground state $n = m = 1$.

If the particles are distinguishable, like an electron and a positron, there is nothing left for us to do. There are no additional symmetry conditions to fulfill, and we end up with four degenerate spin states.

Now consider two electrons. Since they are identical fermions (spin-1/2), the wavefunction has to be antisymmetric. Since the function part is identical for $\psi_{1} (x_{1})$ and $\psi_{1}(x_{2})$, the function part is symmetric, which tells us the spin part must be antisymmetric. We have already found such a linear combination in [[Chapter 1]], and it corresponds to the spin-0 state:

$$
\ket{ 0\;0} = \frac{1}{\sqrt{2}}(\downarrow \uparrow-\uparrow \downarrow). 
$$

As such, we have a single, none-degenerate ground state with the wavefunction

![[Pasted image 20251018180146.png]]

How can we generalize this construction? For $N$ non-interacting particles, bosons the wavefunction $\psi_{+}$ is the sum of all permutations of the product of all wavefunctions for nonequal indices. For Fermions, $\psi_{-}$ is comprised of all the terms of the so-called Slater determinant, which is the determinant of the matrix of all combinations of wavefunctions. An exchange of columns corresponds to the exchange of two particles, which changes the sign of the determinant.

We can also generalize by considering two interacting particles, but we won't worry about this too much, as it can get very complicated very fast.

## Exchange Interaction

If we compare the expectation value of the square of the separation of two particles, for the three cases of distinguishable particles, and two identical particles of total spin 0 and 1, we have

$$
\begin{align}
 \Delta^{2}_{\text{ dist}} & = \ev{x^{2}}_{n} + \ev{x^{2}}_{m} - 2 \ev{x}_{n}\ev{x}_{m} \\[1 em]
 \Delta^{2}_{\pm} & = \Delta^{2}_{\text{ dist}} \mp 2 \abs{x_{nm}}^{2},
\end{align}
$$

for $\Delta_{+}$ corresponding to the symmetric coordinate function, $\Delta_{-}$ the antisymmetric coordinate function, and $x_{mn} = x_{{nm}}= \mel{n}{\hat{ x}}{m}$.

This expectation value makes it seem as though the symmetric coordinate wavefunction brings the particles closer than the antisymmetric or the distinguishable case, while the antisymmetric case does the opposite. This is known as an exchange interaction, sometimes misnamed the exchange "force". We put force in quotation marks because there are *no forces* that are physically moving the particles closer or farther apart.

This does turn out to be useful as a qualitative explanation of properties of many-particle systems.