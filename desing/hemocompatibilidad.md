# Hemocompatibilidad y prevención de trombosis

## Resumen
El contacto de la sangre con superficies sintéticas (silicio, PTFE, Nitinol) activa la cascada de coagulación, lo que puede provocar la formación de trombos (coágulos) dentro del dispositivo o en los vasos conectados. Este documento describe las estrategias integradas en el diseño para minimizar este riesgo.

---

## El problema: ¿Por qué la sangre coagula?

| Superficie | Reacción del cuerpo | Consecuencia |
|------------|---------------------|--------------|
| **Materiales sintéticos no tratados** | Adhesión de proteínas (fibrinógeno) → activación de plaquetas → cascada de coagulación | Trombos que pueden obstruir el filtro o embolizar |
| **Superficies rugosas o con bordes cortantes** | Daño mecánico a glóbulos rojos (hemólisis) y plaquetas | Liberación de factores procoagulantes |

---

## Estrategias de mitigación integradas en el diseño

### 1. Recubrimientos biocompatibles (Capa pasiva)

| Componente | Recubrimiento | Función anti-trombótica |
|------------|---------------|--------------------------|
| **Membrana de nanoporos (silicio)** | Heparina inmovilizada o polímeros zwitteriónicos | La heparina inactiva la trombina; los polímeros zwitteriónicos repelen proteínas |
| **Válvula de Nitinol** | CVD (TiO₂ o DLC) | Superficie inerte, lisa, reduce adhesión plaquetaria |
| **Cápsula de silicona** | PTFE interno (Gore-Tex®) | Superficie lisa, baja energía superficial, antiadherente |
| **Microturbinas** | PDMS o DLC | Elimina bordes cortantes, superficies hidrófilas |

### 2. Geometría y fluidos (Diseño hemodinámico)

| Principio | Aplicación en el dispositivo |
|-----------|------------------------------|
| **Flujo laminar** | Canales de sangre sin esquinas agudas ni estrechamientos bruscos |
| **Evitar estancamiento** | Geometría que evita zonas de remanso (donde se forman coágulos) |
| **Cizallamiento controlado** | Tensión cortante entre 1-5 Pa (fisiológico), evita daño celular |

### 3. Selección de materiales intrínsecamente compatibles

| Material | Propiedad hemocompatible |
|----------|--------------------------|
| **PTFE** | Baja adhesión proteica, usado en injertos vasculares |
| **Titanio (óxido nativo)** | Superficie inerte, similar al hueso, no activa coagulación |
| **PDMS** | Superficie hidrófoba, baja adhesión celular |
| **Grafeno (supercondensador)** | Encapsulado en titanio, no expuesto a sangre |

### 4. Mantenimiento y monitoreo

| Medida | Frecuencia | Propósito |
|--------|------------|-----------|
| **Ecografía Doppler del injerto** | Anual | Detectar trombos en las anastomosis |
| **Análisis de sangre** | Trimestral | Medir dímero D (marcador de trombosis) |
| **Anticoagulación profiláctica** | Según riesgo del paciente | Aspirina a dosis baja (100 mg/día) si hay antecedentes |

**Nota importante:** El diseño aspira a **no requerir anticoagulación crónica** (warfarina, rivaroxabán), pero algunos pacientes de alto riesgo podrían necesitar antiagregantes (aspirina). Esto se decide caso por caso.

---

## Comparación con dispositivos actuales

| Dispositivo | Anticoagulación requerida | Riesgo de trombosis |
|-------------|---------------------------|---------------------|
| **SynCardia (corazón)** | Warfarina (INR 2.5-3.5) obligatoria | Alto (gasto anticoagulante) |
| **Hemodiálisis** | Heparina durante la sesión | Bajo (solo en el circuito) |
| **Este riñón artificial** | **Aspirina solo si hay riesgo** | **Bajo** (diseño optimizado) |

---

## Validación necesaria

| Prueba | Modelo | Criterio de éxito |
|--------|--------|-------------------|
| **Tiempo de trombosis** | Circulación ex vivo (sangre humana, 4-6 horas) | Sin caída de flujo >20% |
| **Adhesión plaquetaria** | Microscopía electrónica | <5% de área cubierta |
| **Estudio en animales** | Cerdo o cordero, 6 meses | Sin trombos clínicamente significativos |

---

## Referencias

- Heparina inmovilizada: estándar en stents y catéteres (ensayos clínicos)
- Polímeros zwitteriónicos (PCB, PSB): estudios de hemocompatibilidad (2020-2025)
- DLC y TiO₂ por CVD: aprobados en cabezas de prótesis de cadera y válvulas cardíacas
- PTFE en injertos vasculares: seguimiento a 20 años sin trombosis en la mayoría
