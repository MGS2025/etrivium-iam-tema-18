# Tema 18 — Catálogo de Diagramas

> **Título oficial**: Lenguajes de programación. Tipos de datos. Operadores. Instrucciones condicionales. Bucles y recursividad. Procedimientos, funciones y parámetros. Vectores y registros. Estructura de un programa.
>
> **Versión**: v1.0
> **Fecha**: 2026-07-06
> **Autor**: ETRIVIUM
> **Formato**: SVG inline (zero-dependencias, escalable, imprimible, accesible con role/aria-label)
> **Paleta**: Ayuntamiento de Madrid #0055a0 (primario) + #d13c3c (alertas) + #2d8659 (ventajas) + #e89822 (callouts)
> **Nota técnica**: las clases CSS de cada SVG llevan sufijo numérico único (`.t1`, `.h1`…) para evitar colisiones de estilos entre los 12 diagramas embebidos en la misma página.

---

## Índice de diagramas

| ID | Título | Sección | Tipo | Formato |
|---|---|---|---|---|
| D1 | Niveles y generaciones de lenguajes | §1.2 | Escala | 660×320 |
| D2 | Compilador frente a intérprete | §1.2 | Flujo | 680×300 |
| D3 | Sintaxis, semántica y pragmática | §1.4 | Bloques | 660×300 |
| D4 | Clasificación de los tipos de datos | §2.1 | Árbol | 680×320 |
| D5 | Sistema de tipos: dos ejes | §2.4 | Matriz | 640×360 |
| D6 | Las tres estructuras de control | §4.1 | Comparativa | 680×300 |
| D7 | Tipos de bucle | §4.3 | Comparativa | 680×320 |
| D8 | Recursividad: pila del factorial | §4.4 | Pila | 640×340 |
| D9 | Memoria: pila y montículo | §4.7 | Estructura | 660×320 |
| D10 | Paso por valor y por referencia | §4.6 | Comparativa | 680×300 |
| D11 | Array frente a registro | §5.2 | Comparativa | 680×320 |
| D12 | Estructura de un programa | §6.1 | Bloques | 640×340 |

---

## D1 · Niveles y generaciones de lenguajes

**Sección**: §1.2 — Evolución y clasificación de los lenguajes
**Propósito**: Situar los lenguajes del más cercano a la máquina (1GL) al más cercano al humano (5GL).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 660 320" role="img" aria-label="Escala de generaciones de lenguajes desde lenguaje máquina de bajo nivel hasta lenguajes de quinta generación de alto nivel">
  <style>.t1{font:700 13px system-ui,sans-serif;fill:#fff}.s1{font:11px system-ui,sans-serif;fill:#fff}.l1{font:11px system-ui,sans-serif;fill:#444}.h1{font:700 13px system-ui,sans-serif;fill:#0055a0}</style>
  <text x="330" y="26" text-anchor="middle" class="h1">De la máquina al humano: generaciones de lenguajes</text>
  <rect x="150" y="44" width="400" height="42" rx="5" fill="#003d73"/><text x="350" y="62" text-anchor="middle" class="t1">1GL · Lenguaje máquina (binario)</text><text x="350" y="78" text-anchor="middle" class="s1">Ceros y unos · dependiente de la CPU</text>
  <rect x="150" y="92" width="400" height="42" rx="5" fill="#0055a0"/><text x="350" y="110" text-anchor="middle" class="t1">2GL · Ensamblador (mnemónicos)</text><text x="350" y="126" text-anchor="middle" class="s1">MOV, ADD, JMP · aún ligado a la máquina</text>
  <rect x="150" y="140" width="400" height="42" rx="5" fill="#3778b5"/><text x="350" y="158" text-anchor="middle" class="t1">3GL · Alto nivel estructurado (C, Java)</text><text x="350" y="174" text-anchor="middle" class="s1">Se dice CÓMO · independiente de la máquina</text>
  <rect x="150" y="188" width="400" height="42" rx="5" fill="#6ea3d2"/><text x="350" y="206" text-anchor="middle" class="t1">4GL · Declarativo (SQL, informes)</text><text x="350" y="222" text-anchor="middle" class="s1">Se dice QUÉ, no cómo</text>
  <rect x="150" y="236" width="400" height="42" rx="5" fill="#9cc3e0"/><text x="350" y="254" text-anchor="middle" style="font:700 13px system-ui;fill:#123">5GL · Lógico / IA (Prolog)</text><text x="350" y="270" text-anchor="middle" style="font:11px system-ui;fill:#123">Restricciones y reglas · el motor deduce</text>
  <text x="40" y="66" class="l1">▼ bajo nivel</text>
  <text x="40" y="258" class="l1">▲ alto nivel</text>
  <text x="650" y="308" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: PRATT, cap. 1]</text>
