# ⚡ Dual-Stage Power Supply (DC-DC Buck + LDO)

**Input:** 6–10V DC  
**Output 1:** 4V @ 3.5A (Buck Converter)  
**Output 2:** 2.6V @ 1.7A (LDO Regulator)  
**Design Tool:** KiCad  
**ICs:** TPS56837H (Buck), TPS7A53B (LDO)

---

## 🧩 Description

This is a compact two-stage regulated power supply. It efficiently converts a 6–10V input into two stable output voltages using a synchronous DC-DC buck converter followed by a low-noise LDO. Designed for powering sensitive analog or mixed-signal circuits.

All design steps were based on TI datasheets, layout guides, and simulation tools. Component values were calculated manually and cross-checked with online calculators.

---

## 🔧 Key Components

| Stage | IC           | Vin     | Vout  | Iout Max | Notes                        |
|-------|--------------|---------|-------|----------|------------------------------|
| Buck  | TPS56837H    | 6–10V   | 4V    | 3.5 A    | Main converter, 500 kHz      |
| LDO   | TPS7A53B     | 4V (from buck) | 2.6V | 1.7 A    | Low-noise output for analog  |

---

## 🖼️ Images

### PCB Layout (Top Layer)  
![PCB Top Layer](img/pcb_top.png)

### Schematic  
*(Insert screenshot here)*

### 3D View  
*(Insert 3D render from KiCad here)*

---

## 📐 Implementation Notes

Design follows TI layout recommendations:

- Short loop area for buck inductor-capacitor paths
- LDO input placed close to buck output, minimal trace impedance
- Wide copper traces and vias sized for 3.5 A current
- Power and analog grounds separated
- Decoupling capacitors placed tightly near IC supply pins

---

## 📁 Project Files

- `/schematic/` — KiCad schematic files  
- `/pcb/` — KiCad board layout  
- `/gerbers/` — Fabrication output files  
- `/bom/` — Bill of Materials (CSV/Excel)  
- `/pdf/` — Printable schematic and layout

---

## 🧮 Tools & Calculators Used

- [TI Webench Power Designer](https://webench.ti.com/power-designer/)
- [Voltage Divider Calculator (ChipDip)](https://www.chipdip.ru/calc/voltage-divider)
- [Trace Width Calculator (AdvancedPCB)](https://www.advancedpcb.com/en-us/tools/trace-width-calculator/)
- [Via Properties Calculator (911EDA)](https://www.911eda.com/pcb-design-calculators/via-properties-calculator/)
- [JLCPCB Capabilities](https://jlcpcb.com/capabilities/pcb-capabilities)

---

## ✅ Project Status

- [x] Schematic completed  
- [x] PCB routed (4 layers)  
- [x] BOM generated  
- [ ] Prototype ordered  
- [ ] Testing (load + thermal)  
- [ ] Oscilloscope ripple analysis

---

## 📚 References

- [TPS56837H Datasheet](https://www.ti.com/product/TPS56837H)
- [TPS7A53B Datasheet](https://www.ti.com/product/TPS7A53B)
- [KiCad Documentation](https://docs.kicad.org/)

---

> 💡 If you're an engineer reviewing this: feel free to suggest layout or thermal improvements. Project still evolving.
