---
type: analysis
status: done
date: 2026-11-15
tags: [uni, mymt, examenes, problemas]
related: [examenes-problemas.json, T2-examenes-analisis.md]
---

# MyMT: problemas de examen, tipos y orden de estudio

Fuente: 127 entradas en `examenes-problemas.json` (105 problemas distintos; 22 son copias del mismo problema en otro fichero, campo `duplicate_of`). Se leyeron todas las páginas de los 33 PDF (ninguna ilegible; las páginas que son portada, anuncio o hoja en blanco no tienen problemas). Los resultados citados abajo los recalculé en Python.

## 1. Cuántos problemas hay por tema

| Tema | Problemas distintos | Parcial |
|---|---|---|
| T2 MCIA | 61 | PEI1 |
| T3 vapor, gas, combinado, cogeneración | 44 | PEC2 |
| T1 fundamentos | 0 sueltos | PEI1 y PEC2 |

- T1 no tiene problemas numéricos propios en ningún fichero. T1 sale como teoría (tests de 2012 y bancos de preguntas) y como base de los problemas de T2 y T3: balances de energía, rendimientos, gas ideal, ρ = p/(R·T).
- Los problemas de T2 dentro de PEI1 son el problema test de 1/3 de la nota.
- Años: 2004-2015 (exámenes abiertos), 2020 (extraordinario), 2022, 2024 (enero), 2025 (PEC1 20 nov). 65 entradas no traen año.

## 2. Formato de la prueba de problemas

- Extraordinario 8 jul 2020: 6 problemas (3 MCIA, 1 vapor, 1 cogeneración MCIA, 1 turbina de gas), 75 min.
- Test: 15 opciones por problema, una sola correcta. Acierto +1; fallo 0; blanco o varias marcas 0. No hay penalización por fallar.
- Modelo de examen y ejemplo de test de problemas: 3 problemas MCIA, mismas reglas.
- PEC1 20 nov 2025: 1 problema MEC con respuesta numérica (1894.4 W), no test.
- Exámenes 2004-2015 y enero 2024: problemas abiertos con varios apartados.
- Test de teoría (otra prueba): 20 min, 20 preguntas, penaliza -1/3 (4 opciones), -1/2 (3), -1 (2). Los tests de 2012 penalizan -0.5 por fallo.
- Como las 15 opciones incluyen el error típico, una respuesta "casi" correcta suele estar en la lista. Compara siempre con el resultado de tu cuenta antes de marcar.

## 3. Ranking de tipos (problemas distintos)

| # | Tipo | N | Exámenes (ejemplos) |
|---|---|---|---|
| 1 | G2 Turbina de gas (Brayton real, dos ejes, regenerativa) | 23 | Jun 2006, Jul 2020 Q6, Ene 2024 (3), colecciones |
| 2 | M1 pme, potencia, par, velocidad de pistón | 18 | Jul 2020 Q1, PE1 2022 Q1-2, PEC1 2022 Q2/Q5, Modelo, ej. PEC1 |
| 3 | G1 Vapor regenerativo / recalentamiento / beneficio | 12 | Feb 2008, Jul 2020 Q4, Ene 2024, colecciones |
| 4 | M2 Rendimiento volumétrico y consumo | 9 | Jul 2020 Q3, PE1 2022 Q3, PEC1 2022 Q4, Modelo |
| 5 | M3 Dosado relativo (sobrealimentado) | 6 | Jul 2020 Q2, Jun 2008, Modelo, ej. PEC1 |
| 6 | M8 Tiempos y ángulos (retraso, combustión, encendidos) | 6 | solo en bancos de test; PE1 2022 Q6 (frente de llama) |
| 7 | M5 Balance energético con gases de escape | 5 | Mar 2015, Sep 2005, PE1 2022 Q5, PEC1 2022 Q6 |
| 8 | M6 Sobrealimentación: turbo, postenfriador | 5 | Ene 2013, colecciones |
| 9 | M9 Curvas, carga parcial, ley de la hélice | 5 | colecciones |
| 10 | M4 Pérdidas mecánicas y pmi | 4 | Abr 2015, PE1 2022 Q4, PEC1 2022 Q1 |
| 11 | G1b Vapor Rankine simple | 4 | Ene 2024, colecciones |
| 12 | G3 Ciclo combinado gas + vapor | 3 | Jun 2004, Jun 2013, colección |
| 13 | G4 Cogeneración con turbina de gas | 2 | Jun 2012, colección |
| 14 | M7 Cogeneración con MCIA | 2 | Jul 2020 Q5, apuntes |

