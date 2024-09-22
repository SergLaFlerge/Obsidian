# Optimal Truncation Order $N_{opt}$

For our previous solutions, we have

$$
a_{n} \approx \frac{n!}{4^{n}}\qc a_{n}\underset{n\rightarrow \infty}{\approx} \frac{n}{4}a_{n-1}.
$$

At $N_{opt}$, which we shall just call $N$, we have

$$
\begin{align}
\frac{n}{4}x^{1/2} & \approx 1 \\[1 em]
x^{1/2} & \approx \frac{4}{n} \\[1 em]
X^{N/2} & \approx \frac{4^{N}}{N^{N}}.
\end{align}
$$

Let us estimate the size of the term at $N$ for $x^{1/2}\omega_{n}$:

$$
\begin{align}
\omega_{n} & \approx \frac{n!}{4} \\[1 em]
& \approx \frac{n^n}{4^{n}e^{n}}. \\[1 em]
x^{N/2} \omega_{N} & \approx \frac{\cancel{4^{N}}}{\cancel{N^{N}}}\cdot \frac{\cancel{N^{N}}}{\cancel{4^{N}}e^{N}} \\[1 em]
& = e^{-N} \\[1 em]
& = \exp (-2 x^{-1/2}),
\end{align}
$$

which is exactly the size of the subdominant solution.

# Singular Points at $\infty$

To deal with singular points at infinity, we simply make a change of variables $x \rightarrow 1/t$, and take $t \rightarrow 0$. First, we point out some useful relations:

$$
\begin{align}
\dv{x} & = \dv{t}{x}\dv{t} = -t^{2}\dv{t} \\[1 em]
\dv[2]{x} & = t^{4}\dv[2]{t} + 2 t^{3}\dv{t}.
\end{align}
$$

Let us apply this to our working example:

$$
\begin{align}
y^{(2)} -x^{-3}y & = 0 \qc x \rightarrow \infty \\[1 em]
\left(t^{4}\dv[2]{t}+ 2 t \dv{t} \right)y (t) -t^{3}y (t) & = 0 \\[1 em]
y^{(2)}(t) + 2 t^{-1}y^{(1)}(t) -t^{-1}y (t) & = 0 \\[1 em]
\end{align}
$$

$$
\begin{align}
y_{1} & = \sum\limits_{n = 0}^{\infty}a_{n}t^{n}\qc a_{0}= 1 \;, a_{1} = 1/2, \cdots \\[1 em]
y_{2} & = \ln (t)\sum\limits_{n = 0}^{\infty}a_{n}t^{n}+ t^{-1}\sum\limits_{n = 0}^{\infty}b_{n}t^{n}\qc b_{0}= 1 \;, b_{1} =-1, \cdots.
\end{align}
$$

Let us take a linear combination $C_{1}y_{1}(1/x)+ C_{2}y_{2}(1/x)$ such that it matches $y_{as}(x)\sim C \exp (2 x^{1/2}+ \cdots)$ as $x \rightarrow 0$.

$$
\begin{align}
C_{1} & = 2[K_{1}(2)+ \gamma_{E}I_{2}(2)] \\[1 em]
C_{2} & = I_{2}(2) \\[1 em]
C & = \frac{K_{2}(2)}{\sqrt{\pi}}.
\end{align}
$$

We will learn how to find these coefficients later in the course.

# Oscillating Asymptotic Solution

So far, we've only found solution for $x > 0$, but we wish to find solution for $x < 0$ as well, to have a complete understanding of the system. To find these solutions as $x \rightarrow 0^{-}$, we taking the following substitution:

$$
\pm x^{-1/2} \rightarrow \pm i (-x)^{-1/2}\qc \ln (x) \rightarrow \ln (-x).
$$

Then

$$
\begin{align}
y_{1}(x) & \sim C_{1}(-x)^{3/4}\sin (2 (-x)^{-1/2})\omega_{1}(x), \\[1 em]
y_{2}(x) & \sim C_{2}(-x)^{3/4}\cos (2 (-x)^{-1/2})\omega_{2}(x)
\end{align}
$$

# Borel Summation of Asymptotic Series

Suppose we have

$$
f (x) \sim \sum\limits_{n = 0}^{\infty}a_{n}x^{n}\qc R = 0.
$$

Consider the formal number series (x = 1)

$$
S = \sum\limits_{n = 0}^{\infty}a_{n},
$$

and let us introduce the Borel transform:

$$
\varphi (x) = \sum\limits_{n = 0}^{\infty}\frac{a_{n}}{n!}x^{n}
$$

as well as the inverse Borel transform:

$$
B (x) = \int_{0}^{\infty}e^{-t}\varphi (xt)\dd{t}.
$$

If we substitute this series for $\varphi (xt)$, we have

$$
\begin{align}
B (x) & = \int_{0}^{\infty}e^{-t}\sum\limits_{n = 0}^{\infty}\frac{a_{n}}{n!}x^{n}t^{n}\dd{t} \\[1 em]
& = \sum\limits_{n = 0}^{\infty}a_{n}x^{n},
\end{align}
$$

for $B (x)= f (x)$ and $B (1)= S$. If this $B (x)$ exists, i.e. there is a convergent series, we call this the Borel sum of $\sum\limits a_{n}x^{n}$.

Example: Take

$$
\sum\limits_{n = 0}^{\infty}2^{n}.
$$

Here, we have

$$
\begin{align}
\varphi (x) & = \sum\limits_{n = 0}^{\infty}\frac{(2 x)^{n}}{n!} \\[1 em]
& = e^{2 x},
\end{align}
$$

so the sum converges. Then

$$
\begin{align}
B (x) & = \int_{0}^{\infty}\exp (-t + 2 tx)\dd{t} \\[1 em]
& = \frac{1}{1-2 x}.
\end{align}
$$

If we then evaluate this at $x = 1$, we get

$$
\eval{\frac{1}{1-2 x}}_{x = 1} = -1.
$$

We can then introduce an $f (x)$ such that

$$
f (1) = \sum\limits_{n = 0}^{\infty}2^{n}.
$$