</svg>
```

---

## D2 · Compilador frente a intérprete

**Sección**: §1.2 — Formas de traducción
**Propósito**: Contrastar la traducción completa previa (compilador) con la traducción línea a línea (intérprete).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Comparación entre compilador que traduce todo el código a ejecutable antes de ejecutar e intérprete que traduce y ejecuta instrucción a instrucción">
  <style>.t2{font:700 12px system-ui,sans-serif;fill:#fff}.b2{font:600 11px system-ui,sans-serif;fill:#123}.l2{font:11px system-ui,sans-serif;fill:#444}.h2{font:700 13px system-ui,sans-serif;fill:#0055a0}</style>
  <text x="170" y="24" text-anchor="middle" class="h2">COMPILADOR</text>
  <rect x="60" y="40" width="90" height="40" rx="5" fill="#9cc3e0"/><text x="105" y="64" text-anchor="middle" class="b2">Código fuente</text>
  <rect x="180" y="40" width="90" height="40" rx="5" fill="#0055a0"/><text x="225" y="60" text-anchor="middle" class="t2">Compilador</text><text x="225" y="74" text-anchor="middle" class="t2">(traduce todo)</text>
  <rect x="300" y="40" width="90" height="40" rx="5" fill="#2d8659"/><text x="345" y="64" text-anchor="middle" class="t2">Ejecutable</text>
  <path d="M150 60 L178 60" stroke="#888" stroke-width="2" marker-end="url(#a2)"/>
  <path d="M270 60 L298 60" stroke="#888" stroke-width="2" marker-end="url(#a2)"/>
  <text x="225" y="102" text-anchor="middle" class="l2">Se traduce UNA vez; luego se ejecuta muchas · rápido</text>
  <line x1="40" y1="130" x2="640" y2="130" stroke="#ccc" stroke-dasharray="4 4"/>
  <text x="170" y="162" text-anchor="middle" class="h2">INTÉRPRETE</text>
  <rect x="60" y="178" width="90" height="40" rx="5" fill="#9cc3e0"/><text x="105" y="202" text-anchor="middle" class="b2">Código fuente</text>
  <rect x="200" y="178" width="110" height="40" rx="5" fill="#e89822"/><text x="255" y="198" text-anchor="middle" class="t2">Intérprete</text><text x="255" y="212" text-anchor="middle" class="t2">línea a línea</text>
  <rect x="360" y="178" width="90" height="40" rx="5" fill="#2d8659"/><text x="405" y="202" text-anchor="middle" class="t2">Resultado</text>
  <path d="M150 198 L198 198" stroke="#888" stroke-width="2" marker-end="url(#a2)"/>
  <path d="M310 198 L358 198" stroke="#888" stroke-width="2" marker-end="url(#a2)"/>
  <text x="255" y="240" text-anchor="middle" class="l2">Traduce y ejecuta a la vez · portable · más lento</text>
  <text x="255" y="262" text-anchor="middle" class="l2">Híbrido (Java): fuente → bytecode → máquina virtual (JVM)</text>
  <defs><marker id="a2" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#888"/></marker></defs>
  <text x="670" y="292" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: SEBESTA, cap. 1]</text>
</svg>
```

---

## D3 · Sintaxis, semántica y pragmática

**Sección**: §1.4 — Los tres niveles de descripción de un lenguaje
**Propósito**: Separar la forma (sintaxis), el significado (semántica) y el uso (pragmática).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 660 300" role="img" aria-label="Tres niveles de un lenguaje: sintaxis como forma o gramática, semántica como significado, pragmática como uso práctico">
  <style>.t3{font:700 13px system-ui,sans-serif;fill:#fff}.s3{font:11px system-ui,sans-serif;fill:#fff}.l3{font:11px system-ui,sans-serif;fill:#444}.h3{font:700 13px system-ui,sans-serif;fill:#0055a0}</style>
  <text x="330" y="26" text-anchor="middle" class="h3">Cómo se describe un lenguaje de programación</text>
  <rect x="40" y="48" width="180" height="130" rx="8" fill="#0055a0"/><text x="130" y="76" text-anchor="middle" class="t3">SINTAXIS</text><text x="130" y="100" text-anchor="middle" class="s3">La FORMA</text><text x="130" y="122" text-anchor="middle" class="s3">Reglas gramaticales</text><text x="130" y="140" text-anchor="middle" class="s3">(BNF): qué está</text><text x="130" y="156" text-anchor="middle" class="s3">bien escrito</text>
  <rect x="240" y="48" width="180" height="130" rx="8" fill="#2d8659"/><text x="330" y="76" text-anchor="middle" class="t3">SEMÁNTICA</text><text x="330" y="100" text-anchor="middle" class="s3">El SIGNIFICADO</text><text x="330" y="122" text-anchor="middle" class="s3">Qué hace cada</text><text x="330" y="140" text-anchor="middle" class="s3">construcción al</text><text x="330" y="156" text-anchor="middle" class="s3">ejecutarse</text>
  <rect x="440" y="48" width="180" height="130" rx="8" fill="#e89822"/><text x="530" y="76" text-anchor="middle" class="t3">PRAGMÁTICA</text><text x="530" y="100" text-anchor="middle" class="s3">El USO</text><text x="530" y="122" text-anchor="middle" class="s3">Estilo, legibilidad,</text><text x="530" y="140" text-anchor="middle" class="s3">buenas prácticas</text><text x="530" y="156" text-anchor="middle" class="s3">(no la impone la gramática)</text>
  <text x="130" y="206" text-anchor="middle" class="l3">Falta un `;` →</text><text x="130" y="222" text-anchor="middle" class="l3">error de sintaxis</text>
  <text x="330" y="206" text-anchor="middle" class="l3">Dividir por 0 →</text><text x="330" y="222" text-anchor="middle" class="l3">error semántico</text>
  <text x="530" y="206" text-anchor="middle" class="l3">Nombres claros →</text><text x="530" y="222" text-anchor="middle" class="l3">buen estilo</text>
  <text x="650" y="288" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: ASU, cap. 1]</text>
