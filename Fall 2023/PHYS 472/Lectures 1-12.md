#  372 Review

The Schrödinger equation:

$$
\begin{align}
i \hbar \pdv{t}\Psi (x, t) & = \frac{-\hbar^{2}}{2 m}\dv[2]{x}\Psi (x, t) + V (x)\Psi (x, t).
\end{align}
$$

We only looked at local, time independent potentials, for which $V (x, t)= V (x)$. Then the solutions to the Schrödinger equation are

$$
\begin{align}
\Psi (x, t) & = \sum\limits_{n}C_{n}(x)\phi_{n}(x),
\end{align}
$$

Which, after working out the properties of the wavefunction, we obtain

$$
\begin{align}
\Psi (x, t) & = \sum\limits_{n}C_{n}(0)\exp \left(\frac{-iE_{n}t}{\hbar} \right)\phi_{n}(x).
\end{align}
$$

The physics problem is then finding the $\phi_{n}(x)$'s.

For the time independent Schrödinger equation, we have

$$
\begin{align}
\hat{H}\phi (x) & = E \phi (x) \\[1 em]
\phi (x) & = \sum\limits_{m}C_{m}\rho_{m}(x).
\end{align}
$$

^d48096

If we substitute [[Lectures 1-12#^d48096|1-1]] into [[Lectures 1-12#^d48096|1-2]], and integrate both sides with $\rho^{*}$, then

$$
\begin{align}
\sum\limits_{m}H_{nm}C_{m} & = EC_{m} \\[1 em]
H_{nm} & \equiv \int \rho^{*}_{n}(x)\hat{H}\rho_{m}(x)\dd{x}.
\end{align}
$$

$V (x)$ can then be any time independent potential.

# Convenient Basis Sets

Many problems can be more easily explored if we use an orthonormal basis that we are familiar with. The best example of this is the infinite square potential well, for which

$$
\begin{align}
\rho_{m}(x) & = \sqrt{\frac{2}{a}}\sin\left(\frac{m \pi x}{a} \right)\qc m \in \mathbb{N}.
\end{align}
$$

This is incredibly useful, as calculating $V_{nm}$ becomes doable since

$$
\begin{align}
V_{nm} & = \int \frac{2}{a}\sin\left(\frac{n \pi x}{a} \right)\cdot V (x) \cdot \sin \left(\frac{m \pi x}{a} \right)\dd{x}.
\end{align}
$$

This gives us the elements of our matrix equation, from which one can find the eigenvectors and eigenvalues. This is known as the method of eigenfunction expansion, and it is a pretty powerful tool for numerically computing wavefunctions to an arbitrary degree of accuracy.

# Many Body Problem

We looked mostly at $N = 2$, but this analysis is valid for any $N$. For 2 particles, $\hat{H}$ becomes

$$
\begin{align}
\hat{H} \psi (\vec{r}_{1}, \vec{r}_{2}) & = E\psi (\vec{r}_{1}, \vec{r}_{2}) \\[1 em]
\hat{H} & = \frac{-\hbar^{2}}{2 m_{1}}\nabla_{1}^{2}-\frac{\hbar^{2}}{2 m_{2}}\nabla_{2}^{2}+ V (\vec{r}_{1}, \vec{r}_{2}).
\end{align}
$$

For non-interacting particles, we can separate the potential term, and therefore separate $\hat{H}$:

$$
\begin{align}
V (x) & = V_{A}(x) + V_{B}(x) \\[1 em]
\hat{H} & = \hat{H}_{1}+ \hat{H}_{2} \\[1 em]
E & = E_{A} + E_{B} \\[1 em]
\hat{H}_{A}\psi_{A} & = E_{A}\psi_{A} \\
\hat{H}_{B}\psi_{B} & = E_{B}\psi_{B},
\end{align}
$$

which again reduces the problem into two, one particle problems.

## Identical Particles

If we had two identical particles collide inside a detector, and the detector saw one of the particles, we would have no idea which one hit the detector, so the two possible events must be treated as if they were the same. Let us introduces a switching operator $\hat{P}$ with the property that

$$
\begin{align}
\hat{P}_{1 2}[\phi_{A}(\vec{r}_{1})\phi_{B}(\vec{r}_{2})] & =  \phi_{B}(\vec{r}_{1})\phi_{A}(\vec{r}_{2}),
\end{align}
$$

and two new wavefunctions,

$$
\begin{align}
\psi_{S} & = \frac{1}{\sqrt{2}}\left[\phi_{A}(\vec{r}_{1})\phi_{B}(\vec{r}_{2})+ \phi_{B}(\vec{r}_{1})\phi_{A}(\vec{r}_{2}) \right], \\[1 em]
\psi_{A} & = \frac{1}{\sqrt{2}}\left[\phi_{A}(\vec{r}_{1})\phi_{B}(\vec{r}_{2})- \phi_{B}(\vec{r}_{1})\phi_{A}(\vec{r}_{2})\right].
\end{align}
$$

If we apply $\hat{P}$  to $\psi_{S}$  and $\psi_{A}$, we see that

$$
\begin{align}
\hat{P}(\psi_{S}) & = \psi_{S}, \\[1 em]
\hat{P}(\psi_{A}) & = -\psi_{A}
\end{align}
$$

These two wavefunctions describe bosons with integer spins and fermions with half-integer spins respectively. If I $A = B$ then

$$
\begin{align}
\psi_{S} & = \phi_{a}\phi_{b} \\[1 em]
\psi_{a} & = 0.
\end{align}
$$

As an example, in the infinite square well, we have three cases:

1. Distinguishable, which implies $\psi (x_{1}, x_{2})= \phi_{A}(x_{1})\phi_{B}(x_{2})$ and $E = E_{1}(A^{2}+ B^{2})$.
2. Symmetric, where we have $\psi_{S}$ as above.
3. Antisymmetric, where with have $\psi_{A}$ as above.

## Exchange Forces

Even when two particles don't interact, they may appear to attract or repel one another, depending on their statistics. We again have to distinguish from the three cases mentioned above. First a general result:

$$
\ev{(x_{1}-x_{2})^{2}} = \ev{x_{1}^{2}}+ \ev{x_{2}^{2}}-2 \ev{x_{1}\cdot x_{2}}.
$$

For the distinguishable case, we have

$$
\begin{align}
\psi (x_{_{1}}, x_{2}) & = \phi_{n1}(x_{1})\phi_{n 2}(x_{2}) \; \text{or}\; \phi_{n 2}(x_{1})\phi_{n1}(x_{2}) \\[1 em]
\ev{(x_{1}-x_{2})^{2}}_{D} & = \ev{x^{2}}_{n_{1}n_{1}}+ \ev{x^{2}}_{n_{2}n_{2}}-2 \ev{x}_{n_{1}n_{1}}\ev{x}_{n_{2}n_{2}}.
\end{align}
$$

Then, for fermions and bosons, we have $\psi_{a}$ and $\psi_{s}$ respectively:

$$
\begin{align}
\psi^{a}_{s} & = \frac{1}{\sqrt{2}}\left[\phi_{n_{1}}(x_{1})\phi_{n_{2}}(x_{2})\mp \phi_{n_{2}}(x_{1})\phi_{n_{1}}(x_{2}) \right] \\[1 em]
\ev{(x_{1}-x_{2})^{2}}^{F}_{B} & = \ev{(x_{1}-x_{2})^{2}}_{D}\pm 2\abs{\ev{x}_{n_{1}n_{2}}}^{2}
\end{align}
$$

## Spin

We attribute to each particle wavefunction a spin $\chi_{n}$, so that

$$
\phi_{r_{1}}\rightarrow \phi (r_{1})\chi_{1}.
$$

This holds true as long as there is no spin-orbit coupling, which we have assumed thus far. For 2-particle wavefunctions, we require 2 spins, one for each particle. In particular, for bosons and fermions, we have

$$
\begin{align}
\chi_{a}\chi_{b} & = \frac{1}{\sqrt{2}}(\ket{\uparrow \downarrow}-\ket{\downarrow \uparrow}) \\[1 em]
\chi_{a}\chi_{b} & = 
\begin{cases}
\ket{\uparrow \uparrow} \\
\frac{1}{\sqrt{2}}(\ket{\uparrow \downarrow}+ \ket{\downarrow\uparrow}) \\
\ket{\downarrow \downarrow}
\end{cases}
\end{align}
$$

respectively. Notice that the symmetric bosons are coupled to the antisymmetric spin singlet and they also cover the $a = b$ case ($\phi_{a}(r_{1})\phi_{a}(r_{2})$), while the antisymmetric fermions are coupled to the symmetric spin triplet.

# Multi-electron Atoms

The Hamiltonian becomes

$$
\hat{H} = \sum\limits_{j = 1}^{z}\left(\frac{-\hbar^{2}}{2 m_{e}}\nabla^{2}_{j}+ \frac{(ze) (-e)}{4 \pi \epsilon_{0}}\cdot \frac{1}{\abs{\vec{r}_{j}}}+ \sum\limits_{k > j}\frac{e^{2}}{4 \pi \epsilon_{0}}\cdot \frac{1}{\abs{\vec{r
}_{k}-\vec{r}_{j}}} \right).
$$

This equation fails to take into account two properties:
1. No spin-orbit coupling, no relativistic effects.
2. The mass of the nucleus is much, much greater than $m_{e}$ (Born-Oppenheimer approximation)

We also ignore the second sum, which represents electron-electron interactions. For $z = 2$, we have helium, of which we have two kinds: orthohelium and parahelium. Orthohelium is represented using the antisymmetric wavefunction and spin triplet, and parahelium is represent using the symmetric wavefunction and spin singlet.

# Solids

They come in two flavors: strong and weak coupling. For strong coupling an atom on the left with wavefunction $\psi_{L}$ coupled to an atom on the right with wavefunction $\psi_{R}$ has a matrix equation

$$
\begin{bmatrix}
E_{0} & -t \\
t & E_{0}
\end{bmatrix}
\begin{bmatrix}
\psi_{L} \\
\psi_{R}
\end{bmatrix}
=
E
\begin{bmatrix}
\psi_{L} \\
\psi_{R}
\end{bmatrix}
$$

that can be diagonalized:

$$
\begin{align}
(E_{0}-E)^{2}-t^{2} & = 0 \\
E_{0}\pm t & = E,
\end{align}
$$

so by bringing two atoms together, one can lower the ground state of the whole system. In this case $t$ simply represents a parameter that appears when we bring the two atoms together.

For weak coupling, imagine dumping $10^{23}$ electrons in an infinite cubic well of dimensions $L \times L \times L$. In that case we would have

$$
\begin{align}
\psi (x, y, z) & = \prod_{j = x, y, z}\sqrt{\frac{2}{L_{j}}}\sin\left(\frac{n_{j} \pi j}{L_{j}} \right) \\[1 em]
E & = \frac{\pi^{2}\hbar^{2}}{2 m_{e}}\left(\frac{n_{x}^{2}}{L_{x}^{2}}+ \frac{n_{y}^{2}}{L_{y}^{2}}+ \frac{n_{z}^{2}}{L_{z}^{2}} \right) \\[1 em]
& = \frac{\pi^{2}\hbar^{2}}{2 m_{e}}(k_{x}^{2}+ k_{y}^{2}+ k_{z}^{2}) \\[1em]
& = \frac{\pi^{2}\hbar^{2}k^{2}}{2 m_{e}}.
\end{align}
$$

To go from this fictitious $k$ to something real, we introduce the electron density $\rho = Nq/V$. Then

$$
k = (3 \pi^{2}\rho)^{1/3}
$$

## Kronig-Penney Model

For solid lattices we may model their structure as a series of finite square wells of some width, where the wells represent the nuclei of the atoms. We will assume that the wells all have the same width, as well as the barriers. We can then invoke Bloch's theorem, which states that in the case where $V (x + L)= V (x)$, we have

$$
\begin{align}
\abs{\psi (x + L)}^{2} & = \abs{\psi (x)}^{2} \\[1 em]
\psi (x + L) & = e^{ikL}\psi (x).
\end{align}
$$

If we then treat $k$ as a quantum number, we have

$$
\psi_{k}(x + L) = e^{ikL}\psi_{k}(x).
$$

The important result is that, for a model with well width $w$, barrier width $b$, and total length $l$, we get

$$
\begin{align}
\cos (kl) & = \cos (k_{0}w)\cosh(Q_{1}b)+ \frac{Q_{1}^{2}-k_{0}^{2}}{2 k_{0}Q_{1}}\sin (k_{0}w)\sinh (Q_{1}b) \\[1 em]
k_{0} & = \sqrt{\frac{2 m_{0}(E-V_{0})}{\hbar^{2}}} \\[1 em]
Q_{1} & = \sqrt{\frac{2 m_{0}(V_{1}-E)}{\hbar^{2}}} \\[1em]
V_{0} & < E < V_{1}
\end{align}
$$

We may replace the hyperbolic functions with trig functions if we define

$$
q_{1}\equiv \sqrt{\frac{2 m_{0}(E-V_{1})}{\hbar^{2}}}.
$$

We would then obtain

$$
\cos (kl) = \cos (k_{0}w)\cos(q_{1}b)+ \frac{q_{1}^{2}-k_{0}^{2}}{2 k_{0}q_{1}}\sin (k_{0}w)\sin(q_{1}b).
$$

In the Dirac comb limit, we have $V_{1}\rightarrow \infty$ and $b \rightarrow 0$, so then our solution is

$$
\begin{align}
\cos (kl) & = \cos (z)+ \frac{\beta}{z}\sin (z)\\[1 em]
z  & \equiv k_{0}l \qc \beta \equiv \frac{m_{0}\alpha l}{\hbar^{2}}
\end{align}
$$

Since $z \approx \sqrt{E}$, we see that $E$ increases as $z$ does. Since the solutions must lie between $-1$ and $1$, there will be regions with solutions and regions without.

In the weak coupling limit, where $V_{1}\rightarrow V_{0}$, we have

$$
E = V_{0}+ \frac{\hbar^{2}}{2 m_{0}}\left(k + \frac{2 \pi n}{l} \right)^{2}.
$$

In the strong coupling limit, we instead have

$$
\begin{align}
\cos (k_{0}w) + \frac{Q_{1}^{2}-k_{0}^{2}}{2 k_{0}Q_{1}}\sin (k_{0}w) & = \eta_{1}-\eta_{2}
\end{align}
$$

$\eta_{1} = 2 e^{-Q_{1}b}\cos (kl)$, which is really small, but $\eta_{2}$ is even smaller. This then resembles the result of a finite square well, from which we can then obtain

$$
E = E_{0} -2 t \cos (kl).
$$

The left hand side of the above question can be factored into its odd and even states:

$$
LHS = \left[\cos \left(\frac{k_{0}w}{2}\right) -\frac{k_{0}}{Q_{1}}\sin \left(\frac{k_{0}w}{2} \right) \right] \cdot \left[\cos \left(\frac{k_{0}w}{2}\right)  +\frac{k_{0}}{Q_{1}}\sin \left(\frac{k_{0}w}{2} \right) \right].
$$

The first term represents the even states and the second the odd states.