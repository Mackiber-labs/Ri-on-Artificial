# Sistema de Control e IA (Unidad Central Extraíble)

## Resumen
El "cerebro" del dispositivo es una unidad sellada de microelectrónica (microcontrolador + sensores) que se aloja en una cavidad específica dentro de la silicona. Esta unidad es **extraíble** mediante un pequeño procedimiento laparoscópico, permitiendo actualizar el hardware sin cambiar el resto del órgano.

## Arquitectura Interna (Todo Integrado)

| Componente | Integración Física | Función |
| :--- | :--- | :--- |
| **Microcontrolador (STM32L / MSP430)** | Encapsulado en resina epoxy dentro de un "cartucho" de titanio. | Procesamiento de datos. |
| **Sensores (Presión, Flujo, pH)** | Montados en la pared interna del dispositivo. | Monitorean la sangre y la orina. |
| **Unidad de Comunicaciones** | Antena NFC/MICS integrada en la pared externa. | Comunicación con el exterior (diagnóstico). |
| **Actuadores (Válvulas)** | Controlados por el microcontrolador. | Apertura/cierre de la salida. |

## La Unidad Extraíble (El "Cartucho")
El microcontrolador y la electrónica compleja no están fundidos en la silicona. Están dentro de un **cartucho estanco de titanio** (tamaño de una pila AA) que se inserta en una bahía del dispositivo.

- **Acceso:** El cirujano localiza la bahía (marcada por un pequeño imán) y extrae el cartucho viejo.
- **Reemplazo:** Se inserta el cartucho nuevo (más RAM, más rápido, nuevo algoritmo de IA).
- **Sellado:** Un anillo de goma PDMS asegura la estanqueidad al insertarlo.

## Algoritmo de Control
1.  **Lectura de Sensores:** Presión (cada 1s), Flujo (cada 10s), Electrolitos (cada 1min).
2.  **Lógica de Micción:** Si presión > umbral (40 cmH₂O) **Y** no hay pico de tos/estornudo, abrir válvula.
3.  **Modo Limpieza (Nanobots):** Si el flujo baja (filtro saturado), activar compuerta de nanobots.
4.  **Glucosa (Extensión):** Si se añade el módulo de páncreas, se ejecuta un PID para liberar insulina.

## Seguridad
- **Watchdog interno:** Si el microcontrolador se cuelga, se reinicia solo.
- **Modo fallo mecánico:** Si la electrónica falla, la válvula de Nitinol tiene un modo manual (inducción externa) para vaciar la vejiga.
