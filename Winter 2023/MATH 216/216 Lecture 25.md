 $f:D \rightarrow \mathbb{R}$, with $D$ an interval and $f$ continuous. Remember that the Mean Value Theorem says something about the behavior of a function between two points. We shall refine this theorem further.

#### Theorem 16

Taylor's Theorem

Let $f:D \rightarrow \mathbb{R}$ be $C^{n}$, and pick $a, b \in D$ with $a \neq b$. Then

$$
\begin{align}
f (b) & = f (a)+ f' (a)(b-a) + \frac{f'' (a)}{2!}(b-a)^{2} + \cdots + \frac{f^{(n-1)}(a)}{(n-1)!}(b-a)^{n-1} + \frac{f^{(n)}(c)}{n!}(b-a)^{n}.
\end{align}
$$

>[! Proof]-
>Consider an auxiliary function $g:D \rightarrow \mathbb{R}$, with
>
>$$
\begin{align}
g (x) & = \sum\limits_{j = 0}^{n-1}\frac{f^{(y)}(x)}{j!}+ d (d-x)^{n}.
\end{align}
>$$
>
>$g$ is differentiable. $g (b)= f (b)$. $g (a)= \sum\limits_{j = 0}^{n-1}\frac{f^{(j)}(a)}{j!}(b-a)^{j}+ d (b-a)^{n}$. We can then choose $d$ so that $g (a)= g (b)$.
>
>$$
\begin{align}
g' (x) & = \sum\limits_{j = 0}^{n-1}\frac{f^{(j + 1)}(x)}{j!}(b-x)^{j} + \sum\limits_{j = 1}^{n-1}\frac{f^{(j)}(x)}{j!}(b-x)^{j-1}(-1)-dn (b-x)^{n-1} \\[1 em]
& = \sum\limits_{j = 1}^{n-1}\frac{f^{(j + 1)}(x)}{j!}(b-x)^{j} + \sum\limits_{j = 0}^{n-2}\frac{f^{(j + 1)}(x)}{j!}(b-x)^{j} -dn (b-x)^{n-1} \\[1 em]
& = \frac{f^{(n)}(x)}{(n-1)!}(b-x)^{n-1} -dn (b-x)^{n-1}.
\end{align}
>$$
>
>Since $g (a)= g (b)$, by lemma 12, $\exists \; c$ strictly between $a, b$ such that $g' (c)= 0$, i.e.
>
>$$
\begin{align}
\frac{f^{(n)}(x)}{(n-1)!}\cancel{(b-c)^{n-1}} & =dn \cancel{(b-c)^{n-1}} \\[1 em]
 d & = \frac{f^{(n)}(c)}{n!}
\end{align}
>$$
>
>And so
>
>$$
\begin{align}
f (b) & = \sum\limits_{j = 0}^{n-1}\frac{f^{(j)}(a)}{j!}(b-a)^{j}+ \frac{f^{(n)}}{n!}(b-a)^{n}.
\end{align}
>$$

Assume $f:D \rightarrow \mathbb{R}$ is $C^{\infty}$, with $a, x \in D$ and $n \in \mathbb{N}$. Then

$$
\begin{align}
f (x) = f (a) + f' (a) (x-a) + \cdots + \frac{f^{(n)}(a)}{n!}(x-a)^{n}+ \frac{f^{(n + 1)}(c)}{(n + 1)!}(x-a)^{n + 1}.
\end{align}
$$

$c$ sits between $a$ and $x$, so it depends on $x, n$ (and $a, f$). The best-case scenario is that

$$
\begin{align}
\abs{\frac{f^{(n + 1)}(c)}{(n + 1)!}(x-a)^{n + 1}}\rightarrow 0
\end{align}
$$

as $n \rightarrow \infty$, at least for $x$ close to $a$, say $x \in (a-\delta, a + \delta)$ for some $\delta > 0$. This polynomial is known as the n-th *Taylor polynomial* of $f$ at $a$, and its corresponding series is its *Taylor series*. In the case where $f$ can be expressed fully by its Taylor series, we say that the function is represented/given by its Taylor series.

Very often, a smooth $f$ is indeed given by its Taylor series at every $a \in D$.

