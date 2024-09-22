# The Exterior Derivative

We have a map $\dd{}:A (M)\rightarrow A (M)$,

$$
\dd{(A^{r}(M))}\subset A^{r + 1}(M).
$$

This map has the following properties:
- $\dd{(\omega_{1}+ \omega_{2})}= \dd{\omega_{1}}+ \dd{\omega_{2}}$.
- $\dd{(\omega_{1}\wedge \omega_{2})}= \dd{\omega_{1}}\wedge \dd{\omega_{2}} + (-1)^{r}\dd{\omega_{1}}\wedge \dd{\omega_{2}}$.
- For $f \in A^{0}(M)= C^{\infty}$, $\dd{f}$ is the differential.
- $\dd{(\dd{f})}= 0$.

If $\dd{}$ exists, then it is local. That is, for $U \ni p$ an open neighborhood in $M$, if $\omega_{1}|_{U}= \omega_{2}|_{U}$, then $\dd{\omega_{1}}\|_{U}= \dd{\omega_{2}}|_{U}$.

## Component Computations

Say $\set{\pdv{x^{i}}}$ is a basis for $T_{p}M$ at each $p \in U \subset M$. Let $\set{\dd{x^{i}}}$ be its dual basis. For $f \in C^{\infty}$, we have

$$
\dd{f} = \pdv{f}{x^{i}}\dd{x^{i}},
$$

and for $\omega = \omega_{j}\dd{x^{j}}$, we have

$$
\begin{align}
\dd{\omega} & = \pdv{\omega_{j}}{x^{i}}\dd{x^{i}}\wedge \dd{x^{j}} \\[1 em]
& = \frac{1}{2}\pdv{\omega_{j}}{x^{i}}(\dd{x^{i}}\otimes \dd{x^{j}}-\dd{x^{j}}\otimes \dd{x^{i}}).
\end{align}
$$

Note: In physics it is common to drop the tensor product for notational convenience.

## Naturality of $\dd{}$

An operator is called *natural* if it commutes with diffeomorphisms. $\dd{}$ is therefore natural.

### Theorem

Let $\Psi:M \rightarrow N$. Let $\Psi^{*}:A (N)\rightarrow A (M)$ denote the pullback of differentiable forms. Then

$$
\Psi^{*}\cdot \dd{} = \dd{}\cdot \Psi^{*}:A (N)\rightarrow A (M).
$$

In other words, the following diagram commutes:

```tikz
		\usepackage{tikz-cd}
		\tikzcdset{scale cd/.style={every label/.append style={scale=#1},
	    cells={nodes={scale=#1}}}}
		
		\begin{document}
		\begin{tikzcd}[color = white, scale cd = 1.5, sep = large]
		 A (N) \arrow[d, "\Psi^{*}" swap] \arrow[r, "\mathrm{d}"] & A (N) \arrow[d,"\Psi^{*}"] \\
		A (M)\arrow[r, "\mathrm{d}"] & A (M)
		\end{tikzcd}
		
		% "swap" changes the position of the label if it gets too cluttered.
		% row sep and column sep sorta lets you scale by adjusting the distances between 
		% your matrix elements. 
		
		\end{document}
		```