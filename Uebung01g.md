<!--
author: Claudia Funke
email: claudia.funke@physik.tu-freiberg.de
title: Lösung Übung 1 
version: 2.0
language: de
narrator: Deutsch Female
comment:  Struktur der Materie Übung 1
@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md
-->

# Übung 1

## Aufgabe 1
> __1.__ Bitte absolvieren sie den im Opal-Kurs bei der Übung 1 hinterlegten [Test zur Vektorrechnung](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/1013219356/CourseNode/1692325844519000012).

## Aufgabe 2

{{0}}
> __2.__ Um eine ungefähre Vorstellung von der Verteilung der Gitterbausteine zu bekommen, kann man sich die Atome auf den Gitterplätzen als starre Kugeln vorstellen, die „auf Stoß“ aneinander liegen. Daraus lässt sich der Anteil des Volumens einer Gitterzelle berechnen, der von den Atomen eingenommen wird. (Aufgabe aus A. Armbrust, H. Janetzki, „Aufgaben zur Festkörperphysik“)

> __a)__ Wie groß ist in diesem „starren Kugelmodell“ der Volumenanteil der Kugeln in einem einfachen kubischen Gitter? 

![Einfach kubisches Gitter](media/sc.png "*Einfach kubisches Gitter; Quelle: A. Ambrust, H. Janetzki, Aufgaben zur Festkörperphysik*") 

{{1}}
**Lösung Aufgabe 2a**

**Volumen der Einheitszelle:** $V_Z=a^3$

{{2}}
**Volumen der Kugel** (mit $r=\frac{a}{2}$):  $V_K=\frac{4 \pi}{3} \left( \frac{a}{2}\right)^3$

{{3}}
**Anzahl der Kugeln:** $N_K=8\cdot \frac{1}{8}$

{{4}}
$$\frac{N_K \cdot V_K}{V_Z}=\frac{1  \cdot \frac{4 \pi}{3} \left( \frac{a}{2}\right)^3}{a^3}=\frac{\pi}{6}=0,52=52 \%$$



{{5}} 
> __b)__ Wie groß ist in diesem „starren Kugelmodell“ der Volumenanteil der Kugeln in einem kubisch raumzentrierten Gitter? 

![Einfach kubisches Gitter](media/bcc.png "*Kubisch raumzentriertes Gitter; Quelle: A. Ambrust, H. Janetzki, Aufgaben zur Festkörperphysik*") 

{{6}}
**Lösung Aufgabe 2b**

{{6}}
**Volumen der Einheitszelle:** $V_Z=a^3$

{{7}}
**Volumen der Kugel** (mit $r=\frac{a\cdot \sqrt{3}}{4}$):  $V_K=\frac{4 \pi}{3} \left( \frac{a\cdot \sqrt{3}}{4}\right)^3=\frac{\pi a^3 \sqrt{3}}{4^2}$

{{8}}
**Anzahl der Kugeln:** $N_K=8\cdot \frac{1}{8}+1=2$

$$\frac{N_K \cdot V_K}{V_Z}=\frac{2}{a^3}\cdot \frac{\pi a^3 \sqrt{3}}{4^2}=\frac{\pi\sqrt{3}}{8}=0,68=68 \%$$

{{9}}
> __c)__ Wie groß ist in diesem „starren Kugelmodell“ der Volumenanteil der Kugeln in einem kubisch flächenzentrierten Gitter? 

![Einfach kubisches Gitter](media/fcc.png "*Kubisch flächenzentriertes Gitter; Quelle: A. Ambrust, H. Janetzki, Aufgaben zur Festkörperphysik*") 

{{10}}
**Lösung Aufgabe 2c**

{{11}}
**Volumen der Einheitszelle:** $V_Z=a^3$

{{12}}
**Volumen der Kugel** (mit $r=\frac{a\cdot \sqrt{2}}{4}$):  $V_K=\frac{4 \pi}{3} \left( \frac{a\cdot \sqrt{2}}{4}\right)^3=\frac{\pi a^3 \cdot 2 \cdot \sqrt{2}}{3 \cdot 4^2}$


