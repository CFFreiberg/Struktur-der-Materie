<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 8
@style
.lia-toc__bottom {
    display: none;
}
@end

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

import: https://github.com/liascript/CodeRunner

@binder:
  url: https://mybinder.org
  repo: YOUR_GITHUB_USER/YOUR_REPO
  ref: main



-->


# Übung 8: 


## Aufgabe 1

                                      {{0}}
> __1.__  Eine für die Auswertung der Röntgenreflexe kubischer Substanzen benötigte Größe ist die Quadratsumme  $ h^2+ k^2 +l^2$. Stellen Sie eine Tabelle zusammen, in der Sie für $1\le h^2+ k^2 +l^2 \le 15$ die zugehörigen $hkl$- Werte für die drei verschiedenen kubischen Gitter (sc, bcc, fcc) eintragen. Für welche Werte von $ h^2+ k^2 +l^2$ sind jeweils Reflexe zu erwarten. Wieso kann man aus der Auftragung eines Beugungsspektrums über $\sin ^2\theta$ erkennen, welches der drei Gitter vorliegt?

                                      {{1}}
**Lösung Aufgabe 1:**

                                      {{2}}
***kubisch primitiv (sc):***

                                      {{2}}
$S_{hkl}= f_j$ mit $f_j=$ Atomformfaktor

                                      {{3}}
***kubisch raumzentriert (bcc):***

                                      {{3}}
 $S_{hkl}=2f_j$ für $h+k+l$  gerade; $S_{hkl}=0$ für $h+k+l$ ungerade

                                      {{4}}
***kubisch flächenzentriert (fcc):***

                                      {{4}}
$S_{hkl}=4\cdot f_j$ für alle $ h,k,l$ gerade oder alle $h,k,l$ ungerade. Sonst Null

                                      {{5}}
<!-- data-type="none" -->
|$ h^2+ k^2 +l^2$| sc $(hkl)$| bcc $(hkl)$ |fcc $(hkl)$|
|:---|:---|:---|:---|
|1|(1,0,0)|-|-|
|2|(1,1,0)|(1,1,0)|-|
|3|(1,1,1)|-|(1,1,1)|
|4|(2,0,0)|(2,0,0)|(2,0,0)|
|5|(2,1,0)|-|-|
|6|(2,1,1)|(2,1,1)|-|
|7|-|-|-|
|8|(2,2,0)|(2,2,0)|(2,2,0)|
|9|(3,0,0); (2,2,1)|-|-|
|10|(3,1,0)|(3,1,0)|-|
|11|(3,1,1)|-|(3,1,1,)|
|12|(2,2,2)|(2,2,2)|(2,2,2)|
|13|(3,2,0)|-|-|
|14|(3,2,1)|(3,2,1)|-|
|15|-|-|-|

                                      {{6}}
Für kubische Gitter gilt:
$$d_{hkl}=\frac{a}{\sqrt{h^2+k^2+l^2}}$$

                                      {{7}}
Eingesetzt in die  Bragg-Bedingung für Beugung (in die erste Ordnung) $\lambda=2\cdot d_{hkl}\cdot \sin(\theta)$ ergibt sich 
$$ \sin^2(\theta)=\left (\frac{\lambda}{2a} \right )^2(h^2+k^2+l^2)$$

                                      {{8}}
Eine Auftragung des Beugungsspektrums über $\sin ^2\theta$ und ein Vergleich mit den vorhandenen Reflexen bei den $h^2+k^2+l^2$-Werten ermöglicht eine Unterscheidung von sc-, bcc- und fcc-Gittern.

                                      {{8}}
![Intensität in Abhängigkeit vom Beugungswinkel](media/intensities.png "*Intensitätsverteilung in Abhängigkeit des Beugungswinkels;  Quelle:  [Rueddiger Mitdank](https://www.researchgate.net/profile/Ruediger-Mitdank/post/What-is-the-significance-of-h2-k2-l2/attachment/5d1b42d83843b0b982591bbc/AS%3A776182228332547%401562067672794/download/intensities.png?_tp=eyJjb250ZXh0Ijp7ImZpcnN0UGFnZSI6InF1ZXN0aW9uIiwicGFnZSI6InF1ZXN0aW9uIn19)*")




