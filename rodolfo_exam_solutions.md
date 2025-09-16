---
title: "Título del Tema"
subtitle: "Subtítulo o Capítulo"
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: "Matemáticas"
grade: "Grado: [X° Año]"
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
  - \fancyhead[L]{Matemáticas - [Tema]}
  - \fancyhead[R]{[Grado]}
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

# Examen de Rodolfo - Primer Parcial
## Soluciones

## I. Determine el orden, grado y linealidad de las siguientes ecuaciones diferenciales

### a) $y' = (2y''')^2x^3 - \frac{2y'}{x+2} = (y')^4 e^x$

**Análisis:**
- **Orden:** La derivada de mayor orden es $y'''$ (tercera derivada), por lo tanto el **orden es 3**.
- **Grado:** La ecuación contiene $(y''')^2$ y $(y')^4$. Para determinar el grado, debemos expresar la ecuación en forma polinómica respecto a la derivada de mayor orden. Reordenando: $(2y''')^2x^3 = (y')^4 e^x + \frac{2y'}{x+2}$. El término de mayor orden $(y''')^2$ tiene exponente 2, por lo tanto el **grado es 2**.
- **Linealidad:** La ecuación contiene términos como $(y''')^2$ y $(y')^4$, que son no lineales en las derivadas. Por lo tanto, la ecuación es **no lineal**.

**Respuesta:** Orden = 3, Grado = 2, No lineal

### b) $\frac{dy}{dx} = 2 \sin(4xy) + \left( \frac{d^2y}{dx^2} \right)^3$

**Análisis:**
- **Orden:** La derivada de mayor orden es $\frac{d^2y}{dx^2}$ (segunda derivada), por lo tanto el **orden es 2**.
- **Grado:** El término $\left( \frac{d^2y}{dx^2} \right)^3$ indica que el **grado es 3**.
- **Linealidad:** La ecuación contiene $\sin(4xy)$ (función no lineal de $x$ e $y$) y $\left( \frac{d^2y}{dx^2} \right)^3$ (término no lineal en la derivada). Por lo tanto, la ecuación es **no lineal**.

**Respuesta:** Orden = 2, Grado = 3, No lineal

## II. Verifique que la solución dada satisface la ecuación diferencial indicada

### ED: $y' = 0.5(100-y)$
### Sol: $y = 5e^{-0.5x} + 100$

**Verificación:**

Primero calculamos $y'$:
$$y = 5e^{-0.5x} + 100$$
$$y' = 5 \cdot (-0.5) \cdot e^{-0.5x} + 0 = -2.5e^{-0.5x}$$

Ahora evaluamos el lado derecho de la ED:
$$0.5(100-y) = 0.5(100 - (5e^{-0.5x} + 100))$$
$$= 0.5(100 - 5e^{-0.5x} - 100)$$
$$= 0.5(-5e^{-0.5x})$$
$$= -2.5e^{-0.5x}$$

**Conclusión:** Como $y' = -2.5e^{-0.5x} = 0.5(100-y)$, la solución propuesta **sí satisface** la ecuación diferencial.

## III. Separe las variables y obtenga la solución general de la ecuación diferencial de primer orden

### a) $y' + ty = y$

**Solución:**

Primero reordenamos la ecuación:
$y' + ty = y$
$y' = y - ty$
$y' = y(1 - t)$

Dado que $(1 - t)$ es una constante, separamos variables:
$\frac{dy}{dx} = y(1 - t)$

Separando variables:
$\frac{dy}{y} = (1 - t)dx$

Integrando ambos lados:
$\int \frac{dy}{y} = \int (1 - t)dx$
$\ln|y| = (1 - t)x + C_1$

Por lo tanto:
$y = Ce^{(1-t)x}$

donde $C = e^{C_1}$ es la constante de integración.

**Solución general:** $y = Ce^{(1-t)x}$

## IV. Obtenga la solución general de la siguiente ecuación diferencial dada

### a) $(x + 2y^2)dx + (xy)dy = 0$

**Solución:**

Esta es una ecuación diferencial de la forma $M(x,y)dx + N(x,y)dy = 0$ donde:
- $M(x,y) = x + 2y^2$
- $N(x,y) = xy$

Verificamos si es exacta calculando:
$$\frac{\partial M}{\partial y} = \frac{\partial}{\partial y}(x + 2y^2) = 4y$$
$$\frac{\partial N}{\partial x} = \frac{\partial}{\partial x}(xy) = y$$

Como $\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$, la ecuación no es exacta.

Buscamos un factor integrante. Calculamos:
$$\frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N} = \frac{4y - y}{xy} = \frac{3y}{xy} = \frac{3}{x}$$

Como esto depende solo de $x$, existe un factor integrante $\mu(x)$:
$$\mu(x) = e^{\int \frac{3}{x}dx} = e^{3\ln|x|} = x^3$$

Multiplicando la ecuación por $\mu(x) = x^3$:
$$x^3(x + 2y^2)dx + x^3(xy)dy = 0$$
$$(x^4 + 2x^3y^2)dx + (x^4y)dy = 0$$

Ahora verificamos que sea exacta:
$$\frac{\partial}{\partial y}(x^4 + 2x^3y^2) = 4x^3y$$
$$\frac{\partial}{\partial x}(x^4y) = 4x^3y$$

Como son iguales, la ecuación es exacta.

Buscamos $F(x,y)$ tal que:
$$\frac{\partial F}{\partial x} = x^4 + 2x^3y^2$$
$$\frac{\partial F}{\partial y} = x^4y$$

Integrando la primera ecuación respecto a $x$:
$$F(x,y) = \int (x^4 + 2x^3y^2)dx = \frac{x^5}{5} + \frac{x^4y^2}{2} + g(y)$$

Derivando respecto a $y$:
$$\frac{\partial F}{\partial y} = x^4y + g'(y)$$

Comparando con $\frac{\partial F}{\partial y} = x^4y$, obtenemos $g'(y) = 0$, por lo tanto $g(y) = C$.

**Solución general:** $\frac{x^5}{5} + \frac{x^4y^2}{2} = C$

O equivalentemente: $x^5 + \frac{5x^4y^2}{2} = C$