</svg>
```

---

## D4 · Clasificación de los tipos de datos

**Sección**: §2.1 — Concepto y clasificación
**Propósito**: Distinguir tipos simples de estructurados y ver ejemplos de cada uno.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Árbol de clasificación de tipos de datos: simples o primitivos (entero, real, carácter, booleano) y estructurados (array, registro, cadena, conjunto)">
  <style>.t4{font:700 12px system-ui,sans-serif;fill:#fff}.s4{font:11px system-ui,sans-serif;fill:#123}.l4{font:11px system-ui,sans-serif;fill:#444}.h4{font:700 13px system-ui,sans-serif;fill:#0055a0}</style>
  <text x="340" y="24" text-anchor="middle" class="h4">Tipos de datos</text>
  <rect x="280" y="38" width="120" height="34" rx="6" fill="#0055a0"/><text x="340" y="60" text-anchor="middle" class="t4">TIPO DE DATO</text>
  <path d="M340 72 L200 100" stroke="#888" stroke-width="1.5"/><path d="M340 72 L480 100" stroke="#888" stroke-width="1.5"/>
  <rect x="120" y="100" width="160" height="34" rx="6" fill="#2d8659"/><text x="200" y="122" text-anchor="middle" class="t4">SIMPLES / PRIMITIVOS</text>
  <rect x="400" y="100" width="160" height="34" rx="6" fill="#e89822"/><text x="480" y="122" text-anchor="middle" class="t4">ESTRUCTURADOS</text>
  <rect x="70" y="152" width="100" height="30" rx="4" fill="#d7e6f4"/><text x="120" y="172" text-anchor="middle" class="s4">Entero</text>
  <rect x="70" y="188" width="100" height="30" rx="4" fill="#d7e6f4"/><text x="120" y="208" text-anchor="middle" class="s4">Real (IEEE 754)</text>
  <rect x="70" y="224" width="100" height="30" rx="4" fill="#d7e6f4"/><text x="120" y="244" text-anchor="middle" class="s4">Carácter</text>
  <rect x="70" y="260" width="100" height="30" rx="4" fill="#d7e6f4"/><text x="120" y="280" text-anchor="middle" class="s4">Booleano</text>
  <rect x="200" y="152" width="90" height="30" rx="4" fill="#d7e6f4"/><text x="245" y="172" text-anchor="middle" class="s4">atómicos,</text>
  <rect x="200" y="188" width="90" height="30" rx="4" fill="#d7e6f4"/><text x="245" y="208" text-anchor="middle" class="s4">indivisibles</text>
  <rect x="420" y="152" width="110" height="30" rx="4" fill="#fbe9cf"/><text x="475" y="172" text-anchor="middle" class="s4">Array / vector</text>
  <rect x="420" y="188" width="110" height="30" rx="4" fill="#fbe9cf"/><text x="475" y="208" text-anchor="middle" class="s4">Registro / struct</text>
  <rect x="420" y="224" width="110" height="30" rx="4" fill="#fbe9cf"/><text x="475" y="244" text-anchor="middle" class="s4">Cadena (string)</text>
  <rect x="420" y="260" width="110" height="30" rx="4" fill="#fbe9cf"/><text x="475" y="280" text-anchor="middle" class="s4">Conjunto, fichero</text>
  <rect x="558" y="188" width="110" height="30" rx="4" fill="#fbe9cf"/><text x="613" y="208" text-anchor="middle" class="s4">agrupan varios</text>
  <text x="670" y="312" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: SEBESTA, cap. 6]</text>
</svg>
```

---

## D5 · Sistema de tipos: dos ejes

**Sección**: §2.4 — Conversión y compatibilidad de tipos
**Propósito**: Separar los dos ejes independientes (estático/dinámico y fuerte/débil) con ejemplos.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 360" role="img" aria-label="Matriz de dos ejes del sistema de tipos: eje horizontal fuerte a débil, eje vertical estático a dinámico, con Java, C, Python y JavaScript ubicados">
  <style>.l5{font:11px system-ui,sans-serif;fill:#444}.h5{font:700 13px system-ui,sans-serif;fill:#0055a0}.a5{font:700 12px system-ui,sans-serif;fill:#0055a0}.c5{font:600 12px system-ui,sans-serif;fill:#123}</style>
  <text x="320" y="24" text-anchor="middle" class="h5">Los dos ejes del sistema de tipos (independientes)</text>
  <line x1="120" y1="70" x2="120" y2="320" stroke="#0055a0" stroke-width="2" marker-end="url(#a5)"/>
  <line x1="120" y1="320" x2="560" y2="320" stroke="#0055a0" stroke-width="2" marker-end="url(#a5)"/>
  <text x="112" y="66" text-anchor="end" class="a5">estático</text>
  <text x="112" y="316" text-anchor="end" class="a5">dinámico</text>
  <text x="128" y="66" class="l5">(tipo en compilación)</text>
  <text x="128" y="316" class="l5">(tipo en ejecución)</text>
  <text x="150" y="340" class="a5">fuerte</text>
  <text x="560" y="340" text-anchor="end" class="a5">débil</text>
  <rect x="150" y="90" width="150" height="60" rx="8" fill="#d7e6f4" stroke="#0055a0"/><text x="225" y="116" text-anchor="middle" class="c5">JAVA</text><text x="225" y="136" text-anchor="middle" class="l5">estático + fuerte</text>
  <rect x="380" y="90" width="150" height="60" rx="8" fill="#fbe9cf" stroke="#e89822"/><text x="455" y="116" text-anchor="middle" class="c5">C</text><text x="455" y="136" text-anchor="middle" class="l5">estático + más débil</text>
  <rect x="150" y="240" width="150" height="60" rx="8" fill="#d7ecd9" stroke="#2d8659"/><text x="225" y="266" text-anchor="middle" class="c5">PYTHON</text><text x="225" y="286" text-anchor="middle" class="l5">dinámico + fuerte</text>
  <rect x="380" y="240" width="150" height="60" rx="8" fill="#f6d9d9" stroke="#d13c3c"/><text x="455" y="266" text-anchor="middle" class="c5">JAVASCRIPT</text><text x="455" y="286" text-anchor="middle" class="l5">dinámico + débil</text>
  <defs><marker id="a5" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#0055a0"/></marker></defs>
  <text x="630" y="352" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: PIERCE; SEBESTA cap. 6]</text>
