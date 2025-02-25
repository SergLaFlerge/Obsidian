# Pre-class Remarks:

## Action Functional and the Lagrangian

To go to a field theory, we need to keep in find two things: Firstly we still want to describe the system by an action, and we still want this action to be the time integral of the Lagrangian. Secondly, going to a field theory means that now both space and time coordinates are independent, and as such, we must incorporate the information from every point in space into our action.

To do this, we can just write the Lagrangian as a spatial integral of a function of the fields. This has a bonus advantage of putting space and time on equal footing, which is a great start to make our field theory relativistic.

 >[!info]+
 > The integrand has units of Lagrangian *density*, but we often omit the density part. We will use the word Lagrangian to refer to this density, but we will use the letter $\mathcal{L}$, while the actual Lagrangian  (Also called the total Lagrangian) will simply be labeled $L$.
 
 The Lagrangian depends on the fields — denoted $\Phi^{A}$ and representing the generalized coordinates $q_{r}$ — and also depends on the generalized velocities $\dot{q}_{{r}}$. Clearly, we should replace $\dot{q}_{r}$ with the derivatives of the fields, but it can't just be a time derivative since all coordinates are now independent. We can make the (correct) educated guess that $q_{r}\to \partial_{\mu}\Phi^{A}$, where $\partial_{\mu}\Phi^{A}$ are the derivatives of the fields.

Since we are only interested in fundamental fields, we do not expect any source or sink of energy or momentum. Because of this, the Lagrangian should not depend *explicitly* on the space-time coordinates. We can then write

$$
\mathcal{A} = \int_{\Omega}\mathcal{L}\left(\Phi^{A}(x), \partial_{\mu}\Phi^{A}(x) \right) \dd[4]{x}.
$$

Generally, we take $\Omega$ to be the entire space-time.

The action must be Poincaré invariant in a covariant theory. This just means that the action must be invariant under Lorentz transformations and space-time translations. Since the space-time volume $\dd[4]{x}$ is Poincaré invariant by itself, the Lagrangian above must also be invariant.

$\mathcal{L}$ is a function, while $\mathcal{A}$ is a number. Objects that map functions to numbers are called *functionals*. The action is a functional of the fields. 

>[!info]+
>The total Lagrangian $L$ is a *function* of $t$, but it is a *functional* of the fields at a given $t$.

We can derive the classical equations of motion from the principle of least action. If we consider the variations $\Phi^{A}\to \Phi^{A}+ \delta \Phi^{A}$ and  $\partial_{\mu}\Phi^{A}+ \partial_{\mu}\delta \Phi^{A}$ with the condition that $\delta \Phi^{A}$ vanishes on the boundary $\partial \Omega$. Then,

$$
\begin{align}
\delta \mathcal{A} & = \int_{\Omega}\pdv{\mathcal{L}}{\Phi^{A}}\delta \Phi^{A} + \frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\Phi^{A})}\partial_{\mu}\delta \Phi^{A}\dd[4]{x} \\[1 em]
& = \int_{\Omega}\pdv{\mathcal{L}}{\Phi^{A}} -\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\Phi^{A})} \right)\dd[4]{x}\cdot \delta \Phi^{A} \\[1 em]
& \quad + \int_{\Omega}\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\Phi^{A})}\delta \Phi^{A} \right) \dd[4]{x}.
\end{align}
$$

By using Gauss' theorem, we can rewrite the second term above as an integral over $\partial \Omega$. However, since this integral contains $\delta \Phi^{A}$ and $\delta \Phi^{A}= 0$ at the boundary, the second term vanishes.

Since $\delta \mathcal{A}= 0$, the other terms must vanish for arbitrary variations of the fields. This can only occur if

$$
\partial_{\mu}\left(\frac{\partial \mathcal{L}}{\partial (\partial_{\mu}\Phi^{A})} \right) = \pdv{\mathcal{L}}{\Phi^{A}}
$$

## Hamiltonian Formalism

The canonical momenta of $\Phi^{A}$ are defined in analogy to systems with finite number of degrees of freedom:

$$
\Pi_{A} \equiv \frac{\delta L}{\delta \dot{\Phi}^{A}}.
$$

$\dot{\Phi}^{A}$ is the time-derivative of $\Phi^{A}$, as expected. We should remember that this is a *partial* derivative, since $\Phi^{A}$ depends on the spatial coordinates as well. The use of $\delta$ over $\partial$ is justified, since $L$ is a functional. $\Pi_{A}$ is the derivative of a functional with respect to a function.

To compute $\Pi_{A}$, we need to know the derivatives with respect to $\dot{\Phi}$ as well as $\Phi^{A}$ and $\nabla \Phi^{A}$. We take inspiration from particle mechanics where $q_{i}$ and $\dot{q}_{i}$ are treated independently. As such:

$$
\frac{\delta}{\delta \dot{\Phi}^{A}(t, \mathbf{x})}\dot{\Phi}^{B}(t, \mathbf{x}) = \delta^{B}_{A}\delta^{3}(\mathbf{x}-\mathbf{y}),
$$

