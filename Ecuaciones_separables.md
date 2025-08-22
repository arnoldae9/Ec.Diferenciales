---
title: "Ecuaciones Diferenciales"
subtitle: "Variables Separables"
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: "Ecuaciones Diferenciales"
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
  - \fancyhead[L]{Ecuaciones Diferenciales}
  - \fancyhead[R]{2° Año}
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
 
# Método de Variables Separables

## Definición

El **método de variables separables** es una técnica para resolver ecuaciones diferenciales ordinarias de primer orden donde es posible separar las variables dependiente e independiente en lados opuestos de la ecuación.

## Forma General

Una ecuación diferencial es **separable** si puede escribirse en la forma:

$$\frac{dy}{dx} = f(x) \cdot g(y)$$

O equivalentemente:
$$M(x)dx + N(y)dy = 0$$

Donde $M(x)$ depende solo de $x$ y $N(y)$ depende solo de $y$.

## Procedimiento de Solución

### Paso 1: Verificar que la ecuación es separable
La ecuación debe poder expresarse como producto de una función de $x$ por una función de $y$.

### Paso 2: Separar las variables
Reorganizar la ecuación para que todas las expresiones con $y$ estén en un lado y todas las expresiones con $x$ en el otro:

$$\frac{dy}{g(y)} = f(x)dx$$

### Paso 3: Integrar ambos lados
$$\int \frac{dy}{g(y)} = \int f(x)dx + C$$

### Paso 4: Resolver para y (si es posible)
Despejar $y$ de la ecuación resultante para obtener la solución general.

## Ejemplos Resueltos

### Ejemplo 1: Ecuación Básica
**Ecuación:** $\frac{dy}{dx} = 3x^2y$

**Paso 1:** Verificar separabilidad
$\frac{dy}{dx} = 3x^2 \cdot y$ (producto de función de $x$ por función de $y$)

**Paso 2:** Separar variables
$$\frac{dy}{y} = 3x^2 dx$$

**Paso 3:** Integrar
$$\int \frac{dy}{y} = \int 3x^2 dx$$
$$\ln|y| = x^3 + C_1$$

**Paso 4:** Resolver para $y$
$$|y| = e^{x^3 + C_1} = e^{C_1} \cdot e^{x^3}$$
$$y = Ce^{x^3}$$ (donde $C = \pm e^{C_1}$)

**Solución general:** $y = Ce^{x^3}$

### Ejemplo 2: Con Condición Inicial
**Ecuación:** $\frac{dy}{dx} = \frac{2x}{y^2}$, con $y(1) = 2$

**Paso 1:** Separar variables
$$y^2 dy = 2x dx$$

**Paso 2:** Integrar
$$\int y^2 dy = \int 2x dx$$
$$\frac{y^3}{3} = x^2 + C$$

**Paso 3:** Aplicar condición inicial $y(1) = 2$
$$\frac{(2)^3}{3} = (1)^2 + C$$
$$\frac{8}{3} = 1 + C$$
$$C = \frac{8}{3} - 1 = \frac{5}{3}$$

**Solución particular:** $\frac{y^3}{3} = x^2 + \frac{5}{3}$

O despejando: $y^3 = 3x^2 + 5$, entonces $y = \sqrt[3]{3x^2 + 5}$

### Ejemplo 3: Ecuación de Crecimiento Poblacional
**Ecuación:** $\frac{dP}{dt} = kP$ (donde $k$ es una constante)

**Separar variables:**
$$\frac{dP}{P} = k dt$$

**Integrar:**
$$\int \frac{dP}{P} = \int k dt$$
$$\ln|P| = kt + C_1$$

**Resolver para P:**
$$P = Ce^{kt}$$ (donde $C = e^{C_1}$)

**Con condición inicial** $P(0) = P_0$:
$$P_0 = Ce^{k \cdot 0} = C$$

**Solución particular:** $P(t) = P_0 e^{kt}$

### Ejemplo 4: Ecuación Logística
**Ecuación:** $\frac{dP}{dt} = rP(1 - \frac{P}{K})$ (crecimiento logístico)

