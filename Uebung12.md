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
|komplexe Festkörper, tiefe T $\Rightarrow$ nur akk. Phononen| einfache Festkörper, mittlere T| hohe T|
|Schallgeschwindigkeit für jeden Polarisationstyp konstant $\omega=v_sK$|$N$ Oszillatoren der selben Frequenz. Die Gitterschwingungen des Kristalls werden gequantelt, d. h. der Festkörper kann Schwingungsenergie nur in diskreten Quanten $ \hbar \cdot \omega _{\mathrm {E} }$ aufnehmen|kinetische Energie $\frac{1}{2} k_\mathrm{B} T$ pro Freiheitsgrad |
|nur Schwingungszustände mit $K \le K_\mathrm{D}$, Vernachlässigung optischer Moden|  optische Phononen|plus nochmal gleiche potentielle Energie|
|$T_\mathrm{D}=\Theta _{{\mathrm {D}}}={\frac {\hbar \cdot \omega _{{\mathrm {D}}}}{k_{{\mathrm {B}}}}}={\frac {\hbar \cdot v_{{\mathrm {D}}}}{k_{{\mathrm {B}}}}}\cdot {\sqrt[ {3}]{{\frac {6\cdot \pi ^{2}\cdot N}{V}}}}$| $\Theta_\mathrm{E}=\frac{\hbar \omega_\mathrm{E}}{k_\mathrm{B}}$|
|$\omega_\mathrm{D}=\sqrt[ {3}]{{\frac {6\cdot \pi ^{2}\cdot v_\mathrm{s}^3 N}{V}}}=v_\mathrm{s}\cdot K_\mathrm{D}$|$\omega_\mathrm{E}$, nur eine Frequenz| |
|$D_{3d}(\omega)=\frac{V}{2\pi^2v_\mathrm{s}^3} \omega^2$|$D(\omega)=N \delta(\omega-\omega_E)$|
|$K_\mathrm{D}=\sqrt[{3}]{6\cdot \pi^2\frac{N}{V}}=\frac{\omega_\mathrm{D}}{v_\mathrm{s}}$| | |
|für $T \ll \Theta_\mathrm{D}$ gilt $C_V^\mathrm{D}=\frac{12 \pi^4}{5} N k_\mathrm{B} (\frac{T}{\Theta})^3 \propto T^3$| $C_V^\mathrm{E}=\begin{cases}   3Nk_\mathrm{B} \big(\frac{\Theta_E}{T} \big)^2 e^{-\Theta_E/T} &\text{für } T\ll \Theta_E \\   3Nk_\mathrm{B} &\text{für } T\gg \Theta_E \end{cases} $|$3Nk_\mathrm{B}$|



                                      {{3}}
![molare Wärmekapazität](media/MolareWaermekapazitaet.png "*Molare Wärmekapazität der Festkörper nach den Theorien von Einstein, Debye und Dulong-Petit Quelle: Hering, E., Martin, R., Stohrer, M., Käß, H. (2016). [Festkörperphysik In: Physik für Ingenieure](https://link.springer.com/chapter/10.1007/978-3-662-49355-7_9). Springer Vieweg, Berlin, Heidelberg.* ")


## Aufgabe 2 

                                      {{0}}
> __2.__ Was versteht man bei einer Phonon-Phonon-Wechselwirkung unter einem Normalprozess und unter einem Umklappprozess? Was muss für die Phononen gelten, damit Umklappprozess überhaupt möglich sind?

                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}
Die Umklapp-Streuung (auch U-Prozess oder Umklapp-Prozess) ist ein Streuprozess, der zu einem Wellenvektor $K$ führt, der außerhalb der ersten Brillouin-Zone liegt. Der Wellenvektor wird durch einen reziproken Gittervektor $G$ in die erste Brillouin-Zone transformiert. Diese Transformation ermöglicht Streuprozesse, die andernfalls gegen den Impulserhaltungssatz verstoßen würden: Zwei nach rechts gerichtete Wellenvektoren können sich zu einem nach links gerichteten Wellenvektor verbinden. Diese Nichterhaltung ist der Grund, warum der Kristallimpuls kein echter Impuls ist.

                                      {{3}}
