# 4.5-Asistencia-Codex-Wokwi-para-simular-practicas-Raspberry-PicoW
# Proyecto: Control de LEDs con Teclado Matricial en Raspberry Pi Pico W

## 📌 Descripción General

Este proyecto implementa un sistema de control digital utilizando un teclado matricial 4x4 para activar y desactivar un conjunto de 12 LEDs conectados a una Raspberry Pi Pico W.

Cada tecla del teclado ejecuta una acción específica, permitiendo controlar LEDs individuales o grupos de LEDs, simulando un sistema de control embebido básico.

---

## 🎯 Objetivos

* Implementar lectura de teclado matricial.
* Controlar múltiples salidas digitales (LEDs).
* Aplicar lógica de control basada en eventos.
* Integrar hardware y software en un sistema embebido.

---

## 🧠 Funcionamiento

* Cada tecla presionada en el keypad genera una señal.
* El microcontrolador interpreta la tecla.
* Se ejecuta una acción sobre uno o varios LEDs:

  * Encendido individual
  * Apagado grupal
  * Encendido grupal

---

## 🔌 Tabla de Conexiones

### LEDs

| LED   | GPIO | Descripción |
| ----- | ---- | ----------- |
| LED1  | GP11 | Número 1    |
| LED2  | GP10 | Número 2    |
| LED3  | GP9  | Número 3    |
| LED4  | GP8  | Número 4    |
| LED5  | GP7  | Número 5    |
| LED6  | GP6  | Número 6    |
| LED7  | GP5  | Número 7    |
| LED8  | GP4  | Número 8    |
| LED9  | GP3  | Letra A     |
| LED10 | GP2  | Letra B     |
| LED11 | GP28 | Letra C     |
| LED12 | GP27 | Letra D     |

Todos los LEDs están conectados a GND mediante resistencias de 220Ω.

---

### Keypad 4x4

| Tipo             | GPIO                   |
| ---------------- | ---------------------- |
| Filas (R1-R4)    | GP26, GP22, GP21, GP20 |
| Columnas (C1-C4) | GP19, GP18, GP17, GP16 |

Las filas tienen resistencias pull-up de 1kΩ conectadas a 3.3V.

---

## 🎮 Mapa de Control

| Tecla | Acción                       |
| ----- | ---------------------------- |
| 1–8   | Enciende LED correspondiente |
| 9     | Enciende LEDs 1–8            |
| 0     | Apaga LEDs 1–8               |
| A–D   | Enciende LEDs 9–12           |
| *     | Enciende LEDs 9–12           |
| #     | Apaga LEDs 9–12              |

---

## 🛠️ Tecnologías Utilizadas

* C++ (Arduino-style)
* Simulador Wokwi
* Microcontrolador RP2040

---

## ▶️ Ejecución

1. Cargar el código en la Raspberry Pi Pico W.
2. Conectar el circuito según el diagrama.
3. Presionar teclas del keypad.
4. Observar el comportamiento de los LEDs.

---

## 📷 Diagrama

El circuito fue diseñado en Wokwi usando el archivo `diagram.json`.

---

## 📌 Autor

Anderson Costa
