---
tags: OE/ALKMAT/Mernoki1 
aliases: ["centrális differencia"]
---
# lemma: centrális differencia
$$f^\prime(x) \approx \dfrac{f(x+h)-f(x-h)}{2h}$$
- $f \in C^3$
- $x,h \in \mathbb{R}$
# lemma: centrális differencia a második derivált kiszámítására
$$f^{\prime \prime}(x) \approx \dfrac{f(x+h)-2*f(x)+f(x-h)}{h^2}$$
- $f \in C^4$
- közelítés hibája $O(h^2)$ nagyságrendű
- $x,h \in \mathbb{R}$