The general solution to the wave packet would be

$$
\Psi (x, t) = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\phi (k)\exp \left(\frac{-i \hbar k^{2}t}{2m} \right)\cdot e^{ikx}\dd{k}.
$$

$\phi (k)$ is related to the probability of finding the particle with some momentum $p = \hbar k$. This is great, but we have no idea what $\phi (k)$ actually is. We are going to propose a Gaussian type of envelope and start at $t = 0$ for simplicity:

$$
\Psi (x, 0) = N \exp \left(\frac{-x^{2}}{4 \Delta^{2}} \right).
$$

This is a Gaussian function at $t = 0$. Applying the normalization condition,

$$
\begin{align}
N & = \frac{1}{\sqrt{\Delta \sqrt{2 \pi}}}\\
\sigma_{x} & = \Delta.
\end{align}
$$

The Fourier transform of $\Psi (x, 0)$ is

$$
\begin{align}
\phi (k) & = \frac{N}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\exp \left(\frac{-x^{2}}{4 \Delta^{2}} \right)\cdot e^{-ikx}\dd{x}\\
& = \sqrt{\frac{2 \Delta}{\sqrt{2 \pi}}}e^{-k^{2}\Delta{2}}\\[1em]
\sigma_{x}\sigma_{k} & = \frac{1}{2}\\
& \Downarrow \\
\sigma_{x}\sigma_{p} & = \frac{\hbar}{2}.
\end{align}
$$

We can now evolve the solution in time:

$$
\begin{align}
\Psi (x, t) & = \frac{1}{\sqrt{2 \pi}}\sqrt{\frac{2 \Delta}{\sqrt{2 \pi}}} \int_{-\infty}^{\infty}\exp \left[-\left(\Delta +\frac{ i \hbar^{2}t}{2m} \right)k^{2}+ ikx \right]\dd{k}\\[1em]
& = \frac{1}{\sqrt{2 \pi}}\sqrt{\frac{2 \Delta}{\sqrt{2 \pi}}}\sqrt{\frac{\pi}{\Delta^{2}+ \frac{i \hbar t}{2m}}}\exp \left(\frac{-x^{2}}{4 \left(\Delta^{2} +\frac{i \hbar t}{2m} \right)} \right).
\end{align}
$$

We can make more sense of this by rewriting this expression with a real and an imaginary part.

$$
\Psi (x, t) = N (t)\exp \left(\frac{-x^{2}}{4 \Delta^{2}(t)} \right)e^{i \varphi (x, t)},
$$

where

$$
\begin{align}
\Delta (t) & = \Delta \left(1 + \frac{\hbar^{2}t^{2}}{4m^{2}\Delta^{4}} \right)^{1/2}\\
N (t) & = \frac{1}{\sqrt{\Delta (t)\sqrt{2 \pi}}}.
\end{align}
$$

The specifics of the imaginary part are not relevant here because we only have one particle, but it will come up later in the course. Anyways,

$$
\Psi^{*}\Psi \sim \exp \left(\frac{-2x^{2}}{4 \Delta^{2}(t)} \right),
$$

so as time increases, the amplitude of this "envelope" decreases, and the spread increases. As time evolves, the particle becomes de-localized. So *how* do we make this envelope move? We add a second term:

$$
\Psi (x, 0) = N \exp \left(\frac{-x^{2}}{4 \Delta^{2}} \right)e^{ik_{0}x}.
$$

This second term will represent our momentum. In this case,

$$
\begin{align}
\phi (k) & = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\exp \left(\frac{-x^{2}}{4 \Delta{2}} \right)\cdot e^{ik_{0}x}\dd{x}\\
& = \sqrt{\frac{2 \Delta}{\sqrt{2 \pi}}}e^{- (k-k_{0})\Delta{2}},
\end{align}
$$

and then our general solution looks like

$$
\begin{align}
\Psi (x, t) & = \frac{1}{\sqrt{2 \pi}}\int_{-\infty}^{\infty}\phi (k)e^{-i
\omega (k)t + ikx}\dd{k} \\[1em]
\omega (k) & =\frac{\hbar k^{2}}{2m}.
\end{align}
$$

We really only care about the contribution at $k = k_{0}$, so Taylor expanding, we get

$$
\omega (k) \approx \omega (k_{0}) + \eval{\dv{\omega}{k}}_{k_{0}}(k-k_{0}) + \order{k^{2}}
$$

so that

$$
\begin{align}
e^{i (kx-\omega (k)t)}  & \approx e^{i (k_{0}x-\omega (k_{0})t)} \cdot \exp \left(i (k-k_{0})\left(x-\eval{\dv{\omega}{k}}_{k_{0}}t \right) \right)\\
& = e^{i (k_{0}x-\omega (k_{0})t)} \cdot \exp \left(i (k-k_{0})\left(x-vt \right)\right),
\end{align}
$$

where $v= v_{g}$ is our group velocity, given by

$$
v_{g} = \eval{\dv{\omega}{k}}_{k_{0}}
$$