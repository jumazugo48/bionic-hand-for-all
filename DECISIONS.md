# Technical Design Decisions — Bionic Hand For All

**Author:** Juan Manuel Zumel González
**Project:** Bionic Hand For All — EIDFS, San Juan, Argentina
**Last updated:** March 2026

This document records the key technical decisions made during the
development of this project, including the options evaluated and
the reasoning behind each choice.

Decisions are documented as they are made throughout the development
process.

---

## Decisión: Microcontroller selection
**Opciones evaluadas:** ESP32 (multiples formatos), Arduino o Atmega, STM32
**Elegida:** ESP32 C3 MINI
**Justificación:** Se eligió el ESP32 principalmente por su velocidad de procesamiento y reloj y su capacidad de conectividad con Wifi y Bluetooth.
Además, el modelo ESP32 C3 MINI se destaca por su tamaño y su costo, resultando conveniente para este caso.

---

## Decisión: Instrumentation amplifier selection.
**Opciones evaluadas:** AD620, INA128, INA106
**Elegida:** AD620
**Justificación:** Se eligió este IC principalmente por su bajo costo.
También, al considerar diferentes vendedores en Aliexpress es el único amplificador de este tipo que ofrecía un vendedor que simultáneamente tenía amplificadores TL074.
Además, al ver tanta información y circuitos para EMG personalizados basados en AD620 consulte su hoja de datos y determiné que era el ideal.

---

## Decisión: Actuators
**Opciones evaluadas:** Servos de bajo peso y compactos (2-8g o categoría sub-micro), MG90S, Combinación motorN20-encoderAS5600-puenteH
**Elegida:** Combinación motorN20-encoderAS5600-puenteH
**Justificación:** Esta opción es la más compacta, sin limite de giro y con suficiente torque y velocidad. Me permite complementarlo con una reducción mecánica a diferencia de un servo que al reducir y aumentar su torque pierdo rango de movimiento.

---

## Decisión: Material of the structure
**Opciones evaluadas:** PETG (impresión 3d), PLA (impr 3d), ABS (impr 3d), resina (impr 3d), fibra de carbono
**Elegida:** PETG
**Justificación:** Se destaca el PETG debido a que al imprimirse con tecnología FDM es mucho más fácil de conseguir que una de resina. Otra razón es el costo, la impresión 3d permite la producción de piezas con formas especificas que es difícil o caro de producir en fibra de carbono o metales. Además, la impresión 3d tiene un peso considerablemente bajo volviéndose en una prótesis cómoda para el usuario. El PETG es un material con una resistencia superior al PLA pero menor que el ABS compensándolo con algo de flexibilidad.

---

## Decisión: PCB manufacturing method
**Opciones evaluadas:** Impresión CNC laser, Acido y planchado con toner, fabricación por empresas (JLCPCB, PCBWay, etc)
**Elegida:** Impresión CNC laser
**Justificación:** Es preferida debido a que la producción es sin costo por maquinaria de un conocido y por ser mucho más precisa que el método tradicional con acido. La fabricación por empresas internacionales se descartó justamente por esa razon, por los costos de producción, de envío y demora de traslado. En caso de no tener al alcance un sistema CNC laser, se optaría por el método tradicional pero son el cuidado necesario para asegurar un buen resultado.

---

## Decisión: Joint joining element
**Opciones evaluadas:** Ejes impresos 3d o incluidos en la misma figura, conjunto de seguro tipo e y perno mecanizado con torno, tornillos extensibles
**Elegida:** conjunto de seguro tipo e y perno mecanizado con torno
**Justificación:** Los ejes impresos en 3d fueron rápidamente descartados por su gran rose y desgaste. Se optó por esta solución debido a que puedo elegir específicamente las dimensiones que son necesarias, su bajo costo y porque los materiales necesarios están disponibles en tiendas locales.

---

## Decisión: Morphology of the prosthesis and type of target amputation
**Elegida:** Amputación distal (a la altura de la muñeca) o desarticulación de muñeca
**Justificación:** Luego de varias entrevistas con diferentes traumatólogos de mano y especialistas llegamos a la conclusion de que orientaríamos la prótesis para amputaciones distales por su gran porcentaje de casos en comparación con otros tipos de amputación de miembro superior por debajo del nivel del codo. Al orientar la prótesis para este tipo de amputación permitiría una futura readaptación para amputaciones transradiales como las mediales o proximales.
