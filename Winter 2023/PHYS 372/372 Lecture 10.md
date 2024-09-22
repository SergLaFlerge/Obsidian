One of the ways we described $\delta (x)$ was as the derivative of the Heaviside function $\Theta (x)$. Looking at the time independent Schrödinger equation again:

$$
\dv[2]{\psi}{x}+ \frac{2m \alpha}{\hbar^{2}} + \delta (x)\psi (x) = k^{2}\psi (x)
$$

and integrating over a small interval $[-\epsilon, \epsilon]$, we get

$$
\begin{align}
\int_{-\epsilon}^{\epsilon}\dv[2]{\psi}{x}\dd{x}+ \frac{2m \alpha}{\hbar^{2}}\int_{-\epsilon}^{\epsilon}\delta (x)\psi (x)\dd{x} & = k^{2}\int_{-\epsilon}^{\epsilon}\psi (x)\dd{x}\\[1em]
\eval{\dv{\psi}{x}}_{0^{-}}^{0^{+}}+ \frac{2m \alpha}{\hbar^{2}}\psi (0) & = k^{2}\order{\epsilon}\Rightarrow \qq{arbitrarily small.}\\[1em]
-2kA+ \frac{2m \alpha}{\hbar^{2}}A & = \cancelto{0}{k^{2}\order{\epsilon}}\qq{as} \epsilon \rightarrow 0 \\[1em]
\cancel{2}k \cancel{A} & = \frac{\cancel{2}m \alpha}{\hbar^{2}}\cancel{A}\\[1em]
k & = \frac{2 \alpha}{\hbar^{2}}\\[1em]
E & = \frac{-\hbar^{2}k^{2}}{2m}= \frac{-m \alpha^{2}}{2 \hbar^{2}}
\end{align}
$$

Notice that there is only one bound state as opposed to the infinite square well or the simple harmonic oscillator, which have an infinite — if discreet — number of bound states. We now know

$$
\begin{align}
\psi (x) & = Ae^{-k \abs{x}}\\[1em]
\int_{-\infty}^{\infty}\psi^{*}\psi \dd{x}& = 1 \Rightarrow A = \sqrt{k}\\[1em]
\psi & = \left(\frac{m \alpha}{\hbar^{2}} \right)^{1/2}\exp \left(\frac{-m \alpha}{\hbar^{2}}\abs{x} \right).
\end{align}
$$

With that, we have finished the bound state . Next comes the complicated bit: The scattering state.

## Scattering States

For the scattering states, we naturally expect solutions that are similar are the free particle problem. The standard free particle problem gives solutions that are not necessarily physical, but we will see that this won't be a be problem anymore. We will have two regions, corresponding to $x < 0$ and $x > 0$.

$$
\begin{align}
(1)\quad \psi_{k} & = Ae^{ikx} + Be^{-ikx}\\
(2) \quad \psi_{k} & = Ce^{ikx} + De^{-ikx},
\end{align}
$$

where $(1)$ is the region $x < 0$, and $(2)$ is the region $x > 0$. The terms with $e^{ikx}$ represent the right-moving waves, while the terms with $e^{-ikx}$ represent the left-moving waves. Now we apply the boundary conditions:

1. $\psi_{k}(0^{-})= \psi_{k}(0^{+})$.
2. $\eval{\dv{x}\psi_{k}}_{0^{+}}-\eval{\dv{x}\psi_{k}}_{0^{-}} = \frac{-2m \alpha}{\hbar^{2}}\psi_{k}(0)$.

BC1 implies that $A + B = C + D$. BC2 then says

$$
\begin{align}
(C-D)ik - (A-B)ik & = \frac{2m \alpha}{\hbar^{2}}(A+  B) \qq{or} (C + D)\\[1em]
C-D & = A \left(1 + 2i \underbrace{\frac{m \alpha}{k\hbar^{2}}}_{\beta} \right) - B \left(1-2i \underbrace{\frac{m \alpha}{k \hbar^{2}}}_{\beta} \right)\\[1em]
C-D & = A (1 + 2i \beta) -B (1-2i \beta)
\end{align}
$$

