# The Free Particle

In classical mechanics, this is the simplest possible problem. If no forces act on our particle, then its velocity remains constant, and that's the end of the story. In quantum mechanics, however, our problem is not so simple.

We start by solving Schrödinger's equation with zero potential everywhere:

$$
\begin{align}
\hat{H} \psi & = E \psi \\
\frac{-\hbar^{2}}{2m}\dv[2]{\psi}{x} & = E \psi \\
\psi_{k} & = Ae^{ikx} + B e^{-ikx} \\
k & = \sqrt{\frac{2mE}{\hbar}}.
\end{align}
$$

Here, $k$ must be a real number, but $A, B$ can be complex. Then,

$$
E_{k} = \frac{k^{2}\hbar^{2}}{2m}.
$$

Now, we apply boundary conditions... But there are no boundary conditions? After all, our particle is not being affected by a potential source, which not only means we have no (current) way of finding $A$ and $B$, but $k$ can also be a continuous variable. Anyways,

$$
\begin{align}
\Psi_{k} (x, t) & = \exp \left(\frac{-iE_{k}}{\hbar}t \right) \psi_{k}(x)\\
& = A \exp \left[ik\left( x-\frac{\hbar k}{2m} \right)t \right] + B\exp \left[-ik\left( x +\frac{\hbar k}{2m} \right)t \right].
\end{align}
$$

The exponential terms represent a wave propagation to the right and to the left, respectively. If you know anything about waves, then you know the propagation terms are of the form

$$
\sin \left[k\left(x-\frac{\omega}{k} \right)t \right].
$$

The so-called "phase velocity" is given by the $\omega/k$ argument. Let $v_{ph}= \frac{\hbar k}{2m}$ be the phase velocity. Then we run into two problems:
1. Mathematically, this *is* a solution, but the lack of boundary conditions prevents us from normalizing the solution, so it looses all its physical meaning.
1. The second problem involves the energy: $$\begin{align}E_{k}& = \frac{p^{2}}{2m}\\ v_{ph}& = \sqrt{\frac{p^{2}}{2m}\cdot \frac{1}{2m}} = \sqrt{\frac{E_{k}}{2m}}\\ E_{k} & = 2mv_{ph}^2 \end{align}$$ but $$\begin{align}E_{k} & = \frac{mv_{c}^{2}}{2}, \end{align}$$ where $v_{c}$ is the "classical" wave velocity. So if we want consistency we need $E_{k, c}= E_{k, ph}$, then $$\frac{mv_{c}^{2}}{2} = 2mv_{ph}^{2}$$ is only true if $$v_{ph} = \frac{v_{c}}{2}.$$ Because of this, we get a third problem: $$\langle v \rangle = \dv{t}\langle x \rangle = 0,$$ and yet the particle should be moving. So what is going on?

## Plane Waves as a Tool

The solutions we obtained are not completely useless, thankfully. Because the Schrödinger equation is linear, we can still find a way to make our mathematically correct answer also make some physical sense. Our wavefunction still has the form

$$
\Psi (x, t) = \sum\limits_{n}C_{n}\psi_{n}(x)\exp \left(\frac{-iE_{n}t}{\hbar} \right).
$$

However, because our solution allows for a continuum instead of discrete values, the sum becomes an integral:

$$
\Psi (x, t) = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\phi (k)\cdot e^{ikx}\cdot \exp \left(\frac{-i \hbar k^{2}t}{2m} \right)\dd{k}.
$$

$k$ is our wave number, where $k > 0$ implies motion to the right, and $k < 0$ implies motion to the left. Now what we want to find is $\phi (k)$, which takes the place of our coefficients $C_{n}$. At $t = 0$,

$$
\Psi (x, 0) = \frac{1}{\sqrt{2k}}\int_{-\infty}^{\infty}\phi (k)\cdot e^{ikx}\dd{k}.
$$

This is a Fourier transform. We have a theorem that guarantees

$$
\int_{-\infty}^{\infty}\abs{\Psi (x, 0)}^{2} \dd{x} = \int_{-\infty}^{\infty}\abs{\phi (k)}^{2}\dd{k}= 1,
$$

so now we have a solution that is normalizable, which solves our first problem.

Physically speaking, $\abs{\phi (k)}$ is related to the probability of $\Psi (x, t)$ having a momentum $p \in [\hbar k, \; \hbar (k + \dd{k})]$ for a given energy $E \in [\frac{\hbar^{2}k^{2}}{2m}, \; \frac{\hbar^{2}k^{2}}{2m}+ \frac{\hbar^{2}k}{m}\dd{k}]$.