# Laplace Method

We start with the Laplace integral from last time:

$$
I (z) = \int_{a}^{b}f (t)\exp[z \varphi (t)]\dd{t}.
$$

Suppose $\varphi (t)$ has a maximum at $t = a$ or $t = b$. Without loss of generality, say the maximum is at $t = a$. The idea is that we will split the integral into two parts:

$$
\begin{align}
I (z) & = I (z, \epsilon) + \delta I = \int_{a}^{a + \epsilon}f (t)\exp[z \varphi (t)]\dd{t} + \int_{a + \epsilon}^{b}f (t)\exp[z \varphi (t)]\dd{t} \\[1 em]
& = \epsilon f (t_{1})\exp[z \varphi (t_{1})] + (b-a-\epsilon)f (t_{2})\exp[z \varphi (t_{2})],
\end{align}
$$

where $t_{1}$ and $t_{2}$ are simply the two intervals marked by the integration bounds. Note that

$$
\varphi (t_{1}) > \varphi (t_{2}) \implies \exp[z \varphi (t)] \gg \exp[z \varphi (t_{2})], 
$$

And so we can actually ignore the $\delta I$ term to a good approximation. Therefore

$$
I (z)\sim I (z, \epsilon).
$$

So now we can consider $\epsilon \rightarrow 0$. Then we can expand in $t-a< \epsilon \ll1$.

$$
\begin{align}
f (t) & = f (a)+ f' (a)(t-a)+ \cdots \\[1 em]
\varphi (t) & = \varphi (a) + \varphi' (a)(t-a)+ \frac{1}{2}\varphi^{(2)}(t-a)^{2}+ \cdots.
\end{align}
$$

Then

$$
\begin{align}
I (z) & \sim f (a) \exp[z \varphi (a)]\int_{a}^{a + \epsilon}\exp[z \varphi' (t-a) ]\dd{t} \\[1 em]
& \sim f (a)\exp[z \varphi (a)]\int_{a}^{b}\exp[z \varphi' (a)(t-a)]\dd{t}\qc s =-z \abs{\varphi' (a)}(t-a) \\[1 em]
& = -\frac{f (a)\exp[z \varphi' (a)]}{z \varphi' (a)}\underbrace{\int_{0}^{z (b-a)\varphi' (a)}e^{-s}\dd{s}}_{\rightarrow 1 \; \text{as}\; z \rightarrow \infty} \\[1 em]
I (z) & \sim \frac{-f (a) \exp[z \varphi (a)])}{z\varphi' (a)}.
\end{align}
$$

If we consider corrections in $1/z$, we have

$$
\begin{align}
\exp[z \varphi (a)]\int_{0}^{\infty}\left[f' (a)(t-a)+ f (a)z \frac{\varphi^{(2)}(a)}{2}(t-a)^{2} \right]\exp[z \varphi' (a)(t-a)]\dd{t} \\[1 em]
& = \frac{\exp[z \varphi (a)]}{z^{2}}\left(\frac{f' (a)}{[\varphi' (a)]^{2}}-\frac{f (a)}{[\varphi' (a)]^{3}} \right), 
\end{align}
$$

which is exactly the same expression we obtained last class using integration by parts.

What happens when our maximum is between $a$ and $b$ instead? For a maximum of $\varphi (c)$ with $a < c < b$, we necessarily have $\eval{\varphi' (t)}_{c}= 0$. We still find that the dominant solution lies in a region $[c-\epsilon, c + \epsilon]$. Then

$$
\begin{align}
I (z) & \sim \int_{c-\epsilon}^{c + \epsilon}f (t)\exp[z \varphi (t)]\dd{t}, \\[1 em]
\abs{t-c} & < \epsilon \ll 1 \\[1 em]
f (t) & = f (c) + f' (c)(t-c) + \frac{1}{2}f^{(2)}(c)(t-c)^{2}+ \cdots \\[1 em]
\varphi (t) & = \varphi (c)+ \cancelto{0}{\varphi'(c)(t-c)}+ \frac{1}{2}\varphi^{(2)}(c)(t-c)^{2}+ \frac{1}{6}\varphi^{(3)}(c)(t-c)^{3}+ \cdots \\[1 em]
I (z )& \sim f (c)\exp[z \varphi (c)]\int_{-\infty}^{\infty}\exp \left[\frac{z \varphi^{(2)}(c)(t-c)^{2}}{2} \right] \dd{t} \\[1 em]
& = \frac{f (c)\exp[z \varphi (c)]\sqrt{2}}{z^{1/2}\abs{\varphi(c)}^{1/2}}\int_{-\infty}^{\infty}e^{-s^{2}}\dd{s} \\[1 em]
& = \frac{f (c) \exp[z\varphi (c)]\sqrt{2 \pi}}{z^{1/2}\abs{\varphi^{(2)}}^{1/2}}
\end{align}
$$

Example: Take our previous Laplace transform for our favorite ODE:

$$
y (x) = \frac{\sqrt{x}}{\pi}\int_{0}^{\pi}\exp \left[\frac{2 \cos \theta}{\sqrt{x}} \right]\cos \theta \dd{\theta}.
$$

Knowing that $x = 0$ is our maximum and making the appropriate substitutions, we obtain

$$
\eval{y (x)}_{x \rightarrow 0, \; z \rightarrow \infty} \sim \frac{x^{3/4}}{2 \pi^{1/2}}\exp \left(\frac{2}{x^{1/2}} \right),
$$

 which is exactly the dominant solution