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


## III Separe las variables y obtenga la solución general de cada Ecuación Diferencial de primer orden. De la solución particular cuando se indiquen condiciones iniciales
a)
$$\dfrac{dM}{dt} = 150 -0.1M \text{ ; } M_{0}=0$$
``pasamos dividiendo``
$$dM = (150 -0.1M) dt$$
Pasamos dividiendo 
$$\dfrac{dM}{(150-0.1M)} = dt$$
Integramos de ambos lados
$$\int{\dfrac{dM}{(150-0.1M)}} = \int{dt}$$
Resolvemos la integral
$$\dfrac{\ln{(150-0.1M)}}{-0.1} + C_1 = t$$
Sustituimos el valor de t y M por las condiciones iniciales, ambos en 0.
$$\dfrac{\ln{(150-0.1(0))}}{-0.1} + C_1 = 0$$
Hacemos un poco de algebra para que sea mas facil de ver
$$C_1 = - \dfrac{\ln{(150)}}{-0.1}$$
$$C_1 = 50.11$$
Sustituimos el valor de 50.11
$$\dfrac{\ln{(150-0.1M)}}{-0.1} + 50.11 = t$$
Opcional: despejamos el valor de M
$$\dfrac{\ln{(150-0.1M)}}{-0.1} = t -50.11$$
$$\ln{(150-0.1M)} = -0.1(t -50.11)$$
$$e^{\ln{(150-0.1M)}} = e^{-0.1(t -50.11)}$$
$$(150-0.1M) = e^{-0.1t + 5.01}$$
$$-0.1M = e^{-0.1t + 5.01}-150$$
$$M = \dfrac{e^{-0.1t + 5.01}-150}{-0.1}$$
---
b)
$$\dfrac{dy}{dx} = e^{3x+2y}$$
Separamos la exponencial
$$\dfrac{dy}{dx} = e^{3x} e^{2y}$$
Intercambiamos el dx con la exponencial que tiene y
$$\dfrac{dy}{e^{2y}} = e^{3x} dx$$
Integramos en ambos lados
$$\int{\dfrac{dy}{e^{2y}}} = \int{e^{3x} dx}$$
Para poder integrar tenemos que cambiar la integral que tiene y a la parte superior de la fraccion
$$\int {e^{-2y}dy} = \int{e^{3x} dx}$$
Integramos, agregando las derivadas en la parte de abajo
$$\dfrac{e^{-2y}}{-2} + C_1 = \dfrac{e^{3x}}{3}$$
Como no tenemos valores iniciales no sustituimos.

Opcional: despejamos y.
$$\dfrac{e^{-2y}}{-2} = \dfrac{e^{3x}}{3} - C_1$$
$$e^{-2y} = -2 \left(\dfrac{e^{3x}}{3} - C_1\right)$$
$$e^{-2y} = - \dfrac{2 e^{3x}}{3} + 2C_1$$
$$C_2 = 2C_1$$
$$e^{-2y} =  \dfrac{-2 e^{3x}}{3} + C_2$$
$$\ln \left({e^{-2y}} \right) = \ln \left({\dfrac{-2 e^{3x}}{3} + C_2}\right)
$$
$$-2y = \ln\left({\dfrac{-2 e^{3x}}{3} + C_2 }\right)$$
$$y = \dfrac{\ln \left({\dfrac{-2 e^{3x}}{3} + C_2} \right)}{-2}$$
$$y = - \dfrac{\ln \left({\dfrac{-2 e^{3x}}{3} + C_2} \right)}{2}$$
---
d)
# Resolución de la Ecuación Diferencial

## Ecuación dada:
$$\csc(y) dx + \sec^2(x) dy = 0$$

## Paso 1: Reorganizar la ecuación

Podemos escribir la ecuación como:
$$\csc(y) dx = -\sec^2(x) dy$$

Separando variables:
$$\frac{dx}{\sec^2(x)} = -\frac{dy}{\csc(y)}$$

## Paso 2: Simplificar las fracciones