![Bild von  Normal- und Umklappprozess ](https://upload.wikimedia.org/wikipedia/commons/e/ef/Phonon_nu_process.svg "*Normal process (N-process) and Umklapp process (U-process). While the N-process conserves total phonon momentum, the U-process changes phonon momentum; Quelle: [Wikipedia Daniel Schwen](https://en.wikipedia.org/wiki/Umklapp_scattering) , [CC BY-SA 3.0](http://creativecommons.org/licenses/by-sa/3.0/&gt)*")

                                      {{4}}
Es gilt der Energieerhaltungssatz:
$$\begin{align*}
E_1+E_2&=E_3\\
\hbar\omega_1+\hbar\omega_2&=\hbar\omega_3\\
\omega_1+\omega_2&=\omega_3
\end{align*}$$

                                      {{5}}
Und der Impulserhaltungssatz:
$$K_1+K_2=K_3+G$$
Bei $G=0$ liegt ein Normalprozeß vor, bei $G\ne 0$ ein Umklappprozeß. 

                                      {{6}}
Für Umklapp-Prozesse müssen $K_1$ und $K_2$  $\ge \frac{1}{2}G$ bzw. $E_1$ und $E_2$ $\ge \frac{1}{2}k_\mathrm{B} \Theta_\mathrm{D}$ sein, da jeder Phononenwellenvektor in der Größenordnung von $ \frac{1}{2}G$ sein muss.


## Aufgabe 3
                                      {{0}}
> __3.__ Welche geometrischen und inneren Effekte können die mittlere freie Weglänge von Phononen begrenzen?


                                      {{1}}



**Lösung Aufgabe 3:**

                                      {{2}}
- Streuung an Fremdatomen
- Streuung an Isotopen bzw. Isotopenverteilung
- Streuung an Gitterfehlern
- Streuung an Kristallgrenzen


## Aufgabe 4 
                                      {{0}}
> __4.__ Wie lauten die Verteilungsfuktionen für die Bose-Einstein-Verteilung, die Maxwell-Bolzmann-Verteilung und die Fermi-Dirac-Verteilung?


                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}

Bose-Einstein Verteilungsfunktion für Bosonen (ganzzahliger Spin, Zustände mehrfach besetzbar) z.B. Phononen:

                                      {{3}}
$$f(E)=\frac{1}{e^{\frac{E-E_\mathrm{F}}{k_\mathrm{B} T}  }-1}$$

                                      {{4}}
Fermi- Dirac Verteilungsfunktion für Fermionen (halbzahliger SpinZustände nur einfach besetzbar), z.B. Elektronen

                                      {{5}}
$$f(E)=\frac{1}{e^{\frac{E-E_\mathrm{F}}{k_\mathrm{B} T}}  +1}   $$

                                      {{6}}
Maxwell-Boltzman Verteilungsfunktion

                                      {{7}}
$$f(E)=\frac{1}{e^{\frac{E-E_\mathrm{F}}{k_\mathrm{B} T}} }= e^{-\frac{E-E_\mathrm{F}}{k_\mathrm{B} T}}  $$


                                      {{8}}
