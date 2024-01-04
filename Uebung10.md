<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 10
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
 

                                      {{3}}


{{3}}

``` python
# Quelle: zusammenkopiert aus https://matplotlib.org

import sys
import numpy as np
import matplotlib.pyplot as plt


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
    x_label = r"$\\dfrac{R }{\\sigma}$"
    y_label = r"$\\dfrac{U }{\\varepsilon}$"
    x = np.linspace(x_min, x_max, x_num)
    fig, ax = plt.subplots()
    line, = ax.plot(x, f1(x),'r--')
    line, = ax.plot(x, f2(x),'b--')
    line, = ax.plot(x, f3(x),'g')
    plt.legend((r"$+\\left (\\dfrac{\\sigma}{R}\\right)^{12}$", r"$-\\left (\\dfrac{\\sigma}{R}\\right)^{6}$", r"$+\\left (\\dfrac{\\sigma}{R}\\right)^{12}-\\left (\\dfrac{\\sigma}{R}\\right)^{6}$" ),loc='upper center', shadow=True)
    plt.grid(True)
    ax.set_xlabel(x_label)
    ax.set_ylabel(y_label)
    ax.set_ylim(y_min, y_max)
    
    plt.show()
main()
```
@Pyodide.eval(`["main.py"]`, `python3 -m compileall .`, `python3 main.py`)

                                      {{4}}
![Lennard-Jones-Potential mit abstoßendem und anziehendem Anteil](media/Lennard-Jones-potential2.png "[Lennard-Jones-Potential; Quelle: MSU Department of Physics and Astronomy, Computational Math Science and Engineering and the Lyman Briggs College](https://physicsatmcl.commons.msu.edu/lennard-jones-potential/), [CC BY-NC-SA 4.0 Deed](https://creativecommons.org/licenses/by-nc-sa/4.0/)")




## Aufgabe 2
                                      {{0}}
> __2.__ Welcher Bereich vom Wellenvektor K hat für elastische Wellen eine sinnvolle physikalische Bedeutung und warum?


                                      {{1}}
**Lösung Aufgabe 2:**

                                      {{2}}


                                      {{3}}




## Aufgabe 3 
                                      {{0}}
> __3.__ Welche Bedeutung kommt einer elastischen Welle zu, wenn dessen Wellenvektor K auf den Grenzen der 1. Brillouin-Zone liegt?

                                      {{1}}
**Lösung Aufgabe 3:**

                                      {{2}}


## Aufgabe 4 

                                      {{0}}
> __4.__ Wie ist die Gruppengeschwindigkeit eines Wellenpaketes definiert? Welche Bedeutung hat die Gruppengeschwindigkeit?

                                      {{1}}
**Lösung Aufgabe 4:**

                                      {{2}}


                                      {{3}}


                                      {{3}}


## Aufgabe 5 
                                      {{0}}
>__5.__ Betrachten Sie eine lineare monoatomare Kette aus äquidistanten Atomen der Masse M im Abstand a, die um ihre Gleichgewichtslage kleine Schwingungen ausführen können (longitudinale Polarisation, harmonische Näherung). Eine Wechselwirkung bestehe ausschließlich zwischen nächsten Nachbarn und sei durch die Federkonstante C charakterisiert. Die Position des n–ten Atoms sei durch xn(t) = na + un(t) beschrieben.


>__a)__ Zeigen Sie, dass die Auslenkung un(t) des n–ten Atoms der Differentialgleichung $M\cdot \frac{\partial u_n(t)}{\partial t^2}=-C \left[2u_n(t)-u_{n+1}(t)-u_{n-1}(t)\right]$ genügt.

>__b)__ Lösen Sie obige Gleichung mit dem Ansatz un(t) = u0(t) eiKna und leiten Sie eine Dispersionsrelation zwischen Frequenz ω und der Wellenzahl K ab. 

>__c)__ Diskutieren Sie den langwelligen Limes Ka <<1 und zeigen Sie insbesondere, dass sich aus obiger Gleichung die (Schall–) Wellengeichung  $ \frac{\partial^2 u(x,t)}{\partial t^2}-v_s^2\frac{\partial^2 u(x,t)}{\partial x^2}=0$   ergibt, wenn man zur Kontinuumsbeschreibung un±1(t) = u(x ± a, t) übergeht.

                                      {{1}}
**Lösung Aufgabe 5:**

                                      {{2}}


                                      {{3}}


## Aufgabe 6 

                                      {{0}}
>__6.__ Gegeben sei eine lineare, monoatomare, quasi-elastische Kette aus Atomen der Masse M = 200amu. Der Abstand zwischen benachbarten Atomen sei a = 4Å. Beachten Sie nur Wechselwirkungen zwischen nächsten Nachbarn. 
a) Die Schallgeschwindigkeit sei 4000m/s. Wie groß ist die Koppelungskonstante C zwischen benachbarten Atomen?
b) Wie groß ist die maximale Frequenz der (ungedämpften) Welle?


                                      {{1}}
**Lösung Aufgabe 6:**

                                      {{2}}



## Aufgabe 7 

                                      {{0}}
>__7.__ Wie kann man sich anschaulich optische und akustische Zustände elastischer Wellen vorstellen? 

                                      {{1}}
**Lösung Aufgabe 7:**

                                      {{2}}



## Aufgabe 8 
                                      {{0}}
>__8.__ Wie viele „Äste“ liefert die Dispersionsrelation für elastische Wellen, wenn die Elementarzelle p Atome besitzt. Wie viele davon sind akustische und optische Äste?


                                      {{0}}
![XX](media/EbenesGitterMadelung.png "*Quelle:  A. Armbrust, H. Janetzki, Aufgaben zur Festkörperphysik*")



                                      {{1}}
**Lösung Aufgabe 8:**

                                      {{2}}


## Aufgabe 9
                                      {{0}}
>__9.__ 9.	Wie heißt der Energiequant einer elastischen Welle?

**Lösung Aufgabe 9:**

                                      {{2}}



## Aufgabe 10
                                      {{0}}
>__10.__ Wie groß ist die Energie eines elastischen Schwingungszustandes mit der Kreisfrequenz wenn der Zustand zu Quantenzahl n angeregt ist?

                                      {{1}}
**Lösung Aufgabe 10:**

                                      {{2}}


## Aufgabe 11
                                      {{0}}
>__11.__ Was ist ein weiches Phonon?

                                      {{1}}
**Lösung Aufgabe 11:**

                                      {{2}}


## Aufgabe 12
                                      {{0}}
>__12.__ Für ein Gitter mit zwei Atomen in der primitiven Einheitszelle sollen die Amplitudenverhältnisse u/v für beide Äste der elastischen Welle bei Kmax=/a bestimmt werden! Zeigen Sie, dass bei diesem K-Wert die beiden Gitter entkoppelt erscheinen: Ein Gitter bleibt in Ruhe, während das andere schwingt.

                                      {{1}}
**Lösung Aufgabe 12:**

                                      {{2}}