Recordemos que:
- $\frac{1}{\sec^2(x)} = \cos^2(x)$
- $\frac{1}{\csc(y)} = \sin(y)$

Por lo tanto:
$$\cos^2(x) dx = -\sin(y) dy$$

## Paso 3: Integrar ambos lados

$$\int \cos^2(x) dx = -\int \sin(y) dy$$

### Para la integral del lado izquierdo:
Usamos la identidad trigonométrica: $\cos^2(x) = \frac{1 + \cos(2x)}{2}$

$$\int \cos^2(x) dx = \int \frac{1 + \cos(2x)}{2} dx = \frac{x}{2} + \frac{\sin(2x)}{4} + C_1$$

### Para la integral del lado derecho:
$$-\int \sin(y) dy = \cos(y) + C_2$$

## Paso 4: Solución general

Combinando los resultados:
$$\frac{x}{2} + \frac{\sin(2x)}{4} = \cos(y) + C$$

donde $C = C_2 - C_1$ es la constante de integración.

## Solución final:

$$\frac{x}{2} + \frac{\sin(2x)}{4} - \cos(y) = C$$

o equivalentemente:

$$\cos(y) = \frac{x}{2} + \frac{\sin(2x)}{4} - C$$

## Verificación

Para verificar, derivamos implícitamente:
$$-\sin(y) \frac{dy}{dx} = \frac{1}{2} + \frac{\cos(2x)}{2}$$

$$\frac{dy}{dx} = -\frac{1 + \cos(2x)}{2\sin(y)} = -\frac{\cos^2(x)}{\sin(y)}$$

Sustituyendo en la ecuación original:
$$\csc(y) + \sec^2(x) \left(-\frac{\cos^2(x)}{\sin(y)}\right) = \frac{1}{\sin(y)} - \frac{1}{\sin(y)} = 0$$ 

## V
a)

Ley de enfriamiento de Newton

$$
\frac{dT}{dt} = -k (T - T_a)
$$

donde:
- $T$ es la temperatura del objeto,
- $t$ es el tiempo,
- $T_a$ es la temperatura ambiente (constante y desconocida),
- $k$ es una constante positiva de proporcionalidad.

Resolvemos esta ecuación diferencial:

Separamos variables:
$$
\frac{dT}{T - T_a} = -k \, dt
$$

Integramos ambos lados:
$$
\int \frac{dT}{T - T_a} = -\int k \, dt
$$
$$
\ln|T - T_a| = -k t + C
$$

Exponenciamos:
$$
T - T_a = e^{-k t + C} = e^C e^{-k t}
$$
Definimos $A = e^C$, entonces:
$$
T(t) = T_a + A e^{-k t}
$$

Ahora, usamos los datos proporcionados:
- En $t = 0$, $T(0) = 78$:
  $$
  78 = T_a + A \quad \Rightarrow \quad A = 78 - T_a
  $$
- En $t = 4$, $T(4) = 71$:
  $$
  71 = T_a + A e^{-4k}
  $$
- En $t = 8$, $T(8) = 65$:
  $$
  65 = T_a + A e^{-8k}
  $$

Sustituimos $A = 78 - T_a$ en las ecuaciones para $t=4$ y $t=8$:

Para $t=4$:
$$
71 = T_a + (78 - T_a) e^{-4k}
$$
$$
71 - T_a = (78 - T_a) e^{-4k} \quad (1)
$$

Para $t=8$:
$$
65 = T_a + (78 - T_a) e^{-8k}
$$
$$
65 - T_a = (78 - T_a) e^{-8k} \quad (2)
$$

Notamos que $e^{-8k} = (e^{-4k})^2$. Entonces, de (1):
$$
e^{-4k} = \frac{71 - T_a}{78 - T_a}
$$

Sustituimos en (2):
$$
65 - T_a = (78 - T_a) \left( \frac{71 - T_a}{78 - T_a} \right)^2
$$
$$
65 - T_a = \frac{(71 - T_a)^2}{78 - T_a}
$$

