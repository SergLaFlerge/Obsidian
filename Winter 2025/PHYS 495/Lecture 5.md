# Fourier Decomposition of the Scalar Field

We can Fourier decompose the field $\phi (x)$ as

$$
\phi (x) = \frac{1}{(2 \pi)^{3/2}}\int \delta (p^{2}-m^{2})A (p)e^{-ip \cdot x}\dd[4]{p},
$$

where $p \cdot x$ is understood to be $\eta_{\mu\nu}p^{\mu}x^{\nu}$, and it is *not* the regular dot product.

We have a factor of $\delta (p^{2}-m^{2})$ to ensure the integral satisfies $(\square + m^{2})\phi (x) = 0$, i.e. the integral vanishes.

We can assume that $\phi (x)$ is Hermitian — $\phi (x) = \phi^{\dagger}(x)$. This implies that $A (-p) = A^{\dagger}(p)$.

We can introduce the theta function $\Theta (p^{0})$ and rewrite the field as

$$
\phi (x) = \frac{1}{(2 \pi)^{3/2}}\int \delta (p^{2}-m^{2})\Theta (p^{0})\left(A (p)e^{-ip \cdot x} + A^{\dagger}(p)e^{ip \cdot x} \right)\dd[4]{p}.
$$

This is done in homework 1. We can also eliminate $p^{0}$ from the equation using the definition of $\delta (f (z))$. Then,

$$
\phi (x) = \int \frac{a (p)e^{-ip \cdot x}+ a^{\dagger}(p)e^{ip \cdot x}}{\sqrt{(2 \pi)^{3}2 E_{p}}}\dd[3]{p},
$$

with

$$
a (p) = \frac{A (p)}{ \sqrt{2 E_{p}}}.
$$

We can do the same for the momentum and obtain

$$
\Pi (x) = \dot{\phi}(x)\int i \sqrt{\frac{E_{p}}{2 (2 \pi^{3})}}\left(-a (p)e^{-ip \cdot x} + a^{\dagger}(p) e^{ip \cdot x} \right)\dd[3]{p}.
$$

The total Hamiltonian is then

$$
H = \frac{1}{2}\int E_{p}\left[a^{\dagger}(p)a (p)+ a (p)a^{\dagger}(p) \right]\dd[3]{p}
$$