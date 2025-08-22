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
 
# Introducción a Ecuaciones Diferenciales

## ¿Qué es una Ecuación Diferencial?

Una **ecuación diferencial** es una ecuación que contiene una función desconocida (variable dependiente) y una o más de sus derivadas. Estas ecuaciones relacionan una función con sus derivadas y describen cómo cambia una cantidad con respecto a otra.

**Forma general:**
$$F(x, y, y', y'', ..., y^{(n)}) = 0$$

Donde:

- $x$ es la variable independiente
- $y$ es la variable dependiente (función desconocida)
- $y', y'', ..., y^{(n)}$ son las derivadas de $y$ respecto a $x$

## Clasificación de Ecuaciones Diferenciales

### Por el Orden
El **orden** de una ecuación diferencial es el orden de la derivada mayor que aparece en la ecuación.

**Ejemplos:**

- **Primer orden:** $\frac{dy}{dx} + 2y = x^2$
- **Segundo orden:** $\frac{d^2y}{dx^2} + 3\frac{dy}{dx} + 2y = 0$
- **n-ésimo orden:** $y^{(n)} + a_{n-1}y^{(n-1)} + ... + a_1y' + a_0y = f(x)$

### Por el Grado
El **grado** es la potencia de la derivada de mayor orden cuando la ecuación está en forma polinomial.

**Ejemplo:**

- Grado 1: $y'' + 3y' + 2y = 0$
- Grado 2: $(y')^2 + y = x$

### Por la Linealidad

#### Ecuaciones Lineales
Una ecuación diferencial es **lineal** si puede escribirse como:
$$a_n(x)y^{(n)} + a_{n-1}(x)y^{(n-1)} + ... + a_1(x)y' + a_0(x)y = f(x)$$

**Características:**

- La variable dependiente $y$ y todas sus derivadas aparecen elevadas a la primera potencia
- No hay productos entre $y$ y sus derivadas
- Los coeficientes dependen solo de la variable independiente $x$

#### Ecuaciones No Lineales
Cualquier ecuación que no cumpla las condiciones de linealidad.

**Ejemplos:**

- $y \cdot y' + x = 0$ (producto de $y$ y $y'$)
- $(y')^2 + y = x$ (derivada al cuadrado)

### Por el Número de Variables

#### Ecuaciones Diferenciales Ordinarias (EDO)
Contienen derivadas de una función respecto a **una sola variable independiente**.

**Ejemplo:** $\frac{d^2y}{dx^2} + 2\frac{dy}{dx} + y = e^x$

#### Ecuaciones Diferenciales Parciales (EDP)
Contienen derivadas parciales de una función respecto a **dos o más variables independientes**.

**Ejemplo:** $\frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} = 0$ (Ecuación de Laplace)

## Soluciones de Ecuaciones Diferenciales

### Solución General
Es una familia de funciones que contiene constantes arbitrarias (tantas como el orden de la ecuación) y satisface la ecuación diferencial.

**Para una EDO de orden n:** $y = f(x, c_1, c_2, ..., c_n)$

### Solución Particular
Se obtiene al asignar valores específicos a las constantes arbitrarias de la solución general, generalmente mediante condiciones iniciales o de frontera.

### Solución Singular
Es una solución que no puede obtenerse de la solución general para ningún valor de las constantes arbitrarias.

## Condiciones Iniciales y de Frontera

### Condiciones Iniciales
Especifican los valores de la función y sus derivadas en un punto particular.

**Para una EDO de segundo orden:**

- $y(x_0) = y_0$
- $y'(x_0) = y_1$

### Condiciones de Frontera
Especifican los valores de la función (y posiblemente sus derivadas) en dos o más puntos diferentes.

**Ejemplo:** $y(a) = \alpha$ y $y(b) = \beta$

## Ejemplos Básicos

### Ejemplo 1: EDO de Primer Orden Lineal
$$\frac{dy}{dx} + 2y = 6$$

**Solución general:** $y = 3 + Ce^{-2x}$

Con condición inicial $y(0) = 5$:
**Solución particular:** $y = 3 + 2e^{-2x}$

### Ejemplo 2: EDO de Segundo Orden Homogénea
$$\frac{d^2y}{dx^2} - 5\frac{dy}{dx} + 6y = 0$$

**Ecuación característica:** $r^2 - 5r + 6 = 0$
**Raíces:** $r_1 = 2, r_2 = 3$
**Solución general:** $y = C_1e^{2x} + C_2e^{3x}$

## Métodos de Solución Básicos

1. **Separación de variables** (para EDO de primer orden)
2. **Factor integrante** (para EDO lineales de primer orden)
3. **Ecuaciones homogéneas** (sustitución apropiada)
4. **Ecuaciones exactas** (verificación de condición de exactitud)
5. **Método de coeficientes indeterminados** (para EDO lineales no homogéneas)
6. **Variación de parámetros** (método general para EDO no homogéneas)

## Puntos Clave para Recordar

- El orden determina el número de constantes arbitrarias en la solución general
- Las condiciones iniciales/frontera permiten encontrar soluciones particulares
- La linealidad facilita significativamente los métodos de solución
- Las EDO son más simples de resolver que las EDP
- La verificación de la solución siempre debe realizarse sustituyendo en la ecuación original