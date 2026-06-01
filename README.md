![License](https://img.shields.io/badge/License-Copyright%20%E2%84%97%20Enrique%20Aguayo-red)
![Non-commercial](https://img.shields.io/badge/Non--commercial-Required-orange)
![No Modification](https://img.shields.io/badge/No%20Modification-Without%20Permission-red)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20465118-blue)](https://doi.org/10.5281/zenodo.20465118)
![Status](https://img.shields.io/badge/Status-Hypothesis%20(Conceptual)-yellow)
![Language](https://img.shields.io/badge/Language-Spanish-red)

# Riñón Artificial Implantable con Limpieza por Nanobots

**Estado del proyecto:** Hipótesis de diseño conceptual. Documentación en progreso.

---

## Resumen

La hemodiálisis crónica afecta a más de 2.5 millones de personas en el mundo. Los pacientes viven atados a una máquina: 3-4 sesiones semanales, 4 horas cada vez, agujas en el brazo, sin poder viajar, sin poder trabajar, sin poder vivir con normalidad. La diálisis prolonga la vida, pero destruye la dignidad y la autonomía.

Este documento propone un **riñón artificial totalmente implantable** que devuelve al paciente la capacidad de orinar con normalidad, cuando él quiere, donde él quiere. Sin componentes externos. Sin bolsas. Sin máquinas.

### Innovaciones principales del diseño

| Área | Innovación | Descripción |
|------|------------|-------------|
| **Filtración** | Membrana de nanoporos (silicio) + adsorción química multicapa | Sin células vivas. Carbón activado, resinas de intercambio iónico y zeolitas retienen urea, creatinina, fósforo. |
| **Limpieza** | Nanobots alojados en cavidad con recarga inalámbrica | Los nanobots (1-10 µm) salen, limpian el filtro y regresan. Reposición por inyección intramuscular cada 6-12 meses. Autodesecho por orina si fallan. |
| **Energía** | PVDF+PDMS (piezoeléctricos) + microturbinas en uréter + supercondensador de grafeno | **Sin baterías tóxicas.** Generación continua por vibración corporal y flujo de orina. Autonomía teórica indefinida. |
| **Materiales** | Silicona médica, PTFE, Nitinol con CVD (TiO₂ o DLC), PVDF encapsulado | Todos biocompatibles. Ningún material tóxico. Liberación de níquel <1 µg/día (límite FDA 35 µg/día). |
| **Control** | Microcontrolador ultra bajo consumo + sensores de presión, flujo, pH y electrolitos | Algoritmo de micción automática. Modo manual de emergencia. |
| **Mantenimiento** | Diseño modular extraíble | Si falla o queda obsoleto, se reemplaza quirúrgicamente como un marcapasos. |

### Componentes principales

- **Filtro primario:** Membrana de nanoporos de silicio o PTFE (basada en UCSF Kidney Project)
- **Filtro secundario:** Adsorción química multicapa (carbón + resinas + zeolitas)
- **Limpieza:** Nanobots alojados + inyección intramuscular de recambio
- **Energía:** PVDF+PDMS (piezoeléctricos en la pared externa) + microturbinas en uréter + supercondensador de grafeno
- **Válvula:** Nitinol con recubrimiento CVD (TiO₂ o DLC) para evitar liberación de níquel
- **Control:** Microcontrolador ultra bajo consumo (Texas Instruments MSP430 o STM32L)
- **Sensores:** Presión (MEMS), flujo (ultrasónico), pH (electrodo), electrolitos (ISE)

---

## Estructura del repositorio

| Carpeta | Contenido |
|---------|-----------|
| `docs/` | Especificaciones, materiales, limitaciones, próximos pasos, referencias |
| `design/` | Diseño técnico de filtros, energía, válvula, control, hemocompatibilidad |
| `cleaning/` | Sistema de limpieza por nanobots y gestión de colonia |
| `figs/` | Diagramas, esquemas, renders 2D del dispositivo |
| `cad/` | Modelos 3D editables (.stl, .step, .blend) para impresión o simulación |

---

## Documentos disponibles

| Archivo | Descripción |
|---------|-------------|
| `docs/especificaciones.md` | Parámetros técnicos (tamaño, peso, flujo, presión) |
| `docs/materiales.md` | Materiales médicos utilizados y su justificación de seguridad |
| `docs/limitaciones.md` | Desafíos técnicos y regulatorios |
| `docs/proximos-pasos.md` | Plan de validación experimental |
| `docs/referencias.md` | Referencias bibliográficas |
| `design/filtro-primario.md` | Membrana de nanoporos: diseño y funcionamiento |
| `design/filtro-secundario.md` | Adsorción química multicapa: capacidad y saturación |
| `design/energia.md` | PVDF+PDMS, microturbinas, supercondensador de grafeno |
| `design/valvula-nitinol.md` | Válvula de Nitinol con recubrimiento CVD |
| `design/selectividad-ionica.md` | Regulación de sodio, potasio, calcio, pH |
| `design/hemocompatibilidad.md` | Prevención de coágulos |
| `design/control-ia.md` | Microcontrolador, sensores, algoritmo |
| `design/filosofia-mantenimiento.md` | Reemplazo quirúrgico y obsolescencia |
| `cleaning/limpieza-nanobots.md` | Nanobots: diseño, función, recarga inalámbrica |
| `cleaning/gestion-colonia.md` | Monitoreo, inyección intramuscular, autodesecho |

---

## Imágenes del diseño

| Imagen | Descripción |
|--------|-------------|
| 
| `figs/Figuras : 1,2,3 y 4, referenciales` | Corte transversal con las capas del dispositivo |


## Próximos pasos

- [ ] Simulación del flujo de orina en las microturbinas (CFD)
- [ ] Pruebas de adsorción del filtro secundario (in vitro)
- [ ] Validación del sistema de nanobots (movilidad, limpieza, recarga)
- [ ] Búsqueda de colaboradores para ensayos preclínicos

---

## Licencia

Copyright © 2026 Enrique Aguayo. Todos los derechos reservados.

Este proyecto está protegido por derechos de autor.

**PERMITIDO:**
- Uso no comercial con fines educativos o de investigación.
- Distribución sin modificación, siempre que se mantenga esta licencia y se dé crédito al autor.

**PROHIBIDO** sin autorización expresa por escrito:
- Uso comercial (incluyendo, pero no limitado a: ofrecerlo como servicio, SaaS, suscripción, integración en productos que generen ingresos, o cualquier uso que genere beneficio económico directo o indirecto).
- Modificación para entornos de producción.
- Distribución de versiones modificadas sin autorización.

Para licencias comerciales, soporte técnico, pilotos empresariales o consultas:  
Contacto: **eaguayo@migst.cl**

Cualquier uso fuera de los términos permitidos requiere permiso previo del autor.  
Las consultas comerciales son bienvenidas y se responderán en un plazo máximo de 7 días hábiles.

---

## Autor

**Enrique Aguayo H.**  
Mackiber Labs  
ORCID: 0009-0004-4615-6825  
GitHub: [@Mackiber-labs](https://github.com/Mackiber-labs)  
Contacto: eaguayo@migst.cl