{{13}}
**Anzahl der Kugeln:** $N_K=8\cdot \frac{1}{8}+6\cdot \frac{1}{2}=4$

$$\frac{N_K \cdot V_K}{V_Z}=\frac{4}{a^3}\cdot \frac{\pi a^3 2\sqrt{2}}{3 \cdot 4^2}=\frac{\pi}{3\cdot\sqrt{2}}=0,74=74 \%$$

{{14}}
> __d)__ Wie groß ist in diesem „starren Kugelmodell“ der Volumenanteil der Kugeln in einem hexagonalem dichtest gepacktem Gitter? 

![Hexagonales Gitter](media/hex.png "*Hexagonales Gitter; Quelle: A. Ambrust, H. Janetzki, Aufgaben zur Festkörperphysik*") 


{{15}}
**Lösung Aufgabe 2d**

{{16}}
Für Berechnung des Volumens der Einheitszelle wird erst die Grundfläche $A$ berechnet und dann mit der Höhe  $c$ der Einheitszelle multipliziert. Für die Berechnung der Grundfläche ist folgende Abbildung hilfreich, denn dort wird deutlich, dass die Grundfläche ein Parallelogramm ist.


{{17}}
**Grundfläche:** $A=a\cdot h=a\cdot \sqrt{a^2-\left( \frac{a}{2} \right)^2}=a^2 \cdot\sqrt{1-\frac{1}{4}}=\frac{a^2 \cdot \sqrt{3}}{2}$

![hexagonales Gitter in der Ebene](media/hexagonal2d.png "*Hexagonales Gitter; Quelle: C. Funke*") 

{{18}}
Der **Zusammenhang zwischen den auf Stoß zusammensitzenden Kugeln mit dem Kugelradius $r$ und den Gitterparametern $a$ und $c$ ** des hexagonal dichtest gepackten Gitters ist etwas komplexer. Zur Herleitung wird folgende Skizze betrachtet:

![hexagonales Gitter in der Ebene](media/hexagonalLoesung.png "*Geometrische  Zusammenhänge im Hexagonalen Gitter; Quelle: links A. Ambrust, H. Janetzki, Aufgaben zur Festkörperphysik; rechts C. Funke*") 

{{19}}
Wenn die Kugeln dichtest gepackt sind und auf Stoß sitzen, dann gilt:
$$l=a=2\cdot r$$

{{20}}
Aus dem linken Teilbild der Abbildung gilt für das senkrecht stehende rechtwinklige Dreieck

$$\left( \frac{c}{2} \right)^2=l^2-x^2$$

$x$ kann durch die Gitterkonsante $a$ ausgedrückt werden, siehe rechte Teilabbildung der obigen Abbildung:

$$x^2+\left( \frac{1}{3}a \right)^2=  \left( \frac{2}{3}a \right)^2$$
$$\Rightarrow x^2= \frac{4}{9}a^2- \frac{1}{9}a^2=\frac{1}{3}a^2$$

Dieser Ausdruck für $x^2$ wird nun zusammen mit $l=a$ in die obige Gleichung mit $\frac{c}{2}$ eingesetzt:
$$\left( \frac{c}{2} \right)^2=l^2-\frac{1}{3}a^2=\frac{2}{3}a^2$$
Damit folgt für $c$
$$c=\sqrt{\frac{4 \cdot 2}{3}a^2}=\sqrt{\frac{8}{3}}a$$
Damit gilt für das Volumen der Einheitszelle

**Volumen der Einheitszelle:** $V_Z=A\cdot c=\frac{a^2 \cdot \sqrt{3}}{2} \cdot \sqrt{\frac{8}{3}}a=\sqrt{2}a^3$

**Volumen der Kugel** (mit $r=\frac{a}{2}$):  $V_K=\frac{4 \pi}{3} \left( \frac{a}{2}\right)^3=\frac{\pi a^3 }{6}$

