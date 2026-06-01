# Especificaciones técnicas del riñón artificial implantable

## Filosofía de diseño
Este dispositivo está diseñado para pacientes con **enfermedad renal terminal (ERT)** que no tienen riñones funcionantes. Por tanto, **el espacio retroperitoneal está disponible** para alojar un dispositivo de mayor tamaño que un riñón sano. No hay competencia con el riñón nativo.

---

## Parámetros generales

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Dimensiones** | 10-15 cm (largo) × 6-8 cm (ancho) × 4-6 cm (grosor) | Aprovecha el espacio retroperitoneal |
| **Volumen total** | 300-600 mL | Similar a un riñón poliquístico o hipertrófico |
| **Peso** | 300-500 g | Aceptable para implante |
| **Material de la cápsula** | Silicona médica (grado implantable) | Flexible, biocompatible |
| **Revestimiento interno** | PTFE expandido (ePTFE) | Liso, antiadherente |

### Justificación del tamaño
En pacientes con enfermedad renal terminal (en diálisis), los riñones nativos:
- Han atrofiado (riñones pequeños y fibrosos) o
- Han sido extirpados (cistectomía radical por cáncer) o
- Son muy pequeños (riñones displásicos)

**El espacio retroperitoneal está disponible.** No hay competencia con el riñón nativo.

---

## Parámetros de filtración (aumentados por tamaño)

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Superficie de membrana (filtro primario)** | 100-200 cm² | Duplica la superficie de un riñón sano |
| **Tamaño de poro** | 10-50 nm | Basado en UCSF Kidney Project |
| **Material del filtro primario** | Silicio microporoso o PTFE | Alta precisión |
| **Tasa de filtración estimada** | 50-100 mL/min | Suficiente para eliminar toxinas |
| **Presión de trabajo** | 80-120 mmHg (presión arterial sistémica) | Sin bombas externas |
| **Caudal sanguíneo necesario** | 2-3 L/min | Dentro del gasto cardíaco total (4-6 L/min) |

### Filtro secundario (adsorción)

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Materiales** | Carbón activado + resinas de intercambio iónico + zeolitas | Multicapa |
| **Espesor total del filtro** | 10-15 mm | Mayor capacidad que en riñón sano |
| **Capacidad de adsorción de urea** | 20-40 g (estimado) | 2× un riñón sano |
| **Capacidad de adsorción de creatinina** | 10-20 g (estimado) | 2× un riñón sano |
| **Capacidad de adsorción de fósforo** | 10-20 g (estimado) | 2× un riñón sano |

---

## Parámetros energéticos (aumentados por tamaño)

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Área piezoeléctrica (PVDF+PDMS)** | 20-30 cm² | Mayor superficie de generación |
| **Potencia piezoeléctrica estimada** | 2-3 mW | 100 µW/cm² × área |
| **Energía diaria generada** | 48-72 mWh | Suficiente para consumo |
| **Microturbinas en uréter** | 10-30 µW | Asistente, mismo valor |
| **Supercondensador de grafeno** | 200-500 J | Mayor capacidad de almacenamiento |
| **Consumo diario estimado** | 2-3 mWh | Aumenta con el tamaño |
| **Margen de generación** | 20-30× | Muy holgado |

---

## Parámetros de la cavidad de nanobots (aumentada)

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Volumen de la cavidad** | 2-3 mL | Mayor colonia de nanobots |
| **Capacidad de nanobots** | 10⁵-10⁶ unidades | Suficiente para años de limpieza |
| **Compuerta** | Nitinol con CVD | Controlada por microcontrolador |

---

## Parámetros de control de glucosa (opcional, extensión futura)

| Parámetro | Valor | Nota |
|-----------|-------|------|
| **Reservorio de insulina** | 2-5 mL | Insulina concentrada (U-500) |
| **Autonomía del reservorio** | 30-90 días | Depende del consumo del paciente |
| **Recarga de insulina** | Inyección subcutánea mensual | Como bombas de insulina actuales |
| **Sensor de glucosa** | MEMS electroquímico | Rango 40-600 mg/dL |

---

## Comparación con riñón sano

| Aspecto | Riñón sano (2 unidades) | Dispositivo propuesto |
|---------|-------------------------|----------------------|
| **Volumen total** | ~300 mL | 300-600 mL |
| **Tasa de filtración** | 90-120 mL/min | 50-100 mL/min |
| **Caudal sanguíneo** | 1.2 L/min | 2-3 L/min |
| **Regulación de electrolitos** | Sí (fina) | Parcial (requiere dieta) |
| **Regulación de pH** | Sí | No (requiere dieta) |
| **Producción de hormonas (EPO, renina)** | Sí | No (requiere inyecciones) |
| **Control de glucosa** | Sí (indirecto) | Opcional (extensión futura) |

**Conclusión:** El dispositivo no iguala todas las funciones de un riñón sano, pero es **suficiente para eliminar toxinas y permitir al paciente orinar sin diálisis**. Las funciones faltantes (electrolitos, pH, hormonas) se suplen con dieta, medicación oral o inyecciones (EPO).

---

## Referencias

- Tamaño de riñón humano: anatomía estándar (Gray's Anatomy)
- Gasto cardíaco humano: 4-6 L/min (fisiología estándar)
- UCSF Kidney Project: tasas de filtración con membranas de silicio
- Bombas de insulina implantables: datos de autonomía y recarga (Medtronic, Insulet)
