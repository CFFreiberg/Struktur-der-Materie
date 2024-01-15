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
> __1.__	Singularität in der Zustandsdichte. 

>__a)__ Ausgehend von der Dispersionsrelation $\omega=\omega_m\left|\sin{\left(\frac{1}{2}Ka\right)}\right|$ für ein einatomiges lineares Gitter aus $N$ Atomen mit Wechselwirkungen nur zwischen nächsten Nachbarn soll gezeigt werden, dass die Zustandsdichtes $D(\omega)=\frac{2N}{\pi}\cdot \frac{1}{(\omega_m^2-\omega^2)^\frac{1}{2}}$ ist, wobei $\omega_m$ die maximale Frequenz ist.

>__b)__ Angenommen, ein optischer Phononenast habe im Dreidimensionalen nahe $K=0$ die Form $\omega(K) = \omega_m – A\cdot K^2$. Zeigen Sie, dass dann für $\omega < \omega_m$ gilt: $D(\omega)=\big(\frac{L}{2\pi}\big)^3\bigg(\frac{2\pi}{A^{\frac{3}{2}}}\bigg)\sqrt{\big(\omega_m-\omega\big)}$. $\omega > \omega_m$ gilt $D(\omega) = 0$. Warum? In diesem Fall ist also die Ableitung der Zustandsdichte unstetig.
   
                                      {{1}}
**Lösung Aufgabe 1:**

{{2}}
Für die Zahl der Zustände (pro Zweig) gilt:
$$N=\int{D(\omega)d\omega=\int{D(K)dK}}\ $$
und damit für die Zustandsdichte: 
$$D(\omega) = D(K)dK/d\omega$$

Für die Zahl $N$ der Zustände im $n$-dimensionalen $K$-Raum gilt:
$$N(K) = \text{Dichte der Zustände} \cdot \text{Volumen des K-Raums}$$

$$\text{Dichte der Zustände}= \left (\frac{L}{2\pi}\right )^n $$

Das Volumen des 1-dim K-Raums ist 2K

**Lösung Aufgabe 1a):**

$$\omega=\omega_m\left|\sin{\left(\frac{1}{2}Ka\right)}\right|$$

wobei für die maximale Frequenz gilt: $\omega_\mathrm{max}=\sqrt{\frac{4C}{M}}$.

$$\Rightarrow K=\frac{2}{a}\arcsin \bigg(\frac{\omega}{\omega_\mathrm{max}})$$

$$\begin{align*}
\Rightarrow \frac{dK}{d\omega}&=\frac{2}{a}\frac{1}{\sqrt{1-\big(\frac{\omega}{\omega_\mathrm{max}}\big)^2}}\frac{1}{\omega_\mathrm{max}}\\
&=\frac{2}{a} \frac{1}{\sqrt{\omega_\mathrm{max}^2-\omega^2}}
\end{align*}$$

Mit der Zustandsdichte für eine Dimension

$$D(\omega)d\omega=\bigg(\frac{L}{2\pi}\bigg)^1\cdot \frac{dK}{d\omega}\cdot d\omega$$

folgt mit $N\cdot a=L$

$$\begin{align*}D(\omega)&=\frac{N\cdot a}{2\pi}\cdot \frac{dK}{d\omega}\\&=\frac{N\cdot a}{2\pi}\cdot\frac{2}{a}\cdot  (\omega_\mathrm{max}^2-\omega^2)^{-\frac{1}{2}}\\
&=\frac{N}{\pi}\frac{1}{\sqrt{\omega_\mathrm{max}^2-\omega^2}}

\end{align*}$$

## Aufgabe 2
                                      {{0}}
> __2.__ Mittlere Wärmeausdehnung einer Kristallzelle (Na). 

>__a)__ Schätzen Sie für eine primitive Elementarzelle eines Natriumkristalls bei $T=300\, \mathrm{K}$ die mittlere Wärmeausdehnung $\frac{\Delta V}{V}$ ab. Nehmen Sie dazu die  Gitterkonstante $a_\mathrm{Na}=4,225\, \AA$ an und den Kompressionsmodul $B$ zu $\mathrm{7 \cdot 10^{10} erg \cdot cm^{-3}= 7 \cdot 10^3 \,J\cdot cm^{-3}=  7 \cdot 10^9 \,J\cdot m^{-3}}$ . Beachten Sie, dass die Debye-Temperatur mit $\mathrm{158\, K}$ geringer als $\mathrm{300\, K}$ ist, so dass die thermische Energie von der Größenordnung von $k_\mathrm{B}\cdot T$ ist (klassische Betrachtung).

>__b)__ Benutzen Sie dieses Ergebnis, um die mittlere thermische Schwankung $\frac{\Delta a}{a}$ der Gitterkonstanten abzuschätzen.



                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}


                                      {{3}}





## Aufgabe 3 
                                      {{0}}
> __3.__ Nullpunkts-Gitterauslenkung und Wärmeausdehnung.   Experimentelle Messungen zeigen, dass mit steigender Temperatur die Gitterkonstante wächst. Wie ist das mittels eines Potential-Modells erklärbar?


                                      {{1}}
**Lösung Aufgabe 3:**

                                      {{2}}


                                      {{3}}


                                      {{4}}


## Aufgabe 4 

                                      {{0}}
> __4.__ Spezifische Wärme einer linearen einatomigen Kette:   Mit Hilfe der Debye-Näherung $D(\omega)= \frac{N}{\omega_\mathrm{D}}$, wobei $\omega_\mathrm{D}=k_\mathrm{B} \cdot \Theta_\mathrm{D}$, berechne man für akustische Phononen die innere Energie und die spezifische Wärme einer einatomigen Kette für die Grenzfälle einer hohen und einer niedrigen Temperatur .

                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}


                                      {{3}}


                                      {{4}}

                                      
{{5}}

