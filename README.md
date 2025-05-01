# Automated-Compressor-driven-Venturi-Priming-System
# Venturi Automated Priming System Controller 🚿💨

This Arduino project automates the priming of a water pump using a Venturi system. It includes safety features such as Emergency Stop, timeout logic, buzzer alerts, and state transitions for safe operation.

## 🔧 Features

- 👆 Start, Reset, and Emergency Stop buttons
- 🚨 Buzzer alerts on timeout or Emergency Stop
- 💧 Water detection via sensor
- 🔁 Automatic transition from priming to pumping
- 🔒 Fault state for safety
- 🎚️ Slide switch to enable/disable buzzer
- 🕒 6s priming grace period; 30s total timeout

## 🧠 System States

- `IDLE`: Waiting for user to press Start
- `PRIMING`: Solenoid and compressor ON, checking for water
- `PUMPING`: Water detected; pump ON
- `FAULT`: Emergency or timeout detected

## 📦 Components

| Component          | Pin # | Notes                          |
|-------------------|-------|--------------------------------|
| Emergency Stop     | 2     | Normally closed (with pull-up) |
| Start Button       | 3     | Normally open (with pull-up)   |
| Reset Button       | 4     | Normally open (with pull-up)   |
| Water Sensor       | 5     | Pull-up enabled                |
| MCR Relay Output   | 6     | Enables main control relay     |
| Solenoid Valve     | 7     | Opens for Venturi priming      |
| Compressor         | 8     | Supplies air to Venturi        |
| Water Pump         | 9     | Activated when water detected  |
| Buzzer             | 10    | Audible alerts                 |
| Slide Switch       | 11    | Activates/deactivates buzzer   |

## 📂 Files Included

- `venturi_controller.ino` - Main Arduino sketch
- `README.md` - This file
- `.gitignore` - Optional file to exclude `*.hex`, `*.bak`, etc.

## 🚀 How to Upload to Arduino

1. Open `venturi_controller.ino` in the Arduino IDE
2. Connect your Arduino board via USB
3. Select correct board and port in **Tools**
4. Click **Upload** ✅

## 🧪 Testing Tips

- Test all buttons independently
- Simulate water detection with a pushbutton or jumper wire
- Slide switch must be **ON (LOW)** for buzzer to sound

## 📘 License

MIT License. You’re free to modify and distribute. Please credit the original author.

---

*Designed by Paul Musyoka @ Nairobi, Kenya 🇰🇪*
