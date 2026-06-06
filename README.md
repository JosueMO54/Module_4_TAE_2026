# Module_4_TAE_2026
## Resumen Consolidado de los Ejercicios

### Ejercicio 1: Implementación de una función lineal (1D)

**Objetivo:** Implementar una función lineal 1D de la forma $y = \beta + \omega x$.

**Implementación:**
- Se completó la función `linear_1d_student(x, beta, omega)` para devolver el valor de $y$ basándose en $x$, $\beta$ y $\omega$.

**Verificación:**
- La implementación se verificó mediante una aserción que comprobaba valores correctos conocidos, confirmando la exactitud de la función.

### Ejercicio 2: Implementación de la función lineal 2D y razonamiento sobre parámetros

**Objetivo:** Implementar una función lineal 2D de la forma $y = \beta + \omega_1 x_1 + \omega_2 x_2$ y explorar sus gráficos de contorno.

**Implementación:**
- Se completó la función `linear_2d_student(x1, x2, beta, omega1, omega2)` para calcular la función lineal 2D.

**Verificación y Exploración:**
- Una prueba rápida confirmó la corrección matemática de la función `linear_2d_student`.
- El código permitió la exploración de los contornos de la función variando parámetros como `beta`, `omega1` y `omega2`, visualizando cómo estos afectan la forma y posición del plano 2D.

### Ejercicio 3: Cálculo por lotes

**Objetivo:** Implementar una función para el cálculo por lotes de múltiples funciones lineales utilizando multiplicación matricial, siguiendo la fórmula $Y = \beta + X\Omega^\top$.

**Implementación:**
- Se implementó la función `linear_batch_student(X, beta, Omega)` para realizar la multiplicación y suma de matrices, calculando la salida `Y` para un lote de entradas `X` y las matrices `beta` y `Omega` dadas.

**Verificación:**
- La función se probó con una salida esperada calculada manualmente, asegurando que las formas y los valores de `Y` fueran correctos. La prueba se pasó con éxito.

### Ejercicio 4: Derivada numérica vs. derivada analítica

**Objetivo:** Implementar la derivada numérica utilizando la fórmula de la diferencia central.

**Implementación:**
- Se implementó la función `numerical_derivative_student(f, x, eps)`. Esta calcula una aproximación de la derivada de una función `f` en el punto `x` utilizando un pequeño valor `eps` (épsilon) para el método de la diferencia central.

**Verificación:**
- La implementación se probó comparando su salida para la función `sin(x)` con su derivada analítica `cos(x)`. Se generó un gráfico para comparar visualmente las derivadas numérica y analítica, demostrando la precisión de la aproximación numérica.

### Ejercicio 5: Derivadas de una función cúbica

**Objetivo:** Explorar las derivadas de una función cúbica definiéndola y su derivada analítica, graficando su línea tangente y comparando las derivadas numérica y analítica.

**Implementación:**
- `f_cubic(x)`: Se definió una función cúbica de ejemplo (por ejemplo, $x^3 - 2x$).
- `df_cubic(x)`: Se implementó la derivada analítica de `f_cubic(x)` (por ejemplo, $3x^2 - 2$).
- **Gráfico de la línea tangente:** Se calculó y graficó `f_cubic(x)` junto con su línea tangente en `x0 = 0.5` utilizando la función auxiliar `tangent_line`.
- **Gráfico de comparación de derivadas:** Se comparó `df_cubic(x)` (derivada analítica) con la derivada numérica obtenida usando `numerical_derivative_student` para `f_cubic(x)`. Ambas se graficaron para una comparación visual.

**Resultados:**
- Los gráficos confirman visualmente que la línea tangente aproxima correctamente la pendiente de la función en el punto dado.
- Las derivadas analíticas y numéricas coincidieron estrechamente, validando tanto la implementación de la derivada como el método de aproximación numérica.

### Ejercicio 6: Gradiente de una función de silla

**Objetivo:** Definir y visualizar una función de silla 2D y su campo de gradiente.

**Implementación:**
- `f_saddle(x1, x2)`: Se definió una función de silla 2D (por ejemplo, $x_1 * x_2$).
- `grad_saddle(x1, x2)`: Se implementó el gradiente analítico de `f_saddle(x1, x2)` como un array `[df/dx1, df/dx2]` (por ejemplo, `[x2, x1]`).
- **Gráfico de contorno:** Se visualizaron los contornos de `f_saddle(x1, x2)` para mostrar la forma de la superficie de la silla.
- **Gráfico del campo de gradiente:** Se superpuso un gráfico de quiver (campo vectorial) que representa el gradiente sobre los contornos, ilustrando que los vectores de gradiente apuntan en la dirección de mayor ascenso.

**Resultados:**
- El gráfico de contorno muestra claramente la forma característica de un punto de silla.
- El gráfico del campo de gradiente representa con precisión la dirección y la magnitud del mayor aumento de la función en varios puntos, confirmando la corrección de la implementación de `grad_saddle`.