</svg>
```

---

## D6 · Las tres estructuras de control

**Sección**: §4.1 — Teorema de Böhm-Jacopini
**Propósito**: Las tres únicas estructuras necesarias: secuencia, selección e iteración.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Las tres estructuras de control de la programación estructurada: secuencia, selección con dos ramas e iteración con bucle de retorno">
  <style>.t6{font:700 12px system-ui,sans-serif;fill:#0055a0}.b6{font:600 11px system-ui,sans-serif;fill:#fff}.l6{font:11px system-ui,sans-serif;fill:#444}.h6{font:700 13px system-ui,sans-serif;fill:#0055a0}</style>
  <text x="340" y="22" text-anchor="middle" class="h6">Böhm-Jacopini (1966): tres estructuras bastan</text>
  <text x="110" y="52" text-anchor="middle" class="t6">1 · SECUENCIA</text>
  <rect x="70" y="64" width="80" height="26" rx="4" fill="#0055a0"/><text x="110" y="81" text-anchor="middle" class="b6">paso A</text>
  <rect x="70" y="98" width="80" height="26" rx="4" fill="#0055a0"/><text x="110" y="115" text-anchor="middle" class="b6">paso B</text>
  <rect x="70" y="132" width="80" height="26" rx="4" fill="#0055a0"/><text x="110" y="149" text-anchor="middle" class="b6">paso C</text>
  <path d="M110 90 L110 98" stroke="#888" marker-end="url(#a6)"/><path d="M110 124 L110 132" stroke="#888" marker-end="url(#a6)"/>
  <text x="110" y="182" text-anchor="middle" class="l6">Una tras otra</text>
  <text x="340" y="52" text-anchor="middle" class="t6">2 · SELECCIÓN</text>
  <polygon points="340,64 380,86 340,108 300,86" fill="#e89822"/><text x="340" y="90" text-anchor="middle" class="b6">¿cond?</text>
  <rect x="258" y="128" width="70" height="26" rx="4" fill="#2d8659"/><text x="293" y="145" text-anchor="middle" class="b6">verdadero</text>
  <rect x="352" y="128" width="70" height="26" rx="4" fill="#d13c3c"/><text x="387" y="145" text-anchor="middle" class="b6">falso</text>
  <path d="M320 100 L293 128" stroke="#888" marker-end="url(#a6)"/><path d="M360 100 L387 128" stroke="#888" marker-end="url(#a6)"/>
  <text x="340" y="182" text-anchor="middle" class="l6">Elige un camino (si / segun)</text>
  <text x="575" y="52" text-anchor="middle" class="t6">3 · ITERACIÓN</text>
  <polygon points="575,64 615,86 575,108 535,86" fill="#e89822"/><text x="575" y="90" text-anchor="middle" class="b6">¿cond?</text>
  <rect x="540" y="128" width="70" height="26" rx="4" fill="#0055a0"/><text x="575" y="145" text-anchor="middle" class="b6">cuerpo</text>
  <path d="M575 108 L575 128" stroke="#888" marker-end="url(#a6)"/>
  <path d="M610 141 C660 141 660 86 617 86" stroke="#2d8659" stroke-width="1.5" fill="none" marker-end="url(#a6)"/>
  <text x="575" y="182" text-anchor="middle" class="l6">Repite mientras se cumpla</text>
  <rect x="60" y="210" width="560" height="30" rx="6" fill="#f2f2f2"/><text x="340" y="230" text-anchor="middle" class="l6">La programación estructurada usa SOLO estas tres · evita el `goto` (Dijkstra, 1968)</text>
  <defs><marker id="a6" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#888"/></marker></defs>
  <text x="670" y="288" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: BOHM66; DIJKSTRA68]</text>
</svg>
```

---

## D7 · Tipos de bucle

