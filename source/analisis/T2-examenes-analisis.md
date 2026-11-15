---
type: reference
goal: g-master
tags: [uni, maquinas, mymt, t2, examenes]
date: 2026-11-15
related: [T1-contenido.md, T2-contenido.md]
source: "OneDrive UPM/Master/53001207-M3 .../materials/Examenes/texto/ (+ PDF para los escaneos a mano)"
---
# T2 (MCIA) y T1: qué preguntan los exámenes reales

PEI1 = martes 17 nov 2026, 08:30. Teoría = 2/3 (test, T1+T2). Problemas = 1/3 (test, solo T2).
Hecho por el droid t2-examenes el 15 nov 2026. Todo sale de los 11 archivos prioritarios del brief más algunos de apoyo.

## 0. Lo esencial (30 segundos)

1. Los problemas son siempre del mismo tipo de cadena: Ẇe, pme, ηv, dosado, gef, Ẇpm, balance de calor. Aprende 6 recetas (sección 3). Salen casi idénticas cada año.
2. En teoría T2 salen cada vez ~12 de 18 preguntas de T2 (2025, 2022). Las preguntas se repiten entre exámenes casi con las mismas palabras (sección 4).
3. Los temas con más peso: ciclos teóricos y diagrama indicador, MEP vs MEC (combustibles, rc, regulación), mecanismo y partes, pme/par/potencia, ηv y sus condiciones de referencia, refrigeración, balance de energía.
4. Respuestas: casi todo el material NO trae solución en las preguntas de teoría. Marcado "sin solución" donde no hay. Los problemas sí traen solución (las compruebo con Python).

## 1. Fuentes y qué traen

| Archivo | Qué es | T2 | Solución |
|---|---|---|---|
| PEC1_Teoria_20_11_2025 | PEC1 teoría, 20 nov 2025, 18 preguntas | 12 de 18 (+1 emisiones TG) | sin solución |
| PEC1_Problemas_20_11_2025 | PEC1 problemas 20 nov 2025: 1 problema | 1 de 1 | solo resultado (1894.4 W) |
| PEC-1-2022-CON-SOLUCION | PEC1 2022, problemas test a mano (Q1,2,4,5,6; falta Q3 en el escaneo) | 5 | sí, completa |
| recopilacion-test-PEC1-parte-1 | 3 problemas + 20 teóricas tipo Ex-Ejemplo + teoría PEC1 2022 (20, falta la 6) | sí | 3 problemas con resultado; teoría sin solución |
| ejemploTestProblemasMyMT / Ex-Ejemplo | Examen ejemplo de la asignatura (3 problemas MCIA / 20 teóricas) | 3 / ~9 | los de la recopilación; Ex-Ejemplo con marca ■ |
| Teoria-Julio-2020, 2020otrook | Extraordinario 8 jul 2020, teoría (20) | 7 / 6 | marca ■ ilegible (columnas mezcladas): sin solución |
| Problemas-Julio-2020 / 2020-JULIO-problemas-resueltos | Extraordinario 2020, 6 problemas (Q1-3 MCIA, Q4 vapor, Q5 cogeneración MCIA, Q6 TG) | Q1,2,3,5 | resuelto Q4 y Q6; Q1-3 en EjerciciosPEC1 |
| PROBLEMAS-PE1 | "PE1 2022/2023", 5 problemas MCIA a mano | 5 | sí, completa |
| EjerciciosPEC1 | Q1-Q3 de julio 2020 resueltos + 2 problemas más | 5 | sí |
| Problemas-De-Todo-MMT | Problemas de clase MCIA (5), resueltos a mano | 5 | sí |
| Preguntas-PEC1-y-PEC2 | Banco de 267 preguntas PEC1 (P1-P267) + PEC2 (P268-P327) | ~210 | casi ninguna |
| preguntasMotTema2 / preguntasMotTema1 | Banco por tema, con notas sueltas | T2 / T1 | algunas notas explicativas |
| KahootM3 | Kahoot de T2 (combustión, mecanismo, sobrealimentación) | sí | sin solución |
| Formulario-Motores-PEC1-2022 | Resumen a mano de dosado, potencia, rc, S/D | T2 | n/a |
| EXAMEN-ENERO-2024-RESUELTO | Es PEC2 (T3: vapor, TG): no sirve para T2 | no | n/a |