<br>
<br>

```tikz
\usepackage{xcolor}
\usepackage{pgfplots}
\definecolor{cyan}{HTML}{00FFFF}
\begin{document}
\begin{tikzpicture}[
	declare function = {
	func(\x) = -20*exp(-x^2)
	;
	}
]
\begin{axis}[ color = white,
axis x line = middle, axis y line = middle,
ymin = -20, ymax = 20, ylabel = {\(V(x)\)},
xmin = -10, xmax = 10, xlabel = {\(x\)},
ticks = none,
domain = -10:10,
samples = 400,
]
\addplot[cyan,thick]{func(x)};
\node (ST1) at (axis cs:-7.5,10){};
\node (DT1) at (axis cs:-2.5,10){};
\node (ST2) at (axis cs:2.5,10){};
\node (DT2) at (axis cs:7.5,10){};
\node (SR1) at (axis cs:-7.5,-10){};
\node (DR1) at (axis cs:-2.5,-10){};
\node (SR2) at (axis cs:2.5,-10){};
\node (DR2) at (axis cs:7.5,-10){};
\draw[->,line width = 1pt] (ST1) -- (DT1) node[midway,above = 3pt]{\(Ae^{ikx}\)};
\draw[->,line width = 1pt] (ST2) -- (DT2) node[midway, above = 3pt]{\(Ce^{-ikx}\)};
\draw[->,line width = 1pt] (DR1) -- (SR1) node[midway, below = 3pt]{\(Be^{-ikx}\)};
\draw[->,line width = 1pt] (DR2) -- (SR2) node[midway, below = 3pt]{\(De^{-ikx}\)};
\end{axis}
\end{tikzpicture}
\end{document}
```
<br>

Let us focus on one direction only, i.e. let $D = 0$. Then

$$
\begin{align}
A + B & = C \\
A (1 + 2i \beta)-B (1-2i \beta) & = C \\[1em]
B = \frac{i \beta}{1-i \beta}A, \quad C & = \frac{i \beta}{1 + i \beta}A
\end{align}
$$

This is a representation of the case where a *stream* of particles is traveling to the right, and it either keeps moving right, or reflects and moves left. Because this is a stream of particles, we don't need to normalize the solutions; The particles together can have a greater than $100 \%$ probability of being anywhere in space. This makes our solutions much easier to work with. This physical representation is a good justification for why $D = 0$, as a stream of particles moving from left to right can't have started on the left. These coefficients are once again related to probabilities: Let

$$
\begin{align}
R & = \frac{\abs{B}^{2}}{\abs{A}^{2}} = \frac{\text{reflected}}{\text{incident}}\\[1em]
T & = \frac{\abs{C}^{2}}{\abs{A}^{2}} = \frac{\text{transmitted}}{\text{incident}}\\[1em]
R & = \frac{\beta^{2}}{1 + \beta^{2}}, \quad T  = \frac{1}{1 + \beta^{2}}.
\end{align}
$$

From these, we can glean two things:
1. $R + T = 1$.
2. These values depend on $k$ (and therefore $E$).

If $D \neq 0$, then $A = 0$. It is a mirror map $x \mapsto-x$, and as such it is also a mirror solution to the one above.

For $V (x)=-\alpha \delta (x)$ then, we obtain two types of solutions:
1. A single bound state for $E < 0$, with solution $$\psi_{1}= \left(\frac{m \alpha}{\hbar^{2}} \right)^{1/2}\exp \left(\frac{-m \alpha \abs{x}}{\hbar^{2}} \right)\qc E_{1} = \frac{-m \alpha^{2}}{2 \hbar^{2}} .$$
2. Continuous solutions for $E > 0$:
	$$
	\psi_{k} = 
	\begin{cases}
     e^{ikx}+ \frac{i \beta}{1-i \beta}, \qq{for} &x < 0 \\
     \frac{1}{1-i \beta}, \qq{for} &x > 0
    \end{cases}. 
 $$