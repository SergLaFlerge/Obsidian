# Lecture 19

Only taking notes for whiteboard ramblings, other notes are given out as well, for the most part.

# Guided Waves

Waveguides:

- Confine EM waves
- Confined are not generally transverse
-  May have longitudinal $E$ or $B$ components
- Boundary conditions determine who waves are allowed
- there may be a cut-off frequency $\omega_{c}$ where $\omega < \omega c$ can't propagate in the waveguide (depending on the type of waveguide).

A common example is optical fiber cable, which is used for internet. It is composed of two glass cylinders with one inside the other, where the inner core has a greater index of refraction, causing total internal reflection. Another is a dielectric slab waveguide, where we instead have a slab causing total internal reflection. Both of these are examples of dielectric waveguides. We will not be discussing these guides in this course, but they are worth mentioning.

Metallic waveguides will be the ones we will be focusing on here. These have hollow cores and look like parallel plates or rectangles. These rectangular waveguides will be a main focus in this course. We may also have circular waveguides, or coaxial waveguides.

## Boundary Conditions

The boundary conditions for a hollow core metallic waveguide are

$$
\begin{align*}
E^{\parallel}&= 0 \\[1 em]
B^{\perp} &= 0
\end{align*}
$$

These imply that $E \approx 0$ inside the metal. Because of this, we have

$$
\begin{align}
\nabla \times \vec{E} & = \pdv{\vec{B}}{t}
\end{align}
$$

And so $\vec{B}= 0$ inside, as long as we started with $B = 0$. Next

$$
\begin{align}
D_{1}^{\perp}-D_{2}^{\perp} & = \sigma_{f}\implies E_{1}^{\perp}= \frac{\sigma_{f}}{\epsilon_{0}} \\[1 em]
\vec{E}_{1}^{\parallel}-\vec{E}_{2}^{\parallel} & = 0 \implies E_{1}^{\parallel}= 0 \\[1 em]
B_{1}^{\perp}-B_{2}^{\perp} & = 0 \implies B_{1}^{\perp}= 0 \\[1 em]
\vec{B}_{1}^{\parallel}-\vec{B}_{2}^{\parallel} & = \mu_{0}\vec{K}_{f}\times \hat{n}.
\end{align}
$$

## Example

Problem 9.29:

Rectangular waveguide with dimensions $2.28 \times 1.01$cm. What TE modes will propagate in this waveguide if the driving frequency is $17$GHz? Suppose you wanted to excite only one TE mode; what range of frequencies would you use? What are the corresponding wavelengths in open space?

$$
\begin{align}
\nu_{mn} & = \frac{\omega_{mn}}{2 \pi} = \frac{c}{2}\sqrt{\left(\frac{m}{a} \right)^{2}+ \left(\frac{n}{b}\right)^{2}}. \\[1 em]
\nu_{10} & = \frac{c}{2 a} = 6.58\; GHz \\
\nu_{2 0} & =...
\end{align}
$$

You will find that, at $17$GHz, there are only four modes that can occur: $TE_{10}, \; TE_{2 0}, \; TE_{01}, \; TE_{11}$