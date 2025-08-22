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
 
# Ecuaciones Diferenciales Exactas

## Definición

Una ecuación diferencial de primer orden de la forma:

$$M(x,y)dx + N(x,y)dy = 0$$

se llama **exacta** si existe una función $F(x,y)$ tal que:

$$\frac{\partial F}{\partial x} = M(x,y) \quad \text{y} \quad \frac{\partial F}{\partial y} = N(x,y)$$

En este caso, la función $F(x,y)$ se denomina **función potencial** de la ecuación diferencial.

## Condición de Exactitud

Una ecuación diferencial $M(x,y)dx + N(x,y)dy = 0$ es exacta si y solo si:

$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$

Esta condición se deriva del teorema de Schwarz sobre la igualdad de las derivadas parciales mixtas.

## Método de Solución

### Paso 1: Verificar exactitud
Comprobar que $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$

### Paso 2: Encontrar la función potencial F(x,y)
1. Integrar $M(x,y)$ respecto a $x$:
   $$F(x,y) = \int M(x,y) dx + g(y)$$
   
2. O integrar $N(x,y)$ respecto a $y$:
   $$F(x,y) = \int N(x,y) dy + h(x)$$

### Paso 3: Determinar la función desconocida
- Si usaste el método 1: Derivar $F$ respecto a $y$ e igualar a $N(x,y)$ para encontrar $g'(y)$
- Si usaste el método 2: Derivar $F$ respecto a $x$ e igualar a $M(x,y)$ para encontrar $h'(x)$

### Paso 4: Escribir la solución
La solución general es:
$$F(x,y) = C$$

donde $C$ es una constante arbitraria.

## Ejemplo Resuelto

**Resolver:** $(2xy + 3)dx + (x^2 - 4y)dy = 0$

**Solución:**

1. **Verificar exactitud:**
   - $M(x,y) = 2xy + 3$, entonces $\frac{\partial M}{\partial y} = 2x$
   - $N(x,y) = x^2 - 4y$, entonces $\frac{\partial N}{\partial x} = 2x$
   
   Como $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x} = 2x$, la ecuación es exacta.

2. **Encontrar F(x,y):**
   $$F(x,y) = \int (2xy + 3)dx = x^2y + 3x + g(y)$$

3. **Determinar g(y):**
   $$\frac{\partial F}{\partial y} = x^2 + g'(y) = N(x,y) = x^2 - 4y$$
   
   Por lo tanto: $g'(y) = -4y$, entonces $g(y) = -2y^2$

4. **Solución:**
   $$F(x,y) = x^2y + 3x - 2y^2 = C$$

## Factores Integrantes

Cuando una ecuación no es exacta, a veces se puede multiplicar por un **factor integrante** $\mu(x,y)$ para hacerla exacta.

### Factores integrantes comunes:

1. **Factor que depende solo de x:** Si $\frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N}$ depende solo de $x$, entonces:
   $$\mu(x) = e^{\int \frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N} dx}$$

2. **Factor que depende solo de y:** Si $\frac{\frac{\partial N}{\partial x} - \frac{\partial M}{\partial y}}{M}$ depende solo de $y$, entonces:
   $$\mu(y) = e^{\int \frac{\frac{\partial N}{\partial x} - \frac{\partial M}{\partial y}}{M} dy}$$

## Aplicaciones

Las ecuaciones exactas aparecen frecuentemente en:

- **Física:** Campos conservativos, termodinámica
- **Ingeniería:** Circuitos eléctricos, mecánica de fluidos
- **Economía:** Modelos de equilibrio
- **Geometría:** Campos de direcciones, trayectorias ortogonales

## Notas Importantes

- Una ecuación exacta representa un campo vectorial conservativo
- La solución $F(x,y) = C$ describe las curvas de nivel de la función potencial
- Si una ecuación no es exacta, verificar si existe un factor integrante antes de usar otros métodos
- Las condiciones iniciales determinan el valor específico de la constante $C$

## Relación con Otros Métodos

- **Variables separables:** Caso especial cuando $M$ depende solo de $x$ y $N$ solo de $y$
- **Ecuaciones homogéneas:** Pueden volverse exactas después de una sustitución apropiada
- **Ecuaciones lineales:** A menudo pueden resolverse como exactas o mediante factores integrantes