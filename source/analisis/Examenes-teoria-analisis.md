---
type: reference
goal: g-master
tags: [uni, maquinas, mymt, examenes, teoria]
date: 2026-11-15
related: [T2-examenes-analisis.md, examenes-teoria.json]
---
# MyMT: qué preguntas de teoría repiten los exámenes

Hecho por el droid ex-teoria el 15 nov 2026. Datos: `Uni/Maquinas/examenes-teoria.json`. PEI1 = T1+T2 (mar 17 nov 2026). PEC2 = T1+T3.

## 0. Lo esencial

- 1281 preguntas de teoría leídas en todos los PDF de la carpeta (y 2 copias oficiales). Quedan 491 preguntas distintas tras quitar las casi idénticas.
- Casi todo el material son bancos de estudiantes que se copian entre sí. Por eso el recuento bruto engaña: usa las preguntas distintas.
- El examen real de nov 2025 repite poco: solo 2 de sus 18 preguntas aparecen en otra fuente. No esperes preguntas copiadas; estudia los conceptos.
- Las respuestas vienen de marcas de otros alumnos (negrita, verde). No son oficiales. Donde las marcas chocan, lo digo.

## 1. Totales por tema

| Tema | Preguntas (bruto) | Preguntas distintas |
|---|---|---|
| T2 MCIA | 790 | 301 |
| T3 vapor/gas/ciclos | 209 | 102 |
| T1 fundamentos | 282 | 88 |
| Total | 1281 | 491 |

Parcial: PEI1 (solo T2) 790; "ambos" (T1) 292; PEC2 (T3) 192; sin clasificar 7. El tema lo puso el droid por el contenido; en los exámenes de 2012 el "Tema 3" es nuestro T2.

## 2. Temas por número de preguntas

Clasificación por palabras clave (aproximada). "Distintas" = tras quitar repetidas. Ordenado por distintas.

| # | Tema (concepto) | Distintas | Bruto |
|---|---|---|---|
| 1 | Pistón, biela, cigüeñal, culata, mecanismo | 75 | 186 |
| 2 | Combustión MEC / Diesel | 64 | 124 |
| 3 | Combustión MEP / Otto | 60 | 157 |
| 4 | Turbina de gas / Brayton / turbohélice | 53 | 110 |
| 5 | Fundamentos / clasificación de máquinas y motores | 49 | 159 |
| 6 | ηv, pme, par, potencia, dosado, rendimientos MCIA | 35 | 90 |
| 7 | Turbina de vapor / Rankine | 31 | 51 |
| 8 | Emisiones y contaminantes MCIA | 29 | 89 |
| 9 | Otros / sin clasificar | 28 | 75 |
| 10 | Sobrealimentación / turbocompresor | 21 | 77 |
| 11 | Refrigeración y lubricación MCIA | 20 | 50 |
| 12 | Ciclos teóricos de aire MCIA | 18 | 60 |
| 13 | Ciclo combinado y cogeneración | 8 | 53 |

Por tema y asunto (distintas): T2 pistón y mecanismo 73; T2 MEC 55; T2 MEP 53; T3 turbina de gas 39; T1 fundamentos 37; T2 ηv/pme/par 26; T3 turbina de vapor 22; T2 emisiones 22; T2 refrigeración 17; T2 sobrealimentación 15; T2 ciclos de aire 15; T3 ciclo combinado/cogeneración 8.

## 3. Tipos de pregunta

Tipo de formato (columna `type` del JSON): casi todo es test de elegir una opción.

| Formato | Preguntas |
|---|---|
| elegir una | 1193 |
| numérica corta | 35 |
| concepto V/F | 34 |
| diagrama/figura | 16 |
| fórmula | 3 |

Tipo de enunciado (heurística por palabras; "distintas" quita repetidas):

