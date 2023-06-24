---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/13tétel
aliases: ["változók szétválasztása"]
TARGET DECK: 02::MSZM1
---

# változók szétválasztása módszere hiperbolikus differenciál egyenletekre
## példa feladat
$$\begin{align}
	\dfrac{\delta ^2u}{\delta t^2} = c^2*\dfrac{\delta^2 u}{\delta x^2} \tag{VSzHPDE.1} \\
	u(0,t)=0 \tag{VSzHPDE.2} \\
	u(L,t)=0 \tag{VSzHPDE.3} \\
	u(x,0) = f(x) \tag{VSzHPDE.4} \\
	u^\prime_t(x,0)=g(x) \tag{VSzHPDE.5}
\end{align}$$
## szeparációs konstans előállítása
$$\begin{align}
	u(x,t) = X(x)*T(t) \tag{VSzHPDE.6} \\
	X(x)*T^{\prime \prime}(t) = c^2*X^{\prime \prime}(x)*T(t) \tag{VSzHPDE.7} \\
	\dfrac{T^{\prime \prime}(t)}{c^2 *T(t)} = \dfrac{X^{\prime \prime}(x)}{X(x)} =k \tag{VSzHPDE.8}
\end{align}$$
- A `(VSzHPDE.6)` alapján behelyettesítünk a `(VSzHPDE.1)` feladatot  
- $k=\mu^2$, ez a szeparációs konstans $\mu > 0$
- $T(t)$
	- $\neq 0$
- $X(x)$
	- $\neq 0$

## feladat megoldása
$$\begin{align}
	X^{\prime \prime}-k*X = 0 \tag{VSzHPDE.9} \\
	T^{\prime \prime} - k*c^2*T=0 \tag{VSzHPDE.10} \\
	X(x) = d_1* \sin( \mu*x ) + d_2 * \cos(\mu * x) \tag{VSzHPDE.11} \\
	u(0,t) = X(0)*T(t) = d_2=0 \tag{VSzHPDE.12} \\
	u(L,t) = \begin{array}{c} &X(L)*T(t) =\\= &d_1* \sin( \mu *L)*T(t) \end{array}= 0 \tag{VSzHPDE.13} \\
	T^{\prime \prime} - \left( c* \dfrac{n*\pi}{L} \right)^2*T = 0 \tag{VszHPDE.14} \\
	T_n(t) = a_n*\sin(\lambda_n*t) + b_n \cos(\lambda_n*t) \tag{VSzHPDE.15} \\
	u(x,t) = \sin \left(\dfrac{n*\pi}{L}*x \right)*\left( \begin{array}{l} a_n \sin(\lambda_n*t)+\\+ b_n\cos(\lambda_n*t)\end{array}\right) \tag{VSzHPDE.16} \\
	u(x,t) = \sum_{n=1}^\infty\sin \left(\dfrac{n*\pi}{L}*x \right)*\left( \begin{array}{l} a_n \sin(\lambda_n*t)+\\+ b_n\cos(\lambda_n*t)\end{array}\right) \tag{VSzHPDE.17}
\end{align}$$

- `(VSzHPDE.12-13)`-t úgy kapjuk, hogy a peremfeltételbe be helyettesítjük a `(VSzHPDE.11)`-t 
- $d_1$
	- $\neq 0$
- `(VSzHPDE.13)` $\Leftrightarrow \sin( \mu* L) =0$
	- ennek feltétele, hogy $\mu = \mu_n = \dfrac{n* \pi}{L}$
- `(VSzHPDE.15)` a `(VSzHPDE.14)` megoldása
- $\lambda_n = c*\dfrac{n*\pi}{L}$
- `(VSzHPDE.17)` a `(VSzHPDE.16)` kiegészítése a szuperpozíció elvének megfelelően, ez az általános megoldás
## megoldás leolvasása
$$\begin{align}
	u(x,0) = f(x) = \sum_{n=1}^\infty b_n \sin \left( \dfrac{n*\pi}{L}*x \right) \tag{VSzHPDE.18} \\
	b_n = \dfrac{2}{L}*\int_0^L f(x)* \sin\left( \dfrac{n*\pi}{L}*x \right)dx \tag{VSzHPDE.19} \\
	u^\prime(x,0) = g(x) = \sum_{n=1}^\infty \lambda_n*a_n*\sin\left( \dfrac{n*\pi}{L}*x \right) \tag{VSzHPDE.20} \\
	a_n = \dfrac{2}{c*n*\pi}\int_0^Lg(x)*\sin \left( \dfrac{n*\pi}{L}*x \right)dx \tag{VSzHPDE.21}
\end{align}$$
- `(VSzHPDE.18)` feltétel, hogy kielégítse a kezdeti érték feltételt `(VSzHPDE.4)`
- `(VSzHPDE.19)` a Fourier sora a `(VSzHPDE.18)`-nak
- `(VSzHPDE.20)` a második perem feltétel `(VSzHPDE.5)`

