# WKB Approximation

If you start with the Schrödinger equation (mostly in 1-D),

$$
\begin{align}
\frac{-\hbar^{2}}{2 m_{0}}\dv[2]{\psi}{x} + V (x)\psi (x) = E \psi (x) \\[1 em]
\dv[2]{\psi}{x}= \frac{-p^{2}}{\hbar^{2}}\psi (x),
\end{align}
$$

where $p (x)= \sqrt{2 m_{0}(E-V (x))}$.

When $E > V (x)$, we call that the "classical" region, whereas for $E < V (x)$ is called the "forbidden" or non-classical region. We can then express $\psi (x)$ as

$$
\begin{align}
\psi (x) & = A (x)e^{i \phi (x)} \\[1 em]
\dv{\psi}{x}& = (A' + iA \phi')e^{i \phi},
\end{align}
$$

where $A$ and $\phi$ are both real. From here,

$$
\begin{align}
\dv[2]{\psi}{x}& =[A'' + iA' \phi' + iA \phi'' + i \phi' A'-A (\phi')^{2}]e^{i \phi} \\[1 em]
\left[A'' + 2 iA' \phi's + iA \phi''-A (\phi')^{2}+ \frac{p^{2}}{\hbar^{2}}\right] & = 0.
\end{align}
$$

Since the imaginary part must equal $0$, we must have $(A^{2}\phi')' = 0$. The real part is then

$$
\begin{align}
A''-A (\phi')^{2}+ \frac{p^{2}}{\hbar^{2}}A & = 0 \\[1 em]
A'' & \approx 0 \\[1 em]
(\phi')^{2} & = \frac{p^{2}}{\hbar^{2}} \\[1 em]
\phi (x) & = \pm \frac{1}{\hbar}\int_{x_{0}}^{x}p (x')\dd{x'}\\[1 em]
\psi_{\text{WKB}}(x) & = \frac{\text{constant}}{\sqrt{\dv{\phi}{x}}}\exp{\left(\pm \frac{i}{\hbar}\int_{x_{0}}^{x}p (x')\dd{x'} \right)}.
\end{align}
$$

A potential with 2 vertical walls then looks like

$$
\begin{align}
\psi_{\text{WKB}} & = \frac{c_{1}}{\sqrt{\dv{\phi}{x}}}\exp \left(-\frac{i}{\hbar}\int... \right) + \frac{c_{2}}{\sqrt{...}}\exp \left(+ \frac{i}{\hbar}\int... \right) \\[1 em]
& = \frac{1}{\sqrt{\dv{\phi}{x}}}[c_{1}\cos (\phi (x)) + c_{2}\sin(\phi (x))] \\[1 em]
\phi (x) & = \int_{0}^{x}\frac{1}{\hbar}p (x')\dd{x'} \\[1 em]
\psi_{W}(x = 0) & = 0 \implies c_{1}= 0 \\[1 em]
\psi_{W}(x  =0) & = 0 \implies \phi (a) = n \pi \qc n \in \mathbb{N}.
\end{align}
$$

From here

$$
\begin{align}
\int_{0}^{a}\sqrt{2 m (E-V (x))}\dd{x} & = n \pi \hbar \\[1 em]
E & = V_{0}+ \frac{n^{2}\pi^{2}\hbar^{2}}{2 ma},
\end{align}
$$

which is exactly what we would expect. That is the classical region. For the forbidden region, we have

$$
\begin{align}
\psi_{W} & = \frac{c}{\sqrt{\abs{p (x)}}}\exp \left[\pm \frac{1}{\hbar}\int_{x_{0}}^{x}p (x')\dd{x'} \right] \\[1 em]
\psi_{W}(x = a) & = \frac{c_{1}}{\sqrt{\abs{p (x)}}} \exp \left[-\frac{1}{\hbar}\int_{0}^{a}\abs{p (x')}\dd{x'} \right].
\end{align}
$$

Here, we are interested in the transmission through a barrier, and so

$$
\begin{align}
T \sim \abs{\frac{F}{A}}^{2} \sim \exp(-2 \gamma), \\[1 em]
\gamma \equiv \frac{1}{\hbar}\int_{0}^{a}\abs{p (x')}\dd{x'}.
\end{align}
$$

In 1928, this led to the Gamow theory of alpha decay.