| # | Tipo | Distintas | Bruto | Ejemplo |
|---|---|---|---|---|
| 1 | completar la frase (característica de un sistema) | 193 | 490 | "El fluido motor de una máquina de fluido:" |
| 2 | otras (pregunta abierta de elegir) | 56 | 143 | "¿Qué condiciones se toman para calcular el rendimiento volumétrico en un motor de aspiración natural?" |
| 3 | cuál de los siguientes (clasificar / elegir) | 34 | 113 | "¿En cuál de los siguientes motores basados en turbomáquinas no tiene sentido utilizar un condensador?" |
| 4 | tendencia / efecto de un cambio | 28 | 59 | "¿Qué sistema mecánico que se usa para aumentar la entalpia del fluido que lo atraviesa permite motores caudale" |
| 5 | elegir la falsa / la que NO | 26 | 88 | "¿Cuál de los siguientes motores basados en turbomáquinas no permite cogeneración?" |
| 6 | qué motor / máquina para una aplicación | 25 | 78 | "¿Con cuál de estos motores térmicos se puede hacer cogeneración sin pérdida de energía mecánica útil?" |
| 7 | cálculo corto | 19 | 26 | "¿Cuántas máquinas térmicas diferentes se pueden encontrar en un turbohélice?" |
| 8 | V/F | 18 | 18 | "Las turbinas de gas suelen tener una mezcla de aire-combustible globalmente cerca de la estequiometría o inclu" |
| 9 | identificar parte / función de un componente | 16 | 72 | "¿Cuál de los siguientes conjuntos de elementos mecánicos es una máquina térmica generadora?" |
| 10 | definición / nombre de un concepto | 13 | 31 | "La parte de la biela asociada a la muñequilla del cigüeñal se denomina:" |
| 11 | identificar figura/esquema | 13 | 16 | "¿A qué compresor corresponde la siguiente figura? [figura: foto de un compresor de tornillo (dos rotores helic" |
| 12 | causa / por qué | 12 | 32 | "¿Por qué los motores Wankel no se han consolidado en el campo de la automoción?" |
| 13 | opción combinada (a y b / todas / ninguna) | 11 | 26 | "El diagrama del indicador es" |
| 14 | valor / orden de magnitud | 9 | 35 | "¿Cuántas máquinas térmicas diferentes se pueden encontrar en un turbohélice*?" |
| 15 | en qué fase / momento / lugar | 8 | 19 | "Cuando se inicia la combustión en un MMPE en modo de mezcla pobre:" |
| 16 | afirmación verdadera entre varias | 4 | 7 | "Señalar la afirmación verdadera" |
| 17 | objetivo / para qué sirve | 3 | 10 | "La recirculación de los gases de escape (EGR) en los MCIA tiene como objetivo:" |
| 18 | condiciones de referencia | 2 | 15 | "¿Qué condiciones de referencia se toman para calcular el rendimiento volumétrico en un motor turboalimentado (" |
| 19 | fórmula | 1 | 3 | "El trabajo interno (o indicado) realizado por el fluido en cada ciclo de un motor de combustión interna altern" |

Lectura: la mayoría son "completa la frase con la característica correcta" de un sistema (MEC, MEP, refrigeración). Siguen "cuál de los siguientes" (clasificar), "elegir la falsa / la que NO", "qué motor sirve para X" e "identificar la parte de un componente". Hay pocos cálculos cortos y casi ninguna fórmula.

## 4. Grupos de preguntas casi idénticas

Fuentes copiadas: Ejemplo Moodle y Extraordinario jul 2020 tienen las mismas preguntas en gran parte; los bancos (Tema1/2/3, tests1motores, TEST PARTE 1, Compilación, Recopilatorio) las copian. Lista de los 30 grupos con más fuentes distintas. Respuesta = la más marcada (marcas a favor / total). No es oficial.