## Aufgabe 2 (Zusammenhang der Breite des Beugungsmaximums mit der Größe des Kristalls)


> __2.__  Betrachten Sie einen linearen (eindimensionalen)  Kristall mit den  Gitterpunkten $r=m\cdot a$ mit  $m \in \mathbb{Z}$ und $a=$ Gitterkonstante. Auf jedem der Gitterpunkte sitzt ein identisches, punktförmiges Streuzentrum. Die Atome werden von einer kohärenten Welle angeregt. In Analogie zur Streuamplitude in einem realen Kristall $F=\sum_G \int n_G \cdot \exp(-i\vec{G}\cdot\vec{r})\cdot dV$  ist die Gesamtstreuamplitude der Streustrahlung proportional zu  $F=f\cdot \sum_{m=0}^M  \exp(-i\Delta k \cdot m \cdot a )$.  Die Summe über $M$ Gitterpunkte hat unter Verwendung der Reihenentwicklung 
> $$ \sum_{m=0}^{M-1}x^m=\frac{1-x^M}{1-x}$$
> den Wert 
> $$F=\frac{1-\exp(-iM(a\cdot \Delta k))}{1-\exp(-i(a\cdot \Delta k))}$$
> Die gestreute Intensität ist proportional zu $|F|^2$. 

> __a)__ Zeigen Sie, dass gilt:
$$|F|^2 \equiv F\cdot \overline{F}=\frac{\sin^2\left( \frac{1}{2}M(a\cdot\Delta k)\right )}{\sin^2\left( \frac{1}{2}(a\cdot\Delta k)\right )}$$

                                      {{0}}
**Lösung Aufgabe 2a:**

                                      {{1}}
$|F|^2 \equiv F\cdot \bar{F}$ muss berechnet werden. Dazu benötigen wir das konjugiert Komplexe von $F$. Mit $ \overline{\left(\frac{z_1}{z_2}\right)} = \frac{\overline z_1}{\overline z_2}$ für $ z_2 \ne 0 $ folgt:
$$\overline{F}=\frac{1-\exp(+iM(a\cdot \Delta k))}{1-\exp(+i(a\cdot \Delta k))}$$

                                      {{2}}
Und damit :
$$|F|^2 \equiv F\cdot \bar{F}=\frac{1-\exp(-iM(a\cdot \Delta k))}{1-\exp(-i(a\cdot \Delta k))}\cdot \frac{1-\exp(+iM(a\cdot \Delta k))}{1-\exp(+i(a\cdot \Delta k))}$$

                                      {{3}}
$$\Rightarrow |F|^2=\frac{1-\exp(+iM(a\cdot \Delta k))-\exp(-iM(a\cdot \Delta k))+1}{1-\exp(+i(a\cdot \Delta k))-\exp(-i(a\cdot \Delta k))+1}$$ 

                                      {{4}}
Da $e^{ix}=\cos(x)+i\sin(x)$ folgt mit $e^{ix}+e^{-ix}=2\cos(x)$
$$\Rightarrow |F|^2=\frac{2-2\cos(Ma\Delta k)}{2-2\cos(a \Delta k)}=\frac{1-\cos(Ma\Delta k)}{1-\cos(a \Delta k)}$$

                                      {{5}}
Mit $\cos(2x)=1-2\sin^2(x)$ folgt:
$$\Rightarrow |F|^2=\frac{1-(1-2\sin^2(\frac{1}{2}Ma\Delta k))}{1-(1-2\sin^2(\frac{1}{2}a \Delta k))}=\frac{\sin^2(\frac{1}{²}Ma\Delta k)}{\sin^2(\frac{1}{2}a \Delta k)}$$

                                      {{6}}