**Anzahl der Kugeln:** $N_K=8\cdot \frac{1}{8}+1=2$

$$\frac{N_K \cdot V_K}{V_Z}=\frac{2\cdot \frac{\pi a^3 }{6}}{\sqrt{2}a^3}=\frac{\pi}{3 \cdot \sqrt{2}}=0,74=74 \%$$

## Aufgabe 3

> __3.__ Das Diamantgitter besteht aus zwei kubisch flächenzentrierten Gittern, wobei das Zweite um ein Viertel der Raumdiagonalen gegenüber dem Ersten verschoben ist. Die Winkel zwischen den tetraedrischen Bindungen der Diamantstruktur sind dieselben wie die Winkel zwischen den Raumdiagonalen eines Würfels, z. B. zwischen [1,1,1] und [1,-1,-1]. 

![Diamantgitter](media/diamant.png "*Diamantgitter; Abbildung erstellt mit VESTA, Quelle: C. Funke*") ![Diamantgitter aus 2 Untergittern](media/SiC.png "*SiC-Gitter; Abbildung erstellt mit VESTA, Quelle: C. Funke*")
*Hinweis: Im SiC-Gitter sind die 2 kubisch-flächenzentrierten Untergitter durch die beiden Atomsorten C und Si besetzt. Dadurch sind die jeweiligen Untergitter besser zu erkennen*

> __a)__ Bestimmen Sie mit Hilfe der elementaren Vektoranalysis die Größe dieses Winkels!

> __b)__ Bestimmen Sie den Volumenanteil im Harte-Kugel-Modell für die Diamant-Kristallstruktur!




**Lösung Aufgabe 3a**
$$\mathrm{cos}({\varphi})=
\begin{pmatrix}1\\ 1\\ 1\\\end{pmatrix} \cdot 
\begin{pmatrix}1\\ -1\\ -1\\\end{pmatrix}=\frac{1-1-1}{\sqrt{3}\cdot \sqrt{3}}=-\frac{1}{3}$$

$\Rightarrow \varphi=\mathrm{arccos(\frac{1}{3})}=109,47°  $

**Lösung Aufgabe 3b**

Volumen der Einheitszelle: $V_\mathrm{EZ}=a^3$

Nun benötigen Sie einen Zusammenhang zischen Kugelvolumen und Gitterkonstante $a$. Die dichtest benachbarten Kugel sollen Stoß auf Stoß sitzen. 
Betrachten Sie folgende Abbildung und wenden Sie den Satz von Pythagoras zweimal an:

![Detail Diamantgitters](media/diamanatdetail.png "*Ausschnitt aus Diamantgitter (ein Achtel der Einheitszelle) zum Erkennen der geometrischen Zusammenhänge zwischen $l$, $x$ und $\frac{a}{4}$; Quelle: A. Ambrust, H. Janetzki, Aufgaben zur Festkörperphysik*")


Dann folgt:
$$l^2=\left(\frac{a}{4}\right)^2+x^2$$
und
$$x^2=\left(\frac{a}{4}\right)^2+\left(\frac{a}{4}\right)^2 \Rightarrow x=\frac{a}{\sqrt{8}}$$

Die zweite Gleichung in die erste Gleichung eingesetzt ergibt


$$l^2=\left(\frac{a}{4}\right)^2+\frac{a^2}{8} \Rightarrow l=\frac{\sqrt{3}\cdot a}{4}$$

Diese Distanz $l$ gibt aber genau den Abstand zweier sich auf Stoß berührender Kugel-(Mittelpunkte) an. Das bedeutert $l= 2 \cdot r$ (mit $r=$ Kugelradius).

Also gilt für das Kugelvolumen der auf Stoß sitzenden Kugeln im Diamantgitter:
$$V_\mathrm{K}=\frac{4\pi}{3}\left(\frac{l}{2}\right)^3= \frac{4\pi}{3}\cdot \frac{3\cdot \sqrt{3} \cdot a^3}{4^3 \cdot 2^3 }=\frac{\pi \cdot \sqrt{3}\cdot a^3}{128}$$

