# Tema 18 — Test de Autoevaluación

> **Título**: Lenguajes de programación. Tipos de datos. Operadores. Instrucciones condicionales. Bucles y recursividad. Procedimientos, funciones y parámetros. Vectores y registros. Estructura de un programa.
> **Formato**: 60 preguntas tipo test A/B/C (formato oficial oposición)
> **Nivel**: C1 — Técnico Auxiliar TIC, Ayuntamiento de Madrid
> **Versión**: v1.0 — Pendiente validación
> **Fecha**: 2026-07-06
> **Fuentes**: ver tema-18-fuentes.md

---

## Instrucciones

- Cada pregunta tiene **3 opciones** (A, B, C). Solo una es correcta.
- Penalización en examen real: respuesta incorrecta descuenta **1/3** del valor de una correcta.
- Tiempo orientativo: 1 minuto por pregunta.
- Distribución: Lenguajes y elementos (P1-P12), Tipos de datos (P13-P22), Operadores (P23-P30), Estructuras de control y modularidad (P31-P46), Vectores y registros (P47-P54), Estructura del programa (P55-P58), Tendencias (P59-P60).

---

### Pregunta 1

**¿Qué es un lenguaje de programación de alto nivel?**

A) Una notación cercana al lenguaje humano e independiente de la máquina, que necesita un traductor
B) El conjunto de instrucciones en binario que ejecuta directamente el procesador
C) Un lenguaje que solo funciona en una arquitectura de CPU concreta

<details><summary>Respuesta</summary>

**Correcta: A) Una notación cercana al lenguaje humano e independiente de la máquina, que necesita un traductor** El alto nivel abstrae el hardware; el binario (B) y el dependiente de la CPU (C) son de bajo nivel.

*Referencia: §1.2 [SEBESTA]*
</details>

---

### Pregunta 2

**La diferencia fundamental entre un algoritmo y un programa es que:**

A) Son sinónimos exactos, no hay diferencia
B) El algoritmo es la secuencia lógica de pasos, independiente del lenguaje; el programa es ese algoritmo escrito en un lenguaje ejecutable
C) El programa es más abstracto que el algoritmo

<details><summary>Respuesta</summary>

**Correcta: B) El algoritmo es la secuencia lógica de pasos, independiente del lenguaje; el programa es ese algoritmo escrito en un lenguaje ejecutable** Un mismo algoritmo puede programarse en C, Java o Python.

*Referencia: §1.1 [SEBESTA]*
</details>

---

### Pregunta 3

**¿Cuáles son los tres componentes con que se define todo lenguaje de programación?**

A) Compilador, intérprete y ensamblador
B) Variables, funciones y bucles
C) Léxico, sintaxis y semántica

<details><summary>Respuesta</summary>

**Correcta: C) Léxico, sintaxis y semántica** Vocabulario (léxico), reglas gramaticales (sintaxis) y significado (semántica), igual que un lenguaje natural.

*Referencia: §1.1 [ASU]*
</details>

---

### Pregunta 4

**En la clasificación por generaciones, SQL es un ejemplo típico de:**

A) Lenguaje de 2.ª generación (ensamblador)
B) Lenguaje de 4.ª generación (declarativo)
C) Lenguaje de 1.ª generación (máquina)

<details><summary>Respuesta</summary>

**Correcta: B) Lenguaje de 4.ª generación (declarativo)** Los 4GL son declarativos: se indica QUÉ se quiere, no CÓMO obtenerlo. SQL es el ejemplo clásico.

*Referencia: §1.2 [PRATT]*
</details>

---

### Pregunta 5

**¿Qué caracteriza a un lenguaje del paradigma imperativo frente a uno declarativo?**

A) El imperativo solo se usa en inteligencia artificial
B) El imperativo no admite variables
C) En el imperativo se indica CÓMO resolver el problema (los pasos); en el declarativo, QUÉ se quiere obtener

<details><summary>Respuesta</summary>

**Correcta: C) En el imperativo se indica CÓMO resolver el problema (los pasos); en el declarativo, QUÉ se quiere obtener** El declarativo (SQL, Prolog) deja el «cómo» al sistema.

*Referencia: §1.2 [SEBESTA]*
</details>

---

### Pregunta 6

**¿Cuál es la diferencia entre un compilador y un intérprete?**

