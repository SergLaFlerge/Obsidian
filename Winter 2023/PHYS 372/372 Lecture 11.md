# Scattering Matrix

For the $\delta$ potential problem, the scattering states can be represented by a matrix. If we  fix two values as we did last class, the other two can be obtained. This gives the matrix

$$
\begin{bmatrix}
C \\ B
\end{bmatrix}
=
\begin{bmatrix}
S_{RR} & S_{RL} \\ S_{LR} & S_{LL}
\end{bmatrix}
\cdot
\begin{bmatrix}
A  \\  D
\end{bmatrix}.
$$

The $2 \times 2$ matrix is called the *scattering matrix*, or the *S-matrix*. If we take $D = 0$ as we did last time, then $C = S_{RR}A$, $B = S_{LR}A$. For the $\delta$ potential,

$$
S_{RR} = \frac{1}{1-i \beta}, \quad S_{LR} = \frac{i \beta}{1-i \beta},
$$

where

$$
\beta = \frac{m \alpha}{\hbar^{2}k}.
$$

If we make $A = 0$ instead, we get

$$
S_{LL} = \frac{1}{1-i \beta}, \quad S_{RL} = \frac{i \beta}{1-i \beta}.
$$

Therefore,

$$
S = \frac{1}{1-i \beta}
\begin{bmatrix}
1 & i \beta \\ i \beta & 1
\end{bmatrix}.
$$

Note that $S$ is unitary; $S^{\dagger}\cdot S = 1$.

# The Finite Square Well
<br>
<br>

```tikz
\usepackage{xcolor}
\usepackage{pgfplots}
\definecolor{cyan}{HTML}{00FFFF}
\begin{document}
\begin{tikzpicture}
\begin{axis}[
color = white,
axis x line = middle, axis y line = middle,
ymin =-2, ymax = 0.5, ylabel ={\(V (x)\)},
xmin = -4, xmax = 4, xlabel ={\(x\)},
ticks = none,
domain =-4:4,
samples = 400,
%grid = both
]
\addplot[cyan, thick,const plot,no marks]coordinates{(-4,0) (-2,-1.5) (2,0) (4,0)}
node[above =-20pt, pos = 0.53, color = white]{$V=-V_{0}$} 
node[below = 1.5pt, pos = 0.15, color = white]{$V = 0$}
node[below = 52pt, pos = 0.90, color = white]{$V = 0$};
\node[label = {[text=cyan]45:{$-a$}},circle,fill, color=cyan, inner sep = 2pt] at (axis cs:-2,0) {};
\node[label ={[text = cyan]135:{$a$}}, circle, fill, color = cyan, inner sep = 2pt] at (axis cs:2,0) {};
\node (S) at (axis cs:-2.2,-1.6){}; % add alittle extra to cover
\node (D) at (axis cs:2.2,-1.6){}; % the whole range
\draw[<->, line width = 1pt] (S) -- (D) node[pos = 0.4, below = 3pt]{$2a$};
\end{axis}
\end{tikzpicture}
\end{document}
```
<br>
<br>

In this case, our potential looks like

$$
V (x) =
\begin{cases}
-V_{0}, \quad &x \leq \abs{a} \\
\; \; \; \,0, \quad &x \geq \abs{a}
\end{cases}.
$$

The general spectrum of the Hamiltonian is split between two regions:
1. $E < 0$, which implies bound states and a discreet spectrum.
2. $E > 0$, which implies scattering states and a continuous spectrum.

Here, we will have to work at both solutions at the same time, since the well is finite, and there are no infinities to separate the two regions. Starting with the bound states,

$$
\begin{align}
\frac{-\hbar^{2}}{2m}\dv[2]{\psi}{x}+ V (x)\psi (x) & = E \psi (x)\\[1em]
\dv [2]{\psi}{x} & = -\left(\frac{2m [E-V (x)]}{\hbar^{2}} \right)\psi (x)\\[1em]
E & = \frac{\hbar^{2}k^{2}}{2m}.
\end{align}
$$

Outside $\abs{x}< a$, $V (x)= 0$, so

$$
\begin{align}
\dv [2]{\psi}{x} & = k^{2}\psi (x)\\[1em]
\psi (x) & = Ae^{-kx}+ Be^{kx}.
\end{align}
$$

As usual, we must remove the pieces that blow up to infinity, therefore

$$
\psi (x) =
\begin{cases}
Ae^{-kx}\qc &x > a \\
Be^{kx}\qc &x < a
\end{cases}.
$$

Inside $\abs{x} <a$, $V (x) = V_{0}$, so

$$
\begin{align}
\frac{\hbar^{2}}{2m}\dv[2]{\psi}{x} + V_{0}\psi (x) & = -E \psi (x)\\[1em]
\dv[2]{\psi}{x} & = \underbrace{\frac{2m(E + V_{0})}{\hbar}}_{= l^{2}}\psi (x)\\[1em]
\psi (x) & = Fe^{-ilx} + Ge^{ilx}\\[1em]
& = (F + G)\cos (lx)+ i (G-F)\sin (lx)\\[1em]
& = C \cos (lx) + D \sin (lx).
\end{align}
$$

This is just about it. To finish off this problem, we shall use a tool known as *parity*. Parity is essentially a map $x \mapsto-x$, and different solutions with have different parities. Notice, for example, that the Hamiltonian can be rewritten as

$$
\hat{H} (\hat{x}, \hat{p}) = \hat{H}(-\hat{x},-\hat{p}).
$$

And we can propose a perfectly valid solution this way. Let us do so now: 

$$
\begin{align}
\hat{H}(\hat{x}, \hat{p})\psi_{n} (x) & = E_{n}\psi_{n}(x)\\[1em]
x & \mapsto-x\\[1em]
\hat{H}(-\hat{x}, -\hat{p})\psi_{n} (-x) & = E_{n}\psi_{n}(-x).
\end{align}
$$

We can now operate on $\psi_{n}(-x)$:

$$
\begin{align}
\hat{H}(\hat{x}, \hat{p})\psi_{n}(-x) & = E_{n}\psi_{n}(-x)\\
\psi_{n}(-x) & = C_{p}\psi_{n}(x)\\
\psi_{n}(x) & = C_{p}^{2}\psi_{n}(x)\\
& \therefore \\
C_{p} & = \pm1.
\end{align}
$$

As such, if $\psi_{n}(-x)=-\psi_{n}(x)$, then we have an odd state, and if $\psi_{n}(-x)= \psi_{n}(x)$, then we have an even state.