<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 6

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

-->




# Übung 7: 


## Aufgabe 1

> __1.__  Wie sind der Strukturfaktor und der Atomformfaktor definiert?

**Lösung Aufgabe 1:**

Die Streuamplitude $F_G$ der am Gitter gebeugten (Röntgen)-Strahlung ist:

$$F_G=N \int_\mathrm{Zelle} n(r) \exp \left\{-i\vec{G} \cdot \vec{r}\right\} \cdot dV=N\cdot S_G$$

mit $N=$ Anzahl der Zellen im Kristall; $S_G=$ Strukturfaktor

Damit ist also der Strukturfaktor $S_G$:

$$S_G = \sum_ j \int  n_j (\vec{r}-\vec{r}_j) \cdot \exp \left\{-i\vec{G} \cdot \vec{r}\right\}\cdot  dV$$
mit $j=$ alle Atome in der Einheitszelle und $\vec{r}_j =$  Ortsvektor des Atoms $j$  und $\vec{\rho}=\vec{r}-\vec{r}_j$. Das kann umgeschreiben werden zu

$$\Rightarrow S_G = \sum_ j \exp \left\{-i\vec{G} \cdot \vec{r}_j\right\}\int  n_j (\vec{\rho}) \cdot \exp \left\{-i\vec{G} \cdot \vec{\rho}\right\} dV$$

$$\Rightarrow S_G = \sum_ j \exp \left\{-i\vec{G} \cdot \vec{r}_j\right\}\cdot f_j$$

$f_j$ ist der Atomformfaktor:

$$f_j =\int  n_j (\vec{\rho}) \cdot \exp \left\{-i\vec{G} \cdot \vec{\rho}\right\} dV$$

Das Integral wird über den gesamten Raum durchgeführt.

Für die Streuamplitude gilt also

$$F_G=N\cdot S_G=N\cdot \sum_ j  f_j \cdot \exp \left\{-i\vec{G} \cdot \vec{r}_j \right\} $$

Die Atompositionen der Atome in der Einheitszelle seien $\vec{r}_j=x_j\cdot \vec{a}_1+y_j\cdot \vec{a}_2+z_j\cdot \vec{a}_3$ wobei die $\vec{a}_{1,2,3}$ die Basisvektoren des realen Gitters sind.


Für den $(h,k,l)$-Reflex gilt dann:

$$\vec{G}_{hkl}\cdot \vec{r}_j= (h\cdot \vec{b}_1+k\cdot \vec{b}_2+l\cdot \vec{b}_3)\cdot(\vec{a}_1+y_j\cdot \vec{a}_2+z_j\cdot \vec{a}_3)$$


$$\Rightarrow \vec{G}_{hkl}\cdot \vec{r}_j=2\pi  (h\cdot x_j+k\cdot y_j+l\cdot z_j)$$

Damit gilt für den zum Reflex $G_{hkl}$ gehörigen Strukturfaktor $S_G$  eines Gitters:

$$ S_{G_{hkl}}=\sum_j f_j\cdot \exp \left\{ -2\pi i (h\cdot x_j+k\cdot y_j+l\cdot z_j )\right\} $$






## Aufgabe 2
> __2.__ Was gilt für den Strukturfaktor des raumzentrierten Gitters?

## Aufgabe 3
> __3.__ Was gilt für den Strukturfaktor des flächenzentrierten Gitters?

## Aufgabe 4
> __4.__ Die Kristallstruktur des Diamants lässt sich durch ein kfz-Gitter mit der Basis 
(0,0,0) und (¼, ¼, ¼) beschreiben. Der übliche Würfel als Einheitszelle hat also 8 Atome.
a) Bestimmen Sie den Strukturfaktor S für die Kombination des fcc-Gitters mit der oben beschriebenen 2-atomigen Basis. 
b) Welches sind die Nullstellen von Strukturfaktors S für Diamant!

## Aufgabe 5
> __5.__ Betrachten Sie ein lineares Gitter mit der Atomfolge ABAB….AB und einem Bindungsabstand A-B gleich ½a. Die Formfaktoren sind fA, fB entsprechend der Atome A, B. Der einfallende Röntgenstrahl stehe senkrecht auf der Atomkette. 
a) Zeigen Sie, dass die Intensität des gebeugten Strahls für ungerade n proportional zu |fA-fB|2 ist und für gerade n proportional zu|fA+fB|2.
b) Was passiert, wenn fA=fB ist?

## Aufgabe 6

> __6.__ Bestrahlt man bei Strukturuntersuchungen Kristalle aus mehreren Atom- oder Ionensorten mit Röntgenstrahlen, so kann man auf die auftretenden Reflexe schließen – man muss allerdings beide Atomsorten getrennt beachten. Kupferoxid (Cu2O) bildet ein kubisch raumzentriertes Gitter mit einem O-Atom im Ursprung und in der Mitte der kubischen Zelle. Die Kupferatome sitzen tetraedrisch um das Sauerstoffatom und haben in der Basis die Koordinaten (a/4, a/4, a/4) (a/4, 3a/4, 3a/4), (3a/4, 3a/4, a/4), (3a/4, a/4, 3a/4). Für welche Millerschen Indizes treten Reflexe auf?