| Grupo | Fuentes | Exámenes reales | Pregunta | Respuesta (marcas) |
|---|---|---|---|---|
| C001 | 7 (17 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿En cuál de los siguientes motores basados en turbomáquinas no tiene sentido utilizar un conden | todas las alternativas propuestas la permiten (9/14) |
| C002 | 7 (13 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Cuál de los siguientes conjuntos de elementos mecánicos no es ni incluye una máquina térmica m | compresor tornillo (11/11) |
| C003 | 7 (13 apar.) | Ejemplo Moodle, Extraord. jul 2020 | El conjunto de elementos mecánicos que transforma hidrógeno en energía mecánica es: | un motor térmico (9/10) |
| C004 | 7 (12 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Cuántas máquinas térmicas diferentes se pueden encontrar en un ciclo combinado con configuraci | 2 (9/9) |
| C005 | 7 (11 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Cuál es un motor de combustión externa? | turbina de vapor (10/10) |
| C006 | 7 (11 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Con cuál de estos motores térmicos se puede hacer cogeneración sin pérdida de energía mecánica | turbina de vapor (5/9) |
| C007 | 6 (16 apar.) | Pruebas 2012 | El fluido motor de una máquina térmica | puede ser compresible o incompresible (11/16) |
| C008 | 6 (13 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Cuál es una parte del pistón de un MCIA? | alojamiento del bulón (3/10) |
| C009 | 6 (13 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Qué condiciones de referencia se toman para calcular el rendimiento volumétrico en un motor tu | presión y temperatura ambientales (10/10) |
| C010 | 6 (12 apar.) | Ejemplo Moodle, Extraord. jul 2020 | A igualdad del resto de parámetros, si la turbina de gas de ciclo simple A [tiene] mayor relaci | la turbina b tiene mayor relación de compresión (6/9) |
| C011 | 6 (11 apar.) | Pruebas 2012 | Una máquina térmica motora (expansora) transforma | energía térmica en energía mecánica (11/11) |
| C012 | 6 (10 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿En qué ciclo es habitual encontrarse una mayor presión de admisión de la turbina? | turbina de vapor (7/7) |
| C013 | 6 (10 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Cuál es verdadera? | la combustión en un mcia se inicia durante la carr (6/7) |
| C014 | 6 (10 apar.) | Ejemplo Moodle, Extraord. jul 2020 | ¿Qué combustible no se puede consumir en un MEP? | biodiésel (8/8) |
| C015 | 6 (10 apar.) | Ejemplo Moodle, Extraord. jul 2020 | Una disminución en la temperatura del vapor vivo de un ciclo de vapor simple, a igualdad del re | menor rendimiento térmico del ciclo (6/7) |
| C016 | 6 (7 apar.) | Extraord. jul 2020 | ¿Con cuál de estos motores térmicos no se puede hacer cogeneración usando energías térmicas res | turbina de vapor (4/5) |
| C017 | 6 (7 apar.) | Extraord. jul 2020 | ¿Cuál no es un motor de combustión externa? | turborreactor (5/5) |
| C018 | 6 (7 apar.) | - | ¿Qué emisión se produce a altas temperaturas con escasez O2? (opciones b-e en el original; falt | co (3/5) |
| C019 | 6 (7 apar.) | Ejemplo Moodle, Extraord. jul 2020 | Suponiendo siempre el mismo gasto de vapor a la entrada de la turbina de alta, una turbina de v | mayor humedad a la salida de turbina aumentando la (6/6) |
| C020 | 6 (6 apar.) | Pruebas 2012 | ¿Por qué no está extendido el uso de TG en automoción? | por su bajo rendimiento en condiciones de funciona (6/6) |
| C021 | 6 (6 apar.) | Pruebas 2012 | En una máquina térmica generadora (compresora), el fluido que la atraviesa: | aumenta su potencial exergético (6/6) |
| C022 | 6 (6 apar.) | Pruebas 2012 | Las turbinas de gas de ciclo abierto: | se usan en aviación por su elevada potencia especí (5/5) |
| C023 | 6 (6 apar.) | Pruebas 2012 | Las turbinas de gas de ciclo abierto: | tienen mayor fiabilidad mecánica que los mcia (5/6) |
| C024 | 6 (6 apar.) | Pruebas 2012 | En lo que se refiere a potencia específica, ¿cuál es la secuencia correcta? | tg>mcia>tv (6/6) |
| C025 | 6 (6 apar.) | Pruebas 2012 | En lo que se refiere a rendimiento térmico, ¿cuál es la secuencia correcta? | cc>mec>tg (6/6) |
| C026 | 6 (6 apar.) | Pruebas 2012 | Señalar el motor térmico que puede alcanzar mayor rendimiento térmico: | motor diesel (5/5) |
| C027 | 6 (6 apar.) | Pruebas 2012 | ¿Por qué los motores Wankel no se han consolidado en el campo de la automoción? | no han podido ser homologados por la normativa ant (4/5) |
| C028 | 6 (6 apar.) | Pruebas 2012 | Señalar la información verdadera: | los motores wankel realizan tres procesos de combu (5/5) |
| C029 | 6 (6 apar.) | Pruebas 2012 | ¿Qué ventajas ofrece el ciclo cerrado respecto al ciclo abierto en un MCE? | aumentan tanto el rendimiento térmico como la pote (6/6) |
| C030 | 6 (6 apar.) | Pruebas 2012 | El criterio de diseño actual de los motores térmicos es: | obtener las menores emisiones locales (6/6) |

## 5. Las 15 preguntas más repetidas

Orden: más fuentes distintas, luego más apariciones. Se salta C013 (mezcla dos preguntas con el mismo enunciado).

### 1. (C001, T3, 17 apariciones en 7 fuentes)
Pregunta: ¿En cuál de los siguientes motores basados en turbomáquinas no tiene sentido utilizar un condensador?
- a) Turbina de gas.
- b) Ciclo combinado.
- c) En todas las alternativas propuestas tiene sentido.
- d) Turbina de vapor.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: todas las alternativas propuestas la permiten (9 de 14 marcas).

### 2. (C002, T1, 13 apariciones en 7 fuentes)
Pregunta: ¿Cuál de los siguientes conjuntos de elementos mecánicos no es ni incluye una máquina térmica motora?
- a) Grupo Turbo (contiene una turbina y un compresor)
- b) Compresor Tornillo
- c) Turbina Centrípeta
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: compresor tornillo (11 de 11 marcas).

### 3. (C003, T1, 13 apariciones en 7 fuentes)
Pregunta: El conjunto de elementos mecánicos que transforma hidrógeno en energía mecánica es:
- a) Una máquina térmica.
- b) Una pila de combustible.
- c) Un motor térmico.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: un motor térmico (9 de 10 marcas).

