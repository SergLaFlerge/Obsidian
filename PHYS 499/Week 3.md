# Review of the First Paper

## Classical Schwarzschild Interior

![[PHYS499-Paper-1.pdf#page=5&rect=129,575,531,636|PHYS499-Paper-1, p.4]]

This is the classical metric for the interior of a static spherically symmetric black hole, in Ashtekar-Barbero (AB) variables. The tildes represent interior coordinates, and $\tilde{T}$ is a time-like coordinate this is associated with the lapse function $\tilde{N}$. This gives the following Hamiltonian:

![[PHYS499-Paper-1.pdf#page=5&rect=155,122,531,180|PHYS499-Paper-1, p.4]]

With the appropriate choice of lapse function, we can decouple $\tilde{b}$ and $\tilde{p}_{b}$ from $\tilde{c}$ and $\tilde{p}_{c}$. Reducing the Hamiltonian to

![[PHYS499-Paper-1.pdf#page=6&rect=215,557,536,600|PHYS499-Paper-1, p.5]]

This yields

![[Pasted image 20250918194210.png]]

We fix the integration constants by comparing the spatial components of the metric with the Schwarzschild interior metric. Eventually, the classical solutions in the Schwarzschild interior coordinates become

![[Pasted image 20250918195044.png]]

Where $R_{s}= 2GM$ is the Schwarzschild radius. Here, the Kretschmann scalar becomes

$$
K_{\text{class}} = \frac{12 (\tilde{b}^{2}+ \gamma^{2})^{2}}{\gamma^{4}\tilde{p}_{c}^{2}}.
$$

The classical singularity resides at $\tilde{p}_{c}= 0$, for which we clearly see $K_{\text{ class}}$ diverges.

## Non-improved Effective Metric

We modify the Poisson algebra according to "the GUP approach" using a quadratic modification:

![[Pasted image 20250918200138.png]]

We note that this modification is not dependent on the coordinate momenta of the variables. Using now the GUP

![[Pasted image 20250918200847.png]]

With a modified algebra

![[Pasted image 20250918200816.png]]

Leads to the uncertainty relation

![[Pasted image 20250918200931.png]]

This implies the existence of a minimal uncertainty in $q$ and $p$, *given that $\alpha> 0$ and $\beta > 0$*, but this has several issues, such as the Chandrasekhar limit no longer existing, allowing arbitrarily large white dwarfs to exist. In fact several approaches lead one to seemingly need to enforce negative deformations in $\alpha$ and $\beta$.

One can essentially trade the existence of a minimal uncertainty with a solution to the above issues by letting the above parameters deform negatively. 

> ([[PHYS499-Paper-1.pdf#page=8&selection=106,0,108,78&color=note|PHYS499-Paper-1, p.7]])
> The negativity of deformation parameters hints that the physical space-time has actually a lattice or granular structure at the Planck scale, essentially a crystal-like universe whose lattice spacing is of the order of Planck length

Is this important for us?

3.1 and 3.2 do not modify the Hamiltonian, but still lead to effective (?) equations of motion that are different from the classical ones, due to modification to the Poisson algebra. The solutions to the modified equations of motion are

![[Pasted image 20250918202028.png]]

in which the constants of integration have been fixed by matching the classical limit of the solutions when $\beta_{b}\to 0$ and $\beta_{c} \to 0$.