A) El compilador traduce el programa completo antes de ejecutarlo; el intérprete traduce y ejecuta instrucción a instrucción
B) El compilador es más lento porque traduce línea a línea
C) El intérprete genera siempre un fichero ejecutable independiente

<details><summary>Respuesta</summary>

**Correcta: A) El compilador traduce el programa completo antes de ejecutarlo; el intérprete traduce y ejecuta instrucción a instrucción** El compilador detecta muchos errores antes de ejecutar; el intérprete los revela en ejecución.

*Referencia: §1.2 [SEBESTA]*
</details>

---

### Pregunta 7

**El modelo de ejecución de Java («compile once, run anywhere») se basa en:**

A) Interpretar directamente el código fuente sin traducirlo
B) Compilar a código máquina específico de cada procesador
C) Compilar a un código intermedio (bytecode) que ejecuta una máquina virtual (JVM)

<details><summary>Respuesta</summary>

**Correcta: C) Compilar a un código intermedio (bytecode) que ejecuta una máquina virtual (JVM)** Es un modelo híbrido: portabilidad del bytecode + compilación JIT para rendimiento.

*Referencia: §1.2 [SEBESTA]*
</details>

---

### Pregunta 8

**La descripción formal de la sintaxis de un lenguaje suele expresarse mediante:**

A) Gramáticas en notación BNF (Backus-Naur Form)
B) Tablas de verdad booleanas
C) Diagramas entidad-relación

<details><summary>Respuesta</summary>

**Correcta: A) Gramáticas en notación BNF (Backus-Naur Form)** La BNF define reglas de producción que el análisis sintáctico del compilador comprueba.

*Referencia: §1.4 [ASU]*
</details>

---

### Pregunta 9

**Escribir `resultado = total / num` cuando `num` vale 0 constituye un:**

A) Error de sintaxis detectado al compilar
B) Error semántico dinámico (se manifiesta al ejecutar)
C) Error de estilo o pragmática, sin consecuencias

<details><summary>Respuesta</summary>

**Correcta: B) Error semántico dinámico (se manifiesta al ejecutar)** La sentencia es sintácticamente correcta; el fallo (división por cero) aparece en tiempo de ejecución.

*Referencia: §1.4 [SCOTT]*
</details>

---

### Pregunta 10

**¿Qué es un identificador en un lenguaje de programación?**

A) El nombre que el programador da a variables, constantes, funciones o tipos
B) Un valor numérico fijo que no puede cambiar
C) Un símbolo que representa una operación aritmética

<details><summary>Respuesta</summary>

**Correcta: A) El nombre que el programador da a variables, constantes, funciones o tipos** Suele distinguir mayúsculas de minúsculas y no puede coincidir con una palabra reservada.

*Referencia: §1.5 [SEBESTA]*
</details>

---

### Pregunta 11

**¿Cuál es la diferencia entre una variable y una constante?**

A) La constante ocupa más memoria que la variable
B) La variable puede cambiar de valor durante la ejecución; la constante mantiene fijo su valor
C) La variable no tiene tipo y la constante sí

<details><summary>Respuesta</summary>

**Correcta: B) La variable puede cambiar de valor durante la ejecución; la constante mantiene fijo su valor** Usar constantes con nombre evita «números mágicos» y mejora el mantenimiento.

*Referencia: §1.5 [MCCONNELL]*
</details>

---

### Pregunta 12

**En programación, ¿qué distingue a una expresión de una sentencia?**

A) La sentencia siempre ocupa una sola línea; la expresión, varias
B) Solo las expresiones pueden contener variables
C) Una expresión se evalúa y produce un valor; una sentencia se ejecuta y produce un efecto

<details><summary>Respuesta</summary>

**Correcta: C) Una expresión se evalúa y produce un valor; una sentencia se ejecuta y produce un efecto** `x + 1` es expresión; `x = x + 1` es una sentencia de asignación.

*Referencia: §1.6 [SEBESTA]*
</details>

---

### Pregunta 13

**Un tipo de dato se define como:**

A) La cantidad de memoria RAM instalada en el equipo
B) Un conjunto de valores posibles junto con las operaciones permitidas sobre ellos
C) El nombre que damos a una variable

<details><summary>Respuesta</summary>

**Correcta: B) Un conjunto de valores posibles junto con las operaciones permitidas sobre ellos** El tipo acota valores, fija la memoria ocupada y permite detectar errores.

