---
title: Torsión
subtitle: Ejemplo
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: Torsión
grade: "Grado: [° Año]"
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
  - \fancyhead[L]{Torsión - Ejemplo}
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
\sigma_x = -150\ \text{kg/m}^2, \quad \sigma_y = 100\ \text{kg/m}^2, \quad \tau_{xy} = 80\ \text{kg/m}^2
$$



## **1. Esfuerzos principales ($\sigma_{\text{max}}, \sigma_{\text{min}}$)**

$$
\sigma_{1,2} = \frac{\sigma_x + \sigma_y}{2} \pm \sqrt{\left( \frac{\sigma_x - \sigma_y}{2} \right)^2 + \tau_{xy}^2}
$$

$$
\sigma_{\text{prom}} = \frac{-150 + 100}{2} = -25
$$
$$
R = \sqrt{\left( \frac{-150 - 100}{2} \right)^2 + 80^2} = \sqrt{(-125)^2 + 6400}
$$
$$
R = \sqrt{15625 + 6400} = \sqrt{22025} \approx 148.41
$$

Entonces:

$$
\sigma_1 = -25 + 148.41 \approx 123.41\ \text{kg/m}^2
$$
$$
\sigma_2 = -25 - 148.41 \approx -173.41\ \text{kg/m}^2
$$

$$
\boxed{\sigma_{\text{max}} = 123.41\ \text{kg/m}^2}
$$
$$
\boxed{\sigma_{\text{min}} = -173.41\ \text{kg/m}^2}
$$



## **2. Ángulo de esfuerzos principales ($2\theta_p$)**

$$
\tan(2\theta_p) = \frac{2\tau_{xy}}{\sigma_x - \sigma_y} = \frac{160}{-250} = -0.64
$$
$$
2\theta_p = \arctan(-0.64) \approx -32.62^\circ \quad \text{(o } 147.38^\circ \text{ para el otro plano)}
$$

Normalmente tomamos el ángulo agudo respecto al eje x, pero aquí depende de cuál esfuerzo principal corresponde.  
Por el círculo de Mohr, el ángulo desde $\sigma_x$ al $\sigma_{\text{max}}$ es $\theta_p \approx -16.31^\circ$ (sentido horario).

$$
\boxed{2\theta_p \approx -32.62^\circ}
$$



## **3. Esfuerzo cortante máximo ($\tau_{\text{max}}$)**

$$
\tau_{\text{max}} = R = 148.41\ \text{kg/m}^2
$$
$$
\boxed{\tau_{\text{max}} = 148.41\ \text{kg/m}^2}
$$



## **4. Esfuerzo normal en el plano de $\tau_{\text{max}}$**

$$
\sigma_n = \frac{\sigma_x + \sigma_y}{2} = -25\ \text{kg/m}^2
$$
$$
\boxed{\sigma_n = -25\ \text{kg/m}^2}
$$



## **5. Ángulo para cortante máximo ($2\theta_c$)**

$$
2\theta_c = 2\theta_p + 90^\circ \approx -32.62^\circ + 90^\circ = 57.38^\circ
$$
$$
\boxed{2\theta_c \approx 57.38^\circ}
$$



## **6. Para $\theta = 20^\circ$, hallar $\sigma, \tau$**

Fórmulas:

$$
\sigma_{x'} = \frac{\sigma_x + \sigma_y}{2} + \frac{\sigma_x - \sigma_y}{2} \cos 2\theta + \tau_{xy} \sin 2\theta
$$
$$
\tau_{x'y'} = -\frac{\sigma_x - \sigma_y}{2} \sin 2\theta + \tau_{xy} \cos 2\theta
$$

Para $\theta = 20^\circ$ → $2\theta = 40^\circ$:

$$
\sigma = -25 + \left( \frac{-150 - 100}{2} \right) \cos 40^\circ + 80 \sin 40^\circ
$$
$$
\sigma = -25 + (-125) \times 0.7660 + 80 \times 0.6428
$$
$$
\sigma = -25 - 95.75 + 51.424 \approx -69.326\ \text{kg/m}^2
$$

$$
\tau = -\left( \frac{-150 - 100}{2} \right) \sin 40^\circ + 80 \cos 40^\circ
$$
$$
\tau = -(-125) \times 0.6428 + 80 \times 0.7660
$$
$$
\tau = 80.35 + 61.28 \approx 141.63\ \text{kg/m}^2
$$

$$
\boxed{\sigma \approx -69.33\ \text{kg/m}^2,\quad \tau \approx 141.63\ \text{kg/m}^2}
$$



**Resumen con $\sigma_x = -150$**:
1. $\sigma_{\text{max}} \approx 123.41$
2. $\sigma_{\text{min}} \approx -173.41$
3. $2\theta_p \approx -32.62^\circ$
4. $\tau_{\text{max}} \approx 148.41$
5. $\sigma_n = -25$
6. $2\theta_c \approx 57.38^\circ$
7. Para $\theta=20^\circ$: $\sigma \approx -69.33,\ \tau \approx 141.63$