>[! Examples]+ Example 17
>1. Consider $f (x)= (x-1)(x-2)= x^{2}-3 x + 2$. Pick $a =-1$, then
>	$$
\begin{align}
f (-1) & = 6 & f' (x) & = 2 x-3  \\[1 em]
f' (-1) & = -5 & f'' (x) & = 2 \\[1 em]
f'' (-1) & = 2 & f^{(n)}& = 0 \; \forall \; n \geq 3 \\[1 em]
f (x)  = x^{2}-3 x+ 2
\end{align}
>$$
 >2. Consider $g (x)=\frac{1}{f (x)}$, then $D = \mathbb{R}\smallsetminus \set{1, 2}$. In this domain $g$ is smooth. This is an ugly function, but we can rewrite it as $$\begin{align}g (x) &= \frac{-1}{x-1}+ \frac{1}{x-2}= \frac{1}{{1-x}}+ \frac{1}{2-x}\\[1 em]& =\frac{1}{2}\frac{1}{1-\frac{x + 1}{2}} -\frac{1}{{3}} \frac{1}{1-\frac{x + 1}{3}}\\[1 em] & = \frac{1}{2}\sum\limits_{n = 0}^{\infty}\left(\frac{x + 1}{2} \right)^{n}-\frac{1}{3}\sum\limits_{n = 0}^{\infty}\left(\frac{x + 1}{3} \right)^{n}\\[1 em] & = \sum\limits_{n = 0}^{\infty}\left(\frac{1}{2^{n + 1}} - \frac{1}{{3^{n + 1}}} \right)(x + 1)^{n} \end{align}$$
 >	This is the Taylor series at $a =-1$. Note that this is only "good" around $a =-1$ due that the asymptotic behavior of $g (x)$.
 >3. Consider $h (x)= \log (1 +x)$. Here, $$\begin{align}h' (x) & = \frac{1}{1 + x} \\[1 em] h'' (x) & = -\frac{1}{(1 + x)^{2}}\\[1 em] & \vdots \\[1 em] h^{(n)}(x) & = (-1)^{n-1}\frac{(n-1)!}{(1 + x)^{n}}  \end{align}$$ The Taylor series of $h (x)$ at $a = 0$ is then $$\sum\limits_{n = 1}^{\infty}\frac{(-1)^{n + 1}}{n}x^{n}.$$ But how good is this approximation really? Well, for points around $0$ it is still accurate. In fact, for $\abs{x}> 1$, the series does *not* converge!

## Two Final Fun Examples

>[! Examples]+ Example 18
>By Taylor's Theorem for a function $f (x)= \log (1 + x)$,
>
>$$
\begin{align}
f (x) & = \log (1 + 0) + x + \frac{1}{2!}\frac{1}{(1 + c)^{2}}x^{2} \\[1 em]
& = x-\frac{x^{2}}{2 (1 + c)}.
\end{align}
>$$
>
>$c$ will depend on $x$. Take $x= \frac{1}{j}, \; j \in \mathbb{N}$. Then
>
>$$
\begin{align}
\log\left( 1 + \frac{1}{j} \right) & = \frac{1}{j} - \frac{1}{2 j^{2}(1 + c_{j})} \\[1 em]
& = \frac{1}{j}- \frac{\bar{c}_{j}}{j^{2}} \\[1 em]
\log (j + 1)-\log (j) & = \frac{1}{j}- \frac{\bar{c}_{j}}{j^{2}} \\[1 em]
\log (n)-\log (n-1) & = \frac{1}{n-1}- \frac{\bar{c}_{n}}{(n-1)^{2}} \\[1 em]
\log n & = 1 + \frac{1}{2}+ \cdots + \frac{1}{n}-\frac{1}{n}-\sum\limits_{j = 1 }^{n-1} \frac{\bar{c}_{j}}{j^{2}} \\[1 em]
\log n & = \mathrm{H}_{n} -\left(\frac{1}{n}+ \sum\limits_{j = 0}^{n-1} \frac{\bar{c}_{j}}{j^{2}} \right),
\end{align}
>$$
>
>with $\mathrm{H}_{n}$ is the n-th harmonic number and the series above is convergent. Call it $b_{n}$, then
>
>$$
\begin{align}
\log n & = \mathrm{H}_{n}-b_{n} \\[1 em]
\mathrm{H}_{n} & = \log{n}+ b_{n}
\end{align}
>$$

From the above, we can gain many insights without effort!
1. The divergence of the harmonic series. Since $\mathrm{H}_{n}$ is the  n-th harmonic number, the series $\mathrm{H}= \log{n}+ b_{n}$ which goes to infinity as $\log n \rightarrow \infty$.
2. The convergence of the alternating harmonic series. $S_{2 n}= \mathrm{H}_{2 n}-\mathrm{H}_{n}= \log{(2 n)}+ b_{2 n}-\log (2 n)-b_{n}= \log{2}+ \cancel{\log{n}}+ b_{2 n}-\cancel{\log n}-b_{n}$, and so $S_{2 n}$ converges.