Aviso 1: el banco P1-P267 mezcla preguntas de examen UPM con un test de taller/FP (P219-P267: cilindros, culatas, tornillos, reglaje, tensión de correa). Esas ~30 no son de examen UPM: prioridad baja.
Aviso 2: el PEC1 de 2025 en problemas fue solo UN problema. Cuando ponga más, saldrán los tipos de la sección 3.
Aviso 3: las "recetas" abajo usan solo lo que sale en los problemas. Revisa tus fórmulas contra T2-contenido.md.

## 2. Preguntas de TEORÍA T2 en exámenes reales

Tipo: C = concepto (elegir/verdadero-falso), D = diagrama o figura, N = numérica. Todas son C salvo la que indique.

### 2.1 PEC1 2025 (20 nov 2025). Sin solución en la fuente.

| Q | Tema | Pregunta (resumen) | Respuesta |
|---|---|---|---|
| 3 | MMPE | Qué comparten MEP estratificado y homogéneo a baja carga (opciones: inicio de combustión, dosado global, método de regular, entrada del combustible) | sin solución |
| 4 | Renovación 2T | Qué motor no usa válvula de escape: MEC 2T uniflujo / MEP 2T por cárter / MEP 4T | sin solución (por razonamiento: MEP 2T barrido por cárter) |
| 5 | Dosado | Por qué mezcla estequiométrica cuasi-exacta en MEP: sonda lambda / catalizador 3 vías / inyección | sin solución (banco P188: catalizador) |
| 6 | Ciclos | "Mayor cilindrada unitaria con el mismo volumen final de compresión da mayor rendimiento del ciclo teórico": V/F | sin solución |
| 8 | pme/par/potencia | A plena carga, el mayor régimen se da en: potencia máxima / par máximo / consumo mínimo | sin solución (banco P128: potencia máxima) |
| 10 | Mecanismo / 2T | Qué elemento NO hay en un motor pequeño de bomba de riego: bujía / cigüeñal / árbol de levas / mariposa | sin solución |
| 11 | MEP vs MEC | Qué MCIA usan bujías | sin solución |
| 12 | Tipos | Rango de potencia máxima de un coche: 40-700 kW / 400 kW-7 MW / 4-70 kW / 4-700 W | sin solución |
| 13 | MEC | Afirmación cierta sobre MEC (picado, combustible volátil, mezcla homogénea, más partículas que MEP) | sin solución |
| 14 | Pérdidas mecánicas | En qué se transforma el rozamiento: bombeo / pot. indicada / calor al aceite y refrigerante / combustión incompleta | sin solución |
| 16 | Combustibles | e-fuel pesado con alta tendencia a autoinflamarse: MEC o MEP | sin solución (MEC) |
| 17 | Refrigeración | Afirmación cierta en refrigeración por líquido (inercia térmica, radiador, termostato, bomba desde cárter) | sin solución (banco P44: termostato) |
| 18 | Emisiones | Emisión más relevante en TG de una isla: CO / H2S / NOx | sin solución (NOx; T3) |

T1 en el mismo examen (5): Q1 rendimiento térmico, Q2 máquina motora vs generadora, Q7 TG en automoción, Q9 compresor scroll, Q15 máquina de vapor.

### 2.2 PEC1 2022 (teoría, 20 preguntas; falta la 6). Sin solución.

