# ServoTester 🎛️

A compact **PWM servo motor tester** PCB designed in **KiCad 9**, built around the classic **NE555 timer IC** in astable mode. Turn the potentiometer — the servo follows.

![PCB 3D View](docs/3d_view.png)

---

## ⚙️ How It Works

The **NE555P** is configured in **astable (free-running) mode**, generating a continuous PWM signal. A potentiometer (**RV2**) adjusts the RC time constants, which changes the duty cycle of the output pulse — directly controlling the servo motor's angular position.

| PWM Pulse Width | Servo Position |
|---|---|
| ~1 ms | 0° (full left) |
| ~1.5 ms | 90° (center) |
| ~2 ms | 180° (full right) |

---

## 🔌 Connectors

| Connector | Function |
|---|---|
| **J1** (2-pin) | Power input (5V DC) |
| **J2** (3-pin) | Servo output — Signal / VCC / GND |

---

## 🧩 Bill of Materials (BOM)

| Ref | Component | Value / Part |
|---|---|---|
| U1 | Timer IC | NE555P |
| D1 | LED | Power indicator |
| D2 | Diode | 1N4148 |
| RV2 | Potentiometer | 100kΩ |
| R1 | Resistor | 1kΩ |
| R3 | Resistor | 56kΩ |
| R4 | Resistor | (see schematic) |
| C1 | Capacitor | (see schematic) |
| J1 | Connector | Conn_01x02 |
| J2 | Connector | Conn_01x03 |

---

## 📐 PCB Specifications

- **Layers:** 2 (F.Cu / B.Cu)
- **Software:** KiCad 9.0
- **Board label:** `servo motor tester`
- **Designer initials:** SEA

---

## 🚀 How to Open

1. Install **[KiCad 9](https://www.kicad.org/download/)**
2. Clone this repository:
   ```bash
   git clone https://github.com/saif-amara/ServoTester.git
   ```
3. Open `ServoTester.kicad_pro` in KiCad
4. Open schematic: `ServoTester.kicad_sch`
5. Open PCB layout: `ServoTester.kicad_pcb`

---

## 📁 Project Structure

```
ServoTester/
├── ServoTester.kicad_pro     # KiCad project file
├── ServoTester.kicad_sch     # Schematic
├── ServoTester.kicad_pcb     # PCB layout
├── .gitignore
└── README.md
```

---

## 👤 Author

**Saif Eddine Amara**  
Embedded Systems Engineering Student — ISSAT Sousse, Tunisia  
Teaching Assistant, Robotics Lab

---

## 📄 License

This project is open-source under the [MIT License](LICENSE).# ServoTester
KiCad 9 PCB design for servo tester circuit
