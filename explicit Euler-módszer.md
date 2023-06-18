---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/05tétel 
aliases: ["explicit Euler módszer"]
TARGET DECK: 02::MSZM1
---
# explicit Euler-módszer
## alapgondolata
- $t_1 = t_0 + h_0$ pontban közelítjük az elméleti megoldást a megoldásgörbe $(x_0,y_0)$ pontbéli érintőjével
- [[Cauchy-feladat]] analógiájára
	- $y(t_0 + h_0) \approx y_0 + h_0y^\prime(t_0) = y_1 = y_0 + h_0 * f(t_0, y_0)$
- és ezután $y_{i+1} = y_i + h_i*f(t_1, y_i)$

# explicit Euler-módszer [[i-edik pont béli globális hiba|globális hibájára]] vonatkozó tétel
$$\max_{1 \le i \le N} ||e_i||_\infty \le (b - x_0) K_2 e^{L(b-x_0)} \max_{0 \le i \le N-1} h_i $$
- $e_i$ a [[i-edik pont béli globális hiba|globális hiba]]
	- $e_0 = y_0 - y(x_0) = 0$
- $y$ a függvény, ami dolgozunk
	- $y(x) \in C^2 [x_0, b]$
- $b$ az intervallum vége
- $x \in \mathbb{R}$
- $K_2$ [[Lipschitz tulajdonság|Lipschitz állandó]] második rendű változata
- $L$ [[Lipschitz tulajdonság|Lipschitz állandó]]
- $h_i$ a lépésköz

# explicit Euler-módszer konvergenciája
A globális hibára vonatkozó tétel szerint a legnagyobb hiba a lépéshosszal arányos, tehát ha
- végtelenül kicsire osztom a lépés közöket
	- $N \to \infty$
	- $\max_{0 \le i \le N} h_i \to 0$,
akkor fennáll, hogy
$$\max_{1 \le i \le N}||e_i||_\infty \to 0$$
tehát elsőrendűben [[konvergencia|konvergens]] a módszer

# kártyák
START
Basic
Front:
explicit Euler-módszer
Back:
## alapgondolata
- $t_1 = t_0 + h_0$ pontban közelítjük az elméleti megoldást a megoldásgörbe $(x_0,y_0)$ pontbéli érintőjével
- [[Cauchy-feladat]] analógiájára
	- $y(t_0 + h_0) \approx y_0 + h_0y^\prime(t_0) = y_1 = y_0 + h_0 * f(t_0, y_0)$
- és ezután $y_{i+1} = y_i + h_i*f(t_1, y_i)$
<!--ID: 1686769730574-->
END