| Q | Tema | Pregunta (resumen) |
|---|---|---|
| 4 | Lubricación | De qué componente aspira la bomba de aceite (cárter) |
| 5 | MEC | Mezcla durante la combustión en MEC: heterogénea / homogénea / estratificada |
| 7 | pme | Si pme a par máx = 12 bar, valor posible a potencia máx: 12 / 15 / 9 bar |
| 8 | rc | rc volumétrica probable en MEC: 10 / 16 / 6 |
| 9 | Distribución | Qué permite el retraso al cierre de la admisión (inercia, llenado) |
| 10 | Combustión MEP | Frente de llama subsónico: ¿en qué motor? |
| 12 | Picado | Definición de picado (autoencendido delante del frente de llama) |
| 13 | Ciclo | Fórmula del trabajo indicado por ciclo (D, sobre figura) |
| 14 | Sobrealimentación | Afirmación cierta en 4T sobrealimentado (lazo de bombeo, p admisión, pérdidas mec.) |
| 16 | Refrigeración | Afirmaciones sobre refrigeración por agua (bomba, termostato, radiador) |
| 17 | Mecanismo | Qué está alojado en el pistón (bulón) |
| 18 | 2T | Qué distingue a un 2T de un 4T (bomba de barrido, potencia específica, coste, lumbreras) |
| 19 | Combustibles | e-fuel volátil con alta resistencia a la autoinflamación: MEP o MEC |
| 20 | pme/par | Dos 4T de 1.9 L con la misma pme máxima tienen igual: potencia / par / ninguna |

T1 en el mismo examen: Q1 ciclo cerrado, Q2 ciclo combinado, Q3 motores térmicos, Q11 energía térmica del fluido, Q15 hidrógeno.

### 2.3 Ex-Ejemplo (examen ejemplo de la asignatura). Marca ■ en el PDF.

| Q | Tema | Pregunta | Respuesta (marca ■) |
|---|---|---|---|
| 2 | Mecanismo | Parte del pistón: segmento / asiento de válvula / alojamiento del bulón | alojamiento del bulón |
| 5 | ηv | Condición de referencia para ηv en motor turboalimentado sin postenfriar | presión y T detrás del compresor centrífugo |
| 6 | Pérdidas mec. | Mayor potencia de pérdidas mecánicas (salto de presiones, caudal, ηi fijos) implica | sin solución (marca ilegible) |
| 10 | Ciclo | Cuándo empieza la combustión en un MCIA | durante la carrera de compresión |
| 12 | Emisiones | Emisión más importante en MCIA de camión de larga distancia: PM / NOx / CO2 | CO2 (marca ■ junto a CO2) |
| 13 | Combustibles | Combustible que no se puede usar en MEP | biodiésel |
| 14 | Balance | Energía química perdida por refrigeración: 60-65 / 30-35 / 10-15 % | 30-35 % |
| 15 | Ciclo | Presión máxima del ciclo teórico de presión limitada vs MEC real | igual |
| 20 | Ciclo | Proceso del MCIA que absorbe trabajo | admisión |

### 2.4 Julio 2020 (teoría, extraordinario, 8 jul 2020) y 2020otrook (otra versión, mismo día). Sin solución (marca ■ ilegible).

Julio 2020: Q2 presión máxima en el MCIA (¿carrera de expansión, compresión o PMS?), Q7 energía química que llega al eje en MEP (60-65 / 40-55 / 30-35 %), Q8 proceso que absorbe trabajo, Q9 combustible no usable en MEP, Q10 condiciones ref. ηv en sobrealimentado mecánicamente, Q12 trabajo indicado del ciclo teórico de aire (mayor/igual/menor que el del MCIA), Q15 parte del pistón.
2020otrook: Q2 energía útil en eje MEP, Q4 trabajo indicado del ciclo teórico, Q7 ηv aspiración natural, Q10 proceso que absorbe trabajo, Q15 cuándo empieza la combustión, Q16 parte del pistón.

### 2.5 Banco P1-P267 (Preguntas-PEC1-y-PEC2): conteo por tema

La fuente no da respuestas (salvo 2 cálculos con solución: P104 tiempo de retraso = 1 ms, P117 tiempo de combustión = 2.2 ms). Los números P son los del PDF.

