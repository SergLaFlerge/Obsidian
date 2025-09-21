# The Hydrogen Atom

$$
\begin{align}
V (r) & = \frac{-e^{2}}{4 \pi \epsilon_{0}}\frac{1}{r} \\[1em]
\dv[2]{u}{\rho} & = \left(1-\frac{\rho_{0}}{\rho}+ \frac{l (l + 1)}{\rho^{2}} \right)u \\[1em]
\rho & = kr \qc \rho_{0} = \frac{me^{2}}{2 \pi \epsilon_{0}\hbar^{2}k}.
\end{align}
$$

Using the power series method we obtain two cases:

$$
\begin{align}
\rho \rightarrow \infty:\quad \dv[2]{u}{\rho} & \approx u \rightarrow u = Ae^{-\rho} + Be^{\rho} \\[1em]
\rho \rightarrow 0:\quad \dv[2]{u}{\rho} & \approx \frac{l (l + 1)}{l^{2}}u \rightarrow u = C \rho^{l + 1}+ D \rho^{-l}.
\end{align}
$$

These are asymptotic behaviors, but we want to see what happens in between the two. We can immediately get rid of the rightmost terms from the equations above, as they are not physical. We can then combine them together, along with some polynomial $\nu(\rho)$, that will give us a reasonable approximation between our two extremes. Let $u (\rho)= \rho^{l + 1}e^{-\rho}\nu (\rho)$. Now, our initial equation changes to

$$
\begin{align}
\rho\dv[2]{u}{\rho} &+ 2 (l + 1-\rho)\dv{\nu}{\rho}+ (\rho_{0}-2 (l + 1))\nu = 0, \\[1em]
\nu (\rho) & = \sum\limits_{i = 0}^{n_{r}}C_{i}\rho^{i}.
\end{align}
$$

We find a recursive relation from the $C_{i}$'s:

$$
\begin{align}
C_{i + 1} & = N_{i}C_{i} \\
N_{i} & = N_{i}(n_{r};, l, \rho_{0}) \\[1em]
i & = n_{r} \Rightarrow C_{n_{r}+ i} = N_{n_{r}} = 0 \\[1em]
\rho_{0} & = 2 (n_{r}+ l + 1) \\[1em]
\rho_{0} & = 2n \qc n = n_{r}+ l + 1.
\end{align}
$$

These polynomials are known as the *associated Leguerre polynomials* $\mathrm{L}_{\beta}^{\alpha}(x)$.

$$
\nu (\rho) = \mathrm{L}_{n_{r}}^{2 lm}(2 \rho).
$$

Then, one can find that

$$
\begin{align}
k & =  \frac{1}{na_{B}}, \\[1em]
a_{B} & = \frac{4 \pi \epsilon_{0}\hbar^{2}}{me^{2}} \approx 0.529 \cdot 10^{-10}m
\end{align}
$$

and so we see that energy is quantized!

$$
\begin{align}
E \Rightarrow E_{n} & = \frac{-\hbar^{2}kn^{2}}{2m} \\[1em]
& = \frac{E_{1}}{n^{2}} \\[1em]
E_{1} & = \frac{-m}{2 \hbar^{2}}\left(\frac{e^{2}}{4 \pi \epsilon_{0}} \right)^{2} \\[1em]
& = 13.6 \;eV.
\end{align}
$$

So we have three numbers that seem to dictate how the atom behaves:
- $n \geq 1$, where $n = n_{r}+ l + 1$.
- $l \geq 0$, where $0 \leq l \leq n - 1$.
- $\abs{m}\leq l \approx 2 l + 1$, with $\sum\limits_{1}^{n-1}2 l - 1= n^{2}$.

So we have three quantum numbers: $n$ gives us the energy, and shows that energy is quantized. $l$ gives us angular momentum quantization. What is $m$? We shall find out next lecture.

What we have now is a wavefunction that describes the electron inside the hydrogen atom:

$$
\begin{align}
\Psi_{nlm}(r, \theta, \phi) & = A_{r}\left(\frac{r}{a_{B}n} \right)^{l}\exp\left(\frac{-r}{a_{B}n}\right)\mathrm{L}_{n-l-1}^{2 l + 1}\left(\frac{2 r}{a_{B}n} \right)Y_{l}^{m}(\theta, \phi)
\end{align}
$$

