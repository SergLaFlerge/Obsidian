# Local Analysis of Linear ODEs

The most general linear ODE has the form

$$
y^{(n)} + P_{n-1}(x)y^{(n-1)} + \cdots + P_{0}(x) y = 0.
$$

If $P_{k}$ are analytic near $x = x_{0}$ the solution is then analytic. That is,

$$
y (x) = \sum\limits_{n = 0}^{\infty}a_{n}(x-x_{0})^{n},
$$

which is a Taylor series. This Taylor series has a convergence radius, which is just a distance to the nearest singularity of $P_{k}(x)$, and $a_{n}= a_{n}(a_{k})$ for $k < n$.

Now suppose that $P_{k}$ has a pole of degree $n-k$ or less at $x = x_{0}$. $x_{0}$ is then called a regular singular point, and $y (x)$ can then have a hole or branch point at $x = x_{0}$. The general idea is that if

$$
\begin{align}
y \sim \frac{1}{(x-x_{0})^{a}}, \\[1 em]
y^{(n)} \sim \frac{1}{(x-x_{0})^{a + n}}
\end{align}
$$

then

$$
P_{0}(x) y \sim \frac{1}{(x-x_{0})^{n + a}}.
$$

For a regular singular point, at least one of the solution has the form

$$
y (x) = (x-x_{0})^{\alpha}\sum\limits_{n = 0}^{\infty} a_{n}(x-x_{0})^{n}.
$$

This is called a Frobenius series, and the sum is exactly analytic, usually shortened to $A (x)$ in this course. This series is an n-th order algebraic equation in $\alpha$.

Consider the case $n = 2$. Then we have two roots, say $\alpha$ and $\beta$. We have the solution for $\alpha$ from above, and the solution for $\beta$ may have a similar form, but we run into a problem when $\alpha = \beta$, as the solution become degenerate. We can use the natural logarithm to make the solution non-degenerate. In particular, we have

$$
y (x) = \ln (x-x_{0})\cdot (x-x_{0})^{\beta}A (x) + (x-x_{0})^{\beta}B (x).
$$

The main idea is that, for constant coefficients, we have $y = e^{\alpha x}$, and from there we obtain an equation in $\alpha$ of n-th order. For $n = 2$ we have that the second solution is $y_{2}(x)= xe^{\alpha x}$, which should come as no surprise from ODE theory.

### Example

$$
y^{(2)} + \frac{2}{x}y^{(1)}-\frac{1}{x}y = 0.
$$

$x = 0$ is a regular singular point. We now take

$$
y = x^{\alpha}\sum\limits_{n = 0}^{\infty} a_{n}x^{n}
$$

and substitute it into our differential equation:

$$
\sum\limits_{n = 0}^{\infty}(n + \alpha)(n + \alpha-1)a_{n}x^{n-2 + \alpha}+ \sum\limits_{n = 0}^{\infty}2(n + \alpha)a_{n}x^{n - 2 + \alpha}-\sum\limits_{n = 0}^{\infty}a_{n}x^{n-1 + \alpha}.
$$

We only care about the "most singular" points, so for $n = 0$, those are the terms with $x^{\alpha-2}$. In that case we have an algebraic equation

$$
\begin{align}
[\alpha (\alpha-1)+ 2 \alpha]a_{0} = 0 \qc a_{0}\neq 0\\[1 em]
\alpha = 0,-1.
\end{align}
$$

If $\alpha= 0$, the solution is simple,

$$
\begin{align}
n (n-1)a_{n}+ 2 na_{n}-a_{n-1}= 0 \\[1 em]
a_{n} = \frac{a_{n-1}}{n (n + 1)}.
\end{align}
$$

The $a_{n-1}$ appears through the last term, as we make an index shift so all powers of $x$ are the same. We now have the coefficients for  one of the solutions. If we go through the same process, we encounter a problem, as $a_{0}= 0$, but our restriction prevents us from having this as a solution. This is where we use our "logarithm exclusion"

$$
y (x) = \ln (x)\cdot x^{\alpha} A (x) + x^{\beta}\sum\limits_{n = 0}^{\infty}b_{n}x^{n},
$$

where $x^{\beta}$ is really $1/x$ and $x^{\alpha}= 1$. The most singular point has the $x^{-3}$ terms, which then give

$$
\begin{align}
b_{0}\beta (\beta+1)b_{0} & = 0 \\[1 em]
\beta & = -1.
\end{align}
$$

For $1/x^{2}$, we have

$$
\begin{align}
a_{0} + (\beta + 1)(\beta + 2)b_{1}-b_{0} & = 0 \\[1 em]
a_{0}-b_{0} & = 0 \\[1 em]
a_{0} & = b_{0} = 1.
\end{align}
$$

The final result is then

$$
\begin{align}
y_{1}(x) & = A (x) = \sum\limits_{n = 0}^{\infty} a_{n}x^{n} \\[1 em]
y_{2}(x) & = \ln (x)A (x) + \frac{1}{x}B (x) \qc B (x) = \sum\limits_{n = 0}^{\infty}b_{n}x^{n}
\end{align}
$$