| Tema | Nº | Números P |
|---|---|---|
| Mecanismo y construcción | 36 (13 de nivel UPM + ~23 de taller) | 2-9, 94, 121-123, 132, 219-225, 238-267 |
| Combustión MEC (retraso, premezclada, difusión, inyección) | 24 | 32, 87, 92, 99, 102, 104, 115-117, 202, 204, 210, 216-218, 226-232, 246-247 |
| Combustión MEP (deflagración, picado, octano, bujía) | 21 | 38, 40, 86, 95, 97, 100-101, 118, 177-183, 186, 189, 193-195, 198 |
| Distribución (AAE, RCE, RCA, cruce) | 19 | 37, 140-146, 213, 224, 248-250, 253-258 |
| Renovación de la carga 2T/4T | 17 | 50, 98, 103, 107, 165-176, 205, 222 |
| Ciclos de aire, indicador, trabajo indicado, lazo de bombeo | 16 | 17, 21, 27, 41-42, 106, 109, 130, 134-136, 138-139, 152, 166, 209 |
| pme, par, potencia, régimen, elasticidad | 14 | 33-34, 52, 128-129, 131, 133, 137, 207, 234-237, 243 |
| Refrigeración | 12 | 20, 44-49, 161-164, 206 |
| Dosado, mezcla rica/pobre, catalizador 3 vías | 10 | 111, 147-148, 187-188, 190-191, 196-197, 201 |
| Sobrealimentación | 10 | 112, 150, 154-160, 233 |
| MEP vs MEC, combustibles, rc, rendimientos típicos | 8 | 19, 35-36, 51, 96, 108, 125, 242 |
| Emisiones | 7 | 18, 83-85, 114, 199-200 |
| MMPE (carga estratificada) | 6 | 90, 105, 184-185, 203, 208 |
| Lubricación y fricción | 6 | 31, 124, 126-127, 211-212 |
| ηv y condiciones de referencia | 5 | 11-13, 149, 214 |
| Sin clasificar | 6 | 10 (T1), 113, 151, 153, 192, 215 |

T1 en el banco: ~51 preguntas (P1, 14-16, 22-30, 39, 43, 53-83, 88-89, 91, 93, 110, 119-120). P268-P327 son de T3 (PEC2).

### 2.6 Conteo de las 5 teorías reales (2025, 2022, Ex-Ejemplo, Julio 2020, otrook): preguntas T2 por tema

| Tema | Veces | Dónde |
|---|---|---|
| Ciclos teóricos / indicador / trabajo / cuándo empieza la combustión | 11 | 2025 Q6; 2022 Q13; Ex-Ej Q10, Q15, Q20; J20 Q2, Q8, Q12; ok Q4, Q10, Q15 |
| MEP vs MEC: tipos, combustibles, rc, rangos | 8 | 2025 Q11, Q12, Q13, Q16; 2022 Q8, Q19; Ex-Ej Q13; J20 Q9 |
| Mecanismo (partes del pistón) | 5 | 2025 Q10; 2022 Q17; Ex-Ej Q2; J20 Q15; ok Q16 |
| Balance de energía (30-35 % útil/refrigeración) | 3 | Ex-Ej Q14; J20 Q7; ok Q2 |
| ηv, condiciones de referencia | 3 | Ex-Ej Q5; J20 Q10; ok Q7 |
| pme / par / potencia | 3 | 2025 Q8; 2022 Q7, Q20 |
| Combustión MEP (picado, frente de llama) | 2 | 2022 Q10, Q12 |
| Pérdidas mecánicas y lubricación | 3 | 2025 Q14; Ex-Ej Q6; 2022 Q4 |
| Refrigeración | 2 | 2025 Q17; 2022 Q16 |
| Emisiones | 2 | 2025 Q18; Ex-Ej Q12 |
| Renovación 2T | 2 | 2025 Q4; 2022 Q18 |
| Combustión MEC; MMPE; dosado/catalizador; sobrealimentación; distribución | 1 cada uno | 2022 Q5; 2025 Q3; 2025 Q5; 2022 Q14; 2022 Q9 |

Por tipo: de ~50 preguntas T2 reales, 100 % son concepto (elegir o verdadero/falso). Ninguna pide dibujar. Una pide fórmula (2022 Q13, trabajo indicado como integral de p dV).

