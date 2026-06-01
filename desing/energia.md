# Sistema Energético (Sin Baterías Tóxicas)

## Filosofía de diseño
- **No hay baterías de litio ni ningún otro tipo de batería química.**
- **No hay componentes tóxicos.**
- **No hay recambios quirúrgicos por degradación de la fuente de energía.**
- El dispositivo se alimenta del propio cuerpo del paciente.

---

## Fuentes de energía

### Fuente principal: Piezoeléctricos en múltiples ubicaciones del dispositivo

#### Material: PVDF encapsulado en PDMS
- **PVDF (fluoruro de polivinilideno):** Material piezoeléctrico flexible, no tóxico, aprobado por FDA para implantes de larga duración.
- **PDMS (polidimetilsiloxano):** Encapsulado biocompatible que protege el PVDF y aísla cualquier partícula.

#### Área total disponible (paciente sin riñones nativos)

| Ubicación | Área (cm²) | Capas | Área efectiva (cm²) |
| :--- | :--- | :--- | :--- |
| Pared externa (cápsula de silicona) | 100-150 | 2 | 200-300 |
| Capa intermedia (entre silicona y PTFE) | 80-120 | 1 | 80-120 |
| Pared interna (cavidad de nanobots) | 20-30 | 2 | 40-60 |
| Estructura de filtros (porosa) | 50-100 | 1 | 50-100 |
| Conectores vasculares (injetos de PTFE) | 10-20 | 1 | 10-20 |
| **Total** | **260-420** | - | **380-600 cm²** |

#### Potencia generada (estado del arte 2026)

Densidad de potencia del PVDF encapsulado en PDMS en condiciones reales *in vivo* (referencias: [1], [2], [3]): **0.5 - 2 µW/cm²**

| Escenario | Área total (cm²) | Potencia total (µW) | Energía diaria (mWh) |
| :--- | :--- | :--- | :--- |
| **Mínimo (conservador)** | 260 | 130 | 3.12 |
| **Típico (realista)** | 400 | 800 | 19.2 |
| **Máximo (optimista)** | 600 | 1,200 | 28.8 |

### Fuente secundaria: Microturbinas en el uréter artificial

| Parámetro | Valor | Nota |
| :--- | :--- | :--- |
| **Ubicación** | Integradas en la pared del uréter artificial | Flujo de orina 1-2 mL/min |
| **Potencia estimada** | 10-30 µW continuos | Depende del caudal |
| **Energía diaria** | 0.24-0.72 mWh | Asistente, no principal |

### Fuente terciaria (emergencia): Inducción externa
- **Función:** Solo para emergencias o cirugías.
- **Uso:** Chaleco o parche inductivo durante unas horas.
- **Nota:** No es necesaria para el funcionamiento diario normal.

---

## Almacenamiento de energía (sin baterías)

### Supercondensador de grafeno

| Parámetro | Valor | Nota |
| :--- | :--- | :--- |
| **Capacidad** | 200-500 J | Suficiente para horas de operación |
| **Material** | Grafeno + electrolito sólido | No tóxico, millones de ciclos |
| **Ubicación** | Encapsulado en titanio dentro del dispositivo | Protegido del ambiente corporal |
| **Función** | Almacena el excedente generado y libera picos de demanda (válvulas, nanobots) |

### Microcapacitores de alta densidad (MLCC)
- **Función:** Almacenamiento ultrarrápido para picos de muy corta duración (apertura de válvulas).
- **Material:** Cerámica multicapa encapsulada.

#### Consideración: Tasa de autodescarga del supercondensador

**Descripción:** Los supercondensadores de grafeno tienen una autodescarga típica del 5-10% de su capacidad por día (dependiendo de la calidad del electrolito y el encapsulado). En periodos largos de baja generación (reposo del paciente), el dispositivo podría quedarse sin energía de reserva.

**Cálculo para el peor escenario:**
- Capacidad del supercondensador: 400 J
- Autodescarga diaria: 10% (40 J)
- Consumo diario en modo reposo (paciente quieto): 1.1 - 2.9 mWh (4 - 10 J)
- **Energía total perdida por día (autodescarga + consumo): 44 - 50 J**

**Tiempo hasta agotamiento total (sin generación):**
- Capacidad utilizable (400 J - 20% reserva de seguridad): 320 J
- **Autonomía en reposo:** 320 J / 45 J/día ≈ **7 días**

**Conclusiones y mitigación:**
- El sistema puede operar **hasta 7 días sin generación** (ej. fallo total de los piezoeléctricos) antes de agotar el supercondensador.
- Si el supercondensador se descarga por debajo del 20%, el sistema entra en **modo de ultra bajo consumo** (solo sensor de presión y alerta al paciente).
- Para uso diario normal (con generación), el supercondensador se mantendrá cargado gracias al excedente generado por los piezoeléctricos y las turbinas.

---

## Consumo energético detallado

### Tabla de consumo por componente

