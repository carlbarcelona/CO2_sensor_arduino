# Arduino CO₂ Monitoring System (MQ135)

## Description

A real-time CO₂ monitoring system using an MQ135 gas sensor with Arduino. Displays CO₂ levels on an I2C LCD, logs data via Serial Plotter, and triggers alerts using LEDs and a buzzer.

## Features

* Real-time CO₂ (PPM) monitoring
* LCD display with air quality classification
* CO₂ trend tracking (increase/decrease in PPM)
* LED indicators (green = safe, red = high CO₂)
* Buzzer alert for unsafe levels
* Serial Plotter logging (time, CO₂, change)
* Sensor warm-up sequence with progress display

## Tech Stack

* Arduino (C/C++)
* MQ135 Gas Sensor
* LiquidCrystal_I2C library
* Serial communication

## Installation

```bash
# 1. Install required Arduino libraries
- LiquidCrystal_I2C
- MQ135

# 2. Connect components
- MQ135 → A0
- Buzzer → Pin 4
- Red LED → Pin 3
- Green LED → Pin 2
- I2C LCD → SDA/SCL

# 3. Upload the code to Arduino using Arduino IDE
```

## Usage

* Power on the Arduino
* Wait for sensor warm-up (progress shown on LCD)
* View CO₂ levels in PPM on LCD
* Monitor trends via Serial Plotter
* Air quality classification:

  * < 250 PPM → QUALITY
  * 250–1000 PPM → GOOD
  * 1001–2000 PPM → BAD
  * > 2000 PPM → DANGER!
* Alerts:

  * ≤1000 PPM → Green LED (Safe)
  * > 1000 PPM → Red LED + Buzzer (Warning)

## Project Structure

* main.ino → Core Arduino program for sensor reading, display, and alerts

## Future Improvements

* Add temperature & humidity compensation
* Implement data logging to SD card
* Improve CO₂ calibration accuracy
* Add wireless monitoring (WiFi/Bluetooth)

## Authors

Barcelona, Carl Sebastian E.
Lacuadra, Florence ( https://github.com/plrnz )
