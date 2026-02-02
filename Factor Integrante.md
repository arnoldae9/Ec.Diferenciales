# Factor Integrante - Ecuaciones Diferenciales

## Definición
El **factor integrante** es una función $\mu(x)$ o $\mu(y)$ que se multiplica por una ecuación diferencial para hacerla **exacta**.

## Ecuación Diferencial Lineal de Primer Orden

### Forma estándar:
$$\frac{dy}{dx} + P(x)y = Q(x)$$

### Factor integrante:
$$\mu(x) = e^{\int P(x)dx}$$

### Solución general:
$$y = \frac{1}{\mu(x)}\left[\int \mu(x)Q(x)dx + C\right]$$

### Procedimiento:
1. Escribir la ecuación en forma estándar
2. Identificar $P(x)$ y $Q(x)$
3. Calcular $\mu(x) = e^{\int P(x)dx}$
4. Multiplicar toda la ecuación por $\mu(x)$
5. Integrar ambos lados

## Ecuaciones Diferenciales Exactas

### Forma general:
$$M(x,y)dx + N(x,y)dy = 0$$

### Condición de exactitud:
$$\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$$

## Cuando NO es exacta - Factor Integrante

### Caso 1: Factor integrante función solo de x
Si $\frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N}$ depende solo de $x$:

$$\mu(x) = e^{\int \frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N}dx}$$

### Caso 2: Factor integrante función solo de y
Si $\frac{\frac{\partial N}{\partial x} - \frac{\partial M}{\partial y}}{M}$ depende solo de $y$:

$$\mu(y) = e^{\int \frac{\frac{\partial N}{\partial x} - \frac{\partial M}{\partial y}}{M}dy}$$

## Factores Integrantes Especiales

### 1. Para ecuaciones de la forma $xdy - ydx + f(x,y)dx = 0$
- $\mu = \frac{1}{x^2}$ (útil para obtener $d(\frac{y}{x})$)
- $\mu = \frac{1}{y^2}$ (útil para obtener $d(\frac{x}{y})$)

### 2. Para ecuaciones de la forma $xdy + ydx + f(x,y)dx = 0$
- $\mu = \frac{1}{xy}$ (útil para obtener $d(\ln|xy|)$)

### 3. Para ecuaciones homogéneas
- $\mu = \frac{1}{x^2 + y^2}$
- $\mu = \frac{1}{xy}$

## Ejemplos Paso a Paso

### Ejemplo 1: Factor Integrante para Ecuación Lineal

**Resolver:** $\frac{dy}{dx} - 2y = 3e^{3x}$

### Paso 1: Identificar la forma estándar
$$\frac{dy}{dx} + P(x)y = Q(x)$$

Donde: $P(x) = -2$ y $Q(x) = 3e^{3x}$

### Paso 2: Calcular el factor integrante
$$\mu(x) = e^{\int P(x)dx} = e^{\int -2dx} = e^{-2x}$$

### Paso 3: Multiplicar la ecuación por $\mu(x)$
$$e^{-2x}\frac{dy}{dx} - 2e^{-2x}y = 3e^{3x} \cdot e^{-2x}$$

$$e^{-2x}\frac{dy}{dx} - 2e^{-2x}y = 3e^{x}$$

### Paso 4: Reconocer el lado izquierdo como derivada
$$\frac{d}{dx}[e^{-2x}y] = 3e^{x}$$

### Paso 5: Integrar ambos lados
$$e^{-2x}y = \int 3e^{x}dx = 3e^{x} + C$$

### Paso 6: Despejar y
$$y = \frac{3e^{x} + C}{e^{-2x}} = 3e^{3x} + Ce^{2x}$$

**Solución final:** $y = 3e^{3x} + Ce^{2x}$

---

### Ejemplo 2: Factor Integrante para Ecuación NO Exacta

**Resolver:** $(3xy + y^2)dx + (x^2 + xy)dy = 0$

### Paso 1: Verificar exactitud
$M = 3xy + y^2$, $N = x^2 + xy$

$\frac{\partial M}{\partial y} = 3x + 2y$

$\frac{\partial N}{\partial x} = 2x + y$

