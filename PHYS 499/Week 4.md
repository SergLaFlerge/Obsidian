We have from (4.3) and (4.4) that 

$$
\begin{align}
\pb{b}{p_{b}} &= G\gamma(1+\bar{\beta}_{b}b^{2}) = G\gamma\left(1+\frac{\beta_{b}L_{0}^{4}}{p_{b}^{2}}b^{2} \right)\\[1em]
\pb{c}{p_{c}} &= 2G\gamma(1+\bar{\beta}_{c}c^{2}) = 2G\gamma\left(1+\frac{\beta_{c}L_{0}^{4}}{p_{c}^{2}}c^{2} \right)
\end{align}
$$

We want the RHS terms to be the result of a Taylor expansion of a $\cos$ term that depends on both coordinate and momentum. For (my) simplicity, we will do a variable change $\bar{\beta}_{i}\to-\bar{\alpha}_{i}$, so that in the new variables, the above read as

$$
\begin{align}
\pb{b}{p_{b}} & = G \gamma (1-\bar{\alpha}_{b}b^{2}) \\[1 em]
\pb{c}{p_{c}} & = 2G \gamma (1-\bar{\alpha}_{c}c^{2})
\end{align}
$$

^df9c33

Recall the Taylor series expansion for $\cos\theta$ about $\theta = 0$:
$$
\cos \theta \approx 1-\frac{\theta^{2}}{2} + \order{\theta}^{4}.
$$

It is clear that by taking $\theta \to \sqrt{2 \bar{\alpha}_{i}}\cdot i^{2}$ for $i = b, c$, we get back our starting equations when expanding to second order. As such, we can now take our [[Week 4#^df9c33|modified]] Poisson brackets from above as a second order perturbative term of the following Poisson brackets:

$$
\begin{align}
 \pb{b}{p_{b}} & = G \gamma \cos(\sqrt{2  \bar{\alpha}_{b}}\cdot b) \\[1 em]
\pb{c}{p_{c}} & = 2G \gamma \cos(\sqrt{2 \bar{\alpha}_{c}}\cdot c)
\end{align}
$$

Using this modified Poisson algebra on the Hamiltonian from [[PHYS499-Paper-1.pdf|paper 1]] results in highly nonlinear differential equations with no analytical solutions. We can, however, modify the lapse function without changing the dynamics of the system. We now attempt another modification to the Hamiltonian. For the lapse function

$$
N(T) = \text{{sgn}}(p_{c})\sqrt{|p_{c}(T)|},
$$

we obtain the new modified Hamiltonian

$$
\tilde{H} = \frac{-1}{2G\gamma^{2}}[(\tilde{b}^{2}+\gamma^{2})\tilde{p}_{b} + \tilde{b}\tilde{c}\tilde{p}_{c}]
$$

This gives an independent equation of motion in $b$ and three coupled equations for the rest. We can, however, decouple $p_{b}$ thanks to the following constraint

$$
(b^{2}+\gamma^{2})\frac{p_{b}}{b} + 2cp_{c} \approx 0.
$$

As of now, we have 

$$
\begin{align}
\dot{\tilde{b}} &= \pb{b}{H} \\[1em]
&= -\frac{\left(b^2+\gamma^2\right) \cos (a b)}{2 \gamma } \\[1em]
b(\tilde{T}) &= -\frac{b \cos (a b)}{a^2 \gamma }-\frac{\left(a^2 b^2-2\right) \sin (a b)}{2 a^3 \gamma }-\frac{\gamma  \sin (a b)}{2 a}
\end{align}
$$

*Potential different approach* Canonical transformation. You can be less strict with your choice of $N$. Just need to be able to solve 3/4 equations. Last one can be found by the constraint. You can choose N such that only one of the coordinate is decoupled $\dot{b}= \dot{b}(b)$