![Bild der Bose-Einstein Verteilung, der Fermi-dirac-Verteilung und der Maxwell-BoilzmannVerteilung ](media/Fermi-Dirac-Bose-Einstein-Maxwell.png "*Bose-Einstein-, Fermi-Dirac- und Maxwell-Boltzmann-Verteilungen in Abhängigkeit von der Energie. Für die Bose-Einstein-Verteilung wurde $\mu = 0$, für die Fermi-Dirac-Verteilung $\mu = 5 k_\mathrm{B}T $ gewählt. Für die Maxwell-Boltzmann-Verteilungen wurde ebenfalls $\mu = 0$ und  $\mu = 5 k_\mathrm{B}T $ gewählt, so dass die klassische Verteilung mit der quantenmechanischen Verteilung für große Werte von $\varepsilon /k_\mathrm{B}T$ zusammenfallen; Quelle: [Rudolf Gross, Physik IV Atome, Moleküle, Wärmestatistik, Walther-Meissner-Institut](https://www.wmi.badw.de/fileadmin/WMI/Lecturenotes/Physics_4/Physik4_Kapitel13.pdf)*")

                                      {{8}}
oder zum Ausprobieren eine [Online-Mathematica-Demonstration](https://demonstrations.wolfram.com/BoseEinsteinFermiDiracAndMaxwellBoltzmannStatistics/)



## Aufgabe 5 

                                      {{0}}
> __5.__ Wie viele Gitterschwingungen $\Delta N$ gibt es nach der Bose-Einstein-Verteilung bei $T=300\,\mathrm{K}$ in einem Kristall mit einem Volumen von $\mathrm{1\, cm^3}$ im Frequenzbereich zwischen $4,0$ und $4,1\,\mathrm{MHz}$ (Schallgeschwindigkeit  $v_\mathrm{s}=6000\,\mathrm{\frac{m}{s}}$)?

                                      {{1}}
**Lösung Aufgabe 5:**

                                      {{2}}
Zahl der Phononen im Bereich $\omega_1$ bis $\omega_2$ im 3D:

                                      {{3}}
$$ \begin{align*}
\Delta N&=3\int_{\omega_1}^{\omega_2} D(\omega)\cdot \frac{1}{e^\frac{\hbar \omega}{k_\mathrm{B} T}-1} d\omega\\
&=3\int_{\omega_1}^{\omega_2} \frac{l^3 \omega^2}{2\pi^2 v_\mathrm{s}^3}\cdot \frac{1}{e^\frac{\hbar \omega}{k_\mathrm{B} T}-1} d\omega\\
&=3\int_{f_1}^{f_2} \frac{l^3 (2\pi f)^2}{2\pi^2 v_\mathrm{s}^3}\cdot \frac{1}{e^\frac{\hbar 2\pi f}{k_\mathrm{B} T}-1} d(2\pi f)
\end{align*}$$

                                      {{4}}
mit $\omega = 2\pi f$ 

                                      {{5}}
Betrachten wir den Exponenten im Exponentialterm für die größte Frequenz $4,1\,\mathrm{MHz}$:
$$\frac{hf}{k_\mathrm{B} T}=\mathrm{\frac{6,6\cdot 10^{-34}Js\cdot 4,1 \, MHz}{1,381\cdot 10^{-23}\frac{J}{K} \cdot 300\,K}}=6,5\cdot 10^{-7}$$

                                      {{6}}
Der Exponent ist also sehr klein, die Exponentailfunktion lässt sich deshalb gut als Taylorreihenentwicklung $e^x=1+x+\frac{x^2}{2!}+\frac{x^2}{3!}+...$  darstellen, wobei die Reihe nach dem linearen Term abgebrochen werden kann.

                                      {{7}}

$$ \begin{align*}

&\overbrace{\approxeq}^{hf \ll k_\mathrm{B}T} 3\int_{f_1}^{f_2} 2\pi \frac{l^3 (2\pi f)^2}{2\pi^2 v_\mathrm{s}^3}\cdot \frac{1}{1+x-1} d f\\
&= 3\int_{f_1}^{f_2} 2\pi \frac{l^3 (2\pi f)^2}{2\pi^2 v_\mathrm{s}^3}\cdot \frac{1}{\frac{hf}{k_\mathrm{B} T}} d f\\
&=\frac{12\pi l^3 k_\mathrm{B} T}{v_\mathrm{s}^3 h}\int_{f_1}^{f_2}fdf\\
&=\frac{12\pi l^3 k_\mathrm{B} T}{v_\mathrm{s}^3 h}\bigg(\frac{f_2^2-f_1^2}{2}\bigg)\\
\end{align*}$$

                                      {{8}}
Mit 

                                      {{8}}
- $f_1 = 4,0 \cdot 10^6\, \frac{1}{s}$ , 
- $f_2 = 4,1 \cdot 10^6\, \frac{1}{s}$,
- $v_\mathrm{s} = 6000 \, \mathrm{\frac{m}{s}}$,
- $T = 300 \, \mathrm{K}$,
- $l^3 = 1\, \mathrm{cm^3}$
- $h = 6,63 \cdot  10^{-34} \,\mathrm{Js}$, und 
- $k_\mathrm{B} = 1,38 \cdot 10^{-23}\, \mathrm{\frac{J}{K}}$ 

                                      {{9}}
folgt:

                                      {{9}}
$$ \Delta N = 4,4 \cdot  10^8$$

                                      {{10}}
Die Zahl der verschiedenen Energie-Eigenwerte im gleichen Frequenzbereich ist dabei:

$$ \begin{align*}
D(\omega)d(\omega) &=3 \frac{l^3 \omega^2}{2\pi^2 v_\mathrm{s}^3}\cdot \Delta \omega\\
&=3\cdot\frac{(0,01\mathrm{m})^3\cdot \left( 2\cdot \pi\frac{4,0 \cdot 10^6 \mathrm{\frac{1}{s}}+4,1 \cdot 10^6 \mathrm{\frac{1}{s}}}{2}\right)^2}{2\cdot \pi^2\cdot (6000\mathrm{\frac{m}{s}})^3}\cdot (4,1 \cdot 10^6 \mathrm{\frac{1}{s}}-4,0 \cdot 10^6 \mathrm{\frac{1}{s}})\\
&\approxeq 286


\end{align*}$$

 


## Aufgabe 6 

                                      {{0}}
> __6.__ Ein Laserstrahl  der Wellenlänge $\lambda=694\, \mathrm{nm}$ durchläuft einen Quarzkristall. Dabei findet eine inelastische Wechselwirkung zwischen Photonen und akustischen Phononen ohne Gitter-Rückstoß statt (Brillouin-Streunung). Berechnen Sie die maximale Frequenz der hierdurch ausgelösten mechanischen Schwingungen und geben Sie die Frequenzverschiebung des gestreuten Lichtes an. (Schallgeschwindigkeit $v_\mathrm{s} = 6000 \,\mathrm{\frac{m}{s}}$, Brechungsindex des Kristalls $n=1,54$)

                                      {{1}}
**Lösung Aufgabe 6:**

                                      {{2}}
Seien $\omega, k$ die Frequenzen und Wellenvektoren  der Photonen und $\Omega, K$ die der Phononen

                                      {{3}}
Energieerhaltungssatz: $\hbar \omega_0=\hbar \omega_1 + \hbar \Omega $

                                      {{4}}
Impulserhaltungssatz: $k_0=k_1+K$

                                      {{5}}
Für Rückstreuung gibt es den maximalen Impulsübertragung $k_1 = -k_0$  und damit $K = 2k_0$

                                      {{6}}
Mit dem Zusammenhang $k=\frac{2\pi}{\lambda_n}=n\frac{2\pi}{\lambda_\mathrm{vac}}$ 

                                      {{7}}
und der Dispersionsrelation für akustische Phononen: $\Omega = v_\mathrm{s} \cdot K =$  folgt:

                                      {{8}}
$$\begin{align*}
\Omega&=v_\mathrm{s} \cdot K\\
&=v_\mathrm{s} \cdot 2k_0\\
&=v_\mathrm{s} \cdot 2 \cdot n\frac{2\pi}{\lambda_\mathrm{vac}}\\
&=6000 \,\mathrm{\frac{m}{s}} \cdot 2 \cdot 1,54 \cdot \frac{2\pi}{694\cdot 10^{-9} \mathrm{m}}\\
&=1,67 \cdot 10^{11} \mathrm{\frac{1}{s}}
\end{align*}$$

                                      {{9}}
Die Frequenzverschiebung $\Delta \omega=-\Omega=\omega_1-\omega_0$ folgt aus dem Energieerhaltungssatz:
$$- \Omega= \omega_1 -  \omega_0 $$
$$\begin{align*}-\frac{\Omega}{2\pi}&=f_1 -  f_0\\
-\frac{1,67 \cdot 10^{11} \mathrm{\frac{1}{s}}}{2\pi}&=f_1 -  f_0\\
-2,66 \cdot 10^{10}\mathrm{\frac{1}{s}}&=\Delta f
\end{align*} $$


                                      {{10}}
Mit der ursprünglichen Frequenz des Lasers $f_0 = \frac{c}{\lambda}=\frac{3\cdot 10^8 \mathrm{\frac{m}{s} }}{694\cdot 10^{-9} \mathrm{m}}= 4,32 \cdot  10^{14} \mathrm{Hz}$

                                      {{11}}
Die relative Frequenzabnahme beträgt damit:

                                      {{12}}
$$\frac{\Delta f}{f_0}  = \frac{2,66 \cdot 10^{10}\mathrm{\frac{1}{s}}}{4,32 \cdot  10^{14} \mathrm{\frac{1}{s}}}=6,15 \cdot 10^{-5}$$


## Aufgabe 7

                                      {{0}}
>__7.__ Welche obere Grenzfrequenz haben Gitterschwingungen in NaCl (Debye-Temperatur $\Theta_\mathrm{D}=\mathrm{ 322 \,K}$)?

                                      {{1}}
**Lösung Aufgabe 7:**

                                      {{2}}
$$\Theta_\mathrm{D}=\mathrm{ 322 \,K}$$

                                      {{3}}
$$\Rightarrow \omega_\mathrm{D}=\frac{k_\mathrm{B} \Theta_\mathrm{D}}{\hbar}=\frac{1,38 \cdot 10^{-23}\, \mathrm{\frac{J}{K}} \cdot  \mathrm{ 322 \,K}}{1,0546 \cdot  10^{-34} \,\mathrm{Js}}=4,21 \cdot 10^{13}\mathrm{\frac{1}{s}}$$

                                      {{4}}
$$\Rightarrow f_\mathrm{D}=\frac{\omega_\mathrm{D}}{2\pi}=\frac{4,21 \cdot 10^{13}\mathrm{\frac{1}{s}}}{2\pi}=6,71 \cdot 10^{12}\mathrm{\frac{1}{s}}=6,71 \cdot 10^{12}\mathrm{Hz
}$$


## Aufgabe 8

                                      {{0}}
>__8.__ Wie groß ist die molare Wärmekapazität für Aluminium bei einer Temperatur von $T=50\, \mathrm{K}$ ($\Theta_\mathrm{D}=\mathrm{400 \,K}$)?

                                      {{1}}
**Lösung Aufgabe 8**

                                      {{2}}
$$\begin{align*}
C_V&=\frac{12 \pi^4 }{5}Nk_\mathrm{B}\bigg(\frac{T}{\Theta_\mathrm{D}}\bigg)^3\\
&=\mathrm{\frac{12 \pi^4 }{5}\cdot 6,02214\cdot 10^{23} \frac{1}{mol}\cdot 1,38 \cdot 10^{-23}\mathrm{\frac{J}{K}}\bigg(\frac{50\, K}{400\, K}\bigg)^3}\\
&=\mathrm{3,79 \frac{J}{mol\cdot K} }
\end{align*}$$