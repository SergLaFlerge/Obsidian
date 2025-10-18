Last week's substitution may have done something. We start with $c$ and $p_{c}$ as they may have simpler forms with the choice of Lapse function (and the form of the Hamiltonian in general).

We change the lapse function from [[Week 5]] to have $B$ as the denominator instead of $p_{b}$. That is,

$$
\begin{align}
N & = \frac{\text{sgn}(p_{c})\sqrt{\abs{p_{c}}}}{B} \\[1em]
H & = \frac{1}{2G\gamma^{2}}\left[\left( Bp_{b}^{2} + \frac{\gamma^{2}}{B} \right)p_{b} + 2Cp_{b}p_{c}^{2} \right]
\end{align}
$$

From here, we can  now examine the Poisson brackets of $C$ and $p_{c}$ to solve the equations of motion:

$$
\begin{align}
\dot{C} & = \pb{C}{H} \\[1em]
\dot{p}_{c} & = -\pb{p_{c}}{H}
\end{align}
$$

**Note** we must also realize that since $C = C(p_{c})$, the Poisson bracket for the Hamiltonian is different. In particular, 

$$
\begin{align}
\partial_{p_{c}}(C) & = \partial_{p_{c}}\left(\frac{c}{p_{c}} \right)\\[1em]
& = \frac{-c}{p_{c}^{2}} \\[1em]
& = \frac{-C}{p_{c}}
\end{align}
$$

It seems as though there will be no analytic solution found for this Poisson algebra.

To do the work numerically, we need to find appropriate boundaries

We found appropriate boundaries.  Now we must find $b$ and $p_{b}$. We substitute solc and solpc into our equations for $b$ and $p_{b}$ to find numerical solutions for them.

Next step is to approximate all four with analytical expressions to obtain an analytical metric (Consult with Jorden).