First coordinate is done ($C$). It has a $\tanh$ fit that converges to the numerical value at $R_{s}$. Problem: it is written in arbitrary variables. Need to write these arbitrary variables in terms of our actual parameters; particularly $K_{c}$. As it stands, the (scaled) fit is as such:

$$
C(t)_{(0, 1)} = \frac{1+\tanh(\alpha(t-t_{0}))}{2}
$$

Which is then scaled to match the numerical solution:

$$
\begin{align}
C (t) & = C (0) + [C (R_{s})-C (0)] \cdot C (t)_{(0, 1)} \\[1 em]
& = C (0) + [C (R_{s})-C (0)]\frac{1+\tanh(\alpha(t-t_{0}))}{2}.
\end{align}
$$

This is for a specific choice of $K_{c}$. We now need to vary $K_{c}$ to see how it is related to $\alpha$ and $t_{0}$.

First observations: Changing $K_{c}$ by an order of magnitude changes the left endpoint by the inverse, i.e. increasing $K_{c}$ by one order of magnitude decreases the magnitude of the left endpoint by one order of magnitude $\implies$ inverse relationship between $C (0)$ and $K_{c}$. By setting  $K_{c}= 1$ we can then determine the proportionality constant:

$$
C (0) \approx -\frac{1.5708}{K_{c}}.
$$

Let $\kappa_{c} =K_{c}\cdot C (0)$. We now have

$$
C (t) = \frac{\kappa_{c}}{K_{c}} + \left[ C (R_{s})-\frac{\kappa_{c}}{K_{c}} \right]\frac{1 + \tanh (\alpha (t-t_{0}))}{2}.
$$

Changing $K_{c}$ does not affect the right endpoint value. Now we see how the slope changes we vary $K_{c}$. We take care of $t_{0}$ last.