**Reescribir:**
$$\frac{dP}{dt} = \frac{rP(K-P)}{K}$$

**Separar variables:**
$$\frac{K \, dP}{P(K-P)} = r \, dt$$

**Usar fracciones parciales:**
$$\frac{K}{P(K-P)} = \frac{1}{P} + \frac{1}{K-P}$$

**Integrar:**
$$\int \left(\frac{1}{P} + \frac{1}{K-P}\right) dP = \int r \, dt$$
$$\ln|P| - \ln|K-P| = rt + C_1$$
$$\ln\left|\frac{P}{K-P}\right| = rt + C_1$$

**Resolver:**
$$\frac{P}{K-P} = Ce^{rt}$$

Despejando $P$:
$$P = \frac{CKe^{rt}}{1 + Ce^{rt}}$$

## Casos Especiales y Consideraciones

### Caso 1: Cuando $g(y) = 0$
Si $g(y_0) = 0$ para algún valor $y_0$, entonces $y = y_0$ es una **solución singular** (equilibrio).

**Ejemplo:** En $\frac{dy}{dx} = y^2 - 4$, si $y^2 - 4 = 0$, entonces $y = 2$ y $y = -2$ son soluciones de equilibrio.

### Caso 2: Pérdida de Soluciones
Al dividir por $g(y)$, podemos perder soluciones donde $g(y) = 0$. Siempre verificar estos casos por separado.

### Caso 3: Integración con Valor Absoluto
Cuando aparece $\ln|y|$, considerar tanto valores positivos como negativos de $y$ en la solución general.

## Aplicaciones en Ingeniería

### 1. Circuitos RC
**Ecuación:** $RC\frac{dV}{dt} + V = 0$ (descarga del capacitor)

**Separar:** $\frac{dV}{V} = -\frac{dt}{RC}$

**Solución:** $V(t) = V_0 e^{-t/RC}$

### 2. Ley de Enfriamiento de Newton
**Ecuación:** $\frac{dT}{dt} = -k(T - T_a)$ (donde $T_a$ es temperatura ambiente)

**Separar:** $\frac{dT}{T - T_a} = -k \, dt$

**Solución:** $T(t) = T_a + (T_0 - T_a)e^{-kt}$

### 3. Decaimiento Radiactivo
**Ecuación:** $\frac{dN}{dt} = -\lambda N$

**Solución:** $N(t) = N_0 e^{-\lambda t}$

### 4. Vaciado de Tanques (Ley de Torricelli)
**Ecuación:** $\frac{dh}{dt} = -k\sqrt{h}$ (donde $h$ es la altura del líquido)

**Separar:** $\frac{dh}{\sqrt{h}} = -k \, dt$

**Integrar:** $2\sqrt{h} = -kt + C$

**Solución:** $h(t) = \left(\frac{C - kt}{2}\right)^2$

## Verificación de Soluciones

Siempre verificar la solución sustituyendo en la ecuación diferencial original:

**Ejemplo:** Si $y = Ce^{x^3}$ es solución de $\frac{dy}{dx} = 3x^2y$

$$\frac{dy}{dx} = \frac{d}{dx}(Ce^{x^3}) = C \cdot 3x^2 e^{x^3} = 3x^2(Ce^{x^3}) = 3x^2y$$ 

## Limitaciones del Método

1. **No todas las EDO son separables:** $\frac{dy}{dx} = x + y$ no es separable
2. **Integración compleja:** Algunas integrales pueden no tener forma cerrada
3. **Soluciones implícitas:** No siempre es posible despejar $y$ explícitamente
4. **Pérdida de soluciones:** Al dividir por funciones que pueden ser cero

## Ejemplos Adicionales Resueltos

### Ejemplo 5: Ecuación con Funciones Trigonométricas
**Ecuación:** $\frac{dy}{dx} = y \cos x$

**Solución:**

- **Separar variables:** $\frac{dy}{y} = \cos x \, dx$
- **Integrar:** $\int \frac{dy}{y} = \int \cos x \, dx$
- **Resultado:** $\ln|y| = \sin x + C_1$
- **Solución general:** $y = Ce^{\sin x}$