*Referencia: §2.1 [PIERCE]*
</details>

---

### Pregunta 14

**¿Cuál de los siguientes es un tipo de dato simple o primitivo?**

A) El registro (struct)
B) El array o vector
C) El booleano

<details><summary>Respuesta</summary>

**Correcta: C) El booleano** Booleano, entero, real y carácter son primitivos (atómicos); array y registro son estructurados.

*Referencia: §2.2 [SEBESTA]*
</details>

---

### Pregunta 15

**Los números reales se representan en los computadores según la norma:**

A) IEEE 754 (coma flotante), con precisión finita
B) ASCII de 7 bits
C) Complemento a dos exacto sin pérdida

<details><summary>Respuesta</summary>

**Correcta: A) IEEE 754 (coma flotante), con precisión finita** Por eso no todos los decimales son exactos y no se deben comparar reales con `=` directamente.

*Referencia: §2.2 [IEEE754]*
</details>

---

### Pregunta 16

**¿Por qué no conviene comparar dos números reales con el operador de igualdad `==`?**

A) Porque el operador `==` no existe para reales en ningún lenguaje
B) Porque los reales siempre son negativos
C) Porque su representación en coma flotante es aproximada; se compara si su diferencia es menor que una tolerancia

<details><summary>Respuesta</summary>

**Correcta: C) Porque su representación en coma flotante es aproximada; se compara si su diferencia es menor que una tolerancia** Se usa `|a − b| < ε` en lugar de `a == b`.

*Referencia: §2.2 [IEEE754]*
</details>

---

### Pregunta 17

**Para almacenar importes de dinero (tributos, tasas) sin errores de redondeo, se recomienda:**

A) Usar entero de céntimos o un tipo decimal exacto, no coma flotante
B) Usar siempre variables de tipo carácter
C) Usar coma flotante de doble precisión, que es exacta

<details><summary>Respuesta</summary>

**Correcta: A) Usar entero de céntimos o un tipo decimal exacto, no coma flotante** Un error de un céntimo por recibo, multiplicado por miles, es un problema contable real.

*Referencia: §2.2 [IEEE754]*
</details>

---

### Pregunta 18

**Un tipo enumerado (enum) como `ESTADO = {ABIERTO, EN_TRAMITE, RESUELTO}` sirve para:**

A) Almacenar números reales con muchos decimales
B) Definir un conjunto fijo de valores con nombre, mejorando la legibilidad frente a usar números
C) Reservar memoria dinámica en el montículo

<details><summary>Respuesta</summary>

**Correcta: B) Definir un conjunto fijo de valores con nombre, mejorando la legibilidad frente a usar números** Es un tipo definido por el usuario.

*Referencia: §2.3 [SEBESTA]*
</details>

---

### Pregunta 19

**La conversión de tipo que realiza automáticamente el lenguaje, normalmente ampliando de un tipo menor a uno mayor sin pérdida, se llama:**

A) Conversión implícita o coerción
B) Conversión explícita o cast forzado
C) Truncamiento manual

<details><summary>Respuesta</summary>

**Correcta: A) Conversión implícita o coerción** Ejemplo: en `3 + 2.5` el entero `3` se convierte a `3.0` automáticamente (widening).

*Referencia: §2.4 [SCOTT]*
</details>

---

### Pregunta 20

**Python es un lenguaje de tipado fuerte y dinámico. Esto significa que:**

A) El tipo se comprueba en compilación y permite mezclar tipos libremente
B) Controla las mezclas de tipos incoherentes (fuerte) y el tipo se asocia al valor y se comprueba en ejecución (dinámico)
C) No tiene tipos de datos

<details><summary>Respuesta</summary>

**Correcta: B) Controla las mezclas de tipos incoherentes (fuerte) y el tipo se asocia al valor y se comprueba en ejecución (dinámico)** Fuerte/débil y estático/dinámico son ejes independientes.

*Referencia: §2.4 [PIERCE]*
</details>

---

### Pregunta 21

**Los ejes «fuerte/débil» y «estático/dinámico» de un sistema de tipos:**

A) Son exactamente lo mismo expresado de dos formas
B) Solo se aplican a lenguajes compilados
C) Son independientes: uno mide cuán estricto es con las mezclas de tipos, el otro cuándo se comprueba el tipo

