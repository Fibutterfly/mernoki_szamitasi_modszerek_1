---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/09tétel
aliases: ["változók szétválasztása"]
TARGET DECK: 02::MSZM1
---

# változók szétválasztása módszer parabolikus típusú egyenletekre
Példa feladat:
$$\begin{align}
 u^\prime_t = c^2*u^{\prime \prime}_{xx} \tag{VSzMP.1}
\end{align}$$
## szeparációs konstans előállítása
Megoldást ebben az alakban keressük:
$$\begin{align}
	u(x,t) = X(x) T(t) \tag{VSzMP.2} \\
	u^\prime_t = \dfrac{\delta T (t)}{\delta t}*X(x) \tag{VSzMP.3} \\
	c^2*u^{\prime \prime}_{xx} =c^2 T(t)* \dfrac{\delta ^2 X(x)}{\delta x^2} \tag{VSzMP.4}
\end{align}$$
Majd előállítjuk a szeparációs konstanst:
$$\begin{align}
	\dfrac{1}{c^2}*\dfrac{T^\prime(t)}{T(t)}=\dfrac{X^{\prime \prime}(x)}{X(x)} = - \mu^2 \tag{VSzMP.5}
\end{align}$$
## szeparációs konstanssal átalakított differenciál egyenlet
$$\begin{align}
	T^\prime + \mu^2*c^2*T=0 \tag{VSzMP.6} \\
	X^{\prime \prime} + \mu^2*X = 0 \tag{VSzMP.7}
\end{align}$$
Majd leolvasom a megoldásait
$$\begin{align}
	T(t) = e^{- \mu^2*c^t*t} \tag{VSzMP.8} \\
	X(x) = \alpha*\sin(\mu*x) + \beta*\cos(\mu*x) \tag{VSzMP.9}
\end{align}$$
## partikuláris megoldás
$$\begin{align}
	X(L) = \alpha*\sin(\mu*L) \tag{VSzMP.10}
\end{align}$$
Ebből következik, hogy
$$\begin{align}
	u(x,t) = \sum_{n=1}^\infty a_n * \sin\left( \dfrac{n*\pi}{L}*x \right)*e^{-\left( \cfrac{n*\pi}{L}*x \right)^2*t} \tag{VSzMP.11}
\end{align}$$
megnézzük $u(x,0)$-ra
$$\begin{align}
	u(x,0) = \sum_{n=1}^\infty a_n * \sin\left( \dfrac{n*\pi}{L}*x \right) \tag{VSzMP.12}
\end{align}$$
És felírjuk a szinuszos Fourier sort
$$\begin{align}
	a_n = \dfrac{2}{L}*\int_0^Lf(x)*\sin\left( \dfrac{n*\pi}{L}*x \right)dx \tag{VSzMP.13}
\end{align}$$

#Galántai/mérnöki_jegyzet 

# kártyák
START
Basic
Front:
változók szétválasztása módszer parabolikus típusú egyenletekre
$$\begin{align}
 u^\prime_t = c^2*u^{\prime \prime}_{xx} \tag{VSzMP.1}
\end{align}$$
szeparációs konstans előállítása
Back:
Megoldást ebben az alakban keressük:
$$\begin{align}
	u(x,t) = X(x) T(t) \tag{VSzMP.2} \\
	u^\prime_t = \dfrac{\delta T (t)}{\delta t}*X(x) \tag{VSzMP.3} \\
	c^2*u^{\prime \prime}_{xx} =c^2 T(t)* \dfrac{\delta ^2 X(x)}{\delta x^2} \tag{VSzMP.4}
\end{align}$$
Majd előállítjuk a szeparációs konstanst:
$$\begin{align}
	\dfrac{1}{c^2}*\dfrac{T^\prime(t)}{T(t)}=\dfrac{X^{\prime \prime}(x)}{X(x)} = - \mu^2 \tag{VSzMP.5}
\end{align}$$
<!--ID: 1687379620745-->
END

START
Basic
Front:
változók szétválasztása módszer parabolikus típusú egyenletekre
$$\begin{align}
 u^\prime_t = c^2*u^{\prime \prime}_{xx} \tag{VSzMP.1}
\end{align}$$
szeparációs konstans : $- \mu^2$
szeparációs konstanssal átalakított differenciál egyenlet
Back:
$$\begin{align}
	T^\prime + \mu^2*c^2*T=0 \tag{VSzMP.6} \\
	X^{\prime \prime} + \mu^2*X = 0 \tag{VSzMP.7}
\end{align}$$
Majd leolvasom a megoldásait
$$\begin{align}
	T(t) = e^{- \mu^2*c^t*t} \tag{VSzMP.8} \\
	X(x) = \alpha*\sin(\mu*x) + \beta*\cos(\mu*x) \tag{VSzMP.9}
\end{align}$$
<!--ID: 1687379620753-->
END

START
Basic
Front:
változók szétválasztása módszer parabolikus típusú egyenletekre
$$\begin{align}
 u^\prime_t = c^2*u^{\prime \prime}_{xx} \tag{VSzMP.1}
\end{align}$$
szeparációs konstans : $- \mu^2$
megoldások:
$$\begin{align}
	T(t) = e^{- \mu^2*c^t*t} \tag{VSzMP.8} \\
	X(x) = \alpha*\sin(\mu*x) + \beta*\cos(\mu*x) \tag{VSzMP.9}
\end{align}$$
partikuláris megoldás
Back:
$$\begin{align}
	X(L) = \alpha*\sin(\mu*L) \tag{VSzMP.10}
\end{align}$$
Ebből következik, hogy
$$\begin{align}
	u(x,t) = \sum_{n=1}^\infty a_n * \sin\left( \dfrac{n*\pi}{L}*x \right)*e^{-\left( \cfrac{n*\pi}{L}*x \right)^2*t} \tag{VSzMP.11}
\end{align}$$
megnézzük $u(x,0)$-ra
$$\begin{align}
	u(x,0) = \sum_{n=1}^\infty a_n * \sin\left( \dfrac{n*\pi}{L}*x \right) \tag{VSzMP.12}
\end{align}$$
És felírjuk a szinuszos Fourier sort
$$\begin{align}
	a_n = \dfrac{2}{L}*\int_0^Lf(x)*\sin\left( \dfrac{n*\pi}{L}*x \right)dx \tag{VSzMP.13}
\end{align}$$
<!--ID: 1687379620759-->
END

START
Basic
Front:
Folyamata a változók szétválasztása módszer parabolikus típusú egyenletekrenek
Back:
Szeparációs konstans előállítása
szeparációs konstanssal átalakított differenciál egyenlet
partikuláris megoldás
<!--ID: 1687379620765-->
END