# kártyák
START
Basic
Front:
változók szétválasztása módszere hiperbolikus differenciál egyenletekre
példa feladat
Back:
$$\begin{align}
	\dfrac{\delta ^2u}{\delta t^2} = c^2*\dfrac{\delta^2 u}{\delta x^2} \tag{VSzHPDE.1} \\
	u(0,t)=0 \tag{VSzHPDE.2} \\
	u(L,t)=0 \tag{VSzHPDE.3} \\
	u(x,0) = f(x) \tag{VSzHPDE.4} \\
	u^\prime_t(x,0)=g(x) \tag{VSzHPDE.5}
\end{align}$$
<!--ID: 1687631561360-->
END

START
Basic
Front:
változók szétválasztása módszere hiperbolikus differenciál egyenletekre
Back:
szeparációs konstans előállítása
$$\begin{align}
	u(x,t) = X(x)*T(t) \tag{VSzHPDE.6} \\
	X(x)*T^{\prime \prime}(t) = c^2*X^{\prime \prime}(x)*T(t) \tag{VSzHPDE.7} \\
	\dfrac{T^{\prime \prime}(t)}{c^2 *T(t)} = \dfrac{X^{\prime \prime}(x)}{X(x)} =k \tag{VSzHPDE.8}
\end{align}$$
- A `(VSzHPDE.6)` alapján behelyettesítünk a `(VSzHPDE.1)` feladatot  
- $k=\mu^2$, ez a szeparációs konstans $\mu > 0$
- $T(t)$
	- $\neq 0$
- $X(x)$
	- $\neq 0$
<!--ID: 1687631561369-->
END

START
Basic
Front:
változók szétválasztása módszere hiperbolikus differenciál egyenletekre
feladat megoldása
Back:
$$\begin{align}
	X^{\prime \prime}-k*X = 0 \tag{VSzHPDE.9} \\
	T^{\prime \prime} - k*c^2*T=0 \tag{VSzHPDE.10} \\
	X(x) = d_1* \sin( \mu*x ) + d_2 * \cos(\mu * x) \tag{VSzHPDE.11} \\
	u(0,t) = X(0)*T(t) = d_2=0 \tag{VSzHPDE.12} \\
	u(L,t) = \begin{array}{c} &X(L)*T(t) =\\= &d_1* \sin( \mu *L)*T(t) \end{array}= 0 \tag{VSzHPDE.13} \\
	T^{\prime \prime} - \left( c* \dfrac{n*\pi}{L} \right)^2*T = 0 \tag{VszHPDE.14} \\
	T_n(t) = a_n*\sin(\lambda_n*t) + b_n \cos(\lambda_n*t) \tag{VSzHPDE.15} \\
	u(x,t) = \sin \left(\dfrac{n*\pi}{L}*x \right)*\left( \begin{array}{l} a_n \sin(\lambda_n*t)+\\+ b_n\cos(\lambda_n*t)\end{array}\right) \tag{VSzHPDE.16} \\
	u(x,t) = \sum_{n=1}^\infty\sin \left(\dfrac{n*\pi}{L}*x \right)*\left( \begin{array}{l} a_n \sin(\lambda_n*t)+\\+ b_n\cos(\lambda_n*t)\end{array}\right) \tag{VSzHPDE.17}
\end{align}$$

- `(VSzHPDE.12-13)`-t úgy kapjuk, hogy a peremfeltételbe be helyettesítjük a `(VSzHPDE.11)`-t 
- $d_1$
	- $\neq 0$
- `(VSzHPDE.13)` $\Leftrightarrow \sin( \mu* L) =0$
	- ennek feltétele, hogy $\mu = \mu_n = \dfrac{n* \pi}{L}$
- `(VSzHPDE.15)` a `(VSzHPDE.14)` megoldása
- $\lambda_n = c*\dfrac{n*\pi}{L}$
- `(VSzHPDE.17)` a `(VSzHPDE.16)` kiegészítése a szuperpozíció elvének megfelelően, ez az általános megoldás
<!--ID: 1687631561375-->
END

START
Basic
Front:
változók szétválasztása módszere hiperbolikus differenciál egyenletekre
megoldás leolvasása
Back:
$$\begin{align}
	u(x,0) = f(x) = \sum_{n=1}^\infty b_n \sin \left( \dfrac{n*\pi}{L}*x \right) \tag{VSzHPDE.18} \\
	b_n = \dfrac{2}{L}*\int_0^L f(x)* \sin\left( \dfrac{n*\pi}{L}*x \right)dx \tag{VSzHPDE.19} \\
	u^\prime(x,0) = g(x) = \sum_{n=1}^\infty \lambda_n*a_n*\sin\left( \dfrac{n*\pi}{L}*x \right) \tag{VSzHPDE.20} \\
	a_n = \dfrac{2}{c*n*\pi}\int_0^Lg(x)*\sin \left( \dfrac{n*\pi}{L}*x \right)dx \tag{VSzHPDE.21}
\end{align}$$
- `(VSzHPDE.18)` feltétel, hogy kielégítse a kezdeti érték feltételt `(VSzHPDE.4)`
- `(VSzHPDE.19)` a Fourier sora a `(VSzHPDE.18)`-nak
- `(VSzHPDE.20)` a második perem feltétel `(VSzHPDE.5)`
<!--ID: 1687631599735-->
END