Como $\frac{\partial M}{\partial y} \neq \frac{\partial N}{\partial x}$, la ecuación **NO ES EXACTA**.

### Paso 2: Buscar factor integrante que dependa solo de x
$$\frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N} = \frac{(3x + 2y) - (2x + y)}{x^2 + xy} = \frac{x + y}{x(x + y)} = \frac{1}{x}$$

Como esto depende solo de $x$, existe $\mu(x)$.

### Paso 3: Calcular el factor integrante
$$\mu(x) = e^{\int \frac{1}{x}dx} = e^{\ln|x|} = x$$

### Paso 4: Multiplicar la ecuación por $\mu(x) = x$
$$x(3xy + y^2)dx + x(x^2 + xy)dy = 0$$

$$(3x^2y + xy^2)dx + (x^3 + x^2y)dy = 0$$

### Paso 5: Verificar que ahora es exacta
$M_1 = 3x^2y + xy^2$, $N_1 = x^3 + x^2y$

$\frac{\partial M_1}{\partial y} = 3x^2 + x^2 = x^2(3 + 1) = 4x^2$

$\frac{\partial N_1}{\partial x} = 3x^2 + 2xy$

**Error en el cálculo, revisemos:**

$\frac{\partial N_1}{\partial x} = \frac{\partial}{\partial x}(x^3 + x^2y) = 3x^2 + 2xy$

$\frac{\partial M_1}{\partial y} = \frac{\partial}{\partial y}(3x^2y + xy^2) = 3x^2 + 2xy$

Ahora sí: $\frac{\partial M_1}{\partial y} = \frac{\partial N_1}{\partial x}$ ✓

### Paso 6: Resolver la ecuación exacta
$$\int M_1 dx = \int (3x^2y + xy^2)dx = x^3y + \frac{x^2y^2}{2} + g(y)$$

$$\frac{\partial}{\partial y}\left[x^3y + \frac{x^2y^2}{2} + g(y)\right] = x^3 + x^2y + g'(y) = N_1 = x^3 + x^2y$$

Por lo tanto: $g'(y) = 0$, entonces $g(y) = 0$

**Solución final:** $x^3y + \frac{x^2y^2}{2} = C$ o $2x^3y + x^2y^2 = C$

## Algoritmo General

1. **Identificar el tipo de ecuación**
2. **Si es lineal:** usar $\mu(x) = e^{\int P(x)dx}$
3. **Si es exacta:** resolver directamente
4. **Si no es exacta:** buscar factor integrante
   - Probar $\mu(x)$ si $\frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N} = f(x)$
   - Probar $\mu(y)$ si $\frac{\frac{\partial N}{\partial x} - \frac{\partial M}{\partial y}}{M} = f(y)$
   - Probar factores especiales según la forma

## Consejos Importantes

- **Siempre verificar** si la ecuación es exacta antes de buscar factor integrante
- **El factor integrante más común** es para ecuaciones lineales
- **Después de encontrar $\mu$**, verificar que la nueva ecuación sea exacta
- **La constante de integración** se puede omitir al calcular el factor integrante

## Fórmulas Clave para Memorizar

$$\boxed{\mu(x) = e^{\int P(x)dx} \text{ (ecuaciones lineales)}}$$

$$\boxed{\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x} \text{ (condición de exactitud)}}$$

$$\boxed{\mu(x) = e^{\int \frac{\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}}{N}dx}}$$

He agregado dos ejemplos completos y detallados:

**Ejemplo 1** muestra cómo resolver una ecuación diferencial lineal usando el factor integrante $\mu(x) = e^{\int P(x)dx}$. Es el caso más común y fundamental.

**Ejemplo 2** demuestra cómo encontrar y aplicar un factor integrante cuando la ecuación no es exacta, siguiendo todo el proceso:
- Verificar que no es exacta
- Determinar si existe factor integrante que depende solo de x
- Calcularlo e aplicarlo
- Verificar que la nueva ecuación es exacta
- Resolverla completamente

Ambos ejemplos incluyen todos los pasos intermedios y verificaciones necesarias para que puedas seguir el proceso completo. ¿Te gustaría que agregue algún ejemplo adicional de otro tipo de factor integrante o algún caso especial?