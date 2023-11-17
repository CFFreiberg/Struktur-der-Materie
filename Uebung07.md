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

> __1.__  Betrachten Sie die Streuamplitude der am Gitter gebeugten Röntgenstrahlung. Wie sind der Strukturfaktor und der Atomformfaktor definiert? Wie sind deren Zusammenhänge?

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

**Lösung Aufgabe 2:**

Das kubisch raumzentriertes Gitter (krz oder bcc) lässt sich durch eine kubische Einheitszelle mit identischen Atomen auf den Plätzen $(x_1,y_1,z_1)=(0,0,0)$ und $(x_2,y_2,z_2)=(\frac{1}{2}, \frac{1}{2},\frac{1}{2})$ beschreiben.

Für den Strukturfaktor gilt dann:

$$ S_{G_{hkl}}=\sum_j f_j\cdot \exp \left\{ -2\pi i (h\cdot x_j+k\cdot y_j+l\cdot z_j )\right\} $$

$$\Rightarrow  S_{G_{hkl}}= f_j\cdot( \exp \left\{ -2\pi i (h\cdot 0+k\cdot 0+l\cdot 0 )\right\} +\exp \left\{ -2\pi i (h\cdot \frac{1}{2}+k\cdot \frac{1}{2}+l\cdot \frac{1}{2} )\right\})$$

$$\Rightarrow  S_{G_{hkl}}=f_j\cdot(  \exp \left\{\ 0\right\} +\exp \left\{ \frac{-2\pi i}{2} (h+k+l )\right\})= f_j\cdot(  1 +\exp \left\{ -\pi i (h+k+l )\right\})$$

$\Rightarrow  S_{G_{hkl}}=0$ für $h+k+l$ ungerade und $S_{G_{hkl}}=2f_j$ für $h+k+l$  gerade.



## Aufgabe 3
> __3.__ Was gilt für den Strukturfaktor des flächenzentrierten Gitters?

**Lösung Aufgabe 3:**

Das kubisch flächenzentrierte Gitter (kfz oder fcc) lässt sich durch eine kubische Einheitszelle mit identischen vier Atomen auf den Plätzen 

$$(x_1,y_1,z_1)=(0,0,0)$$
$$(x_2,y_2,z_2)=(0, \frac{1}{2},\frac{1}{2})$$
$$(x_3,y_3,z_3)=( \frac{1}{2},0,\frac{1}{2})$$
$$(x_4,y_4,z_4)=( \frac{1}{2},\frac{1}{2},0)$$

beschreiben.

Für den Strukturfaktor gilt dann:

$$ S_{G_{hkl}}=\sum_j f_j\cdot \exp \left\{ -2\pi i (h\cdot x_j+k\cdot y_j+l\cdot z_j )\right\} $$

$$\Rightarrow  S_{G_{hkl}}= f_j\cdot(1+\exp \left\{ -\pi i (k+l )\right\}+\exp \left\{ -\pi i (h+l )\right\}+\exp \left\{ -\pi i (h+k )\right\})$$

| Indizes $h,k,l$    |             |  $S_{hkl}$ |
| ------------- |:----------------:| :-----|
| alle $h,k,l$ gerade  | $\Rightarrow$    |$S_{hkl}=4\cdot f_j$ |
| alle $h,k,l$ ungerade  | $\Rightarrow$         |  $S_{hkl}=4\cdot f_j$  |
| Indizes gemischt gerade und ungerade |$\Rightarrow$ |    $S_{hkl}=0$  |






## Aufgabe 4
> __4.__ Die Kristallstruktur des Diamants lässt sich durch ein kfz-Gitter mit der Basis 
$(0,0,0)$ und $(\frac{1}{4},\frac{1}{4},\frac{1}{4})$ beschreiben. Der übliche Würfel als Einheitszelle hat also 8 Atome.

> __a.__ Bestimmen Sie den Strukturfaktor S für die Kombination des fcc-Gitters mit der oben beschriebenen 2-atomigen Basis. 

**Lösung Aufgabe 4a:**

Das Diamantgitter ist ein fcc-Gitter mit derzweiatomigen (Atom A, Atom B)  Basis $(x_A,y_A,z_A)=(0,0,0)$ und $(x_B,y_B,z_B)=(\frac{1}{4}, \frac{1}{4},\frac{1}{4})$
Damit sitzen also die (gleichen) Atome auf den Positionen 

