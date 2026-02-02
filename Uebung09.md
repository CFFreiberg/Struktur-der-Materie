<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 9
@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->


# Übung 9: 


## Aufgabe 1
                                      {{0}}
> __1.__ Edelgaskristalle werden durch das Lennard-Jones Potential beschrieben. Wie lautet die Gleichung für dieses Potential und welche Anteile sind darin wo enthalten? Welcher Anteil ist abstoßend, welcher anziehend?



                                      {{1}}
**Lösung Aufgabe 1:**

                                      {{2}}
Lennard-Jones Potential:
$$ U(R)=4 \varepsilon \left [ \left ( \frac{\sigma}{R} \right)^{12}-\left(\frac{\sigma}{R}\right)^6\right]$$
Der positive  hoch-12-Term ist abstoßend (Pauli Prinzip).  
Der negative hoch 6-Term ist anziehend (van der Waals-Wechselwirkung = induzierte Dipol-Dipol Welchselwirkung)  

                                      {{3}}
************************************
Im folgenden Python-Code können Sie unten links auf Ausführen (</>) drücken, dann bekommen Sie eine Abbildung der einzelnen Anteile des Lennard-Jones Potentials



``` python
# Quelle: zusammenkopiert aus https://matplotlib.org

import sys
import numpy as np
import matplotlib.pyplot as plt

# So that the axis labels are not cut off
from matplotlib import rcParams
rcParams.update({'figure.autolayout': True})

# The parametrized function to be plotted
def f1(variable):
    return 1/variable**12
def f2(variable):
    return -1/variable**6
def f3(variable):
    return (1/variable**12)-(1/variable**6)


def main():
    x_min = 0.8
    x_max = 1.8
    x_num = 100
    y_min = -1
    y_max = 1
    x_label = "$\\dfrac{R }{\\sigma}$"
    y_label = "$\\dfrac{U }{4\\cdot\\varepsilon}$"
    x = np.linspace(x_min, x_max, x_num)
    fig, ax = plt.subplots()
    line, = ax.plot(x, f1(x),'r--')
    line, = ax.plot(x, f2(x),'b--')
    line, = ax.plot(x, f3(x),'g')
    plt.legend(("$+\\left (\\dfrac{\\sigma}{R}\\right)^{12}$", "$-\\left (\\dfrac{\\sigma}{R}\\right)^{6}$", "$+\\left (\\dfrac{\\sigma}{R}\\right)^{12}-\\left (\\dfrac{\\sigma}{R}\\right)^{6}$" ),loc='upper center', shadow=True)
    plt.grid(True)
    ax.set_xlabel(x_label)
    ax.set_ylabel(y_label)
    ax.set_ylim(y_min, y_max)
    
    plt.show()
main()
```
@Pyodide.eval(`["main.py"]`, `python3 -m compileall .`, `python3 main.py`)
************************************

                                      {{4}}
![Lennard-Jones-Potential mit abstoßendem und anziehendem Anteil](media/Lennard-Jones-potential2.png "[Lennard-Jones-Potential; Quelle: MSU Department of Physics and Astronomy, Computational Math Science and Engineering and the Lyman Briggs College](https://physicsatmcl.commons.msu.edu/lennard-jones-potential/), [CC BY-NC-SA 4.0 Deed](https://creativecommons.org/licenses/by-nc-sa/4.0/)")




## Aufgabe 2
                                      {{0}}
> __2.__ Beschreiben Sie mit Hilfe des Lennard-Jones Potentials die Kraft zwischen zwei Edelgas-Atomen!


                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}
$$F=-\left| \vec{\nabla }U(r) \right|=-\frac{\mathrm{d}U(r)}{\mathrm{d}r}$$

                                      {{3}}
$$\begin{align*}

\Rightarrow F&=\ -4\varepsilon\left(\frac{-12\sigma^{12}}{r^{13}}-\ \frac{-6\sigma^6}{r^7}\right)\\
&=\ \frac{24\varepsilon}{r}\ \left[2\left(\frac{\sigma}{r}\right)^{12}-\left(\frac{\sigma}{r}\right)^6\right] 
\end{align*}$$

## Aufgabe 3 
                                      {{0}}
> __3.__ Wie groß ist ungefähr der van der Waals Beitrag zur anziehenden Wechselwirkung in Ionenkristallen und wie wird der Hauptbeitrag der Bindungsenergie in Ionenkristallen noch genannt?

                                      {{1}}
**Lösung Aufgabe 3:**

                                      {{2}}
