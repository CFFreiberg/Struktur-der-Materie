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

import: https://raw.githubusercontent.com/LiaTemplates/Pyodide/master/README.md




-->
<!-- Slider -->
@input(range, min=1, max=30, step=1, value=4) @m
Slider-Wert: **@m**



                                      

```python @plot_script
import numpy as np
import matplotlib.pyplot as plt

# Parameter
x_min = -1.1
x_max = 1.1
x_num = 1000
y_min = 0
y_max = 100

x_label = r"$\frac{\Delta k \cdot a}{2\pi}$"
y_label = r"$\|F|^2$"

# Funktion
def f(variable, m):
    return np.sin(np.pi * variable * m)**2 / np.sin(np.pi * variable)**2

# Slider-Wert aus LiaScript
m = int(LIA.m)

# Daten
x = np.linspace(x_min, x_max, x_num)
y = f(x, m)

# Plot
fig, ax = plt.subplots()
ax.plot(x, y, lw=3)

ax.set_xlabel(x_label)
ax.set_ylabel(y_label)
ax.set_ylim(y_min, y_max)
ax.set_title(f"Anzahl der Atome: {m}")

plt.show()
main()
```
@Pyodide.eval(`["main.py"]`, `python3 -m compileall .`, `python3 main.py`)


