# Complete Local Analysis of the ODE

We now have three regions where we have solutions, with two solutions each:

$$
\begin{align}
x & \rightarrow \pm \infty & x & \rightarrow 0^{+} & x & \rightarrow 0^{-} \\[1 em]
A \left(\frac{1}{x} \right) &, a_{0} = 1 & &\frac{x^{3/4}\exp (2 x^{-1/2})}{2 \sqrt{\pi}} & &\frac{\abs{x}^{3/4}}{\sqrt{\pi}}\cos \left(2 \abs{x}^{-1/2}+ \frac{\pi}{4} \right) \\[1 em]
-A (x) \ln(x) &+ xB \left(\frac{1}{x} \right), \; b_{0}= 1 & & \sqrt{\pi}x^{3/4}\exp (-2 x^{-1/2}) & &\frac{\abs{x}^{3/4}}{\sqrt{\pi}}\sin \left(2 \abs{x}^{-1/2} + \frac{\pi}{4} \right)
\end{align}
$$

# Qualitative Analysis of Non-linear DEs

We will look the DEs of the form

$$
y^{(n)}= F \left(x, y (x), y^{(1)}, ..., y^{(n-1)} \right).
$$

If $F$ does not depend on $x$, the DE is called autonomous. We can turn a non-autonomous equation into an autonomous equation by taking a derivative:

$$
\begin{align}
x & = X (y, ..., y^{(n)}) \\[1 em]
1 = P (y, ..., y^{(n + 1)}).
\end{align}
$$

Now $P$ is an $n + 1$ order autonomous equation. An $n-$th order autonomous equation implies $n$ first-order equations:

$$
\begin{align}
y_{1} & = y \qc y_{2} = y^{(1)} , ..., y_{n} = y^{(n-1)} \\[1 em]
\dot{y}_{1} & = y_{2} \\[1 em]
\dot{y}_{2} & = y_{3} \\[1 em]
& \vdots \\[1 em]
\dot{y}_{n-1} & = F (y_{1}, ..., y_{n}).
\end{align}
$$

Consider the general case:

$$
\begin{align}
\dot{y}_{1} & = f_{1}(y_{1}, ..., y_{n}) \\[1 em]
\dot{y}_{2} & = f_{2} \\[1 em]
&\vdots \\[1 em]
\dot{y}_{n} & = f_{n}.
\end{align}
$$

We will start with the case where $f_{i}$ are analytic

# Method of Critical Points (Critical Exponent)

We have critical points $\bar{y}_{0}$ such that

$$
f_{i}(y_{0_{1}}, ..., y_{0_{n}}) = 0 \; \forall \; i \in[1, n].
$$

The main idea is to linearize the system near $\bar{y}_{0}$ to get a qualitative picture of the trajectories in the phase space.

## One Dimension

We have 3 types of critical points (without loss of generality, we use $y_{0}= 0$):
- Stable node: $\dot{y}=-y^{3}$, $y \underset{t \rightarrow \infty}{\rightarrow}0$.
- Unstable node: $\dot{y}= y^{5}$, $y \underset{t \rightarrow \infty}{\rightarrow}\infty$.
- Saddle point: $\dot{y}= y^{2}$, $y \rightarrow 0$ for $y < 0$ and $y \rightarrow \infty$ for $y > 0$ as $t \rightarrow \infty$.

Consider for example

$$
\begin{align}
\dot{y} & = y^{2} -y \rightarrow y_{0} = 0, 1 \\[1 em]
y (t) & = y_{0} + \epsilon (t)\qc \epsilon (t) \ll 1.
\end{align}
$$

Substituting:

$$
\begin{align}
\dot{\epsilon} & = -\epsilon + \order{\epsilon^{2}} \\[1 em]
\epsilon (t) & = Ce^{-t}\qc \epsilon \underset{t \rightarrow \infty}{\rightarrow} 0
\end{align}
$$

So $0$ is a stable node. For $y_{0}= 1$, we get

$$
\begin{align}
\dot{\epsilon} & = \epsilon + \order{\epsilon^{2}} \\[1 em]
\epsilon & = Ce^{t}\qc \epsilon \underset{t \rightarrow \infty}{\rightarrow} 0,
\end{align}
$$

so $1$ is an unstable node.

## Two Dimensional Systems

We now have

$$
\begin{align}
y_{1} & = y_{0_{1}} + \epsilon_{1} \\
y_{2} & = y_{0_{2}} + \epsilon_{2} \\[1 em]
\dot{\epsilon}_{1} & = a \epsilon_{1} + b \epsilon_{2} + \order{\epsilon^{2}} \\
\dot{\epsilon}_{2} & = c \epsilon_{1} + d \epsilon_{2} + \order{\epsilon^{2}} \\[1 em]
\dot{\bar{\epsilon}} & = \mathbb{M}\bar{\epsilon}\qc
\mathbb{M} =
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
\end{align}
$$

By diagonalizing we reduce the problem to 2 one-dimensional problems:

$$
\begin{align}
\mathbb{M} \bar{\epsilon}_{i} & = \lambda_{i}\bar{\epsilon}_{i} \\[1 em]
\det (\mathbb{M}-\lambda \mathbb{I} ) & = 0 \\[1 em]
\frac{a + d \pm \sqrt{(a + d)^{2}-4 (ad-cb)}}{2} & = \lambda_{i}.
\end{align}
$$

There are three main cases:

1. $\Im (\lambda_{1})= 0$. If both $\lambda_{i}> 0$, it is unstable. If $\lambda_{i}< 0$, it is stable, and if $\lambda_{1}\lambda_{2}$ it is a saddle point.
2. $\Re (\lambda_{i})= 0$. Then $\lambda_{1}= \lambda_{2}^{*}$