---
title: Problemario SOLE
subtitle: Problemario SOLE
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: Ec. Diferenciales
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
  - \fancyhead[L]{Problemario SOLE - Problemario SOLE}
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


# Soluciones del Problemario - Ecuaciones Diferenciales

## Fase 1. Ecuaciones Diferenciales de primer orden.

### I. Determine el orden, grado y linealidad de las siguientes Ecuaciones Diferenciales Ordinarias.

1. $$ y'e^x - y''x^2 + \frac{yy'}{x^3 + 1} = (y')^3 \sin(x) $$
   *   **Orden:** 2 (La derivada de mayor orden es $y''$).
   *   **Grado:** 1 (La potencia de la derivada de mayor orden, $y''$, es 1).
   *   **Linealidad:** No lineal (debido a los términos $yy'$ y $(y')^3$).

2. $$ (2y''')^2x^3 - \frac{2y'}{x+2} = (y')^4 e^x $$
   *   **Orden:** 3 (La derivada de mayor orden es $y'''$).
   *   **Grado:** 2 (La potencia de la derivada de mayor orden, $y'''$, es 2).
   *   **Linealidad:** No lineal (debido a los términos $(2y''')^2$ y $(y')^4$).

3. $$ \frac{dy}{dx} = 2\sin(4xy) + (\frac{d^2y}{dx^2})^3 $$
   *   **Orden:** 2 (La derivada de mayor orden es $\frac{d^2y}{dx^2}$).
   *   **Grado:** 3 (La potencia de la derivada de mayor orden es 3).
   *   **Linealidad:** No lineal (debido al término $\sin(4xy)$ y la potencia de la derivada).

4. $$ xy' + 9xy'' + 3xy''' = y^{IV} $$
   *   **Orden:** 4 (La derivada de mayor orden es $y^{IV}$).
   *   **Grado:** 1 (La potencia de la derivada de mayor orden es 1).
   *   **Linealidad:** Lineal.

### II. Verifique que la solución que se da satisface la Ecuación Diferencial indicada.

a) **ED:** $y'' + 9y = 18$, **SOL:** $y = 2$
   Derivamos la solución: $y' = 0$, $y'' = 0$.
   Sustituimos en la ED: $0 + 9(2) = 18 \implies 18 = 18$.
   La solución satisface la ecuación.

b) **ED:** $\frac{dP}{dt} = P(1 - P)$, **SOL:** $P = \frac{C_1e^t}{1 + C_1e^t}$
   Derivamos la solución usando la regla del cociente:
   $$ \frac{dP}{dt} = \frac{C_1e^t(1 + C_1e^t) - C_1e^t(C_1e^t)}{(1 + C_1e^t)^2} = \frac{C_1e^t}{(1 + C_1e^t)^2} $$
   Sustituimos en el lado derecho de la ED:
   $$ P(1-P) = \frac{C_1e^t}{1 + C_1e^t} \left(1 - \frac{C_1e^t}{1 + C_1e^t}\right) = \frac{C_1e^t}{1 + C_1e^t} \left(\frac{1}{1 + C_1e^t}\right) = \frac{C_1e^t}{(1 + C_1e^t)^2} $$
   Ambos lados son iguales, por lo que la solución es correcta.

c) **ED:** $\frac{d^2y}{dx^2} - 4\frac{dy}{dx} + 4y = 0$, **SOL:** $y = C_1e^{2x} + C_2xe^{2x}$
   Derivamos:
   $y' = 2C_1e^{2x} + C_2e^{2x} + 2C_2xe^{2x}$
   $y'' = 4C_1e^{2x} + 2C_2e^{2x} + 2C_2e^{2x} + 4C_2xe^{2x} = 4C_1e^{2x} + 4C_2e^{2x} + 4C_2xe^{2x}$
   Sustituimos en la ED:
   $$(4C_1e^{2x} + 4C_2e^{2x} + 4C_2xe^{2x}) - 4(2C_1e^{2x} + C_2e^{2x} + 2C_2xe^{2x}) + 4(C_1e^{2x} + C_2xe^{2x})$$
   $$= (4-8+4)C_1e^{2x} + (4-4)C_2e^{2x} + (4-8+4)C_2xe^{2x} = 0$$
   La solución satisface la ecuación.

d) **ED:** $x^3y''' + 2x^2y'' - xy' + y = 12x^2$, **SOL:** $y = C_1x^{-1} + C_2x + C_3x\ln x + 4x^2$
   Derivamos:
   $y' = -C_1x^{-2} + C_2 + C_3(\ln x + 1) + 8x$
   $y'' = 2C_1x^{-3} + C_3x^{-1} + 8$
   $y''' = -6C_1x^{-4} - C_3x^{-2}$
   Sustituyendo y agrupando términos se comprueba que la igualdad se cumple.
   La solución es correcta.

