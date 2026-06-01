# Microturbinas en el Uréter Artificial

## Resumen
Para garantizar la autonomía energética y eliminar la necesidad de baterías tóxicas, el dispositivo incorpora un sistema de microturbinas de flujo axial integradas en la pared del uréter artificial.

Al estar el uréter artificial conectado directamente a la salida del riñón artificial y a la vejiga, la turbina queda totalmente encapsulada dentro del "circuito hidráulico" del dispositivo. No hay partes externas.

## Diseño Integrado

| Componente | Descripción | Integración |
| :--- | :--- | :--- |
| **Ubicación** | En el interior del lumen del uréter artificial. | Totalmente interna. El uréter es una extensión de la carcasa de silicona. |
| **Rotor** | Micro-álabe de titanio o silicio (5-8 mm diámetro). | Suspensión magnética (sin fricción) para evitar trombos. |
| **Estator** | Bobina de cobre encapsulada en PDMS. | Rodea el uréter en un engrosamiento de la pared (tipo "anillo"). |
| **Salida** | Conexión directa al supercondensador. | El cableado va por el interior de la doble capa del dispositivo. |

## Funcionamiento
1.  El flujo de orina (pulsátil, 1-2 mL/min) hace girar el rotor.
2.  El movimiento del rotor en el campo magnético del estator genera una corriente eléctrica.
3.  La corriente pasa por un rectificador interno y carga el supercondensador de grafeno.

## Especificaciones Técnicas

| Parámetro | Valor | Nota |
| :--- | :--- | :--- |
| **Potencia media** | 10-30 µW | Suficiente para el modo "sleep" del microcontrolador. |
| **Pico de potencia** | 50 µW | Durante pulsos de orina (peristalsis). |
| **Caída de presión** | < 5 cmH₂O | Inapreciable para la vejiga. |
| **Biocompatibilidad** | Titanio/PDMS | No tóxico, encapsulado. |

## Ventajas de integrarlo en el uréter extraíble
- **Mantenimiento:** Si la turbina falla, se extrae junto con el riñón artificial. No queda ningún cuerpo extraño en el uréter nativo.
- **Estandarización:** Es un módulo "plug-and-play" dentro del flujo de salida.
