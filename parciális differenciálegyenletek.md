---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/09tétel
aliases: ["PDE","parciális differenciálegyenlet"]
TARGET DECK: 02::MSZM1
---

# Parciális differenciálegyenletek
## implicit alak
$$\begin{align}
	u = u(x_1,x_2, \dots) \tag{PDE.1} \\
	F(x_1, x_2, \dots , x_n, u, u^\prime_{x_1}, \dots, u^\prime_{x_n}, u^{(k)}_{x_1}, \dots u^{(k)}_{x_n}) = 0 \tag{PDE.2}
\end{align}$$
## általános alak (másodrendű)
$$\begin{align}
	\sum_{i,j=1}^n A_{ij}(x)\dfrac{\delta^2 u}{\delta x_i \delta x_j} + \sum_{j=1}^nB_j(x) \dfrac{\delta u}{\delta x_j} + C(x)u = f(x) \tag{PDE.3}
\end{align}$$
ahol:
- $A_{ij}, B_j, C, f,x \in D$
	- mindegyik vektorváltozó függvénye (kivéve az $x$)
- $D \subset \mathbb{R}^n$ 

#Galántai/mérnöki_jegyzet 

# Fontos parciális differenciál egyenletek
- 2D hővezetés (diffuzió) egyenlet $\Delta u = u^{\prime \prime}_{xx} + u^{\prime \prime}_{yy} = \dfrac{1}{a^2}*\dfrac{\delta u}{\delta t}$
- Laplace-egyenlet: $\Delta u = 0$
- Poisson-egyenlet: $\Delta u + f = 0$
- 2D hullámegyenlet (rezgő húr, D'Alember egyenlete): $\Delta u = \dfrac{1}{c^2}* \dfrac{\delta^2 u}{\delta t^2}$

#Galántai/mérnöki_jegyzet 

# parciális differenciál egyenlet kvadratikus alakja
$$Q(\lambda_1, \dots, \lambda_n) = \sum_{ij}^n A_{ij}(x) \lambda_i \lambda_j$$
- $A_{ij},x \in D$
	- mindegyik vektorváltozó függvénye (kivéve az $x$)
- $D \subset \mathbb{R}^n$ 
- $\lambda \in \mathbb{R}$

#Galántai/mérnöki_jegyzet 

# parciális differenciál egyenlet kanonikus alakja
$$Q = \sum_{i=1}^n a_i \xi_i^2$$
- $a_i \in \{ -1,0,1 \}$
- Ez a kvadratikus alak nemszinguálris affin transzformációjából kapjuk

#Galántai/mérnöki_jegyzet 

# parciális differenciál egyenlet csoportosítása a kanonikus alak alapján
![[Parciális differenciál egyenletek - döntési fa - kanonikus alakja szerinti csoportosítás.excalidraw.png]]

#Galántai/mérnöki_jegyzet 

# kártyák
START
Basic
Front:
Mi a parciális differenciál egyenlet implicit alakja?
Back:
$$\begin{align}
	u = u(x_1,x_2, \dots) \tag{PDE.1} \\
	F(x_1, x_2, \dots , x_n, u, u^\prime_{x_1}, \dots, u^\prime_{x_n}, u^{(k)}_{x_1}, \dots u^{(k)}_{x_n}) = 0 \tag{PDE.2}
\end{align}$$
<!--ID: 1687207614380-->
END

START
Basic
Front:
Mi a (másodrendű) parciális differenciál egyenlet általános alakja?
Back:
$$\begin{align}
	\sum_{i,j=1}^n A_{ij}(x)\dfrac{\delta^2 u}{\delta x_i \delta x_j} + \sum_{j=1}^nB_j(x) \dfrac{\delta u}{\delta x_j} + C(x)u = f(x) \tag{PDE.3}
\end{align}$$
ahol:
- $A_{ij}, B_j, C, f,x \in D$
	- mindegyik vektorváltozó függvénye (kivéve az $x$)
- $D \subset \mathbb{R}^n$ 
<!--ID: 1687207614388-->
END

START
Basic
Front:
Milyen fontos parciális differenciál egyenleteket imserünk?
Back:
- 2D hővezetés (diffuzió) egyenlet $\Delta u = u^{\prime \prime}_{xx} + u^{\prime \prime}_{yy} = \dfrac{1}{a^2}*\dfrac{\delta u}{\delta t}$
- Laplace-egyenlet: $\Delta u = 0$
- Poisson-egyenlet: $\Delta u + f = 0$
- 2D hullámegyenlet (rezgő húr, D'Alember egyenlete): $\Delta u = \dfrac{1}{c^2}* \dfrac{\delta^2 u}{\delta t^2}$
<!--ID: 1687207614394-->
END

START
Basic
Front:
parciális differenciál egyenlet kvadratikus alakja
Back:
$$Q(\lambda_1, \dots, \lambda_n) = \sum_{ij}^n A_{ij}(x) \lambda_i \lambda_j$$
- $A_{ij},x \in D$
	- mindegyik vektorváltozó függvénye (kivéve az $x$)
- $D \subset \mathbb{R}^n$ 
- $\lambda \in \mathbb{R}$
<!--ID: 1687207614399-->
END

START
Basic
Front:
parciális differenciál egyenlet kanonikus alakja
Back:
$$Q = \sum_{i=1}^n a_i \xi_i^2$$
- $a_i \in \{ -1,0,1 \}$
- Ez a kvadratikus alak nemszinguálris affin transzformációjából kapjuk
<!--ID: 1687207614406-->
END

START
Basic
Front:
parciális differenciál egyenlet csoportosítása a kanonikus alak alapján
Back:
![[Parciális differenciál egyenletek - döntési fa - kanonikus alakja szerinti csoportosítás.excalidraw.png]]
<!--ID: 1687207634080-->
END