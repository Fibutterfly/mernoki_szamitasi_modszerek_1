---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/04tétel OE/ALKMAT/Mernoki1/08tétel 
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

# Newton-módszer [[nemlineáris peremérték probléma]] esetén
## Jacobi mátrix komponenseinek meghatározása
$$\begin{align}
	&F_1(u) =& \begin{aligned} \dfrac{u_2-2*u_1+\alpha}{h^2}- \\ - f\left( x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \end{aligned} &= 0 \tag{NM.NPP.1} \\ \hline
	&F_i(u) =& \begin{aligned}\dfrac{u_{i+1} - 2*u_i + u_{i-1}}{h^2} - \\ - f\left( x_i, u_i \dfrac{u_{i+1} - u_{i-1}}{2*h} \right)\end{aligned} &= 0 \tag{NM.NPP.2} \\ \hline
	&F_N(u) =& \begin{aligned}\dfrac{\beta - 2*u_N + u_{N-1}}{h^2} -\\- f\left( x_N. u_N, \dfrac{\beta - u_{N-1}}{2*h} \right)\end{aligned} &= 0 \tag{NM.NPP.3}
\end{align}$$
- Mindig az $F(u)=0$-t fejezzük ki

## Tridiagonális mátrix előállítása
$$\begin{align}
	&\dfrac{\delta F_1(u)}{\delta u_1} = - \dfrac{2}{h^2} - f^\prime_y \left(x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \tag{NM.NPP.4} \\
	&\dfrac{\delta F_i(u)}{\delta u_{2}} = \dfrac{2}{h^2} - \dfrac{1}{2*h}*f^\prime_z \left(x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \tag{NM.NPP.5} \\ 
	&\dfrac{\delta F_i(u)}{\delta u_{i-1}} = \dfrac{1}{h^2} + \dfrac{1}{2*h}*f^\prime_z \left(x_i, u_i, \dfrac{u_{i+1} - u_{i-1}}{2*h} \right) \tag{NM.NPP.6} \\
	&\dfrac{\delta F_i(u)}{\delta u_i} = - \dfrac{2}{h^2} - f^\prime_y \left(x_i, u_i, \dfrac{u_{i+1} - u_{i-1}}{2*h} \right) \tag{NM.NPP.7} \\
	&\dfrac{\delta F_i(u)}{\delta u_{i+1}} = \dfrac{1}{h^2} - \dfrac{1}{2*h}*f^\prime_z \left(x_i, u_i, \dfrac{u_{i+1} - u_{i-1}}{2*h} \right) \tag{NM.NPP.8} \\
	&\dfrac{\delta F_N(u)}{\delta u_{N-1}} = \dfrac{1}{h^2} - \dfrac{1}{2*h}*f^\prime_z \left(x_N, u_N, \dfrac{\beta - u_{N-1}}{2*h} \right) \tag{NM.NPP.9} \\
	&\dfrac{\delta F_N(u)}{\delta u_N} = - \dfrac{2}{h^2} - f^\prime_y \left(x_N, u_N, \dfrac{\beta - u_{N-1}}{2*h} \right) \tag{NM.NPP.10}
\end{align}$$
- $J(u) = \left[ \dfrac{\delta F_i(u)}{\delta x_j}\right]_{i,j=1}^n$ állítjuk elő
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

START
Basic
Front:
Milyen lépésekkel lehet megvalósítani a Newton-módszert [[nemlineáris peremérték probléma]] esetén?
Back:
Előállítjuk a Jacobi mátrixot
Majd abból egy Tridiagonálisat
<!--ID: 1687201123558-->
END

START
Basic
Front:
Newton-módszernek a [[nemlineáris peremérték probléma]] esetéhez szükséges Jacobi felírás
Back:
$$\begin{align}
	&F_1(u) =& \begin{aligned} \dfrac{u_2-2*u_1+\alpha}{h^2}- \\ - f\left( x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \end{aligned} &= 0 \tag{NM.NPP.1} \\ \hline
	&F_i(u) =& \begin{aligned}\dfrac{u_{i+1} - 2*u_i + u_{i-1}}{h^2} - \\ - f\left( x_i, u_i \dfrac{u_{i+1} - u_{i-1}}{2*h} \right)\end{aligned} &= 0 \tag{NM.NPP.2} \\ \hline
	&F_N(u) =& \begin{aligned}\dfrac{\beta - 2*u_N + u_{N-1}}{h^2} -\\- f\left( x_N. u_N, \dfrac{\beta - u_{N-1}}{2*h} \right)\end{aligned} &= 0 \tag{NM.NPP.3}
\end{align}$$
- Mindig az $F(u)=0$-t fejezzük ki
<!--ID: 1687201123565-->
END

START
Basic
Front:
Newton-módszerhez ismerjük ezt:
$$\begin{align}
	&F_1(u) =& \begin{aligned} \dfrac{u_2-2*u_1+\alpha}{h^2}- \\ - f\left( x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \end{aligned} &= 0 \tag{NM.NPP.1} \\ \hline
	&F_i(u) =& \begin{aligned}\dfrac{u_{i+1} - 2*u_i + u_{i-1}}{h^2} - \\ - f\left( x_i, u_i \dfrac{u_{i+1} - u_{i-1}}{2*h} \right)\end{aligned} &= 0 \tag{NM.NPP.2} \\ \hline
	&F_N(u) =& \begin{aligned}\dfrac{\beta - 2*u_N + u_{N-1}}{h^2} -\\- f\left( x_N. u_N, \dfrac{\beta - u_{N-1}}{2*h} \right)\end{aligned} &= 0 \tag{NM.NPP.3}
\end{align}$$
Mihez kell és mi a következő lépés?
Back:
$$\begin{align}
	&\dfrac{\delta F_1(u)}{\delta u_1} = - \dfrac{2}{h^2} - f^\prime_y \left(x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \tag{NM.NPP.4} \\
	&\dfrac{\delta F_i(u)}{\delta u_{2}} = \dfrac{2}{h^2} - \dfrac{1}{2*h}*f^\prime_z \left(x_1, u_1, \dfrac{u_2 - \alpha}{2*h} \right) \tag{NM.NPP.5} \\ 
	&\dfrac{\delta F_i(u)}{\delta u_{i-1}} = \dfrac{1}{h^2} + \dfrac{1}{2*h}*f^\prime_z \left(x_i, u_i, \dfrac{u_{i+1} - u_{i-1}}{2*h} \right) \tag{NM.NPP.6} \\
	&\dfrac{\delta F_i(u)}{\delta u_i} = - \dfrac{2}{h^2} - f^\prime_y \left(x_i, u_i, \dfrac{u_{i+1} - u_{i-1}}{2*h} \right) \tag{NM.NPP.7} \\
	&\dfrac{\delta F_i(u)}{\delta u_{i+1}} = \dfrac{1}{h^2} - \dfrac{1}{2*h}*f^\prime_z \left(x_i, u_i, \dfrac{u_{i+1} - u_{i-1}}{2*h} \right) \tag{NM.NPP.8} \\
	&\dfrac{\delta F_N(u)}{\delta u_{N-1}} = \dfrac{1}{h^2} - \dfrac{1}{2*h}*f^\prime_z \left(x_N, u_N, \dfrac{\beta - u_{N-1}}{2*h} \right) \tag{NM.NPP.9} \\
	&\dfrac{\delta F_N(u)}{\delta u_N} = - \dfrac{2}{h^2} - f^\prime_y \left(x_N, u_N, \dfrac{\beta - u_{N-1}}{2*h} \right) \tag{NM.NPP.10}
\end{align}$$
- $J(u) = \left[ \dfrac{\delta F_i(u)}{\delta x_j}\right]_{i,j=1}^n$ állítjuk elő
- nemlineáris peremérték probléma esetén szükséges a Tridiagonális Jacobi mátrixhoz
<!--ID: 1687201123572-->
END