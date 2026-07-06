# Tema 18 — Changelog

> **Título oficial**: Lenguajes de programación. Tipos de datos. Operadores. Instrucciones condicionales. Bucles y recursividad. Procedimientos, funciones y parámetros. Vectores y registros. Estructura de un programa.

---

## v1.0 — 2026-07-06 — Primera versión

**Estado**: pendiente de validación por María y Ana, y de revisión técnica del IAM (Jesús Cuadrado).

**Motivo**: desarrollo del Tema 18, dentro de la serie de temas técnicos generados desde cero (tras T13, T14, T15, T16 y T17), replicando la estructura y el formato de los Temas 1, 11 y 17 ya consolidados, con pestaña Índice y listas anidadas correctas desde el inicio.

### Alcance de la v1.0

| Entregable | Cantidad |
|---|---|
| Contenido teórico | ~13.500 palabras · 7 secciones del esqueleto oficial con 26 epígrafes |
| Diagramas SVG inline | 12 (accesibles con `role`/`aria-label`, clases con sufijo único anti-colisión) |
| Banco de preguntas tipo test | 60 preguntas A/B/C con explicación y referencia, balanceadas **20/20/20** |
| Casos prácticos | 3 (cálculo de tasa / tipos y control; censo del Padrón / arrays y registros; expedientes / recursividad y parámetros) · 10 puntos cada uno |
| Fuentes Tier 1 | 14 referencias canónicas (Sebesta, Scott, Aho-Sethi-Ullman, Pratt, Pierce, Böhm-Jacopini, Dijkstra, Knuth, CLRS, Abelson-Sussman, McConnell, Kernighan-Pike, IEEE 754, ISO C) |

### Decisiones de generación

1. **Sin material de cliente**: solo el esqueleto `Test_Prompting/temas junio/18.md`. Desarrollado desde fuentes canónicas de lenguajes de programación, todas referenciadas.
2. **Estructura fiel al esqueleto oficial**: siete secciones H2 (Lenguajes; Tipos de datos; Operadores; Estructuras de control con la modularidad anidada; Estructuras de datos básicas; Estructura de un programa; Tendencias actuales). Se corrigieron erratas menores del esqueleto de partida (dobles espacios en varios encabezados; falta de puntuación homogénea).
3. **Ejemplos en pseudocódigo neutro en castellano** (decisión de Joan): estilo de oposición agnóstico de lenguaje (`si … fin_si`, `mientras`, `para`, `funcion … devolver`); cuando se ilustra una particularidad real se nombra el lenguaje (C, Java, Python, JavaScript) sin atar el tema a ninguno.
4. **Profundidad ampliada** (decisión de Joan): frente a un temario mínimo se añadió material de alto valor de examen —teorema de Böhm-Jacopini y `goto` de Dijkstra, dos ejes del sistema de tipos (fuerte/débil × estático/dinámico), precisión IEEE 754 y dinero, cortocircuito lógico, traza de recursión, pila vs montículo, coste O(1)/O(n)/O(log n), programación defensiva y siglas DRY/KISS/YAGNI.
5. **Sección «Tendencias actuales» con marco duradero** (decisión de Joan, punto 4 no especificado → resuelto): seguridad de memoria (Rust), tipado gradual (TypeScript, type hints), rasgos funcionales, concurrencia, WebAssembly, IA/low-code — **sin números de versión volátiles** que caduquen en examen, y subrayando que los fundamentos siguen vigentes.
6. **Contexto Ayuntamiento de Madrid** en casos y ejemplos (Padrón, tributos/IBI, expedientes, tasas, 21 distritos).
7. **Frontera con temas vecinos** cuidada: algoritmos y estructuras de datos abstractas al T13; representación binaria de la información al T11; POO al T20; SQL al T19; lenguajes web/script al T23; seguridad en el desarrollo al T25.
8. **Referencias cruzadas validadas contra BOAM 10.032**: T11, T13, T17, T19, T20, T23, T25. Todas comprobadas.
9. **Anti-colisión de SVG**: las clases CSS de cada diagrama llevan **sufijo numérico único** (`.t1`…`.t12`), evitando el bug sistémico de estilos que leakean entre los 12 SVG embebidos en la misma página (lección de T5).

### Pendientes para QA / próxima iteración

- Validación de profundidad por María/Ana/IAM (¿alguna sección a ampliar o recortar?).
- Confirmación del estilo de pseudocódigo (neutro en castellano) frente a alternativas (snippets reales, un lenguaje concreto).
- Verificación ortográfica con corrector es_ES (cuidado con falsos positivos por términos técnicos en inglés: array, string, struct, stack, heap, switch, break…).

### Origen

Generado el 2026-07-06 en el flujo de trabajo de eTrivium, replicando el patrón de los Temas 1 (v2.1), 11 (v3.2), 13 (v1.1), 14 (v1.0), 15 (v1.0), 16 (v1.0) y 17 (v1.0). `build_t18.py` y `_build_css.txt` persistidos en el repo.
