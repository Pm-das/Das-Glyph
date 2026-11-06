# DAS GLYPH

**ESP32-C3 smartwatch prototype with a custom OLED interface.**

DAS GLYPH is a compact smartwatch prototype built around an ESP32-C3 Super Mini and a 0.96-inch 128×64 SSD1306 OLED. The firmware explores embedded C++, display graphics and animation, button-driven navigation, wireless connectivity, NTP time synchronization, and online weather data.

## Hardware

| Component | Details |
|---|---|
| Microcontroller | ESP32-C3 Super Mini |
| Display | 0.96-inch SSD1306 OLED, 128×64, I²C (address 0x3C) |
| OLED SDA | GPIO 8 |
| OLED SCL | GPIO 9 |
| Button 1 | GPIO 3 to GND |
| Button 2 | GPIO 4 to GND |

## Firmware features

- Custom boot animation and full-screen OLED UI
- Digital and analog watch faces
- Scrollable application launcher and button-driven navigation
- 12-hour clock display preference
- NTP time synchronization and local timekeeping while powered after synchronization
- Weather information from Open-Meteo
- Stopwatch, countdown timer, system information, and settings screens
- Wi-Fi connectivity for online data updates

## Repository layout

    DAS-GLYPH/
    ├── README.md
    ├── .gitignore
    ├── docs/
    │   └── PROJECT_ABSTRACT.md
    └── src/
        ├── DAS_GLYPH_v5_Gentle_Icons_12H.ino
        └── secrets.example.h

## Required libraries

Install through Arduino IDE Library Manager:

- Adafruit GFX Library
- Adafruit SSD1306
- ArduinoJson

The ESP32 Arduino core provides the Wi-Fi, HTTP, and time-related headers used by the sketch.

## Setup

1. Install the ESP32 board package in Arduino IDE and select **ESP32C3 Dev Module** (or the matching profile for your board).
2. Install the libraries listed above.
3. Copy `src/secrets.example.h` to `src/secrets.h` and enter your own Wi-Fi SSID and password.
4. Open the firmware in Arduino IDE. Keep `secrets.h` beside the sketch source when compiling. Arduino IDE may require placing the sketch in a folder with the same name as the `.ino` file.
5. Connect the OLED and buttons using the pin mapping above, then compile and upload.

## Button controls

- **Button 1:** Opens the launcher from the home screen, moves the launcher selection, or cycles an action/option inside an app.
- **Button 2:** Short press selects or performs an action; long press navigates back.

See the source comments for detailed interaction behaviour.

## Credentials and security

Wi-Fi credentials are not stored in the public firmware source. Keep your local configuration in `secrets.h`. This file is excluded by `.gitignore`; do not commit credentials or API keys.

## Project status

DAS GLYPH is an evolving personal embedded-systems prototype. Firmware features and hardware details may change as the project is tested and improved. The source in this repository has not been represented as a verified release build.

## Author

**Midhun Das P** · [GitHub @Pm-das](https://github.com/Pm-das)