Der Beitrag der  van der Waals-Wechselwirkung zur anziehenden Wechselwirkung beträgt ca. 1 – 2%  
Der Hauptbeitrag der anziehenden Wechselwirkung ist die elektrostatische Anziehung, die auch **Madelung-Energie** genannt wird.


## Aufgabe 4 

                                      {{0}}
> __4.__ Wie groß ist die gesamte Gitterenergie (elektrostatische Energie) in Ionenkristallen mit 2N Atomen (Formel)?

                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}
Die gesamte Gitterenergie ist die Summe über alle Wechselwirkungsenergien zwischen allen $2N$ Atomen:
$$U_i=\ \sum_{j\ \neq i}\ U_{ij}$$

                                      {{3}}
************************************
Dabei ist die Wechselwirkungsenergie 
$$U_{ij}(R)\ = \begin{cases}
\overbrace{\lambda \cdot  \exp\bigg(\frac{-R}{\rho}\bigg)}^{\mathrm{Abstoßung}} -\frac{q^2}{4 \pi \varepsilon_0 R}  &\text{für nächste Nachbarn}\\
\pm\frac{1}{p_{ij}}\frac{q^2}{4\pi\varepsilon_0 \cdot R}  &\text{alle anderen geometrischen Fälle}  
\end{cases} $$


Dabei sind $\lambda$ und $\rho$  materialabhängige Parameter und $p_{ij}=\frac{r_{ij}}{R}$ der relative Abstand .
************************************

                                      {{4}}
Mit der **Madelung-Konstanten**
$$\alpha =\ \sum_{j}\pm\frac{1}{p_{ij}} $$
und der Anzahl der nächsten Nachbarn $z$ ergibt sich

                                      {{5}}
$$U_G(R)=\ N\cdot U_i=N\bigg(z \cdot \lambda\cdot \exp\left(\frac{-R}{\rho}\right)-\frac{\alpha \cdot  q^2}{4\pi\varepsilon_0 \cdot R}\bigg)$$

                                      {{6}}
Der Gleichgewichtsabstand ergibt sich aus $\frac{\mathrm{d}U_G}{\mathrm{d}R} = 0$ 

                                      {{7}}
$$-\frac{N}{\rho}z\ \lambda \exp \left(\frac{-R_{0}}{\rho}\right)+\frac{N\ \alpha \cdot  q^2}{4\pi\varepsilon_0 \cdot R_0^2}\ = 0$$

                                      {{8}}
$$\Rightarrow z\ \lambda \exp \left(\frac{-R_0}{\rho}\right)= \frac{ \rho \cdot \alpha \cdot  q^2}{4\pi\varepsilon_0 \cdot R_0^2} $$

                                      {{9}}
Damit ergibt sich für den Gleichgewichtsabstand $R_0$ die gesamte Gitterenergie
$$U_G=-N\frac{\alpha \cdot  q^2}{4\pi\varepsilon_0 \cdot R_0}\bigg(1-\frac{\rho}{R_0}\bigg)$$

## Aufgabe 5 
                                      {{0}}
>__5.__ Auf welche energetische Erniedrigung ist die Metallbindung zurückzuführen?

                                      {{1}}
**Lösung Aufgabe 5:**

                                      {{2}}
Bei der metallischen Bindung sind die Valenzelektronen gleichmäßig über das ganze Metall "verschmiert" und sind nicht an einem oder zwei Atomen lokalisiert (im Gegensatz zur kovalenten Bindung). Diese Valenzelktronen bilden einen "See" von ungebundenen, delokalisierten Elektronen, in dem die verbleibenden positiven Ionenrümpfe eingebettet sind. Die Bindungsenergie der metallischen Bindung kommt durch die Reduktion der kinetischen Energie der Valenzelektronen zustande.

                                      {{3}}
Zusatzinfos:
Da die metallische Bindung ungerichtet ist, kristallisieren Metalle hauptsächlich in dicht gepackten Strukturen. Die Bindungsenergie ist mit ca. 1 eV eher klein. Die Bindungsenergie von Alkalimetallen (Li, Na, K, Rb, Cs, Fr) ist wesentlich kleiner als die von Alkali-Halogenid-Kristallen (LiF, NaCl), da bei ersteren die interatomaren Abstände größer sind, was zu einer Verringerung der kinetischen Energie der Valenzeleektronen führt. Bei Übergangsmetallen gibt es wegen der Wechselwirkung zwischen inneren Elektronenschalen (d-Elektronen) höhrere Bindungsenergien.