## 3. PROBLEMAS (test de 1/3, solo T2)

Formato: enunciado + 15 opciones (una correcta). En el examen ejemplo y en julio 2020 el fallo en problemas vale 0. (En teoría resta: -1/3 con 4 opciones, -1/2 con 3, -1 con 2.) La tabla cuenta cada problema por tipo.

### 3.1 Los 7 tipos que se repiten

| Tipo | Nº | Dónde |
|---|---|---|
| A. pme desde Ẇe (o Me) + geometría o Cm | 8 | 2022 Q2; PE1 Q2; J20 Q1; Ex-Ej Q1 (135 kW); EjerciciosPEC1 Q1; clase P1, P2, P4 |
| B. ηv desde consumo (l/h o l/100 km) o desde ṁa | 6 | 2022 Q4; PE1 Q3; J20 Q3; Ex-Ej Q3; clase P3; EjerciciosPEC1 Q3 |
| C. Ẇe desde gef / ηv / ṁf | 5 | 2022 Q5; PE1 Q1; EjerciciosPEC1 Q5; clase P1 (gef); 2025 (bomba, ver E) |
| D. Dosado relativo desde Ẇe, ηv, ηi, ηm | 3 | J20 Q2; Ex-Ej Q2; EjerciciosPEC1 Q2 |
| E. Potencia de pérdidas mecánicas / auxiliares: Ẇpm = Ẇi − Ẇe | 4 | 2022 Q1; PE1 Q4; 2025 (bomba); EjerciciosPEC1 Q4 (pmi) |
| F. Balance de energía: ṁf·Hc = Ẇe + Q̇ref + Q̇rad + Q̇ge | 2 | 2022 Q6; PE1 Q5 |
| G. Leer curvas (par, potencia, gef), comparar dos puntos A/B, Cm máx | 3 | clase P2, P3, P5 |

Fuera de T2 puro pero MCIA: cogeneración con MCIA (J20 Q5); no entra en PEI1 (es T1/T3), no se desarrolla aquí.

### 3.2 Fórmulas de todos los tipos (cada una sale en las soluciones de las fuentes)

- Ẇe = Me·ω = Me·2πn  (n en s⁻¹)
- Cm = 2·S·n  →  n = Cm/(2S).  Con D = S (relación 1): VT = z·π·D²/4·S.
- pme = Ẇe/(VT·n/i) con i = 1/2 en 4T (i = 1 en 2T). Con Ẇ en W y VT en m³ sale en Pa: ÷10⁵ para bar.
- ηe = ηi·ηm = Ẇe/(ṁf·Hc).  gef = ṁf/Ẇe = 1/(ηe·Hc).
- ηv = ṁa/(ρref·VT·n/2). ρref = p/(Ra·T) con las condiciones de referencia (ver abajo).
- F = ṁf/ṁa.  Fr = F/Fe.  Con catalizador 3 vías: Fr = 1.
- Ẇi = ηi·ṁf·Hc.  Ẇpm = Ẇi − Ẇe.  pmi = pme + Ẇpm/(VT·n/2).
- Balance: ṁf·Hc = Ẇe + Q̇ref + Q̇rad + Q̇ge (las pérdidas dadas en % de ṁf·Hc).
- Tiempo de combustión o retraso: t = ángulo/(6·n_rpm) segundos (P104, P117).
- Condiciones de referencia de ηv: aspiración natural → ambientales; mecánica o turbo SIN postenfriar → detrás del compresor; con postenfriador → detrás del postenfriador (en J20 Q2: p = 2 bar, T = 35 °C tras postenfriador). Presión en bar manométrico: sumar patm.

### 3.3 Un esquema resuelto por tipo (datos reales de las fuentes, resultado verificado con Python)

