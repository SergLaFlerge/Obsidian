# WKB Approximation

Consider the example

$$
\epsilon y'' + Q(x)y = 0,
$$

where $Q (x)$ is an analytic function. We solve this as we solved previous ODEs around singular points:

$$
\begin{align}
y & = \exp \left[\frac{1}{\delta}\sum\limits_{n = 0}^{\infty}\delta^{n}S_{n (x)} \right]\qc \delta \sim \epsilon^{\alpha}, \; \alpha > 0 \\[1 em]
y'  & = \frac{1}{\delta}\exp (\cdots)\sum\limits_{n = 0}^{\infty}\delta^{n}S'_{n} \\[1 em]
y'' & = \frac{1}{\delta^{2}}\exp (\cdots)\left(\sum\limits_{n = 0}^{\infty}\delta^{n}S'_{n} \right)^{2}+ \frac{1}{\delta}\exp (\cdots)\sum\limits_{n = 0}^{\infty}\delta^{n}S''_{n}.
\end{align}
$$

Picking terms as we have before, we have

$$
\frac{\epsilon}{\delta^{2}}(S_{0}')^{2}+ \frac{2 \epsilon}{\delta}S_{0}' S'_{1}+ \frac{\epsilon}{\delta}S_{0}'' = Q (x).
$$

For order $\epsilon^{0}$, we have $\delta = \sqrt{\epsilon}$, meaning

$$
\begin{align}
(S'_{0})^{2}& = Q (x) \\[1 em]
S'_{0} & = \sqrt{Q (x)} \\[1 em]
S_{0} & = \pm \int_{0}^{x}\sqrt{Q (t)}\dd{t}
\end{align}
$$

For order $\epsilon^{1/2}$:

$$
\begin{align}
2 S_{0}' S_{1}' + S''_{0} & = 0 \\[1 em]
S_{1}(x) & = \frac{-1}{4}[\ln (Q)] \\[1 em]
y (x) & \sim \frac{C_{1}}{Q^{1/4}}\exp \left[\frac{1}{\epsilon^{1/2}}\int_{a}^{x}\sqrt{Q (t)}\dd{t} \right] + \frac{C_{2}}{Q^{1/4}}\exp \left[-\frac{1}{\epsilon^{1/2}}\int_{a}^{x}\sqrt{Q (t)}\dd{t} \right],
\end{align}
$$

where both terms are $\order{\epsilon^{1/2}}$. This solution very clearly breaks down at $Q (x)\rightarrow 0$. This value $x_{0}$ for which $Q (x_{0})= 0$ is called the *turning point*.

Consider a single turning point at $x = 0$. Then, say $Q (x)< 0$ for $x < x_{0}$ and $Q (x)> 0$ for $x > x_{0}$. We consider Taylor expand $Q (x)$ around $x_{0}$:

$$
Q (x) = ax + \order{x^{2}}.
$$

The question now is, when does the WKB approximation fail? We have

$$
\sum\limits_{n = 0}^{\infty}\epsilon^{n/2}S_{n}\qc S_{0}\approx \epsilon^{1/2}S_{1}.
$$

This then implies

$$
\begin{align}
S_{1} & \sim \frac{1}{4}\ln (ax) \\[1 em]
S_{o} & \sim \int_{b}^{x}\sqrt{at}\dd{t} \\[1 em]
x^{3/2} & \approx \epsilon^{1/2}\qc \text{for}\; b = 0 \\[1 em]
x & \approx \epsilon^{1/3}.
\end{align}
$$

When $\abs{x}< \epsilon^{1/3}$, our expansion breaks down. However, the linear expansion of $Q (x)$ works exactly  for $\abs{x}\ll1$, so we have two matching regions: $[-1,-\epsilon^{1/3}]$ and $[\epsilon^{1/3}, 1]$.

We now have three regions: Region 1 is $x > \epsilon^{1/3}$, region 2 is $\abs{x}< 1$, and region 3 is $x < \epsilon^{1/3}$. In region 1, we have our exponential WKB solution, region 3 has the oscillatory WKB solution, and finally region 2 has our linearized $Q (x)= ax$ solution.