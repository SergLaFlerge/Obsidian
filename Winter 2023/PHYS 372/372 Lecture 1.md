# Why?

The goal of classical mechanics is as follows: A particle of mass $m$ is moving at speed $v$ in the $x-$direction. Where will the particle be at time $t$? In other words, we want to find a function $x (t)$ that describes the position of the particle for all points in time. Knowing this, and some calculus, we can find pretty much every other piece of information about the particle, like its velocity, acceleration, energy, etc. To accomplish this, we start with Newton's Law,

$$
F = ma
$$

And solve the differential equation. This gives all possible solutions to the system, and knowing some initial conditions gives the exact path the particle will follow. That is all of classical mechanics.

Quantum mechanics seeks to answer the same question, but here, we want to find what we call the *wavefunction*,

$$
\Psi (x, t)
$$

And we use an analog of Newton's second law, called *Schrödinger's Equation*:

$$
\begin{align}
i \hbar \frac{\partial}{\partial t}\Psi (x, t) = \frac{1}{2m}\left(-i \hbar\frac{\partial}{\partial x}\right)^{2}\Psi (x, t)+ V (x, t)\Psi (x, t)
\end{align}
$$

