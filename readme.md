# ESP32 Wireless Controller (CYD)

## 🛠️ Hardware Specifications

### Core Components

- **Display Module**: JC2432W328C ESP32 Display Module
  - 2.4" TFT Display (320x240)
  - Capacitive Touch
  - ESP32-WROOM-32
  - USB-C Connection
  - JST Battery Port
  - [Maker Store CYD Display](https://www.makerstore.com.au/product/elec-esp32-2432-28r-21/)

### Power System

- **Battery**: 3.7V Li-Po Battery Pack
  - Connected via JST-PH 2.0mm connector
  - Built-in charging circuit via USB-C
  - Charge LED indicator
  - Protection circuit included
  - [Maker Store 3.7V LiPo Battery](https://www.aliexpress.com/item/1005007203936858.html)

## Software Requirements

### Development Environment

- Visual Studio Code
- PlatformIO IDE Extension
- EEZ Studio for UI development

### Required Libraries

```ini
lib_deps =
    lvgl/lvgl@^9.0.0
    bodmer/TFT_eSPI@^2.5.42
    https://github.com/PaulStoffregen/XPT2046_Touchscreen.git

```

## Project Structure

```ini
project/
├── src/
│   ├── main.cpp              # Main program logic
│   ├── wireless/
│   │   ├── esp_now.cpp      # ESP-NOW implementation
│   │   └── esp_now.h
│   ├── ui/                   # EEZ Studio UI files
│   │   ├── ui.h
│   │   ├── ui.c
│   │   ├── ui_events.cpp
│   │   └── ui_events.h
│   └── config/              # Configuration files
│       ├── pins.h           # Pin definitions
│       └── battery.h        # Battery monitoring config
├── eez/                     # EEZ Studio project files
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
5. Begin controlling RC car or whatever else

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