**Sección**: §4.3 — Bucles e iteraciones
**Propósito**: Distinguir precondicional (while), postcondicional (do-while) y con contador (for).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Comparación de tres bucles: mientras precondicional que puede ejecutarse cero veces, repetir hasta postcondicional que se ejecuta al menos una vez, y para con contador conocido">
  <style>.t7{font:700 12px system-ui,sans-serif;fill:#fff}.l7{font:11px system-ui,sans-serif;fill:#444}.h7{font:700 13px system-ui,sans-serif;fill:#0055a0}.k7{font:700 11px system-ui,sans-serif;fill:#d13c3c}</style>
  <text x="340" y="24" text-anchor="middle" class="h7">Tres tipos de bucle</text>
  <rect x="30" y="44" width="200" height="34" rx="6" fill="#0055a0"/><text x="130" y="66" text-anchor="middle" class="t7">MIENTRAS (while)</text>
  <text x="130" y="98" text-anchor="middle" class="l7">Comprueba ANTES</text>
  <text x="130" y="118" text-anchor="middle" class="k7">Puede ejecutarse 0 veces</text>
  <text x="130" y="140" text-anchor="middle" class="l7">precondicional</text>
  <rect x="40" y="158" width="180" height="90" rx="6" fill="#f2f6fb" stroke="#0055a0"/><text x="130" y="182" text-anchor="middle" class="l7">i = 1</text><text x="130" y="202" text-anchor="middle" class="l7">mientras (i &lt;= 10)</text><text x="130" y="222" text-anchor="middle" class="l7">   procesar(i)</text><text x="130" y="242" text-anchor="middle" class="l7">   i = i + 1</text>
  <rect x="240" y="44" width="200" height="34" rx="6" fill="#2d8659"/><text x="340" y="66" text-anchor="middle" class="t7">REPETIR…HASTA (do-while)</text>
  <text x="340" y="98" text-anchor="middle" class="l7">Comprueba DESPUÉS</text>
  <text x="340" y="118" text-anchor="middle" class="k7">Se ejecuta ≥ 1 vez</text>
  <text x="340" y="140" text-anchor="middle" class="l7">postcondicional</text>
  <rect x="250" y="158" width="180" height="90" rx="6" fill="#f2faf5" stroke="#2d8659"/><text x="340" y="188" text-anchor="middle" class="l7">repetir</text><text x="340" y="210" text-anchor="middle" class="l7">   opcion = leer()</text><text x="340" y="232" text-anchor="middle" class="l7">hasta (opcion = salir)</text>
  <rect x="450" y="44" width="200" height="34" rx="6" fill="#e89822"/><text x="550" y="66" text-anchor="middle" class="t7">PARA (for)</text>
  <text x="550" y="98" text-anchor="middle" class="l7">Con CONTADOR</text>
  <text x="550" y="118" text-anchor="middle" class="k7">Nº de vueltas conocido</text>
  <text x="550" y="140" text-anchor="middle" class="l7">init · condición · incremento</text>
  <rect x="460" y="158" width="180" height="90" rx="6" fill="#fdf6ec" stroke="#e89822"/><text x="550" y="192" text-anchor="middle" class="l7">para i desde 1</text><text x="550" y="214" text-anchor="middle" class="l7">      hasta 21</text><text x="550" y="236" text-anchor="middle" class="l7">   procesar(i)</text>
  <rect x="60" y="266" width="560" height="30" rx="6" fill="#f2f2f2"/><text x="340" y="286" text-anchor="middle" class="l7">Un bucle sin avanzar hacia la salida = bucle infinito (cuelga el programa)</text>
  <text x="670" y="314" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: SEBESTA, cap. 8]</text>