Die Anzahl der Atome pro kubischer Einheitszelle des Diamantgitters ist doppelt so groß wie die im kfz-Gitter, da zu jedem Atom des kfz-Gitters noch ein weiteres um $(\frac{1}{4}, \frac{1}{4}, \frac{1}{4})$ verschobenes dazukommt. Also: $$N=(1+\frac{1}{2}\cdot 6)\cdot 2=8$$.

Damit ergibt sich:
$$\frac{N\cdot V_\mathrm{K}}{V_\mathrm{EZ}}=\frac{8 \cdot \frac{\pi \cdot \sqrt{3}\cdot a^3}{128}}{a^3}=\frac{8\cdot \pi \cdot \sqrt{3}}{128}=\frac{\pi \cdot \sqrt{3}}{16}=0,34$$

Die Volumenausfüllung eines so dicht wie möglich gepackten Diamantgitters ist also nur 34 %.



-----


## Schoenflies-Symbolik:
- Auch als "kurze Kristallklassenbezeichnung" bekannt, ist die Schoenflies-Symbolik eine ältere Methode zur Darstellung von Raumgruppen.
- Sie basiert auf der Punktgruppen-Symmetrie, der höchsten Symmetrie eines Kristalls, und verwendet Buchstaben und Zahlen, um die verschiedenen Punktgruppen darzustellen.
- Diese Bezeichnung ist intuitiv und leicht zu verstehen, insbesondere für Punktgruppen, aber weniger spezifisch für Raumgruppen, da sie nicht die Translationsinformationen enthält.

[Details zu Symmetrieelementen in Schoenfließ-Symbolik](https://de.wikipedia.org/wiki/Schoenflies-Symbolik)

## Hermann-Mauguin-Notation:
- Auch als "erweiterte Hermann-Mauguin-Notation" bekannt, ist diese Methode moderner und detaillierter.
- Sie kombiniert die Information der Punktgruppe mit den Translationsinformationen und ermöglicht eine vollständige Beschreibung der Raumgruppe.
- Die Hermann-Mauguin-Notation verwendet Buchstaben, Zahlen und Symbole, um die Punktgruppen- und Translationsinformationen zu repräsentieren.

[Details zu Symmetrieelementen in Hermann-Mauguin-Symbolik](https://de.wikipedia.org/wiki/Hermann-Mauguin-Symbolik)


## Unterschied:
Der Hauptunterschied zwischen den beiden Notationen liegt in ihrer Detailtiefe und Spezifität:
- Die Schoenflies-Symbolik konzentriert sich hauptsächlich auf die Punktgruppensymmetrie und bietet eine intuitive Darstellung, ist jedoch weniger detailliert in Bezug auf die Translationsinformationen.
- Die Hermann-Mauguin-Notation hingegen bietet eine vollständige Beschreibung der Raumgruppe, einschließlich sowohl der Punktgruppen- als auch der Translationsinformationen. Sie ist spezifischer und detaillierter, aber erfordert möglicherweise mehr Kenntnisse zur Interpretation.

In der Praxis wird die Hermann-Mauguin-Notation häufiger verwendet, da sie die vollständigere und präzisere Methode zur Beschreibung von Raumgruppen ist.

## Quiz
Welche Aussagen sind richtig?

[[X]] Die Schoenflies-Symbolik konzentriert sich hauptsächlich auf die Punktgruppensymmetrie.
[[X]] Die Hermann-Mauguin-Notation bietet eine vollständige Beschreibung der Raumgruppe, einschließlich sowohl der Punktgruppen- als auch der Translationsinformationen.
[[ ]] Die Schoenflließ-Symbolik und die Herrman-Maugin-Symbolik beschreiben genau die gleichen Inhalte.
[[X]] Die Hermann-Mauguin-Notation ist die vollständigere und präzisere Methode zur Beschreibung von Raumgruppen.
[[?]] You can choose more than one correct answer!
***
<div class = "answer">



</div>
***

