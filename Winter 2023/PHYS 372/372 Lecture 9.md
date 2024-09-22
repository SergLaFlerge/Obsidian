From last class, we continue. Recall the relation we had found earlier,

$$
v_{c} = 2v_{p}.
$$

This looks very similar to what we found, and indeed,

$$
v_{c} = v_{g} = 2v_{p},
$$

with

$$
\begin{align}
\omega & = \frac{\hbar k^{2}}{2m}\\[1em]
\dv{\omega}{k} & = \frac{\hbar k}{m}.
\end{align}
$$

It is obvious then, that

$$
v_{p} = \frac{\omega}{k} = \frac{\hbar k}{2m}.
$$

# General Case

So far, we have worked with two extremes:
1. $V (\pm \infty) = \infty$, which relates to the infinite square we whose solutions are bound states, and
2. $V = 0$ everywhere, which relates to the free particle. This gave us continuous energy and non-normalizable solutions.

Every other case can be thought of as a combination of these two extremes.

![[372 Sample Potential|center]]

Classically, any energy is allowed, but in quantum mechanics, we have seen that there are only certain allowed energies for the bound state. The scattering state does however resemble the classical case, which allows continuous energy levels. So naturally a full solution with one of these potentials would look like

$$
\begin{align}
\Psi (x, t) & =  \underbrace{\sum\limits_{n}C_{n}\exp \left(\frac{-iE_{n}t}{\hbar} \right)\psi_{n}(x)}_{\text{bound state}} +  \underbrace{\int \phi (k) \exp \left(\frac{-iE_{k}t}{\hbar}\right) \psi_{k}(x) \dd{k}}_{\text{scattering state}}\\[1em]
C_{n} & = \int_{-\infty}^{\infty}\psi_{n}^{*}\Psi (x, 0)\dd{x}\\[1em]
\phi (k) & = \int_{-\infty}^{\infty}\psi_{k}^{*}\Psi (x, 0)\dd{x}\\[1em]
1 & = \sum\limits_{n}\abs{C_{n}}^{2} + \int \abs{\phi (k)}^{2}\dd{k}
\end{align}
$$

Insert images here whenever you have time.

# The Dirac $\delta (x)$ Function

There are several definitions of the $\delta$ function. The most basic is

$$
\begin{align}
\delta  & = 
\begin{cases}
\infty, \quad x = 0, \\
0, \quad x \neq 0
\end{cases}\\[1em]
& \int_{-\epsilon}^{\epsilon} \delta (x)\dd{x}  = 1 , \; \forall \; \epsilon > 0.
\end{align}
$$

This is nice, but it doesn't give us much to work with. Another definition is the Heaviside function definition:

$$
\begin{align}
\int_{-\infty}^{x}\delta (x')\dd{x'} & = \Theta (x)\\[1em]
\Theta (x) & =
\begin{cases}
1 \quad x > 0 \\
0 \quad x \leq 0
\end{cases} \qq{.}
\end{align}
$$

This definition will be useful to us in the future, but it is still not what we're looking for. The "correct" definition of the $\delta$ function is that it is a distribution function. It is a map $f (x)\mapsto f (0)$, with the following properties:

$$
\begin{align}
\int_{-\infty}^{\infty}f (x)\delta (x-a)\dd{x} & = f (a)\\
\dv{\Theta}{x}& = \delta (x)\\
\delta (x) & = \lim_{\Delta \rightarrow \infty}\frac{1}{\Delta \sqrt{2 \pi}}\exp \left(\frac{-x^2}{4 \Delta^{2}} \right).
\end{align}
$$

This is by far the most useful definition, as it gives some insight into what we can do with the $\delta$ function. For now, we use it as a potential well, and see what solutions we can come up with.

# The $\delta$ Potential

![[372 Delta Potential|center]]

The Hamiltonian is simple:

$$
\hat{H} = \frac{p^{2}}{2m}-\alpha \delta (x).
$$

Moving to the time independent Schrödinger equation:

$$
\frac{-\hbar^{2}}{2m}\dv[2]{x}\psi (x)-\alpha\delta (x) = E \psi (x).
$$

From our previous knowledge, we expect to see bound states for $E < 0$, and scattering states for $E > 0$.

Let us start with the bound states: For $E < 0$, we have

$$
\begin{align}
E & = \frac{-\hbar k^{2}}{2m}\qc \qq{k real,} x \neq 0\\
\dv [2]{x}\psi (x) & = k^{2} \psi (x).
\end{align}
$$

This differential equation has solutions of the form

$$
\begin{align}
\psi (x) & =  Ae^{-kx} + Be^{kx}\\
&  \quad \quad \; \Downarrow
\end{align}
$$

![[372 Delta Bound States 1|center]]

The intersection of the two exponentials must be the same, so

$$
\begin{align}
\psi (x) &=
\begin{cases}
Ae^{-kx}\qc x < 0 \\
Ae^{kx}\qc x > 0
\end{cases}\\
& \quad \quad \quad \Downarrow
\end{align}
$$

```tikz
\usepackage{xcolor}
\usepackage{pgfplots}
\definecolor{cyan}{HTML}{00FFFF}
\begin{document}
\begin{tikzpicture}[
	declare function={
		delta(\x) = (\x < 0)*(1/2)*exp(0.5*\x) + (\x >= 0)*(1/2)*exp(-0.5*\x)
		;
		}
]
\begin{axis}[ color = white,
axis x line = middle, axis y line = middle,
ymin = -0.5, ymax = 1.5, ylabel = \(V(x)\),
xmin = -7, xmax = 7 , xlabel = \(x\),
ticks = none,
domain = -7:7,
samples = 400,
]
\addplot[cyan, thick]{delta(x)};
\node[label = {[text=cyan]0:{$A$}},circle,fill, color=cyan, inner sep = 2pt] at (axis cs:0,0.5) {}; 
\end{axis}
\end{tikzpicture}
\end{document}
```

Notice that

$$
\begin{align}
\eval{\dv{\psi}{x}}_{0^{+}} & = -kA \\[1em]
\eval{\dv{\psi}{x}}_{0^{-}} & = kA
\end{align}
$$

Look a lot like $\Theta (x)$...