# Irregular-singular Points

Here, at least one solution has an essential singularity. For these, we use a Laurent series with infinite negative powers.

$$
y (x) = \sum\limits_{n =-\infty}^{\infty}a_{n}(x-x_{0})^{n}.
$$

That's all for some reason.

# Method of Dominant Balance

Also known as the Liouville-Green method. We look for solutions of the form

$$
\begin{align}
y (x) & = e^{S (x)}, \\[1 em]
S (x) & \sim \frac{1}{x^{\alpha}} \qc \alpha > 0
\end{align}
$$

Let us do a second order example:

$$
y^{(2)} + P_{1}(x)y^{(1)} + P_{0}(x)y = 0.
$$

If we then substitute our guess here, we get

$$
S'' + (S')^{2} + P_{1}(x)S' + P_{0} = 0.
$$

Let's say $x_{0}= 0$ is our irregular-singular point. Then, for $x \rightarrow x_{0}$, we have

$$
\begin{align}
(S')^{2} & \sim \frac{1}{x^{2 + 2 \alpha}}, \\[1 em]
S'' & \sim \frac{1}{x^{2 + \alpha}},
\end{align}
$$

so clearly $S'' \ll (S')^{2}$ when $x\rightarrow 0$, which means we can drop the $S''$ term. Next, let us set $P_{1}= 0$ and $P_{0}=-x^{-3}$. Then we have, for $x \rightarrow 0$,

$$
\begin{align}
(S')^{2} & \sim \frac{1}{x^{3}} \\[1 em]
S' & \sim \frac{1}{x^{3/2}} \\[1 em]
S & \sim \pm 2 x^{-1/2},
\end{align}
$$

and so

$$
y \sim \exp (\pm 2 x^{-1/2}).
$$

Consider $x > 0$, so that we are approaching $0$ from the right. Then it is clear that our solution $y \ll x^{n}$ for any positive $n$. We call this solution the *subdominant solution*. We don't really care much about this solution, so we shall forget about it for now. The question now is, is there a way to improve the leading approximation? Well, we have

$$
S \sim 2 x^{-1/2},
$$

So we should add another correction term $C (x)$ such that $C (x)\ll x^{-1/2}$ as $x \rightarrow 0$. We then have

$$
\begin{align}
S (x) & = 2 x^{-1/2} + C (x) \\[1 em]
S' (x) & = -x^{-3/2} + C' \\[1 em]
S'' (x) & = \frac{3}{2} x^{-5/2} + C''.
\end{align}
$$

Substituting this into our ordinary differential equation gives

$$
\begin{align}
\frac{3}{2}x^{-5/2} + C'' + (C')^{2}-2 x^{-3/2}C' & = 0 \\[1 em]
C' \ll x^{-3/2} \qc C'' \ll x^{-5/2}\\[1 em]
\frac{3}{2}x^{-5/2} + \cancel{C''} + \cancel{(C')^{2}} - 2 x^{-3/2}C' & = 0.
\end{align}
$$

The crossed out terms are terms that are *more* singular than our leading term. They therefore do not have a major contribution, leading to a much simpler ODE. In this case,

$$
\begin{align}
\frac{3}{2}x^{5/2} & \sim 2 x^{-3/2}C' \\[1 em]
C' & \sim x^{-1} \\[1 em]
C & \sim \ln (x) \ll x^{-1/2}.
\end{align}
$$

Our improved solution is now

$$
S (x) \sim 2 x^{-1/2} + \frac{3}{4}\ln (x).
$$

We can further improve our solution by repeating the process above:

$$
\begin{align}
S (x) = 2 x^{-1/2} + \frac{3}{4}\ln (x) &+ D (x)\qc D (x)\ll \ln(x) \\[1 em]
S'' (x) + (S')^{2}+ x^{-3} & = 0 \\[1 em]
D'' + (D')^{2} + 2 D' x^{3/2}+ \frac{3}{2}D' x^{-1} -\frac{3}{16}x^{-2} & = 0 \\[1 em]
D' \ll x^{-1}\qc D'' \ll -x^{-2} \\[1 em]
-2 D' x^{-3/2}-\frac{3}{16}x^{-1} & \sim 0 \\[1 em]
D' & \sim \frac{-3}{32}x^{-1/2} \\[1 em]
D & \sim \frac{-3}{16}x^{1/2} + d.
\end{align}
$$

Now, we have

$$
y (x) = e^{S (x)} \sim cx^{3/4}\exp (2 x^{-1/2})\omega (x),
$$

where $\omega (x)$ is some series in powers of $1/2$.

$$
\omega (x) = \sum\limits_{n = 0}^{\infty}\omega_{n}x^{n/2}
$$

We call $\exp (2x^{-1/2})$ the controlling factor, and the whole $x^{3/4}\exp (2 x^{-1/2})$ is called the leading behavior. 

We can now put all this into our ODE in $y(x)$ and solve for $\omega$:

$$
\begin{align}
\omega'' + \left(\frac{3}{2x} + \frac{2}{x^{3/2}} \right)\omega'-\frac{3}{16x^{2}} & = 0 \\[1 em]
\sum\limits_{n = 0}^{\infty}\frac{n}{2}\left(\frac{n}{2}-1 \right)\omega_{n}x^{n/2-2} +  \frac{3}{2}\sum\limits_{n = 0}^{\infty}\frac{n}{2}\omega_{n}x^{n/2-2}-2 \sum\limits_{n = 0}^{\infty}\frac{n}{2}\omega_{n}x^{n/2-5/2}
&-\frac{3}{16}\sum\limits_{n = 0}^{\infty}\omega_{n}x^{n/2-2} = 0 \\[1 em]
\frac{n}{2}\left(\frac{n}{2}-1 \right)+ \frac{3n}{4}\omega_{n}-\frac{3}{16}\omega_{n} -(n + 1)\omega_{n + 1} & = 0 \\[1 em]
\omega_{n + 1} & = \frac{\omega_{n}}{16}\frac{(2 n + 1)(2 n + 3)}{n + 1}.
\end{align}
$$

As $n \rightarrow \infty$,

$$
\omega_{n + 1} \approx \frac{n}{4}\omega_{n}\qc a_{n} \approx \frac{n!}{4^{n}}.
$$

If we check the radius of convergence, we see that

$$
\begin{align}
R & = \lim_{n \rightarrow \infty}\abs{\frac{\omega_{n}}{\omega_{n + 1}}} \\[1 em]
& = 0
\end{align}
$$

... So our series diverges everywhere... What do we do? It is now time to fully introduce the idea of

## Asymptotic Series

Two series $f (x)$ and $g (x)$ are consider asymptotically equal at $x \rightarrow x_{0}$ if

$$
\lim_{x \rightarrow x_{0}}\frac{f (x)}{g (x)} = 1.
$$

That is what we mean by $f (x)\sim g (x)$. This also implies that $f (x)-g (x)\rightarrow \infty$ as $x \rightarrow x_{0}$. For example,

$$
\begin{align}
f (x) & = \frac{1}{x}+ \ln (x) \qc g (x) =\frac{1}{x} \\[1 em]
\frac{f (x)}{g (x)} = 1 + \frac{\ln (x)}{x},
\end{align}
$$

and the second term goes to $0$ as $x \rightarrow \infty$.

$f (x)$ is consider asymptotically smaller than $g (x)$ at $x \rightarrow x_{0}$ if

$$
\lim_{x \rightarrow x_{0}}\frac{f (x)}{g (x)} = 0
$$

which is what is meant by $f (x) \ll g (x)$. For example

$$
\ln (x) \ll \frac{1}{x^{\alpha}}\; \forall \; \alpha > 0,
$$

so then $f (x)$ has an asymptotic expansion at $x \rightarrow x_{0}$. That is,

$$
f (x) \sim \sum\limits_{n = 0}^{\infty}a_{n}x^{\alpha n}.
$$

<br>

Recall that

$$
\mathcal{E}_{N} = f (x)-\sum\limits_{n = 0}^{N}a_{n}(x-x_{0})^{\alpha n}
$$

if $\mathcal{E}\underset{x \rightarrow x_{0}}{\ll}(x-x_{0})^{\alpha n}$.

For convergent series, $\mathcal{E}_{N}\rightarrow 0$ for *fixed $x$ and $N \rightarrow \infty$*. For asymptotic series, however, $\mathcal{E}_{N}\rightarrow 0$ for *fixed $N$ and $x \rightarrow x_{0}$*.

### The Use of Asymptotic Series

Asymptotic series give the best approximation for $f (x)$ when we truncate it at the optimal order $N_{\text{opt}}$, which depends on $x$ and is defined as

$$
a_{N_{\text{opt}}}(x-x_{0})^{\alpha N_{\text{opt}}} < a_{N_{\text{opt}}+ 1}(x-x_{0})^{\alpha (N_{\text{opt}}+ 1)}.
$$

This means that our series is should be truncated when the terms start to grow. But why is this so? Let us consider the example above and compute $N_{\text{opt}}$:

$$
\begin{align}
a_{n} & \approx \frac{n}{4}a_{n-1} \\[1 em]
\frac{N_{\text{opt}}}{4}x^{1/2} & \approx 1 \\[1 em]
N_{\text{opt}} & \approx 4 x^{-1/2}.
\end{align}
$$

Let us compute the size of the last term in $\omega_{n}x^{n/2}$. Since

$$
\omega_{n} \approx \frac{n!}{4^{n}} \approx \frac{n^{n}}{4^{n}e^{n}}
$$

as $n \rightarrow \infty$, we have

$$
\begin{align}
x^{N_{o}/2}\cdot \omega_{N_{o}} & \approx \frac{4^{N_{o}}}{N_{o}^{N_{o}}}\cdot \frac{N_{o}^{N_{o}}}{4^{N_{o}}e^{N_{o}}} \\[1 em]
& = e^{-N_{o}} \\[1 em] 
& = e^{-4 x^{-1/2}}.
\end{align}
$$

The corresponding term in $y (x)$ is

$$
e^{2 x^{-1/2}}x^{n/2}\omega_{n}\approx e^{-2 x^{-1/2}},
$$

which is exactly the size of the subdominant solution. Therefore, even if the series *was* convergent, the accuracy would not improve by adding more terms.