# ELRS Receiver PCB (ESP8285 + SX1280) 📡

A compact **ExpressLRS (ELRS) receiver hardware design** built around **ESP8285** and the **SX1280** LoRa transceiver.
This repository contains the full **KiCad schematic and PCB layout**, along with documentation and renders.

---

## ✅ Features
- **ESP8285 MCU** (WiFi-enabled microcontroller, ELRS compatible)
- **SX1280 LoRa transceiver** for 2.4GHz ELRS
- **3.3V LDO regulation** using **MIC5219-3.3YMS**
- **Reverse polarity / input protection** using Schottky diode
- **RF output via coax / U.FL connector** support
- Status LED + reset/boot support
- Compact 2-layer PCB layout suitable for UAV / RC applications

---

## 🧩 Block Overview
### 1) MCU Section (ESP8285)
- Powered from 3.3V rail
- Boot/enable circuitry included
- UART pads/testpoints for debugging and flashing

### 2) RF Section (SX1280)
- SPI interface from ESP8285 (MISO/MOSI/SCK/CS)
- Reset and BUSY signals connected
- RF output routed to coax connector
- 52 MHz reference crystal provided

### 3) Power Section
- Input → Schottky protection → **MIC5219 3.3V LDO**
- Local decoupling capacitors placed close to ICs

---

## 📷 Project Preview
> Add your images in `docs/images/` and they will show here.

### Schematic
![Schematic](docs/images/schematic.png)

### PCB Layout
![PCB Layout](docs/images/pcb-layout.png)

---

## 📂 Repository Structure
- `hardware/kicad/` → KiCad project files (`.kicad_pro`, `.kicad_sch`, `.kicad_pcb`)
- `docs/images/` → screenshots (schematic / PCB / 3D view)
- `fabrication/` → Gerbers, drill files, BOM, pick & place (optional)

---

## ✅ Getting Started (KiCad)
1. Install **KiCad 8 / KiCad 9**
2. Open the project file:
   - `hardware/kicad/elrs_receiver.kicad_pro`
3. View schematic:
   - `elrs_receiver.kicad_sch`
4. View PCB:
   - `elrs_receiver.kicad_pcb`
5. Export Gerbers (if needed):
   - PCB Editor → **File → Plot…**

---

## ⚠️ Notes / Disclaimer
This is a personal hardware project made for learning and experimentation.  
Please validate your RF layout, matching network, and manufacturing constraints before using it in real flight systems.

---

## 👤 Author
**Prateek Sarkar**  
Embedded Systems • PCB Design (KiCad) • UAV / Robotics