|   A |    B         |      
|:---| :---        |
|$(x_{A1},y_{A1},z_{A1})=(0,0,0)$ | $(x_{B1},y_{B1},z_{B1})=(\frac{1}{4}, \frac{1}{4},\frac{1}{4})$|
|$(x_{A2},y_{A2},z_{A2})=(0,\frac{1}{2},\frac{1}{2})$ | $(x_{B2},y_{B2},z_{B2})=(\frac{1}{4}, \frac{3}{4},\frac{3}{4})$|
|$(x_{A3},y_{A3},z_{A3})=(\frac{1}{2},0,\frac{1}{2})$ | $(x_{B3},y_{B3},z_{B3})=(\frac{3}{4}, \frac{1}{4},\frac{3}{4})$|
|$(x_{A4},y_{A4},z_{A4})=(\frac{1}{2},\frac{1}{2},0)$ | $(x_{B4},y_{B4},z_{B4})=(\frac{3}{4}, \frac{3}{4},\frac{1}{4})$|

Der Strukturfaktor berechnet sich damit zu 

$$ S_{G_{hkl}}=\sum_j f_j\cdot \exp \left\{ -2\pi i (h\cdot x_j+k\cdot y_j+l\cdot z_j )\right\} $$

$$\Rightarrow S_{G_{hkl}}=f\cdot \left ( 1+ \exp(-i\pi(k+l))+\exp(-i\pi(h+l))+\exp(-i\pi(h+k))) +\exp(\frac{-i\pi}{2}(h+k+l)) +\exp(\frac{-i\pi}{2}(h+3k+3l))+\exp(\frac{-i\pi}{2}(3h+k+3l)) +\exp(\frac{-i\pi}{2}(3h+3k+l)) \right )$$

$$\Rightarrow S_{G_{hkl}}=S_{G_{hkl}}(fcc)\cdot\left ( 1+\exp\left (\frac{-i\pi}{2}(h+k+l) \right )  \right )$$

$$\Rightarrow S_{G_{hkl}}=S_{G_{hkl}}(fcc)\cdot S_{G_{hkl}}(\mathrm{Basis})$$


> __b.__ Welches sind die Nullstellen von Strukturfaktors S für Diamant!

| Indizes $h,k,l$    | $h+k+l$           |  $S_{hkl}$(Basis) | $S_{hkl}$(fcc)|$S_{G_{hkl}} $ |
| ------------------- |:----------------:| :-----| :----- | :------ |
| alle $h,k,l$ gerade  | $4n+2$    |0 | $4f_j$ | 0 |
| alle $h,k,l$ gerade   | $4n$        |  2 |$4f_j$   |$8f_j$|
| alle $h,k,l$ ungerade |$2n+1$, $n$ gerade|    $1-i$  |$4f_j$  |$4f_j\cdot(1-i)$|
| alle $h,k,l$ ungerade |$2n+1$, $n$ ungerade|    $1+i$  |$4f_j$  |$4f_j\cdot(1+i)$|
| 1 grade, 2 ungerade |gerade|    $0$  |$0$  |$0$|
| 2 grade, 1 ungerade |ungerade|    $0$  |$0$  |$0$|

Kleine Zusammenfassung: Keine Reflexe bei gemischten Indizes und keine Reflexe, wenn alle Indizes gerade sind und zusätzlich die Summe der Indizes nicht durch 4 teilbar ist. 

## Aufgabe 5
> __5.__ Betrachten Sie ein lineares Gitter mit der Atomfolge ABAB….AB und einem Bindungsabstand A-B gleich ½a. Die Formfaktoren sind fA, fB entsprechend der Atome A, B. Der einfallende Röntgenstrahl stehe senkrecht auf der Atomkette. 
a) Zeigen Sie, dass die Intensität des gebeugten Strahls für ungerade n proportional zu |fA-fB|2 ist und für gerade n proportional zu|fA+fB|2.
b) Was passiert, wenn fA=fB ist?

## Aufgabe 6

> __6.__ Bestrahlt man bei Strukturuntersuchungen Kristalle aus mehreren Atom- oder Ionensorten mit Röntgenstrahlen, so kann man auf die auftretenden Reflexe schließen – man muss allerdings beide Atomsorten getrennt beachten. Kupferoxid (Cu2O) bildet ein kubisch raumzentriertes Gitter mit einem O-Atom im Ursprung und in der Mitte der kubischen Zelle. Die Kupferatome sitzen tetraedrisch um das Sauerstoffatom und haben in der Basis die Koordinaten (a/4, a/4, a/4) (a/4, 3a/4, 3a/4), (3a/4, 3a/4, a/4), (3a/4, a/4, 3a/4). Für welche Millerschen Indizes treten Reflexe auf?