### III. Separe las variables y obtenga la solución.

a) $\frac{dM}{dt} = 150 - 0.1M$, con $M(0) = 0$
   $$ \frac{dM}{150 - 0.1M} = dt \implies \int \frac{dM}{1500 - M} = \int 0.1 dt $$
   $$ -\ln|1500 - M| = 0.1t + C \implies 1500 - M = Ae^{-0.1t} $$
   $$ M(t) = 1500 - Ae^{-0.1t} $$
   Usando $M(0)=0$: $0 = 1500 - A \implies A = 1500$.
   **Solución particular:** $M(t) = 1500(1 - e^{-0.1t})$

b) $\frac{dy}{dx} = e^{3x+2y}$
   $$ \frac{dy}{dx} = e^{3x}e^{2y} \implies e^{-2y}dy = e^{3x}dx $$
   $$ \int e^{-2y}dy = \int e^{3x}dx \implies -\frac{1}{2}e^{-2y} = \frac{1}{3}e^{3x} + C $$
   **Solución general:** $-\frac{1}{2}e^{-2y} - \frac{1}{3}e^{3x} = C$

c) $y\ln x \frac{dx}{dy} = (\frac{y+1}{x})^2$
   $$ x^2 \ln x dx = \frac{(y+1)^2}{y} dy = (y + 2 + \frac{1}{y}) dy $$
   Integrando ambos lados (la integral de $x^2 \ln x$ se hace por partes):
   $$ \frac{x^3}{3}\ln x - \frac{x^3}{9} = \frac{y^2}{2} + 2y + \ln|y| + C $$

d) $\csc(y)dx + \sec^2(x)dy = 0$
   $$ \frac{dx}{\sec^2(x)} = -\frac{dy}{\csc(y)} \implies \int \cos^2(x)dx = -\int \sin(y)dy $$
   $$ \int \frac{1+\cos(2x)}{2} dx = \cos(y) + C $$
   $$ \frac{x}{2} + \frac{\sin(2x)}{4} = \cos(y) + C $$

### IV. Identifique y resuelva la ED.

a) $xdy - ydx = \sqrt{x^2 + y^2}(xdx + ydy)$
   Usando coordenadas polares $x=r\cos\theta, y=r\sin\theta$, donde $xdy-ydx = r^2d\theta$ y $xdx+ydy=rdr$.
   $$ r^2 d\theta = r(rdr) \implies d\theta = dr $$
   Integrando: $\theta = r + C$.
   **Solución:** $\arctan(\frac{y}{x}) = \sqrt{x^2+y^2} + C$

b) $2xy dx + (x^2 - 1)dy = 0$
   $M=2xy, N=x^2-1$. $\frac{\partial M}{\partial y} = 2x$, $\frac{\partial N}{\partial x} = 2x$. Es exacta.
   $f = \int 2xy dx = x^2y + g(y)$.
   $\frac{\partial f}{\partial y} = x^2 + g'(y) = x^2 - 1 \implies g'(y) = -1 \implies g(y) = -y$.
   **Solución:** $x^2y - y = C$

c) $\frac{dy}{dx} = \frac{xy^2-\cos x \sin x}{y(1-x^2)}$, con $y(0) = 2$
   $(\cos x \sin x - xy^2)dx + y(1-x^2)dy = 0$. Es exacta.
   $f = \int y(1-x^2)dy = \frac{y^2}{2}(1-x^2) + h(x)$.
   $\frac{\partial f}{\partial x} = -xy^2 + h'(x) = \cos x \sin x - xy^2 \implies h'(x) = \frac{1}{2}\sin(2x) \implies h(x) = -\frac{1}{4}\cos(2x)$.
   Solución general: $\frac{y^2}{2}(1-x^2) - \frac{1}{4}\cos(2x) = C$.
   Para $y(0)=2$: $\frac{4}{2}(1) - \frac{1}{4}(1) = C \implies C = 2 - 1/4 = 7/4$.
   **Solución implícita:** $2y^2(1-x^2) - \cos(2x) = 7$.

d) $\sin y dx + (x \cos y - 2y)dy = 0$
   $M=\sin y, N=x\cos y - 2y$. $\frac{\partial M}{\partial y} = \cos y$, $\frac{\partial N}{\partial x} = \cos y$. Es exacta.
   $f = \int \sin y dx = x\sin y + g(y)$.
   $\frac{\partial f}{\partial y} = x\cos y + g'(y) = x\cos y - 2y \implies g'(y) = -2y \implies g(y) = -y^2$.
   **Solución:** $x\sin y - y^2 = C$.

