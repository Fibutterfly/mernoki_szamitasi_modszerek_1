---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/03tétel 
aliases:
TARGET DECK: 02::MSZM1
---
# Wilkinson tétele
$$\begin{align}
	(A+\Delta A)*\widehat{x} = b \tag{W.1} \\
	\dfrac{||\Delta A ||_\infty}{||A||_\infty} \le 8*n^3 *\rho_n *u+O(u^2) \tag{W.2}
\end{align}$$
- $\rho$ a pivot elemek növekedési tényezője
- $A*x=b$ 
	- $A \in \mathbb{C}^{n \times n}$
	- $x \in \mathbb{C}^n$
	- $b \in \mathbb{C}^n$
- $u$ egy szám, kisméretű perturbációt jelöl

#Galántai/mérnöki_jegyzet 

# Wilkinson tételének a következménye

$$\begin{align}
	\dfrac{||\Delta x||_\infty}{||x||_\infty} \le 8*n^3*\rho_n*cond_\infty(A)*u
\end{align}$$
- $||.||_\infty = \max_{i < n}(|x_i|)$
- $\rho$ pivot elemek növekedési tényezője
- $cond_\infty= ||.||_\infty *||.^{-1}||_\infty$
#Galántai/mérnöki_jegyzet 

# kártya
START
Basic
Front:
Wilkonson tétele
Back:
$$\begin{align}
	(A+\Delta A)*\widehat{x} = b \tag{W.1} \\
	\dfrac{||\Delta A ||_\infty}{||A||_\infty} \le 8*n^3 *\rho_n *u+O(u^2) \tag{W.2}
\end{align}$$
- $\rho$ a pivot elemek növekedési tényezője
- $A*x=b$ 
	- $A \in \mathbb{C}^{n \times n}$
	- $x \in \mathbb{C}^n$
	- $b \in \mathbb{C}^n$
- $u$ egy szám, kisméretű perturbációt jelöl
<!--ID: 1686748005619-->
END

START
Basic
Front:
Wilkonson tételének a következménye
Back:
$$\begin{align}
	\dfrac{||\Delta x||_\infty}{||x||_\infty} \le 8*n^3*\rho_n*cond_\infty(A)*u
\end{align}$$
- $||.||_\infty = \max_{i < n}(|x_i|)$
- $\rho$ pivot elemek növekedési tényezője
- $cond_\infty= ||.||_\infty *||.^{-1}||_\infty$
<!--ID: 1686748005628-->
END