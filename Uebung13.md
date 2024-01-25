<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 13
@style
.lia-toc__bottom {
    display: none;
}
@end



import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 13: 


## Aufgabe 1
                                      {{0}}
> __1.__ Warum ist kondensierte Materie für Leitungselektronen so durchlässig?

                                      {{1}}
**Lösung Aufgabe 1:**

                                      {{2}}
Kondensierte Materie ist für Elektronen aus zwei Günden "durchässig". 
- Erstens wird ein Leitungselektron von den Ionenrümpfen eines periodischen Gitters nicht abgelenkt, da seine Ausbreitung auf einer Wellenbewegung beruht, die an das periodische Potential der Ionenrümpfe im Kristallgitter angepaßt ist. 
- Zweitens wird ein Elektron nur selten an einem anderen gestreut, da zwei Elektronen aufgrund des Pauli
Prinzips nie auf dem selben Elektronenniveau sind.


## Aufgabe 2 

                                      {{0}}
> __2.__ Berechnen Sie unter Annahme eines freien Elektronengases die Fermi-Energie, die Fermi-Wellenzahl, die Fermi-Temperatur und die Fermi- Geschwindigkeit für Silber. Silber hat eine Dichte von $10,5\,\mathrm{\frac{g}{cm^3}}$ und liefert ein Elektron pro Atom.

                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}
Für die Elektronenkonzentration $n$ in Ag gilt:                                            
$$\begin{align*}n &=\frac{\text{Anzahl}}{\text{Volumen}}\\
&=1\cdot N_\mathrm{A} \cdot \frac{ \rho}{M_\text{mol}} \\
&=\mathrm{1\cdot 6,022 \cdot 10^{23}\frac{1}{mol} \cdot \frac{ 10,5 \frac{10^{-3}\,kg}{(10^{-2} \, m)^3}}{107,8682 \frac{10^{-3}kg}{mol}}}\\
&= 5,86 \cdot 10^{28}\, \mathrm{m^{-3}}\\
&=5,86 \cdot 10^{22}\, \mathrm{cm^{-3}}\end{align*}$$

Damit folgt für den Fermi-Wellenvektor

$$k_F=\sqrt[3]{3\pi^2n} = \sqrt[3]{3\pi^2 \cdot 5,86 \cdot 10^{22}\, \mathrm{cm^{-3}}} =1,20 \cdot  10^8 \,\mathrm{cm^{-1}}\$$

und die Fermi-Energie

$$\begin{align*}
E_F&=\frac{\hbar^2}{2m_\mathrm{e}} k_\mathrm{F}^2  \\ 
&=\frac{(1,05457\cdot 10^{-34} \mathrm{Js})^2}{2\cdot 9,109382 \cdot 10^{-31} \mathrm {kg}}\cdot  (1,20 \cdot  10^8 \,\mathrm{\frac{1}{10^{-2} m}})^2\\
&= 8,82 \cdot 10^{-19} \mathrm{J} \\
&= 8,82 \cdot 10^{-19} \mathrm{\frac{eV}{1,60218\cdot 10^{-19}}}= 5,5 \,\mathrm{eV}\end{align*}$$

Die Fermi-Temperatur ist:

$$T_\mathrm{F} = \frac{E_\mathrm{F}}{k_\mathrm{B}} = \frac{8,82 \cdot 10^{-19} \mathrm{J}}{1,380665 \cdot 10^{-23}\frac{J}{K}}= 63913\, \mathrm{K}\approx 63,9 \cdot 10^3\, \mathrm{K}$$

Die Fermi-Geschwindigkeit ist:

$$v_\mathrm{F} = \frac{\hbar}{m_\mathrm{e}} k_\mathrm{F}= \frac{1,05457\cdot 10^{-34} \mathrm{Js}}{9,109382 \cdot 10^{-31} \mathrm {kg}} \cdot 1,20 \cdot  10^8 \cdot  10^2\,\mathrm{m^{-1}}=1,39 \cdot10^8 \mathrm{\frac{m}{s}}$$



## Aufgabe 3
                                      {{0}}
> __3.__ Wie groß ist die Zustandsdichte eines dreidimensionalen freien Elektronengases $D(k)$ im reziproken Raum und $D(E)$ im realen Raum?


                                      {{1}}



**Lösung Aufgabe 3:**

                                      {{2}}
Es gilt wieder:

$$\int_{k(E)}^{k(E+\Delta E)} D(k)dk^3=\int_{E}^{E+\Delta E}D(E)dE$$


Die periodischen Randbedingungen für die ebenen Wellen (Knotenpunkte am Kristallrand) bedingen wieder (wie bei den Phononen) eine Quantelung der erlaubten Zustände (Wellenvektoren). Das Volumen pro Zustand im 3D-Impulsraum ist $\frac{(2\pi)^3}{V}$. Da jeder $k$-Wellenvektor von 2 Elektronen mit entgegengesetztem Spin besetzt werden kann, ist die Zustandsdichte damit 

$$D(k)=2\cdot \frac{V}{(2\pi)^3}$$



Die Anzahl $N$ der Zustände für freie Elektronen im 3-dimensionalem Raum in einer Kugel mit dem Radius $k$ ist damit:

$$N(k)=2\cdot\frac{\frac{4\pi}{3}k^3}{\frac{(2\pi)^3}{V}}=\frac{Vk^3}{3\pi^2}$$

Die 2 kommt von den beiden Spin-Möglichkeiten für jeden Wellenvektor $k$




## Aufgabe 4 
                                      {{0}}
> __4.__ Kinetische Energie des Elektronengases: Zeigen Sie, dass die kinetische Energie eines dreidimensionalen Elektronengases aus N freien Elektronen bei 0 K gleich folgendem Ausdruck ist!


                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}



## Aufgabe 5 

                                      {{0}}
> __5.__ Zeigen Sie, dass ein Fermi- Gas mit der Fermi-Energie EF auch am Temperaturnullpunkt einen Fermi- Druck    besitzt. Man vergleiche das Ergebnis mit dem eines klassischen idealen Gases.

                                      {{1}}
**Lösung Aufgabe 5:**

                                      {{2}}

 


## Aufgabe 6 

                                      {{0}}
> __6.__ Konstruieren Sie die ersten drei Brillouin-Zonen eines ebenen quadratischen Gitters.

                                      {{1}}
**Lösung Aufgabe 6:**



## Aufgabe 7

                                      {{0}}
>__7.__ Betrachten Sie ein einfaches ebenes quadratisches Gitter in zwei Dimensionen. Zeigen Sie, dass die kinetische Energie eines freien Elektrons an einer Ecke der ersten Brillouin - Zone doppelt so groß ist wie die eines Elektrons im Mittelpunkt einer Seitenfläche der Zone.

                                      {{1}}
**Lösung Aufgabe 7:**

                                      {{2}}


## Aufgabe 8

                                      {{0}}
>__8.__ Wie groß ist dieses Verhältnis für ein einfaches kubisches Gitter in drei Dimensionen?

                                      {{1}}
**Lösung Aufgabe 8**

                                      {{2}}
$