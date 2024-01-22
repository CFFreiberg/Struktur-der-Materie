<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 12
@style
.lia-toc__bottom {
    display: none;
}
@end



import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 12: 


## Aufgabe 1
                                      {{0}}
> __1.__ Stellen sie für die spezifische Wärme das Debysche $T^3$-Gesetz, das Einstein Modell und die Dulong-Petitsche Regel gegenüber. Welches sind die jeweils getroffenen Randbedingungen/Voraussetzungen? Welche charakteristischen Werte gehören jeweils dazu? In welchen Temperaturbereichen sind sie jeweils gültig?

                                      {{1}}
**Lösung Aufgabe 1:**

                                      {{2}}
|Debye|Einstein|Dulong-Petit|
|:---|:---|:---|
|tiefe T| mittlere T| hohe T|
|Schallgeschwindigkeit für jeden Polarisationstyp konstant|$N$ Oszillatoren der selben Frequenz|kinetische Energie $\frac{1}{2} k_B T$ pro Freiheitsgrad |
|nur Schwingungszustände mit $K \le K_D$|  optische Phononen|plus nochmal gleiche potentielle Energie|
|$T_D=\Theta _{{\mathrm {D}}}={\frac {\hbar \cdot \omega _{{\mathrm {D}}}}{k_{{\mathrm {B}}}}}={\frac {\hbar \cdot v_{{\mathrm {D}}}}{k_{{\mathrm {B}}}}}\cdot {\sqrt[ {3}]{{\frac {6\cdot \pi ^{2}\cdot N}{V}}}}$| $\Theta_E=\frac{\hbar \omega_0 }{K_\mathrm{0}}$|
|$\omega_D=\sqrt[ {3}]{{\frac {6\cdot \pi ^{2}\cdot v_s^3 N}{V}}}=v_s\cdot K_D$|$\omega_0$, nur eine Frequenz| |
|$D_{3d}(\omega)=\frac{V}{2\pi^2v_s^3} \omega^2$|$D(\omega)=N \delta(\omega-\omega_E)$|
|$K_D=\sqrt[{3}]{6\cdot \pi^2\frac{N}{V}}=\frac{\omega_D}{v_s}$| | |
|für $T \ll \Theta_D$ gilt $C_V^D=\frac{12 \pi^4}{5} N k_B (\frac{T}{\Theta})^3 \propto T^3$| $C_V^E=\begin{cases}   3Nk_B \big(\frac{\Theta_E}{T} \big)^2 e^{-\Theta_E/T} &\text{für } T\ll \Theta_E \\   3Nk_B &\text{für } T\gg \Theta_E \end{cases} $|$3Nk_B$|




![molare Wärmekapazität](media/MolareWaermekapazitaet.png "*Molare Wärmekapazität der Festkörper nach den Theorien von Einstein, Debye und Dulong-Petit Quelle: (Hering, E., Martin, R., Stohrer, M., Käß, H. (2016). Festkörperphysik. In: Physik für Ingenieure. Springer Vieweg, Berlin, Heidelberg.)[https://doi.org/10.1007/978-3-662-49355-7_9]* ")


## Aufgabe 2 

                                      {{0}}
> __2.__ Was versteht man bei einer Phonon-Phonon-Wechselwirkung unter einem Normalprozess und unter einem Umklappprozess? Was muss für die Phononen gelten, damit Umklappprozess überhaupt möglich sind?

                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}
Die Umklapp-Streuung (auch U-Prozess oder Umklapp-Prozess) ist ein Streuprozess, der zu einem Wellenvektor $K$ führt, der außerhalb der ersten Brillouin-Zone liegt. Der Wellenvektor wird durch einen reziproken Gittervektor $G$ in die erste Brillouin-Zone transformiert. Diese Transformation ermöglicht Streuprozesse, die andernfalls gegen den Impulserhaltungssatz verstoßen würden: Zwei nach rechts gerichtete Wellenvektoren können sich zu einem nach links gerichteten Wellenvektor verbinden. Diese Nichterhaltung ist der Grund, warum der Kristallimpuls kein echter Impuls ist.

![](https://upload.wikimedia.org/wikipedia/commons/e/ef/Phonon_nu_process.svg "Normal process (N-process) and Umklapp process (U-process). While the N-process conserves total phonon momentum, the U-process changes phonon momentum; Quelle: [Wikipedia DanielSchwen](https://en.wikipedia.org/wiki/Umklapp_scattering) , [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/&gt);")


## Aufgabe 3
                                      {{0}}
> __3.__ Welche geometrischen und inneren Effekte können die mittlere freie Weglänge von Phononen begrenzen?


                                      {{1}}
**Lösung Aufgabe 3a)**

                                      {{2}}


## Aufgabe 4 
                                      {{0}}
> __4.__ Wie lauten die Verteilungsfuktionen für die Bose-Einstein-Verteilung, die Maxwell-Bolzmann-Verteilung und die Fermi-Dirac-Verteilung?


                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}


## Aufgabe 5 

                                      {{0}}
> __5.__ Wie viele Gitterschwingungen gibt es nach der Bose-Einstein-Verteilung bei $T=300\,\mathrm{K}$ in einem Kristall mit einem Volumen von $\mathrm{1\, cm^3}$ Frequenz-bereich zwischen $4,0$ und $4,1\,\mathrm{MHz}$ (Schallgeschwindigkeit = $6000\,\mathrm{\frac{m}{s}}$)?

                                      {{1}}
**Lösung Aufgabe 5:**

## Aufgabe 6 

                                      {{0}}
> __6.__ Ein Laserstrahl (Wellenlänge 694 nm) durchläuft einen Quarzkristall. Dabei findet eine Wechselwirkung zwischen Photonen und Phononen ohne Gitter-Rückstoß statt (Brillouin-Streunung). Berechnen Sie die maximale Frequenz der hierdurch ausgelösten mechanischen Schwingungen und geben Sie die Frequenzverschiebung des gestreuten Lichtes an. (Schallgeschwindigkeit = 6000 m/s, Brechungsindex des Kristalls 1,54)

## Aufgabe 7

                                      {{0}}
>__7.__ Welche obere Grenzfrequenz haben Gitterschwingungen in NaCl (Debye- Temperatur = 322 K)?

## Aufgabe 8

>__8.__ Wie groß ist die molare Wärmekapazität für Aluminium bei 50 K (Debye- Temperatur = 400 K)