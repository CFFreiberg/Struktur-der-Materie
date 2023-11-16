<!--
author:   Claudia Funke

email:    claudia.funke@physik.tu-freiberg.de

version:  0.0.1

language: de

narrator: Deutsch Female

comment:  Struktur der Materie Übung 6

import: https://raw.githubusercontent.com/liaTemplates/KekuleJS/master/README.md

-->



## Aufgabe 4
>__4.__  Zeigen Sie für ein einfach kubisches Gitter, dass $d_\mathrm{hkl}^2=\frac{a^2}{h^2+k^2+l^2} $ gilt!



**Lösung Aufgabe 4:**

Für ein einfach kubisches Gitter gilt: 

$$\vec{G}= \left ( h\cdot \vec{b}_1+k\cdot \vec{b}_2+l\cdot \vec{b}_3\right)= \frac{2\pi}{a^3} \left ( h\cdot \vec{a}_2 \times \vec{a}_3 +k\cdot \vec{a}_3 \times \vec{a}_1+l\cdot \vec{a}_1 \times \vec{a}_2\right)$$

Für das kubische System folgt mit $\vec{a}_1=a\cdot \vec{\hat{x}}$, $\vec{a}_2=a\cdot \vec{\hat{y}}$ und $\vec{a}_3=a\cdot \vec{\hat{z}}$ mit $\vec{\hat{x}}$, $\vec{\hat{y}}$ und $\vec{\hat{z}} orthogonales System von Einheitsvektoren: 


$$\vec{G}=\frac{2\pi}{a^3} \cdot (h\cdot  a^2 \cdot  \vec{\hat{y}}\times \vec{\hat{z}}  + k\cdot  a^2 \cdot \vec{\hat{z}}\times \vec{\hat{x}}+ l\cdot a^2 \cdot \vec{\hat{x}}\times \vec{\hat{y}})$$

Für das kubische System gilt:

$\vec{\hat{y}} \times \vec{\hat{z}}=\vec{\hat{x}}$, $\vec{\hat{z}} \times \vec{\hat{x}}=\vec{\hat{y}} $ und $\vec{\hat{x}} \times \vec{\hat{y}}=\vec{\hat{z}}$ .

$$\Rightarrow \vec{G}=\frac{2\pi a^2}{a} \cdot (h \vec{\hat{x}}  + k \cdot \vec{\hat{y}}+ l^2\cdot \vec{\hat{z}})$$



$$\Rightarrow |\vec{G}|=\frac{2\pi}{a} \sqrt{h^2  + k^2 + l^2} $$





$$\Rightarrow d_\mathrm{hkl} =\frac{2\pi}{|\vec{G}|}=2\pi\cdot \frac{a}{2\pi(\sqrt{h^2  + k^2 + l^2} }=\frac{a}{\sqrt{h^2+k^2+l^2}}$$