## Aufgabe 6 

                                      {{0}}
>__6.__ Nennen Sie Charakteristika der kovalenten Bindung!

                                      {{1}}
**Lösung Aufgabe 6:**

                                      {{2}}
- stark gerichtete Bindung
- Überlappung von Ladungsverteilungen von Elektronen mit antiparallelem Spin (Elektronenpaar-Bindung)
- Die überlappenden Elektronen binden ihre zugehörigen Ionenrümpfe durch die spinabhängige Coulombenergie (elektrostatische Anziehung, Austauschwechselwirkung)
- hohe Bindungsenergie. Viele kovalente, räumlich ausgerichtete Bindungen haben eine größere Bindungsenergie als ungerichtete ionische Bindungen.
- Beispiele: $\mathrm{H_2}$-Molekül, Diamant, Silizium


## Aufgabe 7 

                                      {{0}}
>__7.__ Beschreiben Sie die Wasserstoffbrückenbindung!

                                      {{1}}
**Lösung Aufgabe 7:**

                                      {{2}}
- ein Wasserstoff-Atom oder Proton (H+) wird von zwei Atomen mit starken Kräften angezogen. An dem einem Atom ist es kovalent gebunden, das andere elektronegativere Atom hat ein freies Elektronenpaar.
- weitgehend ionische Bindung (Bindungsenergie ~ 0.1 eV)
- Brücke zwischen **maximal 2 Atomen**
- besonders zwischen F–H...F, O-H...O, N-H...F, C-H...N 
- Wechselwirkung zwischen Wassermolekühlen

Wasserstoffbrückenbindungen sind maßgeblich für die besonderen physikalischen Eigenschaften des Wassers verantwortlich. Sie bewirken unter anderem die vergleichsweise hohe Oberflächenspannung von Wasser, die es Insekten wie dem Wasserläufer ermöglicht, sich auf der Wasseroberfläche fortzubewegen. Aufgrund dieser hohen Oberflächenspannung neigt Wasser außerdem zur Ausbildung von Tropfen.

Darüber hinaus spielen Wasserstoffbrückenbindungen eine zentrale Rolle bei der Struktur des Wassers im festen Aggregatzustand. Im Eis führen sie zu einer offenen, geordneten Gitterstruktur, die bewirkt, dass Eis eine geringere Dichte als flüssiges Wasser besitzt. Dieses ungewöhnliche Verhalten wird als Anomalie des Wassers bezeichnet: Wasser erreicht seine maximale Dichte bei etwa 4 °C. Infolgedessen schwimmt Eis auf flüssigem Wasser, anstatt abzusinken.

Wasserstoffbrückenbindungen sind jedoch keineswegs auf Wasser beschränkt, sondern in der Natur und insbesondere in der Biochemie weit verbreitet. In der DNA werden die komplementären Basenpaare durch Wasserstoffbrückenbindungen zusammengehalten. Auch in Proteinen tragen Wasserstoffbrückenbindungen wesentlich zur Stabilisierung sekundärer und tertiärer Strukturelemente bei und sind damit entscheidend für deren räumliche Struktur und Funktion.


## Aufgabe 8 
                                      {{0}}
************************************
>__8.__ Berechnen Sie zunächst die Madelungkonstante eines ebenen quadratischen Kristallgitters, berücksichtigen sie dabei Nachbarn, die in einem Quadrat mit der Kantenlänge von drei mal nächster-Nachbar-Abstand um ein Zentralatom liegen (siehe Abbildung unten). Nachbaratome auf dieser „Grenze“ werden nur anteilsmäßig miterfasst. 


![Abbildung eines ebenen Ionengitters zur Veranschaulichung der Berechnung der Madelung-Konstanten](media/EbenesGitterMadelung.png "*Quelle:  A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik*")<!--width="50%"-->


> Berechnen Sie dann die Näherung der Madelung-Konstanten für ein 3-dimensionalses Gitter für den in der Abbildung gezeigten Ausschnitt!


![Abbildung eines dreidimensionalen Ionengitters zur Veranschaulichung der Berechnung der Madelung-Konstanten](media/3D-GitterMadelung.png "*Quelle:  A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik*")<!--width="50%"-->
************************************

                                      {{1}}
**Lösung Aufgabe 8:**

                                      {{2}}
Die Madelung Konstante $\alpha$ ist definiert als 
$$\alpha\ =\ \sum_{j}\frac{\pm}{p_{ij}}$$
wobei $R\cdot p_{ij}$ der Abstand  der Atome zueinander ist. Für Ionen mit gleichem Vorzeichen wird per Definition ein "+" verwendet, für Ionenpaare mit unterschiedlichem Vorzeichen der Ladung ein "-".

                                      {{3}}
