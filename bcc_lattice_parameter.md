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

## Problema 2: Determinación del tipo de estructura cúbica

**Datos:**
- Densidad: $\rho = 2.6 \text{ g/cm}^3$
- Peso atómico: $M = 87.62 \text{ g/mol}$
- Parámetro de red: $a = 6.0849 \text{ Å} = 6.0849 \times 10^{-8} \text{ cm}$

**Fórmula para la densidad:**

$$\rho = \frac{n \times M}{V \times N_A}$$

Donde:
- $n$ = número de átomos por celda unitaria
- $V$ = volumen de la celda unitaria = $a^3$
- $N_A = 6.022 \times 10^{23} \text{ átomos/mol}$ (número de Avogadro)

**Cálculo del volumen:**

$$V = a^3 = (6.0849 \times 10^{-8})^3 = 2.253 \times 10^{-22} \text{ cm}^3$$

**Despejando n:**

$$n = \frac{\rho \times V \times N_A}{M}$$

$$n = \frac{2.6 \times 2.253 \times 10^{-22} \times 6.022 \times 10^{23}}{87.62} = 4.0$$

**Resultado:** $n \approx 4$ átomos por celda unitaria

Esto corresponde a una **estructura cúbica centrada en las caras (FCC)**.

## Problema 3: Estructura ortorrómbica del Galio

**Datos:**
- $a = 0.45258 \text{ nm} = 4.5258 \times 10^{-8} \text{ cm}$
- $b = 0.45186 \text{ nm} = 4.5186 \times 10^{-8} \text{ cm}$
- $c = 0.76570 \text{ nm} = 7.6570 \times 10^{-8} \text{ cm}$
- Radio atómico: $r = 0.1218 \text{ nm}$
- Densidad: $\rho = 5.904 \text{ g/cm}^3$
- Masa atómica: $M = 69.72 \text{ g/mol}$
- Número de Avogadro: $N_A = 6.022 \times 10^{23}$ 

### a) Número de átomos por celda unitaria

**Volumen de la celda ortorrómbica:**

$$V = a \times b \times c$$

$$V = 4.5258 \times 10^{-8} \times 4.5186 \times 10^{-8} \times 7.6570 \times 10^{-8} = 1.567 \times 10^{-22} \text{ cm}^3$$

**Número de átomos:**

$$n = \frac{\rho \times V \times N_A}{M} = \frac{5.904 \times 1.567 \times 10^{-22} \times 6.022 \times 10^{23}}{69.72} = 8.0$$

**Resultado:** $n = 8$ átomos por celda unitaria

### b) Factor de empaquetamiento

**Volumen ocupado por los átomos:**

$$V_{\text{átomos}} = n \times \frac{4}{3}\pi r^3$$

$$V_{\text{átomos}} = 8 \times \frac{4}{3} \times \pi \times (0.1218 \times 10^{-7})^3$$

$$V_{\text{átomos}} = 8 \times \frac{4}{3} \times \pi \times 1.808 \times 10^{-24} = 6.075 \times 10^{-23} \text{ cm}^3$$

**Factor de empaquetamiento:**

$$FE = \frac{V_{\text{átomos}}}{V_{\text{celda}}} = \frac{6.075 \times 10^{-23}}{1.567 \times 10^{-22}} = 0.388$$

**Resultado:** Factor de empaquetamiento = $0.388$ o $38.8\%$

## Problema 4: Níquel con estructura FCC

**Datos:**
- Estructura: FCC ($n = 4$ átomos/celda)
- $a = 0.352 \text{ nm} = 3.52 \times 10^{-8} \text{ cm}$
- $M = 58.7 \text{ g/mol}$
- $\rho = 8.94 \text{ g/cm}^3$

### Cálculo del número de Avogadro

**Volumen de la celda:**

$$V = a^3 = (3.52 \times 10^{-8})^3 = 4.365 \times 10^{-23} \text{ cm}^3$$

**Despejando $N_A$ de la ecuación de densidad:**

$$N_A = \frac{n \times M}{\rho \times V}$$

$$N_A = \frac{4 \times 58.7}{8.94 \times 4.365 \times 10^{-23}} = 6.01 \times 10^{23} \text{ átomos/mol}$$

**Resultado:** $N_A \approx 6.01 \times 10^{23}$ átomos/mol

### Átomos en 75 g de Níquel

**Número de moles:**

$$n_{\text{moles}} = \frac{75 \text{ g}}{58.7 \text{ g/mol}} = 1.278 \text{ mol}$$

**Número de átomos:**

$$N_{\text{átomos}} = n_{\text{moles}} \times N_A = 1.278 \times 6.022 \times 10^{23} = 7.69 \times 10^{23} \text{ átomos}$$

**Resultado:** $7.69 \times 10^{23}$ átomos

## Problema 5: Cálculo de radios atómicos

### a) Estructura BCC con $a = 0.3294$ nm

En una estructura BCC, los átomos se tocan a lo largo de la diagonal espacial del cubo:

$$4r = a\sqrt{3}$$

**Cálculo:**

$$r = \frac{a\sqrt{3}}{4} = \frac{0.3294 \times 10^{-7} \times \sqrt{3}}{4}$$

$$r = \frac{0.3294 \times 10^{-7} \times 1.732}{4} = 1.427 \times 10^{-8} \text{ cm}$$

**Resultado:** $r = 1.427 \times 10^{-8}$ cm

### b) Estructura FCC con $a = 4.0862$ Å

En una estructura FCC, los átomos se tocan a lo largo de la diagonal de la cara:

$$4r = a\sqrt{2}$$

**Cálculo:**

$$r = \frac{a\sqrt{2}}{4} = \frac{4.0862 \times 10^{-8} \times \sqrt{2}}{4}$$

$$r = \frac{4.0862 \times 10^{-8} \times 1.414}{4} = 1.446 \times 10^{-8} \text{ cm}$$

**Resultado:** $r = 1.446 \times 10^{-8}$ cm

## Ecuaciones:

**Densidad cristalográfica:**
$$\rho = \frac{n \times M}{V \times N_A}$$

**Factor de empaquetamiento:**
$$FE = \frac{V_{\text{átomos ocupados}}}{V_{\text{celda unitaria}}}$$

**Relaciones geométricas:**
- **BCC:** $4r = a\sqrt{3}$ (contacto por diagonal espacial)
- **FCC:** $4r = a\sqrt{2}$ (contacto por diagonal de cara)