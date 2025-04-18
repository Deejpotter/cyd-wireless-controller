# ESP32 Wireless Controller

## Software Requirements

### Development Environment

- Visual Studio Code
- PlatformIO IDE Extension
- Squareline Studio (optional, for UI modifications)

### Required Libraries

```ini
lib_deps =
    bodmer/TFT_eSPI@^2.5.42
    lvgl/lvgl@^8.3.6
    https://github.com/PaulStoffregen/XPT2046_Touchscreen.git
```

## 🔧 Project Structure

```
project/
├── src/
│   ├── main.cpp              # Main program logic
│   ├── wireless/
│   │   ├── esp_now.cpp      # ESP-NOW implementation
│   │   └── esp_now.h
│   ├── ui/                   # LVGL UI files
│   │   ├── ui.h
│   │   ├── ui.c
│   │   ├── ui_events.cpp
│   │   └── ui_events.h
│   └── config/              # Configuration files
├── template files/          # CYD setup files
├── platformio.ini
└── README.md
```

## ⚙️ Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/yourusername/esp32-wireless-controller.git
cd esp32-wireless-controller
```

2. Copy template files:
   - Copy `lv_conf.h` to `.pio/libdeps/cyd/lv_conf.h`
   - Copy `User_Setup.h` to `.pio/libdeps/cyd/TFT_eSPI`

3. Build and upload:

```bash
pio run --target upload
```

## 📱 Usage

1. Power on via USB-C
2. Wait for initialization
3. Calibrate touch if needed
4. Select control mode
5. Begin controlling RC car

### Control Modes

- Dual joystick mode
- Single joystick with buttons
- Custom configurations available

## 🔍 Troubleshooting

### Display Issues

- Verify template files are correctly placed
- Check TFT_eSPI configuration
- Verify pin connections

### Wireless Issues

- Check ESP-NOW configuration
- Verify MAC addresses match
- Check for interference sources

## 📚 Resources

- CYD Documentation
- LVGL Documentation
- ESP-NOW Guide
- 3D Printable Case

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