![Beugungsmaxima](media/BreiteBeugungsmaximum.png "*Intensitätsverteilung $|F|^2$ bei der Beugung an einem eindimensionalen Gitter mit $M=5$ und $M=10$ Atomen. Auf der $x$-Achse ist $\frac{\Delta ka}{2\pi}$ aufgetragen;  Quelle:  Claudia Funke, erstellt in GeoGebra, licensed under [CC BY-NC-SA ](https://creativecommons.org/licenses/by-nc-sa/4.0/)*")


                                      {{6}}
$|F|^2$ hat damit Hauptmaxima bei $a\cdot \Delta k=2\pi h$, ($h \in \mathbb{Z}$)


                                      {{7}}
In der folgenden, inhaltlich gleichen Abbildung können Sie den Python-Quellcode ausführen, indem sie links unten auf den runden Knopf mit dem </> Zeichen drücken. Dann wird eine Abbildung mit der Intensitätsverteilung $|F|^2$ bei der Beugung an einem eindimensionalen Gitter erzeugt. Die Anzahl der an der Beugung beteiligten Atome kann über die Bewegung des *sliders* variiert werden.

{{7}}
 @input(range, min=1, max=30, step=1, value=4) @m
 
``` python @plot_script
# Quelle: https://matplotlib.org/stable/gallery/widgets/slider_snap_demo.html

import sys
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.widgets import Button, Slider
from matplotlib.widgets import Slider

# The parametrized function to be plotted
def f(variable, m):
    return np.sin(np.pi*variable*m)**2//np.sin(np.pi*variable)**2


def main():
    x_min = -1.1
    x_max = 1.1
    x_num = 1000
    y_min = 0
    y_max = 100
    x_label = "$\\frac{\\Delta k \\cdot a }{2\\pi}$"
    #x_label = "xlabel"
    #y_label = "ylabel"
    y_label = "$\\|F|^2$"
    
    # Define slider parameters
    init_m = 4
    m_min = 1
    m_max = 30
    m_step = 1
    slider_label = "Anzahl der Atome"

    x = np.linspace(x_min, x_max, x_num)
    # Create the figure and the line that we will manipulate
    fig, ax = plt.subplots()
    line, = ax.plot(x, f(x, init_m), lw=3)
    ax.set_xlabel(x_label)
    ax.set_ylabel(y_label)
    ax.set_ylim(y_min, y_max)
    # adjust the main plot to make room for the sliders
    fig.subplots_adjust(left=0.25, bottom=0.25)
    # Make a horizontal slider to control the frequency.
    axfreq = fig.add_axes([0.25, 0.1, 0.65, 0.03])
    m_slider = Slider(
        ax=axfreq,
        label=slider_label,
        valmin=m_min,
        valmax=m_max,
        valstep=m_step,
        valinit=init_m,
    )
    def update(val):
        line.set_ydata(f(x, m_slider.val))
        fig.canvas.draw_idle()
    def reset(event):
        m_slider.reset()
    # register the update function with each slider
    m_slider.on_changed(update)

    resetax = fig.add_axes([0.8, 0.025, 0.1, 0.04])
    button = Button(resetax, 'Reset', hovercolor='0.975')
    button.on_clicked(reset)   

    plt.show()
main()
```
@Pyodide.eval(`["main.py"]`, `python3 -m compileall .`, `python3 main.py`)





                                      {{8}}
> __b.__ Für $a\Delta k=2\pi h$ mit $h \in \mathbb{Z} $ erscheint ein Beugungsmaximum. Ändern wir $\Delta k$ geringfügig und definieren uns ein $\epsilon$ in $a \Delta k=2\pi h+\epsilon$ so, dass $\epsilon$ den Ort des ersten Nulldurchgangs der Funktion $\sin(\frac{1}{²}Ma\Delta k)$ angibt. Zeigen Sie, dass gilt $\epsilon=\frac{2\pi}{M}$, so dass die Breite des Beugungsmaximums proportional zu $\frac{1}{M} $ ist und dadurch für große Werte von $M$ extrem schmal werden kann. 

                                      {{9}}
**Lösung Aufgabe 2b:**

                                      {{10}}
