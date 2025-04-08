# ⚡ Dual-Stage Power Supply (DC-DC Buck + LDO)

**Input:** 6–10V DC  
**Output 1:** 4V @ 3.5A (Buck Converter)  
**Output 2:** 2.6V @ 1.7A (LDO Regulator)  
**Design Tool:** KiCad  
**ICs:** TPS56837H (Buck), TPS7A53B (LDO)

---

## 🧩 Description

This project is a compact, efficient two-stage power supply designed for low-noise applications. It takes a 6–10V DC input and outputs two regulated voltages using a **switching regulator** followed by a **low-noise LDO**.

All stages were calculated, simulated, and implemented using:
- TI Webench for component selection
- KiCad for schematic and PCB
- Manufacturer datasheets for proper layout practices

---

## 🔧 Key Components

| Block | IC | Vin | Vout | Iout | Notes |
|------|----|-----|------|------|-------|
| Buck | TPS56837H | 6–10V | 4V | 3.5A | Synchronous buck, 500kHz |
| LDO  | TPS7A53B  | 4V    | 2.6V | 1.7A | Low-noise, for analog/digital loads |

---

## 📷 Images

### Schematic  
![Schematic](path/to/your_schematic_image.png)

### PCB Layout (Top Layer)  
![PCB](path/to/your_pcb_image.png)

### 3D View  
![3D View](path/to/your_3d_render.png)

---

## 📐 Implementation Notes

> 📌 These are based on recommendations from the datasheets and TI layout guides:

- Buck layout optimized for **short loop area** (Cin, SW, Inductor)
- LDO placed **as close as possible** to buck output with good decoupling
- Wide copper pours for high-current paths
- Ground planes separated for power and analog domains
- RC snubber not used — ripple measurements will confirm if needed

---

## 📁 Project Files

- `project_name.kicad_sch` — Schematic
- `project_name.kicad_pcb` — PCB
- `/gerbers/` — Fabrication files
- `/bom/` — Bill of Materials (CSV)
- `/pdf/` — Printable schematic and layout

---

## ✅ Status

- [x] Schematic complete  
- [x] PCB routed and 3D-checked  
- [x] BOM generated  
- [ ] Prototype ordered  
- [ ] Electrical testing  
- [ ] Ripple + thermal analysis

---

## 📚 References

- [TPS56837H Datasheet](https://www.ti.com/product/TPS56837H)
- [TPS7A53B Datasheet](https://www.ti.com/product/TPS7A53B)
- [TI Webench Power Designer](https://webench.ti.com/power-designer/)
- [KiCad Official Docs](https://docs.kicad.org/)

---