Lectura: en PEI1 el test de 3 problemas es casi siempre M1 + M3 + M2 (Jul 2020, Modelo, ejemplo). En PEC2 domina la turbina de gas, luego el vapor regenerativo, y cierran ciclo combinado y cogeneración.

## 4. Cadena de fórmulas, datos, trampa y ejemplo por tipo

Datos de partida casi siempre dados: Hc, Fe, cp, γ, rendimientos. El vapor se lee de tablas o Mollier (±1-2 %).

### M1 pme / potencia / par / cm (T2)
- Cadena: cm = 2·S·n → n; VT = i·π/4·D²·S; pme = Ne/(VT·n·i) con i = 1/2 (4T) o 1 (2T); Me = Ne/(2πn).
- Datos: cilindros, D, S/D, Ne o Me, cm o n.
- Trampa: i = 1/2 en 4T; unidades de n (rps); S/D = 1 ⇒ S = D.
- Ejemplo (Modelo, Q1): 5 cil., D = 9.3 cm, S/D = 1, Ne = 135 kW, cm = 8.4 m/s. n = 45.16 rps, VT = 2.84 L, pme = 18.93 bar. Opción 18.9. Coincide con la fuente.

### M2 Rendimiento volumétrico (T2)
- Cadena: ṁf = V̇f·ρf; ṁa = ṁf/F (con F = Fr·Fe); ρref = p/(Ra·T); ηv = ṁa/(ρref·VT·n/2).
- Trampa: p manométrica ⇒ sumar patm; ρref depende de dónde se mide (tras compresor o tras postenfriador).
- Ejemplo (Jul 2020 Q3): 17.8 l/h, 4200 rpm, 1.4 bar man., 36 °C, 940 cm³, Fe = 1/15.6, ρf = 850. Con p = 2.4 bar abs: ηv = 72.6 %. Con 1.4 bar abs saldría 124.5 % (imposible: la señal del error).

### M3 Dosado relativo (T2)
- Cadena: Ṅe → ṁf = Ne/(ηi·ηm·Hc); ṁa = ηv·ρ·VT·n/2; F = ṁf/ṁa; Fr = F/Fe.
- Trampa: ηe = ηi·ηm; ρ con T en kelvin y p en Pa.
- Ejemplo (Jul 2020 Q2): VT = 2650 cm³, 57 kW, 3560 rpm, 2 bar, 35 °C, ηv/ηi/ηm = 0.85/0.46/0.62, Fe = 1/17, Hc = 43000. F = 0.03033, Fr = 0.5156. Opción 0.515.

### M4 Pérdidas mecánicas / pmi (T2)
- Cadena: Ẇi = Z·n·wi·i (4T: ½); Ẇe = 2π·n·Me; Ẇpm = Ẇi − Ẇe; ηm = Ẇe/Ẇi.
- Trampa: wi es por cilindro y por ciclo; n en rps.
- Ejemplo (PEC1 2022 Q1): 3 cil., 75 N·m, 3600 rpm, wi = 0.45 kJ. Ẇi = 40.5 kW, Ẇe = 28.27 kW, Ẇpm = 12.23 kW. Opción 12.2.
- PEC1 2025 (MEC): Ẇi = 0.48·280 = 134.4 kW; Ẇe = 0.87·134.4 = 116.93 kW; Ẇpm = 17.47 kW; Ẇaux = 17.47 − 8 = 9.47 kW; bomba = 20 % = 1894.4 W.