Multiplicamos ambos lados por $78 - T_a$:
$$
(65 - T_a)(78 - T_a) = (71 - T_a)^2
$$

Expandimos ambos lados:

Lado izquierdo:
$$
(65 - T_a)(78 - T_a) = 65 \cdot 78 - 65 T_a - 78 T_a + T_a^2 = 5070 - 143 T_a + T_a^2
$$

Lado derecho:
$$
(71 - T_a)^2 = 5041 - 142 T_a + T_a^2
$$

Igualamos:
$$
5070 - 143 T_a + T_a^2 = 5041 - 142 T_a + T_a^2
$$

Restamos $T_a^2$ de ambos lados:
$$
5070 - 143 T_a = 5041 - 142 T_a
$$

Pasamos términos:
$$
5070 - 5041 = 143 T_a - 142 T_a
$$
$$
29 = T_a
$$

Por lo tanto, la temperatura de la habitación es $T_a = 29^\circ \text{C}$.

**Verificación:**
Sustituimos $T_a = 29$ en la ecuación (1):
$$
e^{-4k} = \frac{71 - 29}{78 - 29} = \frac{42}{49} = \frac{6}{7}
$$
Luego para $t=8$:
$$
e^{-8k} = (e^{-4k})^2 = \left( \frac{6}{7} \right)^2 = \frac{36}{49}
$$
Entonces:
$$
T(8) = 29 + (78 - 29) \cdot \frac{36}{49} = 29 + 49 \cdot \frac{36}{49} = 29 + 36 = 65
$$
Que coincide con el dato dado.

**Respuesta final:**
$$
\boxed{29}
$$
La temperatura de la habitación es $29^\circ \text{C}$.

b)
# Problema de Crecimiento Poblacional - Sabinas Hidalgo, N.L.

## Planteamiento del Problema

La tasa de crecimiento de una población $P$ con respecto al tiempo $t$ es directamente proporcional a la misma población. La población de Sabinas Hidalgo, N.L. se duplicó en 22 años.

**Determinar:**
- a) ¿En cuánto tiempo se triplicará esta población?
- b) ¿En cuánto tiempo se cuadriplicará?

## Solución

### 1. Formulación de la Ecuación Diferencial

Si la tasa de crecimiento es directamente proporcional a la población, entonces:

$$\frac{dP}{dt} = kP$$

donde $k$ es la constante de proporcionalidad.

### 2. Resolución de la Ecuación Diferencial

Esta es una ecuación diferencial de variables separables:

$$\frac{dP}{P} = k \, dt$$

Integrando ambos lados:

$$\int \frac{dP}{P} = \int k \, dt$$

$$\ln|P| = kt + C$$

Aplicando la función exponencial:

$$P(t) = e^{kt + C} = e^C \cdot e^{kt}$$

Sea $P_0 = e^C$ la población inicial en $t = 0$:

$$P(t) = P_0 e^{kt}$$

### 3. Determinación de la Constante k

Sabemos que la población se duplica en 22 años, es decir:
- En $t = 22$ años: $P(22) = 2P_0$

Sustituyendo en la ecuación:

$$2P_0 = P_0 e^{22k}$$

$$2 = e^{22k}$$

Aplicando logaritmo natural:

$$\ln(2) = 22k$$

$$k = \frac{\ln(2)}{22}$$

### 4. Ecuación Final del Crecimiento

$$P(t) = P_0 e^{\frac{\ln(2)}{22}t}$$

o equivalentemente:

$$P(t) = P_0 \cdot 2^{\frac{t}{22}}$$

### 5. Resolución de los Incisos

#### a) Tiempo para triplicar la población

Para que $P(t) = 3P_0$:

$$3P_0 = P_0 e^{\frac{\ln(2)}{22}t}$$

$$3 = e^{\frac{\ln(2)}{22}t}$$

$$\ln(3) = \frac{\ln(2)}{22}t$$

$$t = \frac{22 \ln(3)}{\ln(2)}$$

Calculando:

$$t = \frac{22 \times 1.0986}{0.6931} = \frac{24.169}{0.6931} \approx 34.87 \text{ años}$$

#### b) Tiempo para cuadriplicar la población

Para que $P(t) = 4P_0$:

$$4P_0 = P_0 e^{\frac{\ln(2)}{22}t}$$

$$4 = e^{\frac{\ln(2)}{22}t}$$

$$\ln(4) = \frac{\ln(2)}{22}t$$

Como $\ln(4) = \ln(2^2) = 2\ln(2)$:

$$2\ln(2) = \frac{\ln(2)}{22}t$$

$$t = \frac{22 \times 2\ln(2)}{\ln(2)} = 44 \text{ años}$$

## Respuestas

- **a) Tiempo para triplicar:** $t \approx 34.87$ años
- **b) Tiempo para cuadriplicar:** $t = 44$ años

## Verificación

Podemos verificar nuestros resultados:

- Para $t = 22$: $P(22) = P_0 \cdot 2^{\frac{22}{22}} = 2P_0$
- Para $t = 34.87$: $P(34.87) = P_0 \cdot 2^{\frac{34.87}{22}} \approx P_0 \cdot 2^{1.585} \approx 3P_0$
- Para $t = 44$: $P(44) = P_0 \cdot 2^{\frac{44}{22}} = P_0 \cdot 2^2 = 4P_0$

## Fórmula General

$$t = \frac{22 \ln(n)}{\ln(2)} = 22 \log_2(n)$$

c)
# Problema de Desintegración Radioactiva - Plomo-209 (Pb-209)

El plomo-209 (Pb-209) es una sustancia radioactiva con vida media de 3.3 horas. Se tiene una muestra inicial de 5 gramos.

**Determinar:**
- a) ¿En cuánto tiempo se desintegrará el 90% del Pb-209 inicial?
- b) ¿Cuánto tiempo habrá que esperar para que solamente quede 1 gramo?

## Solución

### 1. Formulación de la Ecuación Diferencial

Para una sustancia radioactiva, la tasa de desintegración es proporcional a la cantidad presente:

$$\frac{dN}{dt} = -\lambda N$$

donde:
- $N(t)$ = cantidad de sustancia en el tiempo $t$
- $\lambda$ = constante de desintegración (positiva)
- El signo negativo indica que la cantidad disminuye con el tiempo

### 2. Resolución de la Ecuación Diferencial

Esta es una ecuación diferencial de variables separables:

$$\frac{dN}{N} = -\lambda \, dt$$

Integrando ambos lados:

$$\int \frac{dN}{N} = \int -\lambda \, dt$$

$$\ln|N| = -\lambda t + C$$

Aplicando la función exponencial:

$$N(t) = e^{-\lambda t + C} = e^C \cdot e^{-\lambda t}$$

Sea $N_0 = e^C$ la cantidad inicial en $t = 0$:

$$N(t) = N_0 e^{-\lambda t}$$

### 3. Determinación de la Constante $\lambda$

La **vida media** ($t_{1/2}$) es el tiempo necesario para que la cantidad se reduzca a la mitad:

En $t = t_{1/2} = 3.3$ horas: $N(3.3) = \frac{N_0}{2}$

Sustituyendo:

$$\frac{N_0}{2} = N_0 e^{-3.3\lambda}$$

$$\frac{1}{2} = e^{-3.3\lambda}$$

Aplicando logaritmo natural:

$$\ln\left(\frac{1}{2}\right) = -3.3\lambda$$

$$-\ln(2) = -3.3\lambda$$

$$\lambda = \frac{\ln(2)}{3.3}$$

### 4. Ecuación Final de Desintegración

$$N(t) = N_0 e^{-\frac{\ln(2)}{3.3}t}$$

o equivalentemente:

$$N(t) = N_0 \cdot \left(\frac{1}{2}\right)^{\frac{t}{3.3}} = N_0 \cdot 2^{-\frac{t}{3.3}}$$

Con $N_0 = 5$ gramos:

$$N(t) = 5 \cdot 2^{-\frac{t}{3.3}}$$

