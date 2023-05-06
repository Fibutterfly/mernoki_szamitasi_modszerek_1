---
tags: OE/ALKMAT/Mernoki1 
aliases:
---
# párosított [[Runge-Kutta]] formulák
Választunk két [[Runge-Kutta]] formulát:
Alacsonyabb [[p-ed rendű konvergenciája az egylépéses módszernek|rendű]]:
- $p$ [[p-ed rendű konvergenciája az egylépéses módszernek|rendű]]
- $y_{n+1} = y_n + h_n* \sum_{i=1}^{m} c_i*k_i$
Magasabb [[p-ed rendű konvergenciája az egylépéses módszernek|rendű]]:
- $p+1$
- $\widehat{y}_{n+1} = y_n +h_n*\sum_{i=1}^m d_i*k_i$

Ez reprezentálható a következő mátrixos formában
![[Pasted image 20230505224751.png]]
ahol:
-   $f(x,y)$: a differenciálegyenlet jobboldala
-   $h_n$: az $n$-edik lépésköz
-   $y_n$: az $n$-edik lépésben kiszámolt numerikus megoldás
-   $k_{i}$: az $i$-edik függvényérték a klasszikus [[Runge-Kutta]] formulában
-   $a_i$, $b_{ij}$: az integrálási pontok és súlyok
-   $c_i$: az integrálási pontok súlyai a klasszikus [[Runge-Kutta]] formulában
-   $d_i$: az integrálási pontok súlyai a magasabb [[p-ed rendű konvergenciája az egylépéses módszernek|rendű]] [[Runge-Kutta]] formulában
# párosított [[Runge-Kutta]] formulák [[x pontbéli lokális hiba|lokális hibája]]
$$T(y(t_n),h_n) \approx h_n \sum_{i=1}^m (d_i - c_i)*k_i$$
- $T: \mathbb{R}\times \mathbb{R} \to \mathbb{R}$ a [[x pontbéli lokális hiba|lokális hiba]] függvény
- $y: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ az egzakt megoldások
- $h_n$ az $n.$ lépéshez tartozó lépésköz
-   $k_{i}$: az $i$-edik függvényérték a klasszikus [[Runge-Kutta]] formulában
-   $c_i$: az integrálási pontok súlyai a klasszikus [[Runge-Kutta]] formulában
-   $d_i$: az integrálási pontok súlyai a magasabb [[p-ed rendű konvergenciája az egylépéses módszernek|rendű]] [[Runge-Kutta]] formulában