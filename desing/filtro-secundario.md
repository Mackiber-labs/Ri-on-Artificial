# Filtro secundario: adsorción química multicapa

## Resumen
El filtro secundario complementa al filtro primario. Mientras que el filtro primario separa toxinas por tamaño, el filtro secundario las **retiene por adsorción química**. Está compuesto por una combinación de carbón activado, resinas de intercambio iónico y zeolitas.

---

## Arquitectura multicapa

La sangre filtrada (filtrado glomerular) pasa a través de varias capas en serie:

| Capa | Material | Función | Espesor |
|------|----------|---------|---------|
| **1** | Carbón activado de alta pureza | Adsorbe toxinas orgánicas de alto peso molecular (β2-microglobulina, hormonas) | 1-2 mm |
| **2** | Resina de intercambio catiónico (ej. Amberlite IRP69) | Adsorbe amonio (NH₄⁺) y potasio (K⁺) | 1-2 mm |
| **3** | Resina de intercambio aniónico (ej. Dowex) | Adsorbe fosfato (PO₄³⁻) | 1-2 mm |
| **4** | Zeolita específica (ej. clinoptilolita) | Adsorbe amonio, baja afinidad por sodio | 1-2 mm |
| **5** | Carbón activado de pureza ultra alta (pulido final) | Elimina toxinas residuales | 0.5-1 mm |

**Espesor total del filtro secundario:** 5-9 mm.

---

## Capacidad de adsorción estimada

| Toxina / Electrolito | Capacidad de adsorción | Nota |
|---------------------|------------------------|------|
| **Urea** | 10-20 g | Requiere validación |
| **Creatinina** | 5-10 g | Requiere validación |
| **Fósforo (PO₄³⁻)** | 5-10 g | Requiere validación |
| **Amonio (NH₄⁺)** | 5-10 g | Requiere validación |
| **Potasio (K⁺)** | 5-10 g | Requiere validación |
| **β2-microglobulina** | 1-5 g | Molécula de mayor tamaño |

**Vida útil estimada del filtro secundario (antes de saturación):** 1-3 meses (dependiendo de la carga de toxinas del paciente). La limpieza por nanobots regenera el filtro, extendiendo su vida útil indefinidamente.

---

## Mecanismo de adsorción

### Carbón activado
- **Mecanismo:** Adsorción física (fuerzas de Van der Waals)
- **Selectividad:** Baja (adsorbe una amplia gama de moléculas orgánicas)
- **Regeneración:** Posible por lavado con solventes o calor (no aplicable in vivo)

### Resinas de intercambio iónico
- **Mecanismo:** Intercambio químico reversible
- **Selectividad:** Controlable (según el grupo funcional de la resina)
- **Regeneración:** Posible por lavado con soluciones concentradas de iones

### Zeolitas
- **Mecanismo:** Adsorción molecular por tamaño de poro (tamiz molecular)
- **Selectividad:** Alta para amonio y cationes pequeños
- **Regeneración:** Posible por lavado con soluciones salinas

---

## Limitaciones del filtro secundario

| Limitación | Consecuencia | Mitigación |
|------------|--------------|-------------|
| **Adsorción no selectiva** | Puede eliminar electrolitos esenciales (Na⁺, Ca²⁺) | Control por sensores + dieta del paciente |
| **Saturación** | Pérdida de capacidad de adsorción | Limpieza periódica por nanobots |
| **Regeneración química in vivo** | Difícil sin nanobots | Los nanobots son la solución principal |
| **Fuga de partículas** | Riesgo de embolización | Encapsulado en mallas de PTFE |

---

## Integración con el sistema de limpieza por nanobots

Cuando el filtro secundario se satura, el microcontrolador activa el sistema de limpieza:

1. **Nanobots** salen de la cavidad.
2. Navegan hacia el filtro secundario.
3. Rompen los enlaces entre toxinas y adsorbentes.
4. Las toxinas liberadas salen por la orina.
5. El filtro queda regenerado.

Este ciclo puede repetirse **cientos de veces** a lo largo de la vida del dispositivo.

---

## Materiales específicos recomendados

| Componente | Material específico | Proveedor / Referencia |
|------------|---------------------|------------------------|
| **Carbón activado** | Norit A Supra EUR | Cabot Norit |
| **Resina catiónica** | Amberlite IRP69 (polacrilex) | DuPont / Rohm & Haas |
| **Resina aniónica** | Dowex (cloruro de colestiramina) | Dow Chemical |
| **Zeolita** | Clinoptilolita (grado médico) | Varios proveedores |

---

## Próximos pasos para la validación

1. **Pruebas de adsorción in vitro:** Hacer pasar plasma simulado con concentraciones conocidas de urea, creatinina, fósforo.
2. **Medición de capacidad de saturación:** Determinar cuántos gramos de cada toxina puede adsorber el filtro.
3. **Pruebas de regeneración por nanobots:** Simular la limpieza con nanobots en un modelo de laboratorio.
4. **Estudios de biocompatibilidad:** Evaluar la liberación de partículas y la respuesta celular.

---

## Referencias

- Carbón activado en dispositivos médicos: uso en filtros de diálisis y hemoperfusión
- Resinas de intercambio iónico: Amberlite, Dowex (fichas técnicas de fabricantes)
- Zeolitas (clinoptilolita): estudios en acuicultura y medicina
- Regeneración de adsorbentes: técnicas de limpieza química y térmica
