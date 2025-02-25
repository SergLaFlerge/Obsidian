Some basic plots:

```tikz
\usepackage{pgfplots}
\begin{document}
\begin{tikzpicture}
\begin{axis}[
    axis lines = center,
    xlabel = {\(x\)},
    ylabel = {\(f(x)\)},
    %legend pos = south east,
    ticks = none,
    color = white,
]
\addplot [
    domain = -4:4, 
    samples = 100, 
    color = cyan,
]
{x^2 - 2*x - 1};
%\addlegendentry{\(x^2 - 2x - 1\)}
\addplot[
	domain = -4:4,
	samples = 100,
	color = green,
]
{-20*exp((-x^2)};
%\addlegendentry{\(20 \cdot e^{-x^2}\)}
\end{axis}
\end{tikzpicture}
\end{document}
```

Piecewise plots:

```tikz
\usepackage{pgfplots}
%\pgfplotsset{compat=1.8}
\begin{document}
\begin{tikzpicture}[
  declare function={
    func(\x)= (\x < -pi/2) * (0)   +
              and(\x >= -pi/2, \x < pi/2) * (pi/2-abs(\x))     +
              (\x >= pi/2) * (0)
   ;
  }
]
\begin{axis}[
  axis x line=middle, axis y line=middle,
  ymin=-5, ymax=5, ytick={-5,...,5}, ylabel=$y$,
  xmin=-5, xmax=5, xtick={-5,...,5}, xlabel=$x$,
  domain=-pi:pi,samples=101,
  color = white
]

\addplot [blue,thick] {func(x)};
\end{axis}
\end{tikzpicture} 
\end{document}
```
3D plots:

```tikz
\usepackage{pgfplots} 
\pgfplotsset{compat=1.16} 
\begin{document} 
\begin{tikzpicture}
\begin{axis}[colormap/viridis, color = white] 
\addplot3[ 
	surf, 
	samples=22, 
	domain=-3:3,
	] 
{exp(-x^2-y^2)*x}; 
\end{axis} 
\end{tikzpicture} 
\end{document} 
```
Commutative Diagrams:

```tikz
\usepackage{tikz-cd}

\begin{document}
\begin{tikzcd}[color = white]
A \arrow[rd, "f \circ g" swap] \arrow[r, "f"] & B \arrow[d,"g"] \\
& C
\end{tikzcd}

% "swap" changes the position of the label if it gets too cluttered.
% row sep and column sep sorta lets you scale by adjusting the distances between 
% your matrix elements. 

\end{document}
```

 > [!examples]-  This is a test :)
 > Now we look inside
 
 > [!abstract]- This is a note
 > we love notes for highlighting examples and proofs and such
 
 > [!proof]- This would be a proof
 > $$
 \begin{align}
 a^{2}+ b^{2}= c^{2}
 \end{align}
>$$

$$
\begin{CD}
\kappa(q) = B_{q}/qB_{q}@< < < B_{q}\\
@AAA @AAA6
\end{CD}
$$