<details><summary>Respuesta</summary>

**Correcta: C) Son independientes: uno mide cuán estricto es con las mezclas de tipos, el otro cuándo se comprueba el tipo** Python es fuerte y dinámico; C es estático y relativamente débil.

*Referencia: §2.4 [PIERCE]*
</details>

---

### Pregunta 22

**En un lenguaje con división entera, ¿qué vale `resultado` tras `entero a=7; entero b=2; real resultado = a / b;`?**

A) 3.5, porque el resultado es real
B) Da error de compilación siempre
C) 3.0, porque la división se hace primero entre enteros (7/2=3) y luego se convierte a real

<details><summary>Respuesta</summary>

**Correcta: C) 3.0, porque la división se hace primero entre enteros (7/2=3) y luego se convierte a real** Para obtener 3.5 hay que convertir ANTES de dividir: `(real)a / b`.

*Referencia: §2.4 [SCOTT]*
</details>

---

### Pregunta 23

**El operador módulo (`mod`, `%`) devuelve:**

A) El resto de la división entera entre dos números
B) El cociente sin decimales
C) La potencia del primer número elevado al segundo

<details><summary>Respuesta</summary>

**Correcta: A) El resto de la división entera entre dos números** `n mod 2 == 0` comprueba si `n` es par; es un uso clásico de examen.

*Referencia: §3.1 [SEBESTA]*
</details>

---

### Pregunta 24

**¿Qué operador se usa para comprobar si un número `n` es par?**

A) `n / 2 == 0`
B) `n mod 2 == 0`
C) `n ^ 2 == 0`

<details><summary>Respuesta</summary>

**Correcta: B) `n mod 2 == 0`** Si el resto de dividir entre 2 es cero, el número es par.

*Referencia: §3.1 [SEBESTA]*
</details>

---

### Pregunta 25

**Los operadores relacionales (`<`, `>`, `==`, `!=`) devuelven un valor de tipo:**

A) Entero
B) Booleano (verdadero o falso)
C) Carácter

<details><summary>Respuesta</summary>

**Correcta: B) Booleano (verdadero o falso)** Comparan dos valores y producen el resultado de la comparación.

*Referencia: §3.2 [SEBESTA]*
</details>

---

### Pregunta 26

**El error de escribir `si (x = 5)` en lugar de `si (x == 5)` consiste en:**

A) Confundir el operador de asignación (`=`, guarda un valor) con el de comparación (`==`, pregunta si son iguales)
B) Usar un operador que no existe
C) Escribir un comentario mal cerrado

<details><summary>Respuesta</summary>

**Correcta: A) Confundir el operador de asignación (`=`, guarda un valor) con el de comparación (`==`, pregunta si son iguales)** En muchos lenguajes no da error de compilación y provoca un fallo lógico difícil de detectar.

*Referencia: §3.2 [SEBESTA]*
</details>

---

### Pregunta 27

**La evaluación en cortocircuito (short-circuit) en `a Y b` significa que:**

A) Siempre se evalúan ambos operandos antes de decidir
B) Si `a` es falso, `b` no se evalúa porque el resultado ya es falso
C) El operador `Y` se convierte en `O` automáticamente

<details><summary>Respuesta</summary>

**Correcta: B) Si `a` es falso, `b` no se evalúa porque el resultado ya es falso** Se aprovecha para proteger operaciones, p. ej. evitar una división por cero.

*Referencia: §3.2 [SEBESTA]*
</details>

---

### Pregunta 28

**¿Cuál es el resultado de la expresión `2 + 3 * 4` aplicando la precedencia habitual de operadores?**

A) 20
B) 24
C) 14

<details><summary>Respuesta</summary>

**Correcta: C) 14** La multiplicación tiene mayor precedencia que la suma: `3*4=12`, luego `2+12=14`. Los paréntesis alterarían el orden.

*Referencia: §3.4 [SEBESTA]*
</details>

---

### Pregunta 29

**La sentencia `x += 3` es equivalente a:**

A) `x = x + 3`
B) `x = 3`
C) `x = x * 3`

<details><summary>Respuesta</summary>

**Correcta: A) `x = x + 3`** Es una asignación compuesta que combina la suma con la asignación.

*Referencia: §3.3 [SEBESTA]*
</details>

---

### Pregunta 30

