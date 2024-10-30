# 3D Printer Configuration - README

## Printer Overview
This README outlines the specifications, configurations, and components used for my 3D printer setup. Current settings are committed to serve as a backup before making further changes.

### Printer Model
- **3D Printer**: Creality (specific model unspecified)

### Controller Board
- **MCU Board**: Creality V4.2.7

### Extruder
- **Extruder Model**: Creality Sprite Direct Drive Extruder
  - **Notes**: Added direct drive for improved performance with flexible and standard filaments.

### Bed and Nozzle Specs
- **Bed Dimensions**: (specific bed dimensions not provided)
- **Nozzle Size**: (specific nozzle size not provided)
- **Z-Offset**: 1.15 (adjustable for first layer squish)

### Firmware
- **Firmware**: Klipper

### Additional Components
- **BLTouch**: Installed for automatic bed leveling
  - **Control Pin**: PB0
  - **Sensor Pin**: PB1
  - **BLTouch Offset**: X: 0, Y: 0, Z: 1.0 (customizable in config)
  
## Configurations

### Retraction Settings
- **Retraction Distance**: 0.5 - 1.0 mm (for direct drive)
- **Retraction Speed**: 25 - 45 mm/s

### Temperature Settings
- **PLA Extruder Temp**: 190 - 210°C
- **PLA Bed Temp**: 60°C

### Firmware Settings
- **Communication Interface**: USB
- **Serial Port**: `/dev/serial/by-id/usb-1a86_USB_Serial-if00-port0`
- **Restart Method**: `command`

## Slicer Settings

### Minimum Layer Time
- **Layer Time Goal**: 3 seconds (SuperSlicer configuration)

### Other Slicer Settings
- **Slicer**: SuperSlicer
- **Retraction Settings**: Adjusted for direct drive extruder with reduced retraction distance

## Troubleshooting Notes

### Common Issues
1. **Nozzle Clogging with New PLA**:
   - Possible cause: High printing temperature, try reducing to ~200°C.
   - Use cold pull technique to clean nozzle if clogging occurs.
   
2. **BLTouch Communication Loss**:
   - Verify wiring if issues persist.
   - Check configuration and ensure correct control and sensor pins.

3. **Power and Communication Issues**:
   - Ensure serial connection to `/dev/serial/by-id/usb-1a86_USB_Serial-if00-port0`.
   - Restart Klipper and power cycle as needed.

---

_Last updated: 2024-10-29_

