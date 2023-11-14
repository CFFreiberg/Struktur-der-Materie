<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 6

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

-->




# Übung 6: 




> __1.__  Die primitiven Translationsvektoren des flächenzentrierten kubischen Gitters sind: $\vec{a}_1=\frac{a}{2}\cdot (\hat{y}+\hat{z}) $; $\vec{a}_2=\frac{a}{2}\cdot (\hat{x}+\hat{z})$; $\vec{a}_3=\frac{a}{2}\cdot (\hat{x}+\hat{y})$. Berechnen Sie die primitiven Translationsvektoren des reziproken Gitters! Was für ein reziprokes Gitter ergibt sich?




**Lösung Aufgabe 1a:**

Zuerst wird das Volumen der Einheitszelle im realen Gitter berechnet. Dabei wird folgende Darstellung der $\vec{a_i} $ benutzt:


$\vec{a}_1=\frac{a}{2}\left(\begin{array}{c} 0 \\ 1 \\ 1 \end{array}\right) $, $\vec{a}_2=\frac{a}{2}\left(\begin{array}{c} 1 \\ 0 \\ 1 \end{array}\right) $; $\vec{a}_3=\frac{a}{2}\left(\begin{array}{c} 1 \\ 1 \\ 0 \end{array}\right) $; 

Damit ergibt sich 



$$V_\mathrm{EZ}=\vec{a}_1\cdot (\vec{a}_2\times \vec{a}_3)=\frac{a^3}{8}\left(\begin{array}{c} 0 \\ 1 \\ 1 \end{array}\right)\cdot \left [\left(\begin{array}{c} 1 \\ 0 \\ 1 \end{array}\right) \times \left(\begin{array}{c} 1 \\ 1 \\ 0 \end{array}\right) \right ]$$

$$\Rightarrow V_\mathrm{EZ}=\frac{a^3}{8}\left(\begin{array}{c} 1 \\ 1 \\ 0 \end{array}\right)\cdot \left(\begin{array}{c} 1 \\ 1 \\ -1 \end{array}\right)=\frac{1}{4}a^3$$

Laut Definition sind die reziproken Gittervektoren damit 

$$\vec{b}_1=\frac{2\pi}{V_\mathrm{EZ}}\cdot (\vec{a}_2\times\vec{a}_3)=\frac{2\pi \frac{a^2}{4}}{\frac{a^3}{4}} \left( \begin{array}{c} 1 \\ 0 \\ 1 \end{array} \right)\times \left(\begin{array}{c} 1 \\ 1 \\ 0 \end{array}\right)=\frac{2\pi}{a}\cdot \left( \begin{array}{c} -1 \\ 1 \\ 1 \end{array} \right)$$


$$\vec{b}_2=\frac{2\pi}{V_\mathrm{EZ}}\cdot (\vec{a}_2\times\vec{a}_3)=\frac{2\pi}{a}\left( \begin{array}{c} 1 \\ 1 \\ 0 \end{array} \right)\times \left(\begin{array}{c} 0 \\ 1 \\ 1 \end{array}\right)=\frac{2 \pi}{a}\cdot \left( \begin{array}{c} 1 \\ -1 \\ 1 \end{array} \right)  $$

$$\vec{b}_3=\frac{2\pi}{V_\mathrm{EZ}}\cdot (\vec{a}_2\times\vec{a}_3)=\frac{2\pi}{a}\cdot \left( \begin{array}{c} 0 \\ 1 \\ 1 \end{array} \right)\times \left(\begin{array}{c} 1 \\ 0 \\ 1 \end{array}\right)=\frac{2 \pi}{a}\cdot \left( \begin{array}{c} 1 \\ 1 \\ -1 \end{array} \right)  $$

Durch den Vergleich mit den primitiven Translationsvektoren anderer Raumgitter erkennt man, dass
es sich hierbei um ein kubisch raumzentriertes (bcc) Gitter mit Gitterkonstante $\frac{2 \pi}{a}$ handelt.

> __2.__  Berechnen Sie das reziproke Gitter des rhombischen Gitters.

Angenommen, wir haben ein rhombisches Gitter mit den Gittervektoren:

$$\vec{a_1}=a\cdot \vec{\hat{x}}$$
$$\vec{a_2}=b\cdot \vec{\hat{y}}$$
$$\vec{a_3}=c\cdot \vec{\hat{z}}$$
 mit $\vec{\hat{x}}, \vec{\hat{y}}, \vec{\hat{z}}$ Einheitsvektoren in die entsprechenden Richtungen und jeweils senkrecht aufeinander und $a\ne b\ne c$. 
 
Damit ergibt sich das Volumen der Einheitszelle (einfacher Quader)

$$V_\mathrm{EZ}=\vec{a}_1\cdot (\vec{a}_2\times \vec{a}_3)=a\cdot b\cdot c$$

Die reziproken Gittervektoren können berechnet werden über:
$$\vec{b}_1=\frac{2\pi}{V_\mathrm{EZ}}\cdot (\vec{a}_2\times\vec{a}_3)=\frac{2\pi \cdot b \cdot c} {a\cdot b \cdot c} \left( \begin{array}{c} 0 \\ 1 \\ 0 \end{array} \right)\times \left(\begin{array}{c} 0 \\ 0 \\ 1 \end{array}\right)=\frac{2\pi}{a}\cdot \left( \begin{array}{c} 1 \\ 0 \\ 0 \end{array} \right)=\frac{2\pi}{a}\cdot \vec{\hat{x}}$$

Und analog 

$$\vec{b}_2=\frac{2\pi}{b}\cdot \vec{\hat{y}}$$

   $$\vec{b}_3=\frac{2\pi}{c}\cdot \vec{\hat{z}}$$
Die Beträge der reziproken Gittervektoren sind umgekehrt proportional zu den Längen der entsprechenden Gittervektoren im realen Gitter.

> __3.__  Berechnen Sie den Netzebenenabstand im rhombischen Gitter.

> __4.__  Wie ist die Brillouin- Zone definiert? Zeichnen Sie für das folgende (ebene) reziproke Gitter die Brillouin- Zone!