$|F|^2$ hat  Hauptmaxima bei $a\cdot \Delta k=2\pi h$, ($h \in \mathbb{Z}$)
Für die Umgebung der Maxima $a\Delta k=2\pi h + \epsilon $ folgt mit der Lösung von a):

                                      {{11}}
$$|F|^2=\frac{\sin^2(\frac{1}{2}Ma\Delta k)}{\sin^2(\frac{1}{2}a \Delta k)}=\frac{\sin^2(\frac{1}{2}M(2\pi h+\epsilon))}{\sin^2(\frac{1}{2}(2 \pi  h + \epsilon))}$$

                                      {{12}}
Betrachten wir den Term im Zähler genauer. Mit den Additionstheoremen für den Sinus einer Summe $\sin(x_1​+x_2​)=\sin(x_1)\cdot  \mathrm{​cos}(x_2)​+\sin(x_2)\cdot \mathrm{​cos}(x_1)$ folgt​
$$\sin(\frac{1}{2}M(2\pi h+\epsilon))=\sin(M \pi h+\frac{M\epsilon}{2})=\sin(M \pi h)\cdot \cos(\frac{M\epsilon}{2})+\sin(\frac{M\epsilon}{2})\cdot \cos(M\pi h)$$

                                      {{12}}
Es gilt $\sin(M \pi h)=0$ und $\cos(M\pi h)=\pm 1$ , deshalb folgt:

                                      {{12}}
$$\sin(\frac{1}{2}M(2\pi h+\epsilon))=\pm \sin(\frac{M\epsilon}{2}) $$

                                      {{13}}
Die erste Nullstelle von $\sin(\frac{M\epsilon}{2})$ ist bei $ \epsilon=\frac{2\pi}{M}$. Die "Breite des Maximums" $\epsilon$ wird also kleiner, wenn $M$ größer wird. 

## Aufgabe 3 (Formfaktor H-Atom)


> __3.__  Für das Wasserstoffatom ist im Grundzustand die Elektronendichte gleich
> $$n(r)=\frac{1}{\pi a_0^3}\exp\left ( \frac{-2r}{a_0}\right)$$
>  Dabei ist $a_0$ der Bohrsche Radius. Zeigen Sie, dass der Atomformfaktor gleich 
> $$f_{\Delta k}=\frac{16}{\bigg(4+\Delta k^2\cdot a_0^2\bigg)^2}$$
>  ist, wobei $\Delta k=k-k'$ der Streuvektor ist.

                                      {{0}}
**Lösung Aufgabe 3:**

                                      {{1}}
Für das radialsymmetrische H-Atomist es sinnvoll, Kugelkordinaten $(r, \varphi, \theta)$ zu nutzen:

                                      {{1}}
![Definition Kugelkoordinaten](https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Kugelkoord-def.svg/450px-Kugelkoord-def.svg.png "*Kugelkoordinaten $(r ,\varphi ,\theta ,)$ eines Punktes P und kartesisches Koordinatensystem mit den Achsen x , y , z. Quelle: wikipedia, Author Ag2gaeh, [CC BY-SA 4.0 Deed](https://creativecommons.org/licenses/by-sa/4.0/)*")

                                      {{2}}
$$x = r \cdot \cos \varphi \sin \theta$$
$$y =r \cdot \sin \varphi \sin \theta$$
$$z = r \cdot  \cos \theta$$

                                      {{3}}
$\varphi$ ist der Azimutwinkel, $\theta$ der Höhenwinkel vom Pol aus gemessen und $r$ der Abstand zum Ursprung. Es gilt für das Volumenelemt $dV$:

                                      {{4}}
![Volumenelement in Kugekoordinaten](media/VolumenelemntKugelkoordinaten.png "*[Volumenelement in Kugelkoordinaten, Quelle HTW Berlin](https://mediathek.htw-berlin.de/getMedium/50f14be8a5d003c8a5d2daa9f5f6fc79.pdf)*")



                                      {{5}}
$$dV= dx \cdot dy \cdot dz= (r d\theta)\cdot(dr)\cdot(r \sin \theta d \varphi)=r^2\sin \theta \cdot dr \cdot  d\varphi \cdot d\theta=-r^2 dr \cdot  d\varphi \cdot d(\cos \theta)$$

                                      {{6}}
