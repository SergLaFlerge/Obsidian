![[372 Simple Harmonic Oscillator|center]]

We look at the simple harmonic oscillator: A mass $m$ with potential energy $(1/2)kx^{2}$, total energy $E$, frequency $\omega= \sqrt{k/m}$, amplitude $x_{0}$, initial momentum $p_{0}= m \omega_{0}x_{0}$, and finally, force $F =-kx$. Once again, the main goal here is to find a link between classical mechanics and quantum mechanics.

## Classical Solution

The key here is to find $xp$ in terms of $E$. For that, we find first $x (E, p)$:

$$
\begin{align}
E & = \frac{p^{2}}{2m}\\
& = \frac{1}{2}kx_{0}^{2}\\
&\therefore\\
x_{0}& = \sqrt{\frac{2E}{k}}, \quad \text{and}\quad p_{0}= \sqrt{2mE} \\
x_{0}p_{0}& = \frac{2E}{\omega}\\
x_{0}& = \frac{2E}{\omega p_{0}}\\
\langle x \rangle & \sim \frac{E}{\omega p_{0}}
\end{align}
$$

The last term is meant as an approximation; we are making an educated guess in the same order of magnitude (in this case, we're guessing exactly half, which is a reasonable approximation). From here, we make another approximation,

$$
\sigma_{x}\sigma_{p}\sim \hbar,
$$

where again we only really care about being in the same order of magnitude as $\hbar$. We will make a guess that $\sigma_{p}\sim p_{0}$, or in words, we are saying that $\sigma_{p}$ is maximal, and seeing what happens to $\sigma_{x}$:

$$
\begin{align}
\sigma_{x}& = \frac{\hbar}{p_{0}}\\
& = \frac{\hbar}{\frac{E}{\omega \langle x \rangle}}\\
\frac{\sigma_{x}}{\langle x \rangle}& \sim \frac{\hbar\omega}{E}
\end{align}
$$

From previous courses, we know that $E \sim n \hbar \omega$, so

$$
\begin{align}
\frac{\sigma_{x}}{\langle x \rangle}& \sim \frac{1}{n}.
\end{align}
$$

which is a real life result :)

# Time Independent Schrödinger's Equation

As the name of this section implies, we shall solve the time independent Schrödinger's equation using separation of variables. The time independence really only means that our potential is constant in time, i.e. $V (x, t)= V (x)\; \forall \; t$. This is crucial however, since we otherwise wouldn't be able to separate the variables.

The Schrödinger equation reads

$$
\frac{i \hbar}{2m}\frac{\partial}{\partial t}\Psi (x, t) = \frac{\hbar^{2}}{2m}\frac{\partial^{2}}{\partial x^{2}}\Psi (x, t)+ V (x)\Psi (x, t).
$$

We look for solutions of the form

$$
\Psi (x, t) = \psi (x)\phi (t)
$$

and substitute this guess into Schrödinger's equation:

$$
\frac{i \hbar}{2m}\frac{\partial}{\partial t}\psi \phi = -\frac{\hbar}{2m}\frac{\partial^{2}}{\partial x^{2}}\psi \phi + V \psi \phi.
$$

Dividing the variables separates them:

$$
\frac{i \hbar}{2m}\cdot \frac{1}{\phi}\frac{d \phi}{dt} = -\frac{\hbar^{2}}{2m}\cdot \frac{1}{\psi}\frac{d^{2}\psi}{dx^{2}}+ V \psi = E
$$

$E$ is just a constant, since two functions of different variables can only be equal to each other if they are equal to a constant. This turns our partial differential equation into *two* ordinary differential equations, which are **much** easier to tackle.

$$
\begin{align}
\frac{d \phi}{dt} & = -\frac{2mEi}{\hbar}\phi \\
\phi & = \exp \left(-\frac{iE}{\hbar}t \right) \\[1em]
\frac{-\hbar^{2}}{2m}\frac{d^{2}\psi}{dx^{2}}+ V \psi & = E \psi
\end{align}
$$

The second equation is The Time Independent Schrödinger Equation. Solutions to the time independent Schrödinger equation are called stationary states.

## Stationary States

We have an operator $\hat{Q}(\hat{x}, \hat{p})$. $\hat{Q}$ is stationary if

$$
\frac{d}{dt}\hat{Q}= 0
$$

Let's look at energy:

$$
\begin{align}
E & = \frac{p^{2}}{2m}+ V (x)\\
\hat{H} & = \frac{\hat{p}^{2}}{2m}+ V (x).
\end{align}
$$

Notice we can rewrite the time independent Schrödinger equation using the Hamiltonian operator:

$$
\hat{H}\psi = E \psi,
$$

and this is a textbook eigenvalue problem, where $\psi(x)$  is the eigenfunction, and $E$ is the eigenvalue. Let us look at the expectation value of $H$, $\langle H \rangle$:

$$
\begin{align}
\langle H \rangle & = \int_{-\infty}^{\infty}\Psi^{*}\hat{H} \Psi dx\\
& = E \int_{-\infty}^{\infty}\Psi^{*}\Psi dx \\
& = E (1)\\
& = E.
\end{align}
$$

Now,

$$
\begin{align}
\sigma_{H}^{2}& = \langle H^{2}\rangle-\langle H \rangle^{2}.
\end{align}
$$

We know $\langle H \rangle = E$, so $\langle H\rangle^{2} = E^{2}$. For $\langle H^{2} \rangle$, we re-evaluate:

$$
\begin{align}
\langle H \rangle^{2}& = \int_{-\infty}^{\infty}\psi^{*}\hat{H}^{2}\psi dx = E^{2},
\end{align}
$$

so

$$
\sigma_{H}= 0.
$$

So $\sigma_{H}$ is invariant! Not everything in quantum mechanics is uncertain; $E$ is a stationary state in the time independent Schrödinger equation.

If your function is an eigenfunction of an operator $\hat{Q}$,

$$
\hat{Q}\psi = q \psi
$$

Then it is a stationary state.

There's an infinite number of allowable solutions to the TISE,

$$
\Psi_{n}(x, t) = \exp\left(\frac{-iE_{n}t}{\hbar}\right)\psi_{n}(x),
$$

and none of these by itself is a general solution. However, it should be clear that because $\psi_{n}$ are eigenfunctions, they *must* be orthogonal. This means that a more general solution can be constructed using a linear combination of all the eigenfunctions. That is,

$$
\Psi (x, t) = \sum\limits_{n = 1}^{\infty}C_{n}\exp \left(\frac{-iE_{n}t}{\hbar}\right)\psi_{n}(x),
$$

with initial conditions

$$
\Psi (x, 0) = \sum\limits_{n = 1}^{\infty}C_{n}\psi_{n}(x)
$$