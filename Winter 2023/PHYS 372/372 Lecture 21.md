 Griffiths Example 4.1 and Example 4.2.1

Let us look at the radial equation:

$$
\begin{align}
\pdv{r}\left(r^{2}\dv{R}{r} \right)-\frac{2 mr^{2}}{\hbar^{2}}\left(V (r)-E \right)R & = l (l + 1)R
\end{align}
$$

We will introduce a new function $u (r)= rR (r)$. Our normalization condition is then changed to

$$
\int_{0}^{\infty}\abs{u (r)}^{2}\dd{r}= 1.
$$

Substituting $u (r)$ into the radial equation gives

$$
\begin{align}
\frac{-\hbar^{2}}{2m}\dv[2]{u (r)}{r} + \left[V (r) + \frac{\hbar^{2}}{2m}\frac{l (l + 1)}{r^{2}} \right]u (r) = Eu (r).
\end{align}
$$

The middle term is really our potential now,

$$
V_{\text{eff}} = V (r) + \frac{\hbar^{2}l (l + 1)}{2mr^{2}},
$$

and if we compare this to classical mechanics, the last term of the potential is analogous to $\frac{L^{2}}{2mr^{2}}$. Therefore $L^{2}= \hbar^{2}l (l + 1)$.

So, in 3-D quantum mechanics, the time independent radial Schrödinger equation actually gives us an effective potential that encapsulates the angular momentum! This is the reason that angular momentum is quantized. Let's do some problems now

# Infinite Spherical Well

This time we have

$$
V (r) =
\begin{cases}
0 \qc &r < a \\
\infty \qc &r \geq a
\end{cases}.
$$

From here

$$
\begin{align}
\dv[2]{u (r)}{r} = \left[\frac{l (l + 1)}{r^{2}} -\underbrace{\frac{2mE}{\hbar^{2}}}_{= k^{2}} \right]u (r).
\end{align}
$$

We have two cases:

## $l = 0$

$$
\begin{align}
\dv[2]{u}{r} & = -k^{2}u \\[1em]
u (r) & =  A_{r}\sin (kr) + B_{r}\cos (kr)
\end{align}
$$

Since there is no potential at $r = 0$, we need another boundary condition saying $u = rR (r)\rightarrow 0$ as $r \rightarrow 0$. With this condition we get rid of the $\cos$ term.

$$
u (r) = A_{r}\sin{kr}.
$$

At $r = a$, we want $u (a)= 0$, which implies

$$
\begin{align}
A_{r}\sin(kr) & = 0 \\
A_{r} \sin(ka) & = 0 \\
k & = \frac{n \pi}{a}.
\end{align}
$$

Therefore our solution is

$$
u (r) = A_{r}\sin \left(\frac{n \pi x}{a} \right).
$$

Then

$$
E_{n, 0} = \frac{n^{2}\pi^{2}\hbar^{2}}{2ma^{2}}.
$$

The last step is finding $A_{r}$ by using the normalization condition. It is surprisingly similar to our infinite square well:

$$
\begin{align}
\int_{0}^{\infty}\abs{R (r)}^{2}r^{2}\dd{r} & = 1 \\[1em]
A_{r} & = \left(\frac{2}{a} \right)^{1/2}.
\end{align}
$$

Finally, we have

$$
\begin{align}
\Psi_{nlm}(r, \theta, \phi) \leftrightarrow \ket{nlm}\\[1em]
\Psi_{n00}(r, \theta, \phi) & = R_{n0}Y_{0}^{0}(\theta, \phi) \\[1em]
& = R_{n0}\left(\frac{1}{4 \pi} \right)^{1/4} \\[1em]
& = \frac{\sin (kr)}{r \sqrt{2 \pi a}}
\end{align}
$$

This was the easy solution. The next solution is much more interesting:

## $l \neq 0$

Now we have an extra term, so our differential equation is a little more complicated.

$$
u (r) = A_{r}j_{l}(kr) + B_{r}\eta_{l}(kr),
$$

where $j_{l}$ is known as the spherical Bessel function, and $\eta_{l}$ is the spherical Neumann function. Our energy quantization then becomes

$$
E_{nl} = \frac{\hbar^{2}}{2ma^{2}}B_{nl}^{2}.
$$

That is all the detail we can provide, since the Bessel functions are not analytic.



# The Hydrogen Atom

We will assume that our atom is infinitely heavy so that it does not bounce around. We have one electron bound to the nucleus, and we want to see what happens.

$$
V (r) = \frac{-e^{2}}{4 \pi \epsilon_{0}}\cdot \frac{1}{r}.
$$

Since we only care about the bound states, we will only look at the case $E < 0$. Because the potential depends only on the radius, we can use our radial equation from the previous problem to solve this one. We have

$$
\begin{align}
\dv[2]{u}{r} & = \left[\frac{l (l + 1)}{r^{2}} -\frac{2mE}{\hbar^{2}} \right]u (r).
\end{align}
$$

To get a real, positive answer, we let $k = \frac{\sqrt{-2mE}}{\hbar}$. We introduce a new variable $\rho = kr$, with

$$
\rho_{0} = \frac{me^{2}}{2 \pi \epsilon_{0}\hbar k}.
$$

We now have a different radial equation that looks like

$$
\dv[2]{u}{\rho} = \left[1-\frac{\rho_{0}}{\rho} + \frac{l (l + 1)}{\rho^{2}} \right]u.
$$

We will explore two cases, $\rho \rightarrow 0$ and $\rho \rightarrow \infty$.