---
tags: OE/ALKMAT/Mernoki1 
aliases: ["p-ed rendű konvergencia","rend","rendje","rendű"]
---
# p-ed rendű [[konvergencia|konvergenciája]] az egylépéses módszernek
$$||T(y(x),h)|| \le d_p*h^{p+1}$$
- $T: \mathbb{R}^l \times \mathbb{R} \to \mathbb{R}$ a hibafüggvény
- $y: \mathbb{R} \to \mathbb{R}$ az exact megoldás
- $h \in \mathbb{R}^+$ lépéshossz
- $x, x + h \in [x_0,b]$ 
- ha létezik olyan $d_p > 0$
- $b$ az intervallum vége
- ==wiki szerint:== Ha egy Runge-Kutta 4-ed rendű, akkor a hiba max $10^{-3}$
# p-ed rendű egylépéses módszernek a hibája
$$\max_{1 \le i \le N}||e_i|| \le e^{K(b-a)} \left( ||e_0|| + (b-x_0)* d_p \left( \max_{0 \le i \le N-1}h_i \right)^p \right)$$