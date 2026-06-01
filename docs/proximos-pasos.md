# Próximos pasos para la validación del riñón artificial

## Resumen
Este documento describe el plan experimental para validar el riñón artificial, desde la simulación computacional hasta los ensayos clínicos en humanos. Los pasos están ordenados por creciente complejidad y costo.

---

## Fase 0: Simulación y modelado (6-12 meses)

| Actividad | Herramienta | Objetivo |
|-----------|-------------|----------|
| **Dinámica de fluidos (CFD)** | COMSOL, ANSYS Fluent | Optimizar la membrana de nanoporos, evitar zonas de estancamiento |
| **Modelado electromagnético** | CST Studio, FEMM | Calcular la eficiencia de las microturbinas y la inducción |
| **Simulación de nanobots** | Software de dinámica molecular | Evaluar la capacidad de limpieza del filtro secundario |
| **Balance energético** | Matlab / Python | Verificar que la generación (piezo + turbinas) cubre el consumo |

**Entregable:** Modelo computacional validado, especificaciones finales.

---

## Fase 1: Prototipo de laboratorio (12-18 meses)

| Componente | Actividad | Criterio de éxito |
|------------|-----------|-------------------|
| **Filtro primario** | Fabricar membrana de nanoporos de silicio (10 cm²) | Tasa de filtración >30 mL/min a 100 mmHg |
| **Filtro secundario** | Construir columna de adsorción (carbón + resinas + zeolitas) | Capacidad de adsorción de urea >10 g |
| **Microturbinas** | Prototipo de turbina en circuito de flujo | Generación >10 µW con flujo de 1 mL/min |
| **Piezoeléctricos** | Fabricar película de PVDF+PDMS de 10 cm² | Generación >0.5 mW con vibración simulada (100 Hz) |
| **Nanobots** | Prototipo de nanobots de silicio+PLGA (1-10 µm) | Movilidad controlada por campo magnético |

**Entregable:** Prototipo de banco funcional (sin implantar).

---

## Fase 2: Pruebas ex vivo (6-12 meses)

| Modelo | Descripción | Objetivo |
|--------|-------------|----------|
| **Sangre humana (circuito cerrado)** | Conectar el dispositivo a un depósito de sangre heparinizada | Evaluar hemocompatibilidad, filtración, consumo energético |
| **Orina simulada (circuito independiente)** | Hacer circular orina artificial por el uréter | Probar microturbinas y sistema de limpieza (nanobots) |

**Duración del experimento:** 24-72 horas continuas.

**Entregable:** Datos de rendimiento en condiciones fisiológicas simuladas.

---

## Fase 3: Pruebas en animales pequeños (12-18 meses)

| Modelo animal | Procedimiento | Objetivo |
|---------------|---------------|----------|
| **Rata** (nefrectomizada) | Implantar una versión miniaturizada del dispositivo (factor 1:10) | Evaluar biocompatibilidad básica, ausencia de toxicidad aguda |

**Duración del seguimiento:** 1-3 meses.

**Criterios de éxito:**
- Supervivencia del animal sin diálisis externa
- Urea sanguínea <100 mg/dL
- Sin trombosis visible en los vasos conectados

**Entregable:** Prueba de concepto en mamífero pequeño.

---

## Fase 4: Pruebas en animales grandes (24-36 meses)

| Modelo animal | Procedimiento | Objetivo |
|---------------|---------------|----------|
| **Cerdo o cordero** (nefrectomía unilateral + ligadura parcial del otro riñón) | Implantar el dispositivo a escala real (1:1) | Evaluar eficacia, seguridad, durabilidad a medio plazo |

**Duración del seguimiento:** 6-12 meses.

**Criterios de éxito:**
- Supervivencia con función renal residual mínima (similar a ERT)
- Descenso de urea y creatinina a niveles casi normales
- Formación de coágulos: ausente o mínima
- Degradación de nanobots: ocurre en el plazo previsto (6-9 meses)

**Entregable:** Datos preclínicos para solicitud de ensayo clínico.

---

## Fase 5: Ensayo clínico en humanos (5-10 años)

| Fase | Pacientes | Objetivo | Duración |
|------|-----------|----------|----------|
| **I (seguridad)** | 5-10 | Seguridad a corto plazo (infección, trombosis, eventos adversos) | 6 meses |
| **II (eficacia preliminar)** | 20-30 | Reducción de urea y creatinina, calidad de vida | 12 meses |
| **III (ensayo controlado)** | 100-200 | Comparar con diálisis estándar (supervivencia, complicaciones) | 2-3 años |

**Criterios de inclusión:** Pacientes en lista de espera para trasplante renal, con buena función cardíaca.

**Entregable:** Aprobación regulatoria (FDA, CE) para uso clínico.

---

## Resumen de tiempos

| Fase | Duración estimada | Coste estimado |
|------|-------------------|----------------|
| 0: Simulación | 6-12 meses | $50-100k |
| 1: Prototipo laboratorio | 12-18 meses | $200-500k |
| 2: Pruebas ex vivo | 6-12 meses | $50-100k |
| 3: Animales pequeños | 12-18 meses | $100-200k |
| 4: Animales grandes | 24-36 meses | $1-3M |
| 5: Ensayo clínico | 60-120 meses | $10-30M |
| **Total** | **10-15 años** | **$11-34M** |

**Nota:** Los costes son estimaciones gruesas. Una empresa con experiencia podría reducirlos a la mitad.

---

## Próximos pasos inmediatos (próximos 6 meses)

- [ ] **Financiamiento:** Buscar subvenciones (NIH, Horizon Europe, KidneyX) o inversores ángeles.
- [ ] **Equipo:** Formar un grupo multidisciplinario (ingenieros de fluidos, especialistas en MEMS, veterinarios).
- [ ] **Prototipo rápido:** Comprar una membrana de nanoporos comercial (SiMPore) y acoplarla a un sistema de adsorción de laboratorio.
- [ ] **Simulación:** Ejecutar CFD de la membrana y las microturbinas.