# Angular Momentum

For angular momentum $L$, we have
- $L^{2}= \hbar^{2}l (l + 1)$.
- $L^{2}= \vec{L}\cdot \vec{L}$.
- And the classical $\vec{L}= \vec{r}\times \vec{p}$.

What we now have to do is to find an operator $\hat{Q}$ that behaves the same way. Since $\hat{Q}= \hat{Q}(\vec{r}, \vec{p})$, we have in the position space that $\vec{r}= \vec{r}$, and $\vec{p}=-i \hbar \vec{\nabla}$. Going from classical to quantum, we get

$$
\begin{align}
\hat{\vec{L}} & = \hat{\vec{r}}\times \hat{\vec{p}} \\[1 em]
& = \vec{r} \times (-i \hbar \vec{\nabla}) \\[1 em]
\hat{\vec{L}} & = -i \hbar \left[\left(y \pdv{z}-z \pdv{y} \right)\hat{n}_{x} + \left(z \pdv{x}-x \pdv{z} \right)\hat{n}_{y} + \left(x \pdv{y}-y \pdv{x} \right)\hat{n}_{z} \right].
\end{align}
$$

We will call each term $\hat{L}_{x}, \; \hat{L}_{y}, \hat{L}_{z}$. As with every new operator, we should check what properties it has. Let us start with commutativity, which one should expect is not commutative. Indeed,

$$
\begin{align}
\comm{\hat{L}_{x}}{\hat{L}_{y}} & = \hat{L}_{x}\hat{L}_{y}-\hat{L}_{y}\hat{L}_{x} \\[1em]
& = -\hbar^{2}\left(y \pdv{x}\comm{\pdv{z}}{z}+ x \pdv{y}\comm{z}{\pdv{z}} \right) \\[1em]
& = -\hbar^{2}\left(x \pdv{y}-y \pdv{x} \right) \\[1em]
& = \frac{\hat{L}_{z}}{i \hbar} \\[1em]
&\therefore \\[1em]
\comm{\hat{L_{x}}}{\hat{L}_{y}} & = i \hbar \hat{L}_{z} \\[1 em]
\comm{\hat{L}_{y}}{\hat{L}_{z}} & = i \hbar \hat{L}_{x} \\[1 em]
\comm{\hat{L}_{z}}{\hat{L}_{x}} & = i \hbar \hat{L}_{y}.
\end{align}
$$

As  expected, the operators do not commute. How about $\hat{L}^{2}$? If you compute the commutator $\comm{\hat{L}^{2}}{ \hat{L}_{n}}$, you find that you get $0$, so the operators commute with $\hat{L}^{2}$. What this means is that, unlike the original case, $\hat{L}^{2}$ can share a set of eigenfunction with *one* of the operators. By convention we choose $\hat{L}_{z}$, and so letting $\psi_{\lambda \mu}(\vec{r})$, we have

$$
\begin{align}
\hat{L}^{2} \psi_{\lambda \mu} & = \lambda \psi_{\lambda \mu} \\[1em]
\hat{L}_{z} \psi_{\lambda \mu} & = \mu \psi_{\lambda \mu}.
\end{align}
$$

From the radial equation, we know that $\lambda = \hbar^{2}l (l + 1)$. Now we find what $\mu$ is. We define a new set of ladder operators:

$$
\begin{align}
\hat{L}_{\pm} & = \hat{L}_{x}\pm i\hat{L}_{y} \\[1 em]
\comm{\hat{L}^{2}}{\hat{L}_{\pm}} & = 0 \\[1 em]
\comm{\hat{L}_{z}}{\hat{L}_{+}} & = \hbar \hat{L}_{+} \\[1 em]
\comm{\hat{L}_{z}}{\hat{L}_{-}} & = \hbar \hat{L}_{-}.
\end{align}
$$

Applying the raising operator to $\psi_{\lambda \mu}$, we get

$$
\begin{align}
\hat{L}_{z}\hat{L}_{+} \psi_{\lambda \mu} & = \comm{\hat{L}_{z}}{\hat{L}_{+}}\psi_{\lambda \mu} + \hat{L}_{+}\hat{l}_{z}\psi_{\lambda \mu} \\[1 em]
& = (\mu \hbar)\hat{L}_{+}\psi_{\lambda \mu}
\end{align}
$$