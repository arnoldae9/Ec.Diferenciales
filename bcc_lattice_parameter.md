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

# Cálculo del Parámetro de Red en Estructura BCC

## Datos del Problema
- **Estructura:** BCC (Body-Centered Cubic)
- **Radio atómico:** $r = 0.126$ nm
- **Encontrar:** Parámetro de red $a$

## Análisis de la Estructura BCC

En una estructura cúbica centrada en el cuerpo (BCC):
- Átomos ubicados en las **8 esquinas** del cubo
- **1 átomo** en el **centro** del cubo
- Los átomos se **tocan** a lo largo de la **diagonal del cuerpo**

## Relación Geométrica

### Diagonal del Cuerpo
La diagonal del cuerpo pasa por:
- La mitad de un átomo en una esquina
- Un átomo completo en el centro
- La mitad de un átomo en la esquina opuesta

Por lo tanto:
$$\text{Diagonal del cuerpo} = 4r$$

### Diagonal del Cubo
Para un cubo con arista $a$, la diagonal del cuerpo es:

$$a^2 + (\sqrt{2}a)^2 = d^2$$

> [!NOTE] La raíz de 2 es por otro teorema de Pitágoras.

$$\text{Diagonal} = a\sqrt{3}$$

## Ecuación Principal

Igualando las dos expresiones para la diagonal:
$$4r = a\sqrt{3}$$

## Despejando el Parámetro de Red

$$a = \frac{4r}{\sqrt{3}}$$

## Sustitución Numérica

$$a = \frac{4 \times 0.126 \text{ nm}}{\sqrt{3}}$$

$$a = \frac{0.504 \text{ nm}}{1.732}$$

$$a = 0.291 \text{ nm}$$

## Resultado

> **El parámetro de red es $a = 0.291$ nm**

## Relación General

Para cualquier estructura BCC:
$$a = \frac{4r}{\sqrt{3}} \approx 2.31r$$

Esta relación muestra que el parámetro de red es aproximadamente 2.31 veces el radio atómico en estructuras BCC.