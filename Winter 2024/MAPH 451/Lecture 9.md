# Critical Point Analysis of Lorenz Attractor

Last lecture, we found three critical points:

$$
\begin{align}
x & = y = z = 0 \qc \rho < 1 \\[1 em]
x & = y = \pm r \qc z = r^{2}= \rho-1.
\end{align}
$$

As $\rho$ increases past $1$, our first point goes from a stable node to a saddle point and we get a pitchfork bifurcation, obtaining the other two points. For $r \ll1$, we get a stable node while for $r \rightarrow \infty$, we get some spiral nodes. There are some other interesting results in between as well.

# Global Analysis of ODEs

We have done a thorough look through local analysis of ODEs, where we constructed a solution near a point $x_{0}$ using a variety of methods, such as Taylor series, asymptotic series, and the Frobenius method.

We now turn to the *global* analysis, where we now want a uniform approximation for "all" (read: for a wide range) values of $x$.

Consider the following example:

$$
y'' (x) = f (x)y (x)\qc y (0) = 1, y' (0) = 1.
$$

Let us introduce a small parameter $\epsilon$:

$$
y'' (x) = \epsilon f (x)y (x)
$$

and look for a solution of the form

$$
y (x) = \sum\limits_{n = 0}^{\infty}\epsilon^{n}y_{n}(x).
$$

We then find the solution to our equation by taking $\epsilon \rightarrow 1$. For our example:

$$
\begin{align}
\sum\limits_{n = 0}\epsilon^{n}y''_{n} & = \sum\limits_{n = 0}^{\infty}\epsilon^{n + 1}y_{n}(x) \\[1 em]
\epsilon^{0}:\quad y''_{0} & = 0 \implies y_{0} = 1 + x \\[1 em]
\epsilon^{1}:\quad y_{1}'' & = (1 + x)f (x), \; y_{1}(x) = \int_{0}^{x}\int_{0}^{t}(1 + s)f (s)\dd{s}\dd{t} \\[1 em]
\epsilon^{2}:\quad y''_{2} & = y_{1}f (x), \; y_{2} = \int_{0}^{x}\int_{0}^{t}\int_{0}^{s}\int_{0}^{v}(1 + u)f (u)\dd{u}\dd{v}\dd{s}\dd{t}.
\end{align}
$$

Then

$$
y (x) = (1 + x) + \cancelto{1}{\epsilon}y_{1} + \cancelto{1}{\epsilon^{2}}y_{2}+ \cdots
$$

and we must now pray that our series is actually convergent. For linear equations like the one above, we can readily show that the resulting series is convergent. Suppose $f (x)$ is bounded. That is, $\abs{f (t)}< k$ for $0 < t < k$. Then

$$
\begin{align}
\abs{y_{1}(x)} & \leq k \int_{0}^{x}\int_{0}^{t}s + 1 \dd{s}\dd{t} = k \left(\frac{x^{2}}{2}+ \frac{x^{3}}{6} \right) \\[1 em]
y_{2} & = \int_{0}^{x}\int_{0}^{t}\cancelto{k}{f (s)}k\left(\frac{x^{2}}{2}+ \frac{x^{3}}{6} \right) \dd{s}\dd{t} \\[1 em]
\abs{y_{2}} & \leq k^{2}\left(\frac{x^{4}}{4!}+ \frac{x^{5}}{5!} \right) \\[1 em]
\abs{y_{n}} & \leq k^{n}\left(\frac{x^{2 n}}{(2 n)!}+ \frac{x^{2 n + 1}}{(2 n + 1)!} \right).
\end{align}
$$

This series is factorially convergent.

#### General Prescription

1. Find/introduce a small parameter depend $\epsilon$ such that the leading order of the result is "close" to the exact one.
2. Look for the solution as a series in $\epsilon$.
3. Pray for convergence.

A problem arises if we have a non-analytic dependence on $\epsilon$. Take for example

$$
y'' (x) + y (x) -y^{3}(x) = 0.
$$

The exact solution is

$$
y (x) = \frac{1}{\sqrt{\epsilon}}\tanh \left(\frac{x}{\sqrt{2}} \right),
$$

which our solution will never approach. This singular dependence on a small parameter also appears in linear equations where $\epsilon$ multiplies the highest order derivative. The rest of the chapter will be spent learning methods to overcome these challenges using perturbation theory and boundary layer theory.