---
tags: OE/ALKMAT/Mernoki1 
aliases: ["lokális hiba", "lokális hibájára", "lokális hibára", "x pontbéli lokális hibája","lokális hibája"]
---
# x pontbéli lokális hiba
$$T(y(x),h)=y(x+h)-(y(x)+h*f(x,y(x)))$$
# x pontbéli lokális hiba nagysága
$$|T(y(t_i),h_i)| \le K_2 h_i^2$$
és
$$||T(y(x),H||_\infty \le K_2 h^2 $$
- $x,x+h \in [x_0b]$
- Ahol $2K_2 = \max_{1 \le i \le l} \max_{x \in [x_0,b]} |y_i^{\prime \prime}(x)|$
	- [[Lipschitz tulajdonság|Lipschitz állandó]] másodrendű változata
A lokális hiba függvényről a következőt tudjuk:
$$\begin{aligned}
T(y(x), h) =& (y(x) + h * y^\prime(x) + R_1(x,h))\\
&- (y(x) + h* \overbrace{f(x,y(x))}^{y^\prime(x)}) \\
 =& R_1(x,h)
\end{aligned}
$$
- $R_1(x,h)$ a Taylor-sorfejtés első nem nulla tagja
A megoldásról a következőt tudjuk:
$$y(x+h) = y(x) + h *y^\prime(x) + R_1(x,h)$$
- $y(x) \in C^2[x_0,b]$
Ekkor teljesül, a maradék ragra, hogy
$$||R_1(x,h)||_\infty \le h^2 K_2$$
