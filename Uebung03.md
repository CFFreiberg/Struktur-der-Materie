<!--
author: Claudia Funke
email: claudia.funke@physik.tu-freiberg.de
title: Übung Struktur der Materie I, Arbeitsblatt 3

@style
.lia-toc__bottom {
    display: none;
}
@end


-->

# Übung 3, Kristallgitter
## Aufgabe 1
>__1.__  Durch welches Bravais-Gitter lässt sich ein flächenzentriert tetragonales Gitter beschreiben. Welcher Zusammenhang besteht zwischen den Gitterkonstanten der beiden Gitter und dem Volumen der Einheitszellen?

![flächenzentriertes tetragonales Gitter](media/flaechenzentriert_tetragonal.png "*Beispiel für flächenzentriertes tetragonales Gitter; Quelle:  Claudia Funke licensed under [CC BY-NC-SA ](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")


**Lösung Aufgabe 1** 

Ein flächenzentriertes tetragonales Gitter lässt sich durch eine 45° Drehung um die z-Achse in ein innenzentriertes tetragonales Gitter mit den Gitterkonstanten $a'= \frac{a}{\sqrt{2}}$ und
$c' = c$ und $V_z' =\frac{1}{2} \cdot V_z$ überführen.


![flächenzentriertes tetragonales Gitter](media/flaechenzentriert-tetragonal2.png "*Beispiel für flächenzentriertes tetragonales Gitter; Quelle:  Claudia Funke licensed under [CC BY-NC-SA ](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")

 
## Aufgabe 2
>__2.__  Welcher Zusammenhang besteht zwischen einer ccp-Kugelpackung (cubic close packed), charakterisiert durch den kleinsten Abstand $a_\mathrm{ccp}$ der Atome und den Abstand $c_\mathrm{ccp}$  (mit dem sich die Stapelung der dichtest gepackten Ebenen wiederholt) auf der einen Seite und einem entsprechenden fcc-Gitter (face centered cubic) mit der Gitterkonstanten $a_\mathrm{fcc}$? 

Hinweis: Der Begriff fcc wird oft als Synonym für die kubisch dicht gepackte Struktur (ccp) in Metallen verwendet. Allerdings steht fcc für ein kubisch-flächenzentriertes Bravais-Gitter, das nicht unbedingt dicht gepackt ist, wenn eine Basis mit mehr als einem Atom auf die Gitterpunkte gesetzt wird. So sind z. B. das Diamant- und das Zinkblende-Gitter fcc, aber nicht dicht gepackt. 

![Ebenen-Stapelfolge  ccp-Gitter](media/ccpKugelpackung.png "*Bildquelle: CdangDerivative work: Muskid - Abwandlung von Empilement_compact.svg, [CC BY-SA 3.0](https://commons.wikimedia.org/w/index.php?curid=33976067)*")



Bestimmen Sie die daraus resultierenden Beziehungen zu $a_\mathrm{ccp}$ und $c_\mathrm{ccp}$ eines ccp-Gitters.

**Lösung Aufgabe 2**

Das ccp-Gitter weist in vertikaler Richtung die Reihenfolge ABCABCABC… dichtest gepackter Ebenen auf.

![kubische Einheitszelle kfz](media/kupfer.png "* Blick auf kubische fcc Zelle n [111]-Richtung; [Bildquelle](http://ruby.chemie.uni-freiburg.de/Vorlesung/Strukturtypen/elemente_kupfer.html)*" )


Die Raumdiagonale der kubischen Einheitszelle entspricht der
"Gitterkonstanten" $c$  des ccp-Gitters: $c = \sqrt{3}\cdot a_\mathrm{fcc}$  und die Gitterkonstante $a$ der Hälfte der Flächendiagonalen:  $a_\mathrm{fcc} = \sqrt{2} \cdot a$. 
Daraus folgt $c = \sqrt{6} \cdot a$.

## Aufgabe 3

>__3.__  Vergleichen Sie die Stapelfolgen der dichtest gepackten Ebenen von ccp-Kugelpackungen und hexagonal dichtest gepackten Kugelpackungen (hcp).
Wie groß ist das Verhältnis  $\frac{c_\mathrm{hex}}{a_\mathrm{ccp}}$ ?


**Lösung Aufgabe 3**

![Vergleich Stapelfolgen ccp und hcp](media/VglStapelfolgen.png "*Vergleich der Stapelfolgen für ccp und hcp Gitter; Quelle:  Bilder erstellt mit [VESTA](https://jp-minerals.org/vesta/en/), Claudia Funke licensed under [CC BY-NC-SA ](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")



Das ccp-Gitter (links in der Abbildung) hat die Stapelfolge ABCABC der dichtest gepackten Ebenen. Das hcp-Gitter (rechts in der Abbildung) hat die Stapelfolge ABABAB der dichtest gepackten Ebenen. 
Die "Wiederhollänge" beträgt bei ccp 3 Ebenenabstände, bei hcp 2 Ebenenabstände. Also ist $c_\mathrm{hcp} =\frac{2}{3}\cdot c_\mathrm{ccp} $
Daraus folgt mit dem Ergebnis von Aufgabe 2: 

$$c_\mathrm{hex} = \frac{2}{3} \cdot  \sqrt{6} \cdot  a_\mathrm{ccp}\eqsim 1,63 \cdot a_\mathrm{ccp} $$

Bemerkung: Sowohl die ccp-Kugelpackung als auch die hcp-Kugelpackung hat eine Raumausfüllung von 74 %

## Aufgabe 4
>__4.__  Geben Sie die Zahl der nächsten Nachbarn (Koordinationszahl) für ein fcc-, bcc- und hcp-Gitter an.

**Lösung Aufgabe 4**

+ fcc: 12 NN
+ bcc: 8 NN
+ hcp: 12 NN

