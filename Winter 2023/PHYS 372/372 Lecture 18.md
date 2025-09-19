# Heisenberg Representation and Dirac Quantization

## Heisenberg Representation

1. Originally this was it first formulation of quantum mechanics.
2. This formulation has a more understandable connection to classical mechanics.
3. It is the basis of Dirac — or "canonical" — quantization.
4. Most importantly, it is used in quantum field theory.

Last time we discussed the evolution of a quantum state:

$$
\ket{\psi_{t}} = \hat{U}(t)\ket{\psi_{0}}\qc \hat{U}(t) = \exp \left(-i \frac{\hat{H}}{\hbar}t \right).
$$

The time evolution of an expectation value of an operator $\hat{Q}$ is then

$$
\begin{align}
\ev{Q}(t) & = \ev{\hat{Q}}{\psi_{t}} \\[1em]
& = \int_{-\infty}^{\infty}\Psi^{*}(x, t)\hat{Q}({\hat{p}, \hat{x}})\Psi (x, t)\dd{x} \\[1em]
& = \bar{C}^{\dagger}(t)\hat{Q}\bar{C}(t)\rightarrow \text{(matrix product)}.
\end{align}
$$

We can write this expectation value as follows:

$$
\begin{align}
\ev{Q} & = \ev{\hat{U}^{\dagger}(t)\hat{Q}\hat{U}(t)}{\psi_{0}}, \\[1em]
\bra{\psi_{0}}\hat{U}^{\dagger} & = \bra{\psi_{t}} \hat{U}\ket{\psi_{0}} = \ket{\psi_{t}}.
\end{align}
$$

We can treat the three terms inside as one operator, i.e. $\hat{Q}(t)= \hat{U}^{\dagger}(t)\hat{Q}\hat{U}(t)$. This is known as Heisenberg's representation.

(Make table later?)

In the Schrödinger representation, the quantum state $\ket{\psi_{t}}$ depends on time. Whereas in the Heisenberg representation $\ket{\psi_{0}}$ is time independent. The trade-off is then that the operator of the physical observable $\hat{Q}(\hat{p}, \hat{x})$ is time independent in Schrödinger's representation, while in the Heisenberg representation $\hat{Q}(t)$ is time dependent. However it is true to say that

$$
\ev{\hat{Q}}{\psi_{t}} = \ev{\hat{Q}(t)}{\psi_{0}}.
$$

That's great and all, but what is this all for? In the Schrödinger representation, the time evolution of $\ket{\psi_{t}}$ is governed by the Schrödinger equation

$$
i \hbar \pdv{t}\ket{\psi_{t}} = \hat{H}\ket{\psi_{t}}.
$$

The natural question is then, what is the equation for $\hat{Q}(t)$? It's actually very simple. Recall that

$$
\hat{Q}(t)=  \underbrace{\exp\left(i \frac{\hat{H}}{\hbar}t \right)}_{\hat{U}^{\dagger}}\hat{Q}\underbrace{\exp \left(-i \frac{\hat{H}}{\hbar}t \right)}_{\hat{U}}.
$$

Then,

$$
\begin{align}
i \hbar \pdv{t}\hat{Q}(t) & = -\hat{H}\exp \left(i \frac{\hat{H}}{\hbar}t \right)\hat{Q}\exp \left(-i \frac{\hat{H}}{\hbar}t \right) + \exp \left(i \frac{\hat{H}}{\hbar}t \right)\hat{Q}\exp \left(-i \frac{\hat{H}}{\hbar}t \right) \\[1em]
& =-\hat{H}\hat{Q}(t) + \hat{Q}(t)\hat{H} \\[1 em]
& =\comm{\hat{Q}(t)}{\hat{H}}.
\end{align}
$$

So we have

$$
i \hbar \pdv{t}\hat{Q}(t) = \comm{\hat{Q}}{\hat{H}}.
$$

This is the basic equation in the Heisenberg representation. Historically, this was the first equation of quantum mechanics. If $\hat{Q}$ commutes with the Hamiltonian, the corresponding physical observable does not depend on time for *any* quantum state.

## Dirac Quantization

Recall that the Hamilton representation of classical mechanics (in one dimension) is given by

$$
\begin{align}
&\begin{cases}
\dot{x} & = \pdv{H}{p} \\
\dot{p} & = -\pdv{H}{x}
\end{cases} \\[1em]
H (x, p) & = \frac{p^{2}}{2m}+ V (x).
\end{align}
$$

If we know look at $\dv{Q}{t}= \pdv{Q}{x}\cdot \dot{x}+ \pdv{Q}{p}\cdot \dot{p} = \pdv{Q}{x}\pdv{H}{p}-\pdv{Q}{p}\pdv{H}{t}= \Bqty{Q, H}$. This is known as a *Poisson bracket*. We can then compare the two expressions:

$$
\begin{align}
i \hbar \pdv{t}\hat{Q}(t) & = \comm{\hat{Q}}{\hat{H}} \\[1em]
i \hbar \dv{Q}{t} & = i \hbar \Bqty{Q, H}.
\end{align}
$$

So to "quantize" a theory, you simply replace the Poisson bracket $\{Q_{1}, Q_{2}\}$ with $\frac{1}{i \hbar}\comm{\hat{Q}_{1}}{\hat{Q}_{2}}$. This procedure is known as *Dirac quantization*.