**En una expresión con varios operadores, ¿qué elemento fuerza siempre el orden de evaluación por encima de la precedencia?**

A) El operador de asignación
B) El operador módulo
C) Los paréntesis

<details><summary>Respuesta</summary>

**Correcta: C) Los paréntesis** Lo que está entre paréntesis se evalúa primero; en caso de duda, conviene usarlos para mayor legibilidad.

*Referencia: §3.4 [SEBESTA]*
</details>

---

### Pregunta 31

**Según el teorema de Böhm-Jacopini (1966), cualquier algoritmo puede escribirse combinando únicamente:**

A) Compiladores, intérpretes y ensambladores
B) Secuencia, selección e iteración
C) Variables, constantes y punteros

<details><summary>Respuesta</summary>

**Correcta: B) Secuencia, selección e iteración** Es el fundamento de la programación estructurada, que evita el `goto` (Dijkstra, 1968).

*Referencia: §4.1 [BOHM66]*
</details>

---

### Pregunta 32

**¿Por qué la programación estructurada desaconseja el uso de la instrucción `goto`?**

A) Porque el `goto` es más lento de ejecutar
B) Porque el `goto` no existe en ningún lenguaje moderno
C) Porque genera «código espagueti» difícil de leer y mantener (Dijkstra, 1968)

<details><summary>Respuesta</summary>

**Correcta: C) Porque genera «código espagueti» difícil de leer y mantener (Dijkstra, 1968)** Un programa estructurado tiene un único punto de entrada y de salida por bloque.

*Referencia: §4.1 [DIJKSTRA68]*
</details>

---

### Pregunta 33

**La estructura de selección múltiple `segun` / `switch` / `case` es preferible a muchos `si` encadenados cuando:**

A) Se decide sobre los distintos valores discretos de una misma expresión
B) Solo hay dos caminos posibles
C) No se conoce ninguna condición

<details><summary>Respuesta</summary>

**Correcta: A) Se decide sobre los distintos valores discretos de una misma expresión** Es más legible; la rama `por_defecto` captura los valores no contemplados.

*Referencia: §4.2 [SEBESTA]*
</details>

---

### Pregunta 34

**En un `switch` de lenguajes como C o Java, olvidar el `break` al final de cada caso provoca:**

A) Un error de compilación inmediato
B) Que el programa se detenga
C) Que la ejecución «caiga» (fall-through) al siguiente caso

<details><summary>Respuesta</summary>

**Correcta: C) Que la ejecución «caiga» (fall-through) al siguiente caso** Es un error frecuente; el `break` corta la ejecución del caso.

*Referencia: §4.2 [SEBESTA]*
</details>

---

### Pregunta 35

**¿Cuál es la diferencia entre un bucle `mientras` (while) y un `repetir…hasta` (do-while)?**

A) El `mientras` comprueba la condición antes (puede ejecutarse 0 veces); el `repetir…hasta` la comprueba después (se ejecuta al menos 1 vez)
B) El `mientras` se ejecuta siempre exactamente 10 veces
C) No hay ninguna diferencia entre ellos

<details><summary>Respuesta</summary>

**Correcta: A) El `mientras` comprueba la condición antes (puede ejecutarse 0 veces); el `repetir…hasta` la comprueba después (se ejecuta al menos 1 vez)** El primero es precondicional; el segundo, postcondicional.

*Referencia: §4.3 [SEBESTA]*
</details>

---

### Pregunta 36

**El bucle `para` (for) es el más adecuado cuando:**

A) La condición no puede evaluarse nunca
B) Se conoce de antemano el número de repeticiones
C) Se quiere ejecutar el cuerpo una única vez seguro

<details><summary>Respuesta</summary>

**Correcta: B) Se conoce de antemano el número de repeticiones** Integra inicialización, condición e incremento del contador.

*Referencia: §4.3 [SEBESTA]*
</details>

---

### Pregunta 37

**¿Cuántas veces se ejecuta el cuerpo de `i = 5; mientras (i < 5) hacer … i = i + 1; fin_mientras`?**

A) 0 veces, porque la condición `5 < 5` es falsa de entrada
B) 5 veces
C) Infinitas veces

<details><summary>Respuesta</summary>

**Correcta: A) 0 veces, porque la condición `5 < 5` es falsa de entrada** El `mientras` es precondicional; comprueba antes de entrar.

