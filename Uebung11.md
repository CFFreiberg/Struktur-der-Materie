<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 11
@style
.lia-toc__bottom {
    display: none;
}
@end



import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 11: 


## Aufgabe 1
                                      {{0}}
> __1.__	Singularität in der Zustandsdichte:  Ausgehend von der Dispersionsrelation $\omega=\omega_m\left|\sin{\left(\frac{1}{2}Ka\right)}\right|$ für ein einatomiges lineares Gitter aus $N$ Atomen mit Wechselwirkungen nur zwischen nächsten Nachbarn soll gezeigt werden, dass die Zustandsdichte $D(\omega)=\frac{2N}{\pi}\cdot \frac{1}{(\omega_m^2-\omega^2)^\frac{1}{2}}$ ist, wobei $\omega_m$ die maximale Frequenz ist.

                                      {{1}}
**Lösung Aufgabe 1:**

                                      {{2}}
Vorüberlegung zum Zusammenhang von $D(\omega)$ und $D(K)$: Die mit den endlichen Abmessungen des Kristalls verbundenen Randbedingungen (Knoten am Rand) bewirken, dass nur eine bestimmte Anzahl von Wellenvektoren möglich ist. Wenn wir den Wellenvektor $K$ auf die erste Brillouin-Zone beschränken, finden wir wegen $K\le\frac{\pi}{a}$ folgenden Satz von erlaubten Wellenvektoren: 
$$K=\frac{\pi}{a}\cdot\frac{p}{N};\, p=0,1,2,3,....N$$

                                      {{3}}
Für die Zustandsdichte $D(K)$ im 1-dimensionalen Impulsraum gilt dann: 

                                      {{4}}
$$D(K) = \frac{\text{Anzahl der Zustände}}{ \text{zugehöriges Volumen im K-Raum}}=\frac{N}{\frac{2\pi}{a}}=\frac{Na}{2\pi}=\frac{L}{2\pi}$$

                                      {{5}}
Die Anzahl der Zustände muss im realen Raum und im Impulsraum gleich sein, und zwar der Anzahl der Atome:
$$\begin{align*}
N&=\int_{1.\mathrm{BZ}}D(K)dK\overbrace{=}^{1\mathrm{dim}}\int_{-\frac{\pi}{a}}^{+\frac{\pi}{a}}D(K)dK
=\int_0^{\omega_m}D(\omega)d\omega\\
&=2\int_{0}^{+\frac{\pi}{a}}D(K)dK
\end{align*}$$

                                      {{6}}
Die konstante Zustandsdichte im $K$- Raum übersetzt sich über eine nichtlineare Dispersionskurve $\omega(K)$ in eine Zustandsdichte $D(\omega)$

                                      {{7}}
![Herleitung der Zustandsdichte im Frequenzintervall mit Hilfe der Dispersionsrelation](media/Zustandsdichte_aus_Dispersionsrelation.png "*Herleitung der Zustandsdichte im Frequenzintervall mit Hilfe der Dispersionsrelation; $q=K$; Quelle: Vorlesungsskript zur Vorlesung Festkörperphysik WS 1998/1999 und SS 1999, Prof. Dr. Rudolf Gross und Dr. Achim Marx, Walther-Meissner-Institut*")


                                      {{8}}
Mit $D(K) =\frac{L}{2\pi}$ folgt also für 1 Dimension
$$D(\omega)d\omega=2D(K)dK=\frac{L}{\pi}\cdot dK\cdot =\frac{L}{\pi}\cdot \frac{dK}{d\omega}\cdot d\omega$$



                                      {{9}}
Nun muss also $\frac{dK}{d\omega}$ oder $\frac{d\omega}{dK}$ hergeleitet werden. Dazu wird die Dispersionsrelation genutzt:
$$\omega=\omega_\mathrm{m}\left|\sin{\left(\frac{1}{2}Ka\right)}\right|$$

{{10}}
![Bild Dispersionsrelation](media/A1_Omega_K.png "*Dispersionsrelation $\omega(K)$; Quelle: C. Funke*")

                                      {{11}}
wobei für die maximale Frequenz  $\omega_\mathrm{m}=\sqrt{\frac{4C}{M}}$ gilt.

                                      {{12}}
$$\Rightarrow K=\frac{2}{a}\arcsin \bigg(\frac{\omega}{\omega_\mathrm{m}}\bigg)$$

                                      {{13}}
Mit $\frac{d(\arcsin)}{dx}=\frac{1}{\sqrt{1-x^2}}$ folgt

                                      {{14}}
$$\begin{align*}
\Rightarrow \frac{dK}{d\omega}&=\frac{2}{a}\frac{1}{\sqrt{1-\big(\frac{\omega}{\omega_\mathrm{m}}\big)^2}}\frac{1}{\omega_\mathrm{m}}\\
&=\frac{2}{a} \frac{1}{\sqrt{\omega_\mathrm{m}^2-\omega^2}}
\end{align*}$$



                                      {{15}}
