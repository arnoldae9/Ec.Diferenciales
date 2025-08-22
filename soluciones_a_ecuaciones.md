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

# Ejemplos de Verificación de Soluciones para Ecuaciones Diferenciales

## Instrucciones
Verifique que la solución dada satisface la ecuación diferencial correspondiente.

---

### Ejemplo 1
**Ecuación diferencial:**
$$\frac{dy}{dx} = \frac{2x}{y}$$

**Solución propuesta:**
$$y^2 = x^2 + C$$

---

### Ejemplo 2
**Ecuación diferencial:**
$$\frac{dy}{dt} = \frac{1}{t^2 + 1}$$

**Solución propuesta:**
$$y = \arctan(t) + C$$

---

### Ejemplo 3
**Ecuación diferencial:**
$$\frac{dz}{dx} = 2x\cos(x^2)$$

**Solución propuesta:**
$$z = \sin(x^2) + K$$

---

### Ejemplo 4
**Ecuación diferencial:**
$$\frac{dP}{dt} = \frac{3t^2}{\sqrt{t^3 + 1}}$$

**Solución propuesta:**
$$P = 2\sqrt{t^3 + 1} + A$$

---

### Ejemplo 5
**Ecuación diferencial:**
$$x\frac{dy}{dx} = y + x^2$$

**Solución propuesta:**
$$y = x\ln|x| + Cx$$

---

## Proceso de Verificación
Para verificar cada solución:

1. **Calcular la derivada** de la solución propuesta con respecto a la variable independiente
2. **Sustituir** tanto la función como su derivada en la ecuación diferencial original
3. **Simplificar** para comprobar que ambos lados de la ecuación son iguales
4. **Concluir** si la solución es correcta

### Ejemplo de verificación (para el Ejemplo 2):

Si $y = \arctan(t) + C$, entonces:
- $\frac{dy}{dt} = \frac{1}{t^2 + 1}$
- Sustituyendo en la ecuación: $\frac{1}{t^2 + 1} = \frac{1}{t^2 + 1}$

### Ejemplo de verificación (para el Ejemplo 1):

Si $y^2 = x^2 + C$, entonces derivando implícitamente:

- $2y\frac{dy}{dx} = 2x$

- Por lo tanto: $\frac{dy}{dx} = \frac{x}{y}$

- Pero la ecuación original es $\frac{dy}{dx} = \frac{2x}{y}$

- ¡Esta solución NO es correcta! La solución correcta sería $y^2 = 2x^2 + C$