*Referencia: §4.3 [SEBESTA]*
</details>

---

### Pregunta 38

**Un bucle infinito se produce cuando:**

A) El bucle tiene demasiadas iteraciones definidas
B) La condición de continuación nunca llega a hacerse falsa (p. ej. se olvida incrementar el contador)
C) Se usa un bucle `para` con contador

<details><summary>Respuesta</summary>

**Correcta: B) La condición de continuación nunca llega a hacerse falsa (p. ej. se olvida incrementar el contador)** Es un error grave que cuelga el programa.

*Referencia: §4.3 [SEBESTA]*
</details>

---

### Pregunta 39

**Toda función recursiva correctamente construida debe tener:**

A) Al menos tres parámetros
B) Una variable global compartida
C) Un caso base (condición de parada) y un caso recursivo que se acerque a él

<details><summary>Respuesta</summary>

**Correcta: C) Un caso base (condición de parada) y un caso recursivo que se acerque a él** Sin caso base, la recursión es infinita y desborda la pila (stack overflow).

*Referencia: §4.4 [ABELSON]*
</details>

---

### Pregunta 40

**¿Qué ocurre si una función recursiva carece de caso base o nunca lo alcanza?**

A) El compilador la convierte automáticamente en iterativa
B) Se produce recursión infinita que agota la pila de llamadas (stack overflow)
C) Devuelve siempre el valor 0

<details><summary>Respuesta</summary>

**Correcta: B) Se produce recursión infinita que agota la pila de llamadas (stack overflow)** Cada llamada pendiente ocupa un marco en la pila.

*Referencia: §4.4 [CLRS]*
</details>

---

### Pregunta 41

**Comparando recursividad e iteración para el mismo problema:**

A) La recursión nunca puede sustituirse por iteración
B) La iteración siempre da resultados incorrectos
C) Todo algoritmo recursivo puede reescribirse de forma iterativa; la recursión suele ser más elegante pero consume más memoria (marcos de pila)

<details><summary>Respuesta</summary>

**Correcta: C) Todo algoritmo recursivo puede reescribirse de forma iterativa; la recursión suele ser más elegante pero consume más memoria (marcos de pila)** La iteración es más eficiente en memoria.

*Referencia: §4.4 [CLRS]*
</details>

---

### Pregunta 42

**¿Qué valor devuelve `factorial(4)` según la definición `factorial(n) = n * factorial(n-1)`, con caso base `factorial(1) = 1`?**

A) 24
B) 10
C) 12

<details><summary>Respuesta</summary>

**Correcta: A) 24** `4 * 3 * 2 * 1 = 24`. Se apilan 4 llamadas y se desenrollan desde el caso base.

*Referencia: §4.4 [ABELSON]*
</details>

---

### Pregunta 43

**¿Cuál es la diferencia entre una función y un procedimiento?**

A) El procedimiento solo puede tener un parámetro
B) La función se ejecuta más rápido siempre
C) La función devuelve un valor (se usa en una expresión); el procedimiento no devuelve valor, actúa por sus efectos

<details><summary>Respuesta</summary>

**Correcta: C) La función devuelve un valor (se usa en una expresión); el procedimiento no devuelve valor, actúa por sus efectos** Muchos lenguajes los unifican como funciones que devuelven `void`.

*Referencia: §4.5 [ABELSON]*
</details>

---

### Pregunta 44

**Los beneficios de la programación modular (dividir el programa en subprogramas) incluyen:**

A) Reutilización, legibilidad, mantenimiento y prueba independiente, con alta cohesión y bajo acoplamiento
B) Aumentar el número de líneas de código para que parezca más completo
C) Impedir el uso de funciones y procedimientos

<details><summary>Respuesta</summary>

**Correcta: A) Reutilización, legibilidad, mantenimiento y prueba independiente, con alta cohesión y bajo acoplamiento** Es aplicar «divide y vencerás» al diseño del software.

*Referencia: §4.5 [MCCONNELL]*
</details>

---

### Pregunta 45

**En el paso de parámetros, el «parámetro formal» es:**

A) El valor concreto que se pasa en la llamada
B) La variable que aparece en la definición del subprograma
C) Un tipo de dato primitivo

<details><summary>Respuesta</summary>

