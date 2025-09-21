For a topological space $M$, a real vector bundle over $M$ is a topological space $E$— called the *total space*— with a surjective continuous projection $\pi:E \rightarrow M$ such that
- For each $p \in M$, the set $E_{p}= \pi^{-1}(p)\subset E$ (the *fiber* over $p$) is a $k-$dimensional real vector space, and
- For each $p \in M$, there is a neighborhood $U \ni p$ in $M$ and a homeomorphism $\Phi:\pi^{-1}(U)\rightarrow U \times \mathbb{R}^{n}$ (called a *local trivialization of $E$ over $U$*) such that the following diagram commutes:
	```tikz
	\usepackage{tikz-cd}
	\tikzcdset{scale cd/.style={every label/.append style={scale=#1},
    cells={nodes={scale=#1}}}}
	
	\begin{document}
	\begin{tikzcd}[color = white, scale cd = 1.5, sep = large]
	 \pi^{-1}(U) \arrow[d, "\pi" swap] \arrow[r, "\Phi"] & U \times \mathcal{R}^{k} \arrow[dl,"\pi_{1}"] \\
	U &
	\end{tikzcd}
	
	% "swap" changes the position of the label if it gets too cluttered.
	% row sep and column sep sorta lets you scale by adjusting the distances between 
	% your matrix elements. 
	
	\end{document}
	```

where $\pi_{1}:U \times \mathbb{R}^{k}\rightarrow U$ is a projection on the first factor, and $\Phi_{\pi^{-1}(U)}:\set{q}\times \mathbb{R}^{k}\rightarrow \mathbb{R}^{k}$ is a linear isomorphism.

# Smooth Vector Bundles

If $E, M$ are smooth manifolds, $\pi$ is smooth, and the local trivializations $\Phi$ are smooth diffeomorphisms, then $\pi:E \rightarrow M$ is a smooth vector bundle.

## Trivial Bundles

If there exists a local trivialization $\Phi:\pi^{-1}(M)\rightarrow M \times \mathbb{R}^{k}$ over all of $M$, then the bundle is globally trivial.

Smooth, globally trivial bundles are diffeomorphic to $M \times \mathbb{R}^{k}$, and are also called *product bundles*.

## Overlapping Trivializations

#### Lemma

Let $\pi:E \rightarrow M$ be a smooth vector bundle. Suppose $\Phi:\pi^{-1}(M)\rightarrow U \times \mathbb{R}^{k}$ and $\Psi:\pi^{-1}(V)\rightarrow V \times\mathbb{R}^{k}$ are local trivializations such that $U \cap V$ is non-empty. Then there is a smooth map $\tau:U \cap V \rightarrow \text{GL}(n, \mathbb{R})$ such that the composition $\Phi \circ \Psi^{-1}:(U \cap V)\times \mathbb{R}^{k}\rightarrow (U \cap V)\times \mathbb{R}^{k}$ has the form

$$
\Phi \circ \Psi^{-1}(p, v) = (p, \tau (p)v).
$$

## $\text{GL}(n, \mathbb{R})$

$\text{GL}(n, \mathbb{R})$ is a matrix group. An element of $\text{GL}(n, \mathbb{R})$ may be written as an invertible $n \times n$ matrix with real entries. The group operation is matrix multiplication. If particular, $\text{GL}(n \mathbb{R})$ is a group of automorphisms of the $n-$dimensional space $V = \mathbb{R}^{n}$. They map $V$ to itself bijectively.

## Vector Bundle Construction Lemma

Let $M$ be a smooth manifold with open cover $\set{U_{\alpha}\mid\alpha \in A}$. For each $p \in M$, let $E_{p}$ be a $k-$dimensional vector space, and define

$$
E = \bigcup_{p \in M}E_{p}.
$$

Given
- $\pi:E \rightarrow M:E_{p}\mapsto p$.
- For each $\alpha \in A$, a bijective map $\Phi_{\alpha}:\pi^{-1}(U_{\alpha})\rightarrow U_{\alpha}\times\mathbb{R}^{k}$ whose restriction to each $E_{p}$ is a linear isomorphism $E_{p}\rightarrow \set{p}\times \mathbb{R}^{k}\simeq \mathbb{R}^{k}$, and
-  For each $\alpha, \beta\in A$ such that $U_{\alpha}\cap U_{\beta}$ is non-empty, a smooth map $\tau_{\alpha \beta}:U_{\alpha}\cap U_{\beta}\rightarrow \text{GL}(n, \mathbb{R})$ such that
	$$
\begin{align}
\Phi_{\alpha} \circ \Phi_{\beta}:U_{\alpha}\cap U_{\beta} & \rightarrow U_{\alpha}\cap U_{\beta} \\[1 em]
(p, v) & \mapsto (p, \tau_{\alpha \beta}(p) v)
\end{align}
$$

Then $E$ has a unique manifold structure making it a smooth vector bundle of rank $k$ over $M$.