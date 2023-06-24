---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/11tétel 
aliases: []
TARGET DECK: 02::MSZM1
---

# implicit Euler-módszer parabólikus diferenciálegyenletekhez tartozó séma
![[Pasted image 20230623183834.png]]

#Galántai/mérnöki_jegyzet 

# implicit euler-módszer parabólikus DE-hez tartozó közelítő egyenlet
$$\begin{align}
	\dfrac{U_j^{k+1}-U_j^k}{\Delta t}= \dfrac{a}{(\Delta x)^2}*\left( U_{j+1}^{k+1}- 2*U_j^{k+1} + U_{j+1}^{k+1}\right) \tag{IEPPDE.1} \\
	U_j^{k} = -s*U_{j-1}^{k+1}+(1+2*s)*U_j^{k+1}-s*U_{j+1}^{k+1} \tag{IEPPDE.2} \\
\end{align}$$
$$
\begin{bmatrix}
	1+2*s & -s &0 &0 \\
	-s & 1+2*s& -s& 0 \\
	0 & \ddots & \ddots &   -s \\
	0 & 0& -s &1+2*s
\end{bmatrix} *
\begin{bmatrix}
	U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
\end{bmatrix} = 
\begin{bmatrix}
	U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
\end{bmatrix} +
s* \begin{bmatrix}
	U_1^{k+1} \\ 0 \\ \vdots \\ 0 \\ U_N^{k+1} 
\end{bmatrix} 
$$
- $s = \dfrac{a* \Delta t}{(\Delta x)^2}$
- $U_j^0 = U(x_j,0)=f(x_j)$
- $U_1^k = u_0$
- $U_N^k = u_L$

#Galántai/mérnöki_jegyzet 

# implicit euler-módszer mátrixához tartozó sajátérték
A [[Tridiagonális mátrix spektrális tulajdonságai|Tridiagonális mátrix spektrális sajátértéke]] szerint
$$\lambda_k = 1 + s*s - 2*s*\cos\left( \dfrac{k*\pi}{N-1} \right)$$

#Galántai/mérnöki_jegyzet 

# implicit euler-módszer stabilítása
A sajátérték mindig nagyobb, mint 1 és a megfelelő inverz saját értékek is tartanak a  $0$ mátrixhoz, így feltétel nélküli stabilis

#Galántai/mérnöki_jegyzet 

# kártyák
START
Basic
Front:
implicit Euler-módszer parabólikus diferenciálegyenletekhez tartozó séma
Back:
![[Pasted image 20230623183834.png]]
<!--ID: 1687539241116-->
END


START
Basic
Front:
implicit euler-módszer parabólikus DE-hez tartozó közelítő egyenlet
Back:
$$\begin{align}
	\dfrac{U_j^{k+1}-U_j^k}{\Delta t}= \dfrac{a}{(\Delta x)^2}*\left( U_{j+1}^{k+1}- 2*U_j^{k+1} + U_{j+1}^{k+1}\right) \tag{IEPPDE.1} \\
	U_j^{k} = -s*U_{j-1}^{k+1}+(1+2*s)*U_j^{k+1}-s*U_{j+1}^{k+1} \tag{IEPPDE.2} \\
\end{align}$$
$$
\begin{bmatrix}
	1+2*s & -s &0 &0 \\
	-s & 1+2*s& -s& 0 \\
	0 & \ddots & \ddots &   -s \\
	0 & 0& -s &1+2*s
\end{bmatrix} *
\begin{bmatrix}
	U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
\end{bmatrix} = 
\begin{bmatrix}
	U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
\end{bmatrix} +
s* \begin{bmatrix}
	U_1^{k+1} \\ 0 \\ \vdots \\ 0 \\ U_N^{k+1} 
\end{bmatrix} 
$$
- $s = \dfrac{a* \Delta t}{(\Delta x)^2}$
- $U_j^0 = U(x_j,0)=f(x_j)$
- $U_1^k = u_0$
- $U_N^k = u_L$
<!--ID: 1687539241125-->
END

START
Basic
Front:
implicit euler-módszer mátrixához tartozó sajátérték
Back:
A [[Tridiagonális mátrix spektrális tulajdonságai|Tridiagonális mátrix spektrális sajátértéke]] szerint
$$\lambda_k = 1 + s*s - 2*s*\cos\left( \dfrac{k*\pi}{N-1} \right)$$
<!--ID: 1687539241130-->
END

START
Basic
Front:
implicit euler-módszer stabilítása
Back:
A sajátérték mindig nagyobb, mint 1 és a megfelelő inverz saját értékek is tartanak a  $0$ mátrixhoz, így feltétel nélküli stabilis
<!--ID: 1687539241135-->
END