### 4. (C004, T3, 12 apariciones en 7 fuentes)
Pregunta: ¿Cuántas máquinas térmicas diferentes se pueden encontrar en un ciclo combinado con configuración 1x1?
- a) 3.
- b) 2.
- c) 1.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: 2 (9 de 9 marcas).

### 5. (C005, T1, 11 apariciones en 7 fuentes)
Pregunta: ¿Cuál es un motor de combustión externa?
- a) Turbina de gas (ciclo abierto).
- b) Turbina de vapor.
- c) Motor Wankel.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: turbina de vapor (10 de 10 marcas).

### 6. (C006, T3, 11 apariciones en 7 fuentes)
Pregunta: ¿Con cuál de estos motores térmicos se puede hacer cogeneración sin pérdida de energía mecánica útil?
- a) Turbina de gas de ciclo abierto.
- b) Máquina de vapor.
- c) Turbina de vapor.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: turbina de vapor (5 de 9 marcas). **Marcas en conflicto: comprueba con las diapositivas.**

### 7. (C007, T1, 16 apariciones en 6 fuentes)
Pregunta: El fluido motor de una máquina térmica
- Debe ser siempre compresible [y se comporta como tal]
- Puede ser compresible o incompresible
- Puede ser compresible, pero comportarse como incompresible
Exámenes reales: Pruebas 2012. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: puede ser compresible o incompresible (11 de 16 marcas).

### 8. (C008, T2, 13 apariciones en 6 fuentes)
Pregunta: ¿Cuál es una parte del pistón de un MCIA?
- a) Segmento.
- b) Asiento de la válvula.
- c) Alojamiento del bulón.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema2, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución.
Respuesta más marcada: alojamiento del bulón (3 de 10 marcas). **Marcas en conflicto: comprueba con las diapositivas.**

### 9. (C009, T2, 13 apariciones en 6 fuentes)
Pregunta: ¿Qué condiciones de referencia se toman para calcular el rendimiento volumétrico en un motor turboalimentado (mecánicamente) sin postenfriamiento?
- a) Presión y temperatura ambientales
- b) Presión y temperatura detrás del compresor centrífugo
- c) Presión y temperatura detrás de la turbina centrípeta
- d) Presión y temperatura detrás del grupo turbo
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema2, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución.
Respuesta más marcada: presión y temperatura ambientales (10 de 10 marcas).

### 10. (C010, T3, 12 apariciones en 6 fuentes)
Pregunta: A igualdad del resto de parámetros, si la turbina de gas de ciclo simple A [tiene] mayor relación de compresión que la turbina B (también de ciclo simple): [figura manuscrita: curvas W y η vs P2/P1 con A, B, B' y desigualdades]
- a. La turbina B tiene mayor temperatura de escape.
- b. La turbina B tiene mayor rendimiento de ciclo.
- c. La turbina A tiene mayor temperatura de escape
- d. La turbina A tiene mayor rendimiento de ciclo.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema3, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución.
Respuesta más marcada: la turbina b tiene mayor relación de compresión (6 de 9 marcas).

### 11. (C011, T1, 11 apariciones en 6 fuentes)
Pregunta: Una máquina térmica motora (expansora) transforma
- a) Energía asociada a la materia en energía mecánica.
- b) Energía térmica en energía mecánica
- c) Energía química en energía mecánica.
Exámenes reales: Pruebas 2012. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: energía térmica en energía mecánica (11 de 11 marcas).