</svg>
```

---

## D8 · Recursividad: pila del factorial

**Sección**: §4.4 — Recursividad
**Propósito**: Visualizar el apilamiento de llamadas de factorial(4) y su desenrollado desde el caso base.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 340" role="img" aria-label="Pila de llamadas de factorial de 4: se apilan factorial 4, 3, 2 y 1, el caso base factorial 1 devuelve 1 y se desenrolla multiplicando hasta 24">
  <style>.t8{font:700 12px system-ui,sans-serif;fill:#fff}.l8{font:11px system-ui,sans-serif;fill:#444}.h8{font:700 13px system-ui,sans-serif;fill:#0055a0}.g8{font:700 12px system-ui,sans-serif;fill:#2d8659}</style>
  <text x="320" y="24" text-anchor="middle" class="h8">factorial(4) — apilar (bajar) y desenrollar (subir)</text>
  <text x="150" y="52" text-anchor="middle" class="l8">① Llamadas que se apilan ↓</text>
  <rect x="70" y="64" width="160" height="30" rx="4" fill="#0055a0"/><text x="150" y="84" text-anchor="middle" class="t8">factorial(4) = 4 · …</text>
  <rect x="70" y="100" width="160" height="30" rx="4" fill="#0055a0"/><text x="150" y="120" text-anchor="middle" class="t8">factorial(3) = 3 · …</text>
  <rect x="70" y="136" width="160" height="30" rx="4" fill="#0055a0"/><text x="150" y="156" text-anchor="middle" class="t8">factorial(2) = 2 · …</text>
  <rect x="70" y="172" width="160" height="30" rx="4" fill="#d13c3c"/><text x="150" y="192" text-anchor="middle" class="t8">factorial(1) = 1 (BASE)</text>
  <path d="M150 94 L150 100" stroke="#888" marker-end="url(#a8)"/><path d="M150 130 L150 136" stroke="#888" marker-end="url(#a8)"/><path d="M150 166 L150 172" stroke="#888" marker-end="url(#a8)"/>
  <text x="470" y="52" text-anchor="middle" class="l8">② Resultados que suben ↑</text>
  <rect x="390" y="172" width="160" height="30" rx="4" fill="#2d8659"/><text x="470" y="192" text-anchor="middle" class="t8">devuelve 1</text>
  <rect x="390" y="136" width="160" height="30" rx="4" fill="#2d8659"/><text x="470" y="156" text-anchor="middle" class="t8">2 · 1 = 2</text>
  <rect x="390" y="100" width="160" height="30" rx="4" fill="#2d8659"/><text x="470" y="120" text-anchor="middle" class="t8">3 · 2 = 6</text>
  <rect x="390" y="64" width="160" height="30" rx="4" fill="#2d8659"/><text x="470" y="84" text-anchor="middle" class="t8">4 · 6 = 24</text>
  <path d="M470 172 L470 166" stroke="#2d8659" marker-end="url(#g8m)"/><path d="M470 136 L470 130" stroke="#2d8659" marker-end="url(#g8m)"/><path d="M470 100 L470 94" stroke="#2d8659" marker-end="url(#g8m)"/>
  <path d="M232 187 L388 187" stroke="#d13c3c" stroke-width="1.5" stroke-dasharray="4 3" marker-end="url(#r8)"/>
  <rect x="180" y="250" width="280" height="60" rx="8" fill="#fdf6ec" stroke="#e89822"/><text x="320" y="274" text-anchor="middle" class="g8">Resultado: 24</text><text x="320" y="296" text-anchor="middle" class="l8">Sin caso base → recursión infinita → desbordamiento de pila</text>
  <defs><marker id="a8" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#888"/></marker><marker id="g8m" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#2d8659"/></marker><marker id="r8" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#d13c3c"/></marker></defs>
  <text x="630" y="332" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: ABELSON; CLRS cap. 2]</text>
</svg>
```

---

## D9 · Memoria: pila y montículo

**Sección**: §4.7 — Ámbito y ciclo de vida
**Propósito**: Distinguir la pila (variables automáticas, marcos de llamada) del montículo (memoria dinámica).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 660 320" role="img" aria-label="Organización de la memoria de un programa: pila para variables locales automáticas y marcos de llamada, y montículo o heap para memoria dinámica reservada explícitamente">
  <style>.t9{font:700 12px system-ui,sans-serif;fill:#fff}.l9{font:11px system-ui,sans-serif;fill:#444}.h9{font:700 13px system-ui,sans-serif;fill:#0055a0}.s9{font:11px system-ui,sans-serif;fill:#fff}</style>
  <text x="330" y="24" text-anchor="middle" class="h9">Memoria de un programa en ejecución</text>
  <rect x="70" y="44" width="230" height="240" rx="8" fill="#f2f6fb" stroke="#0055a0"/>
  <text x="185" y="66" text-anchor="middle" class="h9">PILA (stack)</text>
  <rect x="90" y="78" width="190" height="40" rx="4" fill="#0055a0"/><text x="185" y="94" text-anchor="middle" class="t9">marco de main()</text><text x="185" y="110" text-anchor="middle" class="s9">variables locales</text>
  <rect x="90" y="124" width="190" height="40" rx="4" fill="#3778b5"/><text x="185" y="140" text-anchor="middle" class="t9">marco de calcular()</text><text x="185" y="156" text-anchor="middle" class="s9">parámetros + locales</text>
  <rect x="90" y="170" width="190" height="34" rx="4" fill="#6ea3d2"/><text x="185" y="191" text-anchor="middle" class="t9">marco de sumar()</text>
  <text x="185" y="228" text-anchor="middle" class="l9">Automática · nace y muere</text><text x="185" y="246" text-anchor="middle" class="l9">con la llamada · rápida</text><text x="185" y="264" text-anchor="middle" class="l9">Crece y decrece con LIFO</text>
  <rect x="360" y="44" width="230" height="240" rx="8" fill="#f2faf5" stroke="#2d8659"/>
  <text x="475" y="66" text-anchor="middle" class="h9">MONTÍCULO (heap)</text>
  <rect x="385" y="82" width="80" height="46" rx="4" fill="#2d8659"/><text x="425" y="102" text-anchor="middle" class="t9">objeto</text><text x="425" y="118" text-anchor="middle" class="s9">new/malloc</text>
  <rect x="485" y="100" width="80" height="46" rx="4" fill="#2d8659"/><text x="525" y="120" text-anchor="middle" class="t9">array</text><text x="525" y="136" text-anchor="middle" class="s9">dinámico</text>
  <rect x="410" y="158" width="90" height="42" rx="4" fill="#2d8659"/><text x="455" y="183" text-anchor="middle" class="t9">registro</text>
  <text x="475" y="228" text-anchor="middle" class="l9">Dinámica · se reserva y libera</text><text x="475" y="246" text-anchor="middle" class="l9">explícitamente (o recolector</text><text x="475" y="264" text-anchor="middle" class="l9">de basura) · tamaño variable</text>
  <text x="330" y="306" text-anchor="middle" class="l9">Ámbito = DÓNDE se ve la variable · Tiempo de vida = CUÁNTO existe en memoria</text>
  <text x="650" y="316" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: SCOTT, cap. 3]</text>