**Correcta: B) La variable que aparece en la definición del subprograma** El valor concreto de la llamada es el «argumento» o parámetro real.

*Referencia: §4.6 [SCOTT]*
</details>

---

### Pregunta 46

**Si un procedimiento `duplica(x) { x = x * 2 }` recibe la variable `a = 10` por VALOR, tras la llamada `duplica(a)`:**

A) `a` sigue valiendo 10, porque se duplicó una copia y el original no cambia
B) `a` pasa a valer 20
C) `a` queda sin valor definido

<details><summary>Respuesta</summary>

**Correcta: A) `a` sigue valiendo 10, porque se duplicó una copia y el original no cambia** Por referencia, en cambio, `a` pasaría a valer 20.

*Referencia: §4.6 [SCOTT]*
</details>

---

### Pregunta 47

**En el paso por referencia, a diferencia del paso por valor:**

A) Nunca se pueden modificar los datos del llamador
B) Se copia el argumento y el original queda intacto
C) Se pasa la dirección de la variable, por lo que el subprograma puede modificar el original

<details><summary>Respuesta</summary>

**Correcta: C) Se pasa la dirección de la variable, por lo que el subprograma puede modificar el original** En C se emula con punteros; permite devolver varios resultados.

*Referencia: §4.6 [SCOTT]*
</details>

---

### Pregunta 48

**El ámbito (scope) de una variable se refiere a:**

A) La cantidad de memoria que ocupa
B) El número de veces que cambia de valor
C) La región del programa donde la variable es visible y puede usarse

<details><summary>Respuesta</summary>

**Correcta: C) La región del programa donde la variable es visible y puede usarse** Puede ser local (dentro de un subprograma) o global (todo el programa).

*Referencia: §4.7 [SCOTT]*
</details>

---

### Pregunta 49

**Una variable local declarada `static` en C tiene:**

A) Ámbito global y tiempo de vida local
B) Ámbito local (solo visible en su función) pero tiempo de vida global (conserva su valor entre llamadas)
C) Ni ámbito ni tiempo de vida

<details><summary>Respuesta</summary>

**Correcta: B) Ámbito local (solo visible en su función) pero tiempo de vida global (conserva su valor entre llamadas)** Ámbito (dónde es visible) y tiempo de vida (cuánto existe) son conceptos distintos.

*Referencia: §4.7 [SCOTT]*
</details>

---

### Pregunta 50

**Las variables locales automáticas de un subprograma se ubican en la memoria denominada:**

A) Pila (stack): nacen al entrar en el subprograma y mueren al salir
B) Montículo (heap) reservado con `new`
C) Registro del procesador exclusivamente

<details><summary>Respuesta</summary>

**Correcta: A) Pila (stack): nacen al entrar en el subprograma y mueren al salir** La memoria dinámica (con `new`/`malloc`) va al montículo (heap).

*Referencia: §4.7 [SCOTT]*
</details>

---

### Pregunta 51

**Un array (vector) se caracteriza por:**

A) Agrupar campos de tipos distintos accedidos por nombre
B) No tener un orden definido entre sus elementos
C) Ser una colección de elementos del mismo tipo, contiguos en memoria y accesibles por índice en tiempo O(1)

<details><summary>Respuesta</summary>

**Correcta: C) Ser una colección de elementos del mismo tipo, contiguos en memoria y accesibles por índice en tiempo O(1)** El acceso directo por índice es su gran ventaja.

*Referencia: §5.1 [KNUTH1]*
</details>

---

### Pregunta 52

**Acceder a `array[i]` con un índice `i` fuera del rango declarado:**

A) Siempre devuelve el valor 0 sin problemas
B) Es un error grave: en C corrompe memoria; en Java/Python lanza una excepción (IndexOutOfBounds)
C) Amplía automáticamente el tamaño del array

<details><summary>Respuesta</summary>

**Correcta: B) Es un error grave: en C corrompe memoria; en Java/Python lanza una excepción (IndexOutOfBounds)** Hay que respetar los límites del array.

*Referencia: §5.1 [KNUTH1]*
</details>

---

### Pregunta 53

**¿Cuál es la diferencia esencial entre un array y un registro?**

A) El array agrupa elementos del mismo tipo accedidos por índice; el registro agrupa campos de tipos distintos accedidos por nombre
B) El array no cabe en memoria y el registro sí
C) El registro solo puede tener un campo