**Con condición inicial** $y(0) = 3$:
$3 = Ce^{\sin 0} = Ce^0 = C$
**Solución particular:** $y = 3e^{\sin x}$

### Ejemplo 6: Ecuación con Raíces
**Ecuación:** $\frac{dy}{dx} = \frac{\sqrt{1-y^2}}{x}$, para $x > 0$

**Solución:**

- **Separar variables:** $\frac{dy}{\sqrt{1-y^2}} = \frac{dx}{x}$
- **Integrar:** $\int \frac{dy}{\sqrt{1-y^2}} = \int \frac{dx}{x}$
- **Resultado:** $\arcsin(y) = \ln|x| + C$
- **Solución general:** $y = \sin(\ln|x| + C)$

### Ejemplo 7: Ecuación con Productos de Funciones
**Ecuación:** $\frac{dy}{dx} = xy(1+x^2)$

**Solución:**

- **Separar variables:** $\frac{dy}{y} = x(1+x^2) dx$
- **Expandir:** $\frac{dy}{y} = (x + x^3) dx$
- **Integrar:** $\int \frac{dy}{y} = \int (x + x^3) dx$
- **Resultado:** $\ln|y| = \frac{x^2}{2} + \frac{x^4}{4} + C_1$
- **Solución general:** $y = Ce^{\frac{x^2}{2} + \frac{x^4}{4}}$

### Ejemplo 8: Ecuación que Requiere Factorización
**Ecuación:** $\frac{dy}{dx} = \frac{y^2 - 4}{x^2}$

**Solución:**

- **Factorizar:** $\frac{dy}{dx} = \frac{(y-2)(y+2)}{x^2}$
- **Separar variables:** $\frac{dy}{(y-2)(y+2)} = \frac{dx}{x^2}$
- **Fracciones parciales:** $\frac{1}{(y-2)(y+2)} = \frac{A}{y-2} + \frac{B}{y+2}$

Resolviendo: $1 = A(y+2) + B(y-2)$

- Si $y = 2$: $1 = 4A \Rightarrow A = \frac{1}{4}$
- Si $y = -2$: $1 = -4B \Rightarrow B = -\frac{1}{4}$

- **Integrar:** $\int \left(\frac{1/4}{y-2} - \frac{1/4}{y+2}\right) dy = \int \frac{dx}{x^2}$
- **Resultado:** $\frac{1}{4}\ln\left|\frac{y-2}{y+2}\right| = -\frac{1}{x} + C_1$
- **Solución implícita:** $\ln\left|\frac{y-2}{y+2}\right| = -\frac{4}{x} + C$

### Ejemplo 9: Problema de Mezclas
**Situación:** Un tanque contiene 100 L de agua pura. Se bombea salmuera con 2 kg/L de sal a razón de 3 L/min, y la mezcla sale a la misma velocidad.

**Ecuación:** $\frac{dS}{dt} = 6 - \frac{3S}{100}$ (donde $S$ es la cantidad de sal en kg)

**Solución:**

- **Reescribir:** $\frac{dS}{dt} = \frac{600 - 3S}{100}$
- **Separar variables:** $\frac{dS}{600 - 3S} = \frac{dt}{100}$
- **Integrar:** $\int \frac{dS}{600 - 3S} = \int \frac{dt}{100}$
- **Resultado:** $-\frac{1}{3}\ln|600 - 3S| = \frac{t}{100} + C_1$
- **Simplificar:** $\ln|600 - 3S| = -\frac{3t}{100} + C$
- **Solución general:** $600 - 3S = Ae^{-3t/100}$
- **Despejar S:** $S = 200 - \frac{A}{3}e^{-3t/100}$

**Con condición inicial** $S(0) = 0$:
$0 = 200 - \frac{A}{3} \Rightarrow A = 600$

**Solución particular:** $S(t) = 200(1 - e^{-3t/100})$

