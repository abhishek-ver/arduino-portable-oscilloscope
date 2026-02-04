# Arduino Portable Oscilloscope
This repository documents the implementation of an **Arduino-based portable oscilloscope** using an Arduino Nano, a 128×64 OLED display, and button-based navigation.
This project is an **implementation and study** of an existing open Arduino oscilloscope design originally developed by **Noriaki Mitsunaga (2009)**.
The focus of this repository is **hardware integration, firmware execution, and documentation**, not claiming original oscilloscope design.

---

## Overview

The oscilloscope provides waveform visualization and basic signal analysis using the limited resources of the ATmega328P microcontroller. It demonstrates how real-time sampling, triggering, and signal rendering can be achieved on constrained embedded hardware.

---

## Features

- Single and dual-channel ADC sampling (A0 / A1)
- 128×64 OLED waveform display
- Button-driven menu navigation
- Adjustable time/div and voltage/div
- Trigger modes:
  - Auto
  - Normal
  - Scan
- Real-time and equivalent-time sampling
- FFT spectrum display (hardware-limited resolution)
- PWM pulse generator
- DDS waveform generator (multiple waveforms)
- Frequency counter mode

---

## Hardware Platform

Based on the referenced design:

- **Microcontroller:** Arduino Nano (ATmega328P, 16 MHz)
- **Display:** 128×64 OLED (SH1106)
- **Analog inputs:**
  - Channel 1: A0
  - Channel 2: A1
- **User input:** Push buttons using internal pull-up resistors
- **Outputs:**
  - PWM output
  - DDS waveform output
- **Power:** USB or external regulated supply via Arduino Nano
> ⚠️ **Warning**  
> The Arduino ADC input range is limited. External signal conditioning is required to prevent damage when measuring higher voltages.
---

## Performance Notes

- Sampling rate is limited by:
  - ADC conversion speed
  - CPU clock
  - Display update overhead
- FFT and frequency measurements are approximate
- Best suited for **low-frequency signals**
- Not intended to replace commercial test equipment

---

## References & Attribution

This implementation is based on prior open designs and community contributions:

- **Noriaki Mitsunaga** – Original Arduino oscilloscope design (2009)
---

