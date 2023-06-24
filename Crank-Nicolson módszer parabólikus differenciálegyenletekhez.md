---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/12tétel 
aliases: []
TARGET DECK: 02::MSZM1
---

# Crank-Nicolson módszer parabólikus diferenciálegyenletekhez tartozó séma
![[Pasted image 20230623190936.png]]

#Galántai/mérnöki_jegyzet 

# Crank-Nicolson módszer parabólikus DE-hez tartozó közelítő egyenlet

$$\begin{align}
	&\dfrac{U_j^{k+1}-U_j^k}{\Delta t}= \dfrac{a}{(\Delta x)^2}*\left( 
		\begin{aligned}
			U_{j+1}^{k+1}- 2*U_j^{k+1} + U_{j+1}^{k+1}+ \\ +U_{j+1}^k- 2*U_j^k + U_{j+1}^k
		\end{aligned}	
	\right) \tag{CNPA.1} \\
	&\begin{aligned}
		s*U_{j-1}^k+\\+
		(2-2*s)*U_j^k+ \\
		+s*U_{j+1}^k
	\end{aligned} = 
	\begin{aligned}
		-s*U_{j-1}^{k+1}+\\
		+(2+2*s)*U_j^{k+1}- \\
		- s*U_{j+1}^{k+1}
	\end{aligned}\tag{CNPA.2} \\
\end{align}$$
$$
B *
\begin{bmatrix}
	U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
\end{bmatrix} = 
A*\begin{bmatrix}
	U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
\end{bmatrix} +
s* \begin{bmatrix}
	U_1^{k+1} + U_1^k \\ 0 \\ \vdots \\ 0 \\ U_N^{k+1} + U_N^k 
\end{bmatrix} 
$$
$$\begin{align}
	B = \begin{bmatrix}
			2+2*s & -s &0 &0 \\
			-s & 2+2*s& -s& 0 \\
			0 & \ddots & \ddots &   -s \\
			0 & 0& -s &2+2*s
		\end{bmatrix} \\
	A= \begin{bmatrix}
			2-2*s & s &0 &0 \\
			s & 2-2*s& s& 0 \\
			0 & \ddots & \ddots &   s \\
			0 & 0&s &2-2*s
		\end{bmatrix} 
\end{align}$$
- $s = \dfrac{a* \Delta t}{(\Delta x)^2}$
- $U_j^0 = U(x_j,0)=f(x_j)$
- $U_1^k = u_0$
- $U_N^k = u_L$

#Galántai/mérnöki_jegyzet 

# Crank-Nicolson stabilitása
## probléma bemutatása
$$
\begin{bmatrix}
	U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
\end{bmatrix} = 
B^{-1}*A*\begin{bmatrix}
	U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
\end{bmatrix} +
s*B^{-1}* \begin{bmatrix}
	U_1^{k+1} + U_1^k \\ 0 \\ \vdots \\ 0 \\ U_N^{k+1} + U_N^k 
\end{bmatrix} $$
kell vizsgálni
$$\begin{align}B=2*I-s*H\\
A=2*I+s*H \\
H= \begin{bmatrix}
			-2 & 1 &0 &0 \\
			1 & -2& 1& 0 \\
			0 & \ddots & \ddots &   1 \\
			0 & 0& 1 &-2
		\end{bmatrix}
\end{align}$$
## probléma feloldása
$$\mu_k = -2 + 2* \cos \left( \dfrac{k*\pi}{N-1} \right)$$
a [[Tridiagonális mátrix spektrális tulajdonságai|Tridiagonális mátrix spektrális sajátértéke]] alapján
$$\begin{align}
	\dfrac{1- \cos(a)}{2} = \sin^2\left( \dfrac{a}{2} \right) \\
	\mu_k = -4*\sin^2\left(\dfrac{k*\pi}{N-1} \right)
\end{align}$$
Így a $B^{-1}*A$ saját értékei
$$\lambda_k = \dfrac{2-4*s^2\left( \dfrac{k*\pi}{2*(N-1)} \right)}{2+4*s^2\left( \dfrac{k*\pi}{2*(N-1)} \right)}$$
ami mindig $[-1,1]$ intervallumba esik, így a módszer feltétel nélkül stabilis

#Galántai/mérnöki_jegyzet 