### 5. Resolución de los Incisos

#### a) Tiempo para que se desintegre el 90% del Pb-209 inicial

Si se desintegra el 90%, entonces queda el 10% de la cantidad inicial:

$$N(t) = 0.1 \times 5 = 0.5 \text{ gramos}$$

Sustituyendo en la ecuación:

$$0.5 = 5 \cdot 2^{-\frac{t}{3.3}}$$

$$0.1 = 2^{-\frac{t}{3.3}}$$

$$\frac{1}{10} = 2^{-\frac{t}{3.3}}$$

Aplicando logaritmo en ambos lados:

$$\ln\left(\frac{1}{10}\right) = -\frac{t}{3.3} \ln(2)$$

$$-\ln(10) = -\frac{t}{3.3} \ln(2)$$

$$t = \frac{3.3 \ln(10)}{\ln(2)}$$

Calculando:

$$t = \frac{3.3 \times 2.3026}{0.6931} = \frac{7.599}{0.6931} \approx 10.96 \text{ horas}$$

#### b) Tiempo para que quede solamente 1 gramo

Para que $N(t) = 1$ gramo:

$$1 = 5 \cdot 2^{-\frac{t}{3.3}}$$

$$\frac{1}{5} = 2^{-\frac{t}{3.3}}$$

$$0.2 = 2^{-\frac{t}{3.3}}$$

Aplicando logaritmo:

$$\ln(0.2) = -\frac{t}{3.3} \ln(2)$$

$$\ln\left(\frac{1}{5}\right) = -\frac{t}{3.3} \ln(2)$$

$$-\ln(5) = -\frac{t}{3.3} \ln(2)$$

$$t = \frac{3.3 \ln(5)}{\ln(2)}$$

Calculando:

$$t = \frac{3.3 \times 1.6094}{0.6931} = \frac{5.311}{0.6931} \approx 7.66 \text{ horas}$$

## Respuestas

- **a) Tiempo para desintegrar el 90%:** $t \approx 10.96$ horas
- **b) Tiempo para que quede 1 gramo:** $t \approx 7.66$ horas

## Verificación

Podemos verificar nuestros resultados:

- Para $t = 3.3$ horas: $N(3.3) = 5 \cdot 2^{-\frac{3.3}{3.3}} = 5 \cdot 2^{-1} = 2.5$ gramos
- Para $t = 7.66$ horas: $N(7.66) = 5 \cdot 2^{-\frac{7.66}{3.3}} \approx 5 \cdot 2^{-2.32} \approx 1$ gramo
- Para $t = 10.96$ horas: $N(10.96) = 5 \cdot 2^{-\frac{10.96}{3.3}} \approx 5 \cdot 2^{-3.32} \approx 0.5$ gramos

## Fórmula General

Para encontrar el tiempo necesario para que quede una fracción $f$ de la cantidad inicial:

$$t = \frac{3.3 \ln\left(\frac{1}{f}\right)}{\ln(2)} = 3.3 \log_2\left(\frac{1}{f}\right)$$

donde $f = \frac{N(t)}{N_0}$

## Tabla de Desintegración

| Tiempo (horas) | Cantidad restante (gramos) | Porcentaje restante |
|----------------|---------------------------|-------------------|
| 0              | 5.00                      | 100%             |
| 3.3            | 2.50                      | 50%              |
| 6.6            | 1.25                      | 25%              |
| 7.66           | 1.00                      | 20%              |
| 9.9            | 0.625                     | 12.5%            |
| 10.96          | 0.50                      | 10%              |
| 13.2           | 0.3125                    | 6.25%            |

## Observaciones

1. **Patrón exponencial:** La desintegración radioactiva sigue una ley exponencial decreciente.

2. **Vida media constante:** Cada 3.3 horas, la cantidad se reduce a la mitad, independientemente de la cantidad inicial.

3. **Nunca llega a cero:** Teóricamente, siempre quedará una pequeña cantidad de la sustancia, aunque sea negligible en términos prácticos.