# Fermi Gas

The idea of the Fermi gas is to look at a large number $N_{f}$ of non-interacting fermions inside a box of size $a$. The idea seems restrictive, but it can be applied to things such as electrons in a solid. Even though there are huge electrostatic interactions between electrons inside a solid, if said solid is electrically neutral, then these interactions must average out to zero, at least for the electrons on the outer orbits. These outer electrons are loosely bound to their nuclei and are free to move around through the solid almost freely. At the same time, these electrons can't easily leave the solid without a lot of external energy. Clearly the Fermi gas is a reasonable approximation.

Thanks again to the electrons being bounded to the solid, we can model the solid as an infinite square well of size $a^{3}$. We then get the standard wavefunction solution for each electron, with total energy

$$
E_{n_{x}, n_{y}, n_{z}} = \frac{\hbar^{2}\pi^{2}}{2 mo^{2}}(n_{x}^{2}+ n_{y}^{2}+ n_{z}^{2}) = \frac{\hbar^{2}\bar{k}^{2}}{2 m}.
$$

We do not concern ourselves with the wavefunction for this chapter, and so we focus only on the energy of the ground state *as a function of the number of electrons*.

To obtain this, we start by invoking the Pauli exclusion principle: Only two electrons are allowed in any one state $(n_{x}, n_{y}, n_{z})$ (in the case of the electrons, we have seen that this state is the [[Chapter 2|$\ket{ 0 \; 0}$ state]]).

We can now represent $\bar{k}$ as a point in the momentum space, with discrete positive coordinates. These points form a cubic lattice that has cells of size $\pi/a$. The energy off each cell depends only on $\abs{\bar{k}}$. The minimal energy configuration is then the one where we minimize the distance of every electron to the origin in the momentum space.

Notice that when $N_{e}$ is large enough, the lattice gives the shape of $1/8$ of a sphere, called an *octant*. The volume of this octant is then also equal to $N_{e}/2$ cells of volume $\pi^{3}/a^{3}$ (factor of 1/2 because there are two electrons per cube), which then gives the following:

$$
k_{F} = \left(3 \pi^{2}\frac{N_{e}}{a^{3}} \right)^{\frac{1}{3}} = (3 \pi^{2}\rho_{e})^{\frac{1}{3}}.
$$

$k_{F}$ is known as the "Fermi momentum" with corresponding energy

$$
E_{F} = \frac{\hbar^{2}k_{F}^{2}}{2 m} = \frac{\hbar^{2}}{2 m}(3  \rho_{e}\pi^{2})^{2/3}
$$

The above is predictably called the "Fermi energy" and it plays a big role in theoretical physics.

![[Pasted image 20251019140607.png]]

The total energy is then

$$
E_{\text{ total}} = \frac{\hbar^{2}}{10 \pi^{2}m}\frac{(3 \pi^{2}N_{e})^{5/3}}{V^{2/3}}.
$$

We can see that the energy decreases with increasing volume. This means the electron gas exerts pressure. Using thermodynamics, we get that

$$
\begin{align}
 P & = -\dv{E_{\text{ total}}}{V} \\[1 em]
& = \frac{2}{3}\frac{E_{\text{ total}}}{V} \\[1 em]
P & = \frac{\hbar^{2}(3 \pi^{2})^{2/3}}{5 m}\rho^{5/3}_{e}.
\end{align}
$$

This is known as *degeneracy pressure*, and it originates from the kinetic energy of the electrons that cannot go to the lower energy states due to Pauli exclusion. The electrons can have energy as high as $E_{F}$

![[Pasted image 20251019142057.png]]

White dwarfs occur due to this degeneracy pressure balancing out the gravitational energy trying to collapse the gas.