Für das ebene Gitter gilt: $\alpha_{3\ }=$

                                      {{4}}
$$\begin{align*} 
\alpha_{3\ }&=\ 4\frac{+1}{1}\ +\ 4\frac{-1}{\sqrt2} &\text{erstes Quadrat}\\
 &+\ 4\frac{-1}{2}+8\frac{+1}{\sqrt5}+4\frac{-1}{2\sqrt2} &\text{zweites Quadrat}\\
&+4\frac{+1}{3}\frac{1}{2}+8\frac{-1}{\sqrt{10}}\frac{1}{2}
+8\frac{+1}{\sqrt{13}}\frac{1}{2}+4\frac{-1}{3\sqrt2}\frac{1}{4}  &\text{drittes Quadrat}\\
&=\ 1,611..
\end{align*}$$

                                      {{5}}
Für das gezeigte 3D-Gitter gilt:
$$\begin{align*} 
\alpha_1 &=\ 6\frac{+1}{1}\frac{1}{2}\ +12\frac{-1}{\sqrt2}\frac{1}{4}+8\frac{+1}{\sqrt3}\frac{1}{8}\\
 &=\ 1,456..
\end{align*}$$

## Aufgabe 9
                                      {{0}}
>__9.__ Berechnen Sie das Verhältnis der Bindungsenergien und die Gleichgewichtsabstände von Neonkristallen jeweils mit einer bcc-, hcp-, und fcc- Struktur mit Hilfe des Lennard – Jones – Potentials als Funktion von $\sigma$, $\varepsilon$, $N$. Die Gittersummen sind mit $\alpha_{ij}=\frac{r_{ij}}{R}$ gegeben durch 

|Gitter| $A_{6}=\sum\limits_{i,j\ne i}\alpha_{ij}^{-6}$ | $A_{12}=\sum\limits_{i,j\ne i} \alpha_{ij}^{-12} $|
|:---:|:---:|:----:|
|bcc|12,253|9,114|
|hcp|14,4549|12,1323|
|fcc|14,4539|12,1319|

>Welche Struktur erwartet man theoretisch für den Neonkristall? Experimentell stellt man fest, dass Neon in der fcc - Struktur kristallisiert. Welche Gründe könnte es für die Abweichung geben?

                                      {{1}}
**Lösung Aufgabe 9:**

                                      {{2}}
Mit dem Lennard- Jones Potential 
$ U(r)=4 \varepsilon \left [ \left ( \frac{\sigma}{R} \right)^{12}-\left(\frac{\sigma}{R}\right)^6\right]$ ergibt sich für die Gesamtenergie $U_\mathrm{G}$ bei insgesamt $N$ Atomen und damit $\frac{N}{2}$ Atompaaren

                                      {{3}}
$$\begin {align*}
U_\mathrm{G}&=\frac{4N}{2} \varepsilon\left[\sum\limits_{i,j\ne i}{\left(\frac{\sigma}{r_{ij}}\right)^{12}}-\sum\limits_{i,j\ne i}\left(\frac{\sigma}{r_{i,j}}\right)^6\right]\\
&= 2N\varepsilon\left[\sum\limits_{i,j\ne i}{\left(\frac{\sigma}{\alpha_{ij}\cdot R}\right)^{12}}-\sum\limits_{i,j\ne i}\left(\frac{\sigma}{\alpha_{i,j}\cdot R}\right)^6\right]\\
&=2N\varepsilon\left[A_{12}\left(\frac{\sigma}{R}\right)^{12}-A_6\left(\frac{\sigma}{R}\right)^6\right]\end{align*}$$

                                      {{4}}
Für den Gleichgewichtsabstand $R_0$ muss die Gesamtenergie ein Minimum haben, also $\frac{dU_\mathrm{G}}{dR}\vert_{R_0}=0$ gelten:  

                                      {{5}}
$$\frac{dU_\mathrm{G}}{dR} \bigg|_{R_0}=-2N\varepsilon \left[12A_{12}\frac{\sigma^{12}}{R_0^{13}}-6 A_6\frac{\sigma^6}{R_0^7} \right]=0\\$$

                                      {{6}}
$$\Rightarrow 2A_{12}\frac{\sigma^{12}}{R_0^{13}}=A_6\frac{\sigma^6}{R_0^7}$$

                                      {{7}}
