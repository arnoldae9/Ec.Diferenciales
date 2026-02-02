---
title: Elasticidad
subtitle: Elasticidad
author: "Prof. Arnoldo Del Toro Peña"
date: \today
subject: No sé
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
  - \fancyhead[L]{Elasticidad - Elasticidad}
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


# Cálculos de Elasticidad
## Actividad 3.1

### Problemas

**1. Una barra de cobre se somete a un esfuerzo de tensión de 40,000 psi. Si la deformación es totalmente elástica y la barra tiene 12 pulg. de longitud, ¿cuál será el alargamiento resultante si el cobre tiene un módulo elástico de 16 x 10^6 psi?**

Usamos la fórmula del Módulo de Young:
$$ E = \frac{\sigma}{\epsilon} $$
Donde $E$ es el módulo elástico, $\sigma$ es el esfuerzo y $\epsilon$ es la deformación unitaria.

La deformación unitaria se define como:
$$ \epsilon = \frac{\Delta L}{L_0} $$
Donde $\Delta L$ es el alargamiento y $L_0$ es la longitud inicial.

Despejando el alargamiento $\Delta L$:
$$ \Delta L = \epsilon \cdot L_0 = \frac{\sigma}{E} \cdot L_0 $$

Sustituyendo los valores dados:
$\sigma = 40,000 \text{ psi}$
$L_0 = 12 \text{ pulg}$
$E = 16 \times 10^6 \text{ psi}$

$$ \Delta L = \frac{40,000 \text{ psi}}{16 \times 10^6 \text{ psi}} \cdot 12 \text{ pulg} = 0.0025 \cdot 12 \text{ pulg} = 0.03 \text{ pulg} $$

**Solución:** El alargamiento resultante es de $0.03$ pulgadas.

**2. Una muestra cilíndrica de una aleación con un diámetro original de 0.15 pulg y un módulo elástico de 15.5 x10^6 psi. sólo experimentará una deformación elástica cuando se aplique una carga de tracción de 450 lb. Calcula la deformación y la longitud final de la barra, si originalmente medía 10 pulg. de longitud.**

Primero, calculamos el área de la sección transversal:
$d_0 = 0.15 \text{ pulg}$
$$ A_0 = \frac{\pi d_0^2}{4} = \frac{\pi (0.15 \text{ pulg})^2}{4} \approx 0.01767 \text{ pulg}^2 $$

Luego, calculamos el esfuerzo ($\sigma$):
$F = 450 \text{ lb}$
$$ \sigma = \frac{F}{A_0} = \frac{450 \text{ lb}}{0.01767 \text{ pulg}^2} \approx 25464.7 \text{ psi} $$

Ahora, calculamos la deformación unitaria ($\epsilon$):
$E = 15.5 \times 10^6 \text{ psi}$
$$ \epsilon = \frac{\sigma}{E} = \frac{25464.7 \text{ psi}}{15.5 \times 10^6 \text{ psi}} \approx 0.001643 $$

Finalmente, calculamos la longitud final ($L_f$):
$L_0 = 10 \text{ pulg}$
$\Delta L = \epsilon \cdot L_0 = 0.001643 \cdot 10 \text{ pulg} = 0.01643 \text{ pulg}$
$$ L_f = L_0 + \Delta L = 10 \text{ pulg} + 0.01643 \text{ pulg} = 10.01643 \text{ pulg} $$

**Solución:** La deformación es de $0.001643$ y la longitud final es de $10.01643$ pulgadas.

**3. Una barra de acero de 4.0 pulg. de longitud y con una sección transversal cuadrada de 0.8 pulg. por lado, es sometida a una carga de tensión de 20,000 lb y experimenta un alargamiento de 4.0 x 10^-3 pulg. Suponiendo que la deformación es totalmente elástica, calcule el módulo elástico.**

Calculamos el área de la sección transversal:
$A_0 = (0.8 \text{ pulg})^2 = 0.64 \text{ pulg}^2$

Calculamos el esfuerzo ($\sigma$):
$F = 20,000 \text{ lb}$
$$ \sigma = \frac{F}{A_0} = \frac{20,000 \text{ lb}}{0.64 \text{ pulg}^2} = 31,250 \text{ psi} $$

Calculamos la deformación unitaria ($\epsilon$):
$L_0 = 4.0 \text{ pulg}$
$\Delta L = 4.0 \times 10^{-3} \text{ pulg}$
$$ \epsilon = \frac{\Delta L}{L_0} = \frac{4.0 \times 10^{-3} \text{ pulg}}{4.0 \text{ pulg}} = 0.001 $$

Calculamos el módulo elástico ($E$):
$$ E = \frac{\sigma}{\epsilon} = \frac{31,250 \text{ psi}}{0.001} = 31.25 \times 10^6 \text{ psi} $$

**Solución:** El módulo elástico es de $31.25 \times 10^6$ psi.

**4. Una muestra cilíndrica de aluminio que tiene un diámetro de 0.75 pulg. y una longitud de 8.0 pulg. se deforma elásticamente en tensión con una carga de 11,000 lb. Si el aluminio tiene un Módulo Elástico de 10x10^6 psi y una relación de Poisson de 0.33, a) calcula el cambio de longitud en dirección al esfuerzo aplicado y b) calcula el cambio de diámetro en la muestra.**

