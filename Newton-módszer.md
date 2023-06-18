---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/04tétel 
aliases: ["newton módszer"]
TARGET DECK: 02::MSZM1
---
# Newton-módszer
$$\begin{align}
	y - f(x_i) = f^\prime(x_i)*(x-x_i) \tag{NM.1} \\
	x_{i+1} = x_i - \dfrac{f(x_i)}{f^\prime(x_i)} \tag{NM.2}
\end{align}$$
- $f: \mathbb{R} \to \mathbb{R} \in C^\infty$
- Az `(NM.2)` az $y=0$ egyenlet megoldása
- a módszer lényege, hogy a függvényhez érintőt húzunk és a zérushelye adja meg a keresett gyök $i+1$. közelítését

#Galántai/mérnöki_jegyzet 

# kapcsolat a Newton-módszer és a [[Fixpont iterációs módszer|fixpont iterációs eljárás]] között

A newton módszer felírható a
$$x = x - f(x)/f^\prime(x)$$
[[Fixpont iterációs módszer|fixpont iterációs feladatként]]

#Galántai/mérnöki_jegyzet 

# Newton-módszer konvergenciája
$$|x_{i+1}-x^*| \le \dfrac{\gamma}{2* \rho}*|x_i-x^*|^2$$
- $f: (a,b) \to \mathbb{R}$ kétszer folytonosan differenciálható
- $\gamma \ge |f^{\prime \prime}(x)|$
- $|f^\prime(x)| \ge \rho > 0$
- $x^*$ az $f(x)=0$ gyöke a $[a,b]$-n
- Ha ezek mind teljesülnek van olyan $\eta > |x_0 - x^*|$  szám, aminél $x_i \to x^*$
#Galántai/mérnöki_jegyzet 

# Newton-módszer másodrendű konvergenciája
![[Pasted image 20230330233431.png]]
![[Pasted image 20230330233443.png]]
#Galántai/mérnöki_jegyzet 
# Newton-módszer kilépési feltételei
![[Pasted image 20230330234227.png]]
#Galántai/mérnöki_jegyzet 

# Newton-módszer $f \in C^2$-ben
![[Pasted image 20230330234353.png]]
#Galántai/mérnöki_jegyzet 

# Newton módszer több dimenzióban
![[Pasted image 20230330234701.png]]
![[Pasted image 20230330234724.png]]
Jacobi-s alakot nem használjuk!
#Galántai/mérnöki_jegyzet 

# Newton módszer egyenletrendszerekre
![[Pasted image 20230330234912.png]]
#Galántai/mérnöki_jegyzet 


# kártya
START
Basic
Front:
Newton-módszer
Back:
$$\begin{align}
	y - f(x_i) = f^\prime(x_i)*(x-x_i) \tag{NM.1} \\
	x_{i+1} = x_i - \dfrac{f(x_i)}{f^\prime(x_i)} \tag{NM.2}
\end{align}$$
- $f: \mathbb{R} \to \mathbb{R} \in C^\infty$
- Az `(NM.2)` az $y=0$ egyenlet megoldása
- a módszer lényege, hogy a függvényhez érintőt húzunk és a zérushelye adja meg a keresett gyök $i+1$. közelítését
<!--ID: 1686765106921-->
END

START
Basic
Front:
kapcsolat a Newton-módszer és a [[Fixpont iterációs módszer|fixpont iterációs eljárás]] között
Back:
A newton módszer felírható a
$$x = x - f(x)/f^\prime(x)$$
[[Fixpont iterációs módszer|fixpont iterációs feladatként]]
<!--ID: 1686765106929-->
END

START
Basic
Front:
Newton-módszer konvergenciája
Back:
$$|x_{i+1}-x^*| \le \dfrac{\gamma}{2* \rho}*|x_i-x^*|^2$$
- $f: (a,b) \to \mathbb{R}$ kétszer folytonosan differenciálható
- $\gamma \ge |f^{\prime \prime}(x)|$
- $|f^\prime(x)| \ge \rho > 0$
- $x^*$ az $f(x)=0$ gyöke a $[a,b]$-n
- Ha ezek mind teljesülnek van olyan $\eta > |x_0 - x^*|$  szám, aminél $x_i \to x^*$
<!--ID: 1686765106934-->
END