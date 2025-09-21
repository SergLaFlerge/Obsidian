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
 \pb{b}{p_{b}} & = G \gamma \cos(\sqrt{2  \bar{\alpha}_{b}}\cdot b^{2}) \\[1 em]
\pb{c}{p_{c}} & = 2G \gamma \cos(\sqrt{2 \bar{\alpha}_{c}}\cdot c^{2})
\end{align}
$$