A. pme. J20 Q1: 2 cilindros, D = S = 9.2 cm, Ẇe = 58 kW, Cm = 10.3 m/s.
 1) n = Cm/(2S) = 56 s⁻¹.  2) VT = 2·π·0.092²/4·0.092 = 1.22 L.  3) pme = 58e3/(VT·56/2) = 16.9 bar (EjerciciosPEC1: 16.94). Versión Ex-Ej (135 kW, 5 cil., 9.3 cm, 8.4 m/s): 18.9 bar.
 Variante 2022 Q2: dan Me = 265 Nm, Cm = 9.9 m/s, S = 9.4 cm, VT = 2.6 L → n = 52.66 s⁻¹, Ẇe = 87.7 kW, pme = 12.8 bar.

B. ηv. 2022 Q4 (viaje, MEP 2.8 L, 3000 rpm, 9.6 L/100 km, 490 km en 4.2 h, 10 °C, 0.98 bar, ρf = 0.69 g/cm³, Fe = 1/14.7).
 1) ṁf = consumo × distancia ÷ tiempo × ρf = 2.147 g/s (kg/s ×10⁻³).  2) Fr = 1 (catalizador) → ṁa = 14.7·ṁf = 0.0316 kg/s.  3) ρia = 1.293·(0.98/1.013)·(273.15/283.15) = 1.207 kg/m³.  4) ηv = 0.0316/(25·2.8e-3·1.207) = 37.4 %.
 Variante J20 Q3 (MEP sobrealimentado 940 cm³, 17.8 l/h, 1.4 bar manométricos = 2.4 bar abs, 36 °C): ṁf = 17.8·10⁻³·850/3600; ṁa = ṁf/Fe; ρ = p/(Ra·T) → ηv = 72.6 %. Ex-Ej Q3 (2.35 bar abs, 46 °C, 760 cm³, 12.5 l/h) → 64.9 % (la recopilación da 64.9 %; mi cálculo, 64.9 %).

C. Ẇe desde gef. 2022 Q5 (MEP 4T 2.9 L, 2800 rpm, ηv 0.62, gef 256 g/kWh, Fe = 1/15, ρ = 1.45).
 1) ṁa = ηv·ρ·VT·n/2 = 0.061 kg/s.  2) ṁf = ṁa/15 = 4.06 g/s.  3) Ẇe = ṁf/gef = 57.0 kW.

D. Dosado. Ex-Ej Q2 (2.53 L, 107 kW, 3030 rpm, 2 bar, 35 °C, ηv 0.93, ηi 0.49, ηm 0.72, Fe = 1/17, Hc 43 MJ/kg).
 1) ρ = 2e5/(283·308) = 2.294.  2) ṁa = ηv·ρ·VT·n/2.  3) ṁf = Ẇe/(ηi·ηm·Hc) (ηe = ηi·ηm).  4) F = ṁf/ṁa, Fr = F/Fe = 0.88. J20 Q2 (57 kW, 2.65 L, 3560 rpm, 0.85/0.46/0.62) → 0.515.

E. Pérdidas. 2025 (MEC 4T, Q̇f = 280 kW, ηi 0.48, ηm 0.87, fricción+bombeo = 8 kW, bomba = 20 % de los auxiliares).
 1) Ẇi = 0.48·280 = 134.4 kW.  2) Ẇe = 0.87·134.4 = 116.93 kW.  3) Ẇpm = Ẇi − Ẇe = 17.47 kW.  4) Auxiliares = Ẇpm − 8 = 9.47 kW.  5) Bomba = 0.2·9.47 = 1.894 kW = 1894.4 W (coincide con la solución de la fuente).
 2022 Q1: Ẇi = z·n·wi·(1/2) con wi = 0.45 kJ/cil → 40.5 kW (3 cil., 3600 rpm); Ẇe = 2π·60·75 = 28.27 kW; Ẇpm = 12.2 kW.

F. Balance. 2022 Q6 (turbo+intercooler 4T, 1.9 L, 190 Nm, 2800 rpm, ηv 0.93, Fr = 0.75, Fe = 1/14.7, ρ aire = 2.35, Hc 44 MJ/kg, radiación 5 %, refrigeración 22 %).
 1) ṁa = 0.93·(2800/60/2)·1.9e-3·2.35 = 0.097 kg/s.  2) F = 0.75/14.7 = 0.051 → ṁf = 4.94 g/s.  3) Q̇comb = 217.4 kW.  4) Ẇe = 2π·46.67·190 = 55.7 kW.  5) Q̇ge = 217.4 − 55.7 − 0.27·217.4 = 103.0 kW (fuente: 103.1 kW).

