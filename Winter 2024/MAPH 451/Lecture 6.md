Let us begin with a famous example: The asymptotic behavior of $n!$ as $n \rightarrow \infty$: Recall that, to make the factorial smooth, we use the Gamma function.

$$
n! = \Gamma (n + 1) = n \Gamma (n).
$$

We need $\Gamma (z)$ at $z \rightarrow \infty$:

$$
\begin{align}
\Gamma (z) & = \int_{0}^{\infty}\frac{e^{-t}}{t}\cdot t^{z}\dd{t} \\[1 em]
& = \int_{0}^{\infty}\frac{\exp (-t + z \ln t)}{t}\dd{t}.
\end{align}
$$

We can now solve this using the Laplace method from last lecture. With $\varphi (t)= \ln t$ and $f (t)= t^{-1}e^{-t}$, $a = 0$, $b = \infty$. Let's make the variable substitution $s = t/z$. Then

$$
\begin{align}
\Gamma (z) & = \int_{0}^{\infty} \frac{\exp[z (-s + \ln s \ln z)]}{s}\dd{s} \\[1 em]
& = z^{z}\int_{0}^{\infty}\frac{\exp[z (-s + \ln s)]}{s}\dd{s}.
\end{align}
$$

Now, $\varphi(s)=-s + \ln s$ and $f (s)= s^{-1}$. Next,

$$
\begin{align}
\varphi' (s) & = -1 + s^{-1} \\[1 em]
\implies \varphi' (1) & = 0,
\end{align}
$$

and so our maximum is now at $s = 1$. From here,

$$
\begin{align}
\varphi'' (s) & = -s^{-2}, & \varphi'' (1) & = -1 \\[1 em]
f (1) & = 1 , & \varphi (1) & = -1,
\end{align}
$$

and so

$$
\begin{align}
\Gamma (z) & \sim z^{z}\frac{\exp[z\varphi (c)]f (c)}{\sqrt{z}}\left(\frac{pi}{\abs{\varphi'' (c)}} \right)^{1/2}\qc c = 1 \\[1 em]
& = \frac{\sqrt{2 \pi}z^{z}e^{-z}}{\sqrt{z}},
\end{align}
$$

and now

$$
n! \sim \sqrt{2 \pi n}\cdot n^{n}e^{-n}.
$$

# Generalized Fourier Integral

$$
I (z) = \int_{a}^{b} f (t)\exp[iz \varphi (t)]\dd{t}.
$$

We can attack this problem using integration by parts as before:

$$
\begin{align}
I (z) &= \eval{\frac{f (t)\exp[iz \varphi (t)]}{iz\varphi' (t)}}_{a}^{b}-\frac{1}{iz}\int_{a}^{b}\dv{t}\left(\frac{f (t)}{\varphi' (t)} \right)\exp[iz \varphi (t)]\dd{t}, \\[1 em]
\varphi' (t) &\neq 0 \in[a, b] \\[1 em]
I (z) &\underset{z \rightarrow \infty}{\sim} z^{-1}.
\end{align}
$$

## Riemann-Lebesgue Lemma

Consider a contribution ought integral of a region near $t = a$, with $t-a \ll 1$. Then

$$
\begin{align}
\varphi (t) & = \varphi (a) + \varphi' (a)(t-a)+ \cdots \\[1 em]
\Re (\exp[iz \varphi (t)]) & \approx \cos[(\varphi (a)+ \varphi (a)(t-a))z] \\[1 em]
& \rightarrow \cos[C_{1}(t-a)+ C_{2}]\qc \rightarrow \infty.
\end{align}
$$

Suppose $\varphi' (c)= 0$ with $C \in[a, b]$. Then we have

$$
\cos[z (\varphi (c)+ 1/2 \varphi'' (c)(t-a)^{2})].
$$

Without loss of generality, assume $c = a$, and $\varphi' (a)= 0$. Then

$$
I (z) = \underbrace{\int_{a}^{a + \epsilon}f (t)\exp[z \varphi (t)]\dd{t}}_{I (z, \epsilon) \gg z^{-1}} + \underbrace{\int_{a + \epsilon}^{b}f (t)\exp[z \varphi (t)]\dd{t}}_{\order{z^{-1}}}.
$$

Taking $\epsilon \rightarrow 0$, we have

$$
\begin{align}
\varphi (t) & = \varphi (a) + \frac{\varphi'' (a)}{2}(t-a)^{2} + \cdots \\[1 em]
f (t) & = f (a)+ \cdots \\[1 em]
I (z) & \underset{z \rightarrow \infty}{\sim}f (a)\exp[iz \varphi (a)]\int_{a}^{\infty}\exp \left[\frac{iz \varphi'' (a)(t-a)^{2}}{2} \right]\dd{t}.
\end{align}
$$

Let $s = t-a$. Then

$$
I (z) \underset{z \rightarrow \infty}{\sim} f (a)\exp[iz \varphi (a)]\int_{0}^{\infty}\exp\left[\frac{iz \varphi'' (a)s^{2}}{2} \right]\dd{s}.
$$

$s$ is defined such that

$$
\begin{align}
(s')^{2} & = \frac{z\varphi'' (a)}{2}s^{2}\qc \varphi'' (a) > 0 \\[1 em]
I (z) & \sim \frac{f (a)\sqrt{2}}{z^{1/2}[\varphi'' (a)]^{1/2}}e^{i \pi/4}\int_{0}^{\infty}\exp[-(s'')^{2}]\dd{s} \\[1 em]
& = \frac{\sqrt{2}f (a)}{z^{1/2}[\varphi'' (a)]^{1/2}}\exp \left(\frac{i \pi}{4} \right)\frac{\sqrt{\pi}}{2} \\[1 em]
& = f (a)\left[\frac{\pi}{2 z \varphi'' (a)} \right]^{1/2}\exp[i (z \varphi (a))+ \pi/4].
\end{align}
$$

In the general case of $\exp[z (i \psi (t)+ \varphi (t))]$, we find a path in the complex $t-$plane where $\psi (t)=$ const.

### Example

Take, as $x \rightarrow 0$,

$$
\begin{align}
y (x) & = \frac{i \abs{x}^{1/2}}{\pi}\int_{0}^{\pi}\exp[2 i \abs{x}^{-1/2}\cos \theta]\cos \theta\dd{\theta} \\[1 em]
z & \rightarrow \abs{x}^{-1/2}\qc t \rightarrow \theta \qc \varphi (t) \rightarrow 2 \cos t \\[1 em]
f (t) & = \cos t \qc a = 0 \qc b = \pi.
\end{align}
$$

Finding the stationary points:

$$
\begin{align}
\varphi' (t) & = 0 \implies-2 \sin t = 0 \\[1 em]
t & = a , \; b \equiv 0, \pi.
\end{align}
$$

Consider $t = \pi$. $\varphi'' (\pi)= 2$, $f (\pi)=-1$, $\varphi (\pi)=-2$. Then

$$
\frac{i \abs{x}^{1/2}}{\pi}\abs{x}^{1/4}\exp[-2 i \abs{x}^{-1/2}+ i \pi/4]\sqrt{\frac{\pi}{4}}.
$$

For $t = 0$, we then get

$$
\begin{align}
y (x) \underset{x \rightarrow 0^{-}}{\sim}\frac{\abs{x}^{3/4}}{\sqrt{\pi}}\cos \left(2 \abs{x}^{-1/2} + \frac{\pi}{4}\right)
\end{align}
$$