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

-->


# Übung 9: 


## Aufgabe 1
                                      {{0}}
> __1.__ Edelgaskristalle werden durch das Lennard - Jones Potential beschrieben. Wie lautet die Gleichung für dieses Potential und welche Anteile sind darin wo enthalten? Welcher Anteil ist abstoßend, welcher anziehend?



                                      {{1}}
**Lösung Aufgabe 1:**

Lennard- Jones Potential:
$$ U(r)=4 \varepsilon \left [ \left ( \frac{\sigma}{R} \right)^{12}-\left(\frac{\sigma}{R}\right)^6\right]$$
Der positive  hoch-12-Term ist abstoßend (Pauli Prinzip)  
Der negative hoch 6-Term ist anziehend (van der Waals-Wechselwirkung)  


![Lennard-Jones-Potential mit abstoßendem und anziehendem Anteil](media/Lennard-Jones-potential2.png "[Lennard-Jones-Potential; Quelle: MSU Department of Physics and Astronomy, Computational Math Science and Engineering and the Lyman Briggs College](https://physicsatmcl.commons.msu.edu/lennard-jones-potential/), [CC BY-NC-SA 4.0 Deed](https://creativecommons.org/licenses/by-nc-sa/4.0/)")




## Aufgabe 2
> __2.__ Beschreiben Sie mit Hilfe des Lennard - Jones Potentials die Kraft zwischen zwei Edelgas-Atomen!



**Lösung Aufgabe 2:**


$$\begin{align*}
F&=\ -\frac{dU(r)}{dr} \\
\Rightarrow F&=\ -4\varepsilon\left(\frac{-12\sigma^{12}}{R^{13}}-\ \frac{-6\sigma^6}{R^7}\right)\\
&=\ \frac{24\varepsilon}{R}\ \left[2\left(\frac{\sigma}{R}\right)^{12}-\left(\frac{\sigma}{R}\right)^6\right] 
\end{align*}$$

## Aufgabe 3 
> __3.__ Wie groß ist ungefähr der van der Waals Beitrag zur anziehenden Wechselwirkung in Ionenkristallen und wie wird der Hauptbeitrag der Bindungsenergie in Ionenkristallen noch genannt?


**Lösung Aufgabe 3:**

Der Beitrag der  van der Waals-Wechselwirkung zur anziehenden Wechselwirkung beträgt ca. 1 – 2%  
Der Hauptbeitrag der anziehenden Wechselwirkung ist die elektrostatische Anziehung, die auch **Madelung-Energie** genannt wird.


## Aufgabe 4 
> __4.__ Wie groß ist die gesamte Gitterenergie (elektrostatische Energie) in Ionenkristallen mit 2N Atomen (Formel)?


**Lösung Aufgabe 4:**

Die gesamte Gitterenergie ist die Summe über alle Wechselwirkungsenergien zwischen allen $2N$ Atomen:

$$U_i=\ \sum_{j\ \neq i}\ U_{ij}$$

Dabei ist die Wechselwirkungsenergie 



$$U_{ij}\ = \begin{cases}
\lambda \cdot  \exp\bigg(\frac{-R}{\rho}\bigg)\ -\frac{q^2}{4 \pi \varepsilon_0 R}  &\text{für nächste Nachbarn}\\
\pm\frac{1}{p_{ij}}\frac{q^2}{4\pi\varepsilon_0 \cdot R}  &\text{alle anderen geometrischen Fälle}  
\end{cases} $$


Dabei sind $\lambda$ und $\rho$  materialabhängige Parameter und $p_{ij}=\frac{r_{ij}}{R}$ der relative Abstand .

Mit der **Madelung-Konstanten**

$$\alpha =\ \sum_{j}\pm\frac{1}{p_{ij}} $$

und der Anzahl der nächsten Nachbarn $z$ ergibt sich

$$U_G=\ N\cdot U_i=N\bigg(z \cdot \lambda\cdot \exp\left(\frac{-R}{\rho}\right)-\frac{\alpha \cdot  q^2}{4\pi\varepsilon_0 \cdot R}\bigg)$$

Der Gleichgewichtsabstand ergibt sich aus $\frac{dU_G}{dR} = 0$ 


## Aufgabe 5 
>__5.__ Auf welche energetische Erniedrigung ist die Metallbindung zurückzuführen?

**Lösung Aufgabe 5:**


## Aufgabe 6 

>__6.__ Nennen Sie Charakteristika der kovalenten Bindung!

**Lösung Aufgabe 6:**


## Aufgabe 7 

>__7.__ Beschreiben Sie die Wasserstoffbrückenbindung!

**Lösung Aufgabe 7:**


## Aufgabe 8 
>__8.__ Berechnen Sie zunächst die Madelungkonstante eines ebenen quadratischen Kristallgitters, berücksichtigen sie dabei Nachbarn, die in einem Quadrat mit der Kantenlänge von drei mal nächster-Nachbar-Abstand um ein Zentralatom liegen (siehe Abbildung unten). Nachbaratome auf dieser „Grenze“ werden nur anteilsmäßig miterfasst. 



![Abbildung eines ebenen Ionengitters zur Veranschaulichung der Berechnung der Madelung-Konstanten](media/EbenesGitterMadelung.png "*Quelle:  A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik*")




> Berechnen Sie dann die Näherung der Madelung-Konstanten für ein 3-dimensionalses Gitter für den in der Abbildung gezeigten Ausschnitt:


![Abbildung eines dreidimensionalen Ionengitters zur Veranschaulichung der Berechnung der Madelung-Konstanten](media/3D-GitterMadelung.png "*Quelle:  A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik*")

**Lösung Aufgabe 8:**



## Aufgabe 9

>__9__ Berechnen Sie das Verhältnis der Bindungsenergien und die Gleichgewichtsabstände von Neonkristallen jeweils mit einer bcc-, hcp-, und fcc- Struktur mit Hilfe des Lennard – Jones – Potentials als Funktion von $\sigma$, $\varepsilon$, $N$. Die Gittersummen sind mit $\alpha_{ij}=\frac{r_{ij}}{R}$ gegeben durch 

|Gitter| $A_{6}=\sum\limits_{i,j\ne i}\alpha_{ij}^{-6}$ | $A_{12}=\sum\limits_{i,j\ne i} \alpha_{ij}^{-12} $|
|:---:|:---:|:----:|
|bcc|12,253|9,114|
|hcp|14,4549|12,1323|
|fcc|14,4539|12,1319|




>Welche Struktur erwartet man theoretisch für den Neonkristall? Experimentell stellt man fest, dass Neon in der fcc - Struktur kristallisiert. Welche Gründe könnte es für die Abweichung geben?

**Lösung Aufgabe 9:**

## Aufgabe 10

>__10__ Fester molekularer Wasserstoff: Aus Messungen in der Gasphase findet man für $H_2$, dass für die Parameter des Lennard-Jones-Potentials gilt:


$\varepsilon=50\cdot 10^{-16} \,\mathrm{erg= 50 \cdot 10^{-16} \,\frac{g \cdot cm^2}{s^2}= 50\cdot 10^{-16} \cdot 10^{-7} \, J}$

 $\sigma =2,96 \, \AA$
 
 >Wie hoch (in $\mathrm{\frac{kJ}{mol_{H_2}}})$ ist die Bindungsenergie? Führen Sie die Rechnung für eine fcc - Struktur durch. Behandeln sie jedes $H_2$-Molekül als eine Kugel. 


**Lösung Aufgabe 4:**

