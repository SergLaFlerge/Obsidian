# Pre-class Remarks

## Noether's Theorem

While some Lagrangians are known from basic physics, most are not. If we are to construct a Lagrangian that describes a new system, it is often a good idea to rely on symmetries of the system. A system has symmetry if there is a transformation that leaves the system invariant. It so happens that every symmetry of a system is in fact a conserved quantity. Therefore, to find symmetries, we can simply look at what quantities of a system are being conserved and work backwards to find its symmetries. This then lets us make and educated guess at a convenient Lagrangian.

>[!Proof]+ Noether's Theorem
> Every conserved quantity has an associated global symmetry.

As an example, consider an infinitesimal transformation of the coordinate system

$$
x^{\mu} \to x'^{\mu} = x^{\mu} + \delta x^{\mu}.
$$

^5193cc

The fields then transform as

$$
\Phi^{A}(x) \to \Phi'^{A}(x) = \Phi^{A} + \delta \Phi^{A}(x).
$$

^930f07

For the coordinate change $\Omega \to  \Omega'$, the change in the action is given by

$$
\begin{align}
\delta s & = \int_{\Omega'}\mathcal{L}(\Phi'^{A}(x'), \partial'_{\mu}\Phi'^{A}(x'))\dd[4]{x'} - \int_{\Omega}\mathcal{L}(\Phi^{A}(x), \partial_{\mu}\Phi^{A}(x))\dd[4]{x}.
\end{align}
$$

If this $\delta s = 0$, we say that the theory is invariant under the given transformation. $x'$ is a dummy variable in the first integral, so we replace it by $x$ and write

$$
\begin{align}
\delta s & = \int_{\Omega'}\mathcal{L}(\Phi'^{A}(x), \partial'_{\mu}\Phi'^{A}(x)) \dd[4]{x} - \int_{\Omega}\mathcal{L}(\Phi^{A}(x), \partial_{\mu}\Phi^{A}(x))\dd[4]{x} \\[1 em]
 & = \int_{\Omega}\mathcal{L}(\Phi^{A}(x), \partial_{\mu}' \Phi'^{A}(x)) - \mathcal{L}(\Phi^{A}(x), \partial_{\mu}\Phi^{A}(x)) \dd[4]{x} \\[1 em]
& + \int_{\Omega'-\Omega}\mathcal{L} (\Phi'^{A}(x), \partial'_{\mu}\Phi'^{A}(x))\dd[4]{x}.
\end{align}
$$

^5dcbf2

The last integral is an integral over an infinitesimal volume $(\Omega'-\Omega)$, and so we can replace it by another integral, over the boundary $\partial \Omega$:

$$
\begin{align}
\int_{\Omega'-\Omega}\mathcal{L}(\Phi'^{A}, \partial'_{\mu}\Phi'^{A})\dd[4]{x} & = \int_{\partial \Omega}\delta x^{\lambda}\mathcal{L}(\Phi^{A}, \partial_{\mu}\Phi^{A})\dd{S_{\lambda}} \\[1 em]
& = \int_{\Omega}\partial_{\lambda}(\delta x^{\lambda}\mathcal{L}(\Phi^{A}, \partial_{\mu}\Phi^{A}))\dd[4]{x}.
\end{align}
$$

We can suppress the space-time index $x$ since we no longer need to distinguish between coordinates. We can replace $\Phi'$ by $\Phi$ because their difference is of higher order in $\delta x^{\mu}$.

We should now define the variation for fixed $x$. For any function $f (x)$ whose functional form changes to $f' (x)$, we can write

$$
\begin{align}
\bar{\delta}f (x) & \equiv f' (x)-f (x) \\[1 em]
& = [f' (x')-f (x)] - [f' (x')-f' (x)] \\[1 em]
& = \delta f (x) - \partial_{\mu}f (x)\delta x^{\mu},
\end{align}
$$

^4519dc

where we have again ignored high order $\delta x^{\mu}$ terms.

This allows us to simplify the Lagrangian from [[#^5dcbf2|above]]:

$$
\begin{align}
\mathcal{L}(\Phi'^{A}(x), \partial_{\mu}' \Phi'^{A}(x)) & -\mathcal{L}(\Phi^{A}(x), \partial_{\mu}\Phi^{A}(x)) \\[1 em]
& = \pdv{\mathcal{L}}{\Phi^{A}}\bar{\delta}\Phi^{A} + \pdv{\mathcal{L}}{(\partial_{\mu}\Phi^{A})}\bar{\delta}(\partial_{\mu}\Phi^{A}) \\[1 em]
& = \partial_{\mu}\left(\pdv{\mathcal{L}}{(\partial_{\mu}\Phi^{A})}\bar{\delta}\Phi^{A} \right),
\end{align}
$$

where we used the EL equation to get the last equality. Then,

$$
\begin{align}
\delta s & = \int_{\Omega}\partial_{\mu}\left[\pdv{\mathcal{L}}{(\partial_{\mu}\Phi^{A})}\bar{\delta}\Phi^{A} + \mathcal{L}\delta x^{\mu} \right]\dd[4]{x} \\[1 em]
& = \int_{\Omega}\partial_{\mu}\left[\pdv{\mathcal{L}}{(\partial_{\mu})\Phi^{A}}\delta \Phi^{A} - T^{\mu \nu}\delta x_{\nu} \right]\dd[4]{x},
\end{align}
$$

where we used [[#^4519dc|this relation]] to bring back $\delta \Phi^{A}$, and

$$
T^{\mu \nu} = \pdv{\mathcal{L}}{(\partial_{\mu}\Phi^{A})}\partial^{\nu}\Phi^{A} - g^{\mu \nu}\mathcal{L}.
$$

$T^{\mu \nu}$ is called the *stress-energy tensor*. We can now define a current

$$
J^{\mu} = \pdv{\mathcal{L}}{(\partial_{\mu}\Phi^{A})}\delta \Phi^{A} - T^{\mu \nu}\delta x_{\nu},
$$

^7f303e

such that

$$
\delta s = \int_{\Omega}\partial_{\mu}J^{\mu}\dd[4]{x}.
$$

This relation holds for arbitrary variations of the fields and coordinates, so long as the equation of motion are satisfied. If there is a symmetry, $\delta s$ will vanish for arbitrary $\Omega$, even without the use of the equation of motion. Then, we obtain a conservation law when the equations of motion are satisfied. This is Noether's theorem restated mathematically:

>[! Proof]+ Noether's Theorem
>$$\partial_{\mu}J^{\mu}= 0$$
>when the equations of motion are satisfied.

^727c00

$J$ in this case is known as a *Noether current*. It is worth noting that $J^{\mu}$ is defined only up to a constant factor. It may be that, under the [[#^5193cc|original]] [[#^930f07|transformations]], the action instead varies by the integral of a total divergence

$$
\delta s = \int_{\Omega}\partial_{\mu}Y^{\mu}\dd[4]{x},
$$

in which case the expression for the conserved current is the same as [[#^7f303e|before]], with the added $Y^{\mu}$.

Of course, the equation $\partial_{\mu}J^{\mu}= 0$ implies the conservation of a charge, called a *Noether charge*. This Noether charge is defined as an integral over all space

$$
Q \equiv \int J^{0}\dd[3]{x},
$$

as long as the current vanishes fast enough at spatial $\infty$. This works because

$$
\dv{Q}{t} = \int \partial_{0}J^{0}\dd[3]{x} = -\int \nabla \cdot \mathbf{J}\dd[3]{x},
$$

and this second integral can be converted into a surface integral on the spatial surface at infinity, where we have established that it should vanish. Therefore,

$$
\dv{Q}{t} = 0,
$$

and so the Noether charge is conserved. 

# In-class Notes

There are two types of transformations: Continuous and discrete. Something like a reflection is a discrete transformation. A rotation is a continuous transformation.

 $\bar{\delta}$ and $\partial_{\mu}$ commute.