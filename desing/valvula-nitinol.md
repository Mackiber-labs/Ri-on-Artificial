# Válvula de salida de Nitinol

## Resumen
La válvula de salida es el componente que permite vaciar la orina desde el riñón artificial hacia la vejiga. Está fabricada en **Nitinol (NiTi)** con **recubrimiento por CVD** (TiO₂ o DLC) para garantizar biocompatibilidad y evitar la liberación de níquel.

## Especificaciones técnicas

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Material** | Nitinol (NiTi, 50/50) | Superelástico, memoria de forma |
| **Recubrimiento** | TiO₂ o DLC por CVD | Espesor 10-200 nm |
| **Diámetro interno** | 5-8 mm | Similar al uréter humano |
| **Tiempo de apertura** | <100 ms | Pulso de corriente |
| **Tiempo de cierre** | <100 ms | Enfriamiento o pulso inverso |
| **Consumo por apertura/cierre** | 0.25 J | Solo durante el pico |
| **Frecuencia de vaciado** | 6-8 veces al día | Micciones normales |
| **Presión diferencial** | Hasta 100 cmH₂O | Soporta presión de la orina |

## Principio de funcionamiento (memoria de forma)

| Estado | Temperatura | Forma | Posición de la válvula |
|--------|-------------|-------|----------------------|
| **Martensita (frío)** | <34°C | Deformable (se comprime) | Cerrada (por defecto) |
| **Austenita (caliente)** | >36°C (corporal) | Recupera su forma original | Abierta (por pulso de corriente) |

**Ciclo de apertura:**
1. El microcontrolador envía un pulso de corriente (10 ms, 1-2 W).
2. El Nitinol se calienta por encima de su temperatura de transformación (36°C).
3. La válvula se abre (transición a austenita).
4. Tras 30-60 segundos, el microcontrolador interrumpe la corriente.
5. El Nitinol se enfría y la válvula vuelve a su estado cerrado (martensita).

**Consumo energético:** Solo durante el pulso de calentamiento. El resto del tiempo, consumo cero.

## Recubrimiento CVD (ver `recubrimiento-cvd.md` para detalles completos)

| Capa | Espesor | Función |
|------|---------|---------|
| **TiO₂ por CVD** | 10-100 nm | Pasivación avanzada, barrera al níquel |
| **DLC (carbono tipo diamante)** | 50-200 nm | Alta biocompatibilidad, reduce adhesión de proteínas |

**Liberación de níquel:** <1 µg/día (límite FDA: 35 µg/día). Seguro para implante crónico.

## Integración con el sistema de control

La válvula está conectada al microcontrolador (ver `control-ia.md`):

| Señal | Acción |
|-------|--------|
| `Abrir` | Pulso de corriente de 10 ms a 1-2 W |
| `Cerrar` | Corte de corriente (enfriamiento pasivo) |
| `Emergencia` | Modo manual: imán externo para abrir mecánicamente |

## Seguridad y redundancia

| Riesgo | Mitigación |
|--------|------------|
| **Fallo en posición cerrada** (retención aguda) | Válvula redundante (dos en paralelo) + modo manual de emergencia |
| **Fallo en posición abierta** (incontinencia) | Segunda válvula de respaldo + control por sensor de presión |
| **Fatiga térmica** | El Nitinol está diseñado para millones de ciclos (pruebas aceleradas) |
| **Liberación de níquel** | Recubrimiento CVD (TiO₂ o DLC) |

## Validación necesaria

| Prueba | Modelo | Criterio de éxito |
|--------|--------|-------------------|
| **Ciclos mecánicos** | Banco de pruebas (agua, 37°C) | >100,000 ciclos sin fallo |
| **Liberación de níquel** | Inmersión en solución salina, 12 meses | <1 µg/día |
| **Fatiga térmica** | Ciclos de calentamiento/enfriamiento | >10,000 ciclos sin degradación |

## Referencias

- Ver `recubrimiento-cvd.md` para detalles del recubrimiento
- Ver `materiales.md` para composición y seguridad del Nitinol
- Estudio de pasivado de Nitinol para dispositivos médicos (2025)
- FDA 510(k) para dispositivos de embolización con Nitinol recubierto