## Aufgabe 5
>__5.__  Silber hat ein fcc-Gitter. Seine Dichte beträgt $\rho_\mathrm{Ag}=10,49\,\mathrm{\frac{g}{cm^3}}$ und die molare Masse $M_\mathrm{Ag}=107,87 \mathrm{\frac{g}{Mol}}$. Bestimmen Sie die Gitterkonstante.



**Lösung Aufgabe 5**

Allgemein gilt: 

$\rho=\frac{m}{V}$. 

Daraus folgt: $V=\frac{m}{\rho}$. 

Mit $N_\mathrm{A}=6,02214076\cdot 10^{23}\mathrm{\frac{1}{mol}} $ (Avogadro-Konstante) folgt also

$$ V_\mathrm{EZ}=a^3=\frac{\mathrm{Anzahl\, Atome\, in\ EZ}\cdot M_\mathrm{Ag}}{N_\mathrm{A}\cdot \rho_\mathrm{Ag} }$$

$$\Rightarrow a^3=\frac{4\cdot 107,87 \mathrm{\frac{g}{Mol}}}{6,02214076\cdot 10^{23}\mathrm{\frac{1}{mol}}\cdot 10,49\,\mathrm{\frac{g}{cm^3}}}=6,83025\cdot 10^{-23} \mathrm{cm^3}
$$

$$\Rightarrow a=4,09 \cdot 10^{-8} \mathrm{cm}= 4,09 \cdot 10^{-10} \mathrm{m}$$

## Aufgabe 6
>__6.__ Geben Sie für Steinsalz die Koordinaten der Natrium- und Chlorionen in Einheiten der Gitterkonstanten $a$ an.

**Lösung Aufgabe 6**

![NACl-Gitter](https://www.tf.uni-kiel.de/matwis/amat/mw1_ge/kap_3/illustr/nacl_gitter.png "*NaCl-Gitter, Quelle: [Uni Kiel](https://www.tf.uni-kiel.de/matwis/amat/mw1_ge/kap_3/backbone/r3_3_3.html)*")



NaCl: fcc-Gitter mit Basis:

Cl auf (0,0,0) und 
Na auf $(\frac{1}{2}, \frac{1}{2},\frac{1}{2})$ 

Damit sitzen die Atome auf:

Cl: (0,0,0);  $(\frac{1}{2}, \frac{1}{2},0);  (\frac{1}{2}, 0,\frac{1}{2}),  (0, \frac{1}{2},\frac{1}{2})$

Na:  $(\frac{1}{2}, \frac{1}{2},\frac{1}{2})$;  $(0, 0,\frac{1}{2})$;  $(0, \frac{1}{2},0)$; $(\frac{1}{2}, 0,0)$

## Aufgabe 7
>__7.__ Geben Sie den kürzesten Abstand zwischen zwei Ionen im Kristallgitter mit Zinkblendestruktur bezogen auf die Gitterkonstante an.

**Lösung Aufgabe 7**

![Zinkblende-Struktur](https://upload.wikimedia.org/wikipedia/commons/1/12/Sphalerite_polyhedra.png "*Zinkblende-Struktur, Quelle: [Wikipedia](https://de.wikipedia.org/wiki/Zinkblende-Struktur)*")


Die Zinkblende-Struktur wird auch Spahlerit genannt und ist $\alpha$-ZnS. Vergleichen Sie die Struktur mit dem Diamantgitter. Erkennen Sie Ähnlichkeiten?
Der kürzeste Abstand zweier (unterschiedlicher) Atome ist 1/4 der Raumdiagonalen:

$$r_0=\frac{\sqrt{3}}{4}$$

## Aufgabe 8

>__8.__ Zeichnen Sie das flächenzentrierte kubische Gitter. Markieren Sie die Lage von oktaedrisch bzw. tetraedrisch koordinierten Zwischengitterplätzen und zählen Sie die Anzahl der Gitteratome und Zwischengitterplätze ab.

**Lösung Aufgabe 8**

Das fcc Gitter hat 4 Gitteratome pro kubischer Einheitszelle: Jede der acht Ecken eines Würfels werden von insgesamt 8 aneinanderstoßenden Wüfel geteilt. Dann gibt es noch 6 Flächenmitten, die jeweils von zwei Würfeln geteilt werden also insgesamt: 
$$N_\mathrm{Atome/EZ}=8\cdot\frac{1}{8}+6 \cdot\frac{1}{2}=4$$ 


**Oktaederlücke** im fcc:


![Oktaederlücke im fcc-Gitter](https://upload.wikimedia.org/wikipedia/commons/c/c7/Oktaederl%C3%BCcke.png "*Oktaederlücke im fcc-Gitter, Quelle: [Wikipedia](https://de.wikipedia.org/wiki/Oktaederl%C3%BCcke)*")


Es gibt 1 oktaedrische Lücke in der Mitte des Würfels und je eine an den zwölf Kanten, die aber nur zu einem Viertel zählen, da jede Kante von vier Würfeln geteilt wird: 
$$N_{\mathrm{Oktaederlücke}}=1+12\cdot \frac{1}{4}=4$$

**Tetraederlücke** im fcc:
![Tetraederlücke im fcc-Gitter](https://upload.wikimedia.org/wikipedia/commons/f/fc/FCC_Tetrahedral_Void.jpg "*Tetraederlücke im fcc-Gitter, Quelle: [Wikipedia](https://de.wikipedia.org/wiki/Tetraederl%C3%BCcke)* ")



Es gibt je 1 tetraedrische Lücke in der Mitte eines Würfel-Achtels (Würfeloktand). Da es 8 Würfelachtel gibt, gibt es acht Tetraederlücken.
$$N_{\mathrm{Tetraederlücke}}=1\cdot 8=8$$