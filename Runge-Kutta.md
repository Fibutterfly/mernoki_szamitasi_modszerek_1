---
tags: OE/ALKMAT/Mernoki1 
aliases: [""]
---
# explicit Runge-Kutta
$$
\begin{aligned}
	y_{n+1} &= y_n + h_n \sum_{i=1}^m c_i* k_i \\
	k_1 &= f(x_n,y_n) \\
	k_i &= f \left( x_n + a_i*h_n * y_n + h_n * \sum_{j=1}^{i-1} b_{ij}* k_j \right) &(i = 2, \dots, m)
\end{aligned}
$$
- $c_i$ Az $i$-edik lépés középpontjának elhelyezkedését adja meg a lépésközön belül
	- $\sum_{i=1}^m c_i = 1$ esetén $\phi(x,y,0) = f(x,y)$
- $a_i$ Az $i$-edik lépés időbeli elhelyezkedését adja meg, relatív az aktuális időponthoz.
	- $a_i = \sum_{j=1}^{i-1} b_{ij}$ $(i=2, \dots, m)$
- $k$ Az $f$ függvény értékét adja meg az $i$-edik lépés középpontjában.
- $h \in \mathbb{R}^+$ a lépésközt jelöli
- $y:\mathbb{R} \to \mathbb{R}$ az egzakt megoldások
- $b_{ij}$ Az $i$-edik lépés során az $j$-edik részlépés súlyozását adja meg.
	- $b$: Az intervallum végepontját jelöli.
Megadható mátrix sémában is
![[Pasted image 20230505213446.png]]

# explicit Runge-Kutta és az [[explicit Euler-módszer|explicit euler módszer]] közötti kapcsolat
Felírható az [[explicit Euler-módszer|explicit Euler módszer]] a következő explicit Runge-Kutta sémával:
![[Pasted image 20230505213633.png]]

# explicit Runge-Kutta [[i-edik pont béli globális hiba|globális hibája]]
$$\max_{1 \le i \le N}||e_i|| \le \epsilon$$
Amennyiben létezik olyan, hogy
$$||T(y(t_n), h_n||_\infty \le h_n*\epsilon$$
akkor találhatunk olyan $\widehat{c} \ge 0$ konstanst, hogy
$$\max_{1 \le n \le N-1}||e_i||_\infty \le \widehat{c}\epsilon$$
vagy találhatunk olyan $q$-t is, hogy (gyakrabban használt módszer)
$$||T(y(t_n), h_n)||_\infty \le h_n * \epsilon$$
- $0 \le n \le N-1$
ahol:
- $h$ a lépésköz