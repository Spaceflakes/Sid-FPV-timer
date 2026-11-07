# Sid-FPV-timer

An open-source, 8-node FPV drone race timing board designed in KiCad 10, fully compatible with [RotorHazard](https://github.com/RotorHazard/RotorHazard).

---

## Features

- **8x RX5808 Receiver Array:** Integrated 8-channel video receiver layout with dedicated SPI tuning and filtered analog RSSI outputs.
- **Raspberry Pi Integration:** Direct header mount for Raspberry Pi 3B+ / 4 acting as the RotorHazard server.
- **Microcontrollers:** STM32F103 and ESP32-WROOM-32UE handling multi-node timing and wireless telemetry.
- **High-Power Dual Buck Regulators:** Dual Texas Instruments LM61460 (6A) synchronous step-down regulators generating ultra-clean 5V and 3.3V rails from a 2S–6S LiPo battery.
- **Protection & Power:** XT60 power connector, high-voltage reverse/transient TVS surge protection, and onboard CR2032 RTC battery backup.
- **Peripherals:** Dual fan headers with MOSFET control, onboard buzzer, PWM/addressable LED headers, and side-actuated push button.

---

## Hardware Design Files (`PCB/`)

The hardware design is located in the [`PCB/`](PCB/) directory and is designed in **KiCad 10** with self-contained symbol and footprint libraries:

- `PCB/Sid_FPV_Timer.kicad_pro` — KiCad main project file
- `PCB/Sid_FPV_Timer.kicad_sch` — Main schematic sheet
  - `PCB/mcus.kicad_sch` — STM32, ESP32, and Raspberry Pi interface
  - `PCB/power.kicad_sch` — Power distribution and LM61460 regulators
  - `PCB/sensors.kicad_sch` — 8x RX5808 receivers, button, buzzer, and LED logic
- `PCB/Sid_FPV_Timer.kicad_pcb` — Complete PCB layout and routing
- `PCB/Hex_FPV_Timer.kicad_sym` — Custom project symbols (RX5808, G-Switch, CR2032)
- `PCB/Hex_FPV_Timer.pretty/` — Custom project footprints
- `PCB/Sid_FPV_Timer.csv` — Bill of Materials (BOM)

---

## License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. See the [LICENSE](LICENSE) file for the full license text.