$$\Rightarrow \frac{2A_{12}}{A_6}\sigma^6=R_0^6$$

                                      {{8}}
$$\Rightarrow \color{blue} R_0=\sigma\bigg(\frac{2A_{12}}{A_6}\bigg)^\frac{1}{6} $$

                                      {{9}}
Damit ergibt sich die gesamte Bindungsenergie zu 
$$
\begin{align*}U_\mathrm{G}(R_0)&=4\frac{N}{2}\varepsilon\left[A_{12}\left(\frac{\sigma}{\color{blue}\sigma\bigg(\frac{2A_{12}}{A_6}\bigg)^\frac{1}{6}}\right)^{12}-A_6\left(\frac{\sigma}{\color{blue}\sigma\bigg(\frac{2A_{12}}{A_6}\bigg)^\frac{1}{6}}\right)^6\right] \\
&=2N\varepsilon \left[A_{12}\bigg(\frac{A_6}{2A_{12}}\bigg)^2-A_6\frac{A_6}{2A_{12}} \right] \\
&=2N\varepsilon \left[\frac{A_6^2}{4A_{12}}-\frac{A_6^2}{2A_{12}} \right]\\
&=-\frac{N\varepsilon}{2}\frac{A_6^2}{A_{12}}
\end{align*}$$

                                      {{10}}
Mit dieser Formel kann für jede Gittervariante mit den gegebenen $A_6$ und $A_{12}$ der Gleichgewichtsabstand $R_0$ und die gesamte Bindungsenergie berechnet werden:

                                {{11}}
|Gitter| $R_0$ | $U_\mathrm{G}$|
|:---:|:---:|:----:|
|bcc|$1,068438\cdot \sigma$|$-8,23656 \cdot N\varepsilon$ |
|hcp|$1,090167\cdot \sigma$|$\color{red}-8,61107 \cdot N\varepsilon$|
|fcc|$1,090173\cdot \sigma$|$-8,61016 \cdot N\varepsilon$|

                                {{12}}
Daraus folgt:

                                {{13}}
$$U_\mathrm{G}^{\mathrm{hcp}}:U_\mathrm{G}^{\mathrm{fcc}}:U_\mathrm{G}^{\mathrm{bcc}}=1:0,99989:0,95660$$

                                {{14}}
- Theoretisch wäre also das hcp-Gitter am stabilsten, aber die energetischen Unterschiede zum fcp-Gitter sind klein. 
- Das bcc-Gitter sollte nicht vorkommen 

                                {{15}}
Experimentell wird aber das fcc-Gitter und dort ein größerer Gleichgewichtsabsatand von $R_0=1,14\cdot \sigma$ beobachtet. Die Ursache sind die Nullpunktsschwingungen der Atome (gekoppelte harmonische Oszillatoren).


## Aufgabe 10
                                      {{0}}
>__10.__ Fester molekularer Wasserstoff: Betrachten Sie die Bindungsenergie von $H_2$-Molekülen im hcp-Gitter, wobei jedes $H_2$-Molekül als eine Kugel vereinfacht wird. Mit Messungen in der Gasphase werden die Parameter des Lennard-Jones-Potentials für $H_2$ bestimmt, es gilt $\varepsilon= 50\cdot 10^{-23} \, \mathrm{J}$ und $\sigma =2,96 \, \AA$. Wie hoch ist die Bindungsenergie (in $\mathrm{\frac{kJ}{mol(H_2)}}$)? 

                                      {{1}}
**Lösung Aufgabe 10:**

                                      {{2}}
In Aufgabe 9 wurde errechnet:
$$
\begin{align*}U_\mathrm{G}(R_0)&=-\frac{N\varepsilon}{2}\frac{A_6^2}{A_{12}}\\
&=-8,61107 \cdot N\varepsilon\\
&=-8,61107 \cdot \frac{6,023 \cdot 10^{23}}{\mathrm{mol}} \cdot 50\cdot 10^{-23} \, \mathrm{J}\\
&=-2593\, \mathrm{\frac{J}{mol}} =-2,59 \, \mathrm{\frac{kJ}{mol}}
\end{align*}$$

                                      {{3}}
Anmerkung: Der beobachtete Wert der Bindungsenergie ist $-0,751 \mathrm{\frac{kJ}{mol}}$, also wesentlich weniger als berechnet. Quantenmechanische Korrekturen spielen hier eine wichtige Rolle.
Einen kristallinen Festkörper mit hcp Struktur  bildet Wasserstoff unterhalb von 14,02 K. 