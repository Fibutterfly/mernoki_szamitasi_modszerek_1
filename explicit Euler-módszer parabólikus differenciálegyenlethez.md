---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/10tétel 
aliases: ["explicit Euler módszer","explicit Euler-módszer"]
TARGET DECK: 02::MSZM1
---

# explicit euler-módszer parabólikus DE-hez tartozó séma
![[Pasted image 20230621230047.png]]

#Galántai/mérnöki_jegyzet 

# explicit euler-módszer parabólikus DE-hez tartozó közelítő egyenlet
$$\begin{align}
	\dfrac{U_j^{k+1}-U_j^k}{\Delta t}= \dfrac{a}{(\Delta x)^2}*\left( U_{j+1}^k- 2*U_j^k + U_{j+1}^k\right) \tag{EEPPDE.1} \\
	U_j^{k+1} = s*U_{j-1}^k+(1-2*s)*U_j^k+s*U_{j+1}^k \tag{EEPPDE.2} \\
\end{align}$$
$$\
	\begin{bmatrix}
		U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
	\end{bmatrix} =
	\begin{bmatrix}
		1-2*s & s &0 &0 \\
		s & 1-2*s& s& 0 \\
		0 & \ddots & \ddots &   s \\
		0 & 0&s &1-2*s
	\end{bmatrix} * 
	\begin{bmatrix}
		U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
	\end{bmatrix} +
	s* \begin{bmatrix}
		U_1^k \\ 0 \\ \vdots \\ 0 \\ U_N^k 
	\end{bmatrix} 
$$
- $s = \dfrac{a* \Delta t}{(\Delta x)^2}$
- $U_j^0 = U(x_j,0)=f(x_j)$
- $U_1^k = u_0$
- $U_N^k = u_L$

#Galántai/mérnöki_jegyzet 

# explicit euler-módszer parabólikus DE-hez tartozó stabilítása

# explicit euler-módszer parabólikus DE-hez tartozó konvergálása

#Galántai/mérnöki_jegyzet





# Kártyák
START
Basic
Front:
explicit euler-módszer parabólikus DE-hez tartozó séma
Back:
![[Pasted image 20230621230047.png]]
<!--ID: 1687385282708-->
END

START
Basic
Front:
explicit euler-módszer parabólikus DE-hez tartozó közelítő egyenlet
Back:
$$\begin{align}
	\dfrac{U_j^{k+1}-U_j^k}{\Delta t}= \dfrac{a}{(\Delta x)^2}*\left( U_{j+1}^k- 2*U_j^k + U_{j+1}^k\right) \tag{EEPPDE.1} \\
	U_j^{k+1} = s*U_{j-1}^k+(1-2*s)*U_j^k+s*U_{j+1}^k \tag{EEPPDE.2} \\
\end{align}$$
$$\begin{align}
	\begin{bmatrix}
		U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
	\end{bmatrix} =
	\begin{bmatrix}
		1-2*s & s &0 &0 \\
		s & 1-2*s& s& 0 \\
		0 & \ddots & \ddots &   s \\
		0 & 0&s &1-2*s
	\end{bmatrix} * 
	\begin{bmatrix}
		U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
	\end{bmatrix} +
	s* \begin{bmatrix}
		U_1^k \\ 0 \\ \vdots \\ 0 \\ U_N^k 
	\end{bmatrix} 
\end{align}$$
- $s = \dfrac{a* \Delta t}{(\Delta x)^2}$
- $U_j^0 = U(x_j,0)=f(x_j)$
- $U_1^k = u_0$
- $U_N^k = u_L$
<!--ID: 1687385282715-->
END