</svg>
```

---

## D10 · Paso por valor y por referencia

**Sección**: §4.6 — Parámetros y mecanismos de paso
**Propósito**: Mostrar por qué por valor no altera el original y por referencia sí.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 300" role="img" aria-label="Paso por valor copia el argumento y no cambia el original, paso por referencia pasa la dirección y sí modifica la variable original del llamador">
  <style>.t10{font:700 12px system-ui,sans-serif;fill:#fff}.l10{font:11px system-ui,sans-serif;fill:#444}.h10{font:700 13px system-ui,sans-serif;fill:#0055a0}.v10{font:700 12px system-ui,sans-serif;fill:#123}</style>
  <text x="340" y="22" text-anchor="middle" class="h10">duplica(x): { x = x · 2 }  con a = 10</text>
  <text x="170" y="50" text-anchor="middle" class="h10">POR VALOR</text>
  <rect x="70" y="62" width="90" height="46" rx="6" fill="#0055a0"/><text x="115" y="82" text-anchor="middle" class="t10">a = 10</text><text x="115" y="100" text-anchor="middle" class="t10">(llamador)</text>
  <rect x="230" y="62" width="90" height="46" rx="6" fill="#6ea3d2"/><text x="275" y="82" text-anchor="middle" class="t10">x = 10 → 20</text><text x="275" y="100" text-anchor="middle" class="t10">(copia)</text>
  <path d="M160 85 L228 85" stroke="#888" stroke-width="2" marker-end="url(#a10)"/><text x="194" y="78" text-anchor="middle" class="l10">copia</text>
  <text x="170" y="138" text-anchor="middle" class="v10" fill="#2d8659">a sigue valiendo 10 ✓</text>
  <text x="170" y="158" text-anchor="middle" class="l10">El original NO cambia</text>
  <line x1="360" y1="46" x2="360" y2="180" stroke="#ccc" stroke-dasharray="4 4"/>
  <text x="530" y="50" text-anchor="middle" class="h10">POR REFERENCIA</text>
  <rect x="430" y="62" width="90" height="46" rx="6" fill="#0055a0"/><text x="475" y="82" text-anchor="middle" class="t10">a = 10 → 20</text><text x="475" y="100" text-anchor="middle" class="t10">(llamador)</text>
  <rect x="590" y="62" width="80" height="46" rx="6" fill="#e89822"/><text x="630" y="82" text-anchor="middle" class="t10">x → dir(a)</text><text x="630" y="100" text-anchor="middle" class="t10">(referencia)</text>
  <path d="M590 85 L522 85" stroke="#d13c3c" stroke-width="2" marker-end="url(#r10)"/><text x="556" y="78" text-anchor="middle" class="l10">dirección</text>
  <text x="530" y="138" text-anchor="middle" class="v10" fill="#d13c3c">a pasa a valer 20 ⚠</text>
  <text x="530" y="158" text-anchor="middle" class="l10">El original SÍ cambia</text>
  <rect x="60" y="200" width="560" height="56" rx="8" fill="#f2f2f2"/><text x="340" y="222" text-anchor="middle" class="l10">Por valor = copia (seguro, el original intacto) · Por referencia = dirección (puede modificar el original</text><text x="340" y="242" text-anchor="middle" class="l10">y devolver varios resultados). En Java los primitivos van SIEMPRE por valor.</text>
  <defs><marker id="a10" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#888"/></marker><marker id="r10" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#d13c3c"/></marker></defs>
  <text x="670" y="292" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: SCOTT, cap. 8]</text>
</svg>
```

---

## D11 · Array frente a registro