Daraus folgt insgesamt
$$\begin{align*}D(\omega)&=\frac{N\cdot a}{\pi}\cdot \frac{dK}{d\omega}\\&=\frac{N\cdot a}{\pi}\cdot\frac{2}{a}\cdot  (\omega_\mathrm{m}^2-\omega^2)^{-\frac{1}{2}}\\
&=\frac{2N}{\pi}\frac{1}{\sqrt{\omega_\mathrm{m}^2-\omega^2}}
\end{align*}$$

                                      {{16}}
Diese Funktion hat eine Singularität bei $\omega=\omega_\mathrm{m}$

{{17}}
![Bild Zustandsdichte](media/Zustandsdichte.png "*Zustandsdichte $D(\omega)$; Quelle: C. Funke*")

## Aufgabe 2 

                                      {{0}}
> __2.__	Singularität in der Zustandsdichte:  Angenommen, ein optischer Phononenast habe im Dreidimensionalen nahe $K=0$ die Form $\omega(K) = \omega_0 – A\cdot K^2$. Zeigen Sie, dass dann für $\omega < \omega_0$ gilt: $D(\omega)=\big(\frac{L}{2\pi}\big)^3\bigg(\frac{2\pi}{A^{\frac{3}{2}}}\bigg)\sqrt{\big(\omega_0-\omega\big)}$. Für  $\omega > \omega_0$ gilt $D(\omega) = 0$. Warum? In diesem Fall ist also die Ableitung der Zustandsdichte unstetig.

                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}
Die Formel $\omega(K)$ wird nach $K$ umgestellt:
$$K=\pm\sqrt{\frac{\omega_0-\omega(K)}{A}}$$

                                      {{3}}
Das Volumen der Kugel mit Radius $K$ im reziproken Raum ist damit:
$$\Omega=\frac{4\pi}{3}K^3=\frac{4\pi}{3}\bigg(\pm\sqrt{\frac{\omega_0-\omega(K)}{A}}\bigg)^3$$

                                      {{4}}
Das Volumen eines $K$-Wertes im reziproken Raum ist:
$$\Omega_K=\bigg(\frac{2\pi}{L}\bigg)^3$$

                                      {{5}}
Die Anzahl der Zustände $N$ mit Wellenvektor kleiner als $K$ ist damit $N=\frac{\Omega}{\Omega_K}$

                                      {{6}}
Mit $D(\omega)d\omega=dN$ folgt für $\omega < \omega_0$:
$$\begin{align*}
D(\omega)&=\bigg|\frac{dN}{d\omega}\bigg|\\
&=\bigg|\frac{d}{d\omega}\Bigg(\frac{\frac{4\pi}{3}\bigg(\sqrt{\frac{\omega_0-\omega(K)}{A}}\bigg)^3}{\bigg(\frac{2\pi}{L}\bigg)^3}\Bigg)\bigg|\\
&=\bigg|\bigg(\frac{L}{2\pi}\bigg)^3\frac{4\pi}{3}A^{-3/2}\cdot \frac{d}{d\omega}\bigg((\omega_0-\omega(K))^{3/2}\bigg)\bigg|\\
&=\bigg|\bigg(\frac{L}{2\pi}\bigg)^3\frac{4\pi}{3}A^{-3/2}\cdot(-1)\cdot  \frac{3}{2}\cdot (\omega_0-\omega(K))^{1/2}\bigg|\\
&=\bigg(\frac{L}{2\pi}\bigg)^3\frac{2\pi}{A^{3/2}}\cdot (\omega_0-\omega(K))^{1/2}
\end{align*}$$

                                      {{7}}
$D(\omega)=0$ für $\omega>\omega_0$ da der Wellenvektor $K$ beschränkt ist auf $-\frac{\pi}{a}\le K \le \frac{\pi}{a}$. Die Frequenz, die zu $K_{max}=\pm\frac{\pi}{a}$ gehört, ist $\omega_0$. Größere Wellenvektoren sind nicht möglich, deshalb muss bei den zugehörigen Frequenzen auch die Zustandsdichte Null sein. Oder mathematisch argumentiert: für $\omega>\omega_0$ ist der Term $(\omega_0-\omega(K))^{1/2}$ und damit die Zustandsdichte rein imaginär.


## Aufgabe 3
                                      {{0}}
> __3.__ Mittlere Wärmeausdehnung einer Kristallzelle (Na). 

                                      {{0}}
