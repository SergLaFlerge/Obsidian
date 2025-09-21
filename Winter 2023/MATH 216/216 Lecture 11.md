Recall the sequence

$$
\begin{align}
a_{n + 1} & = \frac{1}{2}\left(a_{n}+ \frac{2}{a_{n}} \right), \\
a_{1} & = 2.
\end{align}
$$

We found that $\sqrt{2}\leq a_{n}\leq 2\Rightarrow$ bounded, and $a_{n + 1}< a_{n}\Rightarrow$ decreasing. So $(a_{n})$ converges $(a_{n}\rightarrow \sqrt{2})$. Now we have the tools to see how fast it falls to $\sqrt{2}$.

$$
\begin{align}
a_{n + 1}^{2} & = \frac{1}{4}\left(a_{n}^{2}+ 4 + \frac{4}{a_{n}^{2}} \right)\\
0 & \leq a_{n + 1}-2 = \frac{1}{4}\left(a_{n}-\frac{2}{a_{n}} \right)^{2}\\
& = \frac{1}{4}\frac{(a_{n}^{2}-2)^{2}}{a_{n}^{2}}\\
& \leq \frac{1}{8}(a_{n}^{2}-2)^{2}\\
& \therefore \\
0 & \leq a_{n + 1}-2 \leq \frac{1}{8}(a_{n}^{2}-2)^{2}\quad \forall \; n \in \mathbb{N}\\
a_{2}^{2} -2 & \leq \frac{1}{8}(a_{1}^{2}-2)^{2}\\
a_{3}^{2}-2 & \leq \frac{1}{8}(a_{2}^{2}-2)^{2}\\
& = \frac{1}{8^{2}}(a_{1}^{2}-2)^{4}\\
& \vdots \\
0 \leq a_{n}^{2}-2& \leq \frac{8}{2^{2^{n}}}
\end{align}
$$

Which goes to zero *extremely* fast. Even faster than our $n^{n}$.

This is amazing. If we look at even $a_{4}$, we get the result $a_{4} \approx 1.4142156$, which is already pretty close to $\sqrt{2}\approx 1.4142135$, which is correct to **six** digits!!

In essence, this method of approximating $\sqrt{2}$ was already known by the Babylonians around 1600 B.C. In fact, to can approximate *any* number by changing 2 for any other $n$.