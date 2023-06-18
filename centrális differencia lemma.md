---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/07tétel 
aliases: ["centrális differencia"]
TARGET DECK: 02::MSZM1
---
# lemma: centrális differencia
$$f^\prime(x) \approx \dfrac{f(x+h)-f(x-h)}{2h}$$
- $f \in C^3$
- $x,h \in \mathbb{R}$
- hibája: $O(h^2)$

#Galántai/mérnöki_jegyzet 
# lemma: centrális differencia a második derivált kiszámítására
$$f^{\prime \prime}(x) \approx \dfrac{f(x+h)-2*f(x)+f(x-h)}{h^2}$$
- $f \in C^4$
- közelítés hibája $O(h^2)$ nagyságrendű
- $x,h \in \mathbb{R}$

#Galántai/mérnöki_jegyzet 

# kártyák
START
Basic
Front:
centrális differencia
Back:
$$f^\prime(x) \approx \dfrac{f(x+h)-f(x-h)}{2h}$$
- $f \in C^3$
- $x,h \in \mathbb{R}$
- hibája: $O(h^2)$
<!--ID: 1686774618994-->
END
START
Basic
Front:
centrális differencia a második derivált kiszámítására
Back:
$$f^{\prime \prime}(x) \approx \dfrac{f(x+h)-2*f(x)+f(x-h)}{h^2}$$
- $f \in C^4$
- közelítés hibája $O(h^2)$ nagyságrendű
- $x,h \in \mathbb{R}$
<!--ID: 1686774684519-->
END