>__a)__ Schätzen Sie für eine primitive Elementarzelle eines Natriumkristalls bei $T=300\, \mathrm{K}$ die mittlere Wärmeausdehnung $\frac{\Delta V}{V}$ ab. Nehmen Sie dazu die  Gitterkonstante $a_\mathrm{Na}=4,225\, \AA$ an und den Kompressionsmodul $B$ zu $\mathrm{7 \cdot 10^{10} erg \cdot cm^{-3}= 7 \cdot 10^3 \,J\cdot cm^{-3}=  7 \cdot 10^9 \,J\cdot m^{-3}}$. Beachten Sie, dass die Debye-Temperatur mit $\mathrm{158\, K}$ geringer als $\mathrm{300\, K}$ ist, so dass die thermische Energie von der Größenordnung von $\frac{1}{2}k_\mathrm{B}\cdot T$ ist (klassische Betrachtung).

                                      {{0}}
>__b)__ Benutzen Sie dieses Ergebnis, um die mittlere thermische Schwankung $\frac{\Delta a}{a}$ der Gitterkonstanten abzuschätzen.



                                      {{1}}
**Lösung Aufgabe 3a)**

                                      {{2}}
Das Kompressionsmodul $B$ ist definiert über die zweite Ableitung der  potentiellen Energie des Kristalls $U$ nach der Volumenänderung $\Delta V$, also 
$$B=V\frac{d^2U(\Delta V)}{d(\Delta V)^2}$$

                                      {{3}}
Nach zweimaligem Interieren nach $\Delta V$ auf beiden Seiten folgt:

                                      {{4}}
$$\Rightarrow B \cdot\frac{\Delta V^2}{2}=V\cdot U(\Delta V)$$

                                      {{5}}
$$\Rightarrow U(\Delta V)=\frac{1}{2}B\cdot V \cdot \bigg(\frac{\Delta V}{V}\bigg)^2 \eqsim\frac{1}{2}k_\mathrm{B} T$$

                                   {{6}}
Diese potentielle Energie entspricht der potentiellen Energie einer gespannten Feder $\frac{1}{²}Cx^2$ mit der Federkonstanten $C$. Bei der thermischen Energie wird nur der Beitrag der reinen Volumenausdenhnung mit $\frac{1}{2}k_\mathrm{B} T$ berücksichtigt. Die Freiheitsgrade der Verzerrung (Schermodul) und der Verdrehung (Torsionsmodul) werden nicht angesprochen, dehalb nicht $\frac{3}{2}k_\mathrm{B} T$. 

                                      {{7}}
Damit folgt:
$$\bigg(\frac{\Delta V}{V}\bigg)^2=\frac{k_\mathrm{B} T}{B\cdot V} \Rightarrow$$

                                      {{8}}
$$\begin{align*}
\bigg(\frac{\Delta V}{V}\bigg)&=\sqrt{\frac{k_\mathrm{B} T}{B\cdot V}}\\
&=\mathrm{\sqrt{\frac{1.38065\cdot 10^{-23}\frac{J}{K}\cdot 300\, K }{7\cdot 10^9\frac{J}{m^3}\cdot (4.225\cdot 10^{-10} m)^3}}}\\
&=0,088
\end{align*}$$

                                      {{9}}
**Lösung Aufgabe 3b)**

                                      {{10}}
für isotrope kubische Systeme folgt:
$$\Delta V=(a+\Delta a)^3-a^3=a^3+3a^2\Delta a+......-a^3 \overbrace{\eqsim}^{\Delta a \ll a}3a^2\Delta a$$

                                      {{11}}
und damit 
$$\frac{\Delta V}{V}=\frac{3a^2\Delta a}{a^3}=\frac{3 \Delta a}{a}$$

                                      {{12}}
Mit dieser Gleichung und dem Ergebnis von Aufgabenteil a) folgt 

                                      {{13}}
$$\frac{\Delta a}{a}=\frac{1}{3}\frac{\Delta V}{V} \eqsim0.029$$


## Aufgabe 4 
                                      {{0}}
> __4.__ Nullpunkts-Gitterauslenkung und Wärmeausdehnung:   Experimentelle Messungen zeigen, dass mit steigender Temperatur die Gitterkonstante wächst. Wie ist das mittels eines Potential-Modells erklärbar?


                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}
Die Wärmeausdehnung lässt sich nur durch anharmonische Terme der Gitterenergie $\propto(r-r_0)^3$ und höherer Ordnung erklären, siehe folgende Abbildung. Bei höherer Temperatur werden höhere Schwingungszustände besetzt, deren Schwerpunkte für ein anharmonisches Potenzial bei größeren Gleichgewichtsabständen liegen. Dies führt im thermischen Mittel zu einem größeren Atomabstand.

                                      {{3}}