### Ejemplo 10: Ecuación de Bernoulli Reducible
**Ecuación:** $\frac{dy}{dx} + xy = xy^3$

**Transformación:** Esta es una ecuación de Bernoulli. Dividiendo por $y^3$:
$y^{-3}\frac{dy}{dx} + xy^{-2} = x$

**Sustitución:** $v = y^{-2}$, entonces $\frac{dv}{dx} = -2y^{-3}\frac{dy}{dx}$

**Nueva ecuación:** $-\frac{1}{2}\frac{dv}{dx} + xv = x$

**Multiplicar por -2:** $\frac{dv}{dx} - 2xv = -2x$

**Esta es lineal en v, pero también separable:**
$\frac{dv}{dx} = 2xv - 2x = 2x(v - 1)$

**Separar variables:** $\frac{dv}{v-1} = 2x \, dx$

**Integrar:** $\ln|v-1| = x^2 + C_1$

**Solución para v:** $v = 1 + Ce^{x^2}$

**Regresar a y:** $y^{-2} = 1 + Ce^{x^2}$

**Solución final:** $y = \pm\frac{1}{\sqrt{1 + Ce^{x^2}}}$

### Ejemplo 11: Trayectorias Ortogonales
**Problema:** Encontrar las trayectorias ortogonales a la familia de curvas $y = Cx^2$.

**Solución:**

- **Familia dada:** $y = Cx^2$
- **Derivar:** $\frac{dy}{dx} = 2Cx = \frac{2y}{x}$ (eliminando $C$)
- **Trayectorias ortogonales:** $\frac{dy}{dx} = -\frac{x}{2y}$ (pendiente recíproca negativa)
- **Separar variables:** $2y \, dy = -x \, dx$
- **Integrar:** $\int 2y \, dy = \int -x \, dx$
- **Resultado:** $y^2 = -\frac{x^2}{2} + C$
- **Trayectorias ortogonales:** $x^2 + 2y^2 = K$ (familia de elipses)

### Ejemplo 12: Problema de Velocidad Terminal
**Situación:** Un objeto cae con resistencia del aire proporcional al cuadrado de la velocidad.

**Ecuación:** $m\frac{dv}{dt} = mg - kv^2$ (donde $k > 0$)

**Solución:**

- **Reescribir:** $\frac{dv}{dt} = g - \frac{k}{m}v^2 = g\left(1 - \frac{kv^2}{mg}\right)$
- **Definir:** $v_t = \sqrt{\frac{mg}{k}}$ (velocidad terminal)
- **Ecuación:** $\frac{dv}{dt} = g\left(1 - \frac{v^2}{v_t^2}\right) = \frac{g}{v_t^2}(v_t^2 - v^2)$
- **Separar variables:** $\frac{dv}{v_t^2 - v^2} = \frac{g}{v_t^2} dt$
- **Fracciones parciales:** $\frac{1}{v_t^2 - v^2} = \frac{1}{(v_t-v)(v_t+v)} = \frac{1}{2v_t}\left(\frac{1}{v_t-v} + \frac{1}{v_t+v}\right)$
- **Integrar:** $\frac{1}{2v_t}\ln\left|\frac{v_t+v}{v_t-v}\right| = \frac{g}{v_t^2}t + C$

**Con condición inicial** $v(0) = 0$:
$C = 0$

**Solución implícita:** $\ln\left|\frac{v_t+v}{v_t-v}\right| = \frac{2gt}{v_t}$

**Solución explícita:** $v(t) = v_t \tanh\left(\frac{gt}{v_t}\right)$

## Resumen del Proceso

1. **Identificar** si la ecuación es separable: $\frac{dy}{dx} = f(x)g(y)$
2. **Separar** las variables: $\frac{dy}{g(y)} = f(x)dx$
3. **Integrar** ambos lados: $\int \frac{dy}{g(y)} = \int f(x)dx + C$
4. **Resolver** para $y$ (si es posible)
5. **Aplicar** condiciones iniciales si se proporcionan
6. **Verificar** la solución en la ecuación original
7. **Considerar** soluciones singulares donde $g(y) = 0$