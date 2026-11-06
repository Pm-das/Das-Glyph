# DAS GLYPH — Project Abstract

DAS GLYPH is a compact, ESP32-C3-based smartwatch prototype designed to bring essential smartwatch functions into a small, customizable embedded device. Built around an ESP32-C3 Super Mini microcontroller and a 0.96-inch 128×64 SSD1306 OLED display, the project combines timekeeping, weather information, air-quality information, motivational quotes, and utility applications through a custom graphical user interface.

The device synchronizes its clock through the Network Time Protocol (NTP), enabling it to continue keeping time locally after synchronization while power remains available. Weather information is retrieved using the Open-Meteo service. A locally stored collection of quotes allows the random-quote screen to operate without an internet connection.

The interface includes a large digital watch face, an analog watch face, a dedicated weather screen, a random-quote screen, an animated boot sequence, and an application launcher. Utility functions include a stopwatch, countdown timer, system information, and settings. Button-based interaction, display transitions, and periodic Wi-Fi usage form part of the firmware design.

The project explores embedded programming, wireless communication, API integration, user-interface development, and real-time data handling through the creation of a functional and extensible smartwatch prototype.

## Technology stack

- Microcontroller: ESP32-C3 Super Mini
- Display: SSD1306 128×64 OLED, I²C
- Development environment: Arduino IDE
- Programming language: C/C++ (Arduino framework)
- Libraries: Adafruit GFX, Adafruit SSD1306, ArduinoJson
- Connectivity and services: Wi-Fi, NTP, Open-Meteo

## Hardware pin mapping

- OLED SDA: GPIO 8
- OLED SCL: GPIO 9
- Button 1: GPIO 3 to GND
- Button 2: GPIO 4 to GND