![Zur Veranschaulichung der thermischen Ausdehnung durch anharmonische Effekte](media/thermischeAusdehnunganharmonischeEffekte.png "*Zur Veranschaulichung der thermischen Ausdehnung durch anharmonische Effekte.  Quelle: Vorlesungsskript zur Vorlesung Festkörperphysik WS 1998/1999 und SS 1999, Prof. Dr. Rudolf Gross und Dr. Achim Marx, Walther-Meissner-Institut*")


## Aufgabe 5 

                                      {{0}}
> __5.__ Spezifische Wärme einer linearen einatomigen Kette:  Berechnen Sie für akustische Phononen die innere Energie und die spezifische Wärme einer einatomigen Kette für die Grenzfälle einer hohen und einer niedrigen Temperatur. Nutzen Sie dabei die Debye-Näherung $D(\omega)= \frac{N}{\omega_\mathrm{D}}$, wobei $\omega_\mathrm{D}=k_\mathrm{B} \cdot \Theta_\mathrm{D}$

                                      {{1}}
**Lösung Aufgabe 5:**

Die Debye-Näherung (akustische Phononen) ist eine Kontinuums-Näherung bis zur Debye-Grenzfrequenz $\omega_\mathrm{D}$, wobei $\hbar \omega_\mathrm{D} = k_\mathrm{B} \Theta_\mathrm{D}$ mit $\Theta_\mathrm{D}=$ Debye-Temperatur. 

                                      {{2}}
Mit der [Besetzungswahrscheinlichkeit $f$ für Bosonen](https://de.wikipedia.org/wiki/Bose-Einstein-Statistik) (Bose-Einstein-Verteilung) folgt für die innere Energie der linearen einatomigen Kette
$$f(\omega,T)=\frac{1}{e^{\frac{\hbar \omega}{k_\mathrm{B} T}}-1}$$

                                      {{3}}
$$U(T)=3\int_0^{\omega_\mathrm{D}} \hbar \omega D(\omega)f(\omega,T)d\omega$$
Die 3 steht für zwei transversale und einen longitudinalen akustischen Ast. Einsetzen ergibt:

                                      {{4}}

$$U(T)=3\int_0^{\omega_\mathrm{D}} \hbar \omega \frac{N}{\omega_\mathrm{D}}\frac{1}{e^{\frac{\hbar \omega}{k_\mathrm{B} T}}-1}d\omega$$  

{{5}}
Mit den Substitutionen 
$$\begin {align*}\\
x&=\frac{\hbar\omega}{k_\mathrm{B} T}\\
x_\mathrm{D}&=\frac{\hbar\omega_\mathrm{D}}{k_\mathrm{B} T}=\frac{\Theta_\mathrm{D}}{T}\\
d\omega&=\frac{k_\mathrm{B} T}{\hbar} dx
\end{align*}$$

                                      {{6}}
Folgt
$$U(T)=\frac{3N k_\mathrm{B} T^2}{\Theta_\mathrm{D}}\int_0^{x_\mathrm{D}}\frac{x}{e^x -1}dx$$

                                      {{7}}
**Fall 1, hohe Temperaturen, $T \gg\Theta_\mathrm{D}$, $x \rightarrow 0$**

                                      {{8}}
Aus $e^x \approx 1+x$ folgt  
$$\int_0^{x_\mathrm{D}}\frac{x}{e^x -1}dx=\int_0^{x_\mathrm{D}}\frac{x}{1+x -1}dx=\int_0^{x_\mathrm{D}}1dx=x_\mathrm{D}$$

                                      {{9}}
$$\Rightarrow U(T)=\frac{3N k_\mathrm{B} T^2}{\Theta_\mathrm{D}}x_\mathrm{D}=3N k_\mathrm{B} T$$

                                      {{10}}
Für die spezifische Wäreme gilt also
$$c_\mathrm{V}=\frac{dU}{dT}=3Nk_\mathrm{B}$$

                                      {{11}}
Das entspricht der [Regel von Dulong-Petit](Dulong-Petit-Gesetz).

                                      {{12}}
**Fall 2, niedrige Temperaturen, $T \ll\Theta_\mathrm{D}$, $x \rightarrow \infty$**

                                      {{13}}
$$\int_0^{\infty}\frac{x}{e^x -1}dx=\frac{\pi^2}{6}$$

                                      {{14}}
$$\Rightarrow U(T)=\frac{3N k_\mathrm{B} T^2}{\Theta_\mathrm{D}}\frac{\pi^2}{6}=\frac{\pi^2N k_\mathrm{B} T^2}{2\Theta_\mathrm{D}}$$

                                      {{15}}
$$c_\mathrm{V}=\frac{dU}{dT}=\frac{\pi^2N k_\mathrm{B} T}{\Theta_\mathrm{D}}\propto T$$
Achtung, $c_\mathrm{V}\propto T$ gilt nur in 1D. Für 2D gilt $c_\mathrm{V}\propto T^2$ und für 3D gilt $c_\mathrm{V}\propto T^3$.