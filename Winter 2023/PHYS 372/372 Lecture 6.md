 Last time we introduced the ladder operators, $\hat{a}_{+}$ and $\hat{a}_{-}$, and explored some of their properties. We found that we would rewrite the Hamiltonian in terms of these operators, and this allowed us to be able to find solutions to the simple harmonic oscillator given one solution. This time, we will start by finding this solution, and applying the operators to find a general solution.

Say there exists a solution with the lowest energy state (which we know should exist from other examples) and call it $\psi_{0}$. If we apply $\hat{a}_{-}$, we get

$$
\begin{align}
\hat{a}_{-}(\psi_{0}) & = 0 \\
\left(\frac{i \hat{p}+ m \omega x}{\sqrt{2 \hbar \omega m}} \right)(\psi_{0}) & = 0 \\
(i \hat{p}+ m \omega x)(\psi_{0}) & = 0 \\
\dv{\psi_{0}}{x} & = \frac{-m \omega x}{\hbar}\psi_{0}\\
& \Downarrow \\
\psi_{0} & = A \exp\left(\frac{-m \omega x^{2}}{2\hbar}\right).
\end{align}
$$

So now all we need to do is find $A$. For that, we can use the normalization condition,

$$
\int_{-\infty}^{\infty} |\psi_{0}|^{2}\dd{x} = 1,
$$

And find that

$$
A = \left(\frac{m \omega}{\pi \hbar} \right)^{1/4}e^{i \varphi (t)}.
$$

The exponential term is not relevant here, but it is the most general solution, so it is worth remembering. Therefore, our solution to $\psi_{0}$ is

$$
\begin{align}
\psi_{0}(x) & = \left(\frac{m \omega}{\pi \hbar} \right)^{1/4}\exp \left(\frac{-m \omega x^{2}}{2 \hbar} \right)\\[1em]
E_{0} & = \frac{\hbar \omega}{2}.
\end{align}
$$

Since, we've found the smallest solution, we can now just apply $\hat{a}_{+}$ $n-$times to find the $n-$th solution, i.e.

$$
\begin{align}
\psi_{n} & = \hat{a}_{+}^{n}\psi_{0}\\
E_{n} & = \hbar \omega (n + 1/2).
\end{align}
$$

Finding the $A_{n}$'s is not bad, at least, not with our knowledge of operators. We present the following system of equations:

$$
\begin{align}
\hat{a}_{+}\psi_{n} & = b_{n}\psi_{n + 1}\\
\hat{a}_{-} \psi_{n} & = c_{n}\psi_{n-1}.
\end{align}
$$

The goal is to find the $b_{n}$ that gives $A_{n}$. To that end, we multiply the two equations:

$$
\begin{align}
\hat{a}_{-}\hat{a}_{+}(\psi_{n}) & = (\hat{a}_{+}\hat{a}_{-}+ \comm{\hat{a}_{-}}{\hat{a}_{+}})\psi_{n}\\
& = \left(\frac{\hat{H}}{\hbar \omega}- \frac{1}{2} + 1\right)\psi_{n}\\
& = \left(\frac{\hat{H}}{\hbar \omega}+ \frac{1}{2} \right)\psi_{n}\\
& = \left[\cancel{\hbar \omega}\left(n + \frac{1}{2} \right)\cdot \frac{1}{\cancel{\hbar \omega}}-\frac{1}{2}+ 1 \right]\psi_{0}\\
& = (n + 1)\psi_{0}.
\end{align}
$$

We can now use the normalization condition,

$$
\int_{-\infty}^{\infty}(\hat{a}_{+}\psi_{n})^{*}(\hat{a}_{+}\psi_{n})\dd{x} = |b_{n}|^{2}\overbrace{\int_{-\infty}^{\infty}\abs{\psi_{n+ 1}}^{2}\dd{x}}^{1}
$$

and the fact that the ladder operators are Hermitian to arrive at

$$
\begin{align}
\abs{b_{n}}^{2}& = \int_{-\infty}^{\infty}(\hat{a}_{+}\psi_{n})^{*} (\hat{a}_{-}\psi_{n}) \dd{x}\\
& = \int_{-\infty}^{\infty}\psi^{*} \underbrace{\hat{a}_{-}\hat{a}_{+}\psi_{n}}_{= (n + 1) \psi_{n}} \dd{x}\\
& = (n + 1) \int_{-\infty}^{\infty}\psi_{n}^{*}\psi_{n}\dd{x} \\
& = (n + 1).
\end{align}
$$

From here it follows that

$$
b_{n} = \sqrt{n + 1}
$$

where we again ignore the complex exponential term, which is *sometimes* relevant, but not here. Going back to our original problem, we now have

$$
\begin{align}
\hat{a}_{+}\psi_{n} & = \sqrt{n + 1}\cdot\psi_{n + 1}\\
\psi_{n + 1} & = \frac{\hat{a}_{+}\psi_{n}}{\sqrt{n + 1}}.
\end{align}
$$

Substituting $n \rightarrow n-1$, we get

$$
\psi_{n} = \frac{\hat{a}_{+}\psi_{n-1}}{\sqrt{n}}.
$$

Rinse and repeat $n-$times, and we finally see that

$$
\psi_{n} = \frac{\hat{a}_{+}^{n}\psi_{0}}{\sqrt{n!}},
$$

and so

$$
A = \frac{1}{\sqrt{n!}}.
$$