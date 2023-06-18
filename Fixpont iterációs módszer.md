---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/04tétel 
aliases: ["fixpont iteráció", "fixpont módszer","fixpont iterációs eljárás","fixpont iterációs feladatként","fixpont iterációs feladat"]
TARGET DECK: 02::MSZM1
---

# Fixpont iterációs módszer alap feltételei
$$\begin{align}
	x = g(x) \\
	||g(x) - g(y)|| \le q*||x-y|| \\
\end{align}$$
- $g: \mathbb{R}^n \to \mathbb{R}^n$ folytonos
- $x,y,g(x) \in {\it{D}}$
	- ${\it{D}} \subseteq \mathbb{R}^n$ [[korlátos]], zárt tartomány
- $0 \le q < 1$

#Galántai/mérnöki_jegyzet 

# fixpont iterációs módszer konvergálása
$$\begin{align}
	x_{i+1} = g(x_i) \\
	||x_i - x^*|| \le q^i*||x_0 - x^*||
\end{align}$$
- $g: \mathbb{R}^n \to \mathbb{R}^n$ folytonos
- $x,y,g(x) \in {\it{D}}$
	- ${\it{D}} \subseteq \mathbb{R}^n$ [[korlátos]], zárt tartomány
	- $x^*$ az egyetlen megoldás, ami felé konvergál
- $0 \le q < 1$
- $i \ge 0$

#Galántai/mérnöki_jegyzet 

# Fixpont iterációs eljárás algoritmusa
![[Pasted image 20230614184850.png]]

#Galántai/mérnöki_jegyzet 

# fixpont iterációs eljárás kilépési feltétele
$$\begin{align}
	||x_{n+1} - x_n|| \le(1-q)*\epsilon \tag{FpI.1} \\
	||x_{i+1} - x_i|| \le c_2*\epsilon \tag{FpI.2} \\
	i = i_{max} \tag{FpI.3}
\end{align}$$
- $x \in {\it{D}}$
- ${\it{D}} \subseteq \mathbb{R}^n$, [[korlátos]], zárt tartomány
- $0 \le q < 1$
	- ez általában előre nem ismert
- $\epsilon > 0$ pontosság, amit kívánunk elérni
- $c_2$ hiba korlát szorzó, konstans
- `(FpI.1)`-et akkor használjuk, ha $q$ ismert
- `(FpI.2)` és `(FpI.3)` ha $q$ nem ismert és általában együtt őket

#Galántai/mérnöki_jegyzet 

# kártyák
START
Basic
Front:
Fixpont iterációs módszer alap feltételei
Back:
$$\begin{align}
	x = g(x) \\
	||g(x) - g(y)|| \le q*||x-y|| \\
\end{align}$$
- $g: \mathbb{R}^n \to \mathbb{R}^n$ folytonos
- $x,y,g(x) \in {\it{D}}$
	- ${\it{D}} \subseteq \mathbb{R}^n$ [[korlátos]], zárt tartomány
- $0 \le q < 1$
<!--ID: 1686762398952-->
END

START
Basic
Front:
fixpont iterációs módszer konvergálása
Back:
$$\begin{align}
	x_{i+1} = g(x_i) \\
	||x_i - x^*|| \le q^i*||x_0 - x^*||
\end{align}$$
- $g: \mathbb{R}^n \to \mathbb{R}^n$ folytonos
- $x,y,g(x) \in {\it{D}}$
	- ${\it{D}} \subseteq \mathbb{R}^n$ [[korlátos]], zárt tartomány
	- $x^*$ az egyetlen megoldás, ami felé konvergál
- $0 \le q < 1$
- $i \ge 0$
<!--ID: 1686762419319-->
END

START
Basic
Front:
Fixpont iterációs eljárás algoritmusa
Back:
![[Pasted image 20230614184850.png]]
<!--ID: 1686762398964-->
END

START
Basic
Front:
fixpont iterációs eljárás kilépési feltétele
Back:
$$\begin{align}
	||x_{n+1} - x_n|| \le(1-q)*\epsilon \tag{FpI.1} \\
	||x_{i+1} - x_i|| \le c_2*\epsilon \tag{FpI.2} \\
	i = i_{max} \tag{FpI.3}
\end{align}$$
- $x \in {\it{D}}$
- ${\it{D}} \subseteq \mathbb{R}^n$, [[korlátos]], zárt tartomány
- $0 \le q < 1$
	- ez általában előre nem ismert
- $\epsilon > 0$ pontosság, amit kívánunk elérni
- $c_2$ hiba korlát szorzó, konstans
- `(FpI.1)`-et akkor használjuk, ha $q$ ismert
- `(FpI.2)` és `(FpI.3)` ha $q$ nem ismert és általában együtt őket
<!--ID: 1686762398971-->
END