e) $(10 - 6y + e^{-3x})dx - 2dy = 0$
   No es exacta. Factor integrante $\mu(x) = e^{\int \frac{M_y - N_x}{N} dx} = e^{\int \frac{-6-0}{-2} dx} = e^{3x}$.
   Multiplicando: $(10e^{3x} - 6ye^{3x} + 1)dx - 2e^{3x}dy = 0$. Ahora es exacta.
   $f = \int -2e^{3x}dy = -2ye^{3x} + h(x)$.
   $\frac{\partial f}{\partial x} = -6ye^{3x} + h'(x) = 10e^{3x} - 6ye^{3x} + 1 \implies h'(x) = 10e^{3x} + 1 \implies h(x) = \frac{10}{3}e^{3x} + x$.
   **Solución:** $-2ye^{3x} + \frac{10}{3}e^{3x} + x = C$.

### V. Aplicaciones

a) **Enfriamiento de café:** Ley de Enfriamiento de Newton $\frac{dT}{dt} = k(T - T_a)$.
   Con $T(0)=78, T(4)=71, T(8)=65$.
   La solución es $T(t) = T_a + Ce^{kt}$.
   Resolviendo el sistema de ecuaciones:
   $78 = T_a + C$
   $71 = T_a + Ce^{4k}$
   $65 = T_a + Ce^{8k}$
   Se obtiene que la temperatura de la habitación es **$T_a = 29^\circ C$**.

b) **Crecimiento poblacional:** $\frac{dP}{dt} = kP$.
   $P(22) = 2P_0 \implies 2 = e^{22k} \implies k = \frac{\ln 2}{22}$.
   a) Tiempo para triplicar: $3 = e^{kt} \implies t = \frac{\ln 3}{k} = 22\frac{\ln 3}{\ln 2} \approx 34.87$ años.
   b) Tiempo para cuadruplicar: $4 = e^{kt} \implies t = \frac{\ln 4}{k} = 22\frac{2\ln 2}{\ln 2} = 44$ años.

c) **Decaimiento radioactivo:** Vida media de 3.3 horas, $A_0 = 5$ gr.
   $k = \frac{-\ln 2}{3.3}$.
   a) Tiempo para desintegrar 90% (queda 10%): $0.1 = e^{kt} \implies t = \frac{\ln(0.1)}{k} = 3.3\frac{\ln 10}{\ln 2} \approx 10.96$ horas.
   b) Tiempo para que quede 1 gr: $1 = 5e^{kt} \implies t = \frac{\ln(0.2)}{k} = 3.3\frac{\ln 5}{\ln 2} \approx 7.66$ horas.

## Fase 2. Ecuaciones Diferenciales de orden superior

### VI & VII. Solución de Ecuaciones Homogéneas

a) $y'' + 3y' + 2y = 0$
   Ecuación característica: $r^2+3r+2=0 \implies (r+1)(r+2)=0 \implies r_1=-1, r_2=-2$.
   **Solución:** $y = C_1e^{-x} + C_2e^{-2x}$.

b) $y'' - 4y = 0$
   Ecuación característica: $r^2-4=0 \implies r=\pm 2$.
   **Solución:** $y = C_1e^{2x} + C_2e^{-2x}$.

c) $(D^3 + 9D^2 - 30D - 200)y = 0$
   Raíces de $r^3+9r^2-30r-200=0$ son $r=5, -4, -10$.
   **Solución:** $y = C_1e^{5x} + C_2e^{-4x} + C_3e^{-10x}$.

d) $(D^4 - 17D^3 + 105D^2 - 275D + 250)y = 0$
   Raíces de $r^4 - 17r^3 + 105r^2 - 275r + 250 = 0$ son $r=2$ y $r=5$ (raíz triple).
   **Solución:** $y = C_1e^{2x} + (C_2 + C_3x + C_4x^2)e^{5x}$.

e) $y'' + 2y' + 17y = 0$, con $y(0)=4, y'(0)=-2$
   $r^2+2r+17=0 \implies r = -1 \pm 4i$.
   Solución general: $y = e^{-x}(C_1\cos(4x) + C_2\sin(4x))$.
   Aplicando condiciones iniciales: $C_1=4, C_2=1/2$.
   **Solución particular:** $y = e^{-x}(4\cos(4x) + \frac{1}{2}\sin(4x))$.

### VIII. Coeficientes Indeterminados

a) $y'' + y = x^2 - 4$
   Solución homogénea: $y_h = C_1\cos x + C_2\sin x$.
   Solución particular: $y_p = Ax^2+Bx+C$. Sustituyendo se obtiene $A=1, B=0, C=-6$.
   **Solución:** $y = C_1\cos x + C_2\sin x + x^2 - 6$.

