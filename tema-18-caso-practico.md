# Tema 18 — Casos Prácticos

> **Título oficial**: Lenguajes de programación. Tipos de datos. Operadores. Instrucciones condicionales. Bucles y recursividad. Procedimientos, funciones y parámetros. Vectores y registros. Estructura de un programa.
>
> **Formato**: 3 casos prácticos sobre supuestos reales del Ayuntamiento de Madrid. Cada caso suma **10 puntos**.
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid

Los tres casos recorren el tema en pseudocódigo neutro: el **Caso 1** trabaja **tipos, operadores y estructuras de control** (cálculo de una tasa con condicionales) sobre los tributos; el **Caso 2**, **arrays, registros y bucles** (procesar el censo de los distritos); y el **Caso 3**, **funciones, recursividad y paso de parámetros** sobre la tramitación de expedientes.

---

## Caso 1 — Cálculo de la tasa de un servicio municipal

### Enunciado

El Ayuntamiento aplica una **tasa** por la tramitación de una licencia. La cuota se calcula sobre un **importe base** al que se aplica una **bonificación** según la renta del solicitante: renta inferior a 12.000 € → 50 %; entre 12.000 y 20.000 € → 25 %; superior a 20.000 € → sin bonificación. Además, si el solicitante tiene **familia numerosa**, se aplica **5 puntos porcentuales adicionales** de bonificación (acumulables). La cuota final nunca puede ser negativa. Debe diseñar el algoritmo de cálculo.

### Cuestiones

**Cuestión 1 — Tipos de datos (2 puntos).** Indique qué tipo de dato usaría para: el importe base, la renta, el porcentaje de bonificación y el indicador de familia numerosa. Justifique la elección del tipo para importes monetarios.

**Cuestión 2 — Estructura de control (3 puntos).** Escriba en pseudocódigo la lógica que asigna la bonificación por tramos de renta. ¿Qué estructura de control es la más adecuada y por qué?

**Cuestión 3 — Operadores y expresión (3 puntos).** Escriba la expresión que calcula la `cuota_final` a partir del `importe_base` y la `bonificacion` total (en tanto por uno). Añada el ajuste de familia numerosa y garantice que la cuota no sea negativa.

**Cuestión 4 — Constante y mantenimiento (2 puntos).** Los umbrales (12.000, 20.000) y los porcentajes aparecen en el código. ¿Cómo mejoraría el mantenimiento del programa si el pleno cambia los tramos el año que viene?

### Solución orientativa

- **C1**: `importe_base` y `cuota_final` → **entero de céntimos** o tipo **decimal** exacto (nunca coma flotante, por el redondeo de dinero, §2.2); `renta` → real o entero de euros; `bonificacion` → real (tanto por uno); `familia_numerosa` → **booleano** (verdadero/falso). *(§2.1-2.2)*
- **C2**: condicional **múltiple anidado** (`si … si_no si … si_no`), porque se decide sobre **rangos** de un valor continuo (la renta), no sobre valores discretos —lo que descartaría un `segun`/`switch`—. *(§4.2)*

```
si (renta < UMBRAL_BAJO) entonces
    bonificacion = 0.50
si_no si (renta < UMBRAL_MEDIO) entonces
    bonificacion = 0.25
si_no
    bonificacion = 0.00
fin_si
```

- **C3**: se acumulan los 5 puntos (0.05) si hay familia numerosa y se aplica el operador para evitar negativos. *(§3.1, §3.3, §4.2)*

```
si (familia_numerosa) entonces
    bonificacion = bonificacion + 0.05
fin_si
cuota_final = importe_base * (1 - bonificacion)
si (cuota_final < 0) entonces
    cuota_final = 0
fin_si
```

- **C4**: sustituir los «números mágicos» por **constantes con nombre** (`UMBRAL_BAJO = 12000`, `UMBRAL_MEDIO = 20000`, `BONIF_BAJA = 0.50`…) declaradas en un solo lugar. Así, un cambio de tramos se hace en **un único punto** sin buscar por todo el código (principio DRY, §6.2). *(§1.5, §6.2)*

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Elige tipos correctos y justifica el tipo monetario exacto | 2 |
| Usa condicional múltiple anidado y lo justifica frente a switch | 3 |
| Expresión de cuota correcta con ajuste y control de no-negativo | 3 |
| Propone constantes con nombre para el mantenimiento (DRY) | 2 |

---

## Caso 2 — Procesado del censo de habitantes por distrito

### Enunciado

Se dispone del **censo del Padrón** como un **array de registros** `Habitante`, con los campos `dni`, `nombre`, `edad` (entero) y `codigo_distrito` (entero de 1 a 21). Se pide un módulo que, recorriendo el censo **una sola vez**, calcule: (a) el **número total** de habitantes, (b) cuántos son **mayores de edad** (18 o más) y (c) la **población de cada distrito** en un array indexado por distrito. Los 21 distritos de Madrid se numeran del 1 al 21.

### Cuestiones

**Cuestión 1 — Estructuras de datos (2 puntos).** Defina el tipo registro `Habitante` y declare las estructuras que necesita para almacenar el censo y el resultado de población por distrito.

**Cuestión 2 — Recorrido con bucle (3 puntos).** Escriba en pseudocódigo el recorrido del censo que actualiza los tres resultados. ¿Qué tipo de bucle usa y por qué?

**Cuestión 3 — Acceso a array y a campo (3 puntos).** Explique cómo accede, dentro del bucle, al distrito de cada habitante y cómo incrementa el contador del distrito correspondiente. Distinga el acceso por índice del acceso por campo.

