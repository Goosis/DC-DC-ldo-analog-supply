## Day 1 – March 25

- Defined system requirements: Vin = 6–10 V, Vout1 = 4 V, Iout1 = 3.5 A, Vout2, Iout2 = 2.6 V
- Chose a two-stage power topology: DC-DC buck converter followed by a low-noise LDO
- Selected components:
  - **TPS56837H** (buck converter, 6 A)
  - **TPS7A53B** (LDO regulator, 3 A)
- For **TPS56837H**:
  - Used the [TI WEBENCH Power Designer](https://webench.ti.com/) to calculate values for external components (inductor, input/output capacitors, feedback resistors)
  - Reviewed layout and footprint recommendations in the datasheet (package, thermal pad, via placement)
- For **TPS7A53B**:
  - Manually calculated the feedback resistor values using the datasheet formula:
    \[
    V_{OUT} = V_{REF} \cdot \left(1 + \frac{R_1}{R_2} \right)
    \]
    with V<sub>REF</sub> = 0.5 V
  - Selected R1 = 12.1 kΩ, R2 = 2.87 kΩ to achieve Vout ≈ 2.6 V
  - Calculated feedforward capacitor C<sub>FF</sub> ≈ 1.3 nF to place the zero around 10 kHz

## Day 2 – March 27

- **Completed schematic design** for the power system, incorporating the DC-DC buck converter (TPS56837H) followed by the LDO (TPS7A53B).
- **Recalculated component values** for a few parts based on datasheet recommendations.
  - **Updated feedback resistor values** to fine-tune the output voltage for the LDO (TPS7A53B).
  - **Validated output capacitors**: 47uF and 10uF for both input and output filters to meet the recommended capacitance values.
- **Checked for proper component placement and connections** in the schematic:
  - Verified that feedback resistors, capacitors, and power lines are connected correctly.
  - Ensured proper grounding and component orientation for thermal performance and efficiency.
  - **Fixed errors** related to component placement in the layout for power and ground planes.
- **No major issues** found in the design; proceeding with the next steps of layout design and preparation for PCB.
