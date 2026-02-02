---
title: "Ejemplo inercia"
subtitle: "Momentos de inercia"
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: "Materiales"
grade: "Grado: [2° Año]"
geometry: margin=1in
fontsize: 12pt
lang: es
documentclass: article
header-includes:
  - \usepackage{amsmath}
  - \usepackage{amssymb}
  - \usepackage{mathtools}
  - \everymath{\displaystyle}
  - \everydisplay{\displaystyle}
  - \usepackage{xcolor}
  - \usepackage{tcolorbox}
  - \usepackage{fancyhdr}
  - \pagestyle{fancy}
  - \fancyhead[L]{Materiales}
  - \fancyhead[R]{2}
  - \fancyfoot[C]{\thepage}
  - \tcbuselibrary{most}
  - \newtcolorbox{objetivo}{colback=green!5!white,colframe=green!75!black,title=OBJETIVO}
  - \newtcolorbox{definicion}{colback=yellow!5!white,colframe=orange!75!black,title=DEFINICIÓN}
  - \newtcolorbox{ejemplo}{colback=blue!5!white,colframe=blue!75!black,title=EJEMPLO}
  - \newtcolorbox{ejercicio}{colback=cyan!5!white,colframe=cyan!75!black,title=EJERCICIO}
  - \newtcolorbox{formula}{colback=gray!5!white,colframe=gray!75!black,title=FÓRMULA}
  - \newtcolorbox{nota}{colback=red!5!white,colframe=red!75!black,title=NOTA IMPORTANTE}
--- 
 <!-- pandoc file.md -o file.pdf --pdf-engine=xelatex, puedes usar los begin con: objetivo, definicion, ejemplo, ejercicio, formula, nota-->

$$
I_x = 25.14,\quad I_y = 10.44,\quad I_{xy} = 7.14
$$



## 1. Momentos de inercia principales

Usamos la fórmula:

$$
I_{max, min} = \frac{I_x + I_y}{2} \pm \sqrt{\left( \frac{I_x - I_y}{2} \right)^2 + I_{xy}^2}
$$

### Cálculo paso a paso:

$$
\frac{I_x + I_y}{2} = \frac{25.14 + 10.44}{2} = \frac{35.58}{2} = 17.79
$$

$$
\frac{I_x - I_y}{2} = \frac{25.14 - 10.44}{2} = \frac{14.70}{2} = 7.35
$$

$$
\left( \frac{I_x - I_y}{2} \right)^2 = (7.35)^2 = 54.0225
$$

$$
I_{xy}^2 = (7.14)^2 = 50.9796
$$

$$
\text{Radical} = \sqrt{54.0225 + 50.9796} = \sqrt{105.0021} \approx 10.247
$$



### Momentos principales:

$$
I_{max} = 17.79 + 10.247 = 28.037
$$
$$
I_{min} = 17.79 - 10.247 = 7.543
$$



## 2. Ángulo de los ejes principales

$$
\tan 2\theta_p = \frac{2 I_{xy}}{I_y - I_x} = \frac{2 \times 7.14}{10.44 - 25.14}
$$

$$
\tan 2\theta_p = \frac{14.28}{-14.70} \approx -0.97143
$$

$$
2\theta_p = \arctan(-0.97143)
$$

Dado que el numerador es positivo y el denominador negativo, $2\theta_p$ está en el segundo cuadrante:

$$
2\theta_p = 180^\circ - \arctan(0.97143) \approx 180^\circ - 44.14^\circ = 135.86^\circ
$$

$$
\theta_p \approx 67.93^\circ
$$

Esto significa que el eje principal correspondiente a $I_{max}$ está a $67.93^\circ$ del eje $x$ original, en sentido antihorario.

**Resultado final:**

$$
\boxed{I_{max} = 28.04,\quad I_{min} = 7.54}
$$

$$
\theta_p = 67.93^\circ
$$