Damit folgt für eine allgemeine Funktion $f(x,y,z)$
$$\Rightarrow \int dV f(x,y,z)=\int_V f(x,y,z) dx \cdot dy \cdot dz =\int_{r=0}^{\infty}\int_{\varphi=0}^{2\pi}\int_{\theta=0}^{\pi}{f(r,\varphi, \theta)\cdot r^2\sin{\theta\ d\theta\ d\varphi\ dr}}$$
Für den Atomformfaktor vom H-Atom gilt damit:

                                      {{7}}
$$f_H=\int_V dV \cdot n_H(r) \exp (-i \Delta \vec{ k} \cdot \vec{r}) = \int_{0}^{\infty}\int_{0}^{2\pi}\int_{0}^{\pi}  r^2\sin{\theta\ d\theta\ d\varphi\ dr} \cdot {n_H(r) \exp (-i \Delta \vec{ k} \cdot \vec{r})}$$


                                      {{8}}
$$\Rightarrow f_H= \int_{0}^{\infty}\int_{0}^{2\pi}\int_{\cos \theta = 1}^{\cos \theta =-1}  -r^2 (d (\cos\theta)) \ d\varphi\ dr \cdot {n_H(r) \exp (-i \Delta \vec{ k} \cdot \vec{r})}$$

                                      {{9}}
$$\Rightarrow f_H= 2\pi \int_{0}^{\infty}\int_{\cos \theta = 1}^{\cos \theta =-1}  -r^2 (d (\cos\theta)) \  dr \cdot {n_H(r) \exp (-i \Delta k r \cos \theta)}$$

                                      {{10}}
wobei $\theta$ der Winkel zwischen $\vec{r}$ und $\Delta \vec{k} $ ist. Das Integral nach $d \cos \theta$ kann einfach durchgeführt werden. Beim Vertauschen der Integrationsgrenzen fällt auch das vordere  $-$ weg.

                                      {{11}}
$$\Rightarrow f_H= 2\pi \int_{0}^{\infty} \left [n_H(r) \cdot   r^2 \cdot \frac{{ \exp (-i \Delta k r \cos \theta)}}{-i \Delta kr} \right]_{-1}^{1} dr $$


                                      {{12}}
$$\Rightarrow f_H= 2\pi \int_{0}^{\infty} \left (n_H(r) \cdot   r^2 \cdot \frac{{ \exp (-i \Delta k r 1)-\exp (-i \Delta k r (-1))}}{-i \Delta k r} \right) dr $$
 folgt:


                                      {{13}}
$$\Rightarrow f_H= 2\pi \int_{0}^{\infty} \left (\frac{n_H(r)}{\Delta kr} \cdot   r^2 \cdot 2 \sin ( \Delta k r ) \right) dr $$


                                      {{14}}
An dieser Stelle kann nun die Elektronendichteverteilung für H-Atom $n(r)=\frac{1}{\pi a_0^3}\exp\left ( \frac{-2r}{a_0}\right)$
mit $a_0$ der Bohrscher Radius eingesetzt werden:.

                                      {{15}}
$$\Rightarrow f_H= 4\pi \int_{0}^{\infty} \left (\frac{\frac{1}{\pi a_0^3}\exp\left ( \frac{-2r}{a_0}\right)}{\Delta kr} \cdot   r^2 \cdot 2 \sin ( \Delta k r ) \right) dr $$

                                      {{16}}
$$\Rightarrow f_H= \frac{4}{a_0^3} \int_{0}^{\infty} \left ( \exp\left ( \frac{-2r}{a_0}\right)\cdot   r^2 \cdot \frac{ \sin ( \Delta k r ) }{\Delta kr} \right) dr $$

                                      {{17}}
Dafür muss bei dem Ausdruck für $f_H$ folgende Substitution vorgenommen werden:    
    $\Delta k \cdot r=x$ und $\Delta k dr=dx$


                                      {{18}}
