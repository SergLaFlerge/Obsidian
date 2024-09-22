# Physics With the New Formalism

- An observable $Q$ can have a certain value $q_{n}$ at some time $t_{0}$ only if $\Psi (x, t)$ is an eigenfunction of $\hat{Q}$. Originally, we said that $\hat{Q}\Psi (x, t)= q_{n}\Psi (x, t)$, and at time $t_{0}$, we would have $\Psi (x, t)= \psi_{n}^{Q}(x)$. What we then have is

$$
\begin{align}
\sigma_{Q}^{2} & = \ev{\hat{Q}^{2}}{\psi_{t}} - (\ev{\hat{Q}}{\psi_{t}})^{2} \\[1em]
& = \ev{(Q-\hat{Q})^{2}}{\psi_{t}},
\end{align}
$$

by linearity. Now, using $\hat{Q}^{\dagger}= \hat{Q}$, we can also write

$$
\begin{align}
\ip{\psi_{t}(\hat{Q}-\ev{Q})}{(\hat{Q}-\ev{Q})\psi_{t}} =  \ip{\alpha}
\end{align}
$$

which is zero if and only if $\ket{\alpha}= \ket{0}$, for $\ket{\alpha}= (\hat{Q}-\ev{Q})\ket{\psi_{t}}$. This then gives the result

$$
\hat{Q}\ket{\psi_{t}} =  \ev{Q}\ket{\psi_{t}}
$$

which is really just implying that $\hat{Q}= \ev{Q}$ if $\sigma_{Q}^{2}= 0$ and everything is consistent in the world.

- Assume we now have two observables $Q_{1}$ and $Q_{2}$, which have certain values simultaneously. That is, $\sigma_{Q_{1}}^{2}= \sigma_{Q_{2}}^{2}= 0$. This is only true if $\hat{Q}_{1}$ and $\hat{Q}_{2}$ have a common set of you eigenfunctions $\psi_{n}^{Q}(x)$.

$$
\hat{Q}_{1, 2}\psi_{n}^{Q}(x) = q_{1, 2}\psi_{n}(x)\implies \comm{Q_{1}}{Q_{2}}= 0.
$$

$Q_{1}$ and $Q_{2}$ can can then be represented by (diagonal) matrices.

$$
\begin{bmatrix}
q_{1} & 0 & 0 & \cdots \\
0 & q_{2} & 0 & 0 \\
0 & 0 & q_{3} & 0 \\
\vdots & 0 & 0 & \ddots
\end{bmatrix}.
$$

- Say $\comm{\hat{Q}_{1}}{\hat{Q}_{2}}\neq 0$. Now what? Our job now will be to find the relationship between $\sigma_{Q_{1}}$ and $\sigma_{Q_{2}}$. Recall from earlier that

$$
\sigma_{Q_{1}}^{2} = \ip{\alpha}\qc \ket{\alpha} = \ket{(\hat{Q}_{1}-\ev{Q})\psi_{t}}
$$

and

$$
\ev{Q_{1}} = \ev{\hat{Q}_{1}}{\psi_{t}}.
$$

We can do similarly for $\sigma_{Q_{2}}$:

$$
\begin{align} \\
\sigma_{Q_{2}}^{2} & = \ip{\beta} \\[1em]
\ket{\beta} & = \ket{(\hat{Q_{2}}-\ev{Q_{2}})\psi_{t}}. 
\end{align}
$$

Let us look at $\abs{\ip{\alpha}{\beta}}^{2}$. We know that $\ip{\alpha}{\beta}= z \qc z \in \mathbb{C}$. Then $\abs{z}^{2}= (\real(z))^{2}+ (\imaginary (z))^{2}\geq (\imaginary (z))^{2}$. Using $z$ and $z^{*}$, we can write

$$
\begin{align}
\imaginary (z) & = \frac{z-z^{*}}{2i} \\[1em]
& = \frac{1}{2i}(\ip{\alpha}{\beta}-\ip{\beta}{\alpha}) \\[1em]
& = \frac{1}{2i}\left(\ev{(\hat{Q_{1}}-\ev{Q}_{1})(\hat{Q}_{2}-\ev{Q_{2}})}{\psi_{t}}- \ev{(\hat{Q_{2}}-\ev{Q}_{2})(\hat{Q}_{1}-\ev{Q_{1}})}{\psi_{t}}\right) \\[1em]
& = \frac{1}{2i}\left(\ev{\hat{Q}_{1}\hat{Q}_{2}}{\psi_{t}} - \ev{\hat{Q}_{2}\hat{Q}_{1}}{\psi_{t}} \right) \\[1em]
\imaginary (z) & = \frac{1}{2i}\left(\ev{\comm{\hat{Q}_{1}}{\hat{Q}_{2}}} \right)
\end{align}.
$$

This then implies

$$
\abs{\ip{\alpha}{\beta}}^{2} \geq \left(\frac{1}{2i}\ev{\comm{\hat{Q}_{1}}{\hat{Q}_{2}}} \right).
$$

We can now use the Cauchy-Schwarz inequality:

$$
\begin{align}
\abs{\ip{\alpha}{\beta}}^{2} & \leq \norm{\alpha}^{2}\norm{\beta}^{2} \\[1em]
\sigma_{Q_{1}}\sigma_{Q_{2}} & \geq \frac{1}{2i}\left(\ev{\comm{\hat{Q}_{1}}{\hat{Q}_{2}}} \right).
\end{align}
$$

This is the *generalized uncertainty principle*. Let us take $\hat{Q}_{1}= \hat{x}$ and $\hat{Q}_{2}= \hat{p}$. Then

$$
\begin{align}
\comm{\hat{x}}{\hat{p}} & = \ev{i \hbar}{\psi_{t}} \\[1em]
& = i \hbar \underbrace{\ip{\psi_{t}}}_{= 1} \\[1em]
\sigma_{x}\sigma_{p} & \geq \frac{1}{2i}\cdot i \hbar \\[1em]
\sigma_{x}\sigma_{p} & \geq \frac{\hbar}{2}
\end{align}
$$

Fucking amazing. Fucking beautiful. We can do the same with $E$ and $t$, and we'll actually obtain the same result, but what does it *mean* for us to have an uncertainty in time? Here, $\sigma_{t}$ is associated with characteristic time.