### M5 Balance energético con gases de escape (T2 con T1)
- Cadena: ṁa = ηv·n/2·VT·ρ; F = Fr·Fe; ṁf = F·ṁa; Q̇comb = ṁf·Hc; Q̇ge = Q̇comb − We − pérdidas.
- Trampa: los porcentajes de pérdida son del Q̇comb, no de We.
- Ejemplo (PEC1 2022 Q6): 1.9 L, 190 N·m, 2800 rpm, ηv = 0.93, Fr = 0.75, ρ = 2.35, Fe = 1/14.7, Hc = 44000, pérdidas 5 % + 22 %. ṁa = 0.0969 kg/s, ṁf = 4.94 g/s, Q̇comb = 217.5 kW, We = 55.71 kW, Q̇ge = 103.07 kW. Opción 103.1.

### M6 Turbo y postenfriador (T2)
- Cadena: T2s = T1·rc^((γ−1)/γ); T2 = T1 + (T2s − T1)/ηc; efectividad del postenfriador R = (Te − Ts)/(Te − Tamb); densidad tras el postenfriador → ηv.
- Trampa: T en kelvin; ρ de referencia tras el postenfriador.
- Ejemplo (Ene 2013): VT = 1950 cm³, 3025 rpm, 98 kW, 27 l/h. Me = 309.4 N·m, pme = 19.94 bar, cm = 8.60 m/s, ηe = 0.3453, gef = 239.7 g/kWh, T2 = 299.9 K.

### M7 Cogeneración con MCIA (T2 + T3)
- Cadena: Qf = Ne/ηe; Qref = x·Qf; Qgas = Qf − Ne − Qref; Tg = Tamb + Qgas/(ṁ·cp); Qu = η·Qref + ṁ·cp·(Tg − Tchim); ηglobal = (Ne + Qu)/Qf; REE = Ne/(Qf − Qu/ηcaldera).
- Trampa: la energía de gases se mide desde Tamb; REE lleva Qu/ηcaldera en el denominador.
- Ejemplo (Jul 2020 Q5): 101 kW, ηe = 0.323, 241 g/s, refrigeración 31.1 %, recupera 76.5 %, chimenea 161 °C, Tamb 25 °C, cp = 1, caldera 0.9. Qf = 312.7 kW, Tg = 499.9 °C, Qu = 156.1 kW, REE = 72.5 %. Opción más cercana 72.6 % (diferencia de redondeo).

### M8 Tiempos y ángulos de combustión (T2)
- Cadena: t = ángulo/(360·n); retraso en ms; encendidos cada 720°/Z.
- Ejemplo (test): combustión de 40° a 3000 rpm: t = 40/(6·3000) = 2.22 ms.

### M9 Curvas y carga parcial (T2)
- Cadena: We = Me·2πn; hélice Me = k·n² ⇒ We = 2πk·n³; n₂ = n₁·(We₂/We₁)^(1/3).
- Ejemplo (apuntes): k = 1e6/(2π·25³) = 10.186; al 50 % de potencia n = 1500·0.5^(1/3) = 1190.6 rpm.

### G2 Turbina de gas (T3 con T1)
- Cadena: T2s = T1·rp^((γ−1)/γ); T2 = T1 + (T2s − T1)/ηc; T4s = T3·rp^(−(γ−1)/γ); T4 = T3 − ηt·(T3 − T4s); η = [(1+F)(h3−h4) − (h2−h1)]/(F·Hc).
- Dos ejes: wT1 = wC (con ηm si da), luego T3 − T4 = T2 − T1 y T5 = T4 − wT2/cp; F por la cámara: F = cp(T3−T2)/(ηcc·Hc).
- Datos: T3, rp, ηc, ηt, Hc, F, γ, cp, T1 ambiente.
- Trampa: kelvin; el factor (1+F) y el gasto de combustible; ηm en dos ejes; en un test la opción con rp mal usada está en la lista.
- Ejemplo (Jul 2020 Q6): T3 = 1375 °C, rp = 8.7, ηc = 0.83, ηt = 0.88, Hc = 54000, F = 1/49.5, T1 = 15 °C. T2 = 585.1 K, T4 = 979.5 K, η = 35.31 %. Opción 35.3 %.
- Ejemplo dos ejes (Ene 2024 Q4): rp = 5, ηc = 0.87, ηcc = 0.93, wT2 = 192.5 kJ/kg, T5 = 813 K, T1 = 293 K, Hc = 43000. T2 = 489.62 K, T4 = 1005.5 K, T3 = 1202.12 K, F = 0.0178.