<details><summary>Respuesta</summary>

**Correcta: A) El array agrupa elementos del mismo tipo accedidos por índice; el registro agrupa campos de tipos distintos accedidos por nombre** Un array de registros combina ambos.

*Referencia: §5.2 [KNUTH1]*
</details>

---

### Pregunta 54

**El Padrón Municipal (con dni, nombre, fecha de nacimiento y distrito de cada habitante) se modela de forma natural como:**

A) Un único número entero muy grande
B) Un array (o lista) de registros «Habitante», donde cada habitante es un registro
C) Una constante booleana

<details><summary>Respuesta</summary>

**Correcta: B) Un array (o lista) de registros «Habitante», donde cada habitante es un registro** Es el paso previo a persistirlo en una base de datos relacional (T17/T19).

*Referencia: §5.2 [KNUTH1]*
</details>

---

### Pregunta 55

**La búsqueda binaria (dicotómica) sobre un array:**

A) Funciona sobre cualquier array, esté ordenado o no
B) Es más lenta que la búsqueda secuencial
C) Requiere que el array esté ordenado y tiene coste O(log n), más rápida que la secuencial O(n)

<details><summary>Respuesta</summary>

**Correcta: C) Requiere que el array esté ordenado y tiene coste O(log n), más rápida que la secuencial O(n)** Divide el rango a la mitad en cada paso.

*Referencia: §5.3 [CLRS]*
</details>

---

### Pregunta 56

**El principio DRY (Don't Repeat Yourself) en buenas prácticas de programación consiste en:**

A) No repetir código, factorizando lo común en funciones reutilizables
B) Repetir el código tres veces para asegurar que funciona
C) Documentar cada línea con un comentario

<details><summary>Respuesta</summary>

**Correcta: A) No repetir código, factorizando lo común en funciones reutilizables** Junto con KISS (mantenlo simple) y YAGNI, mejora la mantenibilidad.

*Referencia: §6.2 [MCCONNELL]*
</details>

---

### Pregunta 57

**Un «error lógico» en un programa se caracteriza por:**

A) Impedir que el programa compile
B) Detener el programa con un mensaje del sistema operativo
C) Que el programa se ejecuta sin fallar pero produce un resultado incorrecto; es el más difícil de detectar

<details><summary>Respuesta</summary>

**Correcta: C) Que el programa se ejecuta sin fallar pero produce un resultado incorrecto; es el más difícil de detectar** Se caza con pruebas (testing); se distingue del error de compilación y del de ejecución.

*Referencia: §6.3 [KP]*
</details>

---

### Pregunta 58

**Las pruebas que comprueban una función o módulo de forma aislada se denominan:**

A) Pruebas de aceptación del usuario
B) Pruebas unitarias
C) Pruebas de sistema completo

<details><summary>Respuesta</summary>

**Correcta: B) Pruebas unitarias** Las de integración comprueban módulos juntos; las de sistema/aceptación, el conjunto frente a los requisitos.

*Referencia: §6.3 [KP]*
</details>

---

### Pregunta 59

**El «tipado gradual» (type hints en Python, TypeScript sobre JavaScript) es una tendencia que busca:**

A) Añadir anotaciones de tipo opcionales a lenguajes dinámicos para detectar errores antes sin perder flexibilidad
B) Eliminar todos los tipos de datos de los lenguajes
C) Convertir todos los lenguajes en ensamblador

<details><summary>Respuesta</summary>

**Correcta: A) Añadir anotaciones de tipo opcionales a lenguajes dinámicos para detectar errores antes sin perder flexibilidad** Acerca lo mejor del tipado estático y del dinámico.

*Referencia: §7 [SCOTT]*
</details>

---

### Pregunta 60

**Respecto a las tendencias actuales (seguridad de memoria, concurrencia, IA), los fundamentos del tema (tipos, operadores, estructuras de control, modularidad):**

A) Han quedado obsoletos y ya no se usan
B) Siguen plenamente vigentes por debajo de todas esas tendencias
C) Solo se aplican a lenguajes de bajo nivel

<details><summary>Respuesta</summary>

**Correcta: B) Siguen plenamente vigentes por debajo de todas esas tendencias** Rust, WebAssembly o los asistentes de IA se apoyan en los mismos fundamentos.

*Referencia: §7 [SEBESTA]*
</details>
