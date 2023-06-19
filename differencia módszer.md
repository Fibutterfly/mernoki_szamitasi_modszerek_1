---
tags: OE/ALKMAT/Mernoki1 OE/ALKMAT/Mernoki1/07tétel 
aliases: [""]
TARGET DECK: 02::MSZM1
---

# differencia módszer [[lineáris peremérték problémák]] esetén
$$\begin{align}
	\begin{aligned}
		&\dfrac{u_{i+1}-2*u_i+u_{i-1}}{h^2}+ \\
		&+ p(x_i)*\dfrac{u_{i+1}-u_{i-1}}{2*h} +\\
		& + q(x_i)*u_i 
	\end{aligned} &= r(x_i) \tag{DMLPPE.1} \\
	u_0 &= \alpha \tag{DMLPPE.2} \\
	u_{N+1} &= \beta \tag{DMLPPE.3} \\
	\begin{aligned}
		&\left( 1- \dfrac{h}{2}*p(x_i) \right)*u_{i-1} -\\ 
		&- \left( 2-h^2*q(x_i)*u_i \right) +\\
		&+ \left( 1+ \dfrac{h}{2}*p(x_i) \right)*u_{i+1}  
		
	\end{aligned} &= h^2*r(x_i) \tag{DMLPPE.4}
\end{align}$$

#Galántai/mérnöki_jegyzet 

# differencia módszer [[lineáris peremérték problémák]] esetén mátrixos formában
- Tridiagonálismátrix kapunk ([[sávmátrix]] $p,q=2$)
$$\begin{align}
	a_i =& 1 - \dfrac{h}{2}*p(x_i) \tag{DMLPPEMF.1} \\
	b_i =& -(2-h^2*q(x_i)) \tag{DMLPPEMF.2} \\
	c_i =& 1+\dfrac{h}{2}*p(x_i) \tag{DMLPPEMF.3} \\
\end{align}$$
$$\begin{align}
	&\begin{aligned}
		b_1*u_1 + \\
		+ c_1*u_2 
	\end{aligned} = h^2r(x_i)-a_1*\alpha  \tag{DMLPPEMF.4}\\ \\
	&\begin{aligned}
		a_i*u_{i-1} +\\
		+ b_i*u_i +\\
		+ c_i*u_{i+1}
	\end{aligned}= h^2*r(x_i) \tag{DMLPPEMF.5} \\ \\
	&\begin{aligned}
		a_N*u_{N-1} + \\
		+ b_N*u_N
	\end{aligned} = h^2*r(x_N)-c_N*\beta \tag{DMLPPEMF.6}
\end{align}$$

#Galántai/mérnöki_jegyzet 

# differencia módszer [[konvergencia|konvergenciája]] [[lineáris peremérték problémák]] és [[nemlineáris peremérték probléma ]] esetén
$$\begin{align}
	|u_j - y(x_j)| \le M*\dfrac{h^2}{12}*(M_4+ 2*P*M_3) \tag{DMKLPP.1} \\
	|p(x)| \le P \tag{DMKLPP.2} \\
	0 < Q_1 \le -q(x) \le Q_2 \tag{DMKLPP.3}
\end{align}$$
- $h \le 2/P$
- $y \in C^4 [a,b]$
- $0 \le j \le N+1$
- $M = \max(1,1/Q_1)$
- $M_i= \max_{a \le x \le b}|y^{(i)}(x)$

#Galántai/mérnöki_jegyzet 

# kártya
START
Basic
Front:
differencia módszer [[lineáris peremérték problémák]] esetén
Back:
$$\begin{align}
	\begin{aligned}
		&\dfrac{u_{i+1}-2*u_i+u_{i-1}}{h^2}+ \\
		&+ p(x_i)*\dfrac{u_{i+1}-u_{i-1}}{2*h} +\\
		& + q(x_i)*u_i 
	\end{aligned} &= r(x_i) \tag{DMLPPE.1} \\
	u_0 &= \alpha \tag{DMLPPE.2} \\
	u_{N+1} &= \beta \tag{DMLPPE.3} \\
	\begin{aligned}
		&\left( 1- \dfrac{h}{2}*p(x_i) \right)*u_{i-1} -\\ 
		&- \left( 2-h^2*q(x_i)*u_i \right) +\\
		&+ \left( 1+ \dfrac{h}{2}*p(x_i) \right)*u_{i+1}  
		
	\end{aligned} &= h^2*r(x_i) \tag{DMLPPE.4}
\end{align}$$
Ezzel lényegében egy $p,q=2$ [[sávmátrix|sávmátrixot]] csinálunk
<!--ID: 1686778993169-->
END
START
Basic
Front:
differencia módszer [[lineáris peremérték problémák]] esetén mátrixos formában
$$\begin{aligned}
		&\left( 1- \dfrac{h}{2}*p(x_i) \right)*u_{i-1} -\\ 
		&- \left( 2-h^2*q(x_i)*u_i \right) +\\
		&+ \left( 1+ \dfrac{h}{2}*p(x_i) \right)*u_{i+1}  
		
	\end{aligned} = h^2*r(x_i)$$
Back:
- Tridiagonálismátrix kapunk ([[sávmátrix]] $p,q=2$)
$$\begin{align}
	a_i =& 1 - \dfrac{h}{2}*p(x_i) \tag{DMLPPEMF.1} \\
	b_i =& -(2-h^2*q(x_i)) \tag{DMLPPEMF.2} \\
	c_i =& 1+\dfrac{h}{2}*p(x_i) \tag{DMLPPEMF.3} \\
\end{align}$$
$$\begin{align}
	&\begin{aligned}
		b_1*u_1 + \\
		+ c_1*u_2 
	\end{aligned}
	&= h^2r(x_i)-a_1*\alpha  \tag{DMLPPEMF.4}\\ \\
	&\begin{aligned}
		a_i*u_{i-1} +\\
		+ b_i*u_i +\\
		+ c_i*u_{i+1}
	\end{aligned}&= h^2*r(x_i) \tag{DMLPPEMF.5} \\ \\
	&\begin{aligned}
		a_N*u_{N-1} + \\
		+ b_N*u_N
	\end{aligned} &= h^2*r(x_N)-c_N*\beta \tag{DMLPPEMF.6}
\end{align}$$
<!--ID: 1687127127476-->
END

START
Basic
Front:
differencia módszer [[konvergencia|konvergenciája]] [[lineáris peremérték problémák]] 
Back:
$$\begin{align}
	|u_j - y(x_j)| \le M*\dfrac{h^2}{12}*(M_4+ 2*P*M_3) \tag{DMKLPP.1} \\
	|p(x)| \le P \tag{DMKLPP.2} \\
	0 < Q_1 \le -q(x) \le Q_2 \tag{DMKLPP.3}
\end{align}$$
- $h \le 2/P$
- $y \in C^4 [a,b]$
- $0 \le j \le N+1$
- $M = \max(1,1/Q_1)$
- $M_i= \max_{a \le x \le b}|y^{(i)}(x)$
<!--ID: 1687127714425-->
END