# STM32-4bit-LCD-Interfacing
4-bit LCD interfacing with STM32 using HAL (GPIO)
# STM32 4-bit LCD Interfacing

## About this project

This is a simple project where I interfaced a 16x2 LCD with an STM32 microcontroller using 4-bit mode.
Instead of using all 8 data pins, I used only 4 pins to save GPIOs.

The LCD displays my name:
Swapnali
Rathod

---

## How it works

The LCD is controlled using GPIO pins.
Data is sent in two parts (4-bit each), which is why it's called 4-bit mode.

I created separate functions:

* `lcd_command()` → to send commands
* `lcd_data()` → to send data
* `lcd_string()` → to print strings

The enable pin is toggled to latch the data into the LCD.

---

## Connections used

| LCD Pin | STM32 Pin |
| ------- | --------- |
| D4      | PB10      |
| D5      | PA8       |
| D6      | PA9       |
| D7      | PC7       |
| RS      | PB6       |
| EN      | PA6       |

---
## OUTPUT

![WhatsApp Image 2026-03-29 at 9 42 58 AM](https://github.com/user-attachments/assets/e7db224f-a626-4124-a22e-3a0352cc5d4c)

---
## What I learned

* How 4-bit LCD communication works
* How to use GPIO in STM32 using HAL
* Timing requirements of LCD
* Writing reusable embedded functions

---

## Tools used

* STM32CubeIDE
* STM32 HAL Library

---

## Future improvements

* Add scrolling text
* Display sensor data
* Try I2C LCD to reduce wiring

---

## Note

This is a basic learning project, but it helped me understand how hardware interfacing works at a low level.