**Sección**: §5.2 — Registros o estructuras
**Propósito**: Contrastar el array (homogéneo, por índice) con el registro (heterogéneo, por campo).

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 680 320" role="img" aria-label="Array como colección homogénea accedida por índice numérico frente a registro como colección heterogénea de campos accedidos por nombre">
  <style>.t11{font:700 12px system-ui,sans-serif;fill:#fff}.l11{font:11px system-ui,sans-serif;fill:#444}.h11{font:700 13px system-ui,sans-serif;fill:#0055a0}.i11{font:700 11px system-ui,sans-serif;fill:#0055a0}.c11{font:600 11px system-ui,sans-serif;fill:#123}</style>
  <text x="340" y="24" text-anchor="middle" class="h11">Array (índice)  vs  Registro (campo)</text>
  <text x="170" y="52" text-anchor="middle" class="h11">ARRAY / VECTOR</text>
  <text x="170" y="70" text-anchor="middle" class="l11">mismo tipo · acceso por índice v[i] · O(1)</text>
  <rect x="60" y="82" width="44" height="40" fill="#0055a0"/><rect x="104" y="82" width="44" height="40" fill="#0055a0"/><rect x="148" y="82" width="44" height="40" fill="#0055a0"/><rect x="192" y="82" width="44" height="40" fill="#0055a0"/><rect x="236" y="82" width="44" height="40" fill="#0055a0"/>
  <text x="82" y="107" text-anchor="middle" class="t11">149</text><text x="126" y="107" text-anchor="middle" class="t11">37</text><text x="170" y="107" text-anchor="middle" class="t11">72</text><text x="214" y="107" text-anchor="middle" class="t11">65</text><text x="258" y="107" text-anchor="middle" class="t11">88</text>
  <text x="82" y="138" text-anchor="middle" class="i11">[1]</text><text x="126" y="138" text-anchor="middle" class="i11">[2]</text><text x="170" y="138" text-anchor="middle" class="i11">[3]</text><text x="214" y="138" text-anchor="middle" class="i11">[4]</text><text x="258" y="138" text-anchor="middle" class="i11">[5]</text>
  <text x="170" y="166" text-anchor="middle" class="l11">poblacion[3] → 72 (directo)</text>
  <line x1="345" y1="44" x2="345" y2="250" stroke="#ccc" stroke-dasharray="4 4"/>
  <text x="520" y="52" text-anchor="middle" class="h11">REGISTRO / STRUCT</text>
  <text x="520" y="70" text-anchor="middle" class="l11">tipos distintos · acceso por nombre r.campo</text>
  <rect x="410" y="82" width="220" height="24" fill="#e89822"/><text x="420" y="99" class="c11">dni : cadena</text><text x="560" y="99" class="c11">"12345678Z"</text>
  <rect x="410" y="106" width="220" height="24" fill="#f0a94a"/><text x="420" y="123" class="c11">nombre : cadena</text><text x="560" y="123" class="c11">"Ana"</text>
  <rect x="410" y="130" width="220" height="24" fill="#e89822"/><text x="420" y="147" class="c11">edad : entero</text><text x="560" y="147" class="c11">34</text>
  <rect x="410" y="154" width="220" height="24" fill="#f0a94a"/><text x="420" y="171" class="c11">distrito : entero</text><text x="560" y="171" class="c11">1</text>
  <text x="520" y="196" text-anchor="middle" class="l11">ciudadano.edad → 34 (por campo)</text>
  <rect x="60" y="266" width="560" height="40" rx="8" fill="#f2f2f2"/><text x="340" y="290" text-anchor="middle" class="l11">Array de registros = tabla de datos (p. ej. el Padrón: una fila = un registro Habitante)</text>
  <text x="670" y="318" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: KNUTH1; K&amp;R cap. 6]</text>
</svg>
```

---

## D12 · Estructura de un programa

**Sección**: §6.1 — Organización del código
**Propósito**: Mostrar las partes típicas de un programa y el flujo de arranque en `main`.

```svg
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 340" role="img" aria-label="Partes de un programa: importaciones, declaraciones globales de constantes y tipos, definición de subprogramas y programa principal main que orquesta las llamadas">
  <style>.t12{font:700 12px system-ui,sans-serif;fill:#fff}.l12{font:11px system-ui,sans-serif;fill:#444}.h12{font:700 13px system-ui,sans-serif;fill:#0055a0}.s12{font:11px system-ui,sans-serif;fill:#fff}</style>
  <text x="320" y="24" text-anchor="middle" class="h12">Anatomía de un programa</text>
  <rect x="120" y="40" width="400" height="42" rx="6" fill="#6ea3d2"/><text x="320" y="60" text-anchor="middle" class="t12">1 · Importaciones / bibliotecas</text><text x="320" y="76" text-anchor="middle" class="s12">import, #include, using</text>
  <rect x="120" y="90" width="400" height="42" rx="6" fill="#3778b5"/><text x="320" y="110" text-anchor="middle" class="t12">2 · Declaraciones globales</text><text x="320" y="126" text-anchor="middle" class="s12">constantes (NUM_DISTRITOS = 21), tipos (Ciudadano)</text>
  <rect x="120" y="140" width="400" height="52" rx="6" fill="#0055a0"/><text x="320" y="160" text-anchor="middle" class="t12">3 · Subprogramas</text><text x="320" y="176" text-anchor="middle" class="s12">funciones y procedimientos</text><text x="320" y="190" text-anchor="middle" class="s12">alta cohesión · bajo acoplamiento</text>
  <rect x="120" y="200" width="400" height="52" rx="6" fill="#2d8659"/><text x="320" y="220" text-anchor="middle" class="t12">4 · Programa principal — main()</text><text x="320" y="236" text-anchor="middle" class="s12">PUNTO DE ENTRADA · orquesta las llamadas</text><text x="320" y="248" text-anchor="middle" class="s12">por aquí empieza la ejecución</text>
  <path d="M540 226 C600 226 600 161 522 161" stroke="#e89822" stroke-width="1.5" fill="none" marker-end="url(#a12)"/><text x="600" y="196" text-anchor="middle" class="l12">llama</text>
  <rect x="90" y="270" width="460" height="34" rx="6" fill="#f2f2f2"/><text x="320" y="291" text-anchor="middle" class="l12">Separar datos (tipos), lógica (funciones) y flujo (main) · un cambio, un solo sitio</text>
  <defs><marker id="a12" markerWidth="8" markerHeight="8" refX="4" refY="4" orient="auto"><path d="M0 0 L8 4 L0 8 z" fill="#e89822"/></marker></defs>
  <text x="630" y="332" text-anchor="end" style="font:11px system-ui;fill:#666">[Fuente: MCCONNELL, cap. 4]</text>
</svg>
```
