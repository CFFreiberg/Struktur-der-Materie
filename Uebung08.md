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

## Aufgabe 2
> __2.__  Betrachten Sie einen linearen (eindimensionalen)  Kristall mit den  Gitterpunkten $r=m\cdot a$ mit  $m \in \mathbb{Z}$ und $a=$ Gitterkonstante. Auf jedem der Gitterpunkte sitzt ein identisches, punktförmiges Streuzentrum. Diese Atome werden von einer kohärenten Welle $\Psi_Q=\Psi_{Q,0}e^{i(k_oy-\omega t)}$ angeregt. Die Atome strahlen dann selbst kohärent und ohne Phasenverschiebung Kugelwellen mit der Frequenz $\omega$ ab: $\Psi=\frac{\Psi_0}{r}e^{i(\vec{k}\vec{r}-\omega t)} $ ab.

> __a)__  Welche Intensität wird mit einem Detektor gemessender sich weit weg vom Gitter im Abstand $L$ auf der $x$-Achse befindet?

**Lösung Aufgabe 2a:**


, In Analogie zu $F=\sum_G \int n_G \cdot \exp((i\vec{G}-\vec{\Delta k})\cdot\vec{r})$  ist die Gesamtstreuamplitude der Streustrahlung proportional zu  $F=\sum_m  n_G \cdot \exp((-i m a \Delta k))$. Die Summe über $M$ Gitterpunkte hat (unter Verwendung von $\sum_{m=0} ^{M-1}x^m=\frac{1-x^M}{1-x}$   folgenden Wert: $F=\frac{1-\exp\left(-iM(a\Delta k) \right)}{1-\exp\left(-ia\Delta k  \right)}$ . Die gestreute Intensität ist proportional zu $|F|^2$ . 

> __a.__  Zeigen Sie, dass   gilt!
b) Für ak=2h, h ganze Zahl, erscheint ein Beugungsmaximum. Ändern wir k geringfügig und definieren uns ein  in ak=2h+  so, dass den Ort des ersten Nulldurchgangs der Funktion sin(1/2M(ak) angibt. Zeigen Sie, dass gilt /M, so dass die Breite des Beugungsmaximums proportional zu 1/M ist und dadurch für große Werte von M extrem schmal werden kann. 