b) $y'' + y = 4e^{-x} - 9$
   Solución homogénea: $y_h = C_1\cos x + C_2\sin x$.
   Solución particular: $y_p = Ae^{-x} + B$. Sustituyendo se obtiene $A=2, B=-9$.
   **Solución:** $y = C_1\cos x + C_2\sin x + 2e^{-x} - 9$.

### IX. Problema de Viga

Para una viga empotrada en ambos extremos con carga uniforme $w$, la ecuación de deflexión es $EI y(x) = \frac{w}{24}(-x^4 + 2Lx^3 - L^2x^2)$.
Con $L=12, w=3000, EI=50 \times 10^6$.
La deformación máxima ocurre en $x=L/2=6$.
$$ y(6) = \frac{3000}{24 \cdot 50 \times 10^6} (-(6)^4 + 2(12)(6)^3 - (12)^2(6)^2) $$
$$ y(6) = \frac{1}{400000} (-1296 + 5184 - 5184) = \frac{-1296}{400000} = -0.00324 \text{ m} $$
La deformación máxima es de **3.24 mm**.

## Fase 3. Tópicos de Métodos Numéricos

### X. Método de Falsa Posición
Para $f(x) = x^3 - 6x^2 + 11x - 6.1 = 0$.
Se buscan intervalos donde la función cambia de signo. Por ejemplo, para la raíz cercana a 3:
$f(3) = -0.1$ y $f(3.1) = 0.131$. El intervalo es $[3, 3.1]$.
La fórmula de iteración es $c = b - \frac{f(b)(b-a)}{f(b)-f(a)}$.
Se repite el proceso hasta alcanzar la precisión deseada. Las raíces están cerca de 1.0, 2.0 y 3.0.

### XI. Método de Newton-Raphson
Para $f(x) = x - 1 - 0.5\sin(x) = 0$.
$f'(x) = 1 - 0.5\cos(x)$.
La fórmula de iteración es $x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}$.
Empezando con $x_0 = 1.5$:
$x_1 = 1.5 - \frac{1.5 - 1 - 0.5\sin(1.5)}{1 - 0.5\cos(1.5)} \approx 1.4987$.
Se repite hasta converger.

### XII. Método del Trapecio
Para $\int_0^3 \frac{1}{1+x^2} dx$.
Usando los puntos de la gráfica (0,1), (1,0.5), (2,0.2), (3,0.1) y $h=1$.
Área $\approx \frac{h}{2}(f(x_0)+2f(x_1)+2f(x_2)+f(x_3))$ no es la fórmula correcta para trapecios individuales.
Suma de las áreas de los trapecios:
$A = \frac{1}{2}(1+0.5)(1) + \frac{1}{2}(0.5+0.2)(1) + \frac{1}{2}(0.2+0.1)(1) = 0.75 + 0.35 + 0.15 = 1.25$.
Valor exacto: $\arctan(3) \approx 1.2490$.
Error porcentual: $\frac{|1.2490 - 1.25|}{1.2490} \times 100\% \approx 0.08\%$.

### XIII. Método de Simpson 3/8
Para $\int_0^{0.8} f(x) dx$ con $n=9$.
$h = (0.8-0)/9 = 0.8/9$.
La fórmula es $I = \frac{3h}{8} [f(x_0) + 3f(x_1) + 3f(x_2) + 2f(x_3) + ... + f(x_9)]$.
Se requiere evaluar la función en 10 puntos y aplicar la fórmula.

### XIV. Método de Simpson 1/3
Para $\int_0^{0.8} f(x) dx$ con $n=8$.
$h = (0.8-0)/8 = 0.1$.
La fórmula es $I = \frac{h}{3} [f(x_0) + 4f(x_1) + 2f(x_2) + ... + 4f(x_7) + f(x_8)]$.
Se requiere evaluar la función en 9 puntos y aplicar la fórmula.

### XV. Método de Euler
Para $\frac{dy}{dx} = \frac{\sqrt{y}}{2x+1}$, con $y(0)=4, h=0.5$, encontrar $y(5)$.
Fórmula: $y_{i+1} = y_i + f(x_i, y_i)h$.
$x_0=0, y_0=4$.
$y_1 = y(0.5) = 4 + \frac{\sqrt{4}}{2(0)+1}(0.5) = 4 + 2(0.5) = 5$.
$y_2 = y(1.0) = 5 + \frac{\sqrt{5}}{2(0.5)+1}(0.5) = 5 + \frac{2.236}{2}(0.5) \approx 5.559$.
... Se repite el proceso 10 veces para llegar a $x=5$.