### G1 Vapor regenerativo y recalentamiento (T3 con T1)
- Cadena: estados con tablas; fracción de extracción α por balance del calentador (abierto: α = (h_sat − h_b)/(h_ext − h_b)); wT = (h5−h_ext) + (1−α)(h_ext−h6); η = (wT − wB)/(h5 − h_entrada caldera); beneficio B = (Q_simple − Q_reg)/Q_simple. Con recalentamiento: wT = (h5−h4') + (h5'−h6).
- Trampa: definición de B (ahorro de calor, no ganancia relativa de η); wB despreciable solo si el enunciado lo dice; calcular α antes de wT.
- Ejemplo (Jul 2020 Q4): h5 = 3610, h6 = 2430 kJ/kg, Tcond = 40 °C ⇒ h1 = 167.2, B = 6.3 %, wB = 0. η simple = 34.27 %; η regenerativo = 36.58 %. Opción 36.6 %.

### G1b Vapor Rankine simple (T3)
- Cadena: η = (h5−h6 − wB)/(h5 − h2); wB = v·Δp; ṁ = W/(wT − wB).
- Trampa: ordenar bien los estados 1-2 (bomba) y 5-6 (turbina).

### G3 Ciclo combinado (T3)
- Cadena: Qgases escape = (ma+mf)·cp·(T4 − Tsalida caldera); WTV = ηTV·fracción·E; ηcc = (WTG + WTV)/(ṁf·Hc).
- Ejemplo (Jun 2013): Pe = 35 MW, gef = 220 g/kWh, FR = 0.22, Fe = 1/17, Hc = 48500, cp = 1.2, 80 % de E, ηTV = 0.32. ηTG = 33.74 %, ṁf = 2.139 kg/s, ṁa = 165.3 kg/s, E = 68.74 MW, T4 = 362.1 °C, WTV = 17.60 MW, ηcc = 50.70 %. (La fuente da 165.8 kg/s y 68.49 MW: errata, ver sección 6.)

### G4 Cogeneración con turbina de gas (T3)
- Cadena: T4 con ηt; Q útil = (1+F)·ṁa·cp·(T4 − Tchim) ⇒ ṁa ⇒ ṁf = F·ṁa.
- Ejemplo (Jun 2012): Q = 1 MW, T3 = 950 °C, 9 bar, F = 0.0156, ηt = 0.9, chimenea 100 °C. T4s = 652.8 K, T4 = 709.8 K, ṁa = 2.92 kg/s, ṁf = 0.0456 kg/s = 164.2 kg/h.

### Tipos que cruzan T1 y T3 (y no solo MCIA)
- Balance de energía sobre un volumen de control con ṁ, h, Q̇, Ẇ: es lo mismo en turbina, caldera, cámara y recuperador (G1, G2, G3, G4).
- Rendimientos isentrópicos y gas ideal (T2s, T4s): T1 los da, G2 los usa siempre.
- Ratio de calor útil y energía de combustible (ηglobal, REE) aparece en MCIA y en turbina de gas: misma fórmula.

## 5. "Si solo tienes 2 horas"

