# Regulación de electrolitos (selectividad iónica)

## Resumen
Un riñón biológico no solo filtra toxinas; también regula activamente los niveles de agua, sodio (Na⁺), potasio (K⁺), calcio (Ca²⁺), fósforo (PO₄³⁻) y pH. Los filtros puramente sintéticos (carbón activado, zeolitas) tienden a absorber toxinas de forma no selectiva, lo que podría eliminar también electrolitos esenciales.

Este documento describe cómo el riñón artificial propuesto aborda este desafío.

---

## El problema de los filtros sintéticos no selectivos

| Filtro | Capacidad | Problema |
|--------|-----------|----------|
| **Carbón activado** | Adsorbe moléculas orgánicas de alto peso molecular | No es selectivo; puede absorber vitaminas, hormonas, fármacos |
| **Zeolitas** | Adsorben amonio (NH₄⁺) y cationes | Pueden absorber también sodio y potasio |
| **Resinas de intercambio iónico** | Intercambian iones específicos | Pueden eliminar electrolitos esenciales si no se controlan |

**Riesgo clínico:** Si el filtro elimina electrolitos sin control, el paciente puede desarrollar hiponatremia (bajo sodio), hipopotasemia (bajo potasio), o desequilibrios de calcio y fósforo.

---

## Estrategia de regulación: sensores + control activo

### Capa 1: Filtro primario (membrana de nanoporos de silicio o PTFE)

| Parámetro | Valor | Función |
|-----------|-------|---------|
| **Tamaño de poro** | 10-50 nm | Permite paso de agua, urea, creatinina, electrolitos |
| **Material** | Silicio o PTFE | Alta precisión, baja adsorción no específica |

**Función en electrolitos:** No retiene electrolitos. Los deja pasar libremente hacia el filtrado (orina primaria).

### Capa 2: Filtro secundario (adsorción química multicapa)

| Capa | Material | Función | Selectividad |
|------|----------|---------|--------------|
| **Capa A** | Carbón activado de alta pureza | Adsorbe toxinas orgánicas de alto peso molecular | Baja selectividad (adsorbe todo) |
| **Capa B** | Resina de intercambio catiónico (ej. Amberlite IRP69) | Adsorbe amonio (NH₄⁺) y potasio (K⁺) | Selectividad controlable |
| **Capa C** | Resina de intercambio aniónico (ej. Dowex) | Adsorbe fosfato (PO₄³⁻) | Selectividad controlable |
| **Capa D** | Zeolita específica (ej. clinoptilolita) | Adsorbe amonio, baja afinidad por sodio | Media selectividad |

### Capa 3: Control activo por el microcontrolador

El dispositivo incorpora **sensores de electrolitos** en el filtrado (orina) y en la sangre (opcional). Según las lecturas, el microcontrolador ajusta:

| Sensor medido | Señal al paciente / acción |
|---------------|---------------------------|
| **Sodio bajo en sangre** | Alerta (el paciente debe consumir sal) |
| **Potasio alto en sangre** | Aumentar adsorción por resinas catiónicas |
| **Fósforo alto en sangre** | Aumentar adsorción por resinas aniónicas |
| **pH alterado** | Ajustar flujo o activar modo de corrección |

**Límite de la tecnología:** El dispositivo no puede añadir electrolitos (solo retirarlos). Por tanto, si el paciente elimina electrolitos en exceso, deberá reponerlos por vía oral.

---

## ¿Cómo se regula cada electrolito?

| Electrolito | Mecanismo de regulación en riñón natural | Cómo se imita en el dispositivo |
|-------------|------------------------------------------|--------------------------------|
| **Sodio (Na⁺)** | Reabsorción activa en túbulo proximal y asa de Henle | El dispositivo **no reabsorbe sodio**. El paciente debe regular su ingesta oral. |
| **Potasio (K⁺)** | Secreción en túbulo distal (control por aldosterona) | Resina de intercambio catiónico con adsorción controlada por el microcontrolador |
| **Calcio (Ca²⁺)** | Reabsorción dependiente de vitamina D y PTH | El dispositivo **no reabsorbe calcio**. El paciente debe regular su ingesta oral. |
| **Fósforo (PO₄³⁻)** | Reabsorción inhibida por PTH | Resina de intercambio aniónico (fosfato binders) |
| **Amonio (NH₄⁺)** | Secreción en túbulo colector | Zeolitas (clinoptilolita) o resinas catiónicas |
| **pH (bicarbonato)** | Reabsorción y regeneración de bicarbonato | El dispositivo **no regula pH**. El paciente debe mantener una dieta que evite la acidosis. |

---

## Limitaciones y advertencias

| Limitación | Consecuencia | Mitigación |
|------------|--------------|-------------|
| **No puede añadir electrolitos** | El paciente puede desarrollar déficit | Suplementación oral (dieta o pastillas) |
| **No puede regular sodio** | El sodio filtrado se pierde | El paciente debe consumir sal normalmente |
| **No puede regular pH** | Riesgo de acidosis metabólica | Dieta alcalina (frutas, verduras) o bicarbonato oral |
| **Las resinas se saturan** | Pérdida de capacidad de adsorción | Limpieza periódica por nanobots + recambio de resinas (no previsto) |

**Nota importante:** Este diseño no pretende imitar todas las funciones del riñón natural. Su objetivo es eliminar toxinas y permitir al paciente orinar normalmente. La regulación fina de electrolitos y pH recae en el paciente (dieta) y en el seguimiento médico.

---

## Próximos pasos para mejorar la selectividad

| Investigación | Objetivo | Plazo estimado |
|---------------|----------|----------------|
| Sensores de electrolitos MEMS (Na⁺, K⁺, Ca²⁺, pH) | Monitorización en tiempo real | Ya existen (tecnología comercial) |
| Resinas de intercambio iónico con regeneración química | Permitir que el dispositivo "lave" las resinas sin nanobots | En investigación |
| Biomímesis del túbulo renal (canales iónicos sintéticos) | Reabsorción activa de sodio y calcio | Futuro (10-20 años) |

---

## Conclusión

El riñón artificial propuesto **no regula electrolitos ni pH** de forma activa como un riñón natural. Su función principal es filtrar toxinas (urea, creatinina, fósforo) y permitir la micción normal. La regulación electrolítica recae en:

1. **La dieta del paciente** (ingesta de sal, potasio, calcio, bicarbonato)
2. **El seguimiento médico** (análisis de sangre periódicos)
3. **La suplementación oral** (si es necesario)

Este enfoque es similar al de la diálisis actual, donde el paciente también debe controlar su dieta y electrolitos. La ventaja es que el dispositivo elimina la necesidad de máquinas externas y cateterismos.

---

## Referencias

- Resinas de intercambio iónico en dispositivos médicos: Amberlite, Dowex
- Zeolitas (clinoptilolita) para adsorción de amonio: estudios en acuicultura y medicina
- Sensores de electrolitos MEMS: tecnología comercial (ej. Sensirion, TE Connectivity)
- Dieta en pacientes con insuficiencia renal: guías clínicas de la NKF (National Kidney Foundation)
