<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 6

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

-->


# Übung 8: 


## Aufgabe 1

> __1.__  Eine für die Auswertung der Röntgenreflexe kubischer Substanzen benötigte Größe ist die Quatratsumme  $ h^2+ k^2 +l^2$. Stellen Sie eine Tabelle zusammen, in der Sie für $1\le h^2+ k^2 +l^2 \le 15$ die zugehörigen $hkl$- Werte für die drei verschiedenen kubischen Gitter (sc, bcc, fcc) eintragen. Für welche Werte von $ h^2+ k^2 +l^2$ sind jeweils Reflexe zu erwarten. Wieso kann man aus der Auftragung eines Beugungsspektrums über $\sin ^2\theta$ erkennen, welches der drei Gitter vorliegt?

**Lösung Aufgabe 1:**

***kubisch primitiv (sc):***

$S_{hkl}= f_j$ mit $f_j=$ Atomformfaktor


***kubisch raumzentriert (bcc):***

 $S_{hkl}=2f_j$ für $h+k+l$  gerade; $S_{hkl}=0$ für $h+k+l$ ungerade


***kubisch flächenzentriert (fcc):***

$S_{hkl}=4\cdot f_j$ für alle $ h,k,l$ gerade oder alle $h,k,l$ ungerade. Sonst Null

|$ h^2+ k^2 +l^2$| sc $(hkl)$| bcc $(hkl)$ |fcc $(hkl)$|
|:---|:---|:---|:---|
1|(1,0,0)|-|-|
2|(1,1,0)|(1,1,0)|-|
3|(1,1,1)|-|(1,1,1)|
4|(2,0,0)|(2,0,0)|(2,0,0)|
5|(2,1,0)|-|-|
6|(2,1,1)|(2,1,1)|-|
7|-|-|-|
8|(2,2,0)|(2,2,0)|(2,2,0)|
9|(3,0,0); (2,2,1)|-|-|
10|(3,1,0)|(3,1,0)|-|
11|(3,1,1)|-|(3,1,1,)|
12|(2,2,2)|(2,2,2)|(2,2,2)|
13|(3,2,0)|-|-|
14|(3,2,1)|(3,2,1)|-|
15|-|-|-|

Für kubische Gitter gilt:

$$d_{hkl}=\frac{a}{\sqrt{h^2+k^2+l^2}}$$

Eingesetzt in die  Bragg-Bedingung für Beugung (in die erste Ordnung) $\lambda=2\cdot d_{hkl}\cdot \sin(\theta)$ ergibt sich 

$$ \sin^2(\theta)=\left (\frac{\lambda}{2a} \right )^2(h^2+k^2+l^2)$$

Eine Auftragung des Beugungsspektrums über $\sin ^2\theta$ und ein Vergleich mit den vorhandenen Reflexen bei den $h^2+k^2+l^2$-Werten ermöglicht eine Unterscheidung von sc-, bcc- und fcc-Gittern.

## Aufgabe 2 (Breite des Beugungsmaximums)
> __2.__  Betrachten Sie einen linearen (eindimensionalen)  Kristall mit den  Gitterpunkten $r=m\cdot a$ mit  $m \in \mathbb{Z}$ und $a=$ Gitterkonstante. Auf jedem der Gitterpunkte sitzt ein identisches, punktförmiges Streuzentrum. In Analogie zur Streuamplitude in einem realen Kristall $F=\sum_G \int n_G \cdot \exp(i(\vec{G}-\vec{\Delta k})\cdot\vec{r})\cdot dV$  ist die Gesamtstreuamplitude der Streustrahlung proportional zu  $F=\sum_{m=0}^M  \exp(-i m a \Delta k)$. Atome werden von einer kohärenten Welle $\Psi_Q=\Psi_{Q,0}e^{i(k_oy-\omega t)}$ angeregt. Die Summe über $M$ Gitterpunkte hat den Wert 

$$F=\frac{1-\exp(-iM(a\cdot \Delta k))}{1-\exp(-i(a\cdot \Delta k))}$$
>unter Verwendung der Reihenentwicklung 
$$ \sum_{M=0}^{M-1}x^m=\frac{1-x^M}{1-x}$$
>Die gestreute Intensität ist proportional zu $|F|^2$. 

> __a)__ Zeigen Sie, dass gilt:
$$|F|^2 \equiv F\cdot \overline{F}=\frac{\sin^2\left( \frac{1}{2}M(a\cdot\Delta k)\right )}{\sin^2\left( \frac{1}{2}(a\cdot\Delta k)\right )}$$

**Lösung Aufgabe 2a:**

$|F|^2 \equiv F\cdot \bar{F}$ muss berechnet werden. Dazu benötigen wir das konjugiert Komplexe von $F$. Mit $ \overline{\left(\frac{z_1}{z_2}\right)} = \frac{\overline z_1}{\overline z_2}$ für $ z_2 \ne 0 $ folgt:

$$\overline{F}=\frac{1-\exp(+iM(a\cdot \Delta k))}{1-\exp(+i(a\cdot \Delta k))}$$

Und damit :

$$|F|^2 \equiv F\cdot \bar{F}=\frac{1-\exp(-iM(a\cdot \Delta k))}{1-\exp(-i(a\cdot \Delta k))}\cdot \frac{1-\exp(+iM(a\cdot \Delta k))}{1-\exp(+i(a\cdot \Delta k))}$$

$$\Rightarrow |F|^2=\frac{1-\exp(+iM(a\cdot \Delta k))-\exp(-iM(a\cdot \Delta k))+1}{1-\exp(+i(a\cdot \Delta k))-\exp(-i(a\cdot \Delta k))+1}$$ 

Da $e^{ix}=\cos(x)+i\sin(x)$ folgt mit $e^{ix}+e^{-ix}=2\cos(x)$

$$\Rightarrow |F|^2=\frac{2-2\cos(Ma\Delta k)}{2-2\cos(a \Delta k)}=\frac{1-\cos(Ma\Delta k)}{1-\cos(a \Delta k)}$$

Mit $\cos(2x)=1-\sin^2(2x)$ folgt:

$$\Rightarrow |F|^2=\frac{1-(1-2\sin^2(\frac{1}{²}Ma\Delta k))}{1-(1-2\sin^2(\frac{1}{2}a \Delta k))}=\frac{\sin^2(\frac{1}{²}Ma\Delta k)}{\sin^2(\frac{1}{2}a \Delta k)}$$


![Beugungsmaxima](https://www.geogebra.org/calculator/nup3rbjn)


$|F|^2$ hat damit Nullstellen bei $a\cdot \Delta k=2\pi h$, ($h \in \mathbb{Z}$)

> __b.__ Für $a\Delta k=2\pi h$ mit $h \in \mathbb{Z} $ erscheint ein Beugungsmaximum. Ändern wir $\Delta k$ geringfügig und definieren uns ein $\epsilon$ in $a \Delta k=2\pi h+\epsilon$ so, dass $\epsilon$ den Ort des ersten Nulldurchgangs der Funktion $\sin(\frac{1}{²}Ma\Delta k)$ angibt. Zeigen Sie, dass gilt $\epsilon=\frac{2\pi}{M}$, so dass die Breite des Beugungsmaximums proportional zu $\frac{1}{M}$ist und dadurch für große Werte von $M$ extrem schmal werden kann. 