PEI1 (T1 + T2), problema test de 1/3:
1. 25 min: M1 pme/cm (Modelo Q1, Jul 2020 Q1). Hazlo 3 veces con datos distintos.
2. 25 min: M2 ηv y M3 Fr (Jul 2020 Q2 y Q3; ρ = p/(R·T), i = 1/2).
3. 20 min: M4 pérdidas mecánicas (PEC1 2022 Q1) y M5 balance con gases (PEC1 2022 Q6).
4. 15 min: M7 cogeneración y M6 turbo (Jul 2020 Q5; Ene 2013).
5. 15 min: M8 tiempos (retraso 1 ms, combustión 2.22 ms) y fórmulas de teoría.
6. 20 min: repite sin mirar los 3 del ejemplo de test, con cronómetro (75 min / 6 problemas ≈ 12 min cada uno).

PEC2 (T1 + T3), si lo necesitas después: G2 (Jul 2020 Q6, Ene 2024 Q4), G1 (Jul 2020 Q4), G3 (Jun 2013), G4 (Jun 2012).

## 6. Resultados de la fuente que no coinciden con mi recálculo

- Sep 2006 (MEC, 4T): la fuente mezcla cm y mm. Con D = 160 mm y S = 180 mm: pme = 2.31 MPa, no 0.0023 MPa.
- Jun 2006 (TG): no reproduzco 1099 kW, 2230.93 kW ni 24.25 %. El autor ya duda del apartado 2.
- Feb 2008 (vapor): potencia de bomba WB2 impresa 1946 kW; yo obtengo 1976.7 kW.
- Mar 2015 (MCIA, gases de escape): la fuente usa Fe = 0.055; el CH4 da 0.0583, que lleva a 970 °C en vez de 920 °C.
- Ejercicios PEC1 ej. 5: 55.33 kW solo sale con VT = 1268 cm³; la página parece decir 1768 cm³.
- PE1 2022/2023 Q4: impreso 37.9 kW; con los números sale 32.94 kW (wi ilegible: 1.2 o 1.7 kJ).
- PE1 2022/2023 Q5: We impreso 59.68 kW en algunos pasos; lo correcto es 51.63 kW (el 73.82 kW final es consistente con 51.63).
- Jun 2013 (ciclo combinado): 165.8 kg/s impreso, yo 165.3; E 68.49/68.79 MW impreso, yo 68.74.
- Ene 2024 TG Q3: la solución escribe T4 = 672.26 °C; eso es T4 − T1. T4 correcto = 965.3 K = 692.1 °C.
- Ene 2024 vapor simple y recalentamiento: números a mano parcialmente ilegibles (h5 3410 vs 3420; T4' = 280 °C de tabla, IAPWS da 281-289 °C según valores).
- Jul 2020 TG (solución a mano en MOTORESEJERCICIOSEXAMENES): T4s = 888 K y η = 35.8 % no salen con γ = 1.4 y cp = 1; la solución oficial del PDF Julio (T4 = 979.4 K, η = 35.3 %) sí cuadra.
- "Middle" Q1 y Q3: n difiere 1 %; ηv 67 % frente a 64.9 %.
- Test parte 1 con solución, pregunta 55: la clave marca 0.02 ms; el valor correcto es 2.22 ms y ninguna opción lo es.
- Vapor de la colección (Problemas-De-Todo 2.2): el manuscrito divide por h5−h2 en vez de h5−h2'; η = 0.282 frente a 0.332.
- Ciclo combinado 4.1 (Problemas-De-Todo): Fe(CH4) escrito 0.0777; correcto 0.0583.

## 7. Límites de este análisis

- Los problemas manuscritos de MOTORESEJERCICIOSEXAMENES se reconstruyeron desde esquemas y datos; algunos enunciados son aproximados. Páginas parcialmente ilegibles: 3, 6, 11, 13, 19, 20, 24, 25 de ese fichero.
- 23 entradas no tienen resultado de la fuente comparable (match = null en el JSON).
- Falta PEC1 2022 Q3: el escaneo no lo incluye.
- Los ficheros EjerciciosPEC2, Test-T3-PEC-2, PEC2_Problemas_Enero2026 y ResumenPEC2 (filas 33-37 del índice) no están descargados: no se cubrieron.
- Los problemas de las colecciones sin examen/año no se pueden fechar; el ranking cuenta problemas, no apariciones en convocatorias.