where $\mathbf{x}$ is the space coordinate. This is analogous to $\partial \dot{q}_{i}/\partial \dot{q}_{j}= \delta_{ij}$ and $\partial g_{i}/\partial \dot{q}_{j}= 0$ in the discrete classical case. As per the second condition, the functional derivatives of the fields with respect to $\dot{\Phi}^{A}$ vanish. Also note that the functional derivative of $\dot{\Phi}$ with respect to itself is not dimensionless, but has dimensions of inverse volume.

We can now introduce the Hamiltonian of the system $\mathcal{H}$, which is again understood to be the Hamiltonian *density*. The total Hamiltonian will be denoted by $H$. We can then define $\mathcal{H}$ as

$$
\mathcal{H}(\Phi^{A}, \nabla \Phi^{A}, \Pi_{A}) = \Pi_{A}\dot{\Phi}^{A}-\mathcal{L} (\Phi^{A}, \partial_{\mu}\Phi^{A}).
$$

^d1ee1d

The Lagrangian is a function of the fields and their partial derivatives with respect to all space-time coordinates. In the Hamiltonian, the field time-derivatives are replaced by the canonical momenta $\Pi_{A}$. As a note, the Hamiltonian can still be a function of of spatial derivatives. The total Hamiltonian is analogous to the total Lagrangian (also a functional.)

# In-class Notes

Problem: Suppose we have a system with configuration $q^{n}(t), \; \dot{q}^{n}$. We have some initial condition $q^{n}(t_{i})$ and $\dot{q}(t_{i})$ and we want to get to some final condition $q^{n}(t_{f})$ and $\dot{q}(t_{f})$. We can picture this in phase space as a path through the space. In classical mechanics, there is only one path, which is determined by some

$$
S = \int_{t_{i}}^{t_{f}}L (q, \dot{q})\dd{t}
$$

such that $\delta S = 0$. $L = T-V$ is known as the Lagrangian. $L$ should be Lorentz invariant. From this, we get the EL equations:

$$
\pdv{L}{q^{n}} -\dv{t}\pdv{L}{\dot{q}^{n}} = 0.
$$

To get the Hamiltonian formulation, we let $p_{n}= \partial L/\partial \dot{q}^{n}$. Then, by using a Legendre transform, we define $H = p_{n}\dot{q}^{n}-L$. It can be shown that $H$ depends only on $p$ and $q$. Then,

$$
\begin{align}
\dot{q}^{n} & = \pdv{H}{p_{n}} \\[1 em]
\dot{p}_{n} & = -\pdv{H}{q^{n}}.
\end{align}
$$

Something more fundamental than the Hamiltonian is the Poisson bracket. In fact,

$$
\begin{align}
\dot{q} & = \{q, H\} \\[1 em]
& = \pdv{H}{p_{m}}.
\end{align}
$$

To go to a field theory, we now have fields $\Phi^{A}(x)= \Phi^{A}(x^{\mu})$. The action is then

$$
S = \int_{t_{i}}^{t_{f}}L (\Phi^{A}(t), \partial_{\mu}\Phi^{A})\dd{t}.
$$

We can write $L$ as a Lagrangian density $\mathcal{L}$, and rewrite $S$:

$$
S = \int_{\Omega}\mathcal{L}(\Phi^{A}, \partial_{\mu}\Phi^{A})\dd[4]{x}.
$$

What we really care about is $\mathcal{L}$, and so we will just call it the Lagrangian.

We still select the path according to $\delta S = 0$, which again gives a unique path. The EL equation is very similar to the classical version:

$$
\pdv{\mathcal{L}}{\Phi^{A}} = \partial_{\mu}\left(\pdv{\mathcal{L}}{ (\partial_{\mu}\Phi^{A})}\right).
$$

For the Hamiltonian, we need a field equivalent for momentum:

$$
\Pi_{A}(x) = \frac{\delta L}{\delta \Phi^{A}} = \pdv{\mathcal{L}}{\Phi^{A}}.
$$

Then, the Hamiltonian density can be written as

$$
\mathcal{H} = \Pi_{A}\dot{\Phi}^{A}-\mathcal{L}(\Phi^{A}, \partial_{\mu}\Phi^{A}),
$$

with

$$
H = \int \mathcal{H}(\Phi^{A}, \Pi_{A})\dd[3]{x}.
$$

The Poisson bracket is then defined for fields as

$$
\{F_{1}, F_{2} \} = \int \frac{\delta F_{1}(x)}{\delta \Phi^{A}(z)}\frac{\delta F_{2}(y)}{\delta \Pi_{A}(z)} - \frac{\delta F_{1}(x)}{\delta \Pi_{A}(z)}\frac{\delta F_{2}(y)}{\delta \Phi^{A}(z)}\dd[3]{x}
$$

For example,

$$
\begin{align}
\{q^{B}(x), \Pi_{C}(y)\} = \delta_{C}^{B}\delta (x-y)
\end{align}
$$

Note that $x$, $y$, and $z$ are spatial coordinates (they should be $\mathbf{x}, \; \mathbf{y}, \; \mathbf{z}$).