# Sistema de limpieza por nanobots alojados en cavidad resguardada

## Resumen
En lugar de una pastilla oral cuyos quelantes viajan por toda la sangre, este diseño utiliza un enjambre de nanobots alojados en una cavidad dentro del propio riñón artificial. Los nanobots salen solo cuando el filtro secundario está saturado, realizan la limpieza localmente y regresan a la cavidad para recargarse.

---

## Componentes del sistema

### Cavidad de almacenamiento

| Parámetro | Especificación |
|-----------|----------------|
| **Volumen** | 0.5-1 mL |
| **Material** | Titanio o cerámica médica |
| **Compuerta de salida** | Nitinol con recubrimiento CVD (TiO₂ o DLC) |
| **Control de compuerta** | Microcontrolador (se abre por señal eléctrica) |
| **Medio de suspensión** | Líquido fisiológico estéril (similar al fluido sinovial) |
| **Recarga inalámbrica** | Bobina receptora en la cavidad (inducción) |

### Nanobots

| Parámetro | Especificación |
|-----------|----------------|
| **Tamaño** | 1-10 µm |
| **Material** | Silicio + PLGA (copolímero de ácido láctico-glicólico) |
| **Función principal** | Romper enlaces entre toxinas y el filtro secundario |
| **Mecanismo de limpieza** | Mecánico (microturbulencia local) o químico (liberación de enzimas) |
| **Propulsión** | Flagelos artificiales (como bacterias) o gradiente químico (quimiotaxis) |
| **Energía** | Microbatería recargable por inducción (desde la cavidad) |
| **Autonomía por misión** | 30-60 minutos |
| **Comunicación** | Señal de RF de muy baja potencia o campo magnético |
| **Biodegradabilidad** | Sí (PLGA), se degrada en 6-12 meses si no recibe señal de recarga |

---

## Ciclo de limpieza

| Fase | Acción | Duración estimada |
|------|--------|-------------------|
| **1. Activación** | El microcontrolador detecta saturación del filtro secundario (caída de flujo o aumento de presión) | Automático |
| **2. Apertura** | Se abre la compuerta de la cavidad | 1 segundo |
| **3. Despliegue** | Los nanobots salen y navegan hacia el filtro secundario (quimiotaxis o campo magnético) | 1-5 minutos |
| **4. Limpieza** | Nanobots rompen enlaces toxina-filtro | 10-30 minutos |
| **5. Retirada** | Nanobots regresan a la cavidad | 5-10 minutos |
| **6. Recarga** | Inducción inalámbrica recarga los nanobots en la cavidad | 30-60 minutos |
| **7. Eliminación de toxinas** | Las toxinas liberadas salen por la orina (vejiga → uretra) | Natural |

---

## Ventajas sobre pastilla oral

| Aspecto | Pastilla oral quelante | Nanobots alojados |
|---------|------------------------|-------------------|
| **Selectividad** | Baja (circulan por todo el cuerpo) | Alta (solo actúan dentro del dispositivo) |
| **Toxicidad sistémica** | Riesgo real | Muy bajo (no salen del riñón artificial) |
| **Mantenimiento** | Pastilla periódica | Inyección intramuscular cada 6-12 meses |
| **Autonomía del paciente** | Debe recordar tomar la pastilla | El dispositivo alerta antes de quedarse sin nanobots |
| **Eficiencia** | Variable (depende de absorción) | Controlada (limpieza local directa) |

---

## Seguridad y mitigación de riesgos

| Riesgo | Solución |
|--------|----------|
| **Nanobot perdido** | Biodegradable (PLGA) en 6-12 meses si no recibe señal de recarga |
| **Nanobot defectuoso** | Autodesecho programado + expulsión por orina (ver `autodesecho.md`) |
| **Fallo de comunicación** | El microcontrolador detecta silencio y lanza una segunda oleada |
| **Saturación de la cavidad** | Capacidad para 10,000 nanobots (suficiente para años de limpieza) |
| **Toxicidad del silicio** | El silicio es biocompatible; el PLGA es biodegradable y aprobado por FDA |
| **Reacción alérgica** | La suspensión es fisiológica estéril (bajo riesgo) |

---

## Referencias

- Atala A, et al. (2006). Tissue-engineered bladders. *The Lancet* (andamios de PLGA)
- Estudios de nanobots para limpieza de filtros (literatura emergente, 2020-2025)
- PLGA para dispositivos médicos: aprobaciones FDA
