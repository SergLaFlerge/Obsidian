Last time, we found that

$$
\frac{d}{dt}\int_{-\infty}^{\infty}|\Psi (x, t)|^{2}dx = 0
$$

# Probability Current

We define $j_{x}$ as the probability current,

$$
j_{x} = -\frac{i \hbar}{2m}\left(\Psi^{*}\frac{\partial\Psi}{\partial x} - \frac{\partial\Psi^{*}}{\partial x}\Psi \right)
$$

We can then think of $|\Psi|^2$ as the probability density, which we now call $\rho (x, t)$. Then,

$$
\frac{\partial \rho}{\partial t} = -\frac{\partial}{\partial x}j_{x}
$$

Or, in three dimensions,

$$
\frac{\partial \rho}{\partial t} = -\nabla \cdot \vec{j}.
$$

This is analogous to current conservation in electrodynamics. Call it probability conservation, if you will.

Let's discuss another difference in quantum mechanics vs classical mechanics: Velocity

$$
\langle  v \rangle = \frac{d}{dt} \langle x \rangle
$$

After a great deal of calculations, we arrive at

$$
\langle v \rangle = \frac{i \hbar}{m}\int_{-\infty}^{\infty}\Psi^{*}\frac{\partial}{\partial x} dx
$$

This is actually not very useful, as there is no good way to relate this to its classical counterpart. Instead, it is more use fruitful to look at the momentum. If $p = mv$, then

$$
\begin{align}
\langle p \rangle & = m \langle v \rangle\\
& = -i \hbar \int_{-\infty}^{\infty}\Psi^{*}\frac{\partial}{\partial x}\Psi dx.
\end{align}
$$

Notice that both $\langle x \rangle$  and $\langle p \rangle$ can be expressed as

$$\int \Psi^{*}(\times) \Psi dx$$

and 

$$\int \Psi^{*}\left(-i \hbar \frac{\partial}{ \partial x}\right)\Psi dx$$ 

The terms in parenthesis are known as $\hat{x}$ and $\hat{p}$, respectively. $\hat{x}$ and $\hat{p}$ are known as *operators* .

**Claim:** All classical variables can be expressed in terms of $\hat{x}$ and $\hat{p}$.

Say we have a function $Q (x, p)$. How do we find $\langle Q \rangle$? Simply,

$$
\langle Q (x, p) \rangle = \int_{-\infty}^{\infty} \Psi^{*}\hat{Q}(\hat{x}, \hat{p})\Psi dx.
$$

We can see how much an actual value deviates from its expectation value $\langle Q \rangle$ by using $\sigma_{Q}$:

$$
\sigma_{Q} = \sqrt{\langle Q^{2}\rangle - \langle Q \rangle^{2}}
$$

## Does Ordering Matter?

To answer this question, we look at the commutator, $[\hat{x}, \hat{p}]$.

$$
[\hat{x}, \hat{p}] = \hat{x}\hat{p}-\hat{p}\hat{x}.
$$

If order does not matter, the commutator would be zero. To test this, we use a test function, $\Psi (x)$. If you do the calculation, you will find that

$$
[\hat{x}, \hat{p}] = i \hbar
$$

So the ordering does matter! Eventually, this would lead to Heisenberg's uncertainty principle.

The uncertainty principle is defined as

$$
\sigma_{x}\sigma_{p}\geq \frac{1}{2i}[\hat{x}, \hat{p}].
$$

## Links to Classical Mechanics

We know

$$
\frac{d}{dt}\langle x \rangle = \langle V \rangle = \frac{1}{m} \langle p \rangle.
$$

The Hamiltonian of a system can be defined as

$$
H = \frac{p^{2}}{2m}+ V.
$$

Taking the derivative of $H$ with respect to momentum, we get

$$
\frac{\partial H}{\partial t} = \frac{p}{m},
$$

which means that, in the world of quantum mechanics,

$$
\begin{align}
\frac{d\langle x \rangle}{dt} & =  \left\langle \frac{dH}{dt}\right\rangle = \frac{\langle p \rangle}{m}\\
\frac{d \langle p \rangle}{dt} & = - \left\langle \frac{\partial H}{\partial t}\right\rangle = \langle F \rangle.
\end{align}
$$

Here we run into a small problem: What we actually want is $F (\langle x \rangle)$, not $\langle F (x) \rangle$. But how much does that really matter? We can do an example and see.

$$
\begin{align}
F (x) & = ax^{2}\\
F (\langle x \rangle)& = \langle ax\rangle^{2} \\
& = a \langle x\rangle^{2} \\[1em]
\langle F (x)\rangle & = \langle ax^{2}\rangle\\
& = a \langle x^{2}\rangle \\[1em]
\langle F (x)\rangle - F (\langle x \rangle) & = a (\langle x^{2}\rangle - \langle x \rangle^{2})= \sigma_{x}^2
\end{align}
$$

So if $\sigma_{x}^{2}$ is small, then we recover Hamilton's equation, and you're back at classical mechanics. If, however, $\sigma_{x}^{2}$ is large, you do not recover Hamilton's equation, and you end up not in classical mechanics.