# Borel Summation of Asymptotic Series

Last time, we had

$$
\begin{align}
f (x) & = \sum\limits_{n = 0}^{\infty}a_{n}x^{n}\qc a_{n} = 2^{n} \\[1 em]
\sum\limits_{n = 0}^{\infty} (2 x)^{n} & = \frac{1}{1-2 x}\qc R = \frac{1}{2} \\[1 em]
f (1) & = 1 + 2 + 4 + 8 + \cdots \\[1 em]
B (x) & = \frac{1}{1-2 x}\qc B (1) = -1.
\end{align}
$$

What happens when $R = 0$? Take for example $a_{n}= (-1)^{n}n!$. We then have

$$
\begin{align}
f (x) & = \sum\limits_{n = 0}^{\infty}(-1)^{n}n! x^{n}\qc R = 0 \\[1 em]
\varphi (x) & = \sum\limits_{n = 0}^{\infty}\frac{(-1)^{n}\cancel{n!}x^{n}}{\cancel{n!}} \\[1 em]
& = \sum\limits_{n = 0}^{\infty} (-1)^{n}x^{n} \\[1 em]
& = \frac{1}{1 + x}. \\[1 em]
B (x) & = \int_{0}^{\infty}e^{-t}\phi (xt)\dd{t} \\[1 em]
& = \int_{0}^{\infty}\frac{e^{-t}}{1 + xt}\dd{t} \\[1 em]
& = \frac{e^{1/x}}{x}\Gamma \left(0, \frac{1}{x} \right) \\[1 em]
B(1) & = 0.596... \\[1 em]
B (x \rightarrow 0^{+}) & = 1.
\end{align}
$$

We see that the Borel summation works just fine when we have alternating, factorially growing coefficients. Is it the same with just factorially increasing coefficients? Let us take $a_{n}= n!$. Then

$$
\begin{align}
f (x) & = \sum\limits_{n = 0}^{\infty}n! x^{n} \\[1 em]
\varphi (x) & = \frac{1}{1-x} \\[1 em]
B (x) & = \int_{0}^{\infty}\frac{e^{-t}}{1-xt}\dd{t}.
\end{align}
$$

This is all well and good, but we happen to have a pole at $t = 1/x$, and $x > 0$ for this solution, so we can't integrate this directly. To get some answer, we have to use some complex analysis. In particular,

$$
B (x) = \text{PV}\int_{0}^{\infty}\frac{e^{-t}}{1-xt}\dd{t} \pm i \pi e^{-1/x},
$$

where the second term is a residue, and happens to be the subdominant solution. This is only an approximation, so while the Borel summation works perfectly for our alternating series, it is not quite as effective for a non-alternating factorial series of coefficients.

# Asymptotic Expansion of Integrals

Let's go back to our original working example and apply a Laplace transform:

$$
\begin{align}
y^{(2)} -x^{-3}y & = 0 \\[1 em]
y (x) & =
\begin{cases}
\frac{x^{1/2}}{\pi}\int_{0}^{\pi}\exp (2 x^{-1/2}\cos \theta)\cos \theta \dd{\theta}\qc (x > 0) \\[1 em]
\frac{(-x)^{1/2}}{\pi}\int_{0}^{\pi}\exp[2 i (-x)^{-1/2}\cos \theta]\cos \theta \dd{\theta}\qc (x < 0)
\end{cases}
\end{align}
$$

What happens to $y (x)$ as $x \rightarrow 0$? We are interested in the expansion of two types of integrals:

$$
\begin{align}
I_{1}(z) & = \int_{a}^{b}f (t)\exp[z \varphi (t)]\dd{t}\qc \text{(Laplace integral)} \\[1 em]
I_{2}(z) & = \int_{a}^{b}f (t)\exp[iz \varphi (t)]\dd{t}\qc \text{(Generalized Fourier integral)},
\end{align}
$$

where $f (t)$ and $\varphi (t)$ are both real and continuous.

Let's compute the expansion of the first integral of our working example the $x \rightarrow \infty$:

$$
\begin{align}
y (x) & \underset{x \rightarrow \infty}{=}\frac{x^{-1/2}}{\pi}\left[\int_{0}^{\pi}\left(1 + \frac{2}{x^{1/2}}\cos \theta + \frac{2}{x}\cos^{2}\theta + \frac{1}{x^{3/2}}\frac{3}{4}\cos^{3}\theta + \cdots \right) \right]\cos \theta \dd{\theta} \\[1 em]
& = \sum\limits_{n = 0}^{\infty}\frac{x^{1/2}}{n!}\left(\frac{2}{x^{1/2}} \right)^{n}\cdot \frac{1}{\pi}\int_{0}^{\pi}\cos^{n + 1}\theta \dd{\theta}, \; n = 2 k + 1, \; k \in \mathbb{N}_{0} \\[1 em]
& = \sum\limits_{n = 0}^{\infty}\frac{x^{1/2}}{(2 k + 1)!}\left(\frac{2}{x^{1/2}} \right )^{2 k + 1}\cdot \frac{1}{\pi}\int_{0}^{\pi}\cos^{2 k + 2}\theta \dd{\theta} \\[1 em]
& = \sum\limits_{n = 0}^{\infty}\frac{1}{x^{k}}\underbrace{\frac{2^{2 k + 1}}{(2 k + 1)!}\frac{(2 k + 1)!!}{(2 k + 2)!!}}_{a_{k}} \\[1 em]
a_{k} & = \frac{1}{(k + 1)(k^{2})(k-1)^{2}\cdots1} \\[1 em]
a_{k + 1} & = \frac{a_{k}}{(k + 2)(k + 1)} \\[1 em]
y (x)  & \underset{x \rightarrow \infty}{\longrightarrow}A \left(\frac{1}{x}\right),
\end{align}
$$

where $A (1/x)$ is the analytic part of the Frobenius solution.

Now let us do the same for the Laplace integral using integration by parts:

$$
\begin{align}
I_{1}(z) & = \int_{a}^{b}f (t)\exp[z \varphi (t)]\dd{t} \\[1 em]
& = \frac{1}{z}\int_{a}^{b}\frac{f (z)}{\varphi' (t)}\dv{t}[\exp (z \varphi (t))]\dd{t} \\[1 em]
& = \frac{1}{z}\eval{\frac{f (t)}{\varphi' (t)}\exp[z \varphi (t)]}_{a}^{b}-\frac{1}{z}\int_{0}^{b}\dv{t}\left(\frac{f (t)}{\varphi' (t)} \right) \exp[z \varphi (t)]\dd{t} \\[1 em]
& = \frac{1}{z}\eval{\frac{f (t)}{\varphi' (t)}\exp[z \varphi (t)]}_{a}^{b} -\frac{1}{z^{2}}\eval{\dv{t}\left(\frac{f (t)}{\varphi' (t)} \right)\cdot \frac{1}{\varphi' (t)}\exp[z \varphi (t)]}_{a}^{b} + \order{\frac{1}{z^{3}}}.
\end{align}
$$

We can do this indefinitely to get a series in powers of $1/z$. If $\varphi (b)> \varphi (a)$, we may also neglect the terms with $\varphi (a)$s, is $\exp[z (\varphi (b))]\gg \exp[z \varphi (a)]$. As such,

$$
I_{1}(z) = \frac{1}{z}\frac{f (b)}{\varphi' (b)}\exp[z \varphi (b)] \left[1 + \order{\frac{1}{z^{2}}}\right].
$$