G. Curvas / puntos A y B. Clase P3 (MEP 4T, 4 cil., D = 82.5 mm, S = 81 mm, A: F = 100 N con brazo 1 m, 4500 rpm, ṁf = 4 g/s; B: pme +20 %, ṁf 3.5 g/s, mismo ηe).
 1) A: Me = 100 N·m; pmeA = 7.25 bar; ηe = Ẇe/(ṁf·Hc) = 27.3 %.  2) B: pmeB = 8.7 bar → MeB = 120 N·m; ẆeB = ηe·ṁfB·Hc = 41.2 kW.  3) nB = ẆeB/(2π·MeB) = 3281 rpm.
 Clase P5: de la gráfica de plena carga se lee Me,máx (pme máx a par máx), Ẇe,máx y gef,mín (ηe,máx = 1/(gef,mín·Hc)).

Nota: en PROBLEMAS-PE1 Q1 el enunciado no se ve completo en el escaneo (falta ρ aire). Resultado de la fuente 63.9 kW, que cuadra con ρ ≈ 1.72 kg/m³; con 1.172 saldría 43.6 kW. Revisa antes de usar esa receta.

## 4. LAS 10 COSAS QUE MÁS PREGUNTAN

(Ordenadas por frecuencia: apariciones en exámenes reales + banco.)

1. Problema: pme, Ẇe, Me, Cm y geometría (tipo A). 8 problemas. "Un MEC de 4 tiempos de aspiración natural con 5 cilindros de diámetro 9.3 cm y relación carrera/diámetro igual a la unidad da una potencia en el eje de 135 kW cuando trabaja con una velocidad media de pistón de 8.4 m/s. Calcular la presión media efectiva." (18.9 bar)
2. Problema: ηv desde el consumo de combustible (tipo B) y su aire de referencia. 6 problemas. "...consume 12.5 l/h de combustible a 4300 min⁻¹... presión y temperatura de soplado de turbo 2.35 bar y 46 °C... obtener el rendimiento volumétrico." (64.9 %). Trampa: manométrico vs absoluto; dosado Fr = 1 con catalizador.
3. Problema: cadena ṁf → ṁa → Ẇe con gef, ηv, Fr, Fe (tipos C, D). 8 problemas. "...gasto específico de combustible es 256 g/kWh, obtener la potencia efectiva." (57 kW) "...calcular el dosado relativo de funcionamiento." (0.88).
4. Problema: Ẇpm = Ẇi − Ẇe y balance de calor (tipos E, F). 6 problemas, incluido el único del PEC1 2025: "...calcula la potencia consumida por la bomba de combustible." (1894.4 W). 2022: "Obtener las pérdidas mecánicas para este punto de operación." (12.2 kW)
5. Teoría: ciclos teóricos de aire y qué hace el MCIA real: "¿Cuál es verdadera? La combustión en un MCIA se inicia durante la carrera de compresión / expansión / exactamente en el PMS." Salió en Ex-Ej, ok2020, banco P17. Con ella: la presión máxima va después del PMS (P106, J20 Q2), "La presión máxima de un ciclo teórico de aire de presión limitada es: igual que la del MEC" (Ex-Ej Q15), "El trabajo indicado de un ciclo teórico de aire es: mayor que el del MCIA que simula" (J20 Q12, ok Q4, P139), "¿Cuál de los siguientes procesos de un MCIA absorbe trabajo?" (admisión; Ex-Ej, J20, ok, P27). Total 11 apariciones en 5 teorías.
6. Teoría: MEP vs MEC (combustible, rc, mezcla, regulación, bujías). "¿Qué combustible no se puede consumir en un MEP? Biodiésel/Gas natural/Biogás" (Ex-Ej, J20, P19); "¿En qué motor utilizarías un combustible sintético (e-fuel) pesado con alta tendencia a la autoinflamación?" (2025 Q16, 2022 Q19); rc probable de un MEC 10/16/6 (2022 Q8, P35-36). 8 apariciones.
7. Teoría: partes del motor y mecanismo. "¿Cuál es una parte del pistón de un MCIA? Segmento / Asiento de la válvula / Alojamiento del bulón." (Ex-Ej Q2, J20 Q15, ok Q16, 2022 Q17, banco P2-P9). "¿Desde qué componente aspira la bomba de aceite? Cárter" (2022 Q4, P31). 5 + 13 del banco.
8. Teoría: ηv y condiciones de referencia. "¿Qué condiciones de referencia se toman para calcular el rendimiento volumétrico en un motor turboalimentado sin postenfriamiento?" (Ex-Ej Q5, J20 Q10, ok Q7, P11-P13). Regla: NA ambiente; sobrealimentado sin postenfriar detrás del compresor; con intercooler detrás del intercooler.
9. Teoría: balance y rendimientos típicos. "Del total de la energía química... ¿cuánta se pierde por la necesidad de refrigeración de un MCIA? 30-35 %" (Ex-Ej Q14, P20) y "¿cuánta se convierte en energía útil en el eje en un MEP de automoción en su punto óptimo? 30-35 %" (J20 Q7, ok Q2). Relaciona con pme típica: "Si la pme de un MEP para máximo par vale 12 bar, ¿cuál es posible para máxima potencia? 9 bar" (2022 Q7, P33-34): la pme baja al subir el régimen; par máx a menor régimen que potencia máx (P128, 2025 Q8).
10. Teoría: sobrealimentación, refrigeración, 2T y combustión. Refrigeración (2025 Q17, 2022 Q16, P44-49, P161-164: termostato cerrado en calentamiento, bomba desde cárter a camisas). 2T (2025 Q4, 2022 Q18: bomba de barrido, lumbreras, sin válvulas en barrido por cárter). Combustión MEP/MEC/MMPE y catalizador 3 vías Fr = 1 (2025 Q3 y Q5, 2022 Q5/Q10/Q12; banco P38-P40, P86, P177-P198, P226-P232).

