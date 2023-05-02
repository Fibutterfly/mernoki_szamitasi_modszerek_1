---
tags: OE/ALKMAT/Mernoki1 
aliases: ["kezdetiérték feladatok","kezdeti érték feladat","kezdeti érték feladat"]
---
# Kezdeti érték feladat
## Formája:
$$
\begin{aligned}
	y^\prime =& f(x,y), \\
	y(x_0) =& y_0, \\
\end{aligned}
$$
- $f: \mathbb{R} \times \mathbb{R}^l \to \mathbb{R}^l$
	- $f(x,y) = [f_1(x,y),\dots,f_l(x,y)]^T$
- $x \in \mathbb{R}$
- $y \in \mathbb{R}^l$
## Feltételei
A következő nyílt tartományon:
$$D = \{ (x,y):||x-x_0||_\infty < \kappa_x,||y-y_0||_\infty < \kappa_y\} \subseteq \mathbb{R}^{l+1} $$
folytonos
- $\kappa_x, \kappa_y \in \mathbb{R}^+$
- eleget tesz a [[Lipschitz tulajdonság|Lipschitz]]-feltétel:
	- $||f(x,y)-f(x,z)||_\infty \le L||y-z||_\infty$
		- $L \in \mathbb{R}^+$
## Megoldása
Ha a feltételeknek eleget tesz, akkor pontosan egy megoldása van
$$y(x) = [y_1(x), \dots, y_l(x)]^T$$
- $[x_0,B]$ intervallumon
	- $y^\prime(x) = f(x,y(x))$ $x \in [x_0, B]$