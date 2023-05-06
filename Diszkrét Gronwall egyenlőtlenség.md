---
tags: OE/ALKMAT/Mernoki1 
aliases: ["Gronwall egyenlőtlenség"]
---

# Diszkrét Gronwall egyenlőtlenség
$$\delta_{i+1} \le a_i* \delta_i + \gamma_i$$
egyenlőtlenség megoldása zárt alakban
$$\delta_{n+1} \le \left( \prod_{j=0}^n a_j \right) \delta_0 + \sum_{i=0}^n \left( \prod_{j = i + 1}^n a_j \right) \gamma_i$$
Ahol:
- $n \ge 0$
-   $\delta_i$ az $i$-edik lépésben a [[i-edik pont béli globális hiba|globális hiba]] nagysága
-   $a_i$ az $i$-edik lépésben az úgynevezett stabilitási faktor, amely befolyásolja a hiba növekedését a következő lépésben
-   $\gamma_i$ az $i$-edik lépésben az úgynevezett trunation hiba, amely azért jön létre, mert a numerikus módszerünk csak véges pontossággal képes közelíteni az egzakt megoldást.