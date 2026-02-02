---
title: torsi'on
subtitle: torsion
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: torsion
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
  - \fancyhead[L]{torsi'on - torsion}
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


# Problema 1
$$
\sigma_x = -840\ \text{kg/m}^2, \quad \sigma_y = 1050\ \text{kg/m}^2, \quad \tau_{xy} = 560\ \text{kg/m}^2
$$



## **1. Esfuerzos principales ($\sigma_{\text{max}}, \sigma_{\text{min}}$)**

$$
\sigma_{1,2} = \frac{\sigma_x + \sigma_y}{2} \pm \sqrt{\left( \frac{\sigma_x - \sigma_y}{2} \right)^2 + \tau_{xy}^2}
$$

$$
\sigma_{\text{prom}} = \frac{-840 + 1050}{2} = 105
$$
$$
R = \sqrt{\left( \frac{-840 - 1050}{2} \right)^2 + 560^2} = \sqrt{(-945)^2 + 560^2}
$$
$$
R = \sqrt{893025 + 313600} = \sqrt{1206625} \approx 1098.465
$$

Entonces:

$$
\sigma_1 = 105 + 1098.465 \approx 1203.465\ \text{kg/m}^2
$$
$$
\sigma_2 = 105 - 1098.465 \approx -993.465\ \text{kg/m}^2
$$

$$
\boxed{\sigma_{\text{max}} = 1203.47\ \text{kg/m}^2}
$$
$$
\boxed{\sigma_{\text{min}} = -993.47\ \text{kg/m}^2}
$$



## **2. Ángulo de esfuerzos principales ($2\theta_p$)**

$$
\tan(2\theta_p) = \frac{2\tau_{xy}}{\sigma_x - \sigma_y} = \frac{1120}{-1890} \approx -0.59259
$$
$$
2\theta_p = \arctan(-0.59259) \approx -30.64^\circ
$$

$$
\boxed{2\theta_p \approx -30.64^\circ}
$$



## **3. Esfuerzo cortante máximo ($\tau_{\text{max}}$)**

$$
\tau_{\text{max}} = R = 1098.465\ \text{kg/m}^2
$$
$$
\boxed{\tau_{\text{max}} = 1098.47\ \text{kg/m}^2}
$$



## **4. Esfuerzo normal en el plano de $\tau_{\text{max}}$**

$$
\sigma_n = \frac{\sigma_x + \sigma_y}{2} = 105\ \text{kg/m}^2
$$
$$
\boxed{\sigma_n = 105\ \text{kg/m}^2}
$$



## **5. Ángulo para cortante máximo ($2\theta_c$)**

$$
2\theta_c = 2\theta_p + 90^\circ \approx -30.64^\circ + 90^\circ = 59.36^\circ
$$
$$
\boxed{2\theta_c \approx 59.36^\circ}
$$



## **6. Para $\theta = 20^\circ$, hallar $\sigma, \tau$**

Fórmulas de transformación:

$$
\sigma_{x'} = \frac{\sigma_x + \sigma_y}{2} + \frac{\sigma_x - \sigma_y}{2} \cos 2\theta + \tau_{xy} \sin 2\theta
$$
$$
\tau_{x'y'} = -\frac{\sigma_x - \sigma_y}{2} \sin 2\theta + \tau_{xy} \cos 2\theta
$$

Para $\theta = 20^\circ$ → $2\theta = 40^\circ$:

$$
\sigma = 105 + \left( \frac{-840 - 1050}{2} \right) \cos 40^\circ + 560 \sin 40^\circ
$$
$$
\sigma = 105 + (-945) \times 0.766044 + 560 \times 0.642788
$$
$$
\sigma = 105 - 723.912 + 359.961 \approx -258.951\ \text{kg/m}^2
$$

$$
\tau = -\left( \frac{-840 - 1050}{2} \right) \sin 40^\circ + 560 \cos 40^\circ
$$
$$
\tau = -(-945) \times 0.642788 + 560 \times 0.766044
$$
$$
\tau = 607.434 + 428.985 \approx 1036.419\ \text{kg/m}^2
$$

$$
\boxed{\sigma \approx -258.95\ \text{kg/m}^2,\quad \tau \approx 1036.42\ \text{kg/m}^2}
$$



**Resumen final**:

1. $\sigma_{\text{max}} \approx 1203.47\ \text{kg/m}^2$
2. $\sigma_{\text{min}} \approx -993.47\ \text{kg/m}^2$
3. $2\theta_p \approx -30.64^\circ$
4. $\tau_{\text{max}} \approx 1098.47\ \text{kg/m}^2$
5. $\sigma_n = 105\ \text{kg/m}^2$
6. $2\theta_c \approx 59.36^\circ$
7. Para $\theta=20^\circ$: $\sigma \approx -258.95\ \text{kg/m}^2,\ \tau \approx 1036.42\ \text{kg/m}^2$

# Problema 2

$$
\sigma_x = 840\ \text{kg/m}^2, \quad \sigma_y = 1050\ \text{kg/m}^2, \quad \tau_{xy} = -560\ \text{kg/m}^2
$$



## **1. Esfuerzos principales ($\sigma_{\text{max}}, \sigma_{\text{min}}$)**

$$
\sigma_{1,2} = \frac{\sigma_x + \sigma_y}{2} \pm \sqrt{\left( \frac{\sigma_x - \sigma_y}{2} \right)^2 + \tau_{xy}^2}
$$

$$
\sigma_{\text{prom}} = \frac{840 + 1050}{2} = 945
$$
$$
R = \sqrt{\left( \frac{840 - 1050}{2} \right)^2 + (-560)^2} = \sqrt{(-105)^2 + 313600}
$$
$$
R = \sqrt{11025 + 313600} = \sqrt{324625} \approx 569.76
$$

Entonces:

$$
\sigma_1 = 945 + 569.76 \approx 1514.76\ \text{kg/m}^2
$$
$$
\sigma_2 = 945 - 569.76 \approx 375.24\ \text{kg/m}^2
$$

$$
\boxed{\sigma_{\text{max}} = 1514.76\ \text{kg/m}^2}
$$
$$
\boxed{\sigma_{\text{min}} = 375.24\ \text{kg/m}^2}
$$



## **2. Ángulo de esfuerzos principales ($2\theta_p$)**

$$
\tan(2\theta_p) = \frac{2\tau_{xy}}{\sigma_x - \sigma_y} = \frac{-1120}{-210} \approx 5.3333
$$
$$
2\theta_p = \arctan(5.3333) \approx 79.38^\circ
$$

$$
\boxed{2\theta_p \approx 79.38^\circ}
$$



## **3. Esfuerzo cortante máximo ($\tau_{\text{max}}$)**

$$
\tau_{\text{max}} = R = 569.76\ \text{kg/m}^2
$$
$$
\boxed{\tau_{\text{max}} = 569.76\ \text{kg/m}^2}
$$



## **4. Esfuerzo normal en el plano de $\tau_{\text{max}}$**

$$
\sigma_n = \frac{\sigma_x + \sigma_y}{2} = 945\ \text{kg/m}^2
$$
$$
\boxed{\sigma_n = 945\ \text{kg/m}^2}
$$



## **5. Ángulo para cortante máximo ($2\theta_c$)**

$$
2\theta_c = 2\theta_p + 90^\circ \approx 79.38^\circ + 90^\circ = 169.38^\circ
$$
$$
\boxed{2\theta_c \approx 169.38^\circ}
$$



## **6. Para $\theta = 20^\circ$, hallar $\sigma, \tau$**

Fórmulas de transformación:

$$
\sigma_{x'} = \frac{\sigma_x + \sigma_y}{2} + \frac{\sigma_x - \sigma_y}{2} \cos 2\theta + \tau_{xy} \sin 2\theta
$$
$$
\tau_{x'y'} = -\frac{\sigma_x - \sigma_y}{2} \sin 2\theta + \tau_{xy} \cos 2\theta
$$

Para $\theta = 20^\circ$ → $2\theta = 40^\circ$:

$$
\sigma = 945 + \left( \frac{840 - 1050}{2} \right) \cos 40^\circ + (-560) \sin 40^\circ
$$
$$
\sigma = 945 + (-105) \times 0.766044 - 560 \times 0.642788
$$
$$
\sigma = 945 - 80.435 - 359.961 \approx 504.604\ \text{kg/m}^2
$$

$$
\tau = -\left( \frac{840 - 1050}{2} \right) \sin 40^\circ + (-560) \cos 40^\circ
$$
$$
\tau = -(-105) \times 0.642788 - 560 \times 0.766044
$$
$$
\tau = 67.493 - 428.985 \approx -361.492\ \text{kg/m}^2
$$

$$
\boxed{\sigma \approx 504.60\ \text{kg/m}^2,\quad \tau \approx -361.49\ \text{kg/m}^2}
$$



**Resumen final**:

1. $\sigma_{\text{max}} \approx 1514.76\ \text{kg/m}^2$
2. $\sigma_{\text{min}} \approx 375.24\ \text{kg/m}^2$
3. $2\theta_p \approx 79.38^\circ$
4. $\tau_{\text{max}} \approx 569.76\ \text{kg/m}^2$
5. $\sigma_n = 945\ \text{kg/m}^2$
6. $2\theta_c \approx 169.38^\circ$
7. Para $\theta=20^\circ$: $\sigma \approx 504.60\ \text{kg/m}^2,\ \tau \approx -361.49\ \text{kg/m}^2$

# Problema 4

$$
\sigma_x = -840\ \text{kg/m}^2, \quad \sigma_y = 0\ \text{kg/m}^2, \quad \tau_{xy} = 280\ \text{kg/m}^2
$$



## **1. Esfuerzos principales ($\sigma_{\text{max}}, \sigma_{\text{min}}$)**

$$
\sigma_{1,2} = \frac{\sigma_x + \sigma_y}{2} \pm \sqrt{\left( \frac{\sigma_x - \sigma_y}{2} \right)^2 + \tau_{xy}^2}
$$

$$
\sigma_{\text{prom}} = \frac{-840 + 0}{2} = -420
$$
$$
R = \sqrt{\left( \frac{-840 - 0}{2} \right)^2 + 280^2} = \sqrt{(-420)^2 + 280^2}
$$
$$
R = \sqrt{176400 + 78400} = \sqrt{254800} \approx 504.78
$$

Entonces:

$$
\sigma_1 = -420 + 504.78 \approx 84.78\ \text{kg/m}^2
$$
$$
\sigma_2 = -420 - 504.78 \approx -924.78\ \text{kg/m}^2
$$

$$
\boxed{\sigma_{\text{max}} = 84.78\ \text{kg/m}^2}
$$
$$
\boxed{\sigma_{\text{min}} = -924.78\ \text{kg/m}^2}
$$



## **2. Ángulo de esfuerzos principales ($2\theta_p$)**

$$
\tan(2\theta_p) = \frac{2\tau_{xy}}{\sigma_x - \sigma_y} = \frac{560}{-840} \approx -0.66667
$$
$$
2\theta_p = \arctan(-0.66667) \approx -33.69^\circ
$$

$$
\boxed{2\theta_p \approx -33.69^\circ}
$$



## **3. Esfuerzo cortante máximo ($\tau_{\text{max}}$)**

$$
\tau_{\text{max}} = R = 504.78\ \text{kg/m}^2
$$
$$
\boxed{\tau_{\text{max}} = 504.78\ \text{kg/m}^2}
$$



## **4. Esfuerzo normal en el plano de $\tau_{\text{max}}$**

$$
\sigma_n = \frac{\sigma_x + \sigma_y}{2} = -420\ \text{kg/m}^2
$$
$$
\boxed{\sigma_n = -420\ \text{kg/m}^2}
$$



## **5. Ángulo para cortante máximo ($2\theta_c$)**

$$
2\theta_c = 2\theta_p + 90^\circ \approx -33.69^\circ + 90^\circ = 56.31^\circ
$$
$$
\boxed{2\theta_c \approx 56.31^\circ}
$$



## **6. Para $\theta = 20^\circ$, hallar $\sigma, \tau$**

Fórmulas de transformación:

$$
\sigma_{x'} = \frac{\sigma_x + \sigma_y}{2} + \frac{\sigma_x - \sigma_y}{2} \cos 2\theta + \tau_{xy} \sin 2\theta
$$
$$
\tau_{x'y'} = -\frac{\sigma_x - \sigma_y}{2} \sin 2\theta + \tau_{xy} \cos 2\theta
$$

Para $\theta = 20^\circ$ → $2\theta = 40^\circ$:

$$
\sigma = -420 + \left( \frac{-840 - 0}{2} \right) \cos 40^\circ + 280 \sin 40^\circ
$$
$$
\sigma = -420 + (-420) \times 0.766044 + 280 \times 0.642788
$$
$$
\sigma = -420 - 321.738 + 179.981 \approx -561.757\ \text{kg/m}^2
$$

$$
\tau = -\left( \frac{-840 - 0}{2} \right) \sin 40^\circ + 280 \cos 40^\circ
$$
$$
\tau = -(-420) \times 0.642788 + 280 \times 0.766044
$$
$$
\tau = 269.971 + 214.492 \approx 484.463\ \text{kg/m}^2
$$

$$
\boxed{\sigma \approx -561.76\ \text{kg/m}^2,\quad \tau \approx 484.46\ \text{kg/m}^2}
$$



**Resumen final**:

1. $\sigma_{\text{max}} \approx 84.78\ \text{kg/m}^2$
2. $\sigma_{\text{min}} \approx -924.78\ \text{kg/m}^2$
3. $2\theta_p \approx -33.69^\circ$
4. $\tau_{\text{max}} \approx 504.78\ \text{kg/m}^2$
5. $\sigma_n = -420\ \text{kg/m}^2$
6. $2\theta_c \approx 56.31^\circ$
7. Para $\theta=20^\circ$: $\sigma \approx -561.76\ \text{kg/m}^2,\ \tau \approx 484.46\ \text{kg/m}^2$
