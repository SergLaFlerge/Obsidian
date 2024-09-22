When we are inside the well, and $E > 0$,

$$
\begin{align}
\psi_{n}(x) & = D \cos (lx) + C \sin (lx), \\
l & = \sqrt{\frac{2m (E-V_{0})}{\hbar^{2}}}.
\end{align}
$$

We then started talking about the concept of parity: odd and even states. The even function is the easier one to approach, since we only need to solve for $x > 0$. Therefore, for the even case we have

$$
\psi(x) = 
\begin{cases}
D \cos (lx) \qq{for} &x < a \\
Ae^{-kx} \qq{for} &x > a
\end{cases},
$$

and since $\psi (x)$ must be continuous,

$$
\begin{align}
\psi (a) & = D \cos (la)= Ae^{-kx} \quad &(1)\\[1em]
\eval{\dv{\psi}{x}}_{x = a} & = -Dl \sin (la) = -Ake^{kx} \quad &(2)\\[2em]
\frac{(1)}{(2)} & = l \tan (la) = k \\[1em]
\tan (la) & = \frac{k}{l}\\[1em]
\tan \left(\frac{a \sqrt{2m (E + V_{0})}}{\hbar} \right) & = \sqrt{\frac{-E}{E + V_{0}}}.
\end{align}
$$

There are no further  simplifications that are possible, and so solving for $E$ analytically is impossible.

As expected, we do have a discreet spectrum that appears. However, unlike the infinite square well, we have a finite number of states. While the answer above is not particularly illuminating, we can study some limiting cases:

## Deep Well Limit

$\abs{V_{0}}\rightarrow \infty$. In this limit, we can analyze the lower energy levels $\abs{E_{n}}\approx \abs{V_{0}}$, and $\abs{V_{0}}+ E_{n}< \infty$. Hence,

$$
\begin{align}
\left(\frac{E}{E + V_{0}} \right)^{1/2} & \rightarrow \infty \\[1em]
\tan \left(\frac{a \sqrt{2m (E + V_{0})}}{\hbar} \right) & = \infty \\[1em]
\frac{a \sqrt{2m (E + V_{0})}}{\hbar} & = \frac{(2n + 1)\pi}{2}\qc n \in \mathbb{N}_{0}\\[1em]
E_{n} & \approx \frac{[\pi (n + \frac{1}{2})]^{2}\hbar{2}}{a^{2}}\cdot \frac{1}{2m}-V_{0}\\[1em]
E_{n} & \approx -V_{0} + \frac{\hbar^{2}\pi^{2}n^{2}}{8a^{2}m} \qq{for $n$ odd.}
\end{align}
$$

This solves the even case. It should be clear that doing the odd case will populate the even energy levels.

## Shallow Well Limit

$\abs{V_{0}}\rightarrow 0$. Here, $E_{n}\rightarrow 0$. We can then Taylor expand $\tan (x)\approx x + \order{x^{2}}$. Then

$$
\begin{align}
\frac{2ma^{2}}{\hbar^{2}}(E + V_{0}) & = \frac{-E_{n}}{E + V_{0}}\\[1em]
E_{n}^{2} + \left(\frac{\hbar^{2}}{2ma^{2}}+ 2V_{0} \right)E_{n} + V_{0} & = 0.
\end{align}
$$

This guarantees the existence of at least one solution, regardless of how shallow the well is. Now, since this is a shallow well, we should consider the scattering case as well, let us take a look:

### Shallow Well Scattering Case

For $E > V_{0}$, we get scattering solutions. The time independent Schrödinger equation looks like

$$
\begin{align}
\dv[2]{\psi}{x} & = -k^{2}\psi (x)\\[1em]
E_{k} & = \frac{\hbar^{2}k^{2}}{2m}.
\end{align}
$$

This is much like the standard free particle problem,

$$
\psi (x)
\begin{cases}
Ae^{ikx} + Be^{-ikx} \qq{for} &x < -a \\
Fe^{ikx} + 0 \qq{for} &x > a
\end{cases}.
$$

We have already eliminated one solution because this is just like the $\delta$ potential. Unlike the $\delta$ potential, however, we need to consider the region $x < \abs{a}$:

$$
\begin{align}
\psi_{l}(x) & = C \sin (lx) + D \cos (lx)\\[1em]
l & = \sqrt{\frac{2m (E + V_{0})}{\hbar^{2}}}.
\end{align}
$$

We apply the usual boundary conditions. At $x = a$,

$$
\begin{align}
\psi_{k}(-a) &  \rightarrow C\sin (la) + D \cos (la) = Fe^{ika}\\
\dv{\psi_{k}}{x} & \rightarrow l [C \cos (la)-D \sin (la)] = ikFe^{ika}\\[1em]
B & = \frac{i \sin (2la)}{2}(l^{2}-k^{2})F \\[1em]
F & = \frac{e^{-2ikaA}}{\cos (2la)-\frac{i (k^{2}-l^{2})}{2kl}\sin{(2la)}}\\[1em]
T & = \frac{\abs{F}^{2}}{\abs{A}^{2}} = 1 + \frac{V_{0}^{2}}{4E_{k}(E_{k}+ V_{0})}\sin^{2}\left(\frac{2a \sqrt{2m (E_{k} + V_0)}}{F} \right),
\end{align}
$$

and for $x =-a$,

$$
\begin{align}
\psi_{k} & \rightarrow Ae^{ika} + Be^{-ika} = -C \sin(la) + D \cos (la)\\
\dv{\psi_{k}}{x} & \rightarrow ik (Ae^{ika}-Be^{-ika}) = l[C \cos (la)-D \sin (la)].
\end{align}
$$