**Cuestión 4 — Programación defensiva (2 puntos).** ¿Qué comprobación añadiría antes de usar `codigo_distrito` como índice del array de población? ¿Qué ocurriría si un registro trae un distrito 0 o 25?

### Solución orientativa

- **C1**: registro y arrays. El acceso al elemento del censo es por **índice** (`censo[i]`) y a sus datos por **nombre de campo** (`censo[i].edad`). *(§5.1-5.2)*

```
tipo Habitante = registro
    dni : cadena
    nombre : cadena
    edad : entero
    codigo_distrito : entero
fin_registro

declarar censo : array[1..N] de Habitante
declarar poblacion : array[1..21] de entero   // contador por distrito
```

- **C2**: bucle **`para`** (for), porque el número de habitantes `N` es **conocido**; un único recorrido O(n) calcula los tres resultados (§4.3, §5.3).

```
total = 0
mayores = 0
para d desde 1 hasta 21 hacer poblacion[d] = 0 fin_para   // inicializar
para i desde 1 hasta N hacer
    total = total + 1
    si (censo[i].edad >= 18) entonces
        mayores = mayores + 1
    fin_si
    dist = censo[i].codigo_distrito
    poblacion[dist] = poblacion[dist] + 1
fin_para
```

- **C3**: `censo[i]` accede al **registro** i-ésimo **por índice** (O(1)); `.codigo_distrito` accede a su **campo** **por nombre**. Ese valor se usa a su vez como **índice** del array `poblacion`, y `poblacion[dist] = poblacion[dist] + 1` incrementa el contador de ese distrito. *(§5.1-5.3)*
- **C4**: antes de usarlo como índice, comprobar el **rango**: `si (dist >= 1 Y dist <= 21) entonces …`. Sin esa comprobación, un distrito 0 o 25 provocaría un **acceso fuera de rango** (índice inválido): corrupción de memoria en C o excepción `IndexOutOfBounds` en Java/Python (§5.1). Es programación defensiva (§6.2). *(§5.1, §6.2)*

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Define el registro Habitante y declara censo + array de población | 2 |
| Recorrido en un solo bucle `para` justificado, con inicialización | 3 |
| Distingue acceso por índice (censo[i]) de acceso por campo (.distrito) | 3 |
| Valida el rango del índice antes de usarlo (defensiva) | 2 |

---

## Caso 3 — Tramitación y numeración de expedientes

### Enunciado

Una unidad tramita **expedientes** identificados por un número. Se pide: (a) una **función** que valide si un número de expediente es **par** (por criterio interno, los pares se asignan a la vía telemática); (b) una **función recursiva** que calcule la **suma de los primeros N** números de expediente (1 + 2 + … + N) para una estadística de carga; y (c) razonar el efecto de pasar un contador **por valor** o **por referencia** a un procedimiento que lo incrementa.

### Cuestiones

**Cuestión 1 — Función y operador (2 puntos).** Escriba la función `es_par(n)` que devuelve verdadero si `n` es par. ¿Qué operador utiliza?

**Cuestión 2 — Recursividad (4 puntos).** Escriba la función **recursiva** `suma_hasta(n)` que calcule 1 + 2 + … + n. Identifique el **caso base** y el **caso recursivo**, y explique qué pasaría sin caso base.

**Cuestión 3 — Traza (2 puntos).** Muestre la traza de `suma_hasta(4)` indicando el valor devuelto.

**Cuestión 4 — Paso de parámetros (2 puntos).** Un procedimiento `incrementar(c) { c = c + 1 }` se llama con `contador = 10`. ¿Cuánto vale `contador` después si el paso es **por valor**? ¿Y si es **por referencia**?

### Solución orientativa

- **C1**: usa el operador **módulo** (`mod`), que devuelve el resto (§3.1). Es una **función** porque **devuelve un valor** (booleano), §4.5.

```
funcion es_par(n)
    devolver (n mod 2 == 0)
fin_funcion
```

- **C2**: la función recursiva necesita **caso base** y **caso recursivo** (§4.4). Sin caso base habría **recursión infinita** con desbordamiento de pila.

```
funcion suma_hasta(n)
    si (n <= 1) entonces          // caso base
        devolver n
    si_no
        devolver n + suma_hasta(n - 1)   // caso recursivo
    fin_si
fin_funcion
```

- **C3**: `suma_hasta(4) = 4 + suma_hasta(3) = 4 + (3 + suma_hasta(2)) = 4 + (3 + (2 + suma_hasta(1)))`. El caso base `suma_hasta(1) = 1`. Se desenrolla: `2+1=3`, `3+3=6`, `4+6=` **10**. *(§4.4)*
- **C4**: **por valor**, `contador` sigue valiendo **10** (se incrementó una copia); **por referencia**, `contador` pasa a **11** (se modificó el original a través de su dirección). *(§4.6)*

### Criterios de evaluación

| Criterio | Puntos |
|---|---|
| Función `es_par` correcta usando el operador módulo | 2 |
| Función recursiva con caso base y recursivo bien identificados | 4 |
| Traza de `suma_hasta(4)` = 10 correcta | 2 |
| Distingue el efecto de por valor (10) y por referencia (11) | 2 |

---

*Los tres casos son orientativos y pensados para la autoevaluación; las soluciones muestran una vía correcta, no la única posible. El contexto (tributos, Padrón, expedientes) es propio del Ayuntamiento de Madrid.*
