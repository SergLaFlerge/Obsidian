For $D \subset \mathbb{R}$ and $f:D \rightarrow \mathbb{R}$ continuous, there is one last theorem we would like to explore: The inverse of a function.

#### Theorem 28

Let $D \subset \mathbb{R}$ be an interval, and $f:D \rightarrow \mathbb{R}$ continuous. If $f$ is 1-1 then $f^{-1}:\mathbb{R}\rightarrow D$ is continuous; Moreover, $f^{-1}$ is strictly increasing (or decreasing) precisely if $f$ increasing (or decreasing).

>[! Proof]
>$f (D)$ is an interval by Theorem 24. $f$ is strictly monotone by proposition 27. Assume $f$ is strictly increasing.
>Pick any $y\in f (D)$. Given $\epsilon > 0$, consider $[x-\epsilon, x + \epsilon]$, and assume that $x \in D^{\circ}$. If $x$ is the left or right endpoint of $D$, then consider only $[x, x + \epsilon]$ or $[x-\epsilon, x]$ respectively. Let $\delta = \frac{1}{2}\min \set{f (x + \epsilon)-f (x), f (x)-f (x-\epsilon)}> 0$. Then, $y + \delta \leq y + \frac{n (x + \epsilon)-f (x)}{2}= \frac{f (x + \epsilon)+ f (x)}{2}< f (x + \epsilon)$ and $y-\delta \geq y-\frac{f (x)-f (x-\epsilon)}{2} = \frac{f (x)+ f (x-\epsilon)}{2}> f (x-\epsilon)$. Therefore $y \in f (D)$ and $f^{-1}$ is continuous on $f (D)$. For $x_{1}, x_{2}\in D$, we have $x_{1}< x_{2}\Leftrightarrow f (x_{1}< f (x_{2}))$. Therefore $f^{-1}$ is increasing.

#### Remark 29

In Theorem 28, the conclusion may fail, i.e. $f^{-1}:D \rightarrow \mathbb{R}$ is *not* continuous, if $D$ is not an interval or $f$ is not continuous. Similarly, in proposition 27 $2 \implies 1$ may be false without these assumptions.

Midterm Time