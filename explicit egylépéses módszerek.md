---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/05tétel 
aliases: ["explicit egylépéses módszer", "explicit egylépéses"]
TARGET DECK: 02::MSZM1
---
# explicit egylépéses módszerek
$$y_{i+1} = y_i + h_i \phi(t_i, y_i, h_i)$$
- $\phi: \mathbb{R} \times \mathbb{R}^l \times \mathbb{R} \to \mathbb{R}^l$
	- $||\phi(x,y,h) - \phi(x,z,h)||_\infty \le K||y-z||_\infty$
	- $\phi(x,y,0) = f(x,y)$
- $x \in \mathbb{R}$
- $h \in \mathbb{R}$ lépésköz
- $y \in \mathbb{R}^l$
- $K$ A másodrendű [[Lipschitz tulajdonság|Lipschitz állandó]]

# kapcsolat az explicit egylépéses módszerek és az [[explicit Euler-módszer|explicit Euler módszer]] között
Lényegében a $\phi(x,y,h)=f(x,y)$-nak felel meg

# explicit egylépéses módszerek [[x pontbéli lokális hiba|x pontbéli lokális hibája]]
$$T(y(x),h) = y(x+h) - (y(z)+h*\phi(x,y(x),h))$$
- $T$ a hiba függvény $T: \mathbb{R}^l \times \mathbb{R} \to \mathbb{R}$
- $y \in \mathbb{R}^l$ eredményfüggvény
- $h \in \mathbb{R}$ lépésköz
- $\phi: \mathbb{R} \times \mathbb{R}^l \times \mathbb{R} \to \mathbb{R}$ közelítő függvény

# explicit egylépéses módszer [[i-edik pont béli globális hiba|i-edik pont béli globális hibájára]] vonatkozó összefüggés
$$||e_{i+1}|| \le (1+ h_i *K)*||e_i||+||T(y(t_i),h_i)||$$
- $e_i \in \mathbb{R}^+$ az [[i-edik pont béli globális hiba]]
- $h_i \in \mathbb{R}^+$ az $i$-edik ponthoz tartozó lépésköz
- $K$ az $\phi$ függvény [[Lipschitz tulajdonság|Lipschitz állandója]], azaz $||\phi(t,y,h)-\phi(t,z,h)||\leq K||y-z||$
- $T : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ a hibafüggvény
- $y: \mathbb{R} \to \mathbb{R}$ az egzakt megoldások

# kártya
START
Basic
Front:
Explicit egylépéses módszerek
Back:
$$y_{i+1} = y_i + h_i \phi(t_i, y_i, h_i)$$
- $\phi: \mathbb{R} \times \mathbb{R}^l \times \mathbb{R} \to \mathbb{R}^l$
	- $||\phi(x,y,h) - \phi(x,z,h)||_\infty \le K||y-z||_\infty$
	- $\phi(x,y,0) = f(x,y)$
- $x \in \mathbb{R}$
- $h \in \mathbb{R}$ lépésköz
- $y \in \mathbb{R}^l$
- $K$ A másodrendű [[Lipschitz tulajdonság|Lipschitz állandó]]
<!--ID: 1686769683020-->
END