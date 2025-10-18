Focusing on finding different lapse functions to decouple different components of the Hamiltonian. The idea will be to find a way to solve 3/4 equations, and finding the last one by substitution.

Perhaps some trigonometric substitution can help eliminate the cosine in the Poisson bracket.

Seems like it is not possible to decouple the equations. the cosine term is actually

$$
\begin{align}
\cos\left(\sqrt{2\alpha}\frac{b}{p_{b}} \right),
\end{align}
$$

Canonical transformation: let $b/p_{b}\to u$ such that 

$$
\pb{u}{p_{b}} = \frac{1}{p_{b}}\cos(\sqrt{2\alpha_{b}}u).
$$

Same thig happens with $c/p_{c}\to v$, with

$$
\pb{v}{p_{c}} = -\frac{2}{p_{c}}\cos(\sqrt{2\alpha_{c}}u).
$$

then the Hamiltonian becomes

![[CanonicalTransform.jpg]]

Try similar Lapse, but with $b$ instead of $p_{b}$.

If not good, try numerically. For boundary values, try "Near the horizon", classically find values of canonical vars near the horizon. These will be the boundary vars of the quantum vars near the horizon.