a) Cambio de longitud ($\Delta L$):
Área: $A_0 = \frac{\pi (0.75 \text{ pulg})^2}{4} \approx 0.44178 \text{ pulg}^2$
Esfuerzo: $\sigma = \frac{11,000 \text{ lb}}{0.44178 \text{ pulg}^2} \approx 24899.5 \text{ psi}$
Deformación axial: $\epsilon_{axial} = \frac{\sigma}{E} = \frac{24899.5 \text{ psi}}{10 \times 10^6 \text{ psi}} \approx 0.00249$
$$ \Delta L = \epsilon_{axial} \cdot L_0 = 0.00249 \cdot 8.0 \text{ pulg} = 0.01992 \text{ pulg} $$

b) Cambio de diámetro ($\Delta d$):
Relación de Poisson: $\nu = -\frac{\epsilon_{lateral}}{\epsilon_{axial}}$
Deformación lateral: $\epsilon_{lateral} = -\nu \cdot \epsilon_{axial} = -0.33 \cdot 0.00249 = -0.0008217$
$$ \Delta d = \epsilon_{lateral} \cdot d_0 = -0.0008217 \cdot 0.75 \text{ pulg} \approx -0.000616 \text{ pulg} $$

**Solución:** a) El cambio de longitud es de $0.01992$ pulgadas. b) El cambio de diámetro es de $-0.000616$ pulgadas.

**5. Una probeta cilíndrica de una aleación de 0.31 pulg. de diámetro se somete a una tensión elástica. Una carga de 3530 lb produce una reducción del diámetro de 2x10^-4 pulg. Calcule la relación de Poisson para este material si su Módulo de Elasticidad es de 20.3x10^6 psi.**

Área: $A_0 = \frac{\pi (0.31 \text{ pulg})^2}{4} \approx 0.07547 \text{ pulg}^2$
Esfuerzo: $\sigma = \frac{3530 \text{ lb}}{0.07547 \text{ pulg}^2} \approx 46773.5 \text{ psi}$
Deformación axial: $\epsilon_{axial} = \frac{\sigma}{E} = \frac{46773.5 \text{ psi}}{20.3 \times 10^6 \text{ psi}} \approx 0.002304$
Deformación lateral: $\epsilon_{lateral} = \frac{\Delta d}{d_0} = \frac{-2 \times 10^{-4} \text{ pulg}}{0.31 \text{ pulg}} \approx -0.000645$
$$ \nu = -\frac{\epsilon_{lateral}}{\epsilon_{axial}} = -\frac{-0.000645}{0.002304} \approx 0.28 $$

**Solución:** La relación de Poisson es de $0.28$.

**6. Un cubo de metal cuyas dimensiones son 10 cm x 10 cm x 10cm, se le aplica una carga de 200 MPa en el eje “X”. ¿Cuáles serán las dimensiones del cubo en sus 3 ejes, si tiene un modulo de elasticidad de 2,500 MPa y una relación de Poisson de 0.30?**

Deformación en el eje X:
$\sigma_x = 200 \text{ MPa}$
$E = 2,500 \text{ MPa}$
$$ \epsilon_x = \frac{\sigma_x}{E} = \frac{200 \text{ MPa}}{2,500 \text{ MPa}} = 0.08 $$
Nueva dimensión en X:
$L_x = L_0(1 + \epsilon_x) = 10 \text{ cm} (1 + 0.08) = 10.8 \text{ cm}$

Deformación en los ejes Y y Z:
$\nu = 0.30$
$$ \epsilon_y = \epsilon_z = -\nu \cdot \epsilon_x = -0.30 \cdot 0.08 = -0.024 $$
Nuevas dimensiones en Y y Z:
$L_y = L_z = L_0(1 + \epsilon_y) = 10 \text{ cm} (1 - 0.024) = 9.76 \text{ cm}$

**Solución:** Las nuevas dimensiones son $10.8 \text{ cm} \times 9.76 \text{ cm} \times 9.76 \text{ cm}$.

**7. Calcula la relación de Poisson para una muestra cubica de 15cm x 15cm x15cm, la cual se introduce a una cámara de presión a 200 MPa, si sus dimensiones se redujeron de 15cm a 14.97 cm cada lado. Su Modulo de Elasticidad es de 55,000 MPa.**

La presión es hidrostática, por lo que el esfuerzo es el mismo en todas las direcciones:
$\sigma_x = \sigma_y = \sigma_z = -P = -200 \text{ MPa}$

La deformación unitaria es la misma en todas las direcciones:
$L_0 = 15 \text{ cm}$
$L_f = 14.97 \text{ cm}$
$$ \epsilon = \frac{L_f - L_0}{L_0} = \frac{14.97 - 15}{15} = \frac{-0.03}{15} = -0.002 $$

La ecuación de deformación para un estado de esfuerzo triaxial es:
$$ \epsilon_x = \frac{1}{E}[\sigma_x - \nu(\sigma_y + \sigma_z)] $$
Como $\epsilon_x = \epsilon$ y $\sigma_x = \sigma_y = \sigma_z = -P$:
$$ \epsilon = \frac{1}{E}[-P - \nu(-P - P)] = \frac{-P}{E}(1 - 2\nu) $$

Despejamos la relación de Poisson ($\nu$):
$-0.002 = \frac{-200 \text{ MPa}}{55,000 \text{ MPa}}(1 - 2\nu)$
$$ \frac{-0.002 \cdot 55,000}{-200} = 1 - 2\nu $$
$$ 0.55 = 1 - 2\nu $$
$$ 2\nu = 1 - 0.55 = 0.45 $$
$$ \nu = 0.225 $$

**Solución:** La relación de Poisson es de $0.225$.