### 12. (C012, T3, 10 apariciones en 6 fuentes)
Pregunta: ¿En qué ciclo es habitual encontrarse una mayor presión de admisión de la turbina?
- a) Suelen ser parecidas.
- b) Turbina de gas.
- c) Turbina de vapor.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema3, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución.
Respuesta más marcada: turbina de vapor (7 de 7 marcas).

### 13. (C014, T2, 10 apariciones en 6 fuentes)
Pregunta: ¿Qué combustible no se puede consumir en un MEP?
- a) Biodiésel.
- b) Gas natural.
- c) Biogas.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema2, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución.
Respuesta más marcada: biodiésel (8 de 8 marcas).

### 14. (C015, T3, 10 apariciones en 6 fuentes)
Pregunta: Una disminución en la temperatura del vapor vivo de un ciclo de vapor simple, a igualdad del resto de parámetros, implica:
- a) Menor presión de salida de turbina.
- b) Menor rendimiento interno de turbina.
- c) Menor rendimiento térmico del ciclo.
Exámenes reales: Ejemplo Moodle, Extraord. jul 2020. Bancos: Banco Tema3, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución.
Respuesta más marcada: menor rendimiento térmico del ciclo (6 de 7 marcas).

### 15. (C016, T3, 7 apariciones en 6 fuentes)
Pregunta: ¿Con cuál de estos motores térmicos no se puede hacer cogeneración usando energías térmicas residuales?
- a) Turbina de gas de ciclo abierto.
- b) Ciclo combinado.
- c) Turbina de vapor.
Exámenes reales: Extraord. jul 2020. Bancos: Banco Tema1, Compilación Preguntas PEC1 y PEC2, Recopilatorio tests PEC1 (+PEC1 2022), TEST PARTE 1 con solución, tests1motores.
Respuesta más marcada: turbina de vapor (4 de 5 marcas).

## 6. Cómo puntúa cada examen

| Examen | Teoría | Problemas |
|---|---|---|
| Extraordinario 8 jul 2020 y Ejemplo Moodle | 20 min; +1 acierto; −1/3 (4 opciones), −1/2 (3), −1 (2); blanco 0 | 75 min; +1; fallo 0; blanco 0 |
| Pruebas 2012 (fotos) | +1; −0,5; en pruebas con "inadmisible": −1 si falla esa opción; blanco 0 (blanco inadmisible −0,5) | no consta |
| PEC1 2025, PEC1 2022, enero 2024 | sin cabecera con reglas en el archivo | no consta |
Regla práctica (curso 2025-26, sin confirmar en estos archivos): usa la del Ejemplo Moodle: fallar quita 1/(n−1).

## 7. Lo que casi no aparece

Búsqueda por palabras en las 1281 preguntas. Cero apariciones: ciclo Atkinson/Miller, common rail, turbo-compound, ciclo Ericsson, motor cohete, válvula desmodrómica, números de Mach/Reynolds, ley de Dalton, cinemática biela-manivela, equilibrado y vibraciones, HCCI/RCCI, postcombustión. Una sola o dos: ciclo orgánico (ORC), energía solar, estatorreactor, ciclos supercríticos, coeficiente de dilatación. Cálculos cortos: solo 35 (unos 19 distintos). Fórmulas: 3.

## 8. Límites

- Agrupar preguntas y clasificar tema/tipo se hizo con reglas automáticas. Puede haber grupos mezclados (C013) o preguntas iguales sin unir.
- Las opciones cambian de letra entre versiones: las respuestas se comparan por el texto de la opción, no por la letra.
- Pruebas 2012: programa antiguo; varias respuestas ocultas por casillas negras (sin solución).
- Páginas sin contenido: portadas y anuncios de Wuolah. Sin páginas ilegibles. Archivos sin preguntas de teoría: problemas manuscritos, formularios y apuntes (ver report.md).