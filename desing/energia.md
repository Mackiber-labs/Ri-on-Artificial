# Sistema energético (sin baterías tóxicas)

## Filosofía de diseño
- **No hay baterías de litio ni ningún otro tipo de batería química.**
- **No hay componentes tóxicos.**
- **No hay recambios quirúrgicos por degradación de la fuente de energía.**

---

## Fuentes de energía

### Fuente principal: Piezoeléctricos en la subcapa del riñón artificial

#### Material: PVDF encapsulado en PDMS

| Parámetro | Valor |
|-----------|-------|
| **Material activo** | PVDF (fluoruro de polivinilideno) |
| **Encapsulado** | PDMS (polidimetilsiloxano), 100-300 µm |
| **Ubicación** | Capa intermedia del dispositivo (10 cm²) |
| **Activación** | Vibración del pulso sanguíneo + movimiento corporal |
| **Potencia estimada** | 1 mW continuos (100 µW/cm² × 10 cm²) |
| **Energía diaria** | 24 mWh |

#### Seguridad del PVDF+PDMS
- **Toxicidad:** No tóxica (aprobado por FDA para implantes de larga duración)
- **Biocompatibilidad:** Demostrada in vitro e in vivo (roedores, 6 semanas, sin inflamación)
- **Degradación:** No biodegradable (estable décadas)
- **Materiales descartados:** PZT (contiene plomo, neurotóxico)

### Fuente secundaria: Microturbinas en el uréter artificial

| Parámetro | Valor |
|-----------|-------|
| **Ubicación** | Integradas en el uréter artificial |
| **Caudal de orina** | 0.5-1.5 L/día |
| **Presión en uréter** | 10-20 cmH₂O (1-2 kPa) |
| **Potencia estimada** | 10-30 µW continuos |
| **Energía diaria** | 0.24-0.72 mWh |
| **Función** | Respaldo durante períodos de inactividad prolongada |

### Fuente terciaria (emergencia): Inducción externa
- **Función:** Solo para emergencias o cirugías
- **Uso:** Chaleco o parche inductivo durante unas horas
- **Nota:** No es necesaria para el funcionamiento diario normal

---

## Almacenamiento de energía (sin baterías)

### Supercondensador de grafeno

| Parámetro | Valor |
|-----------|-------|
| **Capacidad** | 100-500 J |
| **Material** | Grafeno + electrolito sólido |
| **Ventajas** | No tóxico, millones de ciclos, no se degrada, no requiere recambio |
| **Ubicación** | Encapsulado en titanio dentro del dispositivo |
| **Función** | Almacena el excedente generado por los piezoeléctricos |

### Microcapacitores de alta densidad
- **Función:** Almacenamiento ultrarrápido para picos de demanda (válvulas Nitinol)
- **Material:** Cerámica multicapa (MLCC) encapsulada

---

## Cálculo de generación vs. consumo

| Concepto | Valor |
|----------|-------|
| **Generación diaria (piezoeléctricos)** | 24 mWh |
| **Generación diaria (microturbinas)** | 0.24 mWh |
| **Total generado** | **24.24 mWh** |
| **Consumo diario estimado** | 1.8 mWh |
| **Margen de seguridad** | **13×** |

---

## Seguridad y redundancia

| Fallo | Respuesta |
|-------|-----------|
| **Fallo de piezoeléctricos** | Las microturbinas mantienen el sistema en modo de bajo consumo durante días |
| **Fallo total de generación** | Inducción externa de emergencia (recarga del supercondensador) |
| **Degradación** | El supercondensador de grafeno no se degrada. No hay mantenimiento programado |
| **Fallo del supercondensador** | Los microcapacitores mantienen la operación durante horas |

---

## Materiales descartados (por toxicidad)

| Material | Razón |
|----------|-------|
| **Baterías de litio** | Tóxicas, requieren recambio quirúrgico, riesgo de incendio |
| **PZT (titanato de circonato de plomo)** | Contiene plomo, neurotóxico |