## 5. Qué estudiar primero (propuesta)

1. Problemas: haz a mano los 7 tipos con las soluciones de la sección 3.3. Es 1/3 de la nota y casi regalado: son la misma cadena de 4 fórmulas.
2. Teoría T2: aprende la lista de la sección 4 puntos 5-10. Son los temas con más apariciones (no medí el % exacto que cubren).
3. T1: solo sale la parte fácil (respuestas de esta lista = mi razonamiento, no de la fuente). Se repiten: hidrógeno → motor térmico (6 veces; CORREGIDO 15 nov: la marca oficial del examen ejemplo Q17 y la diap. 6 dicen motor térmico, no pila de combustible), máquina térmica generadora = compresor de tornillo / grupo turbo (6), mayor presión de admisión en turbina → de vapor (5), motor de combustión externa = turbina de vapor, máquina de vapor, Stirling (5), turbohélice = 2 máquinas (3), cogeneración sin perder energía mecánica útil (pregunta repetida 4 veces; respuesta sin solución, mi razonamiento: turbina de gas de ciclo abierto, no oficial).
4. Deja para el final las ~30 preguntas de taller del banco (P238-P267).

## 6. Límites

- Teoría 2025: sin solución en ninguna fuente. Mis "respuestas por razonamiento" no son oficiales.
- Ex-Ejemplo: las marcas ■ son legibles; en J20 y ok2020 las columnas salen mezcladas y no uso las marcas.
- No leí página a página 0-Ejercicios-de-examen-MMT (2006/2007), MOTORESEJERCICIOSEXAMENES (T3), Problemas-De-Todo-MMT p. 6-24 (T3 y más clase) ni Examenes-T1-T2-y-T3 (fotos de teoría, sin texto). Pueden traer más preguntas T2 con solución.
- PEC1 2022 Q3 falta en el escaneo; teoría 2022 Q6 falta en el texto.