$$\Rightarrow f_H= \frac{4}{a_0^3 } \int_{0}^{\infty} \frac{x^2}{\Delta k^2}e^{  \frac{-2x}{a_0\cdot \Delta k}} \cdot  \frac{ \sin ( x ) }{x} \frac{dx}{\Delta k}=  \frac{4}{a_0^3 \Delta k^3} \int_{0}^{\infty} x e^{  \frac{-2x}{a_0\cdot \Delta k}} \cdot   \sin ( x )  dx$$

                                      {{19}}
An dieser Stelle benötigt der Normalmensch ein [Onlinetool zum Integrallösen](https://www.wolframalpha.com/calculators/integral-calculator/) oder ein altes Tafelwerk ([Bronstein Nr. 463](https://zbmath.org/?q=an:0997.00529)) .

                                      {{20}}
Mit größerer Wahrscheinlichkeit kommen Sie zu folgender Erkenntnis, dass sich folgendes Integral nutzen lässt:
$$\int e^{ax}\cdot x \cdot \sin(bx) dx=\frac{x\cdot e^{ax}}{a^2+b^2}[a \sin(bx)-b \cos(bx)]-\frac{ e^{ax}}{(a^2+b^2)^2}[(a^2-b^2) \sin(bx)-2ab \cos(bx)]$$
Dabei ist $a=  \frac{-2}{a_0\cdot \Delta k}$ und $b=1$.

                                      {{21}}
Einsetzen der Integrationsgrenzen:

                                      {{21}}
+ für $x\rightarrow \infty$ gilt $\frac{x\cdot e^{ax}}{a^2+b^2} \rightarrow 0$, da $a=a=  \frac{-2}{a_0\cdot \Delta k}$ negativ ist.
+ für $x\rightarrow \infty$ gilt $\frac{ e^{ax}}{a^2+b^2} \rightarrow 0$, da $a=a=  \frac{-2}{a_0\cdot \Delta k}$ negativ ist.
+ für $x\rightarrow 0$ gilt $\frac{x\cdot e^{ax}}{a^2+b^2} \rightarrow 0$, da $x\rightarrow 0$ im Produkt steht und $e^{ax} \rightarrow1$
+ für $x\rightarrow 0$ gilt $\frac{ e^{ax}}{a^2+b^2} \rightarrow \frac{1}{(a^2+b^2)^2}$

                                      {{21}}
Damit folgt für diesen Spezialfall der Integrationsgrenzen:
$$\int_0^{\infty} e^{ax}\cdot x \cdot \sin(bx) dx=\frac{1}{(a^2+b^2)^2}\cdot 2 a b \cos(b\cdot 0)=\frac{2 a b}{(a^2+b^2)^2}$$

                                      {{22}}
Nun wird  $a=  \frac{-2}{a_0\cdot \Delta k}$ und $b=1$ zurück eingesetzt:
$$f_H=  \frac{4}{a_0^3 \Delta k^3} \cdot \frac{2\left (-\frac{2}{\Delta k a_0} \cdot 1\right )}{\left (\left(-\frac{2}{\Delta k a_0}\right)^2 + 1^2 \right)^2}=\frac{-16}{a_0^4 \Delta k^4 \left (\left(-\frac{2}{\Delta k a_0}\right)^2 + 1^2 \right)^2}=\frac{-16}{  \left(4 +  \Delta k^2 a_0^2 \right)^2}$$

                                      {{22}}
Beachten Sie:

                                      {{22}}
+ für die Vorwärtsstreuung, d. h.  $\Delta k=0$      ist $ f_{H }=1$. Das entspricht der Ladung des H-Atoms .
+ für die Rutherford Streuung $\Delta k \cdot  a\gg 1 $   ist $ f_{H } \sim\ \frac{1}{\Delta k^4}$

                                      {{23}}
Bitte beachten Sie, dass bei der Streuung an einem einzelnen Atom alle Streuvektoren $\Delta k$ erlaubt sind, im Gegensatz zur Streuung am Kristall. 

                                      {{24}}
Geschafft!