# Kártyák
START
Basic
Front:
Crank-Nicolson módszer parabólikus diferenciálegyenletekhez tartozó séma
Back:
![[Pasted image 20230623190936.png]]
<!--ID: 1687541487641-->
END

START
Basic
Front:
Crank-Nicolson módszer parabólikus DE-hez tartozó közelítő egyenlet
Back:

$$\begin{align}
	&\dfrac{U_j^{k+1}-U_j^k}{\Delta t}= \dfrac{a}{(\Delta x)^2}*\left( 
		\begin{aligned}
			U_{j+1}^{k+1}- 2*U_j^{k+1} + U_{j+1}^{k+1}+ \\ +U_{j+1}^k- 2*U_j^k + U_{j+1}^k
		\end{aligned}	
	\right) \tag{CNPA.1} \\
	&\begin{aligned}
		s*U_{j-1}^k+\\+
		(2-2*s)*U_j^k+ \\
		+s*U_{j+1}^k
	\end{aligned} = 
	\begin{aligned}
		-s*U_{j-1}^{k+1}+\\
		+(2+2*s)*U_j^{k+1}- \\
		- s*U_{j+1}^{k+1}
	\end{aligned}\tag{CNPA.2} \\
\end{align}$$
$$
B *
\begin{bmatrix}
	U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
\end{bmatrix} = 
A*\begin{bmatrix}
	U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
\end{bmatrix} +
s* \begin{bmatrix}
	U_1^{k+1} + U_1^k \\ 0 \\ \vdots \\ 0 \\ U_N^{k+1} + U_N^k 
\end{bmatrix} 
$$
$$\begin{align}
	B = \begin{bmatrix}
			2+2*s & -s &0 &0 \\
			-s & 2+2*s& -s& 0 \\
			0 & \ddots & \ddots &   -s \\
			0 & 0& -s &2+2*s
		\end{bmatrix} \\
	A= \begin{bmatrix}
			2-2*s & s &0 &0 \\
			s & 2-2*s& s& 0 \\
			0 & \ddots & \ddots &   s \\
			0 & 0&s &2-2*s
		\end{bmatrix} 
\end{align}$$
- $s = \dfrac{a* \Delta t}{(\Delta x)^2}$
- $U_j^0 = U(x_j,0)=f(x_j)$
- $U_1^k = u_0$
- $U_N^k = u_L$
<!--ID: 1687541493364-->
END

START
Basic
Front:
Crank-Nicolson stabilitása
probléma bemutatása
Back:
$$
\begin{bmatrix}
	U^{k+1}_2 \\ \vdots \\ U_j^{k+1} \\ \vdots \\ U^{k+1}_j
\end{bmatrix} = 
B^{-1}*A*\begin{bmatrix}
	U_2^k \\ \vdots \\ U_j^k \\ \vdots \\ U_{N-1}^k
\end{bmatrix} +
s*B^{-1}* \begin{bmatrix}
	U_1^{k+1} + U_1^k \\ 0 \\ \vdots \\ 0 \\ U_N^{k+1} + U_N^k 
\end{bmatrix} $$
kell vizsgálni
$$\begin{align}B=2*I-s*H\\
A=2*I+s*H \\
H= \begin{bmatrix}
			-2 & 1 &0 &0 \\
			1 & -2& 1& 0 \\
			0 & \ddots & \ddots &   1 \\
			0 & 0& 1 &-2
		\end{bmatrix}
\end{align}$$
<!--ID: 1687542939217-->
END

START
Basic
Front:
Crank-Nicolson stabilitása
probléma feloldása
Back:
$$\mu_k = -2 + 2* \cos \left( \dfrac{k*\pi}{N-1} \right)$$
a [[Tridiagonális mátrix spektrális tulajdonságai|Tridiagonális mátrix spektrális sajátértéke]] alapján
$$\begin{align}
	\dfrac{1- \cos(a)}{2} = \sin^2\left( \dfrac{a}{2} \right) \\
	\mu_k = -4*\sin^2\left(\dfrac{k*\pi}{N-1} \right)
\end{align}$$
Így a $B^{-1}*A$ saját értékei
$$\lambda_k = \dfrac{2-4*s^2\left( \dfrac{k*\pi}{2*(N-1)} \right)}{2+4*s^2\left( \dfrac{k*\pi}{2*(N-1)} \right)}$$
ami mindig $[-1,1]$ intervallumba esik, így a módszer feltétel nélkül stabilis
<!--ID: 1687542939226-->
END