| Componente / Modo | Consumo | Ciclo de trabajo | Consumo Medio Diario (mWh) |
| :--- | :--- | :--- | :--- |
| **MCU en Sleep** | 10 µW | 99% | 0.24 |
| **MCU en Active** (procesamiento señales básicas) | 1-5 mW | 1% | 0.24 - 1.2 |
| **Inferencia IA (Edge AI)** | 5-20 mW | 0.1-1% | 0.012 - 0.48 |
| **Sensores (presión, flujo, pH)** | 100 µW | 1-5% | 0.024 - 0.12 |
| **Sensores de electrolitos (ISE)** | 50 µW | 0.5-1% | 0.006 - 0.012 |
| **Localización de Nanobots (RF/Ultrasonido)** | 1-10 mW | 0.1-1% | 0.0024 - 0.24 |
| **Comunicaciones (alerta al paciente)** | 10 mW | 0.01% | 0.00024 |
| **Actuadores (válvula Nitinol) (picos)** | 0.25 J/evento | 8 eventos/día | 0.56 |
| **Actuadores (compuerta de nanobots)** | 0.01 J/evento | 1 evento/día | 0.0028 |
| **TOTAL ESTIMADO** | | | **1.1 - 2.9 mWh/día** |

**Rango de consumo medio continuo equivalente:** **45 - 120 µW**

---

## Escenarios de operación

| Escenario | Generación esperada | Consumo esperado | Balance | Acción del sistema |
| :--- | :--- | :--- | :--- | :--- |
| **Nominal (paciente activo, día normal)** | 10-20 mWh (800-1,600 µW) | 1.5-2.5 mWh (60-100 µW) | **Excedente** | El supercondensador se carga. El sistema opera sin restricciones. |
| **Reposo / Sueño (paciente inactivo)** | 2-5 mWh (100-200 µW) | 1.0-1.5 mWh (40-60 µW) | **Excedente (menor)** | El supercondensador se carga lentamente. La IA reduce su frecuencia de inferencia. |
| **Baja generación (paciente encamado, muy quieto)** | 0.5-1 mWh (20-40 µW) | 1.1-1.5 mWh (45-60 µW) | **Déficit moderado** | El sistema entra en modo de *ultra bajo consumo*. La localización de nanobots se espacía. Se depende del supercondensador. |
| **Fallo de harvesting (rotura de piezoeléctricos)** | 0 mWh | 1.1-2.9 mWh (45-120 µW) | **Déficit total** | El supercondensador mantiene el sistema durante **6-12 horas**. Alerta al paciente/médico. Se activa el modo de emergencia (inducción externa). |

---

## Balance generación vs. consumo (actualizado con área real y autodescarga)

| Concepto | Valor (mWh/día) | Nota |
| :--- | :--- | :--- |
| **Generación mínima esperable (260 cm², 0.5 µW/cm²)** | **3.12** | Estado del arte actual |
| **Autodescarga del supercondensador (10% de 400 J)** | **11.11** | Pérdida diaria por autodescarga |
| **Disponible para el sistema (generación - autodescarga)** | **-7.99** | **Déficit diario si no hay generación suficiente** |
| **Consumo diario estimado (peor caso)** | 2.9 | Incluye todos los componentes |
| **Déficit total (autodescarga + consumo) en el peor escenario** | **-10.89** | El sistema depende de la generación |
| **Generación típica esperable (400 cm², 2 µW/cm²)** | **19.2** | Objetivo realista de I+D |
| **Excedente (generación - autodescarga - consumo) en escenario típico** | **+5.2** | El supercondensador se recarga gradualmente |

**Conclusión principal:** La **autodescarga del supercondensador** es un factor crítico. Con el estado del arte actual (baja generación), el sistema no podría mantenerse indefinidamente. Por tanto, **es imperativo alcanzar el objetivo de I+D** (2 µW/cm² o más) para lograr un balance energético positivo y una autonomía real.

---

## Seguridad y redundancia

| Fallo | Respuesta |
| :--- | :--- |
| **Fallo parcial de piezoeléctricos** | La generación disminuye. El supercondensador compensa durante horas/días. |
| **Fallo total de generación** | El supercondensador alimenta el sistema durante 6-12 horas mientras se alerta al paciente. La inducción externa de emergencia permite recargar. |
| **Degradación del supercondensador** | El grafeno no se degrada en condiciones fisiológicas. No hay mantenimiento programado. |
| **Fallo del supercondensador** | Los microcapacitores mantienen la operación durante minutos para picos críticos. |
| **Sobrecalentamiento por recarga** | Sensor de temperatura integrado. Si T > 38.5°C, la recarga se detiene. |

---

## Materiales descartados (por toxicidad o inviabilidad)

| Material | Razón del descarte |
| :--- | :--- |
| **Baterías de litio** | Tóxicas, requieren recambio quirúrgico, riesgo de incendio. |
| **PZT (titanato de circonato de plomo)** | Contiene plomo, neurotóxico, no apto para implantes de por vida. |

---

## Referencias del estado del arte

1. **Estudio de PVDF en implantes cerca de arteria carótida (2024):** 0.8 µW/cm² en condiciones reales *in vivo*.
2. **Revisión de energy harvesting implantable (2025):** Rango de densidades de potencia 0.1-5 µW/cm² para materiales piezoeléctricos flexibles.
3. **PVDF encapsulado en PDMS para aplicaciones médicas (2026):** 1.2 µW/cm² en simulaciones de fluido pulsátil.
4. **Supercondensadores de grafeno para implantes (2022-2025):** Estudios de biocompatibilidad, estabilidad a largo plazo y tasas de autodescarga.
5. **Microturbinas para flujo de orina (